<script lang="ts">
  interface Feature {
    title: string;
    description: string;
    icon: string;
    iconBg?: string;
    iconColor?: string;
  }

  export let tag = "";
  export let tagColor = "text-red-500";
  export let headline = "";
  export let description = "";
  export let features: Feature[] = [];
  export let quote: string | null = null;
</script>

<section class="py-20 bg-white">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
    <div class="mb-12">
      <div class="flex items-center gap-2 mb-4">
        <div class={`w-4 h-1 rounded-full ${tagColor.replace('text-', 'bg-')}`}></div>
        <span class={`text-sm font-semibold ${tagColor} uppercase tracking-wide`}>{tag}</span>
      </div>
      
      <h2 class="text-4xl font-bold text-gray-900 mb-6 max-w-3xl">{headline}</h2>
      <p class="text-lg text-gray-500 max-w-3xl leading-relaxed">{description}</p>
    </div>

    <!-- Features Grid -->
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-x-8 gap-y-12 mb-20">
      {#each features as feature}
        <div class="flex flex-col gap-3">
          <div class={`w-10 h-10 rounded-lg flex items-center justify-center ${feature.iconBg || 'bg-gray-50'} ${feature.iconColor || 'text-gray-600'}`}>
            {@html feature.icon}
          </div>
          <div>
            <h3 class="font-bold text-gray-900 text-sm">{feature.title}</h3>
            <p class="text-sm text-gray-500 mt-1 leading-relaxed">{feature.description}</p>
          </div>
        </div>
      {/each}
    </div>

    <!-- Image Slot -->
    <div class="mb-12 rounded-xl bg-gray-50 border border-gray-200 overflow-hidden shadow-xl">
      <slot name="image" />
    </div>

    <!-- Quote -->
    {#if quote}
      <div class="flex gap-4 max-w-4xl">
        <div class="w-1 bg-blue-500 flex-shrink-0 rounded-full"></div>
        <p class="text-lg text-gray-600 italic">{quote}</p>
      </div>
    {/if}
  </div>
</section>
