<template>
<div>
   <Header/>
  <Movies />
  <br /> <br/>
  <Footer />
 
</div>
</template>

<script>
import Movies from './components/Movies';
import Header from './components/Header';
import Footer from './components/Footer';

export default {
  name: 'App',

  components: {
    Movies,
    Header,
    Footer
  },

  data: () => ({
    //
  }),
};
</script>
