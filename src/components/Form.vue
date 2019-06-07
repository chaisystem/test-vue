<template>
  <div class="container shadow p-3 mb-5 bg-white rounded" id="divform">
    <b-form @submit="onSubmit" @reset="onReset" v-if="show">
      
     <h2>Invoice</h2>
        <div class="col-md-12">
          <b-container class="bv-example-row">
            <b-row>
              <b-col cols="7">                
                <div>
                  <div>
                    <div>                    
                          <input class="bold" type="text" placeholder="Your Company*" v-model="form.company" width="100%">
                      <div>
                          <input type="text" placeholder="Your First and Last Name*" v-model="form.name" width="100%">
                      </div>
                      <div>
                          <input type="text" placeholder="Company Website*" v-model="form.compWeb">
                      </div>
                      <div>
                          <input type="text" placeholder="Company Address" v-model="form.compAddres">
                      </div>
                      <div>
                          <input type="text" placeholder="City, State ZIP" v-model="form.cityZip">
                      </div>
                      <div>
                          <input type="text" placeholder="Country" v-model="form.country">
                      </div>
                      <div>
                          <input type="text" placeholder="Phone No.*" v-model="form.phone">
                      </div>
                      <div>
                          <input type="text" placeholder="Email Address*" value="" v-model="form.email">
                      </div>
                    </div>
                    <div>
                      <div>
                          <input class="bold" type="text" placeholder="Client's Company" value="" width="100%">
                      </div>
                      <div>
                          <input type="text" placeholder="Client's Name" value="" width="100%">
                      </div>
                      <div>
                          <input type="text" placeholder="Client's Address" value="" width="100%">
                      </div>
                      <div>
                          <input type="text" placeholder="City, State ZIP" value="" width="100%">
                      </div>
                      <div>
                          <input type="text" placeholder="Country" value="" width="100%">
                      </div>
                  </div>
                  </div>
                </div>

              </b-col>
              <b-col>
                <div style="border:solid">
                  <div id="divConfig">
                    <div class="sc-cMljjf ihZHsO" style="transform: scale(1);">
                      <button>click</button>
                    </div>
                  </div>
                  <div> 

                    <div class="no-print sc-bxivhb bLRsaW">
                      <span class="sc-EHOje hFjrX">Drag &amp; drop a logo file or click to upload</span>
                      <input class="sc-ifAKCX kkrLZm" type="file" accept="image/*"><img crossorigin="anonymous" src="" alt="Company Logo">
                    </div>  
                                       
                  </div>
                  <div id="divDateInvoice">
                    <div>
                          <label>Invoice No:</label>
                          <input type="text" placeholder="Client's Company" value="" width="100%">
                      </div>
                  </div>
                </div>
                
              </b-col>
            </b-row>
          </b-container>          
        </div>
          
      
      <b-button type="submit" variant="primary">Submit</b-button>      
    </b-form>
    <b-card class="mt-3" header="dev">
      <pre class="m-0">{{ form }}</pre>
    </b-card>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        form: {
          company: '',
          name: '',
          compWeb: '',
          compAddres: '',
          cityZip: '',
          country: '',
          phone: '',
          email: '',
          image: '',
          invoiceNo: '',
          invoiceDate: '',
          dueDate: '',          
          prod: []
        },
        foods: [{ text: 'Select One', value: null }, 'Carrots', 'Beans', 'Tomatoes', 'Corn'],
        show: true
      }
    },
    methods: {
      onSubmit(evt) {
        evt.preventDefault()
        alert(JSON.stringify(this.form))
      },

    }
  }
</script>


<style lang="sass">

input[type=text], textarea 
  border: none 
  padding-top: 5px;


input[type=text]:hover, textarea:hover 
  padding: 3px 0px 3px 3px;
  margin: 5px 1px 3px 0px;
  border: 1px dashed rgb(218, 116, 48);
  width: 80%;

#divform  
  background-color: white;

.bold
  font-weight: bold;
  padding-top: 10px;

::placeholder 
  color: rgb(211,211,211);

input[type=file]:hover 
  padding: 3px 0px 3px 3px;
  margin: 5px 1px 3px 0px;
  border: 1px dashed rgb(218, 116, 48);
  width: 80%;

#divimg
  width: 80%
  border: solid
  text-aling: center
  position: relative;
  left: 10%;

#divDateInvoice 
  padding-top: 20%;

#divConfig
  position: absolute;
  left: -170%;

.kkrLZm
  position: absolute;
  font-size: 10em;
  left: 0px;
  top: 0px;
  width: 100%;
  height: 100%;
  opacity: 0;
  cursor: pointer;

.hFjrX 
    width: 50%;
    font-size: 1em;
    font-weight: 600;
    text-align: center;

.bLRsaW
  position: relative;
  width: 60%;
  max-width: 60%;
  display: flex;
  -moz-box-pack: center;
  justify-content: center;
  -moz-box-align: center;
  align-items: center;
  margin-left: auto;
  overflow: hidden;
  border: 2px dashed rgb(253, 143, 95);
  transform: scale(1);
  transition: transform 0.3s ease 0s;



</style>
