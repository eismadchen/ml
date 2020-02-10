# Сборка рабочего "окружения" для Fedora Workstation 31

1. Добавить репозитории RPM Fusion и обновить все пакеты программного обеспечения

```
sudo dnf install https://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm https://download1.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm

dnf update

```

2. Скачать установщик **[Anaconda](https://www.anaconda.com/distribution/#download-section)** (пакетный менеджер, нужен для простой загрузки нужных библиотек со всеми зависимостями)

3. Установить в `/opt/Anaconda3`

```
sudo chmod 777 ./Anaconda3-2019.10-Linux-x86_64.sh
./Anaconda3-2019.10-Linux-x86_64.sh
```

4. Добавить путь к установленным исходникам в ~/.bashrc

```
PATH=$PATH:/opt/Anaconda3
```

5. Установить Jupyter lab

```
conda install -c conda-forge jupyterlab
```

6. Установить пакеты Julia с помощью пакетного менеджера dnf:

```
dnf install julia
```

7. Скачать .rpm пакет редактора **[Atom](https://atom.io/)** и установить его
8. Дальнейшие инструкции по установке пакета Juno можно найти **[тут](https://atom.io/)** 
