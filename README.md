1. Implemente as linhas seguintes ao final do arquivo ~/.zshrc
2. Personalize o arquivo script.sh com o seu script personalizado

```shell
# ----------
# Scripts personalizados para o zsh
SCRIPT_URL='https://gist.github.com/3843d3d8c6455e854641f6580167d271.git'
FOLDER_NAME='.custom_script'
DIR="$HOME/$FOLDER_NAME"

# Se os arquivos já estiverem clonados apenas atualizar
if [ -d $DIR ]; then
    echo 'Atualizando scripts'
    git -C $DIR pull
# Senão, clonar todos os arquivos
else
    echo 'Clonando scripts'
    git clone $SCRIPT_URL $FOLDER_NAME
fi

# Definir arquivo como fonte
source ~/.custom_script/script.sh
```