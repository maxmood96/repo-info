<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.28`](#telegraf128)
-	[`telegraf:1.28-alpine`](#telegraf128-alpine)
-	[`telegraf:1.28.5`](#telegraf1285)
-	[`telegraf:1.28.5-alpine`](#telegraf1285-alpine)
-	[`telegraf:1.29`](#telegraf129)
-	[`telegraf:1.29-alpine`](#telegraf129-alpine)
-	[`telegraf:1.29.5`](#telegraf1295)
-	[`telegraf:1.29.5-alpine`](#telegraf1295-alpine)
-	[`telegraf:1.30`](#telegraf130)
-	[`telegraf:1.30-alpine`](#telegraf130-alpine)
-	[`telegraf:1.30.2`](#telegraf1302)
-	[`telegraf:1.30.2-alpine`](#telegraf1302-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.28`

```console
$ docker pull telegraf@sha256:cff3d01c9ed05a3fc44dad3a86dac60aac3af75ac6cb3c366baec81792255f83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.28` - linux; amd64

```console
$ docker pull telegraf@sha256:b2cd201bea34161806e76ba49b62898b6d9606898bb01583f82fb202194c4f71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.8 MB (149849951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af1ea27c25a80d3f8531f0553f278fc334ac77e965fb4a167029c18fb5f2071`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:34 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
# Wed, 10 Apr 2024 01:50:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:24:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 17:16:34 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 17:16:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 17:16:35 GMT
ENV TELEGRAF_VERSION=1.28.5
# Wed, 10 Apr 2024 17:16:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 10 Apr 2024 17:16:42 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 10 Apr 2024 17:16:42 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Wed, 10 Apr 2024 17:16:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 17:16:42 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7247ea8d81e671d079d67f3a9909315ef4641b45db90d62a1b18e3430c1937d4`  
		Last Modified: Wed, 10 Apr 2024 05:34:49 GMT  
		Size: 24.0 MB (24046793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c65925cef157ec92ca4ac7ea2fee498997e6f04ceabcc6f5ba6ceec5ff79712`  
		Last Modified: Wed, 10 Apr 2024 17:17:26 GMT  
		Size: 19.2 MB (19151211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e46883b5de031b19b1f858d24ef5c262d06bb7b3105c84db483d710445599e8`  
		Last Modified: Wed, 10 Apr 2024 17:17:23 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8231ba5bf87ff82c9735a2ac75912cf49c80f1660eaa3654159f24b51aba627`  
		Last Modified: Wed, 10 Apr 2024 17:17:32 GMT  
		Size: 57.1 MB (57089148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d114c8e4e5d25e37931d6488a73c1dbd4c2d8741fa03c98ca827e614c3d19b5a`  
		Last Modified: Wed, 10 Apr 2024 17:17:23 GMT  
		Size: 625.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.28` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:8eca32c3467aec622a0255394692b142f94da27625551907640b6581a61ffcdb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137618199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402855611bde250bd2980700760ce8dfa5c0684a846926fe1c88d2bac2a929bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 24 Apr 2024 04:06:51 GMT
ADD file:b6d26ef7cfc03fe202f7a5ac219566bc37f382ffadc9acdad685f2dd318cf0e4 in / 
# Wed, 24 Apr 2024 04:06:52 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:50:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 14:05:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 14:05:51 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 24 Apr 2024 14:05:51 GMT
ENV TELEGRAF_VERSION=1.28.5
# Wed, 24 Apr 2024 14:06:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 24 Apr 2024 14:06:00 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 24 Apr 2024 14:06:01 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Wed, 24 Apr 2024 14:06:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 14:06:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:80e84b3257949a283234599e3906626cfb4ff482d06fa4dc3eaf1dd36551dafa`  
		Last Modified: Wed, 24 Apr 2024 04:10:48 GMT  
		Size: 45.2 MB (45174994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52886721ea5a8a8bac2b197dccd42a74948b88bedcfe0fdf8b24e234c0a660d0`  
		Last Modified: Wed, 24 Apr 2024 05:02:39 GMT  
		Size: 22.0 MB (21953968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49ff3c62cfa8259ba641f429364c1c98fb99aaace66ea71c110c0f3f6a2069b`  
		Last Modified: Wed, 24 Apr 2024 14:06:47 GMT  
		Size: 17.9 MB (17932145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbf8d083657a1224c565a90b217288b841ff1f78db931977faaf6c32f8233ac`  
		Last Modified: Wed, 24 Apr 2024 14:06:42 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68bfc520cba75e16ac65e5d93a50cad1a1a01c1c498734417cacb01dd244e36`  
		Last Modified: Wed, 24 Apr 2024 14:06:54 GMT  
		Size: 52.6 MB (52554656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00438e3d5b9495720a2e89b6686778ae1deef4f951e3a6450b83ba8b652875a6`  
		Last Modified: Wed, 24 Apr 2024 14:06:42 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.28` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:0d1a9fcae9b0347a9a530fdee1435c7fa9f37f2047e102f40686db1a976fd3dd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (144030517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0b9a7332a2f6425127c2a832e966c9da16a1b953a855625b72bbc69e136383`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:32:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 13:45:12 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 13:45:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 24 Apr 2024 13:45:13 GMT
ENV TELEGRAF_VERSION=1.28.5
# Wed, 24 Apr 2024 13:45:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 24 Apr 2024 13:45:20 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 24 Apr 2024 13:45:20 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Wed, 24 Apr 2024 13:45:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 13:45:21 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e100ddc6b415c632410507293430c0fe6bb4228ab320ed59548c6dc030b4e4a`  
		Last Modified: Wed, 24 Apr 2024 08:41:28 GMT  
		Size: 23.6 MB (23586795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935286a1f591251a12c663afdc2596adc4e8b91d91c60c7d53907023fed11a0`  
		Last Modified: Wed, 24 Apr 2024 13:46:02 GMT  
		Size: 19.1 MB (19077226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68421de5c53c46a30146ebc2684bda6aaf65e702e559619ca40243653b5623d8`  
		Last Modified: Wed, 24 Apr 2024 13:45:59 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58e667f2485042742589df6b5d154367ede643d1045ebbae560175210d0e12c`  
		Last Modified: Wed, 24 Apr 2024 13:46:05 GMT  
		Size: 51.8 MB (51750731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe0fc9e0da78a55a803b90c434772adf08fafa1227c8096a8349f033ad12b834`  
		Last Modified: Wed, 24 Apr 2024 13:46:00 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.28-alpine`

```console
$ docker pull telegraf@sha256:57bc33034b6d4d6a96f731b8265a2c9b3985311060ce359879b0fd6ae9b43c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:1.28-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:f7029c882a1e0d8dcba490bac1e95c52907200b5be69479a501eba9d9bd93475
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62934041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7687f8b8bb846071a28467f7e04ee14b36738636e4c07cac62275932bac3259`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:56:08 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 08:56:10 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 16 Mar 2024 08:56:10 GMT
ENV TELEGRAF_VERSION=1.28.5
# Sat, 16 Mar 2024 08:56:17 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 16 Mar 2024 08:56:17 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 16 Mar 2024 08:56:17 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 16 Mar 2024 08:56:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 08:56:17 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162ebdf1596ab6dcfd486bee21886e418f16f6c426a8dd266cba7da20b557281`  
		Last Modified: Sat, 16 Mar 2024 08:56:58 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdd04d97f3dab462dc59e41d85f02932280e01a7d7a2cd1d24c977e5ae0b583`  
		Last Modified: Sat, 16 Mar 2024 08:56:59 GMT  
		Size: 2.6 MB (2610463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc84cbb6d9e3d0bc47ba96808f7dad0ea7ae3dea5956e44a69ad86374660666`  
		Last Modified: Sat, 16 Mar 2024 08:57:07 GMT  
		Size: 56.9 MB (56914244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f389965f1bfc3e1b5beec1fe0af5e3abe25a32310c0f26c303f66e844988f98`  
		Last Modified: Sat, 16 Mar 2024 08:56:58 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.28-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:58b50c2433f9a957d62b40780760df86989c7d7fb6db583f29a82de80c84f609
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57629106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ebbf0803b5bb23e9014912e03226a830106c5da0014f838310c29d6c28e512`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:41:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 02:41:47 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 16 Mar 2024 02:41:47 GMT
ENV TELEGRAF_VERSION=1.28.5
# Sat, 16 Mar 2024 02:41:53 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 16 Mar 2024 02:41:54 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 16 Mar 2024 02:41:54 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 16 Mar 2024 02:41:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 02:41:55 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2675ee4ddf03252fa477bd14d6e59e0470e73d69c7fb12bade1d12e074715140`  
		Last Modified: Sat, 16 Mar 2024 02:42:34 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870e8831f6d198a84a383f159cec54a3ee90276d6772ca50a61c7cd967628656`  
		Last Modified: Sat, 16 Mar 2024 02:42:35 GMT  
		Size: 2.7 MB (2692939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed275664d335915c59116fc4dcb505bd5b0ccd59b112b85c7d0dbecb230b7bd8`  
		Last Modified: Sat, 16 Mar 2024 02:42:40 GMT  
		Size: 51.6 MB (51587851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca806e7a7334d09e576e9279db970934609cd4b9ad9828ebcf85b589837195e`  
		Last Modified: Sat, 16 Mar 2024 02:42:34 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.28.5`

```console
$ docker pull telegraf@sha256:cff3d01c9ed05a3fc44dad3a86dac60aac3af75ac6cb3c366baec81792255f83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.28.5` - linux; amd64

```console
$ docker pull telegraf@sha256:b2cd201bea34161806e76ba49b62898b6d9606898bb01583f82fb202194c4f71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.8 MB (149849951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af1ea27c25a80d3f8531f0553f278fc334ac77e965fb4a167029c18fb5f2071`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:34 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
# Wed, 10 Apr 2024 01:50:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:24:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 17:16:34 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 17:16:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 17:16:35 GMT
ENV TELEGRAF_VERSION=1.28.5
# Wed, 10 Apr 2024 17:16:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 10 Apr 2024 17:16:42 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 10 Apr 2024 17:16:42 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Wed, 10 Apr 2024 17:16:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 17:16:42 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7247ea8d81e671d079d67f3a9909315ef4641b45db90d62a1b18e3430c1937d4`  
		Last Modified: Wed, 10 Apr 2024 05:34:49 GMT  
		Size: 24.0 MB (24046793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c65925cef157ec92ca4ac7ea2fee498997e6f04ceabcc6f5ba6ceec5ff79712`  
		Last Modified: Wed, 10 Apr 2024 17:17:26 GMT  
		Size: 19.2 MB (19151211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e46883b5de031b19b1f858d24ef5c262d06bb7b3105c84db483d710445599e8`  
		Last Modified: Wed, 10 Apr 2024 17:17:23 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8231ba5bf87ff82c9735a2ac75912cf49c80f1660eaa3654159f24b51aba627`  
		Last Modified: Wed, 10 Apr 2024 17:17:32 GMT  
		Size: 57.1 MB (57089148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d114c8e4e5d25e37931d6488a73c1dbd4c2d8741fa03c98ca827e614c3d19b5a`  
		Last Modified: Wed, 10 Apr 2024 17:17:23 GMT  
		Size: 625.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.28.5` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:8eca32c3467aec622a0255394692b142f94da27625551907640b6581a61ffcdb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137618199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:402855611bde250bd2980700760ce8dfa5c0684a846926fe1c88d2bac2a929bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 24 Apr 2024 04:06:51 GMT
ADD file:b6d26ef7cfc03fe202f7a5ac219566bc37f382ffadc9acdad685f2dd318cf0e4 in / 
# Wed, 24 Apr 2024 04:06:52 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:50:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 14:05:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 14:05:51 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 24 Apr 2024 14:05:51 GMT
ENV TELEGRAF_VERSION=1.28.5
# Wed, 24 Apr 2024 14:06:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 24 Apr 2024 14:06:00 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 24 Apr 2024 14:06:01 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Wed, 24 Apr 2024 14:06:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 14:06:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:80e84b3257949a283234599e3906626cfb4ff482d06fa4dc3eaf1dd36551dafa`  
		Last Modified: Wed, 24 Apr 2024 04:10:48 GMT  
		Size: 45.2 MB (45174994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52886721ea5a8a8bac2b197dccd42a74948b88bedcfe0fdf8b24e234c0a660d0`  
		Last Modified: Wed, 24 Apr 2024 05:02:39 GMT  
		Size: 22.0 MB (21953968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49ff3c62cfa8259ba641f429364c1c98fb99aaace66ea71c110c0f3f6a2069b`  
		Last Modified: Wed, 24 Apr 2024 14:06:47 GMT  
		Size: 17.9 MB (17932145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbf8d083657a1224c565a90b217288b841ff1f78db931977faaf6c32f8233ac`  
		Last Modified: Wed, 24 Apr 2024 14:06:42 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68bfc520cba75e16ac65e5d93a50cad1a1a01c1c498734417cacb01dd244e36`  
		Last Modified: Wed, 24 Apr 2024 14:06:54 GMT  
		Size: 52.6 MB (52554656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00438e3d5b9495720a2e89b6686778ae1deef4f951e3a6450b83ba8b652875a6`  
		Last Modified: Wed, 24 Apr 2024 14:06:42 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.28.5` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:0d1a9fcae9b0347a9a530fdee1435c7fa9f37f2047e102f40686db1a976fd3dd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (144030517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0b9a7332a2f6425127c2a832e966c9da16a1b953a855625b72bbc69e136383`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:32:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 13:45:12 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 13:45:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 24 Apr 2024 13:45:13 GMT
ENV TELEGRAF_VERSION=1.28.5
# Wed, 24 Apr 2024 13:45:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 24 Apr 2024 13:45:20 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 24 Apr 2024 13:45:20 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Wed, 24 Apr 2024 13:45:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 13:45:21 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e100ddc6b415c632410507293430c0fe6bb4228ab320ed59548c6dc030b4e4a`  
		Last Modified: Wed, 24 Apr 2024 08:41:28 GMT  
		Size: 23.6 MB (23586795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935286a1f591251a12c663afdc2596adc4e8b91d91c60c7d53907023fed11a0`  
		Last Modified: Wed, 24 Apr 2024 13:46:02 GMT  
		Size: 19.1 MB (19077226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68421de5c53c46a30146ebc2684bda6aaf65e702e559619ca40243653b5623d8`  
		Last Modified: Wed, 24 Apr 2024 13:45:59 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58e667f2485042742589df6b5d154367ede643d1045ebbae560175210d0e12c`  
		Last Modified: Wed, 24 Apr 2024 13:46:05 GMT  
		Size: 51.8 MB (51750731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe0fc9e0da78a55a803b90c434772adf08fafa1227c8096a8349f033ad12b834`  
		Last Modified: Wed, 24 Apr 2024 13:46:00 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.28.5-alpine`

```console
$ docker pull telegraf@sha256:57bc33034b6d4d6a96f731b8265a2c9b3985311060ce359879b0fd6ae9b43c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:1.28.5-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:f7029c882a1e0d8dcba490bac1e95c52907200b5be69479a501eba9d9bd93475
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62934041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7687f8b8bb846071a28467f7e04ee14b36738636e4c07cac62275932bac3259`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:56:08 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 08:56:10 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 16 Mar 2024 08:56:10 GMT
ENV TELEGRAF_VERSION=1.28.5
# Sat, 16 Mar 2024 08:56:17 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 16 Mar 2024 08:56:17 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 16 Mar 2024 08:56:17 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 16 Mar 2024 08:56:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 08:56:17 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162ebdf1596ab6dcfd486bee21886e418f16f6c426a8dd266cba7da20b557281`  
		Last Modified: Sat, 16 Mar 2024 08:56:58 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdd04d97f3dab462dc59e41d85f02932280e01a7d7a2cd1d24c977e5ae0b583`  
		Last Modified: Sat, 16 Mar 2024 08:56:59 GMT  
		Size: 2.6 MB (2610463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc84cbb6d9e3d0bc47ba96808f7dad0ea7ae3dea5956e44a69ad86374660666`  
		Last Modified: Sat, 16 Mar 2024 08:57:07 GMT  
		Size: 56.9 MB (56914244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f389965f1bfc3e1b5beec1fe0af5e3abe25a32310c0f26c303f66e844988f98`  
		Last Modified: Sat, 16 Mar 2024 08:56:58 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.28.5-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:58b50c2433f9a957d62b40780760df86989c7d7fb6db583f29a82de80c84f609
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57629106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ebbf0803b5bb23e9014912e03226a830106c5da0014f838310c29d6c28e512`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:41:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 02:41:47 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 16 Mar 2024 02:41:47 GMT
ENV TELEGRAF_VERSION=1.28.5
# Sat, 16 Mar 2024 02:41:53 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 16 Mar 2024 02:41:54 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 16 Mar 2024 02:41:54 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 16 Mar 2024 02:41:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 02:41:55 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2675ee4ddf03252fa477bd14d6e59e0470e73d69c7fb12bade1d12e074715140`  
		Last Modified: Sat, 16 Mar 2024 02:42:34 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870e8831f6d198a84a383f159cec54a3ee90276d6772ca50a61c7cd967628656`  
		Last Modified: Sat, 16 Mar 2024 02:42:35 GMT  
		Size: 2.7 MB (2692939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed275664d335915c59116fc4dcb505bd5b0ccd59b112b85c7d0dbecb230b7bd8`  
		Last Modified: Sat, 16 Mar 2024 02:42:40 GMT  
		Size: 51.6 MB (51587851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca806e7a7334d09e576e9279db970934609cd4b9ad9828ebcf85b589837195e`  
		Last Modified: Sat, 16 Mar 2024 02:42:34 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.29`

```console
$ docker pull telegraf@sha256:3872666ed599cf044ef200f140f0bcad60035ad680acdcee5c03fdb155b438e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.29` - linux; amd64

```console
$ docker pull telegraf@sha256:6e4965c7046a6d1365942b076ae7fa8e098d1188d7e829b150ef3adf01321eab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155403454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ef0040442278b01826f95a32ed01cd78a4c124e35093239308366dd5384711`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:34 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
# Wed, 10 Apr 2024 01:50:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:24:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 17:16:34 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 17:16:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 17:16:49 GMT
ENV TELEGRAF_VERSION=1.29.5
# Wed, 10 Apr 2024 17:16:53 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 10 Apr 2024 17:16:54 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 10 Apr 2024 17:16:54 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Wed, 10 Apr 2024 17:16:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 17:16:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7247ea8d81e671d079d67f3a9909315ef4641b45db90d62a1b18e3430c1937d4`  
		Last Modified: Wed, 10 Apr 2024 05:34:49 GMT  
		Size: 24.0 MB (24046793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c65925cef157ec92ca4ac7ea2fee498997e6f04ceabcc6f5ba6ceec5ff79712`  
		Last Modified: Wed, 10 Apr 2024 17:17:26 GMT  
		Size: 19.2 MB (19151211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e46883b5de031b19b1f858d24ef5c262d06bb7b3105c84db483d710445599e8`  
		Last Modified: Wed, 10 Apr 2024 17:17:23 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc52e433276e1fb8b4fbff2fe0211fee3358e3e625d380d988746669ecf2cae`  
		Last Modified: Wed, 10 Apr 2024 17:17:52 GMT  
		Size: 62.6 MB (62642654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d085cd3e5daec279260f09e62a833c16c375756c513c340613876251c8a703`  
		Last Modified: Wed, 10 Apr 2024 17:17:42 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.29` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:d613fec4a4b3a8e616426955790c739bf5db7793ff65379083136a3f874706a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143048941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da02257cc86465ef15bf10027de0e8403b1a794c155205de740cf285c1a4f594`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 24 Apr 2024 04:06:51 GMT
ADD file:b6d26ef7cfc03fe202f7a5ac219566bc37f382ffadc9acdad685f2dd318cf0e4 in / 
# Wed, 24 Apr 2024 04:06:52 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:50:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 14:05:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 14:05:51 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 24 Apr 2024 14:06:05 GMT
ENV TELEGRAF_VERSION=1.29.5
# Wed, 24 Apr 2024 14:06:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 24 Apr 2024 14:06:16 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 24 Apr 2024 14:06:16 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Wed, 24 Apr 2024 14:06:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 14:06:16 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:80e84b3257949a283234599e3906626cfb4ff482d06fa4dc3eaf1dd36551dafa`  
		Last Modified: Wed, 24 Apr 2024 04:10:48 GMT  
		Size: 45.2 MB (45174994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52886721ea5a8a8bac2b197dccd42a74948b88bedcfe0fdf8b24e234c0a660d0`  
		Last Modified: Wed, 24 Apr 2024 05:02:39 GMT  
		Size: 22.0 MB (21953968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49ff3c62cfa8259ba641f429364c1c98fb99aaace66ea71c110c0f3f6a2069b`  
		Last Modified: Wed, 24 Apr 2024 14:06:47 GMT  
		Size: 17.9 MB (17932145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbf8d083657a1224c565a90b217288b841ff1f78db931977faaf6c32f8233ac`  
		Last Modified: Wed, 24 Apr 2024 14:06:42 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e854fdae6bef9d5ff1398b2fb4ebee666239698b323d2da4470dfcba8a8eedf`  
		Last Modified: Wed, 24 Apr 2024 14:07:15 GMT  
		Size: 58.0 MB (57985398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0791b57e9b2e9ceb9e9e58235b0502dcb936be0559ecd4d07f8fce70479d0165`  
		Last Modified: Wed, 24 Apr 2024 14:07:03 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.29` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:85ea0d17f506ecabbd6ce8b9eef392a5d113b76e3f75e2850d3d0a1135031569
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.3 MB (149261110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:506b4947b6df7a506c624ff7fa66952e6596f0b137b5270e0c1cd9a31dcd5b71`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:32:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 13:45:12 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 13:45:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 24 Apr 2024 13:45:27 GMT
ENV TELEGRAF_VERSION=1.29.5
# Wed, 24 Apr 2024 13:45:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 24 Apr 2024 13:45:34 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 24 Apr 2024 13:45:34 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Wed, 24 Apr 2024 13:45:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 13:45:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e100ddc6b415c632410507293430c0fe6bb4228ab320ed59548c6dc030b4e4a`  
		Last Modified: Wed, 24 Apr 2024 08:41:28 GMT  
		Size: 23.6 MB (23586795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935286a1f591251a12c663afdc2596adc4e8b91d91c60c7d53907023fed11a0`  
		Last Modified: Wed, 24 Apr 2024 13:46:02 GMT  
		Size: 19.1 MB (19077226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68421de5c53c46a30146ebc2684bda6aaf65e702e559619ca40243653b5623d8`  
		Last Modified: Wed, 24 Apr 2024 13:45:59 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca800b407f790b040ac819f2fa5048e27e9d65e2af8275d71d49991f7eb69c96`  
		Last Modified: Wed, 24 Apr 2024 13:46:20 GMT  
		Size: 57.0 MB (56981324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cc0a6c62dd1e355ca9d10503051ed01becf178938397731daced62ca423804`  
		Last Modified: Wed, 24 Apr 2024 13:46:14 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.29-alpine`

```console
$ docker pull telegraf@sha256:e7189e5fc22b61e1141016ef9e4e3577caada65c8a26544074259f30a1ad9d0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:1.29-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:823a2e316bd3af03d98183c4578af04a0ec9b2e06c98fea702f6de057eafc3fa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68477324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbfd48b205b097d2394b0f2fc0fbe817e35c206890692d30ae95bb45358cc50c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:56:08 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 08:56:10 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 16 Mar 2024 08:56:22 GMT
ENV TELEGRAF_VERSION=1.29.5
# Sat, 16 Mar 2024 08:56:31 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 16 Mar 2024 08:56:32 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 16 Mar 2024 08:56:32 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 16 Mar 2024 08:56:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 08:56:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162ebdf1596ab6dcfd486bee21886e418f16f6c426a8dd266cba7da20b557281`  
		Last Modified: Sat, 16 Mar 2024 08:56:58 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdd04d97f3dab462dc59e41d85f02932280e01a7d7a2cd1d24c977e5ae0b583`  
		Last Modified: Sat, 16 Mar 2024 08:56:59 GMT  
		Size: 2.6 MB (2610463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4512bc4fc4e3f7b669e009a477ad623af9023db4fcbd9ace2be72ab1d91936d3`  
		Last Modified: Sat, 16 Mar 2024 08:57:25 GMT  
		Size: 62.5 MB (62457526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576d31c8349e3d3dae1c2edf7078657d76c6e3c4a2faee5168f8a20c8c2bc0ab`  
		Last Modified: Sat, 16 Mar 2024 08:57:15 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.29-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:a7bed99c8e39b5eebaaa167953481466e7389b4c1b6c4f6774a55b840de5fbdc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62839803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7ba5175eb0179c5c2014027104e9e056df19ce22192b09c92cf96c4c9a96e4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:41:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 02:41:47 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 16 Mar 2024 02:41:58 GMT
ENV TELEGRAF_VERSION=1.29.5
# Sat, 16 Mar 2024 02:42:05 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 16 Mar 2024 02:42:06 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 16 Mar 2024 02:42:06 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 16 Mar 2024 02:42:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 02:42:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2675ee4ddf03252fa477bd14d6e59e0470e73d69c7fb12bade1d12e074715140`  
		Last Modified: Sat, 16 Mar 2024 02:42:34 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870e8831f6d198a84a383f159cec54a3ee90276d6772ca50a61c7cd967628656`  
		Last Modified: Sat, 16 Mar 2024 02:42:35 GMT  
		Size: 2.7 MB (2692939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1affe1933624c96f8732c646cd6e3ddf57d1202cb43246455d627df374eaf266`  
		Last Modified: Sat, 16 Mar 2024 02:42:55 GMT  
		Size: 56.8 MB (56798544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dceff9497b8bf1af89729eff827aa454ef369d6faa5772a8c3e296c790b11e6e`  
		Last Modified: Sat, 16 Mar 2024 02:42:48 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.29.5`

```console
$ docker pull telegraf@sha256:3872666ed599cf044ef200f140f0bcad60035ad680acdcee5c03fdb155b438e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.29.5` - linux; amd64

```console
$ docker pull telegraf@sha256:6e4965c7046a6d1365942b076ae7fa8e098d1188d7e829b150ef3adf01321eab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155403454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ef0040442278b01826f95a32ed01cd78a4c124e35093239308366dd5384711`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:34 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
# Wed, 10 Apr 2024 01:50:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:24:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 17:16:34 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 17:16:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 17:16:49 GMT
ENV TELEGRAF_VERSION=1.29.5
# Wed, 10 Apr 2024 17:16:53 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 10 Apr 2024 17:16:54 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 10 Apr 2024 17:16:54 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Wed, 10 Apr 2024 17:16:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 17:16:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7247ea8d81e671d079d67f3a9909315ef4641b45db90d62a1b18e3430c1937d4`  
		Last Modified: Wed, 10 Apr 2024 05:34:49 GMT  
		Size: 24.0 MB (24046793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c65925cef157ec92ca4ac7ea2fee498997e6f04ceabcc6f5ba6ceec5ff79712`  
		Last Modified: Wed, 10 Apr 2024 17:17:26 GMT  
		Size: 19.2 MB (19151211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e46883b5de031b19b1f858d24ef5c262d06bb7b3105c84db483d710445599e8`  
		Last Modified: Wed, 10 Apr 2024 17:17:23 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc52e433276e1fb8b4fbff2fe0211fee3358e3e625d380d988746669ecf2cae`  
		Last Modified: Wed, 10 Apr 2024 17:17:52 GMT  
		Size: 62.6 MB (62642654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d085cd3e5daec279260f09e62a833c16c375756c513c340613876251c8a703`  
		Last Modified: Wed, 10 Apr 2024 17:17:42 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.29.5` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:d613fec4a4b3a8e616426955790c739bf5db7793ff65379083136a3f874706a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143048941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da02257cc86465ef15bf10027de0e8403b1a794c155205de740cf285c1a4f594`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 24 Apr 2024 04:06:51 GMT
ADD file:b6d26ef7cfc03fe202f7a5ac219566bc37f382ffadc9acdad685f2dd318cf0e4 in / 
# Wed, 24 Apr 2024 04:06:52 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:50:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 14:05:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 14:05:51 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 24 Apr 2024 14:06:05 GMT
ENV TELEGRAF_VERSION=1.29.5
# Wed, 24 Apr 2024 14:06:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 24 Apr 2024 14:06:16 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 24 Apr 2024 14:06:16 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Wed, 24 Apr 2024 14:06:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 14:06:16 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:80e84b3257949a283234599e3906626cfb4ff482d06fa4dc3eaf1dd36551dafa`  
		Last Modified: Wed, 24 Apr 2024 04:10:48 GMT  
		Size: 45.2 MB (45174994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52886721ea5a8a8bac2b197dccd42a74948b88bedcfe0fdf8b24e234c0a660d0`  
		Last Modified: Wed, 24 Apr 2024 05:02:39 GMT  
		Size: 22.0 MB (21953968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49ff3c62cfa8259ba641f429364c1c98fb99aaace66ea71c110c0f3f6a2069b`  
		Last Modified: Wed, 24 Apr 2024 14:06:47 GMT  
		Size: 17.9 MB (17932145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbf8d083657a1224c565a90b217288b841ff1f78db931977faaf6c32f8233ac`  
		Last Modified: Wed, 24 Apr 2024 14:06:42 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e854fdae6bef9d5ff1398b2fb4ebee666239698b323d2da4470dfcba8a8eedf`  
		Last Modified: Wed, 24 Apr 2024 14:07:15 GMT  
		Size: 58.0 MB (57985398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0791b57e9b2e9ceb9e9e58235b0502dcb936be0559ecd4d07f8fce70479d0165`  
		Last Modified: Wed, 24 Apr 2024 14:07:03 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.29.5` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:85ea0d17f506ecabbd6ce8b9eef392a5d113b76e3f75e2850d3d0a1135031569
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.3 MB (149261110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:506b4947b6df7a506c624ff7fa66952e6596f0b137b5270e0c1cd9a31dcd5b71`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:32:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 13:45:12 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 13:45:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 24 Apr 2024 13:45:27 GMT
ENV TELEGRAF_VERSION=1.29.5
# Wed, 24 Apr 2024 13:45:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 24 Apr 2024 13:45:34 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 24 Apr 2024 13:45:34 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Wed, 24 Apr 2024 13:45:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 13:45:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e100ddc6b415c632410507293430c0fe6bb4228ab320ed59548c6dc030b4e4a`  
		Last Modified: Wed, 24 Apr 2024 08:41:28 GMT  
		Size: 23.6 MB (23586795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935286a1f591251a12c663afdc2596adc4e8b91d91c60c7d53907023fed11a0`  
		Last Modified: Wed, 24 Apr 2024 13:46:02 GMT  
		Size: 19.1 MB (19077226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68421de5c53c46a30146ebc2684bda6aaf65e702e559619ca40243653b5623d8`  
		Last Modified: Wed, 24 Apr 2024 13:45:59 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca800b407f790b040ac819f2fa5048e27e9d65e2af8275d71d49991f7eb69c96`  
		Last Modified: Wed, 24 Apr 2024 13:46:20 GMT  
		Size: 57.0 MB (56981324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cc0a6c62dd1e355ca9d10503051ed01becf178938397731daced62ca423804`  
		Last Modified: Wed, 24 Apr 2024 13:46:14 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.29.5-alpine`

```console
$ docker pull telegraf@sha256:e7189e5fc22b61e1141016ef9e4e3577caada65c8a26544074259f30a1ad9d0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:1.29.5-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:823a2e316bd3af03d98183c4578af04a0ec9b2e06c98fea702f6de057eafc3fa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68477324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbfd48b205b097d2394b0f2fc0fbe817e35c206890692d30ae95bb45358cc50c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:56:08 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 08:56:10 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 16 Mar 2024 08:56:22 GMT
ENV TELEGRAF_VERSION=1.29.5
# Sat, 16 Mar 2024 08:56:31 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 16 Mar 2024 08:56:32 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 16 Mar 2024 08:56:32 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 16 Mar 2024 08:56:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 08:56:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162ebdf1596ab6dcfd486bee21886e418f16f6c426a8dd266cba7da20b557281`  
		Last Modified: Sat, 16 Mar 2024 08:56:58 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdd04d97f3dab462dc59e41d85f02932280e01a7d7a2cd1d24c977e5ae0b583`  
		Last Modified: Sat, 16 Mar 2024 08:56:59 GMT  
		Size: 2.6 MB (2610463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4512bc4fc4e3f7b669e009a477ad623af9023db4fcbd9ace2be72ab1d91936d3`  
		Last Modified: Sat, 16 Mar 2024 08:57:25 GMT  
		Size: 62.5 MB (62457526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576d31c8349e3d3dae1c2edf7078657d76c6e3c4a2faee5168f8a20c8c2bc0ab`  
		Last Modified: Sat, 16 Mar 2024 08:57:15 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.29.5-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:a7bed99c8e39b5eebaaa167953481466e7389b4c1b6c4f6774a55b840de5fbdc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62839803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7ba5175eb0179c5c2014027104e9e056df19ce22192b09c92cf96c4c9a96e4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:41:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 02:41:47 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 16 Mar 2024 02:41:58 GMT
ENV TELEGRAF_VERSION=1.29.5
# Sat, 16 Mar 2024 02:42:05 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 16 Mar 2024 02:42:06 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 16 Mar 2024 02:42:06 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 16 Mar 2024 02:42:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 02:42:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2675ee4ddf03252fa477bd14d6e59e0470e73d69c7fb12bade1d12e074715140`  
		Last Modified: Sat, 16 Mar 2024 02:42:34 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870e8831f6d198a84a383f159cec54a3ee90276d6772ca50a61c7cd967628656`  
		Last Modified: Sat, 16 Mar 2024 02:42:35 GMT  
		Size: 2.7 MB (2692939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1affe1933624c96f8732c646cd6e3ddf57d1202cb43246455d627df374eaf266`  
		Last Modified: Sat, 16 Mar 2024 02:42:55 GMT  
		Size: 56.8 MB (56798544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dceff9497b8bf1af89729eff827aa454ef369d6faa5772a8c3e296c790b11e6e`  
		Last Modified: Sat, 16 Mar 2024 02:42:48 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.30`

```console
$ docker pull telegraf@sha256:75af50d15b462c1ad679efd831c98a7d1322cf7f94f34e0b7267f9b45973f4df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.30` - linux; amd64

```console
$ docker pull telegraf@sha256:7b4d3285c9263ddf956c181c072f7152aedd385b7b376600878e4f577bab19f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154783671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70d2f3a9dda678871a1d15135c50ad731e32de112d3a58a1635a537fc97c259`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:34 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
# Wed, 10 Apr 2024 01:50:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:24:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 17:16:34 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 17:16:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 22 Apr 2024 22:25:42 GMT
ENV TELEGRAF_VERSION=1.30.2
# Mon, 22 Apr 2024 22:25:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Mon, 22 Apr 2024 22:25:47 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 22 Apr 2024 22:25:47 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Mon, 22 Apr 2024 22:25:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 22:25:47 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7247ea8d81e671d079d67f3a9909315ef4641b45db90d62a1b18e3430c1937d4`  
		Last Modified: Wed, 10 Apr 2024 05:34:49 GMT  
		Size: 24.0 MB (24046793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c65925cef157ec92ca4ac7ea2fee498997e6f04ceabcc6f5ba6ceec5ff79712`  
		Last Modified: Wed, 10 Apr 2024 17:17:26 GMT  
		Size: 19.2 MB (19151211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e46883b5de031b19b1f858d24ef5c262d06bb7b3105c84db483d710445599e8`  
		Last Modified: Wed, 10 Apr 2024 17:17:23 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b08f004667eb3b18c3e49371bc700008325d69e2a9cc5b513852fd8f65439b5`  
		Last Modified: Mon, 22 Apr 2024 22:26:28 GMT  
		Size: 62.0 MB (62022871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7cebdcdd35756c5e60649efaf9c73404be1163c0aa6785b56575d3a91d5195`  
		Last Modified: Mon, 22 Apr 2024 22:26:19 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.30` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:8c5237515cb51fc5bf2bba17bafb21d35101d69cc311750d460fbf22981a6a32
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142475270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb44be8a4b00a22f71fd22110da989a49f7ef26b1f4cbafb0ae0281ccc768c6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 24 Apr 2024 04:06:51 GMT
ADD file:b6d26ef7cfc03fe202f7a5ac219566bc37f382ffadc9acdad685f2dd318cf0e4 in / 
# Wed, 24 Apr 2024 04:06:52 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:50:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 14:05:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 14:05:51 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 24 Apr 2024 14:06:20 GMT
ENV TELEGRAF_VERSION=1.30.2
# Wed, 24 Apr 2024 14:06:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 24 Apr 2024 14:06:29 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 24 Apr 2024 14:06:29 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Wed, 24 Apr 2024 14:06:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 14:06:30 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:80e84b3257949a283234599e3906626cfb4ff482d06fa4dc3eaf1dd36551dafa`  
		Last Modified: Wed, 24 Apr 2024 04:10:48 GMT  
		Size: 45.2 MB (45174994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52886721ea5a8a8bac2b197dccd42a74948b88bedcfe0fdf8b24e234c0a660d0`  
		Last Modified: Wed, 24 Apr 2024 05:02:39 GMT  
		Size: 22.0 MB (21953968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49ff3c62cfa8259ba641f429364c1c98fb99aaace66ea71c110c0f3f6a2069b`  
		Last Modified: Wed, 24 Apr 2024 14:06:47 GMT  
		Size: 17.9 MB (17932145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbf8d083657a1224c565a90b217288b841ff1f78db931977faaf6c32f8233ac`  
		Last Modified: Wed, 24 Apr 2024 14:06:42 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128efe4859364bc7e5609805398e7dedafefcbd75316d7dfb0bcb09212fa0430`  
		Last Modified: Wed, 24 Apr 2024 14:07:33 GMT  
		Size: 57.4 MB (57411726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68bf7594d0e12f0e1dd643d6d96bd53b36e7bfca8340cd1ecac6b069323c4a42`  
		Last Modified: Wed, 24 Apr 2024 14:07:23 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.30` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:25de4d9685c1049a17c469fc9d53b508d9e66493e02adde3b64292917fdc81a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148699434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d75c995de34e0505e291b68efc64748d8b098a81d5c7d4fc4ba42caaa979ecb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:32:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 13:45:12 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 13:45:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 24 Apr 2024 13:45:38 GMT
ENV TELEGRAF_VERSION=1.30.2
# Wed, 24 Apr 2024 13:45:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 24 Apr 2024 13:45:44 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 24 Apr 2024 13:45:44 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Wed, 24 Apr 2024 13:45:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 13:45:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e100ddc6b415c632410507293430c0fe6bb4228ab320ed59548c6dc030b4e4a`  
		Last Modified: Wed, 24 Apr 2024 08:41:28 GMT  
		Size: 23.6 MB (23586795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935286a1f591251a12c663afdc2596adc4e8b91d91c60c7d53907023fed11a0`  
		Last Modified: Wed, 24 Apr 2024 13:46:02 GMT  
		Size: 19.1 MB (19077226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68421de5c53c46a30146ebc2684bda6aaf65e702e559619ca40243653b5623d8`  
		Last Modified: Wed, 24 Apr 2024 13:45:59 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16de5edc7a15e62e63cfdc108c79c735c6271c7c11e51887f8a368b6e0a8284`  
		Last Modified: Wed, 24 Apr 2024 13:46:36 GMT  
		Size: 56.4 MB (56419647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2660869aa1b2eea6577b68dd5606d242030b2f2635a4797574b712958232b86d`  
		Last Modified: Wed, 24 Apr 2024 13:46:29 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.30-alpine`

```console
$ docker pull telegraf@sha256:f1d9699c33ae80520d21135a322d8a81f1c3e96a154b6d91464696908d62aeac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:1.30-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:8490fa1eb950dacb648491d1c09443830f8ada98945a22008d910a9ec53290be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67857443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:addf040d411128d3aabb776f2887cbe5277734118a808c0061360cc00d89360c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:56:08 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 08:56:10 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Mon, 22 Apr 2024 22:25:52 GMT
ENV TELEGRAF_VERSION=1.30.2
# Mon, 22 Apr 2024 22:25:58 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Mon, 22 Apr 2024 22:25:59 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 22 Apr 2024 22:25:59 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Mon, 22 Apr 2024 22:25:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 22:25:59 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162ebdf1596ab6dcfd486bee21886e418f16f6c426a8dd266cba7da20b557281`  
		Last Modified: Sat, 16 Mar 2024 08:56:58 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdd04d97f3dab462dc59e41d85f02932280e01a7d7a2cd1d24c977e5ae0b583`  
		Last Modified: Sat, 16 Mar 2024 08:56:59 GMT  
		Size: 2.6 MB (2610463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b90fe7e32605d44380672ade68a32b89f8ab574de47e6cdcb0129b5ca690eb3`  
		Last Modified: Mon, 22 Apr 2024 22:26:50 GMT  
		Size: 61.8 MB (61837645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276e354a4af75e82d665de77b7d4cf392770c0509f28a20b7ca2a10669c6d503`  
		Last Modified: Mon, 22 Apr 2024 22:26:40 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.30-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:06f6058b18ac09778316eaba8188c59098d79d3f4d7d8b8c982924647730c206
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62276441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0409a1d4b77454a6d2b29013e5a3a1fd367942702fd694a72dfa00c3d1a9bae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:41:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 02:41:47 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Mon, 22 Apr 2024 22:23:49 GMT
ENV TELEGRAF_VERSION=1.30.2
# Mon, 22 Apr 2024 22:23:57 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Mon, 22 Apr 2024 22:23:58 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 22 Apr 2024 22:23:59 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Mon, 22 Apr 2024 22:23:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 22:23:59 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2675ee4ddf03252fa477bd14d6e59e0470e73d69c7fb12bade1d12e074715140`  
		Last Modified: Sat, 16 Mar 2024 02:42:34 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870e8831f6d198a84a383f159cec54a3ee90276d6772ca50a61c7cd967628656`  
		Last Modified: Sat, 16 Mar 2024 02:42:35 GMT  
		Size: 2.7 MB (2692939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdee343d4a1c1c13ad21243ea6e3c803da3ecb861b1b1a1b994a0d9d797f4548`  
		Last Modified: Mon, 22 Apr 2024 22:24:44 GMT  
		Size: 56.2 MB (56235182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd79f1945a13f12fd7d0be61274f65ce1e3aedb7d13fcd54fbd56cc689e3ac4f`  
		Last Modified: Mon, 22 Apr 2024 22:24:37 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.30.2`

```console
$ docker pull telegraf@sha256:75af50d15b462c1ad679efd831c98a7d1322cf7f94f34e0b7267f9b45973f4df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.30.2` - linux; amd64

```console
$ docker pull telegraf@sha256:7b4d3285c9263ddf956c181c072f7152aedd385b7b376600878e4f577bab19f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154783671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70d2f3a9dda678871a1d15135c50ad731e32de112d3a58a1635a537fc97c259`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:34 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
# Wed, 10 Apr 2024 01:50:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:24:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 17:16:34 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 17:16:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 22 Apr 2024 22:25:42 GMT
ENV TELEGRAF_VERSION=1.30.2
# Mon, 22 Apr 2024 22:25:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Mon, 22 Apr 2024 22:25:47 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 22 Apr 2024 22:25:47 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Mon, 22 Apr 2024 22:25:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 22:25:47 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7247ea8d81e671d079d67f3a9909315ef4641b45db90d62a1b18e3430c1937d4`  
		Last Modified: Wed, 10 Apr 2024 05:34:49 GMT  
		Size: 24.0 MB (24046793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c65925cef157ec92ca4ac7ea2fee498997e6f04ceabcc6f5ba6ceec5ff79712`  
		Last Modified: Wed, 10 Apr 2024 17:17:26 GMT  
		Size: 19.2 MB (19151211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e46883b5de031b19b1f858d24ef5c262d06bb7b3105c84db483d710445599e8`  
		Last Modified: Wed, 10 Apr 2024 17:17:23 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b08f004667eb3b18c3e49371bc700008325d69e2a9cc5b513852fd8f65439b5`  
		Last Modified: Mon, 22 Apr 2024 22:26:28 GMT  
		Size: 62.0 MB (62022871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7cebdcdd35756c5e60649efaf9c73404be1163c0aa6785b56575d3a91d5195`  
		Last Modified: Mon, 22 Apr 2024 22:26:19 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.30.2` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:8c5237515cb51fc5bf2bba17bafb21d35101d69cc311750d460fbf22981a6a32
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142475270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb44be8a4b00a22f71fd22110da989a49f7ef26b1f4cbafb0ae0281ccc768c6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 24 Apr 2024 04:06:51 GMT
ADD file:b6d26ef7cfc03fe202f7a5ac219566bc37f382ffadc9acdad685f2dd318cf0e4 in / 
# Wed, 24 Apr 2024 04:06:52 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:50:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 14:05:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 14:05:51 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 24 Apr 2024 14:06:20 GMT
ENV TELEGRAF_VERSION=1.30.2
# Wed, 24 Apr 2024 14:06:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 24 Apr 2024 14:06:29 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 24 Apr 2024 14:06:29 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Wed, 24 Apr 2024 14:06:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 14:06:30 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:80e84b3257949a283234599e3906626cfb4ff482d06fa4dc3eaf1dd36551dafa`  
		Last Modified: Wed, 24 Apr 2024 04:10:48 GMT  
		Size: 45.2 MB (45174994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52886721ea5a8a8bac2b197dccd42a74948b88bedcfe0fdf8b24e234c0a660d0`  
		Last Modified: Wed, 24 Apr 2024 05:02:39 GMT  
		Size: 22.0 MB (21953968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49ff3c62cfa8259ba641f429364c1c98fb99aaace66ea71c110c0f3f6a2069b`  
		Last Modified: Wed, 24 Apr 2024 14:06:47 GMT  
		Size: 17.9 MB (17932145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbf8d083657a1224c565a90b217288b841ff1f78db931977faaf6c32f8233ac`  
		Last Modified: Wed, 24 Apr 2024 14:06:42 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128efe4859364bc7e5609805398e7dedafefcbd75316d7dfb0bcb09212fa0430`  
		Last Modified: Wed, 24 Apr 2024 14:07:33 GMT  
		Size: 57.4 MB (57411726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68bf7594d0e12f0e1dd643d6d96bd53b36e7bfca8340cd1ecac6b069323c4a42`  
		Last Modified: Wed, 24 Apr 2024 14:07:23 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.30.2` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:25de4d9685c1049a17c469fc9d53b508d9e66493e02adde3b64292917fdc81a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148699434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d75c995de34e0505e291b68efc64748d8b098a81d5c7d4fc4ba42caaa979ecb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:32:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 13:45:12 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 13:45:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 24 Apr 2024 13:45:38 GMT
ENV TELEGRAF_VERSION=1.30.2
# Wed, 24 Apr 2024 13:45:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 24 Apr 2024 13:45:44 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 24 Apr 2024 13:45:44 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Wed, 24 Apr 2024 13:45:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 13:45:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e100ddc6b415c632410507293430c0fe6bb4228ab320ed59548c6dc030b4e4a`  
		Last Modified: Wed, 24 Apr 2024 08:41:28 GMT  
		Size: 23.6 MB (23586795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935286a1f591251a12c663afdc2596adc4e8b91d91c60c7d53907023fed11a0`  
		Last Modified: Wed, 24 Apr 2024 13:46:02 GMT  
		Size: 19.1 MB (19077226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68421de5c53c46a30146ebc2684bda6aaf65e702e559619ca40243653b5623d8`  
		Last Modified: Wed, 24 Apr 2024 13:45:59 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16de5edc7a15e62e63cfdc108c79c735c6271c7c11e51887f8a368b6e0a8284`  
		Last Modified: Wed, 24 Apr 2024 13:46:36 GMT  
		Size: 56.4 MB (56419647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2660869aa1b2eea6577b68dd5606d242030b2f2635a4797574b712958232b86d`  
		Last Modified: Wed, 24 Apr 2024 13:46:29 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.30.2-alpine`

```console
$ docker pull telegraf@sha256:f1d9699c33ae80520d21135a322d8a81f1c3e96a154b6d91464696908d62aeac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:1.30.2-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:8490fa1eb950dacb648491d1c09443830f8ada98945a22008d910a9ec53290be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67857443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:addf040d411128d3aabb776f2887cbe5277734118a808c0061360cc00d89360c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:56:08 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 08:56:10 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Mon, 22 Apr 2024 22:25:52 GMT
ENV TELEGRAF_VERSION=1.30.2
# Mon, 22 Apr 2024 22:25:58 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Mon, 22 Apr 2024 22:25:59 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 22 Apr 2024 22:25:59 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Mon, 22 Apr 2024 22:25:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 22:25:59 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162ebdf1596ab6dcfd486bee21886e418f16f6c426a8dd266cba7da20b557281`  
		Last Modified: Sat, 16 Mar 2024 08:56:58 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdd04d97f3dab462dc59e41d85f02932280e01a7d7a2cd1d24c977e5ae0b583`  
		Last Modified: Sat, 16 Mar 2024 08:56:59 GMT  
		Size: 2.6 MB (2610463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b90fe7e32605d44380672ade68a32b89f8ab574de47e6cdcb0129b5ca690eb3`  
		Last Modified: Mon, 22 Apr 2024 22:26:50 GMT  
		Size: 61.8 MB (61837645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276e354a4af75e82d665de77b7d4cf392770c0509f28a20b7ca2a10669c6d503`  
		Last Modified: Mon, 22 Apr 2024 22:26:40 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.30.2-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:06f6058b18ac09778316eaba8188c59098d79d3f4d7d8b8c982924647730c206
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62276441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0409a1d4b77454a6d2b29013e5a3a1fd367942702fd694a72dfa00c3d1a9bae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:41:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 02:41:47 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Mon, 22 Apr 2024 22:23:49 GMT
ENV TELEGRAF_VERSION=1.30.2
# Mon, 22 Apr 2024 22:23:57 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Mon, 22 Apr 2024 22:23:58 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 22 Apr 2024 22:23:59 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Mon, 22 Apr 2024 22:23:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 22:23:59 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2675ee4ddf03252fa477bd14d6e59e0470e73d69c7fb12bade1d12e074715140`  
		Last Modified: Sat, 16 Mar 2024 02:42:34 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870e8831f6d198a84a383f159cec54a3ee90276d6772ca50a61c7cd967628656`  
		Last Modified: Sat, 16 Mar 2024 02:42:35 GMT  
		Size: 2.7 MB (2692939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdee343d4a1c1c13ad21243ea6e3c803da3ecb861b1b1a1b994a0d9d797f4548`  
		Last Modified: Mon, 22 Apr 2024 22:24:44 GMT  
		Size: 56.2 MB (56235182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd79f1945a13f12fd7d0be61274f65ce1e3aedb7d13fcd54fbd56cc689e3ac4f`  
		Last Modified: Mon, 22 Apr 2024 22:24:37 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:f1d9699c33ae80520d21135a322d8a81f1c3e96a154b6d91464696908d62aeac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:8490fa1eb950dacb648491d1c09443830f8ada98945a22008d910a9ec53290be
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67857443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:addf040d411128d3aabb776f2887cbe5277734118a808c0061360cc00d89360c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:56:08 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 08:56:10 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Mon, 22 Apr 2024 22:25:52 GMT
ENV TELEGRAF_VERSION=1.30.2
# Mon, 22 Apr 2024 22:25:58 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Mon, 22 Apr 2024 22:25:59 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 22 Apr 2024 22:25:59 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Mon, 22 Apr 2024 22:25:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 22:25:59 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162ebdf1596ab6dcfd486bee21886e418f16f6c426a8dd266cba7da20b557281`  
		Last Modified: Sat, 16 Mar 2024 08:56:58 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdd04d97f3dab462dc59e41d85f02932280e01a7d7a2cd1d24c977e5ae0b583`  
		Last Modified: Sat, 16 Mar 2024 08:56:59 GMT  
		Size: 2.6 MB (2610463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b90fe7e32605d44380672ade68a32b89f8ab574de47e6cdcb0129b5ca690eb3`  
		Last Modified: Mon, 22 Apr 2024 22:26:50 GMT  
		Size: 61.8 MB (61837645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:276e354a4af75e82d665de77b7d4cf392770c0509f28a20b7ca2a10669c6d503`  
		Last Modified: Mon, 22 Apr 2024 22:26:40 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:06f6058b18ac09778316eaba8188c59098d79d3f4d7d8b8c982924647730c206
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62276441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0409a1d4b77454a6d2b29013e5a3a1fd367942702fd694a72dfa00c3d1a9bae`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:41:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 02:41:47 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Mon, 22 Apr 2024 22:23:49 GMT
ENV TELEGRAF_VERSION=1.30.2
# Mon, 22 Apr 2024 22:23:57 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Mon, 22 Apr 2024 22:23:58 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 22 Apr 2024 22:23:59 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Mon, 22 Apr 2024 22:23:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 22:23:59 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2675ee4ddf03252fa477bd14d6e59e0470e73d69c7fb12bade1d12e074715140`  
		Last Modified: Sat, 16 Mar 2024 02:42:34 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870e8831f6d198a84a383f159cec54a3ee90276d6772ca50a61c7cd967628656`  
		Last Modified: Sat, 16 Mar 2024 02:42:35 GMT  
		Size: 2.7 MB (2692939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdee343d4a1c1c13ad21243ea6e3c803da3ecb861b1b1a1b994a0d9d797f4548`  
		Last Modified: Mon, 22 Apr 2024 22:24:44 GMT  
		Size: 56.2 MB (56235182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd79f1945a13f12fd7d0be61274f65ce1e3aedb7d13fcd54fbd56cc689e3ac4f`  
		Last Modified: Mon, 22 Apr 2024 22:24:37 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:75af50d15b462c1ad679efd831c98a7d1322cf7f94f34e0b7267f9b45973f4df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:7b4d3285c9263ddf956c181c072f7152aedd385b7b376600878e4f577bab19f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154783671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a70d2f3a9dda678871a1d15135c50ad731e32de112d3a58a1635a537fc97c259`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:34 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
# Wed, 10 Apr 2024 01:50:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:24:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 17:16:34 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 17:16:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 22 Apr 2024 22:25:42 GMT
ENV TELEGRAF_VERSION=1.30.2
# Mon, 22 Apr 2024 22:25:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Mon, 22 Apr 2024 22:25:47 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 22 Apr 2024 22:25:47 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Mon, 22 Apr 2024 22:25:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Apr 2024 22:25:47 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7247ea8d81e671d079d67f3a9909315ef4641b45db90d62a1b18e3430c1937d4`  
		Last Modified: Wed, 10 Apr 2024 05:34:49 GMT  
		Size: 24.0 MB (24046793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c65925cef157ec92ca4ac7ea2fee498997e6f04ceabcc6f5ba6ceec5ff79712`  
		Last Modified: Wed, 10 Apr 2024 17:17:26 GMT  
		Size: 19.2 MB (19151211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e46883b5de031b19b1f858d24ef5c262d06bb7b3105c84db483d710445599e8`  
		Last Modified: Wed, 10 Apr 2024 17:17:23 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b08f004667eb3b18c3e49371bc700008325d69e2a9cc5b513852fd8f65439b5`  
		Last Modified: Mon, 22 Apr 2024 22:26:28 GMT  
		Size: 62.0 MB (62022871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7cebdcdd35756c5e60649efaf9c73404be1163c0aa6785b56575d3a91d5195`  
		Last Modified: Mon, 22 Apr 2024 22:26:19 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:8c5237515cb51fc5bf2bba17bafb21d35101d69cc311750d460fbf22981a6a32
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142475270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddb44be8a4b00a22f71fd22110da989a49f7ef26b1f4cbafb0ae0281ccc768c6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 24 Apr 2024 04:06:51 GMT
ADD file:b6d26ef7cfc03fe202f7a5ac219566bc37f382ffadc9acdad685f2dd318cf0e4 in / 
# Wed, 24 Apr 2024 04:06:52 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:50:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 14:05:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 14:05:51 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 24 Apr 2024 14:06:20 GMT
ENV TELEGRAF_VERSION=1.30.2
# Wed, 24 Apr 2024 14:06:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 24 Apr 2024 14:06:29 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 24 Apr 2024 14:06:29 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Wed, 24 Apr 2024 14:06:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 14:06:30 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:80e84b3257949a283234599e3906626cfb4ff482d06fa4dc3eaf1dd36551dafa`  
		Last Modified: Wed, 24 Apr 2024 04:10:48 GMT  
		Size: 45.2 MB (45174994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52886721ea5a8a8bac2b197dccd42a74948b88bedcfe0fdf8b24e234c0a660d0`  
		Last Modified: Wed, 24 Apr 2024 05:02:39 GMT  
		Size: 22.0 MB (21953968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f49ff3c62cfa8259ba641f429364c1c98fb99aaace66ea71c110c0f3f6a2069b`  
		Last Modified: Wed, 24 Apr 2024 14:06:47 GMT  
		Size: 17.9 MB (17932145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbf8d083657a1224c565a90b217288b841ff1f78db931977faaf6c32f8233ac`  
		Last Modified: Wed, 24 Apr 2024 14:06:42 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128efe4859364bc7e5609805398e7dedafefcbd75316d7dfb0bcb09212fa0430`  
		Last Modified: Wed, 24 Apr 2024 14:07:33 GMT  
		Size: 57.4 MB (57411726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68bf7594d0e12f0e1dd643d6d96bd53b36e7bfca8340cd1ecac6b069323c4a42`  
		Last Modified: Wed, 24 Apr 2024 14:07:23 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:25de4d9685c1049a17c469fc9d53b508d9e66493e02adde3b64292917fdc81a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148699434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d75c995de34e0505e291b68efc64748d8b098a81d5c7d4fc4ba42caaa979ecb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:32:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 13:45:12 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 13:45:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 24 Apr 2024 13:45:38 GMT
ENV TELEGRAF_VERSION=1.30.2
# Wed, 24 Apr 2024 13:45:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 24 Apr 2024 13:45:44 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 24 Apr 2024 13:45:44 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Wed, 24 Apr 2024 13:45:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Apr 2024 13:45:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e100ddc6b415c632410507293430c0fe6bb4228ab320ed59548c6dc030b4e4a`  
		Last Modified: Wed, 24 Apr 2024 08:41:28 GMT  
		Size: 23.6 MB (23586795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935286a1f591251a12c663afdc2596adc4e8b91d91c60c7d53907023fed11a0`  
		Last Modified: Wed, 24 Apr 2024 13:46:02 GMT  
		Size: 19.1 MB (19077226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68421de5c53c46a30146ebc2684bda6aaf65e702e559619ca40243653b5623d8`  
		Last Modified: Wed, 24 Apr 2024 13:45:59 GMT  
		Size: 1.8 KB (1802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16de5edc7a15e62e63cfdc108c79c735c6271c7c11e51887f8a368b6e0a8284`  
		Last Modified: Wed, 24 Apr 2024 13:46:36 GMT  
		Size: 56.4 MB (56419647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2660869aa1b2eea6577b68dd5606d242030b2f2635a4797574b712958232b86d`  
		Last Modified: Wed, 24 Apr 2024 13:46:29 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
