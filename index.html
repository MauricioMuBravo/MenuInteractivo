<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Mundialito Milenio - Menu 3D</title>
    <style>
        /* --- ESTILOS BASE --- */
        body {
            margin: 0;
            overflow: hidden;
            font-family: 'Arial Black', sans-serif;
            background: #000;
        }

        /* --- INTERFAZ DE USUARIO (HTML/CSS) --- */
        #ui {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 100; /* Asegurar que la UI esté sobre el 3D */
            pointer-events: none; /* Dejar pasar clics a las capas inferiores */
            display: flex;
            flex-direction: column;
            align-items: flex-start;
            justify-content: space-between;
        }

        /* Título Principal */
        .header {
            font-size: 70px;
            color: #fff;
            text-transform: uppercase;
            font-style: italic;
            margin: 60px 0 0 100px;
            text-shadow: 0 0 20px #00f2ff, 4px 4px 0px #1a2a6c;
            transform: skewX(-15deg); /* Efecto inclinado arcade */
        }

        /* Lista de Menú */
        .menu-list {
            position: absolute;
            left: 100px;
            top: 35%;
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        /* Items del Menú */
        .item {
            color: #fff;
            font-size: 32px;
            font-style: italic;
            cursor: pointer;
            pointer-events: auto; /* Habilitar clics */
            transition: 0.3s;
            display: flex;
            align-items: center;
            gap: 20px;
            transform: skewX(-20deg); /* Efecto inclinado arcade */
            text-transform: uppercase;
        }

        /* Efecto Hover */
        .item:hover {
            color: #00f2ff; /* Color cian neón */
            transform: skewX(-20deg) scale(1.1) translateX(15px);
            text-shadow: 0 0 10px #00f2ff;
        }

        /* Iconos de Balón */
        .ball-icon {
            width: 40px;
            filter: drop-shadow(0 0 8px #00f2ff);
            transition: transform 0.3s;
        }

        .item:hover .ball-icon {
            transform: rotate(180deg);
        }

        /* --- CAPA THREE.JS (Canvas Inferior) --- */
        #canvas-container {
            position: absolute;
            top: 0;
            left: 0;
            z-index: 1;
        }
    </style>
</head>
<body>

    <div id="ui">
        <h1 class="header">MAIN MENU</h1>
        <div class="menu-list">
            <div class="item"><img src="https://img.icons8.com/plasticine/100/soccer-ball.png" class="ball-icon"> All Stars</div>
            <div class="item"><img src="https://img.icons8.com/plasticine/100/soccer-ball.png" class="ball-icon"> My Captain</div>
            <div class="item"><img src="https://img.icons8.com/plasticine/100/soccer-ball.png" class="ball-icon"> Options</div>
            <div class="item" style="opacity: 0.5;"><img src="https://img.icons8.com/plasticine/100/soccer-ball.png" class="ball-icon"> Path to Glory</div>
        </div>
    </div>

    <div id="canvas-container"></div>

    <script type="importmap">
        { "imports": { "three": "https://unpkg.com/three@0.160.0/build/three.module.js" } }
    </script>
    <script type="module">
        import * as THREE from 'three';

        // Variables principales
        let scene, camera, renderer, player, clouds = [];

        init();
        animate();

        function init() {
            // Escena y Cámara
            scene = new THREE.Scene();
            camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);
            camera.position.set(2, 0, 10); // Ajustar cámara para ver a Oliver en el centro

            // Renderer
            renderer = new THREE.WebGLRenderer({ antialias: true });
            renderer.setSize(window.innerWidth, window.innerHeight);
            renderer.setPixelRatio(window.devicePixelRatio);
            document.getElementById('canvas-container').appendChild(renderer.domElement);

            // Iluminación
            const ambientLight = new THREE.AmbientLight(0xffffff, 0.5); // Luz ambiente suave
            scene.add(ambientLight);
            
            const sun = new THREE.DirectionalLight(0x00f2ff, 1.2); // Luz solar neón
            sun.position.set(5, 10, 7);
            scene.add(sun);

            // --- ESTADIO Y FONDO 3D ---
            // Césped del estadio (Plano con textura)
            const loader = new THREE.TextureLoader();
            const grassTex = loader.load('https://raw.githubusercontent.com/mrdoob/three.js/master/examples/textures/terrain/grasslight-big.jpg');
            grassTex.wrapS = grassTex.wrapT = THREE.RepeatWrapping;
            grassTex.repeat.set(10, 10); // Repetir horizontalmente
            
            const grassMat = new THREE.MeshPhongMaterial({ map: grassTex });
            const grassGeo = new THREE.PlaneGeometry(100, 100);
            const grass = new THREE.Mesh(grassGeo, grassMat);
            grass.rotation.x = -Math.PI / 2; // Acostar el césped
            grass.position.y = -5;
            scene.add(grass);

            // Suelo Grid (Tecnológico - Como en tu imagen)
            const gridHelper = new THREE.GridHelper(100, 30, 0x00f2ff, 0x111); // Líneas cian
            gridHelper.position.y = -4.9; // Justo encima del césped
            scene.add(gridHelper);

            // Fondo del Estadio (Cielo con gradiente)
            const bgGeo = new THREE.SphereGeometry(60, 32, 32);
            const bgMat = new THREE.MeshBasicMaterial({
                color: 0x1a2a6c, // Azul oscuro estadio
                side: THREE.BackSide
            });
            const background = new THREE.Mesh(bgGeo, bgMat);
            scene.add(background);

            // --- JUGADOR MUNDIALITO MILENIO (Oliver) ---
           const proxy = 'https://corsproxy.io/?'; 
const targetUrl = 'https://cdnpublicidad.milenio.com/2026/PublicidadOperaciones/MundialitoMilenio/jugadordefu2.png';

const playerTex = loader.load(proxy + encodeURIComponent(targetUrl));
const playerGeo = new THREE.PlaneGeometry(8, 10); 
const playerMat = new THREE.MeshBasicMaterial({
    map: playerTex,
    transparent: true,
    side: THREE.DoubleSide
});
player = new THREE.Mesh(playerGeo, playerMat);
player.position.set(6, -0.5, 3); 
scene.add(player);

            // --- NUBES DINÁMICAS (Partículas) ---
            const cloudTexture = loader.load('https://raw.githubusercontent.com/mrdoob/three.js/master/examples/textures/lensflare/lensflare0.png');
            const cloudGeo = new THREE.PlaneGeometry(12, 12);
            const cloudMat = new THREE.MeshBasicMaterial({
                map: cloudTexture, transparent: true, opacity: 0.15, depthWrite: false, blending: THREE.AdditiveBlending
            });

            for(let i=0; i<25; i++) {
                const cloud = new THREE.Mesh(cloudGeo, cloudMat);
                cloud.position.set(Math.random()*60-30, Math.random()*25-10, Math.random()*-20);
                cloud.scale.set(Math.random()*3, Math.random()*2, 1);
                scene.add(cloud);
                clouds.push(cloud);
            }

            // Ajuste de ventana
            window.addEventListener('resize', onWindowResize);
        }

        function onWindowResize() {
            camera.aspect = window.innerWidth / window.innerHeight;
            camera.updateProjectionMatrix();
            renderer.setSize(window.innerWidth, window.innerHeight);
        }

        function animate() {
            requestAnimationFrame(animate);
            const time = Date.now() * 0.001;

            // Mover nubes (Paralaje)
            clouds.forEach((c, i) => {
                c.position.x += 0.03 + (i*0.001); // Diferentes velocidades
                if(c.position.x > 35) c.position.x = -35;
                c.rotation.z += 0.001 * (i%2 === 0 ? 1 : -1);
            });

            // Movimiento suave de Oliver (respira/flota)
            if(player) {
                player.position.y = -0.5 + Math.sin(time * 1.2) * 0.4; // Flotación suave vertical
                player.rotation.y = Math.sin(time * 0.5) * 0.1; // Giro suave
            }

            // Cámara "respira" suavemente
            camera.position.x = 2 + Math.sin(time * 0.3) * 0.6;
            camera.position.y = Math.sin(time * 0.3) * 0.2;

            renderer.render(scene, camera);
        }
    </script>
</body>
</html>
