<template>
  <div class="content">
    <section class="section">
      <div class="section-content">
        <h1 class="section-name">
          {{ profile.name }}
          <small>{{ profile.occupation }}</small>
        </h1>

        <p>{{ profile.resume }}</p>
      </div>
    </section><!-- /.section -->

    <section class="section">
      <header class="section-header">
        <h2 class="section-title">Competências <span>técnicas</span></h2>
      </header>

      <div class="section-content">
        <cv-skills :skills="skills" />
      </div>
    </section><!-- /.section -->

    <section class="section">
      <header class="section-header">
        <h2 class="section-title">Experiência <span>profissional</span></h2>
      </header>

      <div class="section-content experience">
        <cv-timeline :items="experiences" />
      </div>
    </section><!-- /.section -->

    <section class="section">
      <header class="section-header">
        <h2 class="section-title">Formação <span>acadêmica</span></h2>
      </header>

      <div class="section-content education">
        <cv-timeline :items="education" />
      </div>
    </section><!-- /.section -->

    <section class="section">
      <header class="section-header">
        <h2 class="section-title">Cursos</h2>
      </header>

      <div class="section-content">
        <cv-courses :courses="courses" />
      </div>
    </section><!-- /.section -->

    <section class="section">
      <header class="section-header">
        <h2 class="section-title">Depoimentos</h2>
      </header>

      <div class="section-content">
        <cv-testimonials :testimonials="testimonials" />
      </div>
    </section><!-- /.section -->
  </div><!-- /.content -->
</template>

<script>
import Skills from './Skills'
import Timeline from './Timeline'
import Testimonials from './Testimonials'
import Courses from './Courses'

export default {
  name: 'Skills',
  components: {
    'cv-skills': Skills,
    'cv-timeline': Timeline,
    'cv-testimonials': Testimonials,
    'cv-courses': Courses
  },
  data () {
    return {
      profile: {
        name: 'Eder Sampaio',
        occupation: 'Front-End Developer',
        resume: 'Formado em Gestão da Tecnologia da Informação, apaixonado por Front-End, web performance e UX.'
      },
      skills: [
        {
          title: 'Vue.js',
          percent: '90'
        },
        {
          title: 'webpack',
          percent: '80'
        },
        {
          title: 'javascript',
          percent: '90'
        },
        {
          title: 'sass',
          percent: '70'
        },
        {
          title: 'css',
          percent: '100'
        },
        {
          title: 'git',
          percent: '90'
        },
        {
          title: 'html5',
          percent: '100'
        },
        {
          title: 'Linux',
          percent: '80'
        }
      ],
      experiences: [
        {
          title: 'Front-End Developer',
          subtitle: 'Gold 360',
          period: 'out de 2017 – o momento',
          text: null
        },
        {
          title: 'Front-End Developer',
          subtitle: 'GFT Group',
          period: 'nov de 2015 – set de 2017',
          text: null
        },
        {
          title: 'Front-End Developer',
          subtitle: 'BRQ IT Solutions',
          period: 'set de 2014 – nov de 2015',
          text: null
        },
        {
          title: 'Front-End Developer',
          subtitle: 'Agência MGF Arte',
          period: 'abr de 2013 – abr de 2014',
          text: null
        }
      ],
      education: [
        {
          title: 'Tecnólogo em Gestão da Tecnologia da Informação',
          subtitle: 'Faculdade Sumaré',
          period: '2010 – 2013'
        }
      ],
      testimonials: [
        {
          name: 'André Vitor Cuba de Miranda',
          occupation: 'System Software Engineer',
          avatar: 'https://media.licdn.com/dms/image/C5603AQGLAGY8AfKZtQ/profile-displayphoto-shrink_800_800/0?e=1526990400&v=alpha&t=7zxoU0nAdsO0nCm92tiJpxv5h1edeU_2GAK-_1cLgWs',
          connection: 'Em 14 de novembro de 2017, André Vitor trabalhava com Eder, mas em empresas diferentes',
          text: 'É preciso pouquíssimo tempo para perceber toda qualidade e profissionalismo presente no trabalho do Eder. Aprendi de forma abundante e profunda conceitos e técnicas sobre web, ux e frontend em geral. Ainda me surpreendo com tamanho conhecimento que ele detém na área e como é compensador e satisfatório tê-lo na equipe. Espero futuramente ter novas oportunidades de trabalharmos juntos e quem sabe compensar parte de todo o conhecimento que ele sempre esteve disposto a ensinar e compartilhar.'
        },
        {
          name: 'Anderson Fernandes Mendes',
          occupation: 'Project Thinker | Business Designer',
          avatar: 'https://media.licdn.com/dms/image/C4D03AQEIvP9_Jad_vQ/profile-displayphoto-shrink_800_800/0?e=1526990400&v=alpha&t=I9H6S1s23D_fSmkAdzLzlpA_cBAQJ4fRk67KGuOF6F4',
          connection: 'Em 6 de agosto de 2015, Anderson supervisionava Eder diretamente',
          text: 'Eder é um excelente profissional, dedicado, e competente. Superou as expectativas das atividades que lhe foram destinadas e trouxe ótimas ideias para equipe.'
        },
        {
          name: 'Hugo Claret',
          occupation: 'Senior UX/UI Specialist / Digital Project Manager',
          avatar: 'https://media.licdn.com/dms/image/C4D03AQFNyHrm0zn4lA/profile-displayphoto-shrink_800_800/0?e=1526990400&v=alpha&t=_HhEZBozeTS4TWUpJ09YNVPF7oIOMtOO4TuCMaxsyTQ',
          connection: 'Em 16 de maio de 2015, Eder trabalhava com Hugo no mesmo grupo',
          text: 'Excelente profissional, detalhista e habilidoso em todas as suas atividades. Possui uma visão coerente, inovadora e altamente produtiva no desenvolvimento Front, sendo assim capaz de mostrar seu conhecimento técnico num todo.'
        },
        {
          name: 'Henrique Lima',
          occupation: 'CTO at Orbitall',
          avatar: 'https://media.licdn.com/dms/image/C5603AQEQpxwU16uAqA/profile-displayphoto-shrink_800_800/0?e=1526990400&v=alpha&t=Q_XrzpQl0VNLyCFtj5IDKt2qfKNIk2Phvnl7xyQqHCs',
          connection: 'Em 25 de julho de 2014, Henrique supervisionava Eder diretamente',
          text: 'Eder, sem dúvida nenhuma, é um dos melhores front-end developers com que pude trabalhar. Alta produtividade, foco e capacidade de criação mostraram resultados impressionantes no site da Akatus e no dashboard de clientes.    '
        }
      ],
      courses: [
        {
          name: 'Introdução ao Vue JS 2',
          institution: 'Udemy',
          workload: '40 horas',
          img: 'https://media.licdn.com/mpr/mpr/shrink_100_100/AAMAAwQIAAkAAQAAAAAAAA5EAAAAJGIwOGUxNjgwLTFhNDItNGRlOS1iMjc2LTU5NmY4NmMyODkzMg.bin'
        },
        {
          name: 'Gulp: automação de tarefas front-end',
          institution: 'Alura',
          workload: '40 horas',
          img: 'https://media.licdn.com/mpr/mpr/shrink_100_100/AAMABAQIAAkAAQAAAAAAABGhAAAAJGZlM2I1OGRiLTI5YjgtNDYwYy04YmY2LTY3NTZjZjJkNGYzYw.bin'
        },
        {
          name: 'Performance Web I',
          institution: 'Alura',
          workload: '40 horas',
          img: 'https://media.licdn.com/mpr/mpr/shrink_100_100/AAMABAQIAAkAAQAAAAAAABGhAAAAJGZlM2I1OGRiLTI5YjgtNDYwYy04YmY2LTY3NTZjZjJkNGYzYw.bin'
        },
        {
          name: 'Expressões regulares',
          institution: 'Alura',
          workload: '40 horas',
          img: 'https://media.licdn.com/mpr/mpr/shrink_100_100/AAMABAQIAAkAAQAAAAAAABGhAAAAJGZlM2I1OGRiLTI5YjgtNDYwYy04YmY2LTY3NTZjZjJkNGYzYw.bin'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scope>
.content {
  background-color: #fff;
}

.section-name {
  color: #333;
  font-size: 36px;
  line-height: 36px;
  font-weight: 700;
  left: -3px;
  letter-spacing: -1px;
  margin-bottom: 30px;
  position: relative;
  text-transform: uppercase;

  small {
    color: #999;
    display: block;
    font-size: 20px;
    font-weight: 300;
    margin-left: 1.5px;
    margin-top: 5px;
    text-transform: lowercase;
  }
}

.section-header {
  border-bottom: 1px solid #efefef;
  padding: 0 40px 25px;
}

.section-title {
  color: #333;
  font-size: 20px;
  font-weight: 700;
  letter-spacing: -1px;
  margin: 0;
  position: relative;
  text-transform: uppercase;

  span {
    font-weight: 300;
  }
}

.section-content {
  padding: 30px 40px;

  p {
    line-height: 22px;
    font-weight: 300;
  }
}

.section-content.experience {

  .timeline:after {
    content: "\f3ee";
  }
}

.section-content.education {

  .timeline:after {
    content: "\f357";
  }
}
</style>
