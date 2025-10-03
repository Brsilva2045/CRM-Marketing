📊 CRM Marketing - Tijuca Alimentos

Painel interno para gestão de Doações, Mídia, Mídia OOH e Patrocínios, desenvolvido com Firebase + Firestore e hospedado via GitHub Pages.
Interface leve em Tailwind CSS e tema institucional Tijuca (cores e logo).

🚀 Funcionalidades

Autenticação anônima (qualquer colaborador pode acessar).

Integração com Firestore em tempo real.

4 módulos principais:

📦 Doações – controle de solicitações, valor, status, observações.

🖼️ Mídia – campanhas digitais, veículos, formatos, custos e prazos.

🏙️ Mídia OOH – outdoors, painéis e mídia externa.

🤝 Patrocínios – entidades/eventos, cotas, valores, status, observações.

Visual unificado com identidade Tijuca Alimentos.

🎨 Identidade Visual

#f5a800 Amarelo Tijuca

#003a70 Azul Tijuca

#00662f Verde Tijuca

Logo oficial:


📂 Estrutura de pastas
📦 crm-marketing
 ┣ 📜 index.html          # Painel inicial
 ┣ 📜 doacoes.html        # Gestão de doações
 ┣ 📜 midia.html          # Gestão de mídia digital
 ┣ 📜 midia_ooh.html      # Gestão de mídia OOH
 ┣ 📜 patrocinio.html     # Gestão de patrocínios
 ┣ 📜 sheet.css           # Estilo extra (se necessário)
 ┗ 📜 README.md           # Este arquivo

🔧 Como rodar

Clonar o repositório

git clone https://github.com/seuusuario/crm-marketing.git
cd crm-marketing


Configurar Firebase

Criar um projeto no Firebase Console
.

Ativar Firestore Database.

Em Authentication → Método de Login, ativar Anônimo.

Substituir no código o seu firebaseConfig (já vem pronto nos HTMLs).

Regras de segurança do Firestore (para teste)

rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read, write: if request.auth != null;
    }
  }
}


Publicar no GitHub Pages

Vá até o repositório → Settings → Pages.

Configure para branch main, pasta /root.

Abra o link gerado:

https://seuusuario.github.io/crm-marketing/

📸 Screenshots
Tela inicial

(adicione aqui prints reais do painel rodando)

👥 Contribuindo

Todo colaborador pode acessar com login anônimo.

Para evoluir o projeto:

Sugira melhorias via Issues.

Faça Pull Requests com correções e novas features.

⚠️ Segurança

As regras atuais permitem acesso a qualquer usuário autenticado anonimamente.
Para uso interno em produção, recomenda-se:

Restringir para o domínio @tijucaalimentos.com.

Criar papéis (admin, leitura, edição).
