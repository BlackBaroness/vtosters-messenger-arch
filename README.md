Спасибо [FabioLolix](https://github.com/FabioLolix) за помощь.

Это установщик VTosters Messenger, форка VK Messenger, для Arch Linux и производных, таких как Manjaro.
Я не являюсь разработчиком этого форка. Оригинал [здесь](https://vtosters.app/).

Он нацелен на платформу x86_64.

Проблема этого пакета в том, что разработчики постят обновления в телеграм-канале. Поэтому приходится
вот так поставлять архив, перекачивая его оттуда.

## Установка
```bash
sudo pacman -S base-devel --needed
git clone https://github.com/BlackBaroness/vtosters-messenger-arch
cd vtosters-messenger-arch/
makepkg -si
```

## Удаление
```bash
sudo pacman -R vtmessenger
```

