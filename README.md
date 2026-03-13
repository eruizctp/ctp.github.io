
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Flujo Venta Online · Hacienda Vichuquén</title>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
<style>
  * { margin: 0; padding: 0; box-sizing: border-box; }
  body { background: #F4F6F8; font-family: 'Inter', sans-serif; color: #1A1A1A; min-height: 100vh; }

  nav {
    background: #fff;
    border-bottom: 1px solid #E5E7EB;
    padding: 0 40px;
    height: 64px;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  .nav-logo { display: flex; align-items: center; gap: 10px; font-weight: 700; font-size: 16px; color: #111; }
  .nav-logo .icon { width: 32px; height: 32px; background: #111; border-radius: 8px; display: flex; align-items: center; justify-content: center; color: #fff; font-size: 12px; font-weight: 800; }
  .nav-badge { background: #F3F4F6; color: #6B7280; font-size: 11px; font-weight: 500; padding: 4px 12px; border-radius: 100px; }

  .page-header { background: #fff; border-bottom: 1px solid #E5E7EB; padding: 40px 40px 36px; }
  .page-header h1 { font-size: 32px; font-weight: 800; color: #111; letter-spacing: -0.5px; }
  .page-header p { margin-top: 6px; font-size: 15px; color: #6B7280; }

  .main { max-width: 860px; margin: 0 auto; padding: 40px 24px 80px; }

  .phase { margin-bottom: 8px; }
  .phase-header { display: flex; align-items: center; gap: 12px; margin-bottom: 10px; }
  .phase-num { width: 28px; height: 28px; border-radius: 50%; background: #111; color: #fff; font-size: 13px; font-weight: 700; display: flex; align-items: center; justify-content: center; flex-shrink: 0; }
  .phase-num.alt { background: #FFF7ED; color: #EA580C; border: 2px dashed #FED7AA; }
  .phase-title { font-size: 13px; font-weight: 600; color: #374151; text-transform: uppercase; letter-spacing: 0.08em; }
  .platform-chip { margin-left: auto; font-size: 11px; font-weight: 500; color: #6B7280; background: #F3F4F6; padding: 3px 10px; border-radius: 100px; border: 1px solid #E5E7EB; }

  .card { background: #fff; border: 1px solid #E5E7EB; border-radius: 12px; padding: 4px 24px 4px; margin-left: 40px; }

  .step { display: flex; align-items: flex-start; gap: 14px; padding: 16px 0; border-bottom: 1px solid #F3F4F6; }
  .step:last-child { border-bottom: none; }
  .step-icon { width: 36px; height: 36px; border-radius: 8px; background: #F9FAFB; border: 1px solid #E5E7EB; display: flex; align-items: center; justify-content: center; font-size: 16px; flex-shrink: 0; margin-top: 1px; }
  .step-title { font-size: 14px; font-weight: 600; color: #111; }
  .step-desc { margin-top: 3px; font-size: 13px; color: #6B7280; line-height: 1.55; }

  .fork-wrapper { padding: 12px 0 16px; border-top: 1px solid #F3F4F6; margin-top: 4px; }
  .fork-intro { font-size: 13px; color: #6B7280; margin-bottom: 12px; }
  .fork { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; }
  .fork-branch { background: #F9FAFB; border: 1px solid #E5E7EB; border-radius: 10px; padding: 14px 16px; }
  .fork-branch.active { background: #EFF6FF; border-color: #BFDBFE; }
  .fork-label { font-size: 10px; font-weight: 700; text-transform: uppercase; letter-spacing: 0.1em; color: #9CA3AF; margin-bottom: 10px; }
  .fork-branch.active .fork-label { color: #3B82F6; }
  .fork-step { display: flex; align-items: flex-start; gap: 8px; padding: 7px 0; border-bottom: 1px solid #E5E7EB; font-size: 12px; color: #374151; font-weight: 500; line-height: 1.4; }
  .fork-branch.active .fork-step { border-bottom-color: #DBEAFE; }
  .fork-step:last-child { border-bottom: none; padding-bottom: 0; }
  .fork-step-icon { flex-shrink: 0; margin-top: 1px; }

  .connector { display: flex; align-items: center; padding: 4px 0 4px 53px; color: #D1D5DB; font-size: 18px; }

  .end-card { background: #111; border-radius: 12px; padding: 18px 24px; display: flex; align-items: center; justify-content: space-between; margin-left: 40px; }
  .end-left { display: flex; align-items: center; gap: 12px; }
  .end-dot { width: 10px; height: 10px; border-radius: 50%; background: #22C55E; }
  .end-card span { font-size: 14px; font-weight: 600; color: #fff; }
  .end-card small { font-size: 12px; color: #6B7280; }

  .retract-card { background: #FFF7ED; border: 1.5px solid #FED7AA; border-radius: 12px; padding: 20px 24px; margin-left: 40px; }
  .retract-label { display: flex; align-items: center; gap: 6px; font-size: 11px; font-weight: 700; color: #EA580C; text-transform: uppercase; letter-spacing: 0.1em; margin-bottom: 12px; }
  .retract-step { display: flex; align-items: center; gap: 10px; padding: 9px 0; border-bottom: 1px solid #FED7AA; font-size: 13px; color: #374151; font-weight: 500; }
  .retract-step:last-child { border-bottom: none; padding-bottom: 0; }

  .legend { margin-top: 40px; display: flex; gap: 18px; flex-wrap: wrap; padding: 18px 20px; background: #fff; border: 1px solid #E5E7EB; border-radius: 12px; }
  .legend-title { width: 100%; font-size: 10px; font-weight: 700; color: #9CA3AF; text-transform: uppercase; letter-spacing: 0.1em; }
  .legend-item { display: flex; align-items: center; gap: 7px; font-size: 12px; color: #6B7280; }
  .legend-dot { width: 8px; height: 8px; border-radius: 50%; flex-shrink: 0; }

  @media (max-width: 600px) {
    nav { padding: 0 20px; }
    .page-header { padding: 28px 20px; }
    .main { padding: 24px 16px 60px; }
    .fork { grid-template-columns: 1fr; }
    .card, .retract-card, .end-card { margin-left: 0; }
    .connector { padding-left: 0; }
  }
</style>
</head>
<body>

<nav>
  <div class="nav-logo">
    <div class="icon">HV</div>
    Hacienda Vichuquén
  </div>
  <div class="nav-badge">Interno · Marketing</div>
</nav>

<div class="page-header">
  <h1>Flujo de venta online</h1>
  <p>Pasos que sigue el cliente desde que nos descubre hasta confirmar su reserva de parcela.</p>
</div>

<div class="main">

  <!-- FASE 1 -->
  <div class="phase">
    <div class="phase-header">
      <div class="phase-num">1</div>
      <div class="phase-title">Descubrimiento</div>
      <div class="platform-chip">YouTube Live</div>
    </div>
    <div class="card">
      <div class="step">
        <div class="step-icon">▶️</div>
        <div>
          <div class="step-title">Asiste al Live en YouTube</div>
          <div class="step-desc">El cliente interesado descubre el proyecto y la oferta de parcelas a través del live de venta online.</div>
        </div>
      </div>
      <div class="step">
        <div class="step-icon">🔗</div>
        <div>
          <div class="step-title">Ingresa al link del chat o escanea el QR</div>
          <div class="step-desc">Desde el live se comparte un enlace o código QR que lo lleva directamente al formulario.</div>
        </div>
      </div>
    </div>
  </div>

  <div class="connector">↓</div>

  <!-- FASE 2 -->
  <div class="phase">
    <div class="phase-header">
      <div class="phase-num">2</div>
      <div class="phase-title">Registro</div>
      <div class="platform-chip">Fillout · Landing</div>
    </div>
    <div class="card">
      <div class="step">
        <div class="step-icon">📋</div>
        <div>
          <div class="step-title">Completa el formulario en Fillout</div>
          <div class="step-desc">Ingresa nombre y apellido, RUT, teléfono, correo y parcela de preferencia (opcional).</div>
        </div>
      </div>
      <div class="step">
        <div class="step-icon">➡️</div>
        <div>
          <div class="step-title">Presiona "Ir a reservar"</div>
          <div class="step-desc">Con el formulario completo, avanza al paso de pago para formalizar la reserva.</div>
        </div>
      </div>
    </div>
  </div>

  <div class="connector">↓</div>

  <!-- FASE 3 -->
  <div class="phase">
    <div class="phase-header">
      <div class="phase-num">3</div>
      <div class="phase-title">Pago de la reserva</div>
      <div class="platform-chip">Getnet · Transferencia</div>
    </div>
    <div class="card">
      <div class="step" style="border-bottom:none; padding-bottom:0;">
        <div class="step-icon">💳</div>
        <div>
          <div class="step-title">Elige método de pago</div>
          <div class="step-desc">El cliente selecciona entre dos opciones disponibles:</div>
        </div>
      </div>
      <div class="fork-wrapper">
        <div class="fork">
          <div class="fork-branch">
            <div class="fork-label">Opción A · Transferencia</div>
            <div class="fork-step"><span class="fork-step-icon">🏦</span> Se muestran los datos de cuenta para transferir</div>
            <div class="fork-step"><span class="fork-step-icon">📤</span> Realiza la transferencia y envía comprobante por WhatsApp</div>
          </div>
          <div class="fork-branch active">
            <div class="fork-label">Opción B · Tarjeta crédito / débito</div>
            <div class="fork-step"><span class="fork-step-icon">💳</span> Ingresa datos de tarjeta en la plataforma Getnet</div>
            <div class="fork-step"><span class="fork-step-icon">✅</span> Realiza el pago y se genera comprobante automático</div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div class="connector">↓</div>

  <!-- FASE 4 -->
  <div class="phase">
    <div class="phase-header">
      <div class="phase-num">4</div>
      <div class="phase-title">Seguimiento comercial</div>
      <div class="platform-chip">WhatsApp · CRM</div>
    </div>
    <div class="card">
      <div class="step">
        <div class="step-icon">🤝</div>
        <div>
          <div class="step-title">Jefe de ventas toma contacto</div>
          <div class="step-desc">Una vez confirmada la reserva, el equipo comercial se comunica con el cliente para avanzar con el proceso.</div>
        </div>
      </div>
      <div class="step">
        <div class="step-icon">📅</div>
        <div>
          <div class="step-title">Agenda visita al terreno</div>
          <div class="step-desc">Se coordina la visita a Hacienda Vichuquén para que el cliente conozca la parcela en terreno.</div>
        </div>
      </div>
      <div class="step">
        <div class="step-icon">📝</div>
        <div>
          <div class="step-title">Rellena formulario y confirma la venta</div>
          <div class="step-desc">El equipo comercial registra la operación y da continuidad al flujo en el CRM.</div>
        </div>
      </div>
    </div>
  </div>

  <div class="connector">↓</div>

  <!-- FIN -->
  <div class="phase" style="margin-bottom: 40px;">
    <div class="phase-header">
      <div class="phase-num" style="background:#22C55E;">✓</div>
      <div class="phase-title">Venta confirmada</div>
    </div>
    <div class="end-card">
      <div class="end-left">
        <div class="end-dot"></div>
        <span>Continúa el flujo en el CRM</span>
      </div>
      <small>Fin del proceso online</small>
    </div>
  </div>

  <!-- RETRACTO -->
  <div class="phase">
    <div class="phase-header">
      <div class="phase-num alt">!</div>
      <div class="phase-title">Caso especial · Retracto</div>
    </div>
    <div class="retract-card">
      <div class="retract-label">⚠️ Proceso de retracto</div>
      <div class="retract-step">↩&nbsp; El cliente solicita retractarse de la reserva</div>
      <div class="retract-step">📄&nbsp; Se arma el documento de retracto</div>
      <div class="retract-step">💰&nbsp; Se devuelve el dinero al cliente</div>
    </div>
  </div>

  <!-- LEGEND -->
  <div class="legend">
    <div class="legend-title">Referencias</div>
    <div class="legend-item"><div class="legend-dot" style="background:#111;"></div> Flujo principal</div>
    <div class="legend-item"><div class="legend-dot" style="background:#3B82F6;"></div> Pago con tarjeta (Getnet)</div>
    <div class="legend-item"><div class="legend-dot" style="background:#9CA3AF;"></div> Pago por transferencia</div>
    <div class="legend-item"><div class="legend-dot" style="background:#22C55E;"></div> Venta confirmada</div>
    <div class="legend-item"><div class="legend-dot" style="background:#EA580C;"></div> Retracto</div>
  </div>

</div>
</body>
</html>
