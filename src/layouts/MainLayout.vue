<template lang="pug">
q-layout(view='hHh Lpr lff')
  q-header.bg-black.text-white
    .row.no-wrap
      q-toolbar(style='height: 64px;', dark)
        q-btn(dense, flat, to='/') W
        q-toolbar-title.text-h6 Test
      q-toolbar.gt-sm.justify-center(style='height: 64px;', dark)
        .text-overline.text-uppercase.text-grey admin.adminArea
        q-badge.q-ml-sm(
          label='v3 Preview'
          color='pink'
          outline
          )
      q-toolbar(style='height: 64px;', dark)
        q-space
        q-btn.q-ml-md(flat, dense, icon='las la-times-circle', label='Exit' color='pink', to='/')
  q-drawer(v-model='leftDrawerOpen', show-if-above, bordered)
    q-list(padding, dense)
      q-item(active-class='bg-primary text-white', v-ripple)
        q-item-section admin.dashboard.title
      q-item(active-class='bg-primary text-white', v-ripple)
        q-item-section admin.sites.title
      q-item-label.q-mt-sm(header).text-caption.text-blue-grey-4 admin.nav.site
      q-item(active-class='bg-primary text-white', v-ripple)
        q-item-section admin.general.title
      q-item(active-class='bg-primary text-white', v-ripple)
        q-item-section admin.analytics.title
      q-item(active-class='bg-primary text-white', v-ripple)
        q-item-section admin.approval.title
      q-item(active-class='bg-primary text-white', v-ripple)
        q-item-section admin.comments.title
      q-item(active-class='bg-primary text-white', v-ripple)
        q-item-section admin.editors.title
      q-item(active-class='bg-primary text-white', v-ripple)
        q-item-section admin.locale.title
      q-item(active-class='bg-primary text-white', v-ripple)
        q-item-section admin.login.title
      q-item(active-class='bg-primary text-white', v-ripple)
        q-item-section admin.navigation.title
      q-item(active-class='bg-primary text-white', v-ripple)
        q-item-section admin.rendering.title
      q-item(active-class='bg-primary text-white', v-ripple)
        q-item-section admin.storage.title
      q-item(active-class='bg-primary text-white', v-ripple)
        q-item-section admin.theme.title
      q-item-label.q-mt-sm(header).text-caption.text-blue-grey-4 admin.nav.users
      q-item(active-class='bg-primary text-white', v-ripple)
        q-item-section admin.auth.title
      q-item(active-class='bg-primary text-white', v-ripple)
        q-item-section admin.groups.title
        q-item-section(side)
          q-badge(color='dark-3', :label='info.groupsTotal')
      q-item(active-class='bg-primary text-white', v-ripple)
        q-item-section admin.users.title
        q-item-section(side)
          q-badge(color='dark-3', :label='info.usersTotal')
      q-item-label.q-mt-sm(header).text-caption.text-blue-grey-4 admin.nav.system
      q-item(active-class='bg-primary text-white', v-ripple)
        q-item-section admin.api.title
      q-item(active-class='bg-primary text-white', v-ripple)
        q-item-section admin.audit.title
      q-item(active-class='bg-primary text-white', v-ripple)
        q-item-section admin.extensions.title
      q-item(active-class='bg-primary text-white', v-ripple)
        q-item-section admin.mail.title
      q-item(active-class='bg-primary text-white', v-ripple)
        q-item-section admin.security.title
      q-item(active-class='bg-primary text-white', v-ripple)
        q-item-section admin.ssl.title
      q-item(active-class='bg-primary text-white', v-ripple)
        q-item-section admin.system.title
      q-item(active-class='bg-primary text-white', v-ripple)
        q-item-section admin.utilities.title
      q-item(active-class='bg-primary text-white', v-ripple)
        q-item-section admin.webhooks.title
      q-item(active-class='bg-primary text-white', v-ripple)
        q-item-section admin.dev.flags.title
  q-page-container
    span Content View
  q-footer
    q-bar.justify-center(dense)
      span(style='font-size: 11px;') Footer
</template>

<script setup>
import { useMeta } from 'quasar'
import { reactive, ref } from 'vue'

// META
useMeta({
  titleTemplate: title => 'Test'
})

// DATA
const leftDrawerOpen = ref(true)
const user = reactive({
  name: 'John Doe',
  email: 'test@example.com',
  picture: null
})
const info = reactive({
  groupsTotal: 3,
  usersTotal: 2
})

</script>
