# Desafio DevSecOps — Gerenciador de Tarefas

## Sobre o Projeto
Este repositório faz parte do desafio prático do módulo de DevSecOps da ADA Tech.
Você receberá este projeto com vulnerabilidades propositais e uma pipeline incompleta.
Seu objetivo é **implementar a pipeline de segurança** e **corrigir as vulnerabilidades**.

## Estado atual
A pipeline está **incompleta**. Os steps de segurança precisam ser implementados por você.

## Sua missão
1. Implementar os steps de segurança no `pipeline.yml`
2. Fazer a pipeline **quebrar** ao detectar os problemas
3. Corrigir as vulnerabilidades encontradas
4. Fazer a pipeline **passar** com tudo verde ✅
5. Documentar o funcionamento da pipeline neste README

## O que implementar
- [ ] Secrets Scanning com **Gitleaks**
- [ ] SAST com **Semgrep**
- [ ] SCA com **Grype**
- [ ] Assinatura do artefato com cosign
- [ ] Deploy com **GitHub Pages**

## Como a pipeline funciona
> **Substitua este bloco pela sua explicação após implementar a pipeline.**

A pipeline implementada tinha foco em segurança e correção de vulnerabilidades.  
O objetivo é garantir que nenhum código inseguro ou vulnerável chegue à produção.
---
## STEPS
1. **Secrets Scanning (Gitleaks)**  
- Verifica se há segredos expostos no código ou no histórico de commits (senhas, tokens, chaves de API).  
- Se encontrar qualquer segredo, a pipeline quebra imediatamente.  
- **Por que importa:** evita que credenciais sensíveis sejam publicadas e expostas.

2. **SAST (Semgrep)**
- Analisa o código estaticamente em busca de padrões inseguros (XSS, injeções, uso de funções perigosas).  
- Se detectar vulnerabilidades, a pipeline falha.  
- **Por que importa:** garante que falhas de segurança sejam corrigidas antes de chegar à produção.

3. **SCA (Grype)**  
- Examina as dependências do projeto em busca de CVEs (vulnerabilidades conhecidas).  
- Se encontrar vulnerabilidades de severidade média ou maior, a pipeline falha.  
- **Por que importa:** protege contra ataques que exploram bibliotecas externas desatualizadas.

4. **Assinatura e Verificação (Cosign)**  
- O artefato gerado é assinado digitalmente e verificado antes do deploy.  
- **Por que importa:** garante integridade e autenticidade, evitando que o artefato seja alterado.

5. **Deploy em Produção (GitHub Pages)**  
- Só acontece se todos os passos anteriores forem aprovados.  
- O site é publicado automaticamente em ambiente seguro.  
- **Por que importa:** garante que apenas código seguro e validado chegue à produção.

## URL de Produção
> Adicione aqui o link do GitHub Pages após o deploy.
