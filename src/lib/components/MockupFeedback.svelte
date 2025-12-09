<div class="relative bg-gray-50 h-[600px] flex">
  <!-- Sidebar (Blurred/Faded) -->
  <div class="w-64 bg-white border-r border-gray-200 flex flex-col flex-shrink-0 opacity-50">
    <div class="p-4 border-b border-gray-100">
      <div class="flex items-center gap-2">
        <div class="w-6 h-6 bg-black rounded text-white flex items-center justify-center text-xs font-bold">U</div>
        <div class="text-sm font-semibold">UserJot</div>
      </div>
    </div>
    <div class="p-3">
      <div class="w-full h-8 bg-gray-100 rounded mb-4"></div>
      <div class="space-y-2">
        <div class="h-6 bg-gray-100 rounded w-3/4"></div>
        <div class="h-6 bg-gray-100 rounded w-1/2"></div>
        <div class="h-6 bg-gray-100 rounded w-2/3"></div>
      </div>
    </div>
  </div>

  <!-- Main Content (Blurred/Faded) -->
  <div class="flex-1 bg-white opacity-50 p-8">
    <div class="h-8 bg-gray-100 rounded w-1/3 mb-6"></div>
    <div class="space-y-4">
      <div class="h-24 bg-gray-50 border border-gray-100 rounded p-4"></div>
      <div class="h-24 bg-gray-50 border border-gray-100 rounded p-4"></div>
    </div>
  </div>

  <!-- Modal (Center Stage) -->
  <div class="absolute inset-0 flex items-center justify-center pointer-events-none">
    <div class="bg-white rounded-xl shadow-2xl border border-gray-200 w-[600px] max-w-full m-4 pointer-events-auto overflow-hidden">
      <div class="p-6">
        <div class="flex justify-between items-start mb-4">
          <div class="flex gap-4">
            <div class="w-12 h-12 rounded-lg bg-gray-100 flex items-center justify-center text-2xl">👾</div>
            <div>
              <h3 class="text-xl font-bold text-gray-900">Github Integration</h3>
              <div class="flex gap-2 mt-1">
                <button class="text-gray-400 hover:text-gray-600" aria-label="Edit"><svg class="w-4 h-4" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15.232 5.232l3.536 3.536m-2.036-5.036a2.5 2.5 0 113.536 3.536L6.5 21.036H3v-3.572L16.732 3.732z"/></svg></button>
                <button class="text-gray-400 hover:text-gray-600" aria-label="Flag"><svg class="w-4 h-4" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16"/></svg></button>
                <button class="text-gray-400 hover:text-gray-600" aria-label="More options"><svg class="w-4 h-4" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 5v.01M12 12v.01M12 19v.01M12 6a1 1 0 110-2 1 1 0 010 2zm0 7a1 1 0 110-2 1 1 0 010 2zm0 7a1 1 0 110-2 1 1 0 010 2z"/></svg></button>
              </div>
            </div>
          </div>
          <button class="text-gray-400 hover:text-gray-600" aria-label="Close modal">
            <svg class="w-5 h-5" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"/></svg>
          </button>
        </div>

        <p class="text-gray-600 mb-6 leading-relaxed">
          Would be cool to integrate Github and have UserJot propose writing an Update based on the changes in the repo. Would save a ton of time and honestly be a lot more descriptive of what behavior has changed/has been added.
        </p>

        <div class="flex items-center gap-3 mb-6">
          <div class="w-8 h-8 rounded-full bg-purple-100 flex items-center justify-center text-purple-600 text-xs font-bold">AW</div>
          <div>
            <div class="text-sm font-medium text-gray-900">Aaron Whitington</div>
            <div class="text-xs text-gray-500">2 days ago</div>
          </div>
          <div class="ml-auto flex gap-3 text-sm text-gray-500">
            <div class="flex items-center gap-1">💬 1</div>
            <div class="flex items-center gap-1">❤️ 2</div>
          </div>
        </div>

        <div class="border-b border-gray-200 mb-4">
          <div class="flex gap-6">
            <button class="pb-2 border-b-2 border-black font-medium text-sm">Comments</button>
            <button class="pb-2 border-b-2 border-transparent text-gray-500 hover:text-gray-700 font-medium text-sm">Reactions</button>
            <button class="pb-2 border-b-2 border-transparent text-gray-500 hover:text-gray-700 font-medium text-sm">Details</button>
          </div>
        </div>

        <div class="relative mb-6">
          <textarea class="w-full border border-gray-200 rounded-lg p-3 text-sm focus:outline-none focus:ring-1 focus:ring-gray-300 resize-none h-24" placeholder="Write a comment..."></textarea>
          <button class="absolute bottom-3 right-3 bg-black text-white text-xs px-3 py-1.5 rounded-md font-medium">Submit</button>
        </div>

        <div class="flex gap-3">
           <div class="w-8 h-8 rounded-full bg-green-100 flex items-center justify-center text-green-600 text-xs font-bold shrink-0">ST</div>
           <div>
             <div class="flex items-baseline gap-2">
               <span class="text-sm font-medium text-gray-900">Shayan Taslim</span>
               <span class="text-xs text-gray-500">Just now</span>
             </div>
             <p class="text-sm text-gray-600 mt-1">Love this idea! Adding it to the roadmap.</p>
             <p class="text-sm text-gray-600 mt-1">Quick question: would you want to pick specific PRs/commits to generate from, or should it auto-detect changes since your last post?</p>
           </div>
        </div>
      </div>
    </div>
  </div>
</div>
