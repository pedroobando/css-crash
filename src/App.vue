<template>
  <div id="app" class="bg-gray-300 h-screen">
		<!-- NAVBAR COMPONENT -->
		<nav class="flex items-center justify-between flex-wrap bg-gray-800 px-6 py-4">
			<div class="flex items-center flex-shrink-0 text-white mr-6">
				<span class="font-bold text-xl">Biznet</span>
			</div>
			<div class="w-full block flex-grow sm:flex sm:items-center sm:w-auto">
				<div class="text-sm sm:flex-grow">
					<a v-for="(iMenu,index) in menuItems" :key="index" :href="iMenu.routeUrl" class="block mt-4 sm:inline-block sm:mt-0 text-teal-200 hover:text-white mr-4">{{iMenu.titulo}}</a>
				</div>

				<div>
					<a href="#" class="inline-block text-sm px-4 py-2 leading-none border rounded text-white border-white hover:border-transparent hover:text-blue-500 hover:bg-white mt-4 md:mt-0">Login</a>
				</div>
			</div>

		</nav>


    <div class="container mx-auto px-2 mt-2">
      <!-- BUTTON -->
      <button class="mx-2 bg-blue-500 hover:bg-blue-400 text-white font-bold py-2 px-4 rounded uppercase">Find Frend</button>
      <button class="btn btn-blue">Find Group</button>

      <!-- ALERT COMPONENT -->
      <div class="bg-red-100 border border-red-400 text-red-700 px-4 py-3 rounded relative my-5" role="alert">
        <strong class="font-bold">Alert..!</strong>
        <span class="block sm:inline ml-2">Please update your password</span>
      </div>

      <!-- CARD COMPONENT -->
      <div class="max-w-sm mx-auto flex p-6 bg-white rounded-lg shadow-xl">
        <div class="flex-shrink-0">
          <img src="@/assets/images/index.jpeg" alt="Travesy" class="h-12 w-12"/>
        </div>
        <div class="ml-6 pt-1">
          <h4 class="text-xl text-gray-900">Travesy Media</h4>
          <p class="text-base text-gray-600">You have a new message</p>
        </div>
      </div>

      <!-- CARD COLUNMS -->
      <div class="container mt-5">
        <!-- Flex on med screens and up -->
        <div class="md:flex">
          <div v-for="(twork,index) in trabajos" :key="index" class="flex-1 text-gray-700 text-center bg-gray-400 px-5 py-5 m-2 rounded">
            <div class="lg:flex lg:items-start">
              <div class="lg:flex-shrink-0">
                <img class="rounded-lg lg:w-40" :src="twork.imagenUrl" :alt="twork.titulo">
              </div>
              <div class="mt-4 lg:mt-0 lg:ml-6">
                <div class="uppercase tracking-wide text-sm text-indigo-600 font-bold">{{twork.titulo}}</div>
                <a href="#" class="block mt-1 text-lg leading-tight font-semibold text-gray-900 hover:underline">{{twork.contenido}}</a>
              </div>
            </div>
          </div>

        </div>
      </div>
      


    </div>
  </div>
</template>

<script>

export default {
  name: 'App',
  components: {
  },
  data: () => ({
    retorno: 'prueba',
    trabajos: [
      {
        imagenUrl: require('@/assets/images/work01.jpg'),
        titulo: 'Network',
        contenido: 'Finding connections to help your business grow'
      },
      {
        imagenUrl: require('@/assets/images/work02.jpg'),
        titulo: 'Working',
        contenido: 'ipsum dolor, sit amet consectetur adipisicing elit. Sequi quos, dolor facilis error fuga consequatur.'
      },
			{
				imagenUrl: require('@/assets/images/work03.jpg'),
				titulo: 'Travesy Media in Work',
				contenido: 'El equipo de Travesy Media trabajando para usted las 24 x 365.'
			}


    ],
		menuItems: [
			{
				titulo: 'Your Bussine',
				routeUrl: '#'
			},
			{
				titulo: 'Networking',
				routeUrl: '#'
			},
			{
				titulo: 'Blog',
				routeUrl: 'http://www.youtube.com'
			}

		]
  })
}
</script>

<style>
</style>
