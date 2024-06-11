<template>
  <section class="w-full bg-gray-100">
    <br /><br />
    <h1 class="w-full text-3xl flex justify-center ms-4 font-extrabold text-[#5A6D9F]">
      Frequently Asked Questions
    </h1>
    <div class="w-full flex justify-center ms-4">
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
            <div class="answer text-start">{{ faq.answer }}<br /><br /></div>
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
          answer: `Click the link in the verification email from verify@codepen.io 
                     (be sure to check your spam folder or other email tabs if it's not in your inbox).
                     Or, send an email with the subject "Verify" to verify@codepen.io 
                     from the email address you use for your CodePen account.`,

          linkText: "How to Verify Email Docs",
          active: false,
          scrollHeight: 0,
        },
        {
          question: "How do I upload and sign a document?",
          answer: `It's likely an infinite loop in JavaScript that we could not catch. 
                     To fix, add ?turn_off_js=true to the end of the URL (on any page, 
                     like the Pen or Project editor, your Profile page, or the Dashboard) 
                     to temporarily turn off JavaScript. When you're ready to run the 
                     JavaScript again, remove ?turn_off_js=true and refresh the page.`,

          linkText: "How to Disable JavaScript Docs",
          active: false,
          scrollHeight: 0,
        },
      ],
    };
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
  color: orange;
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
