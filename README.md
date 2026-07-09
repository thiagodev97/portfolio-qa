# 🎯 Meu Portfólio de QA Manual

Este repositório foi criado para documentar meus estudos, projetos práticos e análises de qualidade de software. Aqui você encontrará relatórios de testes estruturados no padrão internacional de mercado.

---

## 📄 Bug Report: Caso Real de Produção (99Freelas)

### Análise de Impacto de Negócio
Como a falha impossibilita a publicação autônoma de um projeto (atividade fim do usuário) através de um erro sistêmico contínuo de limite excedido, o bug impede o fluxo padrão de negócio. Como existe uma rota de contorno manual (envio de e-mail ao suporte), a severidade é mapeada como Crítica.

### 🛠️ Relatório Técnico (International Standard)

* **Title:** `[Project Publication] Phone verification modal returns "limit exceeded" error on first attempt`
* **Environment:** Production Environment (`99freelas.com.br`) / Web Browser (Google Chrome / Safari)
* **Severity / Priority:** Critical / High
* **Preconditions:**
  1. User must have a registered client account on the platform.
  2. User must be in the process of creating and submitting a new project service.
* **Steps to Reproduce:**
  1. Fill out all the required information to publish a new service.
  2. Click on the **Publish / Submit** button.
  3. When the phone verification **Modal / Popup** opens, enter a valid phone number.
  4. Click on the **Send Code** button.
* **Expected Result:** The system should successfully send an SMS verification code to the user's phone, allowing them to proceed with identity verification smoothly without errors.
* **Actual Result:** The system immediately returns an error message stating that the registration exceeded the maximum limit of code attempts, even if it is the user's very first attempt. The user is blocked from publishing autonomously and is forced to contact support via email for manual project approval.


---

### 🔄 Workaround (Rota de Contorno Atual)
Atualmente, a plataforma mitiga o problema de forma manual: o usuário é orientado a enviar um e-mail para o suporte técnico solicitando a liberação do projeto. O suporte realiza a aprovação interna sem a necessidade do código SMS. Embora isso permita a conclusão do fluxo, a falha crítica no componente de automatização permanece sem correção definitiva, gerando fricção e retrabalho operacional.

<img width="1547" height="877" alt="screenshot bug 99freelas" src="https://github.com/user-attachments/assets/6b251e4e-0b06-4f91-b16c-b5600121e031" />
