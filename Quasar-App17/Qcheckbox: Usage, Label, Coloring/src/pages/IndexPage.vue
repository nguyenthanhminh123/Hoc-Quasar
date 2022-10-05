<template>
  <q-page >
    <div class="q-pa-md">
      <div style="max-width:300px">
        <q-from @submit="submitForm">
          <div>
            <q-input 
              outlined 
              rounded 
              clearable 
              clear-icon="close" 
              color="teal" 
              label="Your Name" 
              v-model="formData.textInput" 
              :rules="[val => !!val || 'Field is required']" 
            />
            <q-select 
              outlined
              rounded
              clearable
              multiple
              counter
              use-chips
              use-input
              new-value-mode="add"
              max-values="2"
              transition-show="jump-dowm"
              transition-hide="jump-dowm"
              clear-icon="close"
              color="teal"
              :rules="[val => !!val || 'Field is required']" 
              :display-value="`Colors: ${formData.colors}`"
              v-model="formData.sex" 
              :options="formData.options" 
              label="Favorite Colors"
              >
              <template v-slot:prepend>
                <q-icon name="person"/>
              </template>
            </q-select>
          </div>
          <div>
            <span>Sex:</span>
            <q-list>
              <q-item>
                <q-item-section avatar>
                  <q-radio 
                    v-model="formData.sex" 
                    val="male" 
                    color="red" 
                  />
                </q-item-section>
                <q-item-section>
                  <q-item-label>
                    Male
                  </q-item-label> 
                  <q-item-label caption>
                    This is a sample caption
                  </q-item-label>
                </q-item-section>
              </q-item>
              <q-item>
                <q-item-section avatar>
                  <q-radio 
                    v-model="formData.sex" 
                    val="female" 
                    color="blue"
                  />
                </q-item-section>
                <q-item-section>
                  <q-item-label>
                    Female
                  </q-item-label>
                    <q-item-label caption>
                        This is a sample caption
                    </q-item-label>
                </q-item-section>
              </q-item>
            </q-list>
          </div>
          <div>
            <q-checkbox 
              v-model="formData.choices" 
              color="mayo" 
              label="Would you like some mayo?" 
            />
            <q-checkbox 
              v-model="formData.choices" 
              color="cheese" 
              label="Would you like some cheese?" 
            />
            <q-checkbox 
              v-model="formData.choices" 
              color="spice" 
              label="Would you like some spice?" 
            />
            {{ formData.choices }}
          </div>
          <div>
            <q-checkbox 
              v-model="formData.hunger" 
              true-value="yes" 
              false-value="no" 
              label="Are you hungry" 
            />
            {{ formData.hunger }}
          </div>
          <div>
            <q-list>
              <q-item>
                <q-item-section avatar>
                  <q-item-label>
                    <q-checkbox 
                      v-model="formData.choices" 
                      val="mayo" 
                      color="green"
                    />
                  </q-item-label>
                </q-item-section>
                <q-item-section>
                  <q-item-label>
                    Mayo
                  </q-item-label>
                  <q-item-label caption>
                    Adds mayo to the food
                  </q-item-label>
                </q-item-section>
              </q-item>
              <q-item>
                <q-item-section avatar>
                  <q-item-label>
                    <q-checkbox 
                      v-model="formData.choices" 
                      val="mayo" 
                      color="green"
                    />
                  </q-item-label>
                </q-item-section>
                <q-item-section>
                  <q-item-label>
                    Cheese
                  </q-item-label>
                  <q-item-label caption>
                    Adds mayo to the food.
                  </q-item-label>
                </q-item-section>
              </q-item>
            </q-list>
          </div>
          <div class="q-pt-md">
            <q-btn 
              type="submit" 
              label="Submit"/>
          </div>
        </q-from>
      </div>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'IndexPage',
  data() {
    return {
     formData: {
      hunger: "no",
      textInput: null,
      colors: [],
      sex: "male",
      choices: [],
      options: [
        "Red",
        "Blue",
        "Green",
        "Yellow",
        "Teal"
      ]
     }
    }
  },
  methods: {
    submitForm() {
      alert('You name is:' + this,formData.textInput);
    }
  }
})
</script>
