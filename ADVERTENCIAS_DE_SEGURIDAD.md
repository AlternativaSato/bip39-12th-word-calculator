# Advertencias de Seguridad Críticas

*Ritual de la Baraja — Alternativa Sato*

## 1. Propósito y evaluación de uso

Este método y sus herramientas asociadas fueron desarrollados con fines
pedagógicos. Su valor principal reside en el **proceso de aprendizaje** de
cómo se genera entropía y se construye una semilla BIP39.

Si decides ir más allá y usar una semilla generada así para fondos reales:
**no confíes en nuestra palabra — evalúa la seguridad por tu cuenta.**
Audita el método y las herramientas, y si tienes dudas, discútelas
abiertamente con la comunidad en este repositorio (issues, pull requests,
auditorías) antes de dar ese paso. Esa evaluación previa es tu
responsabilidad, no un trámite opcional.

## 2. Riesgos inherentes de las herramientas web

El uso de cualquier herramienta web (HTML/JavaScript), incluso descargada
localmente, conlleva riesgos:

- **Keyloggers o malware** pueden capturar la entrada.
- **Un error humano** (como una copia accidental en portapapeles
  persistente) puede comprometer la semilla.
- **El dispositivo mismo** puede estar comprometido.

## 3. Protocolo de ejecución segura (mínimo recomendado)

Si decides utilizar la herramienta HTML para algo más que el ejercicio
educativo, sigue este protocolo sin excepciones:

- ✅ **Usar un Sistema Operativo Live** (ej: Tails, Ubuntu Live) desde un
  USB nuevo o borrado por completo.
- ✅ **Desconectar toda red** (Wi-Fi, Ethernet, Bluetooth) **antes** de
  abrir el archivo.
- ✅ **Utilizar una ventana de navegación privada/incógnito**.
- ✅ **Nunca introducir las palabras en ningún otro software, navegador o
  cuadro de texto.**
- ✅ **Apagar el dispositivo** inmediatamente después de completar el
  ejercicio.

## 4. Aislamiento de red: el requisito no negociable

Esta es la única regla del documento que no es cuestión de criterio
personal, porque no depende de cuánto confíes en el código: **una
computadora conectada a internet puede filtrar información sin que lo
notes, sin importar qué tan auditada esté la herramienta que corres en
ella.**

> Nunca introduzcas tus palabras semilla (ni siquiera las 11 palabras
> preliminares o los 7 bits) en un ordenador que haya estado, esté o
> pueda estar conectado a Internet.

Evalúa todo lo demás por tu cuenta; esto no lo negocies.

## 5. Para custodia real: hardware wallet

Para fondos reales, la única recomendación segura es un **hardware
wallet certificado y de código abierto**. Estos dispositivos implementan
los mismos principios criptográficos de forma aislada, verificada y
robusta. Este método educativo te da el conocimiento para entender **por
qué** esos dispositivos son seguros, **no para reemplazarlos**.

## 6. Responsabilidad y verificación comunitaria

El creador de este método y sus herramientas no se hace responsable por
pérdida de fondos, robos o compromisos de seguridad derivados del uso de
esta metodología o herramientas asociadas. La soberanía implica
responsabilidad personal total — y esa responsabilidad empieza por
verificar antes de confiar, no después.

---

Un proyecto de [Alternativa Sato](https://alternativasato.gitbook.io/alternativasato) · *No confíes, verificá.*
