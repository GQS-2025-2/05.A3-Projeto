📌 **Especificação do Projeto A3**

# 📊 Tema Livre

## 📝 Descrição do Trabalho — 20 pontos  

O grupo deverá propor e desenvolver um projeto de software **com tema livre**, aplicando conceitos aprendidos na disciplina.  
O projeto deve ter **funcionalidades claras e testes automatizados** com base em **TDD e BDD**.

---

## 🎯 Objetivos

- Criar e aplicar **testes unitários**.  
- Implementar práticas de **BDD (Behavior Driven Development)**.  
- Documentar todo o projeto em **README.md**, seguindo boas práticas.  
- Elaborar uma **apresentação** (slides)

---

## 🚀 Instruções Gerais

1. **Data da Apresentação:** 26/11/25  

2. **Grupo & Organização**  
   - Máximo de **6 integrantes**.  
   - Criar uma **organização no GitHub** para o grupo e armazenar todo o código nela.  
   - Utilizar **GitHub Projects** para o gerenciamento de tarefas (colunas: Backlog, Em Progresso, Revisão, Concluído).  
   - Distribuir tarefas e responsáveis de forma equilibrada.

3. **Repositório & README**  
   - O repositório principal deve conter um `README.md` completo, com:
     - Descrição do projeto  
     - Tecnologias utilizadas  
     - Instruções de instalação e execução  
     - Estrutura de pastas e testes  
     - Contribuidores  
     - Licença (opcional)  
   - Consulte: [Como escrever um bom README para seu projeto do GitHub](https://www.freecodecamp.org/portuguese/news/como-escrever-um-bom-arquivo-readme-para-seu-projeto-do-github/).

---

## 🔍 Testes

### 🧩 Testes Unitários

- Criar e executar **testes unitários automatizados** utilizando JUnit, pytest ou outra ferramenta equivalente.  
- Cada classe ou módulo deve ter cobertura de testes de pelo menos **80%**.  

#### Exemplo de Teste Unitário (Java + JUnit 5)

```java
import static org.junit.jupiter.api.Assertions.*;
import org.junit.jupiter.api.Test;

class CalculadoraTest {

    @Test
    void deveSomarDoisNumeros() {
        Calculadora calc = new Calculadora();
        double resultado = calc.somar(2.0, 3.0);
        assertEquals(5.0, resultado, 0.001);
    }
}
```

---

### 🤝 Desenvolvimento Guiado por Comportamento (BDD)

- Criar no mínimo 5 **cenários em Gherkin** descrevendo o comportamento esperado do sistema.  
- Automatizar esses cenários usando frameworks como **Cucumber** ou similares.

#### Exemplo de Cenário BDD em Gherkin

```gherkin
Funcionalidade: Cálculo de Desconto

  Cenário: Aplicar desconto válido
    Dado que o cliente tem um cupom de 10%
    Quando ele realiza uma compra de R$100,00
    Então o valor final deve ser R$90,00
```

#### Exemplo de Implementação em Java (Step Definitions)

```java
@Quando("ele realiza uma compra de {double}")
public void realizaCompra(double valor) {
    resultado = loja.aplicarDesconto(valor, 10.0);
}

@Entao("o valor final deve ser {double}")
public void verificaValorFinal(double esperado) {
    assertEquals(esperado, resultado, 0.01);
}
```

---

### 🧪 Template de Registro de Testes

| ID | Tipo de Teste | Descrição | Resultado Esperado | Resultado Obtido | Status (✅/❌) | Observações |
|----|----------------|------------|--------------------|------------------|----------------|-------------|
| TST-01 | Unitário | Verificar soma de dois números | Resultado igual à soma | _(preencher após execução)_ | | |
| TST-02 | BDD | Calcular desconto de 10% sobre R$100 | Retornar R$90,00 | _(preencher após execução)_ | | |

---

## 🖥️ Apresentação

- Criar pasta `slides/` com o arquivo da apresentação (PowerPoint, PDF ou Google Slides).  
- Slides devem conter:
  1. Introdução  
  2. Motivação  
  3. Desenvolvimento  
  4. Resultados  
  5. Considerações Finais  
- Todos os integrantes devem estar aptos a responder perguntas.  
- A apresentação deve durar **até 5 minutos**, feita por **1 ou 2 integrantes** do grupo.

---
