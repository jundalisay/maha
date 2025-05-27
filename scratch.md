## A Confederation Based on Trade

Based on the definition of Chinese historian Chau-ju-kua, the **immediate** territory of Maharlika included:
- Luzon (Tondo, Bulacan)
- Visayas
- Western Mindanao + Sabah (Pigafetta writes that Cagayan in Mindanao was a penal colony for Borneo)
- Eastern Mindanao (Kingdom of Butuan or Masawa)
- Babuyan Islands

However, there was no single constitution as all the cities were independent:


{{< q a="Chau Ju Kua" c="Chun Fan Chi" >}}
A ship will not remain at anchor longer than three or four days, after which it proceeds to another place; for the savage settlements along the coast of San-su [Visayas] are not connected by common jurisdiction [i.e. are all independent]
{{< /q >}}


This is common in archipelagos. For example, the Greeks were divided into city-states -- The Spartans fought the Athenians and the Athenians fought the Thebans. 


Yet, we call them all as 'the Greeks'. We never take Sparta nor Athens by themselves in isolation, just as we never regard Mindanao in isolation from Luzon, though both can be isolated from Thailand or Papua New Guinea. 


The nobilities were then unified by confederation which allowed each area to have freedom in politics, economics, and culture. Maharlika was part of a regional trade network that included:
- Northern Taiwan
- Luzon (Tondo, Bulacan, Ilocos)
- Visayas (Cebu)
- Mindanao (Butuan as Masawa)
- Borneo (Brunei)
- Moluccas 
- Celebes
- Tendaya


{{< q a="Antonio Morga">}}
According to ancient and modern cosmographers, that part of the world called Asia has adjacent to it a multitude of greater and lesser islands, inhabited by various nations and peoples, and as rich in precious stones, gold, silver, and other minerals, as they abound in fruit and grain, flocks, and animals.

Some of the islands yield all kinds of spices which are carried away and distributed throughout the world. These islands are commonly designated.. as the great archipelago of San Lazaro. 

Among the most famous of them are the islands of Maluco, Céleves, Tendaya, Luzon, Mindanao, and Borneo, which are now called the Filipinas.
{{< /q >}}


*The Filipinas* was the resource-rich region that the Spanish wanted, of which Maharlika was a part. Therefore, **Filipinas, Philippines, or Pilipinas are all abstract ideas of the Spanish which really expressed their ambition and greed** instead of anything about the nations in Southeast Asia. 

In other words, "The Philippines" has nothing to do with Filipinos, but everything to do with the Spanish desire for precious stones, gold, silver, minerals, fruit, grain, animals, and spices. So being "proud to be Pinoy" means being proud for your **land** having precious metals, bananas, coconuts, tuna, etc. and not really for you having skills, morals, or intellect.  






<div style="background-color: {{ .Params.c }}" class="mx-auto text-white flex items-center justify-center min-h-[200px] rounded-lg shadow hover:scale-110 text-white w-full">
  <a href="{{ .Permalink }}">
      <div class="text-center p-6">
        <h3 class="text-3xl text-white font-bold leading-6">{{ .Title }}</h3>
        <hr class="my-2 border-white opacity-50 w-2/3 mx-auto">
        <p class="text-sm text-gray-200">{{ .Params.heading }}</p>
        {{ if .Params.showdate }}
          <div class="leading-none text-gray-500 text-sm">
             {{ .Params.date.Format "January 2, 2006"  }}
          </div>
        {{- end }}
      </div>
  </a>
</div>


⁰¹²³⁴⁵⁶⁷⁸⁹⁺⁻⁼⁽⁾ⁿⁱ


nano config daw

module.exports = {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
    ...(process.env.HUGO_ENVIRONMENT === 'production'
      ? {
          cssnano: {
            preset: 'default',
          },
        }
      : {}),
  },
}




      integrity="{{ $styles.Data.Integrity }}"


      
  {{ $css := resources.Get "css/main.css" }}
    {{ if $css }}
      {{ $options := dict "inlineImports" true }}
      {{ $css = $css | css.PostCSS $options }}
      {{ if hugo.IsProduction }}
        {{ $css = $css | minify | fingerprint }}
      {{ end }}
      <link rel="stylesheet" href="{{ $css.RelPermalink }}">
    {{ else }}
      <!-- CSS file not found -->
      <style>body { color: red; }</style>
    {{ end }}

  {{ if hugo.IsProduction }}
    {{ $css = $css | minify | fingerprint | resources.PostProcess }}
  {{ end }}

    

  <link rel="stylesheet" href="{{ $css.RelPermalink }}">




  

<!-- layouts/partials/breadcrumbs.html -->
<nav aria-label="breadcrumb" class="mb-4">
  <ol class="flex flex-wrap text-sm text-gray-600">
    {{ $url := replace .RelPermalink (printf "/%s/" .Language.Lang) "/" }}
    {{ $lastUrlElement := index (last 1 (split (trim $url "/") "/")) 0 }}
    
    <!-- Home link -->
    <li class="breadcrumb-item">
      <a href="{{ .Site.Home.RelPermalink }}" class="hover:text-blue-600">
        Home
      </a>
      <span class="px-2">></span>
    </li>
    
    <!-- Build breadcrumbs based on URL path -->
    {{ $pathElements := split (trim $url "/") "/" }}
    {{ $currentPath := "/" }}
    
    {{ range $index, $element := $pathElements }}
      {{ $currentPath = printf "%s%s/" $currentPath $element }}
      {{ if ne $element $lastUrlElement }}
        <li class="breadcrumb-item">
          <a href="{{ $currentPath | relLangURL }}" class="dark:text-gray-200 hover:text-blue-600">
            {{ humanize $element }}
          </a>
          <span class="px-2">></span>
        </li>
      {{ else }}
        <li class="breadcrumb-item text-gray-900 font-medium dark:text-gray-200">
          {{ humanize $element }}
        </li>
      {{ end }}
    {{ end }}
  </ol>
</nav>



        <img class="w-12 h-12 rounded-full" src="/icons/{{ $file }}.jpg" alt="{{ $a }}">



        <blockquote class="p-4 my-4 border-s-4 border-gray-300 bg-gray-50 dark:border-gray-500 dark:bg-gray-800">
    <p class="text-xl italic font-medium leading-relaxed text-gray-900 dark:text-white">{{ . }}</p>
</blockquote>



{{ $a := .Get "a" | default "" }}

{{ $avatars := dict
  "Adam Smith" "Smith"
  "Adam-Smith" "Smith"
  "Baruch Spinoza" "Spinoza"
  "David Hume" "hume"
  "Descartes" "Rene Descartes"
  "Foreigner" "Glaucon"
  "Isaac Newton" "Newton"
  "socrates" "Socrates"
}}


{{ $file := cond (isset $avatars $a) (index $avatars $a) "Blank" }}
<!-- replace Blak with $$a  -->



  <!-- {{ range $paginator.Pages }}
          {{ with .Params.categories }}
            <span class="mx-1">•</span>
            <span>
              {{ range $index, $category := . }}
                {{ if $index }}, {{ end }}
                <a href="{{ "categories/" | relLangURL }}{{ $category | urlize }}" class="hover:underline">{{ $category }}</a>
              {{ end }}
            </span>
          {{ end }}
        </div>
        <div class="flex flex-wrap gap-2">
          {{ range .Params.tags }}
            <a href="{{ "tags/" | relLangURL }}{{ . | urlize }}" class="px-2 py-1 text-sm text-blue-600 bg-blue-100 rounded hover:bg-blue-200">{{ . }}</a>
          {{ end }} -->



@layer base {
  /* Style headings within your main content area */
  /* Adjust '.markdown-content' to a class wrapping your Hugo content */
  .markdown-content h1,
  .markdown-content h2,
  .markdown-content h3 {
    /* Default (Light Mode) Styles */
    @apply text-black mb-4 font-bold; /* Example light mode styles */
  }

/*  .markdown-content h1 {
     @apply text-4xl;
  }
  .markdown-content h2 {
     @apply text-3xl;
  }
   .markdown-content h3 {
     @apply text-2xl;
  }*/

  /* Dark Mode Styles */
  .dark .markdown-content h1,
  .dark .markdown-content h2,
  .dark .markdown-content h3 {
     /* Apply dark mode text color */
    @apply text-gray-100; /* Example dark mode text color */
     /* Add any other dark-mode specific overrides */
  }

  /* Alternatively, using Tailwind's dark: variant directly if preferred */
  /* This achieves the same as the .dark selector above with class strategy */
  /*
  .markdown-content h1,
  .markdown-content h2,
  .markdown-content h3 {
    @apply text-gray-900 dark:text-gray-100 mb-4 font-bold;
  }
  .markdown-content h1 { @apply text-4xl; }
  .markdown-content h2 { @apply text-3xl; }
  .markdown-content h3 { @apply text-2xl; }
  */
}
