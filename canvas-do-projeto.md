# Canvas do Projeto

**Projeto:** Aplicativo de Gestão para Transporte Alternativo · **Equipe:** Thayná Fortunato, Wendrieley Clara, Carolaine Silva, Jefferson Douglas, Davy Miguel · **Data:** 15/09/2026 · **Organização parceira:** AMTAPR

---

## 1. Problema

Na cooperativa/empresa de transporte alternativo, motoristas e passageiros precisam controlar escalas, rotas e horários das vans, mas hoje isso é feito manualmente por rádio, papel e caneta, o que causa descontrole nas escalas, falta de previsibilidade para o passageiro e dificuldade de auditoria do fluxo diário pela empresa.

**Evidências de que o problema existe** (dados, falas, observação):

- Uso de rádio, papel e caneta para controlar a operação, sem registro digital centralizado.
- Passageiros esperam no ponto sem saber o horário da próxima van, e motoristas têm dificuldade de manter o intervalo exato entre veículos.

## 2. Quem é afetado

| Quem | Quantas pessoas | Como é afetado hoje |
| ---- | --------------- | -------------------- |
| Passageiros | 16.000 a 21.000 | Esperam sem previsibilidade do horário/localização da van |
| Motoristas | 80 a 110 | Controlam fila e escala manualmente, sem apoio digital |
| Empresa/Cooperativa (Admin) | 1 | Dificuldade de auditar e organizar o fluxo diário da frota |

## 3. Solução proposta

Um aplicativo mobile que conecta empresa, motoristas e passageiros, permitindo organizar escalas e filas de saída das vans e acompanhar a localização dos veículos em tempo real no mapa. Assim, motoristas ganham mais controle da rota e passageiros passam a saber quando a próxima van chega.

## 4. Funcionalidades do MVP (3 a 5)

| # | Funcionalidade | Para quem | Por que é essencial |
| --- | -------------- | --------- | -------------------- |
| 1 | Iniciar e encerrar rota | Motorista | Registra o ciclo operacional da van em tempo real |
| 2 | Visualizar posição na fila de saída | Motorista | Organiza a ordem e o intervalo entre as vans |
| 3 | Consultar previsão da próxima van | Passageiro | Reduz a incerteza durante a espera no ponto |
| 4 | Acompanhar localização do veículo no mapa | Passageiro | Dá visibilidade em tempo real do trajeto da van |
| 5 | Cadastrar/validar frota e motoristas | Empresa/Admin | Base de dados necessária para todo o restante do sistema |

## 5. Fora do escopo

O que **não** faremos nesta versão, e por quê:

| Não faremos | Por quê |
| ----------- | ------- |
| Pagamento/cobrança de passagem dentro do app | Não consta no escopo funcional levantado; foco inicial é escala e rastreamento |
| Autenticação avançada, criptografia e autorização detalhadas | A documentação-base não especifica mecanismos; ficam definidos na implementação |
| Módulo do passageiro no primeiro sprint | MVP prioriza primeiro o módulo do motorista, conforme metodologia ágil adotada |

## 6. Usuários e papéis

| Papel | O que pode fazer |
| ----- | ------------------ |
| Empresa/Admin | Cadastra e gerencia frota e motoristas; configura rotas e intervalos; organiza a fila de saída |
| Motorista | Visualiza posição na fila; inicia e encerra rota; informa lotação do veículo |
| Passageiro | Consulta horário da próxima van; acompanha localização no mapa; identifica o motorista da vez |

## 7. Restrições

| Tipo            | Restrição                                                  |
| --------------- | ----------------------------------------------------------- |
| Prazo           | 18 a 22 semanas (5 fases: planejamento, back-end, front-end, testes/QA, go-live) |
| Equipe          | 5 pessoas, 20 a 25 h/semana no total                          |
| Técnica         | Flutter/Dart (mobile), Node.js ou Firebase Cloud Functions, Cloud Firestore/NoSQL, Google Maps API, WebSockets/Streams para tempo real |
| Contexto de uso | Uso em campo por motoristas e passageiros, com possível instabilidade de conexão (offline-first) |
| Orçamento       | R$ 59.000,00 (investimento inicial: desenvolvimento + implantação e treinamento em 5 unidades) |

## 8. Riscos principais

| Risco | O que faremos |
| ----- | -------------- |
| Queda de sinal de internet em campo | Adotar arquitetura offline-first, armazenando dados localmente e sincronizando quando a conexão voltar |
| Resistência de motoristas mais experientes à tecnologia | Interface simples e intuitiva com botões grandes, além de treinamento focado em facilidade de uso |
| Custos recorrentes de mapas/GPS e nuvem variarem por volume de uso | Monitorar consumo e revisar faixa estimada de R$ 2.000 a R$ 4.000+/mês periodicamente |

## 9. Critérios de sucesso

| Objetivo | Como mediremos | Meta |
| -------- | ---------------- | ----- |
| Reduzir dependência de processos manuais | Nº de escalas/rotas controladas via app vs. papel/rádio | Pelo menos 80% das escalas e rotas do período de teste controladas pelo aplicativo |
| Aumentar previsibilidade para o passageiro | Tempo médio de espera relatado / uso da função "próxima van" | Reduzir em pelo menos 30% o tempo médio de espera percebido pelos passageiros |
| Reduzir falhas humanas e conflitos de escala | Nº de conflitos de escala registrados por mês | Reduzir em pelo menos 50% os conflitos de escala durante o período de teste |

## 10. O que fica depois

- **Quem opera o sistema:** Empresa/cooperativa de transporte alternativo (perfil Empresa/Admin)
- **Quem mantém tecnicamente:** Equipe/empresa responsável pelo desenvolvimento, mediante contrato ou acordo de manutenção com a AMTAPR
- **Custo mensal estimado:** R$ 2.000 a R$ 4.000+ (hospedagem/cloud, banco de dados, mapas/GPS, manutenção e suporte)
- **Licença do código:** a definir entre a equipe, a instituição de ensino e a AMTAPR antes da entrega final.
