<template>
  <div id="app">

  <div id="navfirst">
    <b-navbar toggleable="lg" class="container">                  
      <b-collapse is-nav>
        <b-navbar-nav>  

          <span class="hsg-icon hsg-nav__globe-icon"></span>
          <b-nav-item-dropdown text="Lang">
            <b-dropdown-item disabled>日本語</b-dropdown-item>   
            <b-dropdown-item disabled>Deutsch</b-dropdown-item>          
            <b-dropdown-item disabled>English</b-dropdown-item>   
            <b-dropdown-item disabled>Español</b-dropdown-item>   
            <b-dropdown-item disabled>Português</b-dropdown-item>   
          </b-nav-item-dropdown>

          <b-nav-item href="#">Contact Us</b-nav-item>  
        </b-navbar-nav>            
        
        <b-navbar-nav class="ml-auto"><!-- Right aligned nav items -->
          <b-nav-form>
            <b-form-input size="sm" class="mr-sm-2" placeholder="Search"></b-form-input>
            <b-button size="sm" class="my-2 my-sm-0" type="submit">Search</b-button>
          </b-nav-form>


        </b-navbar-nav>
      </b-collapse>      
    </b-navbar>
  </div>

 <div>
    <b-navbar toggleable="lg" class="container">
      <img class="navbar-toggler" src="https://www.hubspot.com/hubfs/HubSpot_Logos/HSLogo_color.svg" alt="HubSpot Logo">
      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
      <b-collapse id="nav-collapse" is-nav>
                                         
            <img src="https://www.hubspot.com/hubfs/HubSpot_Logos/HSLogo_color.svg" alt="HubSpot Logo">                 
                    
        <b-navbar-nav class="ml-auto"><!-- Right aligned nav items -->

          <b-nav-item-dropdown text="Software" right></b-nav-item-dropdown>
          <b-nav-item-dropdown text="Pricing" right></b-nav-item-dropdown>
          <b-nav-item-dropdown text="Resources" right></b-nav-item-dropdown>
          <b-nav-item-dropdown text="Partners" right></b-nav-item-dropdown>
          <b-nav-item-dropdown text="About" right></b-nav-item-dropdown>


        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
  
  
    <div>
      <h1>Invoice Template Generator</h1>
    </div>

    <div id="body">
      <Form/>
    </div>

    <Info/>
    
  </div>
</template>

<script>
import Form from './components/Form.vue';
import Info from './components/Info.vue';

export default {
  name: 'App',
  components: {
    Form,
    Info
  }
}
</script>

<style lang="sass">
#body
  font: 100% Helvetica, sans-serif;
  background-color: rgb(240,240,240);
  padding-top: 80px;
#navfirst
  background-color: rgb(240,240,240);


</style>
