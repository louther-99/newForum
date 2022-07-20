<template>
    <div class="container-fluid  d-flex body_bg m-0 p-2">

  <iCargoTitle />



<!-- container bordera-c bg-dark m-2 p-2 -->
  <div class = " bg-light d-flex sm flex-column overflow-scroll bordera shadow-lg">
      <UserAvatar />
        
        <div class="container ">


          <UserItemImage />


          <div class=" m-3 row  text-center ">
              <div class="col-sm-4 rounded border border-2  bg-info bd"> <strong>Exact Address</strong> </div>
              <div class="col-sm-4 rounded border border-2  bg-info bd"> <strong>Estimated Size</strong></div>
              <div class="col-sm-4 rounded border border-2  bg-info bd"> <strong>Pickup Date</strong> </div>
              
          <!-- end -->
          </div>
          <!-- removed -->


          <!-- <div class="row text-center m-1 gap-2">
            <div class="col-sm-4 border border-3 border-success"> <strong>Exact Address</strong> </div>
            <div class="col-sm-4 border border-3 border-success"> <input class = " input-sm"type="text" name="weight" id="weight"></div>
           

            <div class="col-sm-4 border border-3 border-success"> <strong>Pickup Dae</strong> </div>
            
          </div> -->

          <!-- start -->

          <div class=" m-3 row  rounded p-1 text-center  p-2 bg">


            
          <!-- end of pasting -->

            <div class="col-sm-4">
              <div class="form-floating d-flex col-sm-4 mt-2 border rounded w-100 border-2 p-1 ">
                <input type="text" class="form-control  inputEllipsis w-70  comp" name="pickupaddress" onFocus="geolocate()"  id="floatingPickup"  placeholder="Pickup Address">
                <label for="floatingPickup">Pickup Address</label>
                <span class="input-group-text material-icons">&#xe55c;</span>
                <!-- &#xE87C; -->
              </div>
  
              <div class="form-floating d-flex col-sm-4 mt-2 border rounded w-100 border-2 p-1">
                <input type="text" class="form-control w-100  inputEllipsis  comp" name="deliveryaddress" onFocus="geolocate()"  id="floatingDelivery"  placeholder="Delivery Addresss">
                <label for="floatingDelivery">Delivery Address</label>
                <span class="input-group-text material-symbols-outlined">&#xf14d;</span>
              </div>
            </div>
         
            <!-- <div class="col-sm-4 mt-2 border border-2 p-3"> <label for="weight"></label>

              <input type="text" placeholder="Weight"  class = " w-50 inputEllipsis" name="weight" id="weight">
            </div> -->
            

            <div class="col-sm-4 rounded bg-muted">
              <div class="form-floating col-sm-4 mt-2 border  rounded w-100 d-flex border-2 p-1">
                <input type="text" class="form-control w-100  inputEllipsis" name="weight" id="weight"  placeholder="Weight">
                <label for="weight">Weight</label>
                <span class="input-group-text material-symbols-outlined">&#xe13d;</span>
              </div>
            </div>
            

      
            <div class="col-sm-4 rounded bg-muted">
              <div class="form-floating col-sm-4 mt-2 border rounded w-100 d-flex border-2  p-1">
                <input type="date" class="form-control w-100" name="Pickup_Date" id="dateofbirth"  placeholder="Date of Birth">
                <label for="dateofbirth"><strong>Date of Birth</strong> </label>
                <span class="input-group-text material-symbols-outlined">&#xebcc;</span>
              </div>
            </div>
            

            
      
          </div>

            
          </div>

         <!-- hr -->
            <hr class="container-fluid d-flex border-3 text-warning opacity-75">

           <div class="d-flex container  justify-content-center text-center mb-3">
            <div class="container">
                <!-- <a href="#" id = "star-btn" class="btn bg-warning ">Star</a> -->
                <button id = "star-btn" type="button" class="btn btn-warning" data-toggle="modal" data-target="#rating">
                 Stars
                </button>
                <!-- <div class="container ">
                  <div class="rating container ">
                    <i class="rating__star fa fa-star border"></i>
                    <i class="rating__star fa fa-star border"></i>
                    <i class="rating__star fa fa-star border"></i>
                    <i class="rating__star fa fa-star border"></i>
                    <i class="rating__star fa fa-star border"></i>
                  </div>
                </div> -->
                
            </div>


            <!-- Bid button -->
            <div class="container">
              <!-- Button trigger modal -->
              <button type="button" class="btn  btn-warning" data-bs-toggle="modal" data-bs-target="#bidModal">
                Bid
              </button>
             
            </div>
            
            
           </div> 
          
      
       
      </div> 
<!-- End of bordera -->







<!-- Modal -->
<div class="modal fade" id="bidModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title" id="exampleModalLabel">Bidding Info</h5>
        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
      </div>
      <div class="modal-body">
        
<form class="row g-3">
  <div class="col-xl-12">
    <label for="inputPrice" class="form-label">Price</label>
    <input type="number" class="form-control" id="inputPrice">
  </div>
  <div class="col-xl-12">
    <label for="inputPickupDate" class="form-label">Pickup Date</label>
    <input type="date" class="form-control" id="inputPickupDate">
  </div>
  <div class="col-xl-12">
    <label for="inputVehicle" class="form-label">Type of Vehicle Type or Service</label>
    <select id="inputVehicle" class="form-select">
      <option selected>Choose...</option>
      <option>RoRo Boat</option>
      <option>Small Pickup</option>
      <option>Closed Van</option>
      <option>Pickup Truck</option>
      <option>6w Fwd Truck</option>
    </select>
  </div>
  <div class="col-12 text-end">
    <button type="submit" class="btn btn-primary">Submit</button>
  </div>
</form>
      </div>
      <!-- <div class="modal-footer">
        <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
        <button type="button" class="btn btn-primary">Submit</button>
      </div> -->
    </div>
  </div>
</div>


<!-- Modal -->
<div class="modal fade" id="rating" tabindex="-1" role="dialog" aria-labelledby="exampleModalCenterTitle" aria-hidden="true">
  <div class="modal-dialog modal-dialog-centered" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title" id="exampleModalLongTitle">Modal title</h5>
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
      </div>
      <div class="modal-body">
        ...
      </div>
      <div class="modal-footer">
        <button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
        <button type="button" class="btn btn-primary">Save changes</button>
      </div>
    </div>
  </div>
</div>

</div>  <!-- Main container -->
</template>



<script>   
import UserItemImage from './UserItemPicture.vue'
import UserAvatar from './Avatar.vue'
import iCargoTitle from './Title.vue'
    export default {
        name : "MainContent",
        components: {
          iCargoTitle,
          UserAvatar,
          UserItemImage
        }

    }

  
    
</script>