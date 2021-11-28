<template>
  <header>
      <div class="header container ">
          <img src="../assets/logo-futurama.png" alt="">
          <h2>Character List</h2>
          <div class="input-container">
              <form action="">
                  <input type="text" placeholder="Inserisci il nome di un personaggio" v-model="userSearch" @keyup="$emit('searchChar', userSearch )">
                  <button type="submit" @click.prevent="$emit('searchChar', userSearch )">Search</button>
                  <button type="reset" class="reset">Reset</button>
              </form>
          </div>
      </div>
  </header>
</template>

<script>
export default {
    name: 'Header',

    data() {
        return {
            userSearch: ''
        }
    }
    
    
}
</script>

<style lang="scss">
@import '@/styles/vars';

    header {
        .header {
            padding: 15px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            img {
                height: 150px;
            }
            h2 {
                color: $primary-color;
                font-weight: 300;
                padding-bottom: 10px;
            }
            .input-container {
                width: 50%;
                form {
                    display: flex;
                    input {
                    height: 30px;
                    background-color: transparent;
                    border: none;
                    border-bottom: 2px solid $primary-color;
                    width: 100%;
                    margin-right: 5px;
                    color: white;
                    font-size: 18px;
                    outline: none;
                    }
                    button {
                        background-color: $tertiary-color;
                        border: none;
                        border-radius: 5px;
                        padding: 5px;
                        margin-right: 5px;
                        color: $primary-color;
                        font-weight: 700;
                        cursor: pointer;
                        &:hover {
                            background-color: white;
                            color: $tertiary-color;
                        }
                    }
                    .reset {
                        background-color: $primary-color;
                        color: $tertiary-color
                    }
                }

            }
        }
    }
</style>