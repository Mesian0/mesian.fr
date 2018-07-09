<template>
  <div class="cv">
    <header>
      <div class="profilePic">
        <img src="@/assets/profile_pic.png" alt="profile picture">
      </div>
      <div class="titleSection">
        <h1>Jeremy Berteloot</h1>
        <h3>Développeur web front-end & full-stack</h3>
        <status></status>
      </div>
    </header>
    <section>
      <h2>En bref</h2>
      <article>
        <ul>
          <li>Je suis un concepteur-développeur <strong>full-stack</strong> souhaitant s'orienter vers le <strong>front-end</strong></li>
          <li>J'utilise quotidiennement <tech-item :tech="techs.javascript"></tech-item>, <tech-item :tech="techs.git"></tech-item> et <tech-item :tech="techs.visualCode"></tech-item></li>
          <li>J'ai déjà travaillé sur des environnements <tech-item :tech="techs.macos"></tech-item>, <tech-item :tech="techs.windows"></tech-item> et <tech-item :tech="techs.archlinux"></tech-item></li>
          <li>Je monte actuellement en compétence sur <tech-item :tech="techs.angular"></tech-item>.</li>
          <li>Originaire de Montpellier, j'aime le <strong>webdesign</strong>, la <tech-item :tech="techs.guitar"></tech-item>, mon <tech-item :tech="techs.dog"></tech-item> et les <tech-item :tech="techs.wow"></tech-item></li>
          <li>J'ai un très bon niveau en <tech-item :tech="techs.english"></tech-item></li>
        </ul>
      </article>
    </section>
    <section>
      <h2>Expérience</h2>
      <article>
        <ul>
          <li class="outer">
            <div>2016 - en poste ADOC Solutions (Nantes)</div>
            <div class="jobTitle">Développeur web full-stack</div>
            <adoc-projects :techs="techs"></adoc-projects>
          </li>
          <li class="outer">
            <div>2013 - 2016 Auto-Entreprise (Montpellier)</div>
            <div class="jobTitle">Développeur web full-stack <tech-item :tech="techs.php"></tech-item> <tech-item :tech="techs.jquery"></tech-item> <tech-item :tech="techs.laravel"></tech-item> <tech-item :tech="techs.ubuntu"></tech-item></div>
          </li>
          <li class="outer">
            <div>2012 - 2013 Lundi Matin (Montpellier)</div>
            <div class="jobTitle">Développeur web full-stack sur ERP SAAS <tech-item :tech="techs.php"></tech-item> <tech-item :tech="techs.jquery"></tech-item></div>
          </li>
          <li class="outer">
            <div>2011 Virdys 3D (Nîmes)</div>
            <div class="jobTitle">Développeur web <tech-item :tech="techs.php"></tech-item></div>
          </li>
          <li class="outer">
            <div>2010 CFA (Marguerittes)</div>
            <div class="jobTitle">Développeur web <tech-item :tech="techs.php"></tech-item></div>
          </li>
        </ul>
      </article>
    </section>
    <section>
      <h2>Formations</h2>
      <article>
        <ul>
          <li class="outer">
            <div>2015 - 2016 Preston's College (Preston - UK)</div>
            <strong>Cambridge English Level 2 Certificate in ESOL Skills for Life</strong>
          </li>
          <li class="outer">
            <div>2013 - 2015 Université Paul Valéry (Montpellier)</div>
            <strong>Licence 2 Langues, Littératures et Civilisations Etrangères (Anglais)</strong>
          </li>
          <li class="outer">
            <div>2012 - 2013 IUT de Montpellier-Sète (Montpellier)</div>
            <strong>Licence Progiciels de Gestion intégrés - ERP</strong>
          </li>
          <li class="outer">
            <div>2009 - 2011 Lycée de la CCI (Nîmes)</div>
            <strong>BTS Informatique de Gestion</strong>
          </li>
        </ul>
      </article>
    </section>
    <footer></footer>
  </div>
</template>

<script>
import TechItem from '@/components/TechItem'
import AdocProjects from '@/components/AdocProjects'
import Status from '@/components/Status'
export default {
  components: {
    TechItem,
    AdocProjects,
    Status
  },
  data () {
    return {
      techs: {
        javascript: { label: 'Javascript', pic: 'javascript.png', color: '#f7df1e' },
        git: { label: 'git', pic: 'git.png', color: '#ef511e' },
        visualCode: { label: 'Visual Code', pic: 'vscode.png', color: '#5965b7' },
        macos: { label: 'Mac OS', pic: 'macos.png', color: '#5965b7', gradient: { type: 'vertical', from: '#78b5dc', to: '#af939b' } },
        windows: { label: 'Windows', pic: 'windows.png', color: '#278bdb' },
        archlinux: { label: 'Archlinux', pic: 'archlinux.png', color: '#65b7e1' },
        angular: { label: 'Angular', pic: 'angular.png', color: '#c42d2f' },
        guitar: { label: 'Guitare jazz', pic: 'guitar.png', color: '#e27c3e' },
        dog: { label: 'Chien', pic: 'dog.png', color: '#ffa015' },
        wow: { label: 'Jeux de rôle en ligne massivement multijoueur', pic: 'wow.png', color: '#313347' },
        english: { label: 'Anglais', pic: 'english.png', color: '#8B3926' },
        node: { label: 'NodeJS', pic: 'node.png', color: '#88C043' },
        docker: { label: 'Docker', pic: 'docker.png', color: '#17B5EB' },
        minio: { label: 'Minio (AWS S3)', pic: 'minio.png', color: '#3B3B3B' },
        elasticsearch: { label: 'Elastic Search', pic: 'elasticsearch.png', color: '#F6BE15' },
        vue: { label: 'VueJS', pic: 'vue.png', color: '#81D0AD' },
        apollo: { label: 'Apollo', pic: 'apollo.png', color: '#112B49' },
        php: { label: 'PHP', pic: 'php.png', color: '#8195D4' },
        laravel: { label: 'Laravel', pic: 'laravel.png', color: '#FB5C48' },
        ubuntu: { label: 'Ubuntu', pic: 'ubuntu.png', color: '#9A5228' },
        graphql: { label: 'GraphQL', pic: 'graphql.png', color: '#F192D2' },
        jquery: { label: 'jQuery', pic: 'jquery.png', color: '#1068AD' }
      }
    }
  }
}
</script>

<style lang="scss">
.cv {
  max-width: 1000px;
  margin: auto;
}

header {
  position: relative;
  width: 100%;
  height: 150px;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 40px 0;

  .profilePic {
    margin: 30px;
  }

  .profilePic, .profilePic > img {
    height: 100%;
    width: auto;
  }

  .titleSection {
    text-align: left;
    display: flex;
    align-items: flex-start;
    justify-content: center;
    flex-direction: column;
  }

  h1, h3 {
    line-height: 1.2em;
    margin: 0;
  }

  h1 {
    color: #646464;
    font-weight: 600;
  }

  h3 {
    color: #b7b7b7;
    font-weight: 400;
  }
}

section {
  padding-left: 50px;
  h2 {
    position: relative;
    display: flex;
    color: #aaaaaa;
    line-height: 1.8em;
    margin-top: 25px;
    margin-bottom: 0;
    &::before {
      content: '';
      position: absolute;
      left: -10px;
      width: 4px;
      border-radius: 3px;
      height: 100%;
      background: #aaaaaa;
      margin-right: 10px;
    }
  }

  article {
    .jobTitle {
      font-weight: 600;
      color: #404040;
    }
    ul {
      display: flex;
      flex-direction: column;
      justify-content: flex-start;

      li {
        margin: 4px 0;
      }

      li.outer {
        text-align: left;
        padding-left: 20px;
        margin: 10px 0;
      }
    }
  }
}

.icon {
  font-size: 16px;
}

.icon.code {
  color: #0984e3;
}

.icon.language {
  color: #55efc4;
}
</style>
