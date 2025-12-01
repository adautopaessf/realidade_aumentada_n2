# 📦 Pasta de Modelos 3D

## Instruções

Coloque seu arquivo de modelo 3D aqui:

- **Nome do arquivo:** `carro.glb`
- **Formato:** GLB ou glTF
- **Modelo:** LADA VAZ 2106 (ou qualquer carro de sua preferência)

## Como Obter o Modelo

### Opção 1: Modelo LADA VAZ 2106 (Recomendado)

1. Acesse: https://sketchfab.com/3d-models/lada-2106-b77f65712abe4e49b6df1e26dcdeb8e5
2. Clique em "Download 3D Model"
3. Selecione formato GLB
4. Salve como `carro.glb` nesta pasta

### Opção 2: Modelo de Teste Rápido

Execute este comando no terminal (na raiz do projeto):

```bash
curl -o assets/models/carro.glb https://raw.githubusercontent.com/KhronosGroup/glTF-Sample-Models/master/2.0/CesiumMilkTruck/glTF-Binary/CesiumMilkTruck.glb
```

### Opção 3: Outros Sites

- **Sketchfab:** https://sketchfab.com/
- **Free3D:** https://free3d.com/
- **TurboSquid:** https://www.turbosquid.com/
- **Poly Haven:** https://polyhaven.com/

## Verificar o Modelo

Antes de usar, teste o modelo em:
- https://gltf-viewer.donmccurdy.com/

## Otimizar o Modelo

Se o modelo estiver muito grande (>20MB):
- https://gltf.report/

## Estrutura Esperada

```
assets/models/
└── carro.glb   ← Seu arquivo deve estar aqui
```

## Formatos Suportados

- ✅ **GLB** (recomendado) - arquivo único
- ✅ **glTF** - pode vir com arquivos .bin e texturas separadas

**Dica:** GLB é mais fácil pois tudo está em um único arquivo!
