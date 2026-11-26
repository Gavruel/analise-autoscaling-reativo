# Limites do autoscaling reativo diante de picos de demanda

Apresentação do artigo **"Engenharia de performance e modelagem de filas em sistemas distribuídos: limites do autoscaling reativo diante de picos de demanda"**, Universidade São Judas Tadeu (USJT), 2026.

**Acesse:** https://gavruel.github.io/analise-autoscaling-reativo/

## Sobre o trabalho

O artigo usa teoria das filas para mostrar por que o autoscaling reativo, sozinho, não protege a latência durante rajadas abruptas de demanda. A contribuição é a razão adimensional

```
Π = Tp / t*  =  (λ1 / C − 1) · (Tp / Ttol)
```

que compara o tempo de provisionamento de novas instâncias (Tp) com o tempo que a fila leva para estourar a tolerância de espera (t*). Quando Π > 1, a capacidade nova chega depois de a latência já ter sido violada.

A apresentação inclui um **simulador interativo** do modelo de fluido: dá para mudar a demanda, as instâncias, o tempo de provisionamento e a tolerância e ver a fila crescer e drenar em tempo real.

## Como usar

- **No computador ou projetor:** abra o link e navegue com as setas ou a barra de espaço. F11 deixa em tela cheia.
- **No celular:** o mesmo link abre em modo leitura, com os slides em uma página rolável.
- `?modo=slides` força o formato de apresentação; `?modo=leitura` força o modo leitura.

O projeto é um único `index.html`, sem dependências nem etapa de build.

## Autores

- Leonardo da Silva Vitorio
- Davi Ferreira Serapião dos Santos
- Kauê Henrique Figueredo Marques
- Natan Calasans Rodrigues de Andrade
- Gabriel Henrique Nascimento Paulino Santos

## Observação

O modelo é analítico e ilustrativo: os valores numéricos são hipotéticos e não vêm de experimentos próprios.
