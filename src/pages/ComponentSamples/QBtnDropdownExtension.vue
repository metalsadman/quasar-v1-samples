<template>
  <div class="q-pa-md">
    <q-btn-dropdown color="primary" label="Dropdown Button" v-model="menu">
      <q-list>
        <!-- <q-item clickable v-close-popup @click="onItemClick">
          <q-item-section>
            <q-item-label>Photos</q-item-label>
          </q-item-section>
        </q-item>

        <q-item clickable v-close-popup @click="onItemClick">
          <q-item-section>
            <q-item-label>Videos</q-item-label>
          </q-item-section>
        </q-item> -->

        <q-item clickable v-close-popup @click="onItemClick" :key="1">
          <q-item-section>
            <q-item-label>
              <test />
            </q-item-label>
          </q-item-section>
        </q-item>
      </q-list>
    </q-btn-dropdown>
    <div class="row justify-between q-gutter-md">
      <div class="col bg-primary">
        Some content....
      </div>
      <div class="col bg-secondary">
        Some content2...
      </div>
    </div>
  </div>
</template>
<script>
import test from 'components/dropdown'
export default {
  components: {
    test
  },
  data () {
    return {
      menu: false
    }
  },
  methods: {
    onItemClick () {
      console.log('Clicked on an Item')
    }
  }
}
</script>