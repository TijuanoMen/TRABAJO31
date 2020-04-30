<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <tittle>NEWSLETTER</tittle>
    <link href="https://fonts.googleapis.com/css?family=Lato:300,400,700,900" rel="stylesheet">
    <link rel="stylesheet" href="css/normalize.css">
    <link rel="stylesheet" href="css/styles.css">
</head>
<body>

    <header class="site-header">
        <div class="contenedor contenido-header">
            <div class="barra">
                <a href="index.html" class="logo2"><img src="https://www.google.com/url?sa=i&url=https%3A%2F%2Fmailrelay.com%2Fes%2Fnewsletter&psig=AOvVaw0jeSE4dXQfyPVE7j54dESs&ust=1588370093896000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCPDPxpOSkekCFQAAAAAdAAAAABAD"></a>
                <div class="mobile-menu">
                    <a href="#navegacion">
                        <img src="img/barras.svg" alt="Icono Menu">
                    </a>
                    
                    
                </div>
                <div class="container">
  <h2>Meus anuncios</h2>

  <p-confirmDialog [style]="{width: '50vw'}"></p-confirmDialog>
  <p-tabView>
    <p-tabPanel header="Anúncios ativos ({{anunciosAtivos.length}})">
        <div class="meus-anuncios-grid">
            <app-meu-anuncio *ngFor="let anuncio of anunciosAtivos" [anuncio]="https://es.sendinblue.com/lp/newsletter/?utm_source=adwords&utm_medium=cpc&utm_content=Newsletter&utm_extension=&utm_term=newsletter&utm_matchtype=e&utm_campaign=1012177099&utm_network=g&km_adid=340439517061&km_adposition=&km_device=c&utm_adgroupid=73942186292&gclid=Cj0KCQjw7qn1BRDqARIsAKMbHDb2_7KMPYHn0Mf8ugoZasdkHLfkaOQYP3MiluTI_Xp67IHTKaFgDcwaAlbuEALw_wcB">
                <span class="button">
                    <div class="dropdown-container">
                        <div class="dropdown-trigger"><i class="fas fa-ellipsis-v"></i></div>
                        <div class="dropdown-content">
                          <div class="dropdown-link" (click)="visualizar(anuncio)">Visualizar</div>
                          <div class="dropdown-link" (click)="atualizar(anuncio)">Atualizar</div>
                          <div class="dropdown-link" (click)="desativar(anuncio)">Desativar</div>
                          <div class="dropdown-link" (click)="excluir(anuncio)">Excluir</div>
                        </div>
                    </div>
                  </span>
            </app-meu-anuncio>
        </div>
    </p-tabPanel>
    <p-tabPanel header="Anúncios inativos ({{anunciosInativos.length}})">
        <div class="meus-anuncios-grid">
            <app-meu-anuncio *ngFor="let anuncio of anunciosInativos" [anuncio]="anuncio">
                <span class="button">
                    <div class="dropdown-container">
                        <div class="dropdown-trigger"><i class="fas fa-ellipsis-v"></i></div>
                        <div class="dropdown-content">
                          <div class="dropdown-link" (click)="atualizar(anuncio)">Atualizar</div>
                          <div class="dropdown-link" (click)="ativar(anuncio)">Ativar</div>
                          <div class="dropdown-link" (click)="excluir(anuncio)">Excluir</div>

                        </div>
                    </div>
                  </span>
            </app-meu-anuncio>
          </div>
    </p-tabPanel>
    <p-tabPanel header="Anúncios expirados ({{anunciosExpirados.length}})">

        <app-meu-anuncio *ngFor="let anuncio of anunciosExpirados" [anuncio]="anuncio">
          <span class="button" (click)="renovar(anuncio)">Renovar</span>
          <span class="button" (click)="excluir(anuncio)">Excluir</span>
        </app-meu-anuncio>

    </p-tabPanel>
</p-tabView>


</div>
</body>
</html>

                
