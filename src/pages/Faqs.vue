<template>
  <Layout>
    <div class="faqs">
      <h2>Questions? Look Here!</h2>
      <p>Take a look and see if we're the right fit for your next project.</p>
    </div>
    <div class="accordion">
      <div v-for="(faq, index) in faqs" :key="index">
        <input type="radio" name="faqs" :id="index" class="accordion__input" />
        <label :for="index" class="accordion__label">{{ faq.question }}</label>
        <div class="accordion__content">
          <p>
            {{ faq.answer }}
          </p>
        </div>
      </div>
    </div>
  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'FAQs',
  },
  data() {
    return {
      faqs: [
        {
          question: 'Will you install parts I purchased online?',
          answer:
            "We will gladly install any parts that you show up to our shop with. While we are happy to isntall your parts we can't offer any warranty on the parts.",
        },
        {
          question: 'How long will it take to lift my truck?',
          answer:
            'Any lift project typically will take 1-3 days. The more complex the lift the closer it will take to 3 days',
        },
        {
          question: 'How long will it take to lift my truck?',
          answer:
            'Any lift project typically will take 1-3 days. The more complex the lift the closer it will take to 3 days',
        },
        {
          question: 'How long will it take to lift my truck?',
          answer:
            'Any lift project typically will take 1-3 days. The more complex the lift the closer it will take to 3 days',
        },
        {
          question: 'How long will it take to lift my truck?',
          answer:
            'Any lift project typically will take 1-3 days. The more complex the lift the closer it will take to 3 days',
        },
        {
          question: 'How long will it take to lift my truck?',
          answer:
            'Any lift project typically will take 1-3 days. The more complex the lift the closer it will take to 3 days',
        },
      ],
    };
  },
};
</script>
