<template>
  <div>
    <ul>
      <adoc-project :title="'Projet interne de gestion de stockage de binaire / recherche full-text'">
        <ul>
          <li>Réalisation d'une application back-end en API Rest <tech-item :tech="techs.node"></tech-item> - Express</li>
          <li>Installation via <tech-item :tech="techs.docker"></tech-item>, paramétrage et utilisation de la stack <tech-item :tech="techs.minio"></tech-item>, <tech-item :tech="techs.elasticsearch"></tech-item></li>
        </ul>
      </adoc-project>
      <adoc-project :title="'Projet de gestion documentaire SAAS'">
        <ul>
          <li>Réalisation d'une application front-end SPA <tech-item :tech="techs.vue"></tech-item> <tech-item :tech="techs.apollo"></tech-item> - Vue Router, Vuex, Axios</li>
          <li>Réalisation d'une application back-end en API Rest <tech-item :tech="techs.php"></tech-item> <tech-item :tech="techs.laravel"></tech-item> <tech-item :tech="techs.graphql"></tech-item> - JWT, MySQL</li>
          <li>Déploiement sur <tech-item :tech="techs.ubuntu"></tech-item> - Nginx</li>
        </ul>
      </adoc-project>
      <adoc-project :title="'Projet de gestion documentaire pour client bancaire'">
        <ul>
          <li>Réalisation d'une application front-end SPA <tech-item :tech="techs.vue"></tech-item> - Vue Router, Vuex, Axios</li>
          <li>Réalisation d'une application back-end en API Rest <tech-item :tech="techs.php"></tech-item> <tech-item :tech="techs.laravel"> - JWT, MySQL</tech-item></li>
          <li>Déploiement sur <tech-item :tech="techs.ubuntu"></tech-item> - Nginx, crontab</li>
        </ul>
      </adoc-project>
    </ul>
  </div>
</template>

<script>
import TechItem from '@/components/TechItem'
import AdocProject from '@/components/AdocProject'
export default {
  components: {
    TechItem,
    AdocProject
  },
  props: {
    techs: {
      type: Object,
      required: true
    }
  }
}
</script>

<style scoped>

</style>
