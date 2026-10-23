FinAI — versão para GitHub Pages + Google Drive

O QUE ESTA VERSÃO FAZ
- Mantém o FinAI como aplicação estática, sem servidor pago.
- No Dashboard, inclui uma secção para ligar ao Google Drive.
- Guarda quatro ficheiros JSON na pasta FinAI do Google Drive:
  1. Transações e orçamentos
  2. Classificações aprendidas
  3. Investimentos
  4. Objetivos
- O envio e a restauração são manuais, quando clicas nos botões. Não há sincronização automática.
- O armazenamento local atual continua a existir. A primeira restauração substitui os dados locais correspondentes, por isso cria uma cópia de segurança antes de restaurar.

ANTES DE USAR O GOOGLE DRIVE
É necessário criar um OAuth Client ID no Google Cloud e ativar a Google Drive API. Depois, adicionar o endereço do site GitHub Pages como origem JavaScript autorizada. O Client ID é colocado no campo da aplicação; não coloques credenciais privadas ou chaves secretas no HTML.

PUBLICAR NO GITHUB PAGES
1. Guarda uma cópia de segurança dos dados do FinAI atual usando “Guardar cópia”.
2. No GitHub, cria um repositório para o site. Não carregues extratos, cópias JSON ou dados financeiros para o repositório.
3. Carrega o ficheiro FinAI_GitHub_Drive.html e renomeia-o para index.html no repositório.
4. Nas definições do repositório, abre Pages e escolhe publicar a partir do branch principal (root).
5. Abre o endereço Pages criado e configura o Google OAuth Client ID para esse endereço.

MIGRAR OS DADOS EXISTENTES
A versão publicada terá armazenamento local separado da versão aberta como ficheiro no computador. Não assumes que os dados passam automaticamente entre os dois. Mantém a cópia JSON antiga em segurança. Quando o Google Drive estiver configurado, envia os dados a partir da versão onde estão os dados que pretendes guardar.

LIMITAÇÕES IMPORTANTES
- Não é sincronização automática em tempo real; é necessário enviar/restaurar manualmente.
- Os dados financeiros são sensíveis. Protege a conta Google e não partilhes os ficheiros de cópia.
- O FinAI usa uma autorização OAuth no navegador e a permissão drive.file, destinada aos ficheiros que esta aplicação cria/usa. A configuração do Google Cloud tem de estar correta para o acesso funcionar.
- A aplicação continua a depender da Internet para carregar a biblioteca Excel e o serviço de autenticação Google.
