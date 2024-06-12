<template>
  <section class="w-full bg-gray-100">
    <br /><br />
    <h1 class="w-full text-3xl flex justify-center font-bold text-[#5A6D9F]">FAQs</h1>
    <br />
    <div class="flex flex-wrap">
      <div class="w-full">
        <ul class="flex mb-0 list-none w-1/4 justify-center mx-auto pt-3 pb-4">
          <li
            class="-mb-px last:mr-0 flex-auto text-center"
            v-for="tab in tabs"
            :key="tab.id"
          >
            <a
              class="text-sm font-bold uppercase py-3 rounded shadow-lg block leading-normal cursor-pointer"
              @click="openTab = tab.id"
              :class="
                openTab === tab.id ? 'text-white bg-primary-color' : 'text-black bg-white'
              "
            >
              <!-- <iconify-icon v-if="tab.icon" :icon="tab.icon" :class="tab.icon + 'absolute mr-1 '"></iconify-icon>  -->
              {{ tab.name }}
            </a>
          </li>
        </ul>

        <div class="relative flex flex-col min-w-0 break-words w-full mb-6 rounded">
          <div class="px-4 py-5 flex-auto">
            <div class="tab-content tab-space">
              <!-- English FAQ -->
              <div v-show="openTab === 1">
                <div class="w-full flex justify-center">
                  <div class="wrapper-faq mt-4">
                    <div
                      class="container-faq"
                      v-for="(faq, index) in faqs_en"
                      :key="`en-${index}`"
                    >
                      <div
                        class="question"
                        :class="{ active: faq.active }"
                        @click="toggleAnswer(index, 'en')"
                      >
                        {{ faq.question }}
                      </div>
                      <div
                        class="answercont"
                        :style="{
                          maxHeight: faq.active ? faq.scrollHeight + 'px' : '0px',
                        }"
                        :ref="`answer-en-${index}`"
                      >
                        <p class="answer text-start">{{ faq.answer }}<br /><br /></p>
                      </div>
                    </div>
                  </div>
                </div>
              </div>

              <!-- Myanmar FAQ -->
              <div v-show="openTab === 2">
                <div class="w-full flex justify-center">
                  <div class="wrapper-faq mt-4">
                    <div
                      class="container-faq"
                      v-for="(faq, index) in faqs_mm"
                      :key="`mm-${index}`"
                    >
                      <div
                        class="question"
                        :class="{ active: faq.active }"
                        @click="toggleAnswer(index, 'mm')"
                      >
                        {{ faq.question }}
                      </div>
                      <div
                        class="answercont"
                        :style="{
                          maxHeight: faq.active ? faq.scrollHeight + 'px' : '0px',
                        }"
                        :ref="`answer-mm-${index}`"
                      >
                        <p class="answer text-start">{{ faq.answer }}<br /><br /></p>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "FAQ",
  data() {
    return {
      openTab: 1,
      tabs: [
        { id: 1, name: "EN", icon: "flag:us-4x3" },
        {
          id: 2,
          name: "MM",
          imgSrc:
            "https://upload.wikimedia.org/wikipedia/commons/thumb/1/10/Flag_of_Myanmar_%281974%E2%80%932010%29.svg/2560px-Flag_of_Myanmar_%281974%E2%80%932010%29.svg.png",
        },
      ],
      faqs_en: [
        {
          question: "How secure are my documents?",
          answer:
            "We use advanced encryption protocols to ensure your documents are safe and secure. All data is encrypted during transit and at rest, making it virtually impossible for unauthorized parties to access your sensitive information.",
          linkText: "How to Verify Email Docs",
          active: false,
          scrollHeight: 0,
        },
        {
          question: "How do I upload and sign a document?",

          answer: `Uploading and signing a document is simple:\n\u2022 Upload your document in PDF format.\n\u2022 Add signature fields where needed.\n\u2022 Send the document to recipients for signing.\n\u2022 Receive the signed document back in your Google mail account.`,
          active: false,
          scrollHeight: 0,
        },
        {
          question: "What types of documents can I sign?",
          answer:
            "You can sign a wide variety of documents including contracts, agreements, NDAs, invoices, and more. Our service supports PDF files, which is the standard format for digital signatures",
          linkText: "How to Verify Email Docs",
          active: false,
          scrollHeight: 0,
        },
        {
          question: "Can I track the status of my documents?",
          answer:
            "Yes, our service provides real-time tracking and status updates for your documents. You can see when a document has been viewed, signed, or sent, allowing you to stay informed throughout the entire signing process.",
          linkText: "How to Verify Email Docs",
          active: false,
          scrollHeight: 0,
        },
        {
          question: `How many pages can my PDF document have for signing?`,
          answer:
            "You can upload and sign PDF documents with up to 50 pages. This allows you to handle lengthy contracts, agreements, and other extensive documents without any issues.",
          linkText: "How to Verify Email Docs",
          active: false,
          scrollHeight: 0,
        },
        {
          question: "What is the maximum file size for uploading documents?",
          answer:
            "Our platform supports uploading PDF files up to 50 MB in size. This ensures you can upload high-quality documents without worrying about file size limitations.",
          linkText: "How to Verify Email Docs",
          active: false,
          scrollHeight: 0,
        },
        {
          question: "Can multiple people sign the same document?",
          answer:
            "Yes, our service supports multiple signers on a single document. You can easily add multiple recipients and specify the order in which they should sign, ensuring a smooth and efficient signing process for all parties involved.",
          linkText: "How to Verify Email Docs",
          active: false,
          scrollHeight: 0,
        },
        {
          question: "Do we need to sign our signatures again and again?",
          answer:
            "No, you don’t need to sign multiple times. You can add your handwritten signature by uploading it in JPEG or PNG file format, or, you can draw and save your signature in your account by using ‘Draw’ function in GENI SIGN.",
          linkText: "How to Verify Email Docs",
          active: false,
          scrollHeight: 0,
        },
        {
          question: "How can I set the signing area on the paper?",
          answer:
            "When you reach the step of preparing document after choosing recipients, you can set your signing area by dragging content blocks from right sidebar.",
          linkText: "How to Verify Email Docs",
          active: false,
          scrollHeight: 0,
        },
      ],
      faqs_mm: [
        {
          question: "ကျွန်ုပ်တို့ စာရွက်စာတမ်းတွေ ဘယ်လောက်လုံခြုံမှုရှိလဲ",
          answer: `လူကြီးမင်းတို့ စာရွက်စာတမ်းတွေ လုံခြုံမှုအပြည့်ရှိဖို့အတွက် အဆင့်မြင့် encryption protocols ကိုအသုံးပြုထားပါတယ်
                    ဒေတာများအားလုံးကို အကူးအပြောင်းလုပ်နေချိန်နဲ့ ကျန်အချိန်များမှာ encrypted လုပ်ထားတာကြောင့် ခွင့်ပြုချက်မရှိသောသူများမှ လူကြီးမင်းတို့၏အရေးကြီးသော အချက်အလက်များကို ဝင်ရောက်ကြည့်ရှု၍မရနိုင်ပါ
                    s`,
          active: false,
          scrollHeight: 0,
        },
        {
          question: "စာရွက်စာတမ်းတစ်ခုကို လက်မှတ်ထိုးမယ်ဆို ဘာကစလုပ်ရမလဲ",
          answer: `စာရွက်စာတမ်းတင်ပြီး လက်မှတ်ထိုးရတဲ့ လုပ်ငန်းစဉ်ကလွယ်ကူပါတယ်
					\n\u2022 အရင်ဆုံးလက်မှတ်ထိုးမည့် စာရွက်စာတမ်းကို pdf format နဲ့ တင်ရပါမယ်
					\n\u2022 စာရွက်ပေါ်မှာ လက်မှတ်ရေးထိုးမည့်နေရာတွေကို သတ်မှတ်ပေးရပါမယ်
					\n\u2022 လက်မှတ်ထိုးမည့် သက်ဆိုင်တဲ့သူတွေဆီ ပေးပို့ပါ
					\n\u2022 လက်မှတ်ထိုးပြီးသား စာရွက်စာတမ်းတွေကို လူကြီးမင်းတို့ရဲ့ google mail account ထဲမှာ ပြန်လည်ရရှိမှာဖြစ်ပါတယ်`,
          linkText: "How to Verify Email Docs",
          active: false,
          scrollHeight: 0,
        },
        {
          question: " ဘယ်လို စာရွက်စာတမ်းအမျိုးအစားတွေ လက်မှတ်ထိုးလို့ရမလဲ",
          answer: `ကျွန်ုပ်တို့ GENI Sign မှာ စာချုပ်များ၊ သဘောတူညီချက်များ၊ ပါဝင်သူကလွဲပြီး အခြားသူများသိလို့မရတဲ့ လျှို့ဝှက်သဘောတူစာချုပ်များ၊ ငွေတောင်းခံလွှာများစတာတွေအပြင် လိုအပ်တဲ့စာရွက်စာတမ်းများစွာကိုလည်း လက်မှတ်ထိုးနိုင်ပါတယ်
                    File တွေကိုတော့ ဒစ်ဂျစ်တယ်လက်မှတ်တွေအတွက် စံသတ်မှတ်ထားတဲ့ Portable Document Format(pdf) ကို support ပေးထားပါတယ်`,
          linkText: "How to Verify Email Docs",
          active: false,
          scrollHeight: 0,
        },
        {
          question: "ကျွန်ုပ်တို့ စာရွက်စာတမ်းတွေရဲ့ အခြေအနေတွေရော သိနိုင်မလား",
          answer:
            "ဟုတ်ကဲ့ သိနိုင်ပါတယ်၊ ကျွန်ုပ်တို့ GENI Sign မှာဆိုရင် ပို့လိုက်တဲ့ စာရွက်စာတမ်း ရောက်သွားပြီလား၊ လက်ခံမည့်သူဘက်က ဖွင့်ကြည့်ပြီးပြီလား၊ လက်မှတ်ထိုးပြီးပြီလား စတဲ့ စာရွက်စာတမ်းရဲ့ အခြေအနေတွေကို အချိန်နဲ့တပြေးညီ အသိပေးမှာဖြစ်ပါတယ်",
          linkText: "How to Verify Email Docs",
          active: false,
          scrollHeight: 0,
        },
        {
          question:
            "လက်မှတ်ထိုးဖို့အတွက် စာရွက်စာတမ်း (PDF File) တစ်ခုမှာ စာမျက်နှာဘယ်လောက်အထိ ပါလို့ရလဲ",
          answer:
            "စာမျက်နှာအရွက် (၅၀) အထိတင်ပြီး လက်မှတ်ထိုးလို့ရတာမလို့ ရှည်လျားတဲ့ စာချုပ်စာတမ်းတွေ၊ သဘောတူညီချက်တွေနဲ့ အခြားအရေးကြီးစာရွက်စာတမ်းမှန်သမျှကို အခက်အခဲမရှိ လက်မှတ်ရေးထိုးနိုင်မှာဖြစ်ပါတယ်",
          active: false,
          scrollHeight: 0,
        },
        {
          question: "စာရွက်စာတမ်းတစ်ခုကို File Size အကြီးဆုံးဘယ်လောက်ထိတင်လို့ရမလဲ",
          answer:
            "စာရွက်စာတမ်းတစ်ခုကို 50MB ထိတင်ခွင့်ပေးထားပါတယ်၊ ဒါကြောင့်မလို့ File Size အတွက်ကို စိတ်ပူစရာမလိုပဲ အရည်အသွေးမြင့် ကြည်လင်တဲ့ စာရွက်စာတမ်းတွေကို အသုံးပြုနိုင်မှာဖြစ်ပါတယ်",
          active: false,
          scrollHeight: 0,
        },
        {
          question: "စာရွက်စာတမ်းတစ်ခုထဲမှာ လူအများကြီးထိုးလို့ရနိုင်လား",
          answer:
            "ဟုတ်ကဲ့ ရပါတယ်၊ ကျွန်ုပ်တို့ GENI Sign ဟာဆိုရင် စာရွက်စာတမ်းတစ်ခုထဲမှာ လက်မှတ်ထိုးဖို့ လိုအပ်သူအကုန် အသုံးပြုလို့ရအောင် support ပေးထားပါတယ်၊ လက်မှတ်ထိုးဖို့ လက်ခံရရှိမည့်လူကို အလွယ်တကူထပ်ထည့်နိုင်ပြီး ဘယ်သူပြီးမှဘယ်သူရေးထိုးရမယ်ဆိုတဲ့ အစဉ်လိုက်လည်း သတ်မှတ်လို့ရတာမလို့ ပါဝင်တဲ့သူအကုန် ချောချောမွေ့မွေ့နဲ့ တိကျသေချာစွာ လက်မှတ်ရေးထိုးနိုင်မှာဖြစ်ပါတယ်",
          active: false,
          scrollHeight: 0,
        },
        {
          question: "ကျွန်ုပ်တို့လက်မှတ်တွေက အကြိမ်ကြိမ်ရေးထိုးရမှာလား",
          answer:
            "အကြိမ်ကြိမ်ရေးထိုးနေစရာမလိုပါ၊ လူကြီးမင်းတို့ရဲ့ ကိုယ်ပိုင်အကောင့်ထဲမှာ ထိုးမြဲလက်မှတ်တစ်ခုကို JPEG or PNG File ပုံစံဖြင့်တင်ထားခြင်း သို့မဟုတ် website ထဲက Draw function ကိုအသုံးပြုပြီး လူကြီးမင်းတို့လက်မှတ်ကို‌ တစ်ကြိမ်ရေးထိုးပြီးသိမ်းထားရုံဖြင့် အလွယ်တကူပြန်လည်အသုံးပြုနိုင်မှာဖြစ်ပါတယ်",
          active: false,
          scrollHeight: 0,
        },
        {
          question: "စာရွက်ပေါ်မှာ လက်မှတ်ရေးထိုးမည့်နေရာတွေကို ဘယ်လိုသတ်မှတ်ရမလဲ",
          answer:
            "စာရွက်စာတမ်းလက်ခံရရှိမည့်သူ‌ကိုရွေးချယ်ပြီး စာရွက်စာတမ်းပြင်ဆင်သည့်အဆင့်ရောက်တဲ့အခါ ညာဘက်ခြမ်းမှာရှိတဲ့ Content Blocks လေးတွေထဲမှ လိုတာကိုဆွဲပြီး လူကြီးမင်းတို့ လက်မှတ်ရေးထိုးလိုတဲ့နေရာကို သတ်မှတ်ပေးလို့ရပါတယ်",
          active: false,
          scrollHeight: 0,
        },
      ],
    };
  },
  computed: {
    formattedAnswer() {
      return this.faq.answer.replace(/\n/g, "<br>");
    },
  },
  methods: {
    toggleAnswer(index, language) {
      let faqArray = this.faqs_en;
      if (language === "mm") {
        faqArray = this.faqs_mm;
      }
      console.log(index);
      faqArray[index].active = !faqArray[index].active;
      this.$nextTick(() => {
        const refName = `answer-${language}-${index}`;
        const answerElement = this.$refs[refName];
        console.log(answerElement);
        if (answerElement && answerElement[0]) {
          faqArray[index].scrollHeight = answerElement[0].scrollHeight;
        } else if (answerElement) {
          faqArray[index].scrollHeight = answerElement.scrollHeight;
        }
      });
    },
    toggleTabs(tabNumber) {
      this.openTab = tabNumber;
    },
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Lato:400,400i,700");

* {
  font-family: Lato, sans-serif;
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

.wrapper-faq {
  width: 60%;
}

h1 {
  margin-bottom: 20px;
}

.container-faq {
  background-color: white;
  color: black;
  border-radius: 20px;
  box-shadow: 0 5px 6px 0 rgb(0, 0, 0, 0.2);
  margin: 20px 0;
}

.question {
  font-size: 1.2rem;
  font-weight: 400;
  padding: 20px 80px 20px 20px;
  position: relative;
  display: flex;
  align-items: center;
  cursor: pointer;
}

.question::after {
  content: "\002B";
  color: #5a6d9f;
  font-size: 2.2rem;
  position: absolute;
  right: 20px;
  transition: 0.2s;
}

.question.active::after {
  transform: rotate(45deg);
}

.answercont {
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.3s ease-out;
}

.answer {
  padding: 0 20px 20px;
  line-height: 1.5rem;
}

@media screen and (max-width: 790px) {
  html {
    font-size: 14px;
  }

  .wrapper-faq {
    width: 80%;
  }
}
</style>
