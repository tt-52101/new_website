<template>
  <div class="mobile-subsidebar">
    <div class="inner">
      <div class="sidebar-title">
        <h3>Dashboards</h3>
      </div>

      <ul class="submenu" data-simplebar>
        <VCollapseLinks>
          <template #header>
            Personal
            <i aria-hidden="true" class="iconify" data-icon="feather:chevron-right" />
          </template>

          <RouterLink :to="{ name: 'other' }" class="is-submenu">
            <i aria-hidden="true" class="lnil lnil-home"></i>
            <span>Other</span>
          </RouterLink>
        </VCollapseLinks>
      </ul>
    </div>
  </div>
</template>
