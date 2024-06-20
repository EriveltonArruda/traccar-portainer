# traccar-portainer

1º Integre o WSL com o Docker (siga a documentação do wsl)

2º Instale o portainer-CE no WSL seguindo o passo a passo pelo link:
https://docs.portainer.io/start/install-ce/server/docker/linux

3º Após isntalar o portainer não entre nele ainda, gere primeiro a config do traccar dentro do wsl do Ubuntu, isso vai criar o arquivo traccar.xml que é necessário para rodar o portainer.
bash -c "$(wget -qLO - https://raw.githubusercontent.com/bigbeartechworld/big-bear-scripts/master/generate-traccar-config/run.sh)"

4º Entre no Portainer via localhost:9443, selecione a opção stack no lado esquerdo e crie uma nova stack

5º Na nova Stack, coloque o conteúdo do docker-composer.yml que está neste repositório dentro da pasta instalar-traccar-portainer;

6º Pronto, o traccar está instalado e rodando no Docker no seu WSL2
