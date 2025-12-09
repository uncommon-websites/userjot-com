<script lang="ts">
  import { onMount } from 'svelte';

  type Color = 'blue' | 'purple' | 'yellow' | 'gray' | 'green';

  interface Item {
    title: string;
    status: string;
    votes: number;
    date: string;
    color: Color;
  }

  const items: Item[] = [
    { title: "In-app widgets for collecting feedback", status: "Planned", votes: 55, date: "Nov 21", color: "blue" },
    { title: "Linear Integration", status: "In Progress", votes: 42, date: "Nov 22", color: "purple" },
    { title: "Webhooks", status: "Reviewing", votes: 23, date: "Nov 23", color: "yellow" },
    { title: "Post on behalf of a user", status: "Reviewing", votes: 12, date: "Dec 28", color: "yellow" },
    { title: "Kanban View for Roadmap", status: "Pending", votes: 11, date: "Nov 24", color: "gray" },
    { title: "Public API for changelog", status: "Planned", votes: 9, date: "Feb 21", color: "blue" },
    { title: "Display links as links in the comments", status: "Completed", votes: 8, date: "Jan 13", color: "green" },
    { title: "Github Issues Integration", status: "Closed", votes: 5, date: "Jun 19", color: "gray" },
    { title: "Disable self-registration", status: "Pending", votes: 5, date: "Jan 11", color: "gray" },
    { title: "Enable SSO", status: "Pending", votes: 1, date: "Feb 11", color: "gray" },
  ];

  const colorClasses: Record<Color, string> = {
    blue: "bg-blue-100 text-blue-800",
    purple: "bg-purple-100 text-purple-800",
    yellow: "bg-yellow-100 text-yellow-800",
    gray: "bg-gray-100 text-gray-800",
    green: "bg-green-100 text-green-800"
  };

  const dotColors: Record<Color, string> = {
    blue: "bg-blue-500",
    purple: "bg-purple-500",
    yellow: "bg-yellow-500",
    gray: "bg-gray-500",
    green: "bg-green-500"
  };
</script>

<section class="pt-32 pb-20 overflow-hidden">
  <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
    
    <!-- Headline -->
    <h1 class="text-5xl md:text-6xl font-bold tracking-tight text-gray-900 mb-6 leading-tight max-w-5xl mx-auto">
      Collect feedback <span class="inline-block align-middle text-4xl md:text-5xl">💬</span> prioritize with votes <span class="inline-block align-middle text-4xl md:text-5xl">🗳️</span> auto-sync your roadmap, and <span class="inline-block align-middle text-4xl md:text-5xl">💥</span> keep users engaged automatically
    </h1>
    
    <!-- Subheadline -->
    <p class="text-xl text-gray-500 mb-10 max-w-3xl mx-auto leading-relaxed">
      UserJot is the complete feedback platform for SaaS teams. Beautiful feedback boards that organize ideas, roadmaps that sync automatically, changelogs that write themselves, and engagement loops that run themselves.
    </p>
    
    <!-- CTA -->
    <div class="flex flex-col items-center gap-6">
      <a href="#start" class="inline-flex items-center px-8 py-4 border border-transparent text-lg font-medium rounded-full text-white bg-black hover:bg-gray-800 transition-colors shadow-lg hover:shadow-xl">
        Get Started Free
        <svg class="ml-2 w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 7l5 5m0 0l-5 5m5-5H6" />
        </svg>
      </a>
      
      <!-- Trust Signals -->
      <div class="flex flex-wrap justify-center gap-x-8 gap-y-2 text-sm text-gray-500">
        <div class="flex items-center gap-1.5">
          <svg class="w-4 h-4 text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"/></svg>
          Free forever
        </div>
        <div class="flex items-center gap-1.5">
          <svg class="w-4 h-4 text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"/></svg>
          30-second setup
        </div>
        <div class="flex items-center gap-1.5">
          <svg class="w-4 h-4 text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"/></svg>
          Unlimited users
        </div>
      </div>
    </div>

    <!-- Dashboard Mockup -->
    <div class="mt-20 relative mx-auto max-w-5xl">
      <div class="bg-white rounded-xl shadow-2xl border border-gray-200 overflow-hidden text-left">
        <!-- Mockup Header/Toolbar -->
        <div class="h-12 bg-white border-b border-gray-100 flex items-center px-4 gap-2">
          <div class="flex gap-1.5">
            <div class="w-3 h-3 rounded-full bg-red-400"></div>
            <div class="w-3 h-3 rounded-full bg-yellow-400"></div>
            <div class="w-3 h-3 rounded-full bg-green-400"></div>
          </div>
        </div>
        
        <div class="flex h-[600px] bg-gray-50">
          <!-- Sidebar -->
          <div class="w-64 bg-white border-r border-gray-200 flex flex-col flex-shrink-0">
            <div class="p-4 border-b border-gray-100">
              <div class="flex items-center gap-2">
                <div class="w-6 h-6 bg-black rounded text-white flex items-center justify-center text-xs font-bold">U</div>
                <div class="text-sm font-semibold">UserJot <span class="text-xs font-normal text-gray-400 block">Pro Plan</span></div>
                <svg class="ml-auto w-4 h-4 text-gray-400" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"/></svg>
              </div>
            </div>
            
            <div class="p-3">
              <button class="w-full flex items-center justify-center gap-2 bg-white border border-gray-200 rounded-md py-1.5 text-sm font-medium text-gray-600 shadow-sm mb-6">
                Create Request <span class="text-gray-400">+</span>
              </button>
              
              <div class="space-y-6">
                <div>
                  <div class="text-xs font-semibold text-gray-400 uppercase tracking-wider mb-2 px-2">Requests</div>
                  <div class="space-y-0.5">
                    <div class="flex items-center justify-between px-2 py-1.5 text-sm text-gray-600 hover:bg-gray-50 rounded cursor-pointer">
                      <div class="flex items-center gap-2"><div class="w-2 h-2 rounded-full border border-gray-300"></div> Pending</div>
                      <span class="text-gray-400 text-xs">45</span>
                    </div>
                    <div class="flex items-center justify-between px-2 py-1.5 text-sm text-gray-600 hover:bg-gray-50 rounded cursor-pointer">
                      <div class="flex items-center gap-2"><div class="w-2 h-2 rounded-full bg-yellow-400"></div> Reviewing</div>
                      <span class="text-gray-400 text-xs">13</span>
                    </div>
                    <div class="flex items-center justify-between px-2 py-1.5 text-sm text-gray-600 hover:bg-gray-50 rounded cursor-pointer">
                      <div class="flex items-center gap-2"><div class="w-2 h-2 rounded-full bg-blue-400"></div> Planned</div>
                      <span class="text-gray-400 text-xs">28</span>
                    </div>
                    <div class="flex items-center justify-between px-2 py-1.5 text-sm text-gray-600 hover:bg-gray-50 rounded cursor-pointer">
                      <div class="flex items-center gap-2"><div class="w-2 h-2 rounded-full bg-purple-400"></div> In Progress</div>
                      <span class="text-gray-400 text-xs">4</span>
                    </div>
                    <div class="flex items-center justify-between px-2 py-1.5 text-sm text-gray-600 hover:bg-gray-50 rounded cursor-pointer">
                      <div class="flex items-center gap-2"><div class="w-2 h-2 rounded-full bg-green-400"></div> Completed</div>
                      <span class="text-gray-400 text-xs">80</span>
                    </div>
                    <div class="flex items-center justify-between px-2 py-1.5 text-sm text-gray-600 hover:bg-gray-50 rounded cursor-pointer">
                      <div class="flex items-center gap-2"><div class="w-2 h-2 rounded-full bg-gray-400"></div> Closed</div>
                      <span class="text-gray-400 text-xs">30</span>
                    </div>
                  </div>
                </div>
                
                <div>
                  <div class="text-xs font-semibold text-gray-400 uppercase tracking-wider mb-2 px-2">Services</div>
                  <div class="space-y-0.5">
                    <div class="flex items-center gap-2 px-2 py-1.5 text-sm text-gray-600 hover:bg-gray-50 rounded cursor-pointer">
                      <svg class="w-4 h-4 text-gray-400" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 20l-5.447-2.724A1 1 0 013 16.382V5.618a1 1 0 011.447-.894L9 7m0 13l6-3m-6 3V7m6 10l4.553 2.276A1 1 0 0121 18.382V7.618a1 1 0 01-1.447-.894L15 7m0 13V7"/></svg>
                      Roadmap
                    </div>
                    <div class="flex items-center gap-2 px-2 py-1.5 text-sm text-gray-600 hover:bg-gray-50 rounded cursor-pointer">
                      <svg class="w-4 h-4 text-gray-400" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z"/></svg>
                      Changelog
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
          
          <!-- Main Content -->
          <div class="flex-1 flex flex-col bg-white">
            <div class="h-16 border-b border-gray-100 flex items-center justify-between px-6">
              <div class="flex items-center gap-4">
                <h2 class="text-lg font-semibold text-gray-900">Requests</h2>
                <div class="flex items-center gap-2 text-sm text-gray-500 bg-gray-50 px-2 py-1 rounded border border-gray-200">
                  <svg class="w-3 h-3" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 4a1 1 0 011-1h16a1 1 0 011 1v2.586a1 1 0 01-.293.707l-6.414 6.414a1 1 0 00-.293.707V17l-4 4v-6.586a1 1 0 00-.293-.707L3.293 7.293A1 1 0 013 6.586V4z"/></svg>
                  1 Filter
                </div>
              </div>
              <div class="flex items-center gap-3">
                <div class="relative">
                  <svg class="w-4 h-4 absolute left-3 top-1/2 transform -translate-y-1/2 text-gray-400" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"/></svg>
                  <input type="text" placeholder="Search..." class="pl-9 pr-4 py-1.5 text-sm border border-gray-200 rounded-md focus:outline-none focus:ring-1 focus:ring-gray-300 w-48" aria-label="Search requests">
                </div>
                <button class="p-1.5 hover:bg-gray-50 rounded border border-gray-200 text-gray-500" aria-label="Filter requests">
                   <svg class="w-4 h-4" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 4h13M3 8h9m-9 4h6m4 0l4-4m0 0l4 4m-4-4v12"/></svg>
                </button>
                <button class="p-1.5 bg-black text-white rounded hover:bg-gray-800" aria-label="Add new request">
                   <svg class="w-4 h-4" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4v16m8-8H4"/></svg>
                </button>
              </div>
            </div>
            
            <div class="flex-1 overflow-auto">
              <table class="w-full text-left">
                <thead class="bg-gray-50 text-xs font-medium text-gray-500 uppercase tracking-wider">
                  <tr>
                    <th class="px-6 py-3 border-b border-gray-100 w-12"></th>
                    <th class="px-6 py-3 border-b border-gray-100">Title</th>
                    <th class="px-6 py-3 border-b border-gray-100">Status</th>
                    <th class="px-6 py-3 border-b border-gray-100">Votes</th>
                    <th class="px-6 py-3 border-b border-gray-100 text-right">Date</th>
                  </tr>
                </thead>
                <tbody class="divide-y divide-gray-100">
                  {#each items as item}
                    <tr class="hover:bg-gray-50 group cursor-pointer">
                      <td class="px-6 py-4">
                        <div class="w-4 h-4 border border-gray-300 rounded"></div>
                      </td>
                      <td class="px-6 py-4">
                        <div class="text-sm font-medium text-gray-900">{item.title}</div>
                      </td>
                      <td class="px-6 py-4">
                        <span class={`inline-flex items-center px-2.5 py-0.5 rounded-full text-xs font-medium ${colorClasses[item.color]}`}>
                          <div class={`w-1.5 h-1.5 rounded-full mr-1.5 ${dotColors[item.color]}`}></div>
                          {item.status}
                        </span>
                      </td>
                      <td class="px-6 py-4">
                        <div class="flex items-center text-sm text-gray-500">
                          <svg class="w-4 h-4 mr-1 text-gray-400" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 10h4.764a2 2 0 011.789 2.894l-3.5 7A2 2 0 0115.263 21h-4.017c-.163 0-.326-.02-.485-.06L7 20m7-10V5a2 2 0 00-2-2h-.095c-.5 0-.905.405-.905.905 0 .714-.211 1.412-.608 2.006L7 11v9m7-10h-2M7 20H5a2 2 0 01-2-2v-6a2 2 0 012-2h2.5"/></svg>
                          {item.votes}
                        </div>
                      </td>
                      <td class="px-6 py-4 text-right text-sm text-gray-500">
                        {item.date}
                      </td>
                    </tr>
                  {/each}
                </tbody>
              </table>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>
