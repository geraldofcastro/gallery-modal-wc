# gallery-modal-wc
Modal e gerenciador de imagens 


### CONFIGURANDO O WIDGETS MODAL E PEQUENO GERENCIADOR DE IMAGENS

#### 1 - Cole a pasta "modal_gallery" para dentro de "_cdn/widgets/"

#### 2 - Abra o "dashboard.php" e logo acima da tag "\</head>" cole o código abaixo:

    <!-- Modal e Bliblioteca de imagens -->
    <script src="../_cdn/widgets/modal_gallery/modal_gallery.js"></script>
    <link rel="stylesheet" href="../_cdn/widgets/modal_gallery/modal_gallery.css"/>


#### 3 - Ainda na "dashboard.php" e logo abaixo da tag "\<body>" cole o código abaixo:

    <!-- Modal Uploads -->
    <div class="wc_modal" id="modal-arquivos">
        <div class="wc_modal-dialog wc_modal-lg">

            <div class="wc_modal-content">
                <div class="wc_modal-header">
                    <button type="button" class="wc_close" data-close="wc_modal">
                        <span>×</span>
                    </button>
                    <h4 class="modal-title" id="mySmallModalLabel">Biblioteca de Imagens</h4>
                </div>

                <div  class="wc_modal-body">
                    <div class="arquivos-uploads iframe embed-responsive">
                        <p>Biblioteca de Imagens Vázia</p>
                    </div>
                </div>

                <div class="wc_modal-footer">
                    <button class='btn btn_red arquivos_close fl_right' data-close="wc_modal">Fechar</button>
                    <div class="clear"></div>
                </div>
            </div>

        </div>
    </div>


#### 4 - No arquivo "create.php" que você for usar o "gerenciador de imagens", no post por exemplo, faça:

##### 4.1 - Cole o código abaixo, no lugar de sua preferencia. Ele irá mostrar o botão que dispara a ação que abre a modal:
        
        <label class="label">
            <a class='btn btn_blue m_top arquivos' data-id="#modal-arquivos" style="margin-left: 0;">Biblioteca de Imagens</a>
            <input type="text" name="capa_cover_file" readonly="readonly" class="input-upload" />
            <a class='btn btn_red arquivos_clear' title="Limpar Seleção">x</a>
        </label>

##### 4.2 - Cole a classe "capa_cover" na tag "\<img>" que mostra a thumb da capa.

