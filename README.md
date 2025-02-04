# relogio-js-and-css
![Template relogio](https://github.com/weslei573/Portfolio-Website/blob/main/assets/project-1.png)


# Resumo do funcionamento do código:

1. **Seleção dos elementos:**

   - São selecionados os elementos HTML correspondentes aos ponteiros de segundos, minutos e horas usando `document.querySelector`.

2. **Função `setDate`:**

   - Cria um objeto `Date` para obter o horário atual.
   - **Ponteiro dos segundos:**
     - Calcula o ângulo com base no número de segundos (`(seconds / 60) * 360`) e adiciona 90 graus para compensação.
     - Aplica a rotação ao elemento dos segundos via CSS (`transform: rotate(...)`).
   - **Ponteiro dos minutos:**
     - Calcula o ângulo com base nos minutos e ajusta levemente conforme os segundos (`(mins / 60) * 360 + (seconds / 60) * 6`), adicionando 90 graus.
     - Aplica a rotação e define estilos adicionais (largura e posição) ao elemento dos minutos.
   - **Ponteiro das horas:**
     - Calcula o ângulo baseado nas horas e ajusta com os minutos (`(hour / 12) * 360 + (mins / 60) * 30`), somando 90 graus.
     - Aplica a rotação e define estilos extras (largura, posição e cor de fundo) ao elemento das horas.

3. **Atualização contínua:**
   - Utiliza `setInterval` para chamar a função `setDate` a cada 1000 milissegundos (1 segundo), garantindo que os ponteiros se movam de acordo com o horário atual.
   - A função `setDate` também é chamada imediatamente para iniciar o relógio sem atraso.

**Resultado:**  
O código implementa um relógio analógico que atualiza dinamicamente os ponteiros dos segundos, minutos e horas de acordo com o horário atual, realizando a animação e ajustes de estilo via JavaScript e CSS.
