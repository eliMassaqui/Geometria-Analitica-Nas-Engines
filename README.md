🧠 Geometria Analítica Aplicada a Engines e Jogos Imersivos

> Matemática de precisão, mundos de impacto.



Este repositório é um compêndio técnico voltado para a aplicação de Geometria Analítica no desenvolvimento de motores gráficos e jogos 3D interativos com Unity. Cada conceito matemático aqui abordado possui aplicação direta na lógica espacial computacional, permitindo o domínio total sobre posições, trajetórias, colisões e rotações em ambientes tridimensionais.


---

🎮 Relevância Estratégica

Em jogos, nada é aleatório — tudo é vetorado, rotacionado e interpolado.

A Geometria Analítica fornece as ferramentas matemáticas que tornam possível:

🎯 Projéteis guiados com precisão vetorial;

🎥 Câmeras orbitais suaves e responsivas;

🧠 Sistemas de IA com campo de visão tático;

🧱 Mapas modulares com simetria, aleatoriedade e controle espacial rigoroso;

🌀 Rotações suaves sem perda de eixo (quaternions);

🔍 Colisões e detecções baseadas em equações exatas.


> Transforme o cálculo vetorial em mecânicas de jogo com propósito.




---

✍️ Fundamentos Teóricos + Implementações Técnicas

Cada seção abaixo traduz um conceito matemático em lógica operacional de game engine. As fórmulas são acompanhadas de código funcional em C# para uso imediato na Unity.

📏 1. Distância entre dois pontos (2D e 3D)

Uso: Proximidade entre entidades, verificação de colisão, raio de alcance.

Fórmulas:
2D: 
3D: 

float DistanciaEntrePontos(Vector3 a, Vector3 b)
{
    return Vector3.Distance(a, b);
}


---

🧭 2. Equação Paramétrica da Reta

Uso: Definição de trajetórias lineares, lasers, movimentos contínuos.

Fórmula: 

Vector3 RetaParametrica(Vector3 pontoInicial, Vector3 direcao, float t)
{
    return pontoInicial + t * direcao;
}


---

🔄 3. Produto Escalar (Dot Product)

Uso: Cálculo de ângulos, verificação de alinhamento, campo de visão.

Fórmula: 

float ProdutoEscalar(Vector3 a, Vector3 b)
{
    return Vector3.Dot(a.normalized, b.normalized);
}

> Se o resultado for próximo de 1, os vetores estão alinhados. Se for 0, são ortogonais.




---

✖️ 4. Produto Vetorial (Cross Product)

Uso: Cálculo de vetores normais a superfícies, torques e eixos de rotação.

Vector3 ProdutoVetorial(Vector3 a, Vector3 b)
{
    return Vector3.Cross(a, b);
}

> Essencial para física vetorial e sombreamento em 3D.




---

🧾 5. Equação do Plano

Fórmula: 

Uso: Criação de superfícies planas, detecção de impacto contra paredes, triggers invisíveis.

bool PontoNoPlano(Vector3 ponto, float A, float B, float C, float D)
{
    float resultado = A * ponto.x + B * ponto.y + C * ponto.z + D;
    return Mathf.Approximately(resultado, 0f);
}


---

🌐 6. Circunferência (2D)

Fórmula: 

Uso: Zonas de ação, radares circulares, magias em área.

bool PontoDentroDeCircunferencia(Vector2 ponto, Vector2 centro, float raio)
{
    return Vector2.Distance(ponto, centro) <= raio;
}


---

♻️ 7. Rotação 2D com Números Complexos

Fórmula: 

Uso: Rotações de sprites, movimento circular, economia computacional.

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


---

🌀 8. Slerp com Quaternions

Uso: Interpolação esférica de rotações. Evita Gimbal Lock e preserva orientações suaves.

Quaternion RotacaoSuave(Quaternion inicio, Quaternion fim, float t)
{
    return Quaternion.Slerp(inicio, fim, t);
}

> Essencial para câmeras orbitais, drones, e entidades voadoras com controle realista.




---

🧠 Conclusão Executiva

Geometria Analítica é infraestrutura invisível de qualquer engine de sucesso.

Compreender vetores, planos e quaternions não é apenas requisito acadêmico — é uma vantagem técnica competitiva. Este repositório existe para que desenvolvedores possam sair do empirismo visual e entrar no controle matemático rigoroso do espaço interativo.

> Domine o espaço. Projete com precisão. Programe com propósito.



