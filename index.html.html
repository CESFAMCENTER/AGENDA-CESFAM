<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>AgendaSalud · CESFAM</title>

<!-- ═══════════════════════════════════════════════════════════
     PASO 1: REEMPLAZA ESTOS 7 VALORES CON LOS DE TU FIREBASE
     ═══════════════════════════════════════════════════════════ -->
<script>
var FB_CONFIG = {
  apiKey: "AIzaSyBGeTXreDfb9ar56FkWBzN1g6nWm7vUuvg",
  authDomain: "agenda-cesfam-f5f0a.firebaseapp.com",
  databaseURL: "https://agenda-cesfam-f5f0a-default-rtdb.firebaseio.com",
  projectId: "agenda-cesfam-f5f0a",
  storageBucket: "agenda-cesfam-f5f0a.firebasestorage.app",
  messagingSenderId: "699268506130",
  appId: "1:699268506130:web:1333fba48b845f7be82ecb"
};
</script>
<!-- ═══════════════════════════════════════════════════════════ -->

<script src="https://www.gstatic.com/firebasejs/8.10.1/firebase-app.js"></script>
<script src="https://www.gstatic.com/firebasejs/8.10.1/firebase-database.js"></script>

<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">

<style>
*{box-sizing:border-box;margin:0;padding:0}
body{font-family:'Inter',sans-serif;background:#f0f4f8;color:#1a202c;min-height:100vh}

/* LOADING */
#pantalla-carga{position:fixed;inset:0;background:#1B4F72;display:flex;flex-direction:column;align-items:center;justify-content:center;z-index:9999;color:white}
#pantalla-carga h2{font-size:22px;margin-bottom:8px}
#pantalla-carga p{font-size:14px;opacity:0.75}
.rueda{width:40px;height:40px;border:3px solid rgba(255,255,255,0.3);border-top:3px solid white;border-radius:50%;animation:girar 0.8s linear infinite;margin-bottom:20px}
@keyframes girar{to{transform:rotate(360deg)}}

/* HEADER */
header{background:#1B4F72;color:white;padding:0 20px;height:58px;display:flex;align-items:center;justify-content:space-between;position:sticky;top:0;z-index:100;box-shadow:0 2px 8px rgba(0,0,0,0.2)}
.logo{font-size:18px;font-weight:700;letter-spacing:-0.3px}
.logo span{font-size:13px;font-weight:400;opacity:0.7;margin-left:6px}
#btn-volver{background:rgba(255,255,255,0.15);border:1px solid rgba(255,255,255,0.3);color:white;border-radius:20px;padding:5px 14px;cursor:pointer;font-size:13px;font-family:'Inter',sans-serif;display:none}
#btn-volver:hover{background:rgba(255,255,255,0.25)}

/* MAIN */
.contenedor{max-width:640px;margin:0 auto;padding:20px 16px 80px}
.vista{display:none}
.vista.activa{display:block}

/* CARDS */
.card{background:white;border-radius:14px;padding:20px;margin-bottom:16px;box-shadow:0 1px 4px rgba(0,0,0,0.07)}
.card-titulo{font-size:15px;font-weight:700;color:#1B4F72;margin-bottom:4px}
.card-sub{font-size:13px;color:#718096}
.card-head{display:flex;align-items:center;gap:12px;margin-bottom:16px;padding-bottom:12px;border-bottom:1px solid #f0f4f8}
.icono{font-size:22px}

/* PORTAL */
.hero{text-align:center;padding:28px 16px 16px}
.hero h1{font-size:26px;font-weight:700;color:#1B4F72;margin-bottom:8px;line-height:1.3}
.hero p{font-size:14px;color:#718096;max-width:340px;margin:0 auto}
.portales{display:grid;grid-template-columns:1fr 1fr;gap:14px;margin-top:16px}
@media(max-width:420px){.portales{grid-template-columns:1fr}}
.portal{background:white;border-radius:16px;padding:28px 16px;text-align:center;cursor:pointer;border:2px solid transparent;transition:all 0.2s;box-shadow:0 2px 8px rgba(0,0,0,0.06)}
.portal:hover{border-color:#2980B9;transform:translateY(-2px);box-shadow:0 8px 20px rgba(27,79,114,0.13)}
.portal .ico{width:56px;height:56px;border-radius:50%;margin:0 auto 14px;display:flex;align-items:center;justify-content:center;font-size:24px}
.portal.paciente .ico{background:#EBF5FB}
.portal.admin .ico{background:#FEF9E7}
.portal h3{font-size:16px;font-weight:700;margin-bottom:5px}
.portal p{font-size:13px;color:#718096}

/* STEPS */
.pasos{display:flex;align-items:center;margin-bottom:20px}
.paso{display:flex;align-items:center;flex:1}
.paso-dot{width:30px;height:30px;border-radius:50%;background:#e2e8f0;color:#a0aec0;display:flex;align-items:center;justify-content:center;font-size:13px;font-weight:700;flex-shrink:0;transition:all 0.3s}
.paso-dot.activo{background:#1B4F72;color:white}
.paso-dot.hecho{background:#27AE60;color:white}
.paso-linea{flex:1;height:2px;background:#e2e8f0;transition:background 0.3s}
.paso-linea.hecha{background:#27AE60}

/* FECHAS */
.fechas-grid{display:flex;flex-wrap:wrap;gap:8px;margin-bottom:16px}
.fecha-btn{padding:10px 12px;border-radius:10px;border:1.5px solid #e2e8f0;background:white;cursor:pointer;font-family:'Inter',sans-serif;font-size:13px;font-weight:600;transition:all 0.2s;text-align:center;min-width:64px}
.fecha-btn.sel{background:#1B4F72;color:white;border-color:#1B4F72}
.fecha-btn:hover:not(.sel):not(:disabled){border-color:#2980B9;color:#1B4F72}
.fecha-btn:disabled{opacity:0.4;cursor:not-allowed}
.fecha-btn .dia-num{font-size:20px;font-weight:700;display:block}
.fecha-btn .dia-nom{font-size:11px;display:block}
.fecha-btn .dia-mes{font-size:10px;opacity:0.7;display:block}

/* ESPECIALIDADES */
.tags{display:flex;flex-wrap:wrap;gap:8px}
.tag{padding:6px 14px;border-radius:20px;background:#EBF5FB;color:#1B4F72;font-size:13px;font-weight:600;cursor:pointer;border:1.5px solid transparent;transition:all 0.2s}
.tag.sel{background:#1B4F72;color:white}
.tag:hover:not(.sel){border-color:#1B4F72}

/* CUPOS */
.cupos-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:10px}
@media(max-width:340px){.cupos-grid{grid-template-columns:repeat(2,1fr)}}
.cupo-btn{padding:12px 8px;border-radius:10px;border:1.5px solid #e2e8f0;background:white;cursor:pointer;text-align:center;transition:all 0.2s;font-family:'Inter',sans-serif;width:100%}
.cupo-btn:hover{border-color:#2980B9;background:#EBF5FB}
.cupo-btn.sel{border-color:#1B4F72;background:#1B4F72;color:white}
.cupo-hora{font-size:16px;font-weight:700;display:block}
.cupo-prof{font-size:11px;color:#718096;display:block;margin-top:2px}
.cupo-btn.sel .cupo-prof{color:rgba(255,255,255,0.7)}

/* FORMULARIO */
.campo{margin-bottom:14px}
.campo label{display:block;font-size:12px;font-weight:700;color:#718096;margin-bottom:5px;text-transform:uppercase;letter-spacing:0.5px}
.campo input,.campo select{width:100%;padding:11px 14px;border:1.5px solid #e2e8f0;border-radius:9px;font-family:'Inter',sans-serif;font-size:15px;color:#1a202c;background:white;outline:none;transition:border-color 0.2s}
.campo input:focus,.campo select:focus{border-color:#2980B9}
.campo select{appearance:none;background-image:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='12' height='8' viewBox='0 0 12 8'%3E%3Cpath d='M1 1l5 5 5-5' stroke='%23718096' stroke-width='2' fill='none' stroke-linecap='round'/%3E%3C/svg%3E");background-repeat:no-repeat;background-position:right 14px center;padding-right:36px}
input[type=date],input[type=time]{width:100%;padding:11px 14px;border:1.5px solid #e2e8f0;border-radius:9px;font-family:'Inter',sans-serif;font-size:15px;color:#1a202c;background:white;outline:none}
input[type=date]:focus,input[type=time]:focus{border-color:#2980B9}

/* BOTONES */
.btn{display:flex;align-items:center;justify-content:center;gap:8px;padding:13px 24px;border-radius:10px;font-family:'Inter',sans-serif;font-size:15px;font-weight:600;cursor:pointer;border:none;width:100%;transition:all 0.2s;margin-bottom:10px}
.btn:disabled{opacity:0.55;cursor:not-allowed}
.btn-pri{background:#1B4F72;color:white}
.btn-pri:hover:not(:disabled){background:#154060}
.btn-ok{background:#27AE60;color:white}
.btn-ok:hover:not(:disabled){background:#1e8449}
.btn-sec{background:white;border:1.5px solid #e2e8f0;color:#718096}
.btn-sec:hover{border-color:#1B4F72;color:#1B4F72}
.btn-borrar{background:#FDEDEC;color:#922B21;border:1px solid #fadbd8;font-size:13px;padding:6px 12px;border-radius:7px;cursor:pointer;font-family:'Inter',sans-serif;font-weight:600}
.btn-borrar:hover{background:#E74C3C;color:white}

/* ALERTAS */
.alerta{padding:13px 15px;border-radius:10px;font-size:13px;margin-bottom:14px;line-height:1.5}
.alerta-info{background:#EBF5FB;color:#1B4F72;border-left:3px solid #2980B9}
.alerta-ok{background:#EAFAF1;color:#1A6B3C;border-left:3px solid #27AE60}
.alerta-err{background:#FDEDEC;color:#922B21;border-left:3px solid #E74C3C}

/* CONFIRMACIÓN */
.caja-confirm{background:#1B4F72;color:white;border-radius:16px;padding:28px;text-align:center;margin-bottom:16px}
.confirm-codigo{font-size:32px;font-weight:700;letter-spacing:5px;background:rgba(255,255,255,0.15);padding:12px 24px;border-radius:12px;display:inline-block;margin:14px 0}
.confirm-sub{font-size:13px;opacity:0.8}

/* BADGES */
.badge{display:inline-flex;align-items:center;padding:3px 10px;border-radius:20px;font-size:12px;font-weight:600}
.badge-ok{background:#EAFAF1;color:#1A6B3C}
.badge-mal{background:#FDEDEC;color:#922B21}
.badge-gris{background:#f0f4f8;color:#718096}

/* STATS */
.stats{display:grid;grid-template-columns:repeat(3,1fr);gap:10px;margin-bottom:16px}
.stat{background:white;border-radius:10px;padding:14px;text-align:center;box-shadow:0 1px 4px rgba(0,0,0,0.06)}
.stat-n{font-size:28px;font-weight:700}
.stat-l{font-size:11px;color:#718096;margin-top:2px}
.stat.azul .stat-n{color:#1B4F72}
.stat.verde .stat-n{color:#27AE60}
.stat.naranjo .stat-n{color:#E67E22}

/* LISTAS */
.item-reserva{display:flex;align-items:center;justify-content:space-between;padding:13px 0;border-bottom:1px solid #f0f4f8;gap:12px}
.item-reserva:last-child{border-bottom:none}
.item-hora{font-size:18px;font-weight:700;color:#1B4F72;min-width:50px}
.item-info{flex:1}
.item-nombre{font-size:14px;font-weight:600}
.item-rut{font-size:12px;color:#718096;margin-top:2px}
.item-cupo{display:flex;align-items:center;justify-content:space-between;padding:10px 0;border-bottom:1px solid #f0f4f8;gap:10px}
.item-cupo:last-child{border-bottom:none}

/* TABS */
.tabs{display:flex;border-bottom:2px solid #e2e8f0;margin-bottom:16px}
.tab{padding:10px 16px;border:none;background:transparent;font-family:'Inter',sans-serif;font-size:14px;font-weight:600;color:#718096;cursor:pointer;border-bottom:2px solid transparent;margin-bottom:-2px}
.tab.activa{color:#1B4F72;border-bottom-color:#1B4F72}

/* SECCIÓN */
.sec-titulo{font-size:11px;font-weight:700;text-transform:uppercase;letter-spacing:0.8px;color:#a0aec0;margin-bottom:10px;display:flex;align-items:center;gap:8px}
.sec-titulo::after{content:'';flex:1;height:1px;background:#e2e8f0}
.mt{margin-top:14px}

/* VACÍO */
.vacio{text-align:center;padding:30px 16px;color:#a0aec0}
.vacio-ico{font-size:40px;margin-bottom:10px}
.vacio h3{font-size:14px;font-weight:600;color:#718096;margin-bottom:5px}

/* LIVE */
.live{display:inline-flex;align-items:center;gap:5px;font-size:11px;color:#27AE60;font-weight:600}
.dot-live{width:7px;height:7px;border-radius:50%;background:#27AE60;animation:pulsar 2s infinite}
@keyframes pulsar{0%,100%{opacity:1}50%{opacity:0.3}}

/* PIN */
.pin-input{font-size:36px;letter-spacing:14px;text-align:center;width:100%;padding:16px;border:2px solid #e2e8f0;border-radius:12px;font-family:monospace;outline:none;background:white}
.pin-input:focus{border-color:#1B4F72}

/* TOAST */
.toast{position:fixed;bottom:28px;left:50%;transform:translateX(-50%) translateY(120px);background:#1a202c;color:white;padding:12px 24px;border-radius:100px;font-size:14px;font-weight:500;transition:transform 0.3s;z-index:9999;white-space:nowrap;box-shadow:0 4px 16px rgba(0,0,0,0.2)}
.toast.visible{transform:translateX(-50%) translateY(0)}

/* dos columnas grilla admin */
.grid2{display:grid;grid-template-columns:1fr 1fr;gap:10px}
</style>
</head>
<body>

<!-- PANTALLA DE CARGA -->
<div id="pantalla-carga">
  <div class="rueda"></div>
  <h2>AgendaSalud</h2>
  <p>Conectando con la base de datos...</p>
</div>

<!-- HEADER -->
<header id="encabezado" style="display:none">
  <div class="logo">AgendaSalud <span>CESFAM</span></div>
  <button id="btn-volver" onclick="volver()">← Volver</button>
</header>

<!-- APP -->
<div class="contenedor" id="app" style="display:none">

  <!-- ── LANDING ── -->
  <div class="vista" id="v-inicio">
    <div class="hero">
      <h1>Agenda tu hora médica</h1>
      <p>Reserva tu atención de forma rápida y sin llamadas telefónicas</p>
    </div>
    <div class="alerta-info alerta">📅 Atención de lunes a viernes · Cupos disponibles en tiempo real</div>
    <div class="portales">
      <div class="portal paciente" onclick="ir('v-fecha')">
        <div class="ico">🏥</div>
        <h3>Soy Paciente</h3>
        <p>Reserva tu hora disponible</p>
      </div>
      <div class="portal admin" onclick="ir('v-pin')">
        <div class="ico">⚙️</div>
        <h3>Administrador</h3>
        <p>Panel de gestión de cupos</p>
      </div>
    </div>
  </div>

  <!-- ── PACIENTE: FECHA ── -->
  <div class="vista" id="v-fecha">
    <div class="pasos">
      <div class="paso"><div class="paso-dot activo" id="pd1">1</div><div class="paso-linea" id="pl1"></div></div>
      <div class="paso"><div class="paso-dot" id="pd2">2</div><div class="paso-linea" id="pl2"></div></div>
      <div class="paso"><div class="paso-dot" id="pd3">3</div><div class="paso-linea" id="pl3"></div></div>
      <div class="paso"><div class="paso-dot" id="pd4">✓</div></div>
    </div>
    <div class="card">
      <div class="card-head"><span class="icono">📅</span>
        <div><div class="card-titulo">Selecciona la fecha</div><div class="card-sub">Días con cupos disponibles</div></div>
      </div>
      <div class="fechas-grid" id="grid-fechas"></div>
      <div class="sec-titulo mt">Otra fecha</div>
      <input type="date" id="input-fecha" onchange="elegirFechaManual(this.value)">
    </div>
    <div class="card">
      <div class="card-head"><span class="icono">🩺</span>
        <div><div class="card-titulo">Especialidad</div><div class="card-sub">Filtra por tipo de atención</div></div>
      </div>
      <div class="tags" id="tags-esp"></div>
    </div>
    <button class="btn btn-pri" onclick="irACupos()">Ver cupos disponibles →</button>
  </div>

  <!-- ── PACIENTE: CUPOS ── -->
  <div class="vista" id="v-cupos">
    <div class="card">
      <div class="card-head"><span class="icono">🕐</span>
        <div><div class="card-titulo" id="titulo-cupos">Horarios disponibles</div><div class="card-sub" id="sub-cupos"></div></div>
      </div>
      <div id="contenedor-cupos"></div>
    </div>
    <button class="btn btn-sec" onclick="ir('v-fecha')">← Cambiar fecha</button>
  </div>

  <!-- ── PACIENTE: FORMULARIO ── -->
  <div class="vista" id="v-form">
    <div id="resumen-cupo"></div>
    <div class="card">
      <div class="card-head"><span class="icono">👤</span>
        <div><div class="card-titulo">Tus datos</div><div class="card-sub">Completa para confirmar</div></div>
      </div>
      <div class="campo">
        <label>Nombre completo</label>
        <input id="f-nombre" type="text" placeholder="Ej: Juan Pérez Soto">
      </div>
      <div class="campo">
        <label>RUT</label>
        <input id="f-rut" type="text" placeholder="Ej: 12.345.678-9" maxlength="12" oninput="formatearRut(this)">
      </div>
      <div class="campo">
        <label>Teléfono (opcional)</label>
        <input id="f-tel" type="tel" placeholder="+56 9 1234 5678">
      </div>
      <div class="alerta alerta-info" style="font-size:13px">Al confirmar, el cupo se bloquea en tiempo real y nadie más puede tomarlo.</div>
    </div>
    <button class="btn btn-ok" id="btn-confirmar" onclick="confirmar()">✓ Confirmar reserva</button>
    <button class="btn btn-sec" onclick="ir('v-cupos')">← Cambiar horario</button>
  </div>

  <!-- ── PACIENTE: CONFIRMACIÓN ── -->
  <div class="vista" id="v-confirmado">
    <div class="caja-confirm">
      <div style="font-size:48px">🎉</div>
      <div style="font-size:20px;font-weight:700;margin-top:10px">¡Reserva confirmada!</div>
      <div style="font-size:14px;opacity:0.8;margin-top:4px">Tu código de atención:</div>
      <div class="confirm-codigo" id="cod-confirm"></div>
      <div class="confirm-sub" id="det-confirm"></div>
    </div>
    <div class="card" id="detalle-confirm"></div>
    <div class="alerta alerta-info" style="font-size:13px">📸 Toma captura de pantalla. Presenta este código en recepción el día de tu atención.</div>
    <button class="btn btn-sec" onclick="inicio()">Volver al inicio</button>
  </div>

  <!-- ── ADMIN: PIN ── -->
  <div class="vista" id="v-pin">
    <div class="card" style="max-width:300px;margin:30px auto;text-align:center">
      <div style="font-size:48px;margin-bottom:12px">🔐</div>
      <div class="card-titulo" style="font-size:17px">Panel Administrativo</div>
      <div class="card-sub" style="margin-bottom:16px">Ingresa tu PIN de 4 dígitos</div>
      <div class="campo">
        <input class="pin-input" id="input-pin" type="password" maxlength="4" placeholder="••••"
          onkeyup="if(event.key==='Enter')verificarPin()">
      </div>
      <div id="error-pin" style="color:#E74C3C;font-size:13px;margin-bottom:12px;display:none">PIN incorrecto</div>
      <button class="btn btn-pri" onclick="verificarPin()">Ingresar →</button>
      <div style="margin-top:12px;font-size:12px;color:#a0aec0">PIN de acceso: 1234</div>
    </div>
  </div>

  <!-- ── ADMIN: PANEL ── -->
  <div class="vista" id="v-admin">
    <div style="display:flex;align-items:center;justify-content:space-between;margin-bottom:14px">
      <div style="font-size:15px;font-weight:700;color:#1B4F72">Panel de Gestión</div>
      <span class="live"><span class="dot-live"></span>Tiempo real</span>
    </div>

    <div class="tabs">
      <button class="tab activa" onclick="cambiarTab('reservas',this)">📋 Reservas</button>
      <button class="tab" onclick="cambiarTab('cupos',this)">🗓 Cupos</button>
      <button class="tab" onclick="cambiarTab('agregar',this)">➕ Agregar</button>
    </div>

    <!-- TAB: RESERVAS -->
    <div id="tab-reservas">
      <div class="stats" id="estadisticas"></div>
      <div class="campo">
        <label>Fecha a revisar</label>
        <input type="date" id="admin-fecha" onchange="cargarReservas()">
      </div>
      <div class="card">
        <div class="card-head"><span class="icono">📋</span>
          <div><div class="card-titulo">Reservas del día</div><div class="card-sub" id="sub-reservas"></div></div>
        </div>
        <div id="lista-reservas"><div class="vacio"><div class="vacio-ico">⏳</div><p>Cargando...</p></div></div>
      </div>
    </div>

    <!-- TAB: CUPOS -->
    <div id="tab-cupos" style="display:none">
      <div class="campo">
        <label>Fecha</label>
        <input type="date" id="admin-fecha-cupos" onchange="cargarCupos()">
      </div>
      <div class="card">
        <div class="card-head"><span class="icono">🗓</span>
          <div><div class="card-titulo">Cupos configurados</div><div class="card-sub" id="sub-cupos-admin"></div></div>
        </div>
        <div id="lista-cupos"></div>
      </div>
    </div>

    <!-- TAB: AGREGAR -->
    <div id="tab-agregar" style="display:none">
      <div class="card">
        <div class="card-head"><span class="icono">➕</span>
          <div><div class="card-titulo">Agregar cupos en bloque</div></div>
        </div>
        <div class="campo">
          <label>Profesional</label>
          <select id="nuevo-prof"><option value="">Seleccionar...</option></select>
        </div>
        <div class="campo">
          <label>Especialidad</label>
          <select id="nuevo-esp">
            <option>Medicina General</option>
            <option>Enfermería</option>
            <option>Kinesiología</option>
            <option>Matrona</option>
            <option>Nutrición</option>
          </select>
        </div>
        <div class="campo">
          <label>Fecha</label>
          <input type="date" id="nuevo-fecha">
        </div>
        <div class="grid2">
          <div class="campo"><label>Hora inicio</label><input type="time" id="nuevo-ini" value="08:00"></div>
          <div class="campo"><label>Hora fin</label><input type="time" id="nuevo-fin" value="13:00"></div>
        </div>
        <div class="campo">
          <label>Intervalo entre cupos</label>
          <select id="nuevo-intervalo">
            <option value="15">15 minutos</option>
            <option value="20">20 minutos</option>
            <option value="30" selected>30 minutos</option>
            <option value="60">60 minutos</option>
          </select>
        </div>
        <button class="btn btn-ok" onclick="agregarCupos()">✓ Guardar cupos en Firebase</button>
      </div>
      <div class="card">
        <div class="card-head"><span class="icono">👩‍⚕️</span>
          <div><div class="card-titulo">Agregar profesional</div></div>
        </div>
        <div class="campo">
          <label>Nombre completo</label>
          <input type="text" id="nuevo-prof-nombre" placeholder="Ej: Dr. Ana López">
        </div>
        <button class="btn btn-sec" style="width:auto;padding:10px 20px;font-size:14px" onclick="agregarProfesional()">+ Agregar</button>
      </div>
    </div>
  </div>

</div><!-- /contenedor -->

<div class="toast" id="toast"></div>

<script>
// ═══════════════════════════════════════════════════
// CONFIGURACIÓN Y ESTADO
// ═══════════════════════════════════════════════════
var PIN_ADMIN = '1234';
var sel = { fecha: null, esp: null, cupoId: null };
var historial = [];
var db;
var escuchadores = [];

// ═══════════════════════════════════════════════════
// INICIO: FIREBASE
// ═══════════════════════════════════════════════════
window.onload = function() {
  // Verificar si está configurado
  if (FB_CONFIG.apiKey === "AIzaSyAbCdEfGhIjKlMnOpQrStUvWxYz123456") {
    document.getElementById('pantalla-carga').innerHTML =
      '<div style="text-align:center;padding:24px;max-width:380px">' +
      '<div style="font-size:52px;margin-bottom:14px">⚠️</div>' +
      '<h2 style="color:white;margin-bottom:10px;font-size:20px">Falta configurar Firebase</h2>' +
      '<p style="color:rgba(255,255,255,0.8);font-size:14px;line-height:1.7">' +
      'Abre el archivo <strong>index.html</strong> con el Bloc de notas, busca la sección ' +
      '"{
  "rules": {
    ".read": true,
    ".write": true
  }
}" y pega los datos de tu proyecto Firebase.<br><br>' +
      'Sigue la guía paso a paso entregada.' +
      '</p></div>';
    return;
  }

  try {
    firebase.initializeApp(FB_CONFIG);
    db = firebase.database();
    cargarDatosIniciales();
  } catch(e) {
    document.getElementById('pantalla-carga').innerHTML =
      '<div style="text-align:center;padding:24px;max-width:380px">' +
      '<div style="font-size:52px;margin-bottom:14px">🔴</div>' +
      '<h2 style="color:white;margin-bottom:10px;font-size:20px">Error de conexión</h2>' +
      '<p style="color:rgba(255,255,255,0.8);font-size:14px;line-height:1.7">' +
      'No se pudo conectar con Firebase. Verifica que los 7 valores estén correctos.' +
      '<br><br><strong>Detalle:</strong> ' + e.message + '</p></div>';
  }
};

function cargarDatosIniciales() {
  // Timeout de 8 segundos
  var timeout = setTimeout(function() {
    document.getElementById('pantalla-carga').innerHTML =
      '<div style="text-align:center;padding:24px;max-width:420px">' +
      '<div style="font-size:52px;margin-bottom:14px">⏱️</div>' +
      '<h2 style="color:white;margin-bottom:14px;font-size:18px">No se pudo conectar</h2>' +
      '<div style="background:rgba(255,255,255,0.12);border-radius:12px;padding:16px;text-align:left;font-size:13px;color:rgba(255,255,255,0.9);line-height:1.8">' +
      '<strong>Verifica estos 3 puntos en Firebase:</strong><br><br>' +
      '1️⃣ &nbsp;<strong>Realtime Database creada</strong><br>' +
      '&nbsp;&nbsp;&nbsp;&nbsp;console.firebase.google.com → tu proyecto → Compilación → Realtime Database → Crear base de datos<br><br>' +
      '2️⃣ &nbsp;<strong>Reglas en modo público</strong><br>' +
      '&nbsp;&nbsp;&nbsp;&nbsp;Pestaña Reglas → debe decir ".read": true y ".write": true → Publicar<br><br>' +
      '3️⃣ &nbsp;<strong>databaseURL correcta</strong><br>' +
      '&nbsp;&nbsp;&nbsp;&nbsp;Debe ser exactamente:<br>' +
      '&nbsp;&nbsp;&nbsp;&nbsp;<code style="background:rgba(0,0,0,0.3);padding:3px 8px;border-radius:4px;font-size:11px">https://agenda-cesfam-f5f0a-default-rtdb.firebaseio.com</code>' +
      '</div>' +
      '<button onclick="location.reload()" style="margin-top:16px;background:white;color:#1B4F72;border:none;border-radius:10px;padding:12px 24px;font-size:15px;font-weight:700;cursor:pointer;width:100%">🔄 Reintentar</button>' +
      '</div>';
  }, 8000);

  db.ref('profesionales').once('value', function(snap) {
    clearTimeout(timeout);
    if (!snap.val()) {
      cargarDatosEjemplo(function() { mostrarApp(); });
    } else {
      mostrarApp();
    }
  }, function(err) {
    clearTimeout(timeout);
    document.getElementById('pantalla-carga').innerHTML =
      '<div style="text-align:center;padding:24px;max-width:420px">' +
      '<div style="font-size:52px;margin-bottom:14px">🔴</div>' +
      '<h2 style="color:white;margin-bottom:14px;font-size:18px">Error de base de datos</h2>' +
      '<div style="background:rgba(255,255,255,0.12);border-radius:12px;padding:16px;text-align:left;font-size:13px;color:rgba(255,255,255,0.9);line-height:1.8">' +
      '<strong>Error detectado:</strong> ' + err.message + '<br><br>' +
      '✅ Verifica que las Reglas de Realtime Database sean:<br>' +
      '<code style="background:rgba(0,0,0,0.3);padding:4px 8px;border-radius:4px;font-size:11px">{ "rules": { ".read": true, ".write": true } }</code>' +
      '</div>' +
      '<button onclick="location.reload()" style="margin-top:16px;background:white;color:#1B4F72;border:none;border-radius:10px;padding:12px 24px;font-size:15px;font-weight:700;cursor:pointer;width:100%">🔄 Reintentar</button>' +
      '</div>';
  });
}

function mostrarApp() {
  document.getElementById('pantalla-carga').style.display = 'none';
  document.getElementById('encabezado').style.display = 'flex';
  document.getElementById('app').style.display = 'block';
  ir('v-inicio');
}

// ═══════════════════════════════════════════════════
// DATOS DE EJEMPLO (primer uso)
// ═══════════════════════════════════════════════════
function cargarDatosEjemplo(callback) {
  var profs = {
    p1: { nombre: 'Dr. Carlos Vega' },
    p2: { nombre: 'EU. Claudia Muñoz' },
    p3: { nombre: 'KIN. Roberto Herrera' },
    p4: { nombre: 'Mat. Patricia Silva' },
    p5: { nombre: 'Dr. Andrés Rojas' }
  };

  var cupos = {};
  var contador = 1;

  function agregarBloqueLocal(fecha, profId, esp, hIni, hFin, intervalo) {
    var partes = hIni.split(':');
    var h = parseInt(partes[0]);
    var m = parseInt(partes[1]);
    var partesFin = hFin.split(':');
    var fh = parseInt(partesFin[0]);
    var fm = parseInt(partesFin[1]);
    while (h * 60 + m < fh * 60 + fm) {
      var hora = pad(h) + ':' + pad(m);
      var id = 'c' + contador++;
      cupos[id] = { fecha: fecha, hora: hora, profesionalId: profId, especialidad: esp, reservado: false };
      m += intervalo;
      if (m >= 60) { h += Math.floor(m / 60); m = m % 60; }
    }
  }

  var t0 = getFecha(0), t1 = getFecha(1), t2 = getFecha(2), t3 = getFecha(3), t4 = getFecha(4);
  agregarBloqueLocal(t0,'p1','Medicina General','08:00','11:30',30);
  agregarBloqueLocal(t0,'p2','Enfermería','08:30','12:00',20);
  agregarBloqueLocal(t0,'p3','Kinesiología','09:00','12:00',30);
  agregarBloqueLocal(t0,'p4','Matrona','10:00','12:30',30);
  agregarBloqueLocal(t1,'p1','Medicina General','08:00','13:00',30);
  agregarBloqueLocal(t1,'p5','Medicina General','08:00','12:00',30);
  agregarBloqueLocal(t1,'p2','Enfermería','08:00','12:30',20);
  agregarBloqueLocal(t2,'p1','Medicina General','08:00','13:00',30);
  agregarBloqueLocal(t2,'p4','Matrona','08:30','11:30',30);
  agregarBloqueLocal(t3,'p2','Enfermería','08:00','12:00',20);
  agregarBloqueLocal(t3,'p3','Kinesiología','09:00','12:30',30);
  agregarBloqueLocal(t4,'p1','Medicina General','08:00','13:00',30);
  agregarBloqueLocal(t4,'p4','Matrona','09:00','12:00',30);

  var datos = { profesionales: profs, cupos: cupos };
  db.ref().set(datos, function() {
    if (callback) callback();
  });
}

// ═══════════════════════════════════════════════════
// UTILIDADES
// ═══════════════════════════════════════════════════
function pad(n) { return n < 10 ? '0' + n : '' + n; }

function getFecha(offset) {
  var d = new Date();
  d.setDate(d.getDate() + offset);
  return d.toLocaleDateString('en-CA'); // YYYY-MM-DD
}

function hoy() { return getFecha(0); }

function formatearFecha(str) {
  var d = new Date(str + 'T12:00:00');
  return d.toLocaleDateString('es-CL', { weekday: 'long', day: 'numeric', month: 'long' });
}

function formatearFechaCorta(str) {
  var d = new Date(str + 'T12:00:00');
  var wd = d.toLocaleDateString('es-CL', { weekday: 'short' });
  return {
    nom: wd.charAt(0).toUpperCase() + wd.slice(1),
    dia: d.getDate(),
    mes: d.toLocaleDateString('es-CL', { month: 'short' })
  };
}

function formatearRut(input) {
  var v = input.value.replace(/[^0-9kK]/g, '');
  if (v.length > 1) {
    var cuerpo = v.slice(0, -1).replace(/\B(?=(\d{3})+(?!\d))/g, '.');
    input.value = cuerpo + '-' + v.slice(-1).toUpperCase();
  } else {
    input.value = v;
  }
}

function toast(msg) {
  var t = document.getElementById('toast');
  t.textContent = msg;
  t.classList.add('visible');
  setTimeout(function() { t.classList.remove('visible'); }, 2800);
}

// ═══════════════════════════════════════════════════
// NAVEGACIÓN
// ═══════════════════════════════════════════════════
function ir(vistaId) {
  document.querySelectorAll('.vista').forEach(function(v) { v.classList.remove('activa'); });
  document.getElementById(vistaId).classList.add('activa');
  historial.push(vistaId);
  document.getElementById('btn-volver').style.display = vistaId === 'v-inicio' ? 'none' : 'block';
  window.scrollTo(0, 0);

  if (vistaId === 'v-fecha')   iniciarFecha();
  if (vistaId === 'v-cupos')   renderCupos();
  if (vistaId === 'v-admin')   iniciarAdmin();
}

function volver() {
  historial.pop();
  var prev = historial[historial.length - 1] || 'v-inicio';
  historial.pop();
  ir(prev);
}

function inicio() {
  sel.fecha = null; sel.esp = null; sel.cupoId = null;
  limpiarEscuchadores();
  historial = [];
  ir('v-inicio');
}

function limpiarEscuchadores() {
  escuchadores.forEach(function(fn) { fn(); });
  escuchadores = [];
}

// ═══════════════════════════════════════════════════
// PASOS
// ═══════════════════════════════════════════════════
function actualizarPasos(activo) {
  for (var i = 1; i <= 4; i++) {
    var dot = document.getElementById('pd' + i);
    if (!dot) continue;
    if (i < activo) { dot.className = 'paso-dot hecho'; dot.textContent = '✓'; }
    else if (i === activo) { dot.className = 'paso-dot activo'; dot.textContent = i === 4 ? '✓' : i; }
    else { dot.className = 'paso-dot'; dot.textContent = i === 4 ? '✓' : i; }
    var linea = document.getElementById('pl' + i);
    if (linea) linea.className = 'paso-linea' + (i < activo ? ' hecha' : '');
  }
}

// ═══════════════════════════════════════════════════
// PACIENTE: FECHA
// ═══════════════════════════════════════════════════
function iniciarFecha() {
  actualizarPasos(1);
  document.getElementById('input-fecha').min = hoy();

  db.ref('cupos').once('value', function(snap) {
    var cupos = snap.val() || {};
    var gridFechas = document.getElementById('grid-fechas');
    gridFechas.innerHTML = '';

    for (var i = 0; i < 8; i++) {
      var fecha = getFecha(i);
      var haySlots = false;
      Object.values(cupos).forEach(function(c) {
        if (c.fecha === fecha && !c.reservado) haySlots = true;
      });

      var f = formatearFechaCorta(fecha);
      var btn = document.createElement('button');
      btn.className = 'fecha-btn' + (sel.fecha === fecha ? ' sel' : '');
      btn.disabled = !haySlots;
      btn.style.opacity = haySlots ? '1' : '0.4';
      btn.style.cursor = haySlots ? 'pointer' : 'not-allowed';
      btn.innerHTML =
        '<span class="dia-nom">' + f.nom + '</span>' +
        '<span class="dia-num">' + f.dia + '</span>' +
        '<span class="dia-mes">' + f.mes + '</span>';
      (function(fec) {
        btn.onclick = function() { elegirFecha(fec); };
      })(fecha);
      gridFechas.appendChild(btn);
    }

    // Especialidades
    var esps = [];
    Object.values(cupos).forEach(function(c) {
      if (esps.indexOf(c.especialidad) === -1) esps.push(c.especialidad);
    });
    esps.sort();

    var tagsEl = document.getElementById('tags-esp');
    tagsEl.innerHTML = '';
    ['Todas'].concat(esps).forEach(function(esp) {
      var esAll = esp === 'Todas';
      var tag = document.createElement('span');
      tag.className = 'tag' + ((esAll && !sel.esp) || sel.esp === esp ? ' sel' : '');
      tag.textContent = esp;
      tag.onclick = function() {
        sel.esp = esAll ? null : esp;
        iniciarFecha();
      };
      tagsEl.appendChild(tag);
    });

    if (!sel.fecha) elegirFecha(hoy());
  });
}

function elegirFecha(fecha) {
  sel.fecha = fecha;
  iniciarFecha();
}

function elegirFechaManual(val) {
  if (val) { sel.fecha = val; iniciarFecha(); }
}

function irACupos() {
  if (!sel.fecha) { toast('Selecciona una fecha'); return; }
  ir('v-cupos');
}

// ═══════════════════════════════════════════════════
// PACIENTE: CUPOS
// ═══════════════════════════════════════════════════
function renderCupos() {
  actualizarPasos(2);
  var contenedor = document.getElementById('contenedor-cupos');
  contenedor.innerHTML = '<div class="vacio"><div class="vacio-ico">⏳</div><p>Cargando cupos...</p></div>';

  db.ref('cupos').once('value', function(snap) {
    var cupos = snap.val() || {};
    var lista = [];
    Object.entries(cupos).forEach(function(par) {
      var id = par[0], c = par[1];
      if (c.fecha === sel.fecha && !c.reservado) {
        if (!sel.esp || c.especialidad === sel.esp) lista.push(Object.assign({ id: id }, c));
      }
    });
    lista.sort(function(a, b) { return a.hora > b.hora ? 1 : -1; });

    document.getElementById('titulo-cupos').textContent = formatearFecha(sel.fecha);
    document.getElementById('sub-cupos').textContent =
      lista.length + ' cupo' + (lista.length !== 1 ? 's' : '') + ' disponible' + (lista.length !== 1 ? 's' : '');

    if (lista.length === 0) {
      contenedor.innerHTML = '<div class="vacio"><div class="vacio-ico">📭</div><h3>Sin cupos disponibles</h3><p>No hay cupos para esta fecha.</p></div>';
      return;
    }

    // Agrupar por especialidad
    db.ref('profesionales').once('value', function(pSnap) {
      var profs = pSnap.val() || {};
      var grupos = {};
      lista.forEach(function(c) {
        if (!grupos[c.especialidad]) grupos[c.especialidad] = [];
        grupos[c.especialidad].push(c);
      });

      var html = '';
      Object.entries(grupos).forEach(function(par) {
        var esp = par[0], items = par[1];
        html += '<div class="sec-titulo" style="margin-top:14px">' + esp + '</div><div class="cupos-grid">';
        items.forEach(function(c) {
          var profNom = profs[c.profesionalId] ? profs[c.profesionalId].nombre.split(' ').slice(0,2).join(' ') : '';
          html += '<button class="cupo-btn' + (sel.cupoId === c.id ? ' sel' : '') + '" onclick="elegirCupo(\'' + c.id + '\')">' +
            '<span class="cupo-hora">' + c.hora + '</span>' +
            '<span class="cupo-prof">' + profNom + '</span>' +
            '</button>';
        });
        html += '</div>';
      });
      contenedor.innerHTML = html;
    });
  });
}

function elegirCupo(id) {
  sel.cupoId = id;
  actualizarPasos(3);

  db.ref('cupos/' + id).once('value', function(snap) {
    var c = snap.val();
    db.ref('profesionales/' + c.profesionalId).once('value', function(pSnap) {
      var prof = pSnap.val() ? pSnap.val().nombre : '';
      document.getElementById('resumen-cupo').innerHTML =
        '<div class="alerta alerta-info" style="display:flex;align-items:center;gap:12px">' +
        '<span style="font-size:24px">📋</span>' +
        '<div><div style="font-weight:700;font-size:15px">' + c.hora + ' hrs · ' + c.especialidad + '</div>' +
        '<div style="font-size:13px;color:#1B4F72">' + prof + ' · ' + formatearFecha(c.fecha) + '</div></div></div>';
      ir('v-form');
    });
  });
}

// ═══════════════════════════════════════════════════
// PACIENTE: CONFIRMAR RESERVA
// ═══════════════════════════════════════════════════
function confirmar() {
  var nombre = document.getElementById('f-nombre').value.trim();
  var rut    = document.getElementById('f-rut').value.trim();
  var tel    = document.getElementById('f-tel').value.trim();

  if (!nombre) { toast('Ingresa tu nombre completo'); return; }
  if (!rut || rut.length < 7) { toast('Ingresa un RUT válido'); return; }

  var btn = document.getElementById('btn-confirmar');
  btn.disabled = true;
  btn.textContent = 'Guardando...';

  var cupoRef = db.ref('cupos/' + sel.cupoId);

  // Transacción atómica: evita doble reserva
  cupoRef.transaction(function(cupo) {
    if (cupo && !cupo.reservado) {
      cupo.reservado = true;
      return cupo;
    }
    return; // abortar si ya está reservado
  }, function(error, committed, snap) {
    if (error) {
      toast('Error al guardar. Intenta nuevamente.');
      btn.disabled = false; btn.textContent = '✓ Confirmar reserva';
      return;
    }

    if (!committed) {
      toast('⚠️ Este cupo ya fue tomado. Elige otro horario.');
      btn.disabled = false; btn.textContent = '✓ Confirmar reserva';
      ir('v-cupos');
      return;
    }

    var cupoData = snap.val();
    var prefijos = { 'Medicina General':'MED','Enfermería':'ENF','Kinesiología':'KIN','Matrona':'MAT','Nutrición':'NUT' };
    var prefijo = prefijos[cupoData.especialidad] || 'ATN';

    // Generar código único
    db.ref('reservas').once('value', function(rSnap) {
      var total = rSnap.val() ? Object.keys(rSnap.val()).length : 0;
      var codigo = prefijo + '-' + pad3(total + 1);

      var reservaData = {
        cupoId: sel.cupoId,
        nombre: nombre,
        rut: rut,
        telefono: tel,
        codigo: codigo,
        timestamp: new Date().toISOString()
      };

      db.ref('reservas').push(reservaData, function() {
        db.ref('profesionales/' + cupoData.profesionalId).once('value', function(pSnap) {
          var prof = pSnap.val() ? pSnap.val().nombre : '';
          document.getElementById('cod-confirm').textContent = codigo;
          document.getElementById('det-confirm').textContent = cupoData.hora + ' hrs · ' + formatearFecha(cupoData.fecha);
          document.getElementById('detalle-confirm').innerHTML =
            '<div class="sec-titulo">Detalle de tu reserva</div>' +
            '<div class="item-reserva"><span style="color:#718096;font-size:13px;min-width:90px">Especialidad</span><span style="font-weight:600">' + cupoData.especialidad + '</span></div>' +
            '<div class="item-reserva"><span style="color:#718096;font-size:13px;min-width:90px">Profesional</span><span style="font-weight:600">' + prof + '</span></div>' +
            '<div class="item-reserva"><span style="color:#718096;font-size:13px;min-width:90px">Fecha</span><span style="font-weight:600">' + formatearFecha(cupoData.fecha) + '</span></div>' +
            '<div class="item-reserva" style="border:none"><span style="color:#718096;font-size:13px;min-width:90px">Hora</span><span style="font-weight:600">' + cupoData.hora + ' hrs</span></div>';
          actualizarPasos(4);
          ir('v-confirmado');
          btn.disabled = false; btn.textContent = '✓ Confirmar reserva';
        });
      });
    });
  });
}

function pad3(n) { return n < 10 ? '00' + n : n < 100 ? '0' + n : '' + n; }

// ═══════════════════════════════════════════════════
// ADMIN: PIN
// ═══════════════════════════════════════════════════
function verificarPin() {
  var pin = document.getElementById('input-pin').value;
  if (pin === PIN_ADMIN) {
    document.getElementById('input-pin').value = '';
    document.getElementById('error-pin').style.display = 'none';
    ir('v-admin');
  } else {
    document.getElementById('error-pin').style.display = 'block';
    document.getElementById('input-pin').value = '';
  }
}

// ═══════════════════════════════════════════════════
// ADMIN: PANEL
// ═══════════════════════════════════════════════════
function iniciarAdmin() {
  var t = hoy();
  document.getElementById('admin-fecha').value = t;
  document.getElementById('admin-fecha-cupos').value = t;
  document.getElementById('nuevo-fecha').value = t;
  cargarOpcProfesionales();
  cambiarTab('reservas', document.querySelector('.tab.activa'));
  cargarEstadisticas();
  cargarReservas();

  // Escuchar cambios en tiempo real
  limpiarEscuchadores();

  var refCupos = db.ref('cupos');
  var cbCupos = refCupos.on('value', function() {
    cargarEstadisticas();
    cargarCupos();
    cargarReservas();
  });
  escuchadores.push(function() { refCupos.off('value', cbCupos); });

  var refRes = db.ref('reservas');
  var cbRes = refRes.on('value', function() {
    cargarEstadisticas();
    cargarReservas();
  });
  escuchadores.push(function() { refRes.off('value', cbRes); });
}

function cargarEstadisticas() {
  var t = hoy();
  db.ref('cupos').once('value', function(snap) {
    var cupos = snap.val() || {};
    var total = 0, reservados = 0;
    Object.values(cupos).forEach(function(c) {
      if (c.fecha === t) { total++; if (c.reservado) reservados++; }
    });
    document.getElementById('estadisticas').innerHTML =
      '<div class="stat azul"><div class="stat-n">' + total + '</div><div class="stat-l">Cupos hoy</div></div>' +
      '<div class="stat verde"><div class="stat-n">' + (total - reservados) + '</div><div class="stat-l">Disponibles</div></div>' +
      '<div class="stat naranjo"><div class="stat-n">' + reservados + '</div><div class="stat-l">Reservados</div></div>';
  });
}

function cargarReservas() {
  var fecha = document.getElementById('admin-fecha').value;
  document.getElementById('sub-reservas').textContent = formatearFecha(fecha);

  db.ref('cupos').once('value', function(cSnap) {
    var cupos = cSnap.val() || {};
    var cupoDia = [];
    Object.entries(cupos).forEach(function(par) {
      var id = par[0], c = par[1];
      if (c.fecha === fecha && c.reservado) cupoDia.push(Object.assign({ id: id }, c));
    });
    cupoDia.sort(function(a, b) { return a.hora > b.hora ? 1 : -1; });

    db.ref('reservas').once('value', function(rSnap) {
      var reservas = rSnap.val() || {};
      db.ref('profesionales').once('value', function(pSnap) {
        var profs = pSnap.val() || {};
        var lista = document.getElementById('lista-reservas');

        if (cupoDia.length === 0) {
          lista.innerHTML = '<div class="vacio" style="padding:24px 0"><div class="vacio-ico">📭</div><p>Sin reservas para esta fecha</p></div>';
          return;
        }

        var html = '';
        cupoDia.forEach(function(cupo) {
          var res = null;
          Object.values(reservas).forEach(function(r) { if (r.cupoId === cupo.id) res = r; });
          if (!res) return;
          var prof = profs[cupo.profesionalId] ? profs[cupo.profesionalId].nombre : '';
          html += '<div class="item-reserva">' +
            '<div class="item-hora">' + cupo.hora + '</div>' +
            '<div class="item-info">' +
              '<div class="item-nombre">' + res.nombre + '</div>' +
              '<div class="item-rut">' + res.rut + '</div>' +
              '<div style="font-size:11px;color:#a0aec0;margin-top:2px">' + prof + ' · ' + cupo.especialidad + '</div>' +
            '</div>' +
            '<div style="text-align:right">' +
              '<span class="badge badge-ok">' + res.codigo + '</span>' +
              (res.telefono ? '<div style="font-size:11px;color:#718096;margin-top:4px">' + res.telefono + '</div>' : '') +
            '</div>' +
          '</div>';
        });
        lista.innerHTML = html || '<div class="vacio" style="padding:24px 0"><div class="vacio-ico">📭</div><p>Sin reservas para esta fecha</p></div>';
      });
    });
  });
}

function cargarCupos() {
  var fecha = document.getElementById('admin-fecha-cupos').value;
  document.getElementById('sub-cupos-admin').textContent = formatearFecha(fecha);

  db.ref('cupos').once('value', function(cSnap) {
    var cupos = cSnap.val() || {};
    db.ref('profesionales').once('value', function(pSnap) {
      var profs = pSnap.val() || {};
      var lista = [];
      Object.entries(cupos).forEach(function(par) {
        var id = par[0], c = par[1];
        if (c.fecha === fecha) lista.push(Object.assign({ id: id }, c));
      });
      lista.sort(function(a, b) { return a.hora > b.hora ? 1 : -1; });

      var el = document.getElementById('lista-cupos');
      if (lista.length === 0) {
        el.innerHTML = '<div class="vacio" style="padding:24px 0"><div class="vacio-ico">📭</div><p>Sin cupos para esta fecha</p></div>';
        return;
      }

      var html = '';
      lista.forEach(function(c) {
        var prof = profs[c.profesionalId] ? profs[c.profesionalId].nombre : 'Profesional';
        html += '<div class="item-cupo">' +
          '<div style="font-size:17px;font-weight:700;color:#1B4F72;min-width:48px">' + c.hora + '</div>' +
          '<div style="flex:1"><div style="font-size:14px;font-weight:600">' + prof + '</div><div style="font-size:12px;color:#718096">' + c.especialidad + '</div></div>' +
          '<div>' + (c.reservado
            ? '<span class="badge badge-mal">Reservado</span>'
            : '<button class="btn-borrar" onclick="borrarCupo(\'' + c.id + '\')">Eliminar</button>'
          ) + '</div>' +
        '</div>';
      });
      el.innerHTML = html;
    });
  });
}

function borrarCupo(id) {
  if (!confirm('¿Eliminar este cupo? No se puede deshacer.')) return;
  db.ref('cupos/' + id).remove(function() {
    toast('Cupo eliminado ✓');
  });
}

function agregarCupos() {
  var profId    = document.getElementById('nuevo-prof').value;
  var esp       = document.getElementById('nuevo-esp').value;
  var fecha     = document.getElementById('nuevo-fecha').value;
  var ini       = document.getElementById('nuevo-ini').value;
  var fin       = document.getElementById('nuevo-fin').value;
  var intervalo = parseInt(document.getElementById('nuevo-intervalo').value);

  if (!profId) { toast('Selecciona un profesional'); return; }
  if (!fecha)  { toast('Selecciona una fecha'); return; }
  if (!ini || !fin) { toast('Ingresa los horarios'); return; }

  var pIni = ini.split(':');
  var h = parseInt(pIni[0]), m = parseInt(pIni[1]);
  var pFin = fin.split(':');
  var fh = parseInt(pFin[0]), fm = parseInt(pFin[1]);
  var agregados = 0;
  var promesas = [];

  db.ref('cupos').once('value', function(snap) {
    var existentes = snap.val() || {};

    while (h * 60 + m < fh * 60 + fm) {
      var hora = pad(h) + ':' + pad(m);
      var yaExiste = false;
      Object.values(existentes).forEach(function(c) {
        if (c.fecha === fecha && c.profesionalId === profId && c.hora === hora) yaExiste = true;
      });

      if (!yaExiste) {
        var ref = db.ref('cupos').push();
        promesas.push(ref.set({ fecha: fecha, hora: hora, profesionalId: profId, especialidad: esp, reservado: false }));
        agregados++;
      }

      m += intervalo;
      if (m >= 60) { h += Math.floor(m / 60); m = m % 60; }
    }

    if (agregados === 0) { toast('Esos cupos ya existen'); return; }

    Promise.all(promesas).then(function() {
      toast('✓ ' + agregados + ' cupo' + (agregados !== 1 ? 's' : '') + ' guardado' + (agregados !== 1 ? 's' : '') + ' en Firebase');
      cambiarTab('cupos', null);
      document.getElementById('admin-fecha-cupos').value = fecha;
      cargarCupos();
    });
  });
}

function agregarProfesional() {
  var nombre = document.getElementById('nuevo-prof-nombre').value.trim();
  if (!nombre) { toast('Ingresa el nombre del profesional'); return; }
  db.ref('profesionales').push({ nombre: nombre }, function() {
    document.getElementById('nuevo-prof-nombre').value = '';
    cargarOpcProfesionales();
    toast('Profesional agregado ✓');
  });
}

function cargarOpcProfesionales() {
  db.ref('profesionales').once('value', function(snap) {
    var profs = snap.val() || {};
    var select = document.getElementById('nuevo-prof');
    select.innerHTML = '<option value="">Seleccionar profesional...</option>';
    Object.entries(profs).forEach(function(par) {
      var opt = document.createElement('option');
      opt.value = par[0];
      opt.textContent = par[1].nombre;
      select.appendChild(opt);
    });
  });
}

function cambiarTab(tab, btnEl) {
  ['reservas','cupos','agregar'].forEach(function(t) {
    document.getElementById('tab-' + t).style.display = t === tab ? 'block' : 'none';
  });
  document.querySelectorAll('.tab').forEach(function(b) { b.classList.remove('activa'); });
  if (btnEl) { btnEl.classList.add('activa'); }
  else {
    document.querySelectorAll('.tab').forEach(function(b, i) {
      if (['reservas','cupos','agregar'][i] === tab) b.classList.add('activa');
    });
  }
}
</script>
</body>
</html>
