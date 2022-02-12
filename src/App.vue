<template>
  <div class="relative min-h-screen md:flex text-white">
    <main class="flex-1">
      <div class="mx-auto">
        <div class="grid grid-cols-1 md:grid-cols-12">
          <div class="h-screen bg-blue-gray-1 hidden lg:col-span-4 lg:block">
            <div class="h-screen flex items-center mx-auto">
              <div class="">
                <div class="grid grid-cols-1">
                  <div class="mb-4 flex items-center mx-auto">
                    <img src="https://via.placeholder.com/80x60" class="mr-4" alt="">
                    <h1 class="font-extrabold text-4xl">Robô Trader Mágico</h1>
                  </div>
                  <div class="mx-auto mb-4">
                    <p>
                      Faça já seu cadastro para começar a lucrar com o Robô Trader Mágico.
                    </p>
                  </div>
                  <div class="w-full mb-8">
                    <img src="https://via.placeholder.com/700x400" alt="">
                  </div>
                  <div class="mx-auto w-4/6">
                    <p class="text-xl mb-4 -ml-4 font-bold">
                      Ative sua conta
                    </p>
                    <ol class="list-decimal font-light">
                      <li>Criar conta</li>
                      <li>Licença</li>
                      <li>Depositar</li>
                    </ol>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="bg-primary h-screen lg:col-span-8 grid grid-cols-1">
            <div class="p-4 flex items-center h-[80vh] md:h-[94vh]">
              <div class="mx-auto lg:w-4/6">
                <div class="grid grid-cols-1 gap-4">
                  <div class="mb-4 flex items-center">
                    <img src="https://via.placeholder.com/80x60" class="mr-4" alt="">
                    <h1 class="font-extrabold text-4xl">Robô Trader Mágico</h1>
                  </div>
                  <div class="flex items-center gap-2">
                    <p>Crie sua conta na </p>
                    <img src="@/assets/images/logoiqoption.png" class="w-24" alt="">
                  </div>
                  <div class="grid grid-cols-1 gap-4">
                    <div>
                      <input v-model="email" class="outline-none p-4 bg-blue-gray-2 text-white rounded-xl w-full placeholder:text-white" placeholder="E-mail de acesso" type="text">
                    </div>
                    <div>
                      <input v-model="whatsapp" class="outline-none p-4 bg-blue-gray-2 text-white rounded-xl w-full placeholder:text-white" placeholder="Seu WhatsApp" type="text">
                    </div>
                    <div>
                      <input v-model="password" class="outline-none p-4 bg-blue-gray-2 text-white rounded-xl w-full placeholder:text-white" placeholder="Digite uma senha" type="password">
                    </div>
                    <div>
                      <label class="flex items-center">
                        <input type="checkbox" class="form-checkbox">
                        <span class="text-lg ml-4">Aceito os <a href="#" class="text-secondary">termos e condições</a></span>
                      </label>
                    </div>
                    <div>
                      <button @click="handleSubmit" class="w-full bg-secondary text-white text-lg p-4 rounded-xl hover:opacity-90">
                        Criar minha conta
                      </button>
                    </div>
                    <div class="text-center mt-4">
                      <a href="#">Já tenho uma conta</a>
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <div class="p-4 relative bottom-0 w-full flex items-end">
              <div class="flex justify-center w-full">
                <p class="text-center">
                  O Robô Trader Mágico não está diretamente relacionado à plataforma IQ Option e é criado por uma equipe de desenvolvedores independentes.
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </main>
  </div>
</template>

<script lang="ts">
import { defineComponent, Ref, ref } from "vue";

export default defineComponent({
  setup() {
    const email: Ref<string> = ref('');
    const whatsapp: Ref<string> = ref('');
    const password: Ref<string> = ref('');

    const handleSubmit = () => {
      alert(`
        E-mail: ${email.value}
        WhatsApp: ${whatsapp.value}
        Senha: ${password.value}`);
    }

    return {
      email,
      whatsapp,
      password,
      handleSubmit,
    };
  }
});
</script>
