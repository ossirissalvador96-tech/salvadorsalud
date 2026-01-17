# salvadorsalud

<html lang="es">
<head>
<meta charset="UTF-8">
<title>NutriBalance Salvador</title>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Inter:wght@400;500;600&display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
<style>
:root {
  --primary: #5D5FEF;
  --secondary: #EF5DA8;
  --accent: #00D4AA;
  --dark: #121826;
  --light: #F8FAFC;
  --gray: #94A3B8;
  --border-radius: 16px;
  --box-shadow: 0 10px 30px rgba(0, 0, 0, 0.08);
  --transition: all 0.3s ease;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Inter', sans-serif;
}

body {
  background: linear-gradient(135deg, #F0F4FF 0%, #F9F5FF 100%);
  color: var(--dark);
  min-height: 100vh;
  line-height: 1.6;
}

/* HEADER */
.hero-section {
  background: linear-gradient(90deg, var(--dark) 0%, #2D3748 100%);
  color: white;
  padding: 4rem 2rem;
  text-align: center;
  position: relative;
  overflow: hidden;
}

.hero-section::before {
  content: '';
  position: absolute;
  width: 300px;
  height: 300px;
  background: radial-gradient(circle, rgba(93, 95, 239, 0.2) 0%, transparent 70%);
  top: -100px;
  right: -100px;
}

.hero-section h1 {
  font-family: 'Poppins', sans-serif;
  font-size: 3.5rem;
  font-weight: 700;
  margin-bottom: 0.5rem;
  background: linear-gradient(90deg, var(--accent), var(--primary));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.hero-tagline {
  font-size: 1.2rem;
  opacity: 0.9;
  max-width: 700px;
  margin: 0 auto;
}

/* CONTAINER */
.container {
  max-width: 1400px;
  margin: 0 auto;
  padding: 2rem;
}

/* GRID SISTEM */
.dashboard-grid {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  gap: 1.5rem;
  margin-bottom: 2rem;
}

/* TARJETAS */
.card {
  background: white;
  border-radius: var(--border-radius);
  padding: 2rem;
  box-shadow: var(--box-shadow);
  transition: var(--transition);
  border: 1px solid rgba(0, 0, 0, 0.05);
}

.card:hover {
  transform: translateY(-5px);
  box-shadow: 0 15px 40px rgba(0, 0, 0, 0.12);
}

.card-title {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  margin-bottom: 1.5rem;
  font-family: 'Poppins', sans-serif;
  font-size: 1.5rem;
  font-weight: 600;
  color: var(--dark);
}

.card-title i {
  color: var(--primary);
  font-size: 1.3rem;
}

/* FORMULARIOS */
.input-group {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  margin-bottom: 1.5rem;
}

.input-row {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 1rem;
}

.input-field {
  position: relative;
}

.input-field label {
  display: block;
  margin-bottom: 0.5rem;
  font-weight: 500;
  color: var(--dark);
}

.input-field input, .input-field select {
  width: 100%;
  padding: 0.85rem 1rem;
  border: 2px solid #E2E8F0;
  border-radius: 10px;
  font-size: 1rem;
  transition: var(--transition);
  background: white;
}

.input-field input:focus, .input-field select:focus {
  outline: none;
  border-color: var(--primary);
  box-shadow: 0 0 0 3px rgba(93, 95, 239, 0.1);
}

/* BOTONES */
.btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 0.5rem;
  padding: 0.85rem 1.75rem;
  border: none;
  border-radius: 10px;
  font-weight: 600;
  font-size: 1rem;
  cursor: pointer;
  transition: var(--transition);
}

.btn-primary {
  background: linear-gradient(90deg, var(--primary), #7879F1);
  color: white;
}

.btn-primary:hover {
  background: linear-gradient(90deg, #7879F1, var(--primary));
  transform: translateY(-2px);
}

.btn-secondary {
  background: var(--accent);
  color: white;
}

.btn-secondary:hover {
  background: #00C29A;
  transform: translateY(-2px);
}

.btn-danger {
  background: #FF6B8B;
  color: white;
}

.btn-danger:hover {
  background: #FF5577;
}

.btn-warning {
  background: #FFA94D;
  color: white;
}

.btn-warning:hover {
  background: #FF983D;
}

.btn-small {
  padding: 0.5rem 1rem;
  font-size: 0.9rem;
}

.action-buttons {
  display: flex;
  gap: 0.5rem;
}

/* TABLAS REDISEÑADAS */
.data-table {
  width: 100%;
  border-collapse: separate;
  border-spacing: 0;
  margin-top: 1.5rem;
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
}

.data-table thead {
  background: linear-gradient(90deg, var(--dark), #2D3748);
  color: white;
}

.data-table th {
  padding: 1.2rem 1rem;
  text-align: left;
  font-weight: 600;
  font-family: 'Poppins', sans-serif;
}

.data-table tbody tr {
  border-bottom: 1px solid #F1F5F9;
  transition: var(--transition);
}

.data-table tbody tr:hover {
  background-color: #F8FAFC;
}

.data-table td {
  padding: 1.2rem 1rem;
  color: #334155;
}

/* BADGES IMC */
.status-badge {
  display: inline-block;
  padding: 0.4rem 1rem;
  border-radius: 20px;
  font-size: 0.85rem;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

.status-low {
  background: linear-gradient(90deg, #FFD166, #FFC145);
  color: #7A5000;
}

.status-normal {
  background: linear-gradient(90deg, #06D6A0, #00C29A);
  color: #00533A;
}

.status-high {
  background: linear-gradient(90deg, #EF476F, #E83A5F);
  color: #7A0026;
}

/* CALCULADORA DE CALORÍAS */
.calculator-container {
  background: linear-gradient(135deg, #F0F9FF 0%, #FEF7FF 100%);
  border-radius: var(--border-radius);
  padding: 2rem;
  border: 1px solid rgba(93, 95, 239, 0.1);
}

.calculator-result {
  background: white;
  border-radius: 12px;
  padding: 1.5rem;
  margin-top: 1.5rem;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
  display: none;
}

.calculator-result.active {
  display: block;
  animation: fadeIn 0.5s ease;
}

.result-value {
  font-size: 2.5rem;
  font-weight: 700;
  color: var(--primary);
  margin: 0.5rem 0;
}

.result-label {
  color: var(--gray);
  font-size: 0.95rem;
}

/* RECOMENDACIONES */
.recommendations-container {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 1.5rem;
  margin-top: 1.5rem;
}

.recommendation-card {
  background: white;
  border-radius: 12px;
  padding: 1.5rem;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
  border-left: 4px solid var(--accent);
  transition: var(--transition);
}

.recommendation-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
}

.recommendation-icon {
  width: 50px;
  height: 50px;
  background: linear-gradient(135deg, var(--primary), #7879F1);
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 1rem;
  color: white;
  font-size: 1.3rem;
}

/* FOOTER */
.footer {
  background: var(--dark);
  color: white;
  padding: 3rem 2rem;
  text-align: center;
  margin-top: 4rem;
}

.footer-content {
  max-width: 800px;
  margin: 0 auto;
}

.footer-logo {
  font-family: 'Poppins', sans-serif;
  font-size: 2rem;
  font-weight: 700;
  margin-bottom: 1rem;
  background: linear-gradient(90deg, var(--accent), var(--secondary));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.footer-copyright {
  color: var(--gray);
  margin-top: 1.5rem;
}

/* ANIMACIONES */
@keyframes fadeIn {
  from { opacity: 0; transform: translateY(10px); }
  to { opacity: 1; transform: translateY(0); }
}

/* RESPONSIVE */
@media (max-width: 1200px) {
  .dashboard-grid {
    grid-template-columns: repeat(6, 1fr);
  }
  
  .span-6 { grid-column: span 6; }
  .span-4 { grid-column: span 6; }
  .span-8 { grid-column: span 6; }
}

@media (max-width: 768px) {
  .hero-section h1 {
    font-size: 2.5rem;
  }
  
  .dashboard-grid {
    grid-template-columns: 1fr;
  }
  
  .span-6, .span-4, .span-8 {
    grid-column: span 1;
  }
  
  .input-row {
    grid-template-columns: 1fr;
  }
}
</style>
</head>

<body>

<!-- HEADER -->
<section class="hero-section">
  <h1>NutriBalance Pro</h1>
  <p class="hero-tagline">Control nutricional avanzado • Cálculo de requerimientos • Recomendaciones personalizadas</p>
</section>

<!-- CONTENIDO PRINCIPAL -->
<div class="container">
  <div class="dashboard-grid">
    
    <!-- REGISTRO DE PACIENTES (izquierda) -->
    <div class="card span-6">
      <div class="card-title">
        <i class="fas fa-user-plus"></i>
        <h2>Registro de Pacientes</h2>
      </div>
      
      <div class="input-group">
        <div class="input-row">
          <div class="input-field">
            <label for="pnombre">Nombre completo</label>
            <input type="text" id="pnombre" placeholder="Ej: Ana López">
          </div>
          
          <div class="input-field">
            <label for="pedad">Edad</label>
            <input type="number" id="pedad" placeholder="Ej: 32">
          </div>
        </div>
        
        <div class="input-row">
          <div class="input-field">
            <label for="pmeta">Objetivo del paciente</label>
            <select id="pmeta">
              <option value="">Seleccione un objetivo</option>
              <option value="Perder peso">Perder peso</option>
              <option value="Ganar masa muscular">Ganar masa muscular</option>
              <option value="Mantener peso">Mantener peso</option>
              <option value="Mejorar salud general">Mejorar salud general</option>
            </select>
          </div>
          
          <div class="input-field">
            <label for="pgenero">Género</label>
            <select id="pgenero">
              <option value="Femenino">Femenino</option>
              <option value="Masculino">Masculino</option>
            </select>
          </div>
        </div>
        
        <button class="btn btn-primary" onclick="guardarPaciente()">
          <i class="fas fa-save"></i> Guardar paciente
        </button>
      </div>
      
      <div class="table-container">
        <table class="data-table">
          <thead>
            <tr>
              <th>Nombre</th>
              <th>Edad</th>
              <th>Género</th>
              <th>Objetivo</th>
              <th>Acciones</th>
            </tr>
          </thead>
          <tbody id="pacientesTabla"></tbody>
        </table>
      </div>
    </div>
    
    <!-- EVALUACIÓN IMC (derecha) -->
    <div class="card span-6">
      <div class="card-title">
        <i class="fas fa-weight-scale"></i>
        <h2>Evaluación Corporal</h2>
      </div>
      
      <div class="input-group">
        <div class="input-row">
          <div class="input-field">
            <label for="inombre">Nombre del paciente</label>
            <input type="text" id="inombre" placeholder="Buscar paciente registrado">
          </div>
          
          <div class="input-field">
            <label for="ipeso">Peso (kg)</label>
            <input type="number" id="ipeso" step="0.1" placeholder="Ej: 68.5">
          </div>
          
          <div class="input-field">
            <label for="ialtura">Altura (m)</label>
            <input type="number" id="ialtura" step="0.01" placeholder="Ej: 1.72">
          </div>
        </div>
        
        <button class="btn btn-secondary" onclick="guardarIMC()">
          <i class="fas fa-calculator"></i> Calcular y guardar
        </button>
      </div>
      
      <div class="table-container">
        <table class="data-table">
          <thead>
            <tr>
              <th>Paciente</th>
              <th>IMC</th>
              <th>Estado</th>
              <th>Recomendación</th>
              <th>Acciones</th>
            </tr>
          </thead>
          <tbody id="imcTabla"></tbody>
        </table>
      </div>
    </div>
    
    <!-- CALCULADORA DE CALORÍAS (abajo izquierda) -->
    <div class="card span-8">
      <div class="card-title">
        <i class="fas fa-fire"></i>
        <h2>Calculadora de Requerimientos Nutricionales</h2>
      </div>
      
      <div class="calculator-container">
        <div class="input-group">
          <div class="input-row">
            <div class="input-field">
              <label for="ccal-edad">Edad</label>
              <input type="number" id="ccal-edad" placeholder="Ej: 35">
            </div>
            
            <div class="input-field">
              <label for="ccal-genero">Género</label>
              <select id="ccal-genero">
                <option value="Femenino">Femenino</option>
                <option value="Masculino">Masculino</option>
              </select>
            </div>
            
            <div class="input-field">
              <label for="ccal-peso">Peso (kg)</label>
              <input type="number" id="ccal-peso" step="0.1" placeholder="Ej: 70.5">
            </div>
            
            <div class="input-field">
              <label for="ccal-altura">Altura (cm)</label>
              <input type="number" id="ccal-altura" placeholder="Ej: 172">
            </div>
          </div>
          
          <div class="input-row">
            <div class="input-field">
              <label for="ccal-actividad">Nivel de actividad</label>
              <select id="ccal-actividad">
                <option value="1.2">Sedentario (poco o ningún ejercicio)</option>
                <option value="1.375">Ligero (ejercicio 1-3 días/semana)</option>
                <option value="1.55" selected>Moderado (ejercicio 3-5 días/semana)</option>
                <option value="1.725">Activo (ejercicio 6-7 días/semana)</option>
                <option value="1.9">Muy activo (ejercicio intenso diario)</option>
              </select>
            </div>
            
            <div class="input-field">
              <label for="ccal-objetivo">Objetivo</label>
              <select id="ccal-objetivo">
                <option value="mantener">Mantener peso</option>
                <option value="bajar">Bajar de peso</option>
                <option value="subir">Subir de peso/masa muscular</option>
              </select>
            </div>
          </div>
          
          <button class="btn btn-primary" onclick="calcularCalorias()">
            <i class="fas fa-calculator"></i> Calcular requerimientos
          </button>
        </div>
        
        <div id="caloriasResultado" class="calculator-result">
          <h3>Resultados de tu cálculo</h3>
          <div class="input-row">
            <div class="input-field">
              <div class="result-label">Calorías diarias necesarias</div>
              <div class="result-value" id="caloriasTotal">0</div>
              <div class="result-label">kcal/día</div>
            </div>
            
            <div class="input-field">
              <div class="result-label">Carbohidratos recomendados</div>
              <div class="result-value" id="carbohidratosTotal">0</div>
              <div class="result-label">gramos/día</div>
            </div>
            
            <div class="input-field">
              <div class="result-label">Proteínas recomendadas</div>
              <div class="result-value" id="proteinasTotal">0</div>
              <div class="result-label">gramos/día</div>
            </div>
            
            <div class="input-field">
              <div class="result-label">Grasas recomendadas</div>
              <div class="result-value" id="grasasTotal">0</div>
              <div class="result-label">gramos/día</div>
            </div>
          </div>
          
          <div class="input-field" style="margin-top: 1rem;">
            <div class="result-label">Recomendación personalizada</div>
            <div id="recomendacionPersonalizada"></div>
          </div>
        </div>
      </div>
    </div>
    
    <!-- RECOMENDACIONES (abajo derecha) -->
    <div class="card span-4">
      <div class="card-title">
        <i class="fas fa-heart-circle-check"></i>
        <h2>Recomendaciones Saludables</h2>
      </div>
      
      <p>Consejos para mantener un estilo de vida saludable y balanceado:</p>
      
      <div class="recommendations-container">
        <div class="recommendation-card">
          <div class="recommendation-icon">
            <i class="fas fa-glass-water"></i>
          </div>
          <h3>Hidratación adecuada</h3>
          <p>Bebe al menos 2 litros de agua al día. La hidratación mejora el metabolismo y la función cerebral.</p>
        </div>
        
        <div class="recommendation-card">
          <div class="recommendation-icon">
            <i class="fas fa-apple-whole"></i>
          </div>
          <h3>Comidas balanceadas</h3>
          <p>Incluye proteínas, carbohidratos complejos y grasas saludables en cada comida principal.</p>
        </div>
        
        <div class="recommendation-card">
          <div class="recommendation-icon">
            <i class="fas fa-moon"></i>
          </div>
          <h3>Sueño de calidad</h3>
          <p>Duerme 7-9 horas diarias. El descanso adecuado es esencial para la recuperación y regulación hormonal.</p>
        </div>
        
        <div class="recommendation-card">
          <div class="recommendation-icon">
            <i class="fas fa-dumbbell"></i>
          </div>
          <h3>Actividad regular</h3>
          <p>Realiza al menos 150 minutos de actividad moderada o 75 minutos de actividad intensa por semana.</p>
        </div>
        
        <div class="recommendation-card">
          <div class="recommendation-icon">
            <i class="fas fa-carrot"></i>
          </div>
          <h3>Fibra suficiente</h3>
          <p>Consume 25-30g de fibra diaria de frutas, verduras, legumbres y cereales integrales.</p>
        </div>
        
        <div class="recommendation-card">
          <div class="recommendation-icon">
            <i class="fas fa-brain"></i>
          </div>
          <h3>Salud mental</h3>
          <p>Practica técnicas de manejo del estrés como meditación, respiración profunda o yoga.</p>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- FOOTER -->
<footer class="footer">
  <div class="footer-content">
    <div class="footer-logo">NutriBalance Salvador</div>
    <p>Tu aliado en nutrición y salud integral. Herramientas profesionales para el cuidado nutricional personalizado.</p>
    <div class="footer-copyright">PROYECTO DE MODULO FELIZA MATEO</div>
  </div>
</footer>

<script>
// Datos almacenados
let pacientes = [], imcs = [];
let editP = -1, editI = -1;

// FUNCIONES PARA PACIENTES
function guardarPaciente() {
  const nombre = document.getElementById('pnombre').value.trim();
  const edad = document.getElementById('pedad').value;
  const meta = document.getElementById('pmeta').value;
  const genero = document.getElementById('pgenero').value;
  
  if (!nombre || !edad || !meta) {
    alert('Por favor completa todos los campos requeridos');
    return;
  }
  
  const obj = {
    id: Date.now(),
    nombre,
    edad,
    genero,
    meta
  };
  
  if (editP >= 0) {
    pacientes[editP] = obj;
    editP = -1;
  } else {
    pacientes.push(obj);
  }
  
  // Limpiar formulario
  document.getElementById('pnombre').value = '';
  document.getElementById('pedad').value = '';
  document.getElementById('pmeta').value = '';
  
  renderPacientes();
}

function renderPacientes() {
  const tabla = document.getElementById('pacientesTabla');
  tabla.innerHTML = '';
  
  pacientes.forEach((p, i) => {
    const fila = document.createElement('tr');
    
    fila.innerHTML = `
      <td>${p.nombre}</td>
      <td>${p.edad} años</td>
      <td>${p.genero}</td>
      <td>${p.meta}</td>
      <td>
        <div class="action-buttons">
          <button class="btn btn-warning btn-small" onclick="editarPaciente(${i})">
            <i class="fas fa-edit"></i>
          </button>
          <button class="btn btn-danger btn-small" onclick="eliminarPaciente(${i})">
            <i class="fas fa-trash"></i>
          </button>
        </div>
      </td>
    `;
    
    tabla.appendChild(fila);
  });
}

function editarPaciente(i) {
  const p = pacientes[i];
  document.getElementById('pnombre').value = p.nombre;
  document.getElementById('pedad').value = p.edad;
  document.getElementById('pmeta').value = p.meta;
  document.getElementById('pgenero').value = p.genero;
  editP = i;
  
  // Scroll al formulario
  document.getElementById('pnombre').scrollIntoView({ behavior: 'smooth' });
}

function eliminarPaciente(i) {
  if (confirm('¿Estás seguro de que quieres eliminar este paciente?')) {
    pacientes.splice(i, 1);
    renderPacientes();
  }
}

// FUNCIONES PARA IMC
function guardarIMC() {
  const nombre = document.getElementById('inombre').value.trim();
  const peso = parseFloat(document.getElementById('ipeso').value);
  const altura = parseFloat(document.getElementById('ialtura').value);
  
  if (!nombre || !peso || !altura || altura <= 0) {
    alert('Por favor completa todos los campos con valores válidos');
    return;
  }
  
  const imc = (peso / (altura ** 2)).toFixed(2);
  let estado, clase, recomendacion;
  
  if (imc < 18.5) {
    estado = 'Bajo peso';
    clase = 'status-low';
    recomendacion = 'Consulta con un especialista para aumentar peso de forma saludable';
  } else if (imc < 25) {
    estado = 'Normal';
    clase = 'status-normal';
    recomendacion = 'Mantén tus hábitos actuales y realiza actividad física regular';
  } else if (imc < 30) {
    estado = 'Sobrepeso';
    clase = 'status-high';
    recomendacion = 'Considera reducir el consumo de alimentos procesados y aumentar actividad física';
  } else {
    estado = 'Obesidad';
    clase = 'status-high';
    recomendacion = 'Consulta con un profesional de la salud para un plan personalizado';
  }
  
  const obj = {
    id: Date.now(),
    nombre,
    imc,
    estado,
    clase,
    recomendacion,
    peso,
    altura
  };
  
  if (editI >= 0) {
    imcs[editI] = obj;
    editI = -1;
  } else {
    imcs.push(obj);
  }
  
  // Limpiar formulario
  document.getElementById('inombre').value = '';
  document.getElementById('ipeso').value = '';
  document.getElementById('ialtura').value = '';
  
  renderIMC();
}

function renderIMC() {
  const tabla = document.getElementById('imcTabla');
  tabla.innerHTML = '';
  
  imcs.forEach((x, i) => {
    const fila = document.createElement('tr');
    
    fila.innerHTML = `
      <td>${x.nombre}</td>
      <td><strong>${x.imc}</strong></td>
      <td><span class="status-badge ${x.clase}">${x.estado}</span></td>
      <td>${x.recomendacion}</td>
      <td>
        <div class="action-buttons">
          <button class="btn btn-warning btn-small" onclick="editarIMC(${i})">
            <i class="fas fa-edit"></i>
          </button>
          <button class="btn btn-danger btn-small" onclick="eliminarIMC(${i})">
            <i class="fas fa-trash"></i>
          </button>
        </div>
      </td>
    `;
    
    tabla.appendChild(fila);
  });
}

function editarIMC(i) {
  const x = imcs[i];
  document.getElementById('inombre').value = x.nombre;
  document.getElementById('ipeso').value = x.peso;
  document.getElementById('ialtura').value = x.altura;
  editI = i;
  
  // Scroll al formulario
  document.getElementById('inombre').scrollIntoView({ behavior: 'smooth' });
}

function eliminarIMC(i) {
  if (confirm('¿Estás seguro de que quieres eliminar este registro de IMC?')) {
    imcs.splice(i, 1);
    renderIMC();
  }
}

// CALCULADORA DE CALORÍAS Y CARBOHIDRATOS
function calcularCalorias() {
  const edad = parseInt(document.getElementById('ccal-edad').value);
  const genero = document.getElementById('ccal-genero').value;
  const peso = parseFloat(document.getElementById('ccal-peso').value);
  const altura = parseInt(document.getElementById('ccal-altura').value);
  const actividad = parseFloat(document.getElementById('ccal-actividad').value);
  const objetivo = document.getElementById('ccal-objetivo').value;
  
  if (!edad || !peso || !altura) {
    alert('Por favor completa todos los campos requeridos');
    return;
  }
  
  // Cálculo de TMB (Tasa Metabólica Basal) - Fórmula de Mifflin-St Jeor
  let tmb;
  if (genero === 'Masculino') {
    tmb = 10 * peso + 6.25 * altura - 5 * edad + 5;
  } else {
    tmb = 10 * peso + 6.25 * altura - 5 * edad - 161;
  }
  
  // Calorías según actividad
  let calorias = tmb * actividad;
  
  // Ajustar según objetivo
  let ajusteObjetivo = 0;
  let recomendacion = '';
  
  if (objetivo === 'bajar') {
    ajusteObjetivo = -500;
    recomendacion = 'Para bajar de peso de forma saludable, crea un déficit de 500 kcal diarias combinando dieta y ejercicio.';
  } else if (objetivo === 'subir') {
    ajusteObjetivo = 500;
    recomendacion = 'Para aumentar masa muscular, consume un superávit de 500 kcal diarias con énfasis en proteínas y entrenamiento de fuerza.';
  } else {
    recomendacion = 'Para mantener tu peso actual, equilibra tu consumo calórico con tu nivel de actividad física.';
  }
  
  calorias += ajusteObjetivo;
  
  // Cálculo de macronutrientes (proporciones según objetivo)
  let proteinas, carbohidratos, grasas;
  
  if (objetivo === 'subir') {
    // Más proteínas para ganar masa muscular
    proteinas = peso * 2.2; // 2.2g por kg de peso
    grasas = (calorias * 0.25) / 9; // 25% de grasas
    carbohidratos = (calorias - (proteinas * 4) - (grasas * 9)) / 4;
  } else if (objetivo === 'bajar') {
    // Proteínas moderadas para preservar músculo
    proteinas = peso * 1.8; // 1.8g por kg de peso
    grasas = (calorias * 0.25) / 9; // 25% de grasas
    carbohidratos = (calorias - (proteinas * 4) - (grasas * 9)) / 4;
  } else {
    // Mantenimiento
    proteinas = peso * 1.6; // 1.6g por kg de peso
    grasas = (calorias * 0.25) / 9; // 25% de grasas
    carbohidratos = (calorias - (proteinas * 4) - (grasas * 9)) / 4;
  }
  
  // Mostrar resultados
  document.getElementById('caloriasTotal').textContent = Math.round(calorias);
  document.getElementById('carbohidratosTotal').textContent = Math.round(carbohidratos);
  document.getElementById('proteinasTotal').textContent = Math.round(proteinas);
  document.getElementById('grasasTotal').textContent = Math.round(grasas);
  document.getElementById('recomendacionPersonalizada').textContent = recomendacion;
  
  // Mostrar sección de resultados
  document.getElementById('caloriasResultado').classList.add('active');
}

// Inicializar con algunos datos de ejemplo
window.addEventListener('DOMContentLoaded', () => {
  // Datos de ejemplo
  pacientes = [
    { id: 1, nombre: 'María González', edad: 32, genero: 'Femenino', meta: 'Perder peso' },
    { id: 2, nombre: 'Carlos Ruiz', edad: 45, genero: 'Masculino', meta: 'Mejorar salud general' }
  ];
  
  imcs = [
    { id: 1, nombre: 'María González', imc: 24.8, estado: 'Normal', clase: 'status-normal', recomendacion: 'Mantén tus hábitos actuales y realiza actividad física regular', peso: 65, altura: 1.62 },
    { id: 2, nombre: 'Carlos Ruiz', imc: 28.5, estado: 'Sobrepeso', clase: 'status-high', recomendacion: 'Considera reducir el consumo de alimentos procesados y aumentar actividad física', peso: 85, altura: 1.73 }
  ];
  
  renderPacientes();
  renderIMC();
});
</script>

</body>
</html>
