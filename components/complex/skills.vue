<template lang="pug">
  section.py-16.mb-16.bg-white
    h1.text-center.uppercase.mb-8.text-xl.font-bold  
      span.font-normal What 
      | I do

    div.flex.justify-center
      div.mx-4
        h2.uppercase.border-b-2.border-gray-200.mb-4 Development
        ul
          each val in ['HTML5/CSS3', 'CSS preprocessor', 'PostCSS', 'CSS Frameworks', 'BEM/ITCSS/SMACSS/OOCSS', 'Javascript/Vue/Angular/jQuery', 'Git/NPM/Webpack/Gulp/Yeoman', 'Wordpress integration & dev', 'CMS integration']
            li= val
      div.mx-4
        h2.uppercase.border-b-2.border-gray-200.mb-4 Skills
        ul
          each val in ['Front-end / UI development', 'Fast responsive website', 'Responsive design', 'User experience', 'Design System', 'Cross browser compatibility', 'Problem solving and analytical', 'Close attention to detail', 'Responsive newsletters building']
            li= val      
</template>

<script>
export default {
  name: 'Skills'
}
</script>
