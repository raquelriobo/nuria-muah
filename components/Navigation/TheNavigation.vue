<template lang="pug">
  v-container
    v-navigation-drawer(width= 180 v-model="drawer" :mini-variant="miniVariant" :clipped="clipped" fixed app)
      v-list
        v-list-item(v-for="(item, i) in items" :key="i" :to="item.to" router exact)
          v-list-item-action
            v-icon {{ item.icon }}
          v-list-item-content
            v-list-item-title(v-text="item.title")
        v-list-item(@click="dialog=true" router exact)
          v-list-item-action
            v-icon {{ contact.icon }}
          v-list-item-content
            v-list-item-title(v-text="contact.title")
    v-app-bar(:clipped-left="clipped" fixed app)
      v-app-bar-nav-icon(class="hidden-sm-and-up" @click.stop="drawer = !drawer")
      v-btn(class="hidden-sm-and-up" icon @click.stop="miniVariant = !miniVariant")
        v-icon mdi-{{ `chevron-${miniVariant ? 'right' : 'left'}` }}
      //- v-btn(class="hidden-xs-only" icon @click.stop="clipped = !clipped")
      //-   v-icon mdi-application
      v-toolbar-title
        nuxt-link(to="/" tag="span" style="cursor: pointer") {{title}}
      v-spacer
      v-toolbar-items(class="hidden-xs-only")
        v-btn(text
              v-for="(item, i) in items" 
              :key="i" 
              :to="item.to")
          v-icon(left dark) {{ item.icon }}
          | {{ item.title }}
        v-btn(text 
              @click="dialog=true")
          v-icon(left dark) {{ contact.icon }}
          | {{ contact.title }}
        ContactForm(:value="dialog"
                    @input="dialog=$event")
</template>

<script>
import ContactForm from "@/components/Contact/ContactForm";

export default {
  name: "TheNavigationDrawer",
  components: { ContactForm },
  data() {
    return {
      dialog: false,
      clipped: false,
      drawer: false,
      contact: {
        icon: "mdi-face",
        title: "Contact"
      },
      items: [
        {
          icon: "mdi-heart",
          title: "Home",
          to: "/"
        },
        {
          icon: "mdi-brush",
          title: "Works",
          to: "/works"
        },
        {
          icon: "mdi-book-open-variant",
          title: "About",
          to: "/about"
        }
        // {
        //   icon: "mdi-face",
        //   title: "Admin",
        //   to: "/admin"
        // }
      ],
      miniVariant: false,
      right: true,
      title: "NURIA RIOBO MUAH"
    };
  }
};
</script>
