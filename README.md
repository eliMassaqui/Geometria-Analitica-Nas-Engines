
# 🧠 Geometria Analítica Aplicada a Engines e Jogos Imersivos

> Matemática de precisão, mundos de impacto.

Este repositório aplica conceitos de **Geometria Analítica** no desenvolvimento de **motores gráficos** e **jogos 3D interativos** com Unity. Cada conceito possui aplicação direta na lógica computacional espacial: posições, colisões, trajetórias e rotações com total controle.

---

## 🎮 Relevância Estratégica

Nada em um jogo é aleatório — tudo é vetorizado, rotacionado e interpolado.

Com Geometria Analítica, você desenvolve:

- 🎯 Projéteis guiados com precisão vetorial;
- 🎥 Câmeras orbitais suaves e dinâmicas;
- 🧠 IA com detecção de campo de visão;
- 🧱 Mundos modulares, simétricos ou caóticos;
- 🌀 Rotações suaves com quaternions;
- 🔍 Colisões baseadas em fórmulas reais.

---

## ✍️ Conceitos Matemáticos + Códigos Unity

Cada item apresenta teoria + implementação prática em C#.

### 📏 1. Distância entre dois pontos

**2D:**  
d = raiz de [(x2 - x1)² + (y2 - y1)²]

**3D:**  
d = raiz de [(x2 - x1)² + (y2 - y1)² + (z2 - z1)²]

```csharp
float DistanciaEntrePontos(Vector3 a, Vector3 b)
{
    return Vector3.Distance(a, b);
}
```

---

### 🧭 2. Equação da reta (paramétrica)

**Fórmula:**  
P(t) = ponto_inicial + t * direção

```csharp
Vector3 RetaParametrica(Vector3 pontoInicial, Vector3 direcao, float t)
{
    return pontoInicial + t * direcao;
}
```

---

### 🔄 3. Produto Escalar (Dot Product)

**Fórmula:**  
a · b = |a| * |b| * cos(θ)

```csharp
float ProdutoEscalar(Vector3 a, Vector3 b)
{
    return Vector3.Dot(a.normalized, b.normalized);
}
```

---

### ✖️ 4. Produto Vetorial (Cross Product)

```csharp
Vector3 ProdutoVetorial(Vector3 a, Vector3 b)
{
    return Vector3.Cross(a, b);
}
```

---

### 🧾 5. Equação do plano

**Fórmula:**  
Ax + By + Cz + D = 0

```csharp
bool PontoNoPlano(Vector3 ponto, float A, float B, float C, float D)
{
    float resultado = A * ponto.x + B * ponto.y + C * ponto.z + D;
    return Mathf.Approximately(resultado, 0f);
}
```

---

### 🌐 6. Circunferência (2D)

**Fórmula:**  
(x - a)² + (y - b)² = r²

```csharp
bool PontoDentroDeCircunferencia(Vector2 ponto, Vector2 centro, float raio)
{
    return Vector2.Distance(ponto, centro) <= raio;
}
```

---

### ♻️ 7. Rotação 2D com Números Complexos

**Fórmula:**  
z' = z * (cos(θ) + i * sen(θ))

```csharp
Vector2 Rotacionar2D(Vector2 ponto, float anguloGraus)
{
    float rad = anguloGraus * Mathf.Deg2Rad;
    float cos = Mathf.Cos(rad);
    float sin = Mathf.Sin(rad);
    return new Vector2(
        ponto.x * cos - ponto.y * sin,
        ponto.x * sin + ponto.y * cos
    );
}
```

---

### 🌀 8. Slerp com Quaternions

```csharp
Quaternion RotacaoSuave(Quaternion inicio, Quaternion fim, float t)
{
    return Quaternion.Slerp(inicio, fim, t);
}
```

---

## 🧠 Conclusão

Geometria Analítica é o motor invisível por trás de qualquer engine sofisticada.

Dominar vetores, planos e quaternions transforma ideias em realidade digital — com realismo, precisão e desempenho.

> Domine o espaço. Projete com precisão. Programe com propósito.
