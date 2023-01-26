# Computação Gráfica

## Construções

1. Iluminação - esfera.
2. Iluminação - prismas e pirâmides.
3. Objeto (.obj ou .ply).
4. Esfera com textura.

## Instalação

Será necessário apenas o **Python 3.8** com o venv instalado. Inicie um novo venv e instale as dependências com o arquivo `requirements.txt`:

```bash
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

Caso você esteja executando via WSL, pode se deparar com vários erros. Isso ocorre pela falta de uma interface gráfica. Para contornar esse problema, vamos instalar algumas libs e forçar o uso de uma delas para a construção das interfaces:

```bash
sudo apt install ubuntu-desktop mesa-utils freeglut3-dev
export PYOPENGL_PLATFORM=glx
export LIBGL_ALWAYS_INDIRECT=0
```

Do lado do Windows, ainda será necessário instalar o [VcXsrv](https://sourceforge.net/projects/vcxsrv/) e escolher as opções `Multiple Windows`, `display 0`, `start no client` e `disable native opengl`. Se quiser mais informações, pode dar uma olhada na [issue #2855](https://github.com/microsoft/WSL/issues/2855) do WSL.

Agora para rodar as soluções, basta executar os arquivos `app.py` dentro de cada pasta. Por exemplo:

```bash
python c1/app.py
python c2/app.py
python c3/app.py
python c4/app.py
```

Em todas as soluções é possível movimentar o objeto clicando e arrastando na tela com o botão esquerdo do mouse, movimentar usando o botão direito do mouse e com o botão central se afastar ou aproximar. Além disso, se quiser fechar o programa, basta pressionar a tecla `ESC`.

> **Nota:** Caso tenha passado pelos problemas no WSL e os tenha corrigido como descrito acima, não se esqueça de executar `export PYOPENGL_PLATFORM=glx` e `export LIBGL_ALWAYS_INDIRECT=0` sempre que for rodar o projeto, antes ou depois de executar `source venv/bin/activate`.