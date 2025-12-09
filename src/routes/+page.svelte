<script>
  import Header from '$lib/components/Header.svelte';
  import Hero from '$lib/components/Hero.svelte';
  import StatsGrid from '$lib/components/StatsGrid.svelte';
  import FeatureSection from '$lib/components/FeatureSection.svelte';
  import IntegrationSection from '$lib/components/IntegrationSection.svelte';
  import EngagementSection from '$lib/components/EngagementSection.svelte';
  import ComparisonTable from '$lib/components/ComparisonTable.svelte';
  import StepsSection from '$lib/components/StepsSection.svelte';
  import PricingSection from '$lib/components/PricingSection.svelte';
  import TeamSection from '$lib/components/TeamSection.svelte';
  import CTASection from '$lib/components/CTASection.svelte';
  import FAQSection from '$lib/components/FAQSection.svelte';
  import Footer from '$lib/components/Footer.svelte';
  
  import MockupFeedback from '$lib/components/MockupFeedback.svelte';
  import MockupRoadmap from '$lib/components/MockupRoadmap.svelte';
  import MockupChangelog from '$lib/components/MockupChangelog.svelte';

  const feedbackFeatures = [
    {
      title: "Upvoting & reactions",
      description: "Users vote on what they want, best ideas rise to the top",
      icon: `<svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z"/></svg>`,
      iconColor: "text-red-500",
      iconBg: "bg-red-50"
    },
    {
      title: "AI duplicate detection",
      description: "Shows similar ideas as users type, consolidating votes",
      icon: `<svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.75 17L9 20l-1 1h8l-1-1-.75-3M3 13h18M5 17h14a2 2 0 002-2V5a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/></svg>`,
      iconColor: "text-purple-500",
      iconBg: "bg-purple-50"
    },
    {
      title: "Auto-categorization",
      description: "AI automatically tags and organizes by feature area",
      icon: `<svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 7h.01M7 3h5c.512 0 1.024.195 1.414.586l7 7a2 2 0 010 2.828l-7 7a2 2 0 01-2.828 0l-7-7A1.994 1.994 0 013 12V7a4 4 0 014-4z"/></svg>`,
      iconColor: "text-blue-500",
      iconBg: "bg-blue-50"
    },
    {
      title: "Discussion threads",
      description: "Users discuss ideas, add context, and refine together",
      icon: `<svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 12h.01M12 12h.01M16 12h.01M21 12c0 4.418-4.03 8-9 8a9.863 9.863 0 01-4.255-.949L3 20l1.395-3.72C3.512 15.042 3 13.574 3 12c0-4.418 4.03-8 9-8s9 3.582 9 8z"/></svg>`,
      iconColor: "text-green-500",
      iconBg: "bg-green-50"
    },
    {
      title: "Guest & anonymous",
      description: "Let anyone submit feedback without creating an account",
      icon: `<svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z"/></svg>`,
      iconColor: "text-orange-500",
      iconBg: "bg-orange-50"
    },
    {
      title: "Private boards",
      description: "Create internal boards for sensitive customer feedback",
      icon: `<svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v4h8z"/></svg>`,
      iconColor: "text-indigo-500",
      iconBg: "bg-indigo-50"
    },
    {
      title: "Powerful search",
      description: "Semantic search finds ideas even with different wording",
      icon: `<svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"/></svg>`,
      iconColor: "text-teal-500",
      iconBg: "bg-teal-50"
    },
    {
      title: "In-app widget",
      description: "Embed feedback collection directly in your product",
      icon: `<svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 5a1 1 0 011-1h14a1 1 0 011 1v2a1 1 0 01-1 1H5a1 1 0 01-1-1V5zM4 13a1 1 0 011-1h6a1 1 0 011 1v6a1 1 0 01-1 1H5a1 1 0 01-1-1v-6zM16 13a1 1 0 011-1h2a1 1 0 011 1v6a1 1 0 01-1 1h-2a1 1 0 01-1-1v-6z"/></svg>`,
      iconColor: "text-pink-500",
      iconBg: "bg-pink-50"
    }
  ];

  const roadmapFeatures = [
    {
      title: "Status-based updates",
      description: "Roadmap auto-syncs when feedback status changes",
      icon: `<svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 4v5h.582m15.356 2A8.001 8.001 0 004.582 9m0 0H9m11 11v-5h-.581m0 0a8.003 8.003 0 01-15.357-2m15.357 2H15"/></svg>`,
      iconColor: "text-purple-500",
      iconBg: "bg-purple-50"
    },
    {
      title: "Vote visibility",
      description: "Show critical features have the most customer demand",
      icon: `<svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"/><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z"/></svg>`,
      iconColor: "text-blue-500",
      iconBg: "bg-blue-50"
    },
    {
      title: "Progress notifications",
      description: "Notify users when feedback moves between statuses",
      icon: `<svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 17h5l-1.405-1.405A2.032 2.032 0 0118 14.158V11a6.002 6.002 0 00-4-5.659V5a2 2 0 10-4 0v.341C7.67 6.165 6 8.388 6 11v3.159c0 .538-.214 1.055-.595 1.436L4 17h5m6 0v1a3 3 0 11-6 0v-1m6 0H9"/></svg>`,
      iconColor: "text-green-500",
      iconBg: "bg-green-50"
    },
    {
      title: "In-app roadmap",
      description: "Embed in your app to reduce \"when will this ship?\" tickets",
      icon: `<svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 5a1 1 0 011-1h14a1 1 0 011 1v2a1 1 0 01-1 1H5a1 1 0 01-1-1V5zM4 13a1 1 0 011-1h6a1 1 0 011 1v6a1 1 0 01-1 1H5a1 1 0 01-1-1v-6zM16 13a1 1 0 011-1h2a1 1 0 011 1v6a1 1 0 01-1 1h-2a1 1 0 01-1-1v-6z"/></svg>`,
      iconColor: "text-orange-500",
      iconBg: "bg-orange-50"
    }
  ];

  const changelogFeatures = [
    {
      title: "AI writes everything",
      description: "Writes posts, generates titles, tags, and schedules publishing",
      icon: `<svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.75 17L9 20l-1 1h8l-1-1-.75-3M3 13h18M5 17h14a2 2 0 002-2V5a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/></svg>`,
      iconColor: "text-green-500",
      iconBg: "bg-green-50"
    },
    {
      title: "Auto-pull feedback",
      description: "AI surfaces closed feedback and writes changelog entries",
      icon: `<svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 4v5h.582m15.356 2A8.001 8.001 0 004.582 9m0 0H9m11 11v-5h-.581m0 0a8.003 8.003 0 01-15.357-2m15.357 2H15"/></svg>`,
      iconColor: "text-blue-500",
      iconBg: "bg-blue-50"
    },
    {
      title: "Smart notifications",
      description: "Auto-email everyone who voted on shipped features",
      icon: `<svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 17h5l-1.405-1.405A2.032 2.032 0 0118 14.158V11a6.002 6.002 0 00-4-5.659V5a2 2 0 10-4 0v.341C7.67 6.165 6 8.388 6 11v3.159c0 .538-.214 1.055-.595 1.436L4 17h5m6 0v1a3 3 0 11-6 0v-1m6 0H9"/></svg>`,
      iconColor: "text-orange-500",
      iconBg: "bg-orange-50"
    },
    {
      title: "In-app changelog",
      description: "New update indicator appears in widget when you publish",
      icon: `<svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 5a1 1 0 011-1h14a1 1 0 011 1v2a1 1 0 01-1 1H5a1 1 0 01-1-1V5zM4 13a1 1 0 011-1h6a1 1 0 011 1v6a1 1 0 01-1 1H5a1 1 0 01-1-1v-6zM16 13a1 1 0 011-1h2a1 1 0 011 1v6a1 1 0 01-1 1h-2a1 1 0 01-1-1v-6z"/></svg>`,
      iconColor: "text-pink-500",
      iconBg: "bg-pink-50"
    }
  ];
</script>

<Header />

<main>
  <Hero />
  <StatsGrid />
  
  <div id="product">
    <FeatureSection 
      tag="Customer Feedback Platform" 
      tagColor="text-red-500"
      headline="Beautiful feedback boards where great ideas are born"
      description="Give your users a dedicated space to share ideas, vote on features they want, and see what you're building. Our AI-powered boards organize feedback automatically, detect duplicates, and help you discover what really matters to your customers."
      features={feedbackFeatures}
    >
      <div slot="image">
        <MockupFeedback />
      </div>
    </FeatureSection>

    <FeatureSection 
      tag="Product Roadmap Software" 
      tagColor="text-purple-500"
      headline="A product roadmap that updates itself automatically"
      description="Never update a spreadsheet again. Change feedback status → roadmap reflects it instantly. Show users what's coming and keep them engaged."
      features={roadmapFeatures}
      quote="Your roadmap becomes a living document that builds trust. Users see you're actively working on their requests, reducing churn and increasing engagement."
    >
      <div slot="image">
        <MockupRoadmap />
      </div>
    </FeatureSection>

    <FeatureSection 
      tag="Product Changelog Software" 
      tagColor="text-green-500"
      headline="AI-powered changelog that writes, schedules, and notifies"
      description="The most advanced changelog tool: AI writes your posts, pulls in shipped feedback, and notifies the right users automatically. Collaborate with your team and keep customers engaged—no manual work."
      features={changelogFeatures}
    >
      <div slot="image">
        <MockupChangelog />
      </div>
    </FeatureSection>
  </div>

  <IntegrationSection />
  <EngagementSection />
  <ComparisonTable />
  <StepsSection />
  <PricingSection />
  <TeamSection />
  <CTASection />
  <FAQSection />
</main>

<Footer />

