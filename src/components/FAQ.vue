<template>
  <section class="w-full bg-gray-100">
    <br /><br />
    <h1 class="w-full text-3xl flex justify-center font-bold text-[#5A6D9F]">
      FAQs
    </h1>
    <div class="w-full flex justify-center ">
      <div class="wrapper-faq mt-4">
        <div class="container-faq" v-for="(faq, index) in faqs" :key="index">
          <div
            class="question"
            :class="{ active: faq.active }"
            @click="toggleAnswer(index)"
          >
            {{ faq.question }}
          </div>
          <div
            class="answercont"
            :style="{ maxHeight: faq.active ? faq.scrollHeight + 'px' : '0px' }"
            :ref="`answer-${index}`"
          >
            <p class="answer text-start" >{{ faq.answer }}<br /><br /></p>
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
      faqs: [
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
    };
  },
  computed: {
    formattedAnswer() {
      return this.faq.answer.replace(/\n/g, "<br>");
    }
  },
  methods: {
    toggleAnswer(index) {
      this.faqs[index].active = !this.faqs[index].active;
      this.$nextTick(() => {
        const refName = `answer-${index}`;
        const answerElement = this.$refs[refName];
        if (answerElement && answerElement[0]) {
          this.faqs[index].scrollHeight = answerElement[0].scrollHeight;
        } else if (answerElement) {
          this.faqs[index].scrollHeight = answerElement.scrollHeight;
        }
      });
    },
    formattedAnswer(answer) {
      return answer.replace(/\n/g, '<br>').replace(/\\u2022/g, '&bull;');
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
