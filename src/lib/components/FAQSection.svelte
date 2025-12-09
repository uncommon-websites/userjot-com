<script lang="ts">
  let openIndex: number | null = null;

  const faqs = [
    { question: "How quickly can I start collecting feedback?", answer: "You can be up and running in less than 30 seconds. Just create an account and share your link." },
    { question: "Can I customize the feedback experience?", answer: "Yes, you can customize the colors, branding, and domain to match your product." },
    { question: "What if I receive too much feedback?", answer: "UserJot has built-in tools to help you organize, filter, and prioritize feedback so you don't get overwhelmed." },
    { question: "How does UserJot help me prioritize user feedback?", answer: "You can sort by votes, date, or status. You can also see which users are requesting which features." },
    { question: "Can UserJot help reduce customer churn?", answer: "Yes, by showing users that you are listening and building what they want, you increase their loyalty and reduce churn." },
    { question: "Is UserJot suitable for SaaS companies?", answer: "Absolutely. UserJot is built specifically for SaaS teams." },
    { question: "Can I use UserJot as a product roadmap software?", answer: "Yes, UserJot includes a fully functional roadmap that syncs with your feedback board." },
    { question: "Does UserJot offer feedback tracking?", answer: "Yes, you can track the status of every piece of feedback from 'Pending' to 'Completed'." },
    { question: "Can I create a product changelog with UserJot?", answer: "Yes, UserJot has a built-in changelog feature that lets you publish updates to your users." },
    { question: "How can UserJot improve customer experience management?", answer: "By providing a transparent and easy way for customers to give feedback, you improve their overall experience." },
    { question: "Does UserJot support guest or anonymous feedback?", answer: "Yes, you can allow users to submit feedback without creating an account." },
    { question: "Can I customize UserJot to match my brand?", answer: "Yes, you can add your logo, change colors, and use your own domain." },
    { question: "What integrations does UserJot offer?", answer: "We integrate with tools like Slack, Discord, Linear, Jira, and GitHub." }
  ];

  function toggle(index: number) {
    openIndex = openIndex === index ? null : index;
  }
</script>

<section id="help" class="py-20 bg-white">
  <div class="max-w-3xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="mb-12">
      <h2 class="text-3xl font-bold text-gray-900 mb-4">Frequently asked questions</h2>
      <p class="text-gray-500">Everything you need to know about customer feedback management and how UserJot helps you build better products.</p>
    </div>

    <div class="divide-y divide-gray-100 border-t border-gray-100">
      {#each faqs as faq, i}
        <div class="py-4">
          <button 
            class="w-full flex justify-between items-center text-left focus:outline-none group"
            on:click={() => toggle(i)}
          >
            <span class="text-sm font-medium text-gray-900 group-hover:text-gray-600 transition-colors">{faq.question}</span>
            <span class="ml-6 flex-shrink-0">
              <svg class={`w-4 h-4 text-gray-400 transform transition-transform ${openIndex === i ? 'rotate-180' : ''}`} fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
              </svg>
            </span>
          </button>
          {#if openIndex === i}
            <div class="mt-2 pr-12">
              <p class="text-sm text-gray-500">{faq.answer}</p>
            </div>
          {/if}
        </div>
      {/each}
    </div>
  </div>
</section>
