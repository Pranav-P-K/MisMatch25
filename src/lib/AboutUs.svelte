<script lang="ts">
  import '../app.css';
</script>

<div id="about" class="min-h-screen text-white p-6 font-sans flex flex-col justify-center items-center">
  <div class="w-full max-w-4xl mx-auto mb-12 px-4">
      <div class="relative bg-black rounded-lg p-8 border-2 border-blue-500 shadow-[0_0_30px_rgba(0,149,255,0.5)] hover:shadow-[0_0_50px_rgba(0,149,255,0.5)] transition-all duration-200">
          <div class="text-center space-y-6">
              <h2 class="text-4xl md:text-5xl font-bold text-transparent bg-clip-text bg-gradient-to-r from-purple-400 via-pink-300 to-purple-400 animate-pulse">
                  About Us
              </h2>
              <h3 class="text-xl md:text-2xl text-purple-300">Welcome to MISMATCH!</h3>
              <p class="text-purple-200/90 leading-relaxed max-w-2xl mx-auto">
                  A one-of-a-kind hackathon hosted by the IEEERAS Club of VIT Chennai!
              </p>
              <div class="space-y-4 text-purple-200/80">
                  <p class="leading-relaxed max-w-2xl mx-auto">
                      Mismatch is all about breaking boundaries, blending ideas, and creating innovative solutions by bringing together unique perspectives.
                  </p>
                  <p class="leading-relaxed max-w-2xl mx-auto">
                      With real-world challenges and an open platform to showcase your groundbreaking ideas, Mismatch promises an experience like no other!
                  </p>
              </div>
              <p class="text-lg md:text-xl font-medium text-pink-400 mt-8">
                  Let's mismatch, create, and reshape the world of tomorrow!
              </p>
          </div>
      </div>
  </div>

  <div class="w-full max-w-5xl mx-auto px-4">
      <div class="grid grid-cols-1 md:grid-cols-12 gap-8">
          <div class="md:col-span-5 space-y-16 md:pl-10">
              <div class="relative">
                  <div class="absolute inset-0 bg-purple-600/30 rounded-xl blur-xl"></div>
                  <div class="relative bg-black/90 rounded-xl p-6 border-2 border-purple-500 hover:shadow-[0_0_20px_rgba(0,149,255,0.5)] transition-all duration-200">
                      <p class="text-center text-purple-200/90 leading-relaxed">
                          The IEEERAS Club at VIT Chennai is a community of tech enthusiasts, innovators, and problem-solvers.
                      </p>
                  </div>
              </div>
              <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                  <img src="/vit.jpg" alt="VIT Chennai Campus" class="w-full h-48 object-cover rounded-tr-[5rem] border border-purple-500/50" />
                  <img src="/vit2.png" alt="VIT Chennai Campus" class="w-full h-48 object-cover rounded-tl-[6rem] border border-purple-500/50" />
              </div>
          </div>
          
          <div class="hidden md:flex md:col-span-2 justify-center">
              <div class="w-px h-full bg-purple-500/50"></div>
          </div>
          
          <div class="md:col-span-5 -space-y-8">
              <div class="flex justify-center md:justify-end">
                  <img class="w-60 md:w-100 h-70" src="/ras.svg" alt="IEERAS Logo" />
              </div>
              <div class="relative">
                  <div class="absolute inset-0 bg-purple-600/30 rounded-xl blur-xl"></div>
                  <div class="relative bg-black/90 rounded-xl p-6 border-2 border-purple-500 hover:shadow-[0_0_50px_rgba(0,149,255,0.5)] transition-all duration-200">
                      <p class="text-center text-purple-200/90 leading-relaxed">
                          At VIT Chennai, a premier institute known for excellence in education and research, we aim to provide a platform for bright minds to shine.
                      </p>
                      <div class="absolute hidden md:block -bottom-6 -right-12">
                          <img src="/Controller.png" class="w-28 md:w-42 h-auto transform rotate-12" alt="controller" />
                      </div>
                  </div>
              </div>
          </div>
      </div>
  </div>
</div>
