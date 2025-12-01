# 🚗 Projeto de Realidade Aumentada - Exposição Virtual de Veículos

Projeto de Realidade Aumentada desenvolvido para disciplina universitária, utilizando **AR.js** e **A-Frame** para criar uma experiência imersiva de visualização de modelos 3D de veículos através de marcadores.

## 📋 Descrição

Este projeto permite visualizar 5 modelos 3D de veículos diferentes em Realidade Aumentada, utilizando marcadores fiduciais. Basta apontar a câmera do smartphone ou webcam para um dos marcadores impressos para ver o veículo correspondente em 3D sobreposto ao mundo real.

## 🎯 Versões Disponíveis

### 1. Versão Completa com Seletor (index.html) ⭐ RECOMENDADO
- **5 veículos diferentes** selecionáveis por botões
- **1 marcador:** Hiro (único marcador necessário)
- **Interface interativa:** Botões na parte inferior para trocar entre veículos
- **Ideal para:** Demonstração completa e interativa do projeto

### 2. Versão Simples (index-hiro.html)
- **1 veículo:** Police Car
- **1 marcador:** Hiro (padrão AR.js)
- **Ideal para:** Testes rápidos e demonstrações simples

### 3. Versão Multi-Marcador (index-multi.html)
- **5 veículos com 5 marcadores diferentes** (experimental)
- **Marcadores:** Hiro, Kanji, Letter A, B, F
- **Nota:** Requer múltiplos marcadores impressos

## 🚀 Como Usar

### Passo 1: Preparar o Marcador

**Versão Completa (index.html) - RECOMENDADO:**
- Você precisa apenas do **marcador Hiro**
- Use o arquivo `marcador_police.png` na raiz do projeto
- Ou `assets/markers/hiro.png`
- Imprima em papel branco A4 (tamanho mínimo 5x5cm)

**Versão Multi-Marcador (index-multi.html) - Opcional:**
- Requer 5 marcadores diferentes
- Veja [MARCADORES_PARA_IMPRIMIR.html](MARCADORES_PARA_IMPRIMIR.html) para mais detalhes

### Passo 2: Executar o Projeto

#### Opção A: Usando Python (Recomendado)

```bash
# Navegue até a pasta do projeto
cd /caminho/para/atv_ra_henning

# Inicie um servidor HTTP
python3 -m http.server 8000

# Acesse no navegador
# Local: http://localhost:8000/index.html
```

#### Opção B: Usando ngrok (Para testar no celular via HTTPS)

```bash
# Em um terminal, inicie o servidor Python
python3 -m http.server 8000

# Em outro terminal, inicie o ngrok
ngrok http 8000

# Use a URL HTTPS fornecida pelo ngrok no seu celular
# Exemplo: https://xxxxx.ngrok-free.dev/index.html
```

### Passo 3: Testar a Experiência AR

**Versão Completa (index.html):**
1. Abra a URL no navegador (Chrome ou Safari)
2. Permita o acesso à câmera quando solicitado
3. Aponte a câmera para o **marcador Hiro** impresso
4. Veja o veículo 3D aparecer sobre o marcador!
5. **Use os botões na parte inferior** para alternar entre os 5 veículos disponíveis
6. Os botões aparecem automaticamente quando o marcador é detectado

**Recursos Interativos:**
- 🔘 Botões coloridos para cada veículo
- 🟢 Indicador visual do veículo ativo
- 📱 Interface responsiva para mobile
- ⚡ Troca instantânea entre modelos

## 📱 Compatibilidade

### Navegadores Suportados:
- ✅ Google Chrome (Desktop e Mobile)
- ✅ Safari (iOS - requer HTTPS)
- ✅ Firefox (Desktop)
- ⚠️ Edge (pode ter limitações)

### Requisitos:
- Câmera (webcam ou câmera do smartphone)
- Conexão HTTPS (obrigatório para iOS/Safari)
- Iluminação adequada
- Marcadores impressos ou exibidos em tela

## 🛠️ Tecnologias Utilizadas

- **HTML5** - Estrutura da aplicação
- **JavaScript (ES6)** - Lógica e interatividade
- **A-Frame 1.5.0** - Framework para WebVR/WebXR
- **AR.js** - Biblioteca de Realidade Aumentada
- **WebGL** - Renderização 3D no navegador
- **getUserMedia API** - Acesso à câmera

## 📂 Estrutura do Projeto

```
atv_ra_henning/
├── index.html                   # Versão completa com seletor ⭐ PRINCIPAL
├── index-hiro.html              # Versão simples (1 veículo)
├── index-multi.html             # Versão multi-marcador (experimental)
├── MARCADORES_PARA_IMPRIMIR.html # Guia de marcadores
├── README.md                    # Este arquivo
├── marcador_police.png          # Marcador Hiro para impressão
├── assets/
│   ├── models/                  # Modelos 3D GLB
│   │   ├── police_car.glb       # 9.2 MB - Carro de polícia
│   │   ├── audi_pb18_e_tron_low_poly_3d.glb  # 577 KB - Audi
│   │   ├── generic_sedan_car.glb             # 52 MB - Sedan
│   │   ├── generic_sport_coupe_car.glb       # 42 MB - Cupê
│   │   └── red_car.glb          # 5.9 MB - Carro vermelho
│   └── markers/                 # Marcadores AR
│       ├── hiro.png             # Marcador Hiro
│       └── MARCADORES.md        # Documentação dos marcadores
```

## 🎨 Modelos 3D

**Versão Principal (index.html) - Todos com marcador Hiro:**

| Veículo | Arquivo | Tamanho | Botão |
|---------|---------|---------|-------|
| Police Car | police_car.glb | 9.2 MB | Police Car |
| Audi PB18 e-tron | audi_pb18_e_tron_low_poly_3d.glb | 577 KB | Audi e-tron |
| Generic Sedan | generic_sedan_car.glb | 52 MB | Sedan |
| Sport Coupé | generic_sport_coupe_car.glb | 42 MB | Sport Coupé |
| Red Car | red_car.glb | 5.9 MB | Red Car |

## 💡 Dicas para Melhor Experiência

1. **Iluminação:** Use ambiente bem iluminado, evite contra-luz
2. **Marcador:** Imprima em boa qualidade, sem manchas ou dobras
3. **Distância:** Mantenha 20-50cm entre câmera e marcador
4. **Estabilidade:** Mantenha o marcador em superfície plana e estável
5. **Performance:** Use a versão simples (index-hiro.html) em dispositivos mais antigos
6. **Seleção de Veículos:** Os botões aparecem automaticamente quando o marcador é detectado
7. **Troca de Modelos:** Clique nos botões coloridos para alternar entre os veículos instantaneamente

## ⚙️ Configurações e Personalização

### Ajustar Escala do Modelo

No arquivo HTML, localize a entidade do veículo e ajuste o parâmetro `scale`:

```html
<a-entity
    gltf-model="#model-id"
    scale="0.5 0.5 0.5"    <!-- Aumentar ou diminuir valores -->
    position="0 0 0"
    rotation="0 0 0">
</a-entity>
```

### Adicionar Novos Modelos

1. Coloque o arquivo `.glb` em `assets/models/`
2. Adicione referência em `<a-assets>`:
```html
<a-asset-item id="novo-modelo" src="./assets/models/seu_modelo.glb"></a-asset-item>
```
3. Crie um novo marcador:
```html
<a-marker preset="kanji" id="marker-novo">
    <a-entity gltf-model="#novo-modelo" scale="1 1 1"></a-entity>
</a-marker>
```

## 🐛 Solução de Problemas

### Câmera não abre
- **Causa:** Permissão negada ou HTTPS não configurado
- **Solução:** Use HTTPS (ngrok) ou permita acesso à câmera nas configurações do navegador

### Marcador não detecta
- **Causa:** Iluminação ruim, marcador borrado ou muito pequeno
- **Solução:** Melhore iluminação, imprima marcador maior (mínimo 5x5cm)

### Modelo não aparece
- **Causa:** Arquivo GLB corrompido ou caminho errado
- **Solução:** Verifique console do navegador (F12) para erros, confirme caminho do arquivo

### Performance lenta
- **Causa:** Modelos muito grandes (generic_sedan: 52MB)
- **Solução:** Use versão simples ou reduza qualidade dos modelos

## 📝 Licença

Projeto desenvolvido para fins educacionais - Disciplina Universitária

## 👤 Autor

Desenvolvido por Adauto Souza
- Projeto: Realidade Aumentada com AR.js
- Curso: [Sua Instituição/Curso]
- Data: Novembro 2025

## 🙏 Agradecimentos

- [AR.js](https://ar-js-org.github.io/AR.js-Docs/) - Framework de AR
- [A-Frame](https://aframe.io/) - Framework WebVR
- [Sketchfab](https://sketchfab.com/) - Modelos 3D utilizados
- Comunidade open-source

---

**Nota:** Este projeto requer HTTPS para funcionar em dispositivos iOS (iPhone/iPad). Use ngrok para criar um túnel HTTPS local durante os testes.
