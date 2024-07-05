# Linux 6.1.y
* Realtek 8852B SDIO Wireless driver


Add to source-tree
```
rm -fdr drivers/net/wireless/realtek/rtl8852bs
mkdir -p drivers/net/wireless/realtek/rtl8852bs
cp -fr ../rtl8852bs/* drivers/net/wireless/realtek/rtl8852bs/
rm -f drivers/net/wireless/realtek/rtl8852bs/README.md
echo "obj-\$(CONFIG_RTL8852BS)		+= rtl8852bs/" >> drivers/net/wireless/realtek/Makefile
sed -i '/source "drivers\/net\/wireless\/realtek\/rtl818x\/Kconfig"/a source "drivers\/net\/wireless\/realtek\/rtl8852bs\/Kconfig"' \
	"drivers/net/wireless/realtek/Kconfig"
```
