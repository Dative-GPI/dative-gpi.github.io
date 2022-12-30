<template>
  <div class="min-h-screen">
    <AppBar>
      <NuxtLink to="/" class="px-2 flex text-center justify-center flex-col hover:bg-slate-100">
        <img src="~/assets/img/app-logo.png" class="h-20" style="max-width: none;"  alt="logo">
      </NuxtLink>
      <div class="grow">
        <!-- Spacing -->
      </div>
      <AppBarLink to="/dative">
        DATIVE
      </AppBarLink>
      <AppBarLink to="/fleetManagement">
        Notre offre de gestion de flotte
      </AppBarLink>
      <AppBarLink to="/monitoring">
        Notre offre monitoring
      </AppBarLink>
      <AppBarLink to="/cybersecurity">
        Notre offre cybersécurité
      </AppBarLink>
    </AppBar>
    <NuxtPage style="min-height: calc(100vh - 80px - 80px);" />
    <AppFooter />
  </div>
</template>
