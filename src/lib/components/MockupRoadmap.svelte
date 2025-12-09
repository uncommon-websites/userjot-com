<div class="bg-gray-50 h-[600px] flex flex-col overflow-hidden rounded-xl border border-gray-200">
  <!-- Header -->
  <div class="bg-white border-b border-gray-200 p-4 flex justify-between items-center">
    <div class="font-bold text-lg">Roadmap</div>
    <div class="flex gap-2">
       <div class="w-8 h-8 rounded-full bg-gray-200"></div>
       <div class="w-8 h-8 rounded-full bg-gray-200"></div>
    </div>
  </div>

  <!-- Kanban Board -->
  <div class="flex-1 overflow-x-auto p-6">
    <div class="flex gap-6 h-full">
      
      <!-- Column 1: Under Review -->
      <div class="w-72 flex-shrink-0 flex flex-col gap-3">
        <div class="flex items-center justify-between mb-1">
          <div class="flex items-center gap-2 font-medium text-sm text-gray-700">
            <div class="w-2 h-2 rounded-full bg-yellow-400"></div>
            Under Review
            <span class="bg-gray-200 text-gray-600 px-1.5 py-0.5 rounded text-xs">13</span>
          </div>
          <button class="text-gray-400 hover:text-gray-600">+</button>
        </div>

        <!-- Card 1 -->
        <div class="bg-white p-3 rounded shadow-sm border border-gray-200 cursor-pointer hover:shadow-md transition-shadow">
          <div class="text-sm font-medium text-gray-900 mb-2">Sort and Display by Most Recent Reply</div>
          <div class="flex items-center gap-3 text-xs text-gray-400">
            <div class="flex items-center gap-1">💬 2</div>
            <div class="flex items-center gap-1">❤️ 1</div>
          </div>
        </div>

        <!-- Card 2 -->
        <div class="bg-white p-3 rounded shadow-sm border border-gray-200 cursor-pointer hover:shadow-md transition-shadow">
          <div class="text-sm font-medium text-gray-900 mb-2">Outseta Integration</div>
          <div class="flex items-center gap-3 text-xs text-gray-400">
            <div class="flex items-center gap-1">💬 2</div>
            <div class="flex items-center gap-1">❤️ 1</div>
          </div>
        </div>

        <!-- Card 3 -->
        <div class="bg-white p-3 rounded shadow-sm border border-gray-200 cursor-pointer hover:shadow-md transition-shadow">
          <div class="text-sm font-medium text-gray-900 mb-2">App is geoblocking to Nigerian networks</div>
          <div class="flex items-center gap-3 text-xs text-gray-400">
            <div class="flex items-center gap-1">💬 2</div>
            <div class="flex items-center gap-1">❤️ 1</div>
          </div>
        </div>
        
        <!-- Card 4 -->
        <div class="bg-white p-3 rounded shadow-sm border border-gray-200 cursor-pointer hover:shadow-md transition-shadow">
           <div class="text-sm font-medium text-gray-900 mb-2">Sign-in process needs improvement</div>
           <div class="flex items-center gap-3 text-xs text-gray-400">
            <div class="flex items-center gap-1">💬 3</div>
            <div class="flex items-center gap-1">❤️ 5</div>
          </div>
        </div>
      </div>

      <!-- Column 2: Planned -->
      <div class="w-72 flex-shrink-0 flex flex-col gap-3">
        <div class="flex items-center justify-between mb-1">
          <div class="flex items-center gap-2 font-medium text-sm text-gray-700">
            <div class="w-2 h-2 rounded-full bg-blue-400"></div>
            Planned
            <span class="bg-gray-200 text-gray-600 px-1.5 py-0.5 rounded text-xs">28</span>
          </div>
          <button class="text-gray-400 hover:text-gray-600">+</button>
        </div>

        <!-- Card 1 -->
        <div class="bg-white p-3 rounded shadow-sm border border-gray-200 cursor-pointer hover:shadow-md transition-shadow">
          <div class="text-sm font-medium text-gray-900 mb-2">Workspace Default Language Setting</div>
          <div class="flex items-center gap-3 text-xs text-gray-400">
            <div class="flex items-center gap-1">💬 1</div>
          </div>
        </div>

        <!-- Card 2 -->
        <div class="bg-white p-3 rounded shadow-sm border border-gray-200 cursor-pointer hover:shadow-md transition-shadow">
          <div class="text-sm font-medium text-gray-900 mb-2">Configurable translations (i18n)</div>
          <div class="flex items-center gap-3 text-xs text-gray-400">
            <div class="flex items-center gap-1">💬 3</div>
            <div class="flex items-center gap-1">❤️ 6</div>
          </div>
        </div>

        <!-- Card 3 -->
        <div class="bg-white p-3 rounded shadow-sm border border-gray-200 cursor-pointer hover:shadow-md transition-shadow">
          <div class="text-sm font-medium text-gray-900 mb-2">Improve CTA on Mobile</div>
          <div class="flex items-center gap-3 text-xs text-gray-400">
            <div class="flex items-center gap-1">💬 3</div>
            <div class="flex items-center gap-1">❤️ 11</div>
          </div>
        </div>
        
        <!-- Card 4 -->
        <div class="bg-white p-3 rounded shadow-sm border border-gray-200 cursor-pointer hover:shadow-md transition-shadow">
          <div class="text-sm font-medium text-gray-900 mb-2">Menu stays open, needs to close on outside click</div>
          <div class="flex items-center gap-3 text-xs text-gray-400">
            <div class="flex items-center gap-1">💬 2</div>
            <div class="flex items-center gap-1">❤️ 1</div>
          </div>
        </div>
      </div>

      <!-- Column 3: In Progress -->
      <div class="w-72 flex-shrink-0 flex flex-col gap-3">
        <div class="flex items-center justify-between mb-1">
          <div class="flex items-center gap-2 font-medium text-sm text-gray-700">
            <div class="w-2 h-2 rounded-full bg-purple-400"></div>
            In Progress
            <span class="bg-gray-200 text-gray-600 px-1.5 py-0.5 rounded text-xs">4</span>
          </div>
          <button class="text-gray-400 hover:text-gray-600">+</button>
        </div>

        <!-- Card 1 -->
        <div class="bg-white p-3 rounded shadow-sm border border-gray-200 cursor-pointer hover:shadow-md transition-shadow">
          <div class="text-sm font-medium text-gray-900 mb-2">Favicon sometimes not loading</div>
          <div class="flex items-center gap-3 text-xs text-gray-400">
            <div class="flex items-center gap-1">💬 2</div>
            <div class="flex items-center gap-1">❤️ 1</div>
          </div>
        </div>
        
        <!-- Card 2 -->
        <div class="bg-white p-3 rounded shadow-sm border border-gray-200 cursor-pointer hover:shadow-md transition-shadow">
          <div class="text-sm font-medium text-gray-900 mb-2">Enable SSO</div>
          <div class="flex items-center gap-3 text-xs text-gray-400">
            <div class="flex items-center gap-1">💬 8</div>
            <div class="flex items-center gap-1">❤️ 6</div>
          </div>
        </div>
        
        <!-- Card 3 -->
        <div class="bg-white p-3 rounded shadow-sm border border-gray-200 cursor-pointer hover:shadow-md transition-shadow">
          <div class="text-sm font-medium text-gray-900 mb-2">Kanban View for Roadmap</div>
          <div class="flex items-center gap-3 text-xs text-gray-400">
            <div class="flex items-center gap-1">💬 11</div>
            <div class="flex items-center gap-1">❤️ 24</div>
          </div>
        </div>
      </div>

    </div>
  </div>
</div>
