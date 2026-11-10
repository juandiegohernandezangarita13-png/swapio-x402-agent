# 🚀 Guion de Video y Pitch Técnico: Agente Autónomo con x402 y Swap.io
**Bounty:** Make a video about our x402 Feature (Superteam Earn — $500 USDC)  
**Duración:** 90 segundos (rango permitido: 60 - 120 segundos)  
**Etiquetas obligatorias en X:** `@swapdotio` y `@Superteam`  

---

## 🎬 Estructura del Video (Segundo a Segundo)

### [00:00 - 00:20] El Problema: Por qué los agentes de IA no pueden usar APIs tradicionales
* **Visual:** Diagrama en pantalla mostrando un bot de IA bloqueado por formularios de tarjeta de crédito y claves API estáticas.
* **Voz en off:**
  > "Los agentes autónomos de IA ya están aquí, pero tienen un gran problema para interactuar con finanzas descentralizadas: las APIs tradicionales exigen tarjetas de crédito humanas, suscripciones mensuales de 500 dólares y claves API que se filtran fácilmente. ¿Por qué un bot que opera de forma esporádica debería pagar una mensualidad fija?"

### [00:20 - 00:50] La Solución: El flujo x402 con Swap.io
* **Visual:** Animación del flujo HTTP 402 paso a paso:
  1. `GET /v1/quote` -> 
  2. `HTTP 402 Payment Required` (Cabecera con monto: 0.0001 USDC) -> 
  3. Firma y pago on-chain en Solana -> 
  4. Cotización devuelta instantáneamente.
* **Voz en off:**
  > "Aquí entra el protocolo **x402** integrado en **Swap.io**. 
  > El flujo es radicalmente simple:
  > Primero, nuestro agente solicita una ruta de swap a la API Hermes de Swap.io.
  > La API responde con el código HTTP estándar 402: *Payment Required*, indicando un costo de una fracción de centavo.
  > El agente firma y envía el micro-pago en USDC directamente en Solana.
  > Y en milisegundos, recibe la mejor cotización y la transacción lista para firmar. Sin cuentas, sin KYC y sin suscripciones fijas."

### [00:50 - 01:15] Caso de Uso Concreto: Bot de Rebalanceo de Portafolio en Telegram
* **Visual:** Demo en pantalla del código `agent_client.py` ejecutándose en la terminal recibiendo la respuesta 402 y la cotización en vivo.
* **Voz en off:**
  > "Imaginemos nuestro caso de uso concreto: un **Agente Autónomo de Rebalanceo en Telegram**. Solo consulta precios cuando la volatilidad del mercado se dispara. Con x402 y Swap.io, el bot solo gasta exactamente cuando consulta; si está en reposo durante días, el costo es cero absoluto. Esto desbloquea una economía pura de máquina a máquina."

### [01:15 - 01:30] Cierre y Llamado a la Acción
* **Visual:** Logos de Swap.io y Superteam con el enlace a `https://docs.swap.io/developer-tools/agent-api-x402/quickstart`.
* **Voz en off:**
  > "El futuro de las finanzas autónomas no necesita tarjetas de crédito: necesita micro-pagos nativos. Prueba la Agent API de Swap.io en hermes.swap.io y lleva tus agentes de Solana al siguiente nivel."

---

## 💻 Entregable de Código (Bonus +30% de Calificación)
El script de prueba ejecutable se encuentra en:  
[`agent_client.py`](./agent_client.py)
