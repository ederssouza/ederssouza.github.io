<template>
  <aside class="profile">
    <cv-profile-avatar :image="avatar.link" :title="avatar.title" />

    <nav>
      <cv-profile-menu :links="links" />
      <cv-profile-footer :medias="medias" />
    </nav>
  </aside><!-- /.profile -->
</template>

<script>
import ProfileAvatar from './ProfileAvatar'
import ProfileMenu from './ProfileMenu'
import ProfileFooter from './ProfileFooter'

export default {
  name: 'Profile',
  components: {
    'cv-profile-avatar': ProfileAvatar,
    'cv-profile-menu': ProfileMenu,
    'cv-profile-footer': ProfileFooter
  },
  data () {
    return {
      avatar: {
        link: 'https://avatars0.githubusercontent.com/u/3737645?s=460&v=4',
        title: 'Eder Sampaio'
      },
      links: [
        {
          title: 'Sobre',
          icon: 'ion-person',
          active: true
        },
        {
          title: 'Portfolio',
          icon: 'ion-camera',
          active: false
        },
        {
          title: 'Contato',
          icon: 'ion-android-chat',
          active: false
        }
      ],
      medias: [
        {
          link: '//linkedin.com/in/ederssouza',
          title: 'LinkedIn',
          icon: 'ion-social-linkedin'
        },
        {
          link: '//github.com/ederssouza',
          title: 'GitHub',
          icon: 'ion-social-github'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.profile {}
</style>
