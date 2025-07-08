# 🧠 Geometria Analítica para Engines e Jogos Imersivos

> **Transforme fórmulas matemáticas em mundos vivos.**

Este repositório conecta a precisão da **Geometria Analítica** à liberdade criativa do **desenvolvimento de jogos em Unity**.
Aqui, vetores, planos e quaternions deixam de ser abstrações e tornam-se **instrumentos de controle absoluto sobre o espaço tridimensional interativo**.

---

## 🎮 Por Que Isso Importa?

Em um **jogo**, nada é por acaso.
Cada **movimento**, **colisão**, **campo de visão** e **rotação** é consequência direta de uma equação.

Com Geometria Analítica, você programa:

* 🎯 *Balas* que seguem inimigos com precisão vetorial.
* 🎥 *Câmeras* orbitais suaves em 360°.
* 🧠 *IA* que detecta jogadores por campo de visão.
* 🌐 *Mapas modulares*, simétricos ou caóticos com lógica espacial rigorosa.

> **Matemática que move pixels com propósito.**

---

## ✍️ Fundamentos Teóricos com Código Prático

### 📏 1. Distância entre dois pontos (2D e 3D)

**Aplicação:** Proximidade, colisão, alcance.

**Fórmulas:**
2D: $d = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2}$
3D: $d = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2 + (z_2 - z_1)^2}$

```csharp
float DistanciaEntrePontos(Vector3 a, Vector3 b)
{
    return Vector3.Distance(a, b);
}
```

### 🗺️ 2. Equação da reta (paramétrica)

**Aplicação:** Trajetórias, movimentações, projéteis.

**Fórmula:** $\vec{r}(t) = \vec{P}_0 + t \cdot \vec{v}$

```csharp
Vector3 RetaParametrica(Vector3 pontoInicial, Vector3 direcao, float t)
{
    return pontoInicial + t * direcao;
}
```

### ♻️ 3. Produto Escalar (Dot Product)

**Aplicação:** Visão, alinhamento, ângulos de ataque, FOV.

**Fórmula:** $\vec{a} \cdot \vec{b} = |\vec{a}| \cdot |\vec{b}| \cdot \cos(\theta)$

```csharp
float ProdutoEscalar(Vector3 a, Vector3 b)
{
    return Vector3.Dot(a.normalized, b.normalized);
}
```

### ✖️ 4. Produto Vetorial (Cross Product)

**Aplicação:** Normais, torque, rotações ortogonais.

```csharp
Vector3 ProdutoVetorial(Vector3 a, Vector3 b)
{
    return Vector3.Cross(a, b);
}
```

### 🗒️ 5. Equação do Plano

**Fórmula:** $Ax + By + Cz + D = 0$

**Uso:** Superfícies planas, colisão com paredes, limites.

```csharp
bool PontoNoPlano(Vector3 ponto, float A, float B, float C, float D)
{
    float resultado = A * ponto.x + B * ponto.y + C * ponto.z + D;
    return Mathf.Approximately(resultado, 0f);
}
```

### 🌀 6. Circunferência (2D)

**Fórmula:** $(x - a)^2 + (y - b)^2 = r^2$

**Uso:** Zonas de ação, detecção radial, efeitos.

```csharp
bool PontoDentroDeCircunferencia(Vector2 ponto, Vector2 centro, float raio)
{
    return Vector2.Distance(ponto, centro) <= raio;
}
```

### 🎈 7. Rotação 2D com Números Complexos

**Fórmula:** $z' = z \cdot (\cos \theta + i \sin \theta)$

**Uso:** Rotações leves e precisas em 2D.

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

### 🌀 8. Slerp com Quaternions

**Uso:** Rotações suaves sem gimbal lock (câmeras, naves, drones).

```csharp
Quaternion RotacaoSuave(Quaternion inicio, Quaternion fim, float t)
{
    return Quaternion.Slerp(inicio, fim, t);
}
```

---

## 🎯 Conclusão

**Geometria Analítica não é apenas equação: é engenharia espacial.**
Compreender e aplicar esses conceitos é essencial para qualquer desenvolvedor que almeje criar jogos com **mecânicas coerentes**, **movimentos realistas** e **mundos digitais imersivos**.

> Dominando a matemática, você domina o espaço.
