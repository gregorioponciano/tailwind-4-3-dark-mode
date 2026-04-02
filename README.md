<p align="center">
  <img src="https://img.shields.io/badge/Tailwind_CSS-v4.0-06B6D4?style=for-the-badge&logo=tailwind-css&logoColor=white" alt="Tailwind CSS 4">
  <img src="https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JS ES6">
  <img src="https://img.shields.io/badge/UI/UX-Dark_Mode-222222?style=for-the-badge" alt="Dark Mode">
</p>

<h1 align="center">🌙 Tailwind CSS 4.0 + Dark Mode Strategy</h1>

<p align="center">
  <strong>Implementação moderna de Dark Mode utilizando as novas funcionalidades do Tailwind CSS v4, com foco em variáveis CSS e performance.</strong>
</p>

---

## 📝 Sobre o Projeto

Este repositório serve como um guia prático para configurar e alternar entre os temas **Light** e **Dark** utilizando o **Tailwind CSS**. Diferente das versões anteriores, exploramos aqui a nova abordagem de configuração via CSS-first, aproveitando o poder das variáveis nativas do navegador.

### ✨ Funcionalidades

* **🌓 Troca Dinâmica de Tema:** Alternância entre modos claro e escuro via classe ou preferência do sistema.
* **⚡ Tailwind v4 Engine:** Uso da nova engine mais rápida e baseada em CSS moderno.
* **🎨 Paleta de Cores Otimizada:** Cores selecionadas para manter o contraste e a legibilidade em ambos os modos.
* **💾 Persistência:** Armazenamento da preferência do usuário no `localStorage`.

---

## 🏗️ Como Funciona?

O Dark Mode no Tailwind pode ser ativado de duas formas principais:
1. **Media Strategy:** Baseado nas configurações de cor do Sistema Operacional do usuário.
2. **Selector Strategy:** Utilizando uma classe (geralmente `.dark`) no elemento `<html>`, permitindo que o usuário escolha o tema manualmente.



---

## 🛠️ Configuração Técnica

### 1. Estrutura CSS (Tailwind 4 Style)
No Tailwind 4, a configuração é mais voltada para o arquivo CSS principal:

```css
@import "tailwindcss";

@theme {
  --color-brand: #3b82f6;
  
  @variant dark (&:where(.dark, .dark *));
}

:root {
  --background: #ffffff;
  --foreground: #111827;
}

.dark {
  --background: #0f172a;
  --foreground: #f8fafc;
}
