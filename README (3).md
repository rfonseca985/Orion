# ORION

ORION e uma consciencia digital local para preservar memoria, identidade, valores, objetivos e continuidade intelectual do usuario.

Importante: este projeto nao transfere consciencia biologica nem prova continuidade subjetiva real. Ele cria uma representacao digital persistente baseada em registros, conversas, memorias declaradas, perfil evolutivo e um modelo de linguagem rodando localmente.

## Objetivo

- Rodar 100% local na sua maquina.
- Usar ferramentas open source.
- Guardar conversas e memorias em SQLite.
- Simular uma rede neural biologicamente inspirada, com limites fisicos aproximados.
- Manter um perfil vivo do usuario.
- Responder sempre como ORION, com continuidade, profundidade e contexto.
- Permitir exportar seu legado em Markdown.

## Stack open source

- Python 3.10+
- SQLite local
- Ollama local
- Modelo recomendado: `qwen2.5:7b-instruct` ou outro modelo com licenca permissiva que voce escolher

O codigo deste projeto esta sob licenca MIT. O modelo de IA e baixado separadamente; para manter tudo aberto, use apenas modelos com licenca open source permissiva.

## Instalacao gratuita

1. Instale Python:
   https://www.python.org/downloads/

   No Windows, marque a opcao `Add Python to PATH` durante a instalacao.

2. Instale Ollama:
   https://ollama.com/download

3. Baixe um modelo local:

```powershell
ollama pull qwen2.5:7b-instruct
```

Ou clique duas vezes em:

```text
instalar_modelo.bat
```

Se sua maquina for mais fraca, tente:

```powershell
ollama pull qwen2.5:1.5b-instruct
```

Antes de usar qualquer modelo, confira a licenca do modelo escolhido. Para manter o projeto 100% open source, prefira modelos Apache-2.0, MIT ou outra licenca open source permissiva.

## Como rodar

No Windows, clique duas vezes em:

```text
run_orion.bat
```

O arquivo tenta usar `py` primeiro e depois `python`.

Ou rode pelo terminal:

```powershell
python orion.py
```

Para escolher outro modelo:

```powershell
$env:ORION_MODEL="qwen2.5:7b-instruct"
python orion.py
```

## Comandos dentro do ORION

- `/ajuda` mostra todos os comandos.
- `/status` testa o Ollama e lista modelos locais.
- `/modelo` mostra o modelo atual.
- `/modelo nome` troca o modelo nesta sessao.
- `/mente` mostra energia, fadiga, sinapses e memoria de trabalho da rede neural.
- `/descansar` recupera energia e consolida memoria na rede neural.
- `/lembrar texto` salva uma memoria importante.
- `/aprender texto` faz o mesmo que `/lembrar`.
- `/perfil` mostra o perfil persistente.
- `/set chave valor` atualiza uma parte do perfil.
- `/memorias` lista memorias salvas.
- `/resumo` cria um resumo de continuidade.
- `/exportar` exporta o legado para `exports/orion_legacy.md`.
- `/sair` encerra.

## Rede neural biologicamente inspirada

O arquivo `human_mind_network.py` cria uma rede local com:

- neuronios com potencial, limiar de disparo e periodo refratario;
- sinapses excitatorias e inibitorias;
- energia finita e fadiga;
- ruido interno;
- limite de memoria de trabalho;
- plasticidade sinaptica;
- decaimento, poda e consolidacao durante descanso;
- areas funcionais simuladas: sensorial, hipocampo, pre-frontal, amigdala, modo padrao e motora.

Para testar a rede isoladamente:

```powershell
python human_mind_network.py
```

Dentro dela:

```text
/descansar
/sair
```

Essa rede nao e um cerebro humano real. Ela e uma aproximacao computacional pequena, criada para dar ao ORION restricoes semelhantes as do cerebro: capacidade limitada, gasto de energia, esquecimento, ruido, fadiga e consolidacao.

## Como alimentar a memoria

Use frases como:

```text
/lembrar Eu valorizo liberdade intelectual, autonomia e profundidade emocional.
/lembrar Meu objetivo e construir uma IA local que preserve minha identidade cognitiva.
/lembrar Quero que ORION seja direto, estrategico, leal e filosoficamente profundo.
```

Tudo fica salvo localmente em:

```text
data/orion.sqlite3
```

## Privacidade

Por padrao, o banco de dados fica somente na sua maquina. O projeto conversa com o Ollama em `localhost`. Nao envie esse banco para nuvens ou terceiros se ele contiver informacoes intimas.

## Solucao de problemas

Se aparecer `Python nao foi encontrado`, instale Python e marque `Add Python to PATH`.

Se aparecer `Nao consegui conectar ao Ollama`, abra o aplicativo Ollama e rode:

```powershell
ollama list
```

Se o modelo nao existir, rode:

```powershell
ollama pull qwen2.5:7b-instruct
```

Dentro do ORION, use:

```text
/status
```

## Evolucao sugerida

Proximos passos possiveis:

- Interface web local.
- Criptografia do banco.
- Importacao de diarios, audios e documentos.
- Memoria semantica com embeddings locais.
- Acoplar a rede biologicamente inspirada diretamente ao prompt do ORION.
- Rotina de revisao diaria para atualizar identidade, valores e objetivos.
- Backup criptografado em disco externo.
