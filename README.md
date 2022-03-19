main        : branch de produção (última release)
develop     : branch de desenvolvimento (branch principal)
feature/... : novas funcionalidades/melhorias
bugfix/...  : correção de código
hotfix/...  : correção crítica de código que está em produção


# Exemplo, preciso desenvolver uma nova tela (nova funcionalidade/feature):
1. Trocar para a branch develop:
git checkout develop

2. Receber atualizações da branch develop:
git pull

3. Criar a sua nova branch feature:
git checkout -b feature/tela-login

4. Publicar branch:
git push -u origin feature/tela-login

5. Faça as suas modificações: crie arquivos, modifique códigos, e etc.
  Faça seu code review e depois:
    Prepare os arquivos (stage):
git add .
    Faça commit dos arquivos preparados:
git commit "feat: create login screen"
    Publique o commit no repositório remoto:
git push

6. Sinalizar para a QA que a funcionalidade foi implementada. Enviar para teste.

7. Quando for aprovado pelo(a) QA você poderá fazer um merge para develop:
Isso traria as modificações de feature/tela-login para develop. 
Porém, o correto seguindo o fluxo padrão, é criar um PULL REQUEST:
feature/tela-login -> develop
Nesse momento, o senior faz revisão do seu código e testa a funcionalidade implementada.

Se fosse via linha de comando (não fazer nos projetos do instituto):
git checkout develop
git merge feature/tela-login

8. O senior faz o code review e aceita/rejeitar o Pull Request através da interface web (gitlab, github, bitbucket).

## Observações
Sempre ter **muita atenção**, especialmente antes de executar cada comando git, para ter certeza de que está trabalhando na branch correta e no projeto correto.