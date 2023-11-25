<script>
export default {
  components: {},
  props: {
    title: String,
    imageName: String,
    dcType: String,
    dcPrice: String,
    indexCard: Number,
  },
};
</script>

<template>
  <div
    class="modal fade prova"
    :id="`exampleModal${indexCard}`"
    tabindex="-1"
    aria-labelledby="exampleModalLabel"
    aria-hidden="true">
    <div class="modal-dialog ms_modal-dialog">
      <div class="modal-content ms_modal">
        <div class="modal-title ms_modal-title">
          <h3>{{ title }}</h3>
        </div>
        <img :src="imageName" alt="" />
        <div class="ms_modal-description">
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Nam,
            voluptatem. Iure consequatur nisi accusantium maxime quaerat numquam
            aperiam eos vitae fugit placeat non, fuga, rem animi! Recusandae
            perspiciatis quasi repudiandae! Lorem ipsum dolor sit amet
            consectetur adipisicing elit. Iure quia ad quae vero tempore
            aspernatur amet tempora. Accusantium rem neque ratione optio,
            facere, eius nam enim eos accusamus, tempore voluptatibus.
          </p>
        </div>
        <div class="ms_modal-footer">
          <span>Book's Type: {{ dcType }}</span>
          <span>Price: {{ dcPrice }}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;
.prova {
  width: 100vw;
  height: 100vh;
  padding: 5rem 7rem;

  .ms_modal-dialog {
    max-width: 100%;
    margin: 0;
  }
}
.ms_modal {
  display: flex;
  flex-direction: column;
  padding: 3rem;
  margin: 0 auto;
  width: 100%;
  height: 100%;

  background: $mainColor;
  border: 5px solid black;
  border-radius: 2rem;
  img {
    width: 200px;
  }

  .ms_modal-description {
    padding-top: 1.5rem;
  }

  .ms_modal-footer {
    padding-top: 4rem;
    display: flex;
    justify-content: space-between;

    span {
      color: white;
      font-weight: bold;
    }
  }
}
</style>
