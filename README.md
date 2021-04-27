dnsmasq-regex for OpenWrt/LEDE
Thanks to @aa65535
This is the dnsmasq-regex Makefile for OpenWrt 15.05(or higher) or LEDE.
Compile
Klonen Sie das Git-File und überprüfen Sie das Ergebnis
For OpenWrt:
# Für OpenWrt 15.05 und neuer die Zielplattform ar71xx
tar xjf OpenWrt-SDK-ar71xx-for-linux-x86_64-gcc-4.8-linaro_uClibc-0.9.33.2.tar.bz2
cd OpenWrt-SDK-ar71xx-*

# Clone den openWRT-Zweig
git clone -b openwrt https://github.com/lixingcong/dnsmasq-regex-openwrt package/dnsmasq
For LEDE:
# Für LEDE 17.01.4 die Zielplattform ar71xx 
tar xjf lede-sdk-17.01.4-ar71xx-generic_gcc-5.4.0_musl-1.1.16.Linux-x86_64.tar.xz
cd lede-sdk-17.01.4-*

# Clone den LEDE-Zweig
git clone -b lede https://github.com/lixingcong/dnsmasq-regex-openwrt package/dnsmasq
Build it:
# Wählen Sie die Datei aus, die Sie kompilieren möchten. dnsmasq，Drücken Sie M, um
# Base system -> dnsmasq 
make menuconfig

# Beginnen Sie mit der Kompilierung
make package/dnsmasq/compile V=99

# finde ipk Pack

find bin | grep dnsmasq
Regex match domains config
# Example here:
https://github.com/lixingcong/dnsmasq-regex-openwrt/blob/lede/conf-files-example/dnsmasq.conf


