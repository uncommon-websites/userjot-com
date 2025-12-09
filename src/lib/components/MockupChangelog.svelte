<div class="relative bg-gray-50 h-[600px] flex flex-col overflow-hidden rounded-xl border border-gray-200">
  <!-- Header -->
  <div class="bg-white border-b border-gray-200 p-4 flex justify-between items-center">
    <div class="flex items-center gap-4">
      <div class="w-8 h-8 bg-black rounded text-white flex items-center justify-center font-bold">U</div>
      <div class="flex gap-2 text-sm text-gray-500">
        <span>/</span>
        <span class="text-gray-900 font-medium">New feature</span>
      </div>
    </div>
    <div class="flex gap-2">
       <button class="px-3 py-1.5 text-sm font-medium text-gray-600 hover:bg-gray-50 rounded border border-gray-200">Save</button>
       <button class="px-3 py-1.5 text-sm font-medium text-gray-600 hover:bg-gray-50 rounded border border-gray-200">Draft</button>
       <button class="px-3 py-1.5 text-sm font-medium text-white bg-black hover:bg-gray-800 rounded">Scheduled</button>
    </div>
  </div>

  <!-- Editor Content -->
  <div class="flex-1 bg-white p-12 max-w-3xl mx-auto w-full shadow-sm my-8 rounded-lg border border-gray-100">
    <div class="mb-6">
      <div class="inline-flex items-center px-2.5 py-0.5 rounded-full text-xs font-medium bg-purple-100 text-purple-800 mb-4">
        New feature <span class="ml-1">🔒</span>
      </div>
      <h1 class="text-4xl font-bold text-gray-900 mb-4">Control who sees your Roadmap & Changelog 🔒</h1>
      <div class="flex items-center gap-2 text-sm text-gray-500 mb-8">
        <div class="w-6 h-6 rounded-full bg-gray-200"></div>
        <span>Aaron Whitington</span>
        <span>•</span>
        <span>2 days ago</span>
      </div>
    </div>
    
    <div class="space-y-4 text-gray-600">
      <p>You can now make your Roadmap and Changelog private while keeping everything else public.</p>
      <h3 class="text-lg font-bold text-gray-900 mt-6">What's new:</h3>
      <ul class="list-disc pl-5 space-y-2">
        <li>Toggle Roadmap visibility on/off independently</li>
        <li>Toggle Changelog visibility on/off independently</li>
      </ul>
      <p class="mt-4">Why this matters: Sometimes you want to collect feedback publicly but keep your plans private. Or share your changelog but not your roadmap. Now you have full control, use UserJot however works best for your product.</p>
      
      <div class="mt-8 p-4 bg-gray-50 rounded border border-gray-200">
         <div class="h-32 bg-gray-200 rounded animate-pulse"></div>
      </div>
    </div>
  </div>

  <!-- AI Assistant Sidebar (Right) -->
  <div class="absolute right-4 top-20 w-80 bg-white rounded-xl shadow-2xl border border-gray-200 overflow-hidden">
    <div class="p-4 border-b border-gray-100 flex justify-between items-center bg-gray-50">
      <div class="font-semibold text-sm">AI assistant</div>
      <button class="text-gray-400 hover:text-gray-600" aria-label="Close assistant"><svg class="w-4 h-4" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"/></svg></button>
    </div>
    <div class="p-4 space-y-4">
      <div class="flex gap-3">
        <div class="w-8 h-8 rounded-full bg-black text-white flex items-center justify-center flex-shrink-0">AI</div>
        <div class="bg-gray-100 rounded-lg rounded-tl-none p-3 text-sm text-gray-700">
          Can you please add relevant tags to this changelog?
        </div>
      </div>
      
      <div class="flex gap-3 flex-row-reverse">
         <div class="w-8 h-8 rounded-full bg-gray-200 flex items-center justify-center flex-shrink-0">U</div>
         <div class="bg-black text-white rounded-lg rounded-tr-none p-3 text-sm">
           Sure! Based on the content, I suggest adding:
         </div>
      </div>

      <div class="flex gap-2 flex-wrap pl-11">
        <span class="px-2 py-1 bg-gray-100 border border-gray-200 rounded text-xs text-gray-600">Updating tags...</span>
        <span class="px-2 py-1 bg-gray-100 border border-gray-200 rounded text-xs text-gray-600">Done</span>
      </div>

      <div class="flex gap-3">
        <div class="w-8 h-8 rounded-full bg-black text-white flex items-center justify-center flex-shrink-0">AI</div>
        <div class="bg-gray-100 rounded-lg rounded-tl-none p-3 text-sm text-gray-700">
          I've also added "The security team satisfied users into champions who tell others about your product."
        </div>
      </div>
      
      <div class="flex gap-3">
        <div class="w-8 h-8 rounded-full bg-black text-white flex items-center justify-center flex-shrink-0">AI</div>
        <div class="bg-gray-100 rounded-lg rounded-tl-none p-3 text-sm text-gray-700">
          Would you like me to add or remove any other tags (bug fix, documentation, new feature, performance)?
        </div>
      </div>

      <button class="w-full bg-black text-white rounded py-2 text-sm font-medium mt-2">Schedule this post for tomorrow morning please.</button>
      
      <div class="flex gap-2 justify-center">
         <div class="w-2 h-2 rounded-full bg-gray-300 animate-bounce"></div>
         <div class="w-2 h-2 rounded-full bg-gray-300 animate-bounce delay-100"></div>
         <div class="w-2 h-2 rounded-full bg-gray-300 animate-bounce delay-200"></div>
      </div>
    </div>
  </div>
</div>
