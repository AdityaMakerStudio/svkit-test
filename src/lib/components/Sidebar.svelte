<script>
    // Define navigation options
    let navOptions = [
      { name: 'Dashboard', route: '/' },
      { name: 'Profile', route: '/profile' },
      { name: 'Users', route: '/profile' },
      { name: 'Hospitals', route: '/profile' },
      { name: 'Compliance', route: '/profile' },
      { name: 'Bookings', route: '/profile' },
    ];
  </script>
  
  <div class="w-64 h-full font-mono shrink-0 bg-green-200 px-4  border-gray-100 flex  border-2 ">
    <ul>
      {#each navOptions as option}
        <li>
          <a href="{option.route}">{option.name}</a>
        </li>
      {/each}
    </ul>
</div>