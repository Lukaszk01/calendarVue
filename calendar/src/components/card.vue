<template>
  <mdb-container>
    <mdb-flipping-card
      :flipped="flipped"
      innerClass="text-center h-100 w-100"
      style="max-width: 22rem; height: 465px;"
    >
      <mdb-card class="face front">
        <mdb-view hover>
          <a href="#!">
            <mdb-card-image
              src="https://mdbootstrap.com/img/Photos/Others/photo5.jpg"
              alt="Card image cap"
            ></mdb-card-image>
            <mdb-mask flex-center waves overlay="white-slight"></mdb-mask>
          </a>
        </mdb-view>
        <mdb-card-body>
          <mdb-card-title class="pl-5">
            Card title
            <mdb-btn class="float-right pb-5" style="bottom: 10px" flat @click="flipped=true">
              <mdb-icon size="lg" class="black-text" icon="share-alt" />
            </mdb-btn>
          </mdb-card-title>

          <hr />
          <p
            class="font-small grey-dark-text"
          >Some quick example text to build on the card title and make up the bulk of the card's content.</p>
          <mdb-btn flat>
            Read more
            <mdb-icon class="pl-2" icon="angle-double-right" />
          </mdb-btn>
        </mdb-card-body>
      </mdb-card>
      <mdb-card class="face back" style="height: 465px;">
        <mdb-card-body>
          <mdb-card-title class="pl-5">
            Social shares
            <mdb-btn style="bottom: 10px" flat @click="flipped=false">
              <mdb-icon size="lg" icon="times" />
            </mdb-btn>
          </mdb-card-title>
          <hr />
          <mdb-row class="justify-content-center pt-3">
            <mdb-btn tag="a" floating class="btn-dribbble">
              <mdb-icon fab icon="dribbble" />
            </mdb-btn>
            <mdb-btn tag="a" floating class="btn-slack">
              <mdb-icon fab icon="slack-hash" />
            </mdb-btn>
            <mdb-btn tag="a" floating class="btn-ins">
              <mdb-icon fab icon="instagram" />
            </mdb-btn>
            <mdb-btn tag="a" floating class="btn-pin">
              <mdb-icon fab icon="pinterest" />
            </mdb-btn>
          </mdb-row>
          <mdb-row class="justify-content-center">
            <mdb-btn tag="a" floating class="btn-tw">
              <mdb-icon fab icon="twitter" />
            </mdb-btn>
            <mdb-btn tag="a" floating class="btn-gplus">
              <mdb-icon fab icon="google-plus-g" />
            </mdb-btn>
            <mdb-btn tag="a" floating class="btn-git">
              <mdb-icon fab icon="github" />
            </mdb-btn>
          </mdb-row>
          <h5 class="text-center pt-5 pb-2">Join our community</h5>
          <hr />
          <mdb-row class="justify-content-center pt-4">
            <mdb-btn tag="a" class="pl-4 pr-4 btn-fb">
              <mdb-icon fab icon="facebook-f" />
            </mdb-btn>
            <mdb-btn tag="a" class="pl-4 pr-4 btn-tw">
              <mdb-icon fab icon="twitter" />
            </mdb-btn>
            <mdb-btn tag="a" class="pl-4 pr-4 btn-li">
              <mdb-icon fab icon="linkedin-in" />
            </mdb-btn>
            <mdb-btn tag="a" class="pl-4 pr-4 btn-ins">
              <mdb-icon fab icon="instagram" />
            </mdb-btn>
          </mdb-row>
        </mdb-card-body>
      </mdb-card>
    </mdb-flipping-card>
  </mdb-container>
</template>

<script>
  import {
    mdbContainer,
    mdbRow,
    mdbCol,
    mdbCard,
    mdbCardImage,
    mdbCardBody,
    mdbCardTitle,
    mdbCardUp,
    mdbCardAvatar,
    mdbBtn,
    mdbView,
    mdbMask,
    mdbIcon,
    mdbFlippingCard,
    mdbAvatar
  } from "mdbvue";

  export default {
    name: "CardAnimationsPage",
    components: {
      mdbContainer,
      mdbRow,
      mdbCol,
      mdbCard,
      mdbCardImage,
      mdbCardBody,
      mdbCardTitle,
      mdbCardUp,
      mdbCardAvatar,
      mdbBtn,
      mdbView,
      mdbMask,
      mdbIcon,
      mdbFlippingCard,
      mdbAvatar
    },
    data() {
      return {
        flipped: false
      };
    }
  };
</script>
</script>
