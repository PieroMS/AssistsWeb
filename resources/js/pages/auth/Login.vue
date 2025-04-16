<template>
   <div class="min-h-screen flex">
     <div
       class="hidden md:flex w-1/2 bg-indigo-500 items-center justify-center p-8"
     >
      <!-- src="{{ asset('images/login.jpg') }}" -->
      <img
         src="https://storage.googleapis.com/cloud-gadmin_1/Grdar/5eb5973c0b601.jpg"
         alt="Login"
         class="w-full h-auto max-h-[500px] object-cover rounded-2xl shadow-xl"
       />
     </div>
 
     <div class="flex flex-col justify-center w-full md:w-1/2 bg-white p-8 md:p-16">
       <div class="max-w-md w-full mx-auto">
         <h2 class="text-3xl font-bold text-gray-800 mb-2">Bienvenido de nuevo</h2>
         <p class="text-gray-500 mb-8">Ingresa tus credenciales para continuar</p>
 
         <form @submit.prevent="login" class="space-y-6">
           <div>
             <label for="email" class="block text-sm font-medium text-gray-700">Correo electrónico</label>
             <input
               type="email"
               id="email"
               v-model="email"
               required
               class="mt-1 w-full px-4 py-2 border border-gray-300 rounded-xl focus:outline-none focus:ring-2 focus:ring-indigo-500"
               placeholder="tucorreo@ejemplo.com"
             />
           </div>
 
           <div>
             <label for="password" class="block text-sm font-medium text-gray-700">Contraseña</label>
             <input
               type="password"
               id="password"
               v-model="password"
               required
               class="mt-1 w-full px-4 py-2 border border-gray-300 rounded-xl focus:outline-none focus:ring-2 focus:ring-indigo-500"
               placeholder="••••••••"
             />
           </div>
 
           <div class="flex items-center justify-between text-sm">
             <label class="flex items-center space-x-2">
               <input type="checkbox" class="form-checkbox text-indigo-500" />
               <span>Recordarme</span>
             </label>
             <a href="#" class="text-indigo-500 hover:underline">¿Olvidaste tu contraseña?</a>
           </div>
 
           <button
             type="submit"
             class="w-full bg-indigo-500 text-white py-2 rounded-xl hover:bg-indigo-600 transition"
           >
             Ingresar
           </button>
         </form>
       </div>
     </div>
   </div>
 </template>
 
 <script setup>
 import { ref } from 'vue'
 
 const email = ref('')
 const password = ref('')
 
 const login = () => {
   console.log('Login:', { email: email.value, password: password.value })
 }
 </script>
 