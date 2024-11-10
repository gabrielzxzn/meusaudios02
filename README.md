<html>
  <head>
    <meta charset="UTF-8">
    <title>Áudio</title>
    <link rel="stylesheet" href="https://cdn.plyr.io/3.6.7/plyr.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css">
    <style>
      @import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;700&display=swap');
        
      body {
        height: 100vh;
        overflow: hidden;
        margin: 0px;
      }    

      .audio-container {
        display: flex;
        align-items: center;
        justify-content: space-between;
        font-family: 'Open Sans', sans-serif;
        justify-content: flex-start;
        cursor: pointer; 
        width: 100px;
      }

      .audio-container img {
        width: 50px;
        height: 50px;
        border-radius: 50%;
        object-fit: cover;
        padding-right: 8px;
        padding-left: 10px;
      }

      .audio-container .microphone-icon {
        position: relative;
        margin-left: -67px;
        margin-bottom: -25px;
        font-size: 22px;
        color: #4ad954;
      }

      .audio-container .microphone-icon.blue {
        color: #3db8ee;
      }

      .plyr--audio .plyr__control.plyr__tab-focus,
      .plyr--audio .plyr__control:hover,
      .plyr--audio .plyr__control[aria-expanded=false] {
        background: rgba(0, 0, 0, 0);
        background: var(--plyr-audio-control-background-hover, var(--plyr-color-main, var(--plyr-color-main, rgba(0, 0, 0, 0))));
        color: rgba(0, 0, 0, 0);
        color: var(--plyr-audio-control-color-hover, #797979)
      }

      .plyr--audio .plyr__controls {
        background: rgba(0, 0, 0, 0);
        background: var(--plyr-audio-controls-background, rgba(0, 0, 0, 0));
        border-radius: inherit;
        color: #4a5464;
        color: var(--plyr-audio-control-color,#4a5464);
        margin-left: 0px;
        padding: 0px;
      }

      .plyr--audio .plyr__control--overlaid .plyr__control__icon {
        font-size: 33px;
      }

      .plyr--full-ui input[type=range]::-webkit-slider-thumb {
        -webkit-appearance: none;
        border: 0;
        border-radius: 100%;
        box-shadow: 0 1px 1px rgba(35,40,47,.15),0 0 0 1px rgba(35,40,47,.2);
        box-shadow: var(--plyr-range-thumb-shadow,0 1px 1px rgba(35,40,47,.15),0 0 0 1px rgba(35,40,47,.2));
        height: 13px;
        height: var(--plyr-range-thumb-height,13px);
        margin-top: -4px;
        margin-top: calc(var(--plyr-range-thumb-height,13px)/2*-1 - var(--plyr-range-track-height,5px)/2*-1);
        position: relative;
        -webkit-transition: all .2s ease;
        transition: all .2s ease;
        width: 13px;
        width: var(--plyr-range-thumb-height,13px);
        background: var(--range-thumb-background, #4ad954);
      }  

      .plyr--full-ui input[type=range].blue::-webkit-slider-thumb {
        background: var(--range-thumb-background-active, #3db8ee);
      }
    
      .hide {
        display: none;
      }

      .plyr__controls .plyr__controls__item.plyr__progress__container:first-child,
      .plyr__controls .plyr__controls__item.plyr__time+.plyr__time,
      .plyr__controls .plyr__controls__item.plyr__time:first-child {
        padding-left: 0;
        display: block;
        margin-left: 7.5px;
      }

      .plyr__time+.plyr__time:before {
        content: "";
        margin-right: var(--plyr-control-spacing);
      }

      .plyr--audio .plyr__controls .plyr__controls__item.plyr__time--current.hide,
      .plyr--audio .plyr__controls .plyr__controls__item.plyr__time--duration.hide {
        display: none;
      }

    </style>
  </head>
  <body>
    <div hidden="" id="sprite-plyr">
      <!-- SVG Sprite Definitions Here -->
    </div>
    <div class="audio-container" id="audioContainer">
      <!-- Cole o link do Seu áudio Abaixo-->
      <div tabindex="0" class="plyr plyr--full-ui plyr--audio plyr--html5 blue plyr--paused" style="--range-thumb-background: #3db8ee;">
        <div class="plyr__controls">
          <button class="plyr__controls__item plyr__control" type="button" data-plyr="play" aria-label="Play">
            <svg class="icon--pressed" aria-hidden="true" focusable="false">
              <use xlink:href="#plyr-pause"></use>
            </svg>
            <svg class="icon--not-pressed" aria-hidden="true" focusable="false">
              <use xlink:href="#plyr-play"></use>
            </svg>
            <span class="label--pressed plyr__sr-only">Pause</span>
            <span class="label--not-pressed plyr__sr-only">Play</span>
          </button>
          <div class="plyr__controls__item plyr__progress__container">
            <div class="plyr__progress">
              <input data-plyr="seek" type="range" min="0" max="100" step="0.01" value="0" autocomplete="off" role="slider" aria-label="Seek" aria-valuemin="0" aria-valuemax="16.222" aria-valuenow="2.840382" id="plyr-seek-3125" aria-valuetext="00:02 of 00:16" style="--value: 17.51%;" seek-value="-3.3542976939203357">
              <progress class="plyr__progress__buffer" min="0" max="100" value="100" role="progressbar" aria-hidden="true">% buffered</progress>
              <span class="plyr__tooltip" style="left: 0%;">00:00</span>
            </div>
          </div>
          <div class="plyr__controls__item plyr__time--current plyr__time hide" aria-label="Current time">00:02</div>
          <div class="plyr__controls__item plyr__time--duration plyr__time" aria-label="Duration">00:07</div>
        </div>
        <audio class="plyr" src="https://midias-s3-global.sendbot.cloud/sendbot/public/workspaces/cm2fopiec0007j1th2pbzb3ug/typebots/cm39bdwy70003v41c3aieg8cq/blocks/thtceyv0slpsp4lcxwjxhy7m?v=1731208301670"></audio>
      </div>
      <!-- Cole o link da Sua imagem Abaixo-->
      <img src="https://midias-s3-global.sendbot.cloud/sendbot/public/workspaces/cm2fopiec0007j1th2pbzb3ug/typebots/cm39bdwy70003v41c3aieg8cq/hostAvatar?v=1731106152265" alt="Imagem">
      <div class="microphone-icon blue">
        <i class="fas fa-microphone"></i>
      </div>
    </div>

    <script src="https://cdn.plyr.io/3.6.7/plyr.js"></script>
    <script>
      document.addEventListener('DOMContentLoaded', function() {
        const player = new Plyr('.plyr', {
          controls: ['play', 'progress', 'current-time', 'duration']
        });

        const audioElement = document.querySelector('.plyr');
        const currentTimeElement = document.querySelector('.plyr__time--current');
        const durationElement = document.querySelector('.plyr__time--duration');
        const microphoneIcon = document.querySelector('.microphone-icon');
        const playButton = document.querySelector('.plyr__controls button[data-plyr="play"]');

        currentTimeElement.classList.add('hide'); // Adiciona a classe 'hide' para ocultar inicialmente
        durationElement.classList.add('hide'); // Adiciona a classe 'hide' para ocultar inicialmente

        // Quando o áudio estiver pronto para tocar, mostra a duração e atualiza o tempo atual
        audioElement.addEventListener('loadedmetadata', function() {
          const duration = audioElement.duration;
          durationElement.textContent = formatTime(duration);
        });

        // Exibe o tempo atual e atualiza a barra de progresso
        audioElement.addEventListener('timeupdate', function() {
          const currentTime = audioElement.currentTime;
          currentTimeElement.textContent = formatTime(currentTime);

          // Atualiza o valor da barra de progresso
          const progress = (currentTime / audioElement.duration) * 100;
          document.querySelector('input[type="range"]').value = progress;
        });

        // Formata o tempo para o formato "mm:ss"
        function formatTime(seconds) {
          const minutes = Math.floor(seconds / 60);
          const secondsLeft = Math.floor(seconds % 60);
          return `${minutes}:${secondsLeft < 10 ? '0' + secondsLeft : secondsLeft}`;
        }

        // Alterna entre play e pause quando o contêiner for clicado
        document.getElementById('audioContainer').addEventListener('click', function() {
          if (audioElement.paused) {
            audioElement.play();
            playButton.setAttribute('aria-label', 'Pause');
            microphoneIcon.classList.add('blue');
          } else {
            audioElement.pause();
            playButton.setAttribute('aria-label', 'Play');
            microphoneIcon.classList.remove('blue');
          }
        });
      });
    </script>
  </body>
</html>
