<template>
  <Layout>
    <div class="intro container">
      <div class="intro__img">
        <g-image src="~/assets/imgs/twin-trans.jpg" width="700" />
      </div>

      <div class="intro__content">
        <h2>You'll have a hard time wiping that smile off your face</h2>
        <p>
          For the last 25 years we have been building engines, restoring classic
          cars, lifting trucks and Jeeps. Whatever vision you have for your car,
          here are Cruisers we can make that happen.
        </p>

        <g-link class="btn btn--primary">Schedule A Free Consultation</g-link>
      </div>
    </div>

    <div class="numbers">
      <h4>Over the past <span class="underline">25 years</span> we have...</h4>

      <div class="numbers__container">
        <div class="number" v-for="(number, index) in numbers" :key="index">
          <p>
            <span class="counter" :data-target="number.number">0</span
            ><span>+</span>
            <br />
            {{ number.action }}
          </p>
        </div>
      </div>
    </div>

    <div class="about">
      <g-image class="about__img" src="~/assets/imgs/about-land.jpg" />

      <h4 class="underline">Our Story</h4>

      <p>
        Give a call to the shop, and you are likely to hear the greeting
        “Cruisers Motorsports, Bob speaking.” This salutation is like gold to
        muscle car owners throughout the area, because they know they have
        reached the one guy, the best guy, to fix whatever ails their pride and
        joy.
      </p>
      <p>
        Ever since he can remember, Bob Schmus, owner of Cruisers Motorsports,
        has been a motor-head. In his early days he was souping up go carts and
        dirt bikes, and he quickly moved on to street rides and the race track.
        At 16, he was working on drag race motors and in 1987 Bob opened Custom
        Car Care completing restorations and performance and competition engine
        building and conversions, including a national show winner in his first
        year in business. By the time he was eighteen, Bob was the go-to guy for
        complete motor builds on some of the meanest rides in Connecticut. When
        stock car legend Evie Pierce decided to come out of retirement after 25
        years, he turned to Bob for his IMCA modified engine, which won the
        championship up at the old Sullivan County Speedway track, a quarter
        mile loop now know as Bethel Motor Speedway.
      </p>
      <p>
        Bob But he knew that in order to be a success he needed to understand
        all aspects of the business, so after five years, including one year as
        crew chef for Bill Mitchell special vehicle development. He went to
        school at University of Miami earning a degree in Business
        Administration. Before the diploma was even printed, Bob had his next
        business constructed, and immediately after graduation, he moved back to
        Connecticut and opened Cruisers in April, 1995. In addition to being a
        top notch car guy, Bob has been an independent business owner and an
        entrepreneur his entire life, and has never once looked back.
      </p>
    </div>
  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'Our Story',
  },
  data() {
    return {
      numbers: [
        { number: '600', action: 'Engines Built' },
        { number: '500', action: 'Trucks Lifted' },
        { number: '125', action: 'Classics Restored' },
        { number: '5000', action: 'Happy Customers' },
      ],
    };
  },
  methods: {
    count() {
      const counters = document.querySelectorAll('.counter');
      const speed = 20; // The lower the slower

      counters.forEach(counter => {
        const updateCount = () => {
          const target = +counter.getAttribute('data-target');
          const count = +counter.innerText;

          // Lower inc to slow and higher to slow
          const inc = target / speed;

          // Check if target is reached
          if (count < target) {
            // Add inc to count and output in counter
            counter.innerText = Math.ceil(count + inc);
            // Call function every ms
            setTimeout(updateCount, 40);
          } else {
            counter.innerText = target;
          }
        };

        updateCount();
      });
    },
  },
  mounted() {
    this.count();
  },
};
</script>
