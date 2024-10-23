# **5. PROJETO PÁGINA ESTÁTICA**

#### Arquivo index.html:

```
<!DOCTYPE html>
<html lang="pt-br">

   <head>
      <meta charset="UTF-8">
      <meta http-equiv="X-UA-Compatible" content="ie=edge">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Portifólio</title>
      <link rel="stylesheet" href="css/styles.css">
      <link rel="preconnect" href="https://fonts.googleapis.com">
      <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
      <link href="https://fonts.googleapis.com/css2?family=Heebo:wght@100..900&display=swap" rel="stylesheet">
   </head>

   <body>
      <header>
         <nav id="navbar">
            <a class="nav-brand" href="#">Ivan Rogério Lucas Parmegiani</a>

            <ul class="nav-list">
               <li class="nav-item">
                  <a href="#">Trabalhos</a>
               </li>
               <li class="nav-item">
                  <a href="#">Blog</a>
               </li>
               <li class="nav-item">
                  <a href="#">Contato</a>
               </li>
            </ul>
            <div class="hamburger-menu">
               <svg xmlns="http://www.w3.org/2000/svg" x="0px" y="0px" width="48" height="48" viewBox="0 0 48 48">
                  <path fill="#607D8B" d="M6 22H42V26H6zM6 10H42V14H6zM6 34H42V38H6z"></path>
               </svg>
            </div>
         </nav>
      </header>

      <main>
         <section id="banner">
            <div class="banner-content">
               <h1 class="banner-content-title">Olá, sou Ivan, <br> desenvolvedor de Sistemas Web.</h1>
               <p class="banner-content-subtitle">
                  Lorem ipsum dolor, sit amet consectetur adipisicing elit. Reprehenderit esse et quasi necessitatibus
                  illo! Saepe necessitatibus, corporis eligendi corrupti nemo numquam dolore hic ullam sapiente incidunt!
                  Aliquid quaerat veritatis voluptas.
               </p>
               <button class="banner-content-btn">Baixar Currículo</button>
            </div>

            <img src="images/ivan2.jpg" alt="Ivan Parmegiani" class="banner-content-image">
         </section>

         <section id="posts">
            <div class="posts-content">
               <div class="posts-content-header">
                  <h2 class="section-title">Postagens recentes</h2>
                  <a class="view-all-link" href="#">Ver tudo</a>
               </div>

               <div class="posts-cards">
                  <div class="post-card">
                     <h3>Criando um sistema de design do zero</h3>
                     <span>19 Set 2024</span>
                     <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Facilis sunt temporibus omnis adipisci
                        veritatis reprehenderit, eveniet obcaecati commodi molestias, nobis tenetur, aspernatur
                        laboriosam
                        eaque accusamus tempora itaque debitis illo voluptatem.</p>
                  </div>
                  <div class="post-card">
                     <h3>Criando ícones pixel perfeitos no Figma</h3>
                     <span>19 Set 2024</span>
                     <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Facilis sunt temporibus omnis
                        adipisci
                        veritatis reprehenderit, eveniet obcaecati commodi molestias, nobis tenetur, aspernatur
                        laboriosam
                        eaque accusamus tempora itaque debitis illo voluptatem.</p>
                  </div>
               </div>

            </div>
         </section>
      </main>

      <footer>
      </footer>

   </body>
</html>
```

#### Arquivo CSS – styles.css

```
<!-- Arquivo CSS – styles.css -->

   * {
   margin: 0;
   padding: 0;
   box-sizing: border-box;
   }

   body,
   button,
   input,
   select,
   textarea {
   font-size: "Heebo", sans-serif;
   }

   /*cor de fundo da pagina html*/
   body {
   background-color: #f7f7f7;
   }

   header {
   background-color: #fff;
   height: 80px;
   }

   header #navbar {
   display: flex;
   /*background-color: #777; */
   justify-content: space-between; /*alinhar o texto horizontalmente*/
   align-items: center; /*alinhando o texto*/

   padding: 0 2rem;
   max-width: 1200px;
   margin: 0 auto; /*zerando as margens em cima e em baixo, depois colocando auto para o conteúdo ficar no meio*/
   height: 80px;
   }

   header #navbar .nav-brand {
   text-decoration: none;
   font-size: 1.5rem;
   font-weight: 700;
   color: #333;
   }

   header #navbar .nav-list {
   list-style: none;

   display: flex;
   align-items: center;
   gap: 31px;
   }

   header #navbar .nav-list .nav-item a {
   text-decoration: none;
   color: #333;
   font-size: 20px;
   font-weight: 500;
   }

   header #navbar .nav-list .nav-item a:hover {
   color: #777;
   transition: color 0.3s;
   }

   header #navbar .hamburger-menu {
   display: none;
   }

   @media (max-width: 740px) {
   header #navbar .hamburger-menu {
      display: block;
   }

   header #navbar .nav-list {
      display: none;
   }
   }

   /*Section banner*/
   main {
   margin-top: 6rem;
   }

   main #banner {
   display: flex;
   justify-content: space-between;

   max-width: 1200px;
   padding: 0 2rem;
   margin: 0 auto;
   }

   main #banner .banner-content .banner-content-title {
   font-size: 44px;
   font-weight: 700;
   line-height: 60px;
   margin-bottom: 40px;
   }

   main #banner .banner-content .banner-content-subtitle {
   font-size: 16px;
   font-weight: 400;
   line-height: 24px;
   max-width: 500px;
   margin-bottom: 38px;
   }

   main #banner .banner-content .banner-content-btn {
   background-color: #00a8cc; /*cor do botão*/
   color: white; /*cor do texto*/
   font-size: 20px; /*tamanhp do texto do botão*/
   font-weight: 500; /*peso de 500*/
   border-radius: 2px; /**/
   padding: 8px 24px; /*espaçamento em baixo e em cima e, depois nas laterais*/
   border: none;
   }

   main #banner .banner-content-image {
   border-radius: 50%; /*deixar a imagem redonda*/
   width: 100%; /*defino um tamanho 100% da imagem*/
   max-width: 300px; /*defino um tamanho para a imagem*/
   }

   @media (max-width: 920px) {
   main #banner {
      /*flex-direction: column;*/
      flex-direction: column-reverse;
      align-items: center;
      gap: 2rem;
   }
   main #banner .banner-content {
      text-align: center;
   }
   }

   /*Section Posts*/
   section#posts {
   margin-top: 71px;
   background-color: #edf7fa;
   }

   #posts .posts-content {
   padding: 0 2rem;
   max-width: 1200px;
   margin: 0 auto; /*zerando as margens em cima e em baixo, depois colocando auto para o conteúdo ficar no meio*/
   }

   #posts .posts-content .posts-content-header {
   display: flex;
   justify-content: space-between;
   align-items: center;
   padding: 2rem 0;
   }

   #posts .posts-content .posts-content-header .section-title {
   font-size: 22px;
   font-weight: 500;
   }

   #posts .posts-content .posts-content-header .view-all-link {
   text-decoration: none;
   color: #00a8cc;
   }

   #posts .posts-content .posts-cards {
   display: flex; /*deixar um ao lado do outro*/
   gap: 20px; /*alinhar*/
   margin-bottom: 2rem;
   }

   #posts .posts-content .posts-cards .post-card {
   background-color: white;
   padding: 24px;
   }

   #posts .posts-content .posts-cards .post-card h3 {
   font-size: 26px;
   font-weight: 700;
   margin-bottom: 37px;
   }

   #posts .posts-content .posts-cards .post-card span {
   font-size: 18px;
   font-weight: 400;
   margin-bottom: 24px; /*margim inferior*/
   display: block;
   }

   #posts .posts-content .posts-cards .post-card p {
   font-size: 16px;
   font-weight: 400;
   }

   @media (max-width: 740px) {
   #posts .posts-content .posts-cards {
      flex-direction: column;
   }
   }
```