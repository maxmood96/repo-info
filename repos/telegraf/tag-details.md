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
$ docker pull telegraf@sha256:12e9d4c85ab1ceacaf555f39414936d36414b3f6b7d9f3e2e376a5ea27fed672
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
$ docker pull telegraf@sha256:e652d9848e12aba5bd42e16e129a5f78bbb5065267f52d7e876231c7887e7e65
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137595798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b5d38200c543a3ca334a370a4749f0fd248505baad7a1028f88c48f58da92f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Apr 2024 00:57:54 GMT
ADD file:30e85746fe77290a5de7286ebb7e2484b39554122eadc92de3df4ef4d95de9ff in / 
# Wed, 10 Apr 2024 00:57:55 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:42:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 21:07:19 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 21:07:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 21:07:22 GMT
ENV TELEGRAF_VERSION=1.28.5
# Wed, 10 Apr 2024 21:07:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 10 Apr 2024 21:07:34 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 10 Apr 2024 21:07:34 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Wed, 10 Apr 2024 21:07:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 21:07:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:debd7c42d7ee74277f743dba14187c21ed8be6cf4f57abbaeb7b88c779282f09`  
		Last Modified: Wed, 10 Apr 2024 01:03:59 GMT  
		Size: 45.2 MB (45158610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1564e42498f84ce1d5bb6808049f9c674335b23f95ba63cf15c09549e3990e59`  
		Last Modified: Wed, 10 Apr 2024 06:59:53 GMT  
		Size: 22.0 MB (21950348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539a4933e1ca11975efc637d7e77bdc64694d79c67486aad5a374fef984db85e`  
		Last Modified: Wed, 10 Apr 2024 21:08:28 GMT  
		Size: 17.9 MB (17929696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0aa4c7886b8f03ebf9c562814862ec2279f0f4f50bb586e092cfc3e945d44e`  
		Last Modified: Wed, 10 Apr 2024 21:08:22 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62c4fd6654a8208a28983d5ede5a6ca28d7713ca9df6639947ffb9983f37ab19`  
		Last Modified: Wed, 10 Apr 2024 21:08:34 GMT  
		Size: 52.6 MB (52554708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b02330caff1872505e811cf3b808cbb5aeccda0b829efd6ec00aa5f199a8f0f`  
		Last Modified: Wed, 10 Apr 2024 21:08:22 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.28` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:84dc2a14788b61fd4215d8d8fabcea77d0b39e731475b52e17a5dcfd95615057
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (144007815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adad30f46c40ec7c21187ba8fe613b2eca5118374eff8590304610891498815f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:12 GMT
ADD file:d795219dc83a41b5bb4106e62eebd31ceef0aae1b81541156eae5fe98e89337c in / 
# Wed, 10 Apr 2024 00:40:13 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:22:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:35:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:35:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 13:35:37 GMT
ENV TELEGRAF_VERSION=1.28.5
# Wed, 10 Apr 2024 13:35:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 10 Apr 2024 13:35:43 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 10 Apr 2024 13:35:43 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Wed, 10 Apr 2024 13:35:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 13:35:43 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1e92f3a395ff98a929e797a3c392bb6d0f05531068d34b81d3cd41ed6ce82ca4`  
		Last Modified: Wed, 10 Apr 2024 00:43:42 GMT  
		Size: 49.6 MB (49596265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374850c6db1702573c7004d630027931be318b2d71cb28e890e2fcd0f0730712`  
		Last Modified: Wed, 10 Apr 2024 04:31:58 GMT  
		Size: 23.6 MB (23582868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c468dc23d21179efdf47892064269078a995fd2767b1e3d09765ba2418ebc69`  
		Last Modified: Wed, 10 Apr 2024 13:36:29 GMT  
		Size: 19.1 MB (19075482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6faae097dafbe140054f7608fe560fa16a117e207ea91b565b539d0c3a8970`  
		Last Modified: Wed, 10 Apr 2024 13:36:26 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e540708f1625d54bdb52afd3b9fea1afe8639fb489fff3691561ec1861411a`  
		Last Modified: Wed, 10 Apr 2024 13:36:32 GMT  
		Size: 51.8 MB (51750773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7599b21d41fb6732631fb213af052a2a1bdfb675778239a87f35a529e9d46a08`  
		Last Modified: Wed, 10 Apr 2024 13:36:26 GMT  
		Size: 624.0 B  
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
$ docker pull telegraf@sha256:12e9d4c85ab1ceacaf555f39414936d36414b3f6b7d9f3e2e376a5ea27fed672
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
$ docker pull telegraf@sha256:e652d9848e12aba5bd42e16e129a5f78bbb5065267f52d7e876231c7887e7e65
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137595798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b5d38200c543a3ca334a370a4749f0fd248505baad7a1028f88c48f58da92f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Apr 2024 00:57:54 GMT
ADD file:30e85746fe77290a5de7286ebb7e2484b39554122eadc92de3df4ef4d95de9ff in / 
# Wed, 10 Apr 2024 00:57:55 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:42:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 21:07:19 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 21:07:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 21:07:22 GMT
ENV TELEGRAF_VERSION=1.28.5
# Wed, 10 Apr 2024 21:07:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 10 Apr 2024 21:07:34 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 10 Apr 2024 21:07:34 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Wed, 10 Apr 2024 21:07:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 21:07:35 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:debd7c42d7ee74277f743dba14187c21ed8be6cf4f57abbaeb7b88c779282f09`  
		Last Modified: Wed, 10 Apr 2024 01:03:59 GMT  
		Size: 45.2 MB (45158610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1564e42498f84ce1d5bb6808049f9c674335b23f95ba63cf15c09549e3990e59`  
		Last Modified: Wed, 10 Apr 2024 06:59:53 GMT  
		Size: 22.0 MB (21950348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539a4933e1ca11975efc637d7e77bdc64694d79c67486aad5a374fef984db85e`  
		Last Modified: Wed, 10 Apr 2024 21:08:28 GMT  
		Size: 17.9 MB (17929696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0aa4c7886b8f03ebf9c562814862ec2279f0f4f50bb586e092cfc3e945d44e`  
		Last Modified: Wed, 10 Apr 2024 21:08:22 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62c4fd6654a8208a28983d5ede5a6ca28d7713ca9df6639947ffb9983f37ab19`  
		Last Modified: Wed, 10 Apr 2024 21:08:34 GMT  
		Size: 52.6 MB (52554708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b02330caff1872505e811cf3b808cbb5aeccda0b829efd6ec00aa5f199a8f0f`  
		Last Modified: Wed, 10 Apr 2024 21:08:22 GMT  
		Size: 623.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.28.5` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:84dc2a14788b61fd4215d8d8fabcea77d0b39e731475b52e17a5dcfd95615057
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (144007815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adad30f46c40ec7c21187ba8fe613b2eca5118374eff8590304610891498815f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:12 GMT
ADD file:d795219dc83a41b5bb4106e62eebd31ceef0aae1b81541156eae5fe98e89337c in / 
# Wed, 10 Apr 2024 00:40:13 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:22:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:35:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:35:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 13:35:37 GMT
ENV TELEGRAF_VERSION=1.28.5
# Wed, 10 Apr 2024 13:35:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 10 Apr 2024 13:35:43 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 10 Apr 2024 13:35:43 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Wed, 10 Apr 2024 13:35:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 13:35:43 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1e92f3a395ff98a929e797a3c392bb6d0f05531068d34b81d3cd41ed6ce82ca4`  
		Last Modified: Wed, 10 Apr 2024 00:43:42 GMT  
		Size: 49.6 MB (49596265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374850c6db1702573c7004d630027931be318b2d71cb28e890e2fcd0f0730712`  
		Last Modified: Wed, 10 Apr 2024 04:31:58 GMT  
		Size: 23.6 MB (23582868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c468dc23d21179efdf47892064269078a995fd2767b1e3d09765ba2418ebc69`  
		Last Modified: Wed, 10 Apr 2024 13:36:29 GMT  
		Size: 19.1 MB (19075482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6faae097dafbe140054f7608fe560fa16a117e207ea91b565b539d0c3a8970`  
		Last Modified: Wed, 10 Apr 2024 13:36:26 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e540708f1625d54bdb52afd3b9fea1afe8639fb489fff3691561ec1861411a`  
		Last Modified: Wed, 10 Apr 2024 13:36:32 GMT  
		Size: 51.8 MB (51750773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7599b21d41fb6732631fb213af052a2a1bdfb675778239a87f35a529e9d46a08`  
		Last Modified: Wed, 10 Apr 2024 13:36:26 GMT  
		Size: 624.0 B  
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
$ docker pull telegraf@sha256:3932b00fa4ab52c4fe976b8dceb02c96a4a736c328bebbfc25fbbeee170260c1
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
$ docker pull telegraf@sha256:dc2f371884613576b3432608eef8a2775c9ea4dfac9461d66e25d86fed58c21a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143026555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5598d7873bb0826da0f080dc6220607f66f126d6fd0c17669ab9fa4a67a54369`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Apr 2024 00:57:54 GMT
ADD file:30e85746fe77290a5de7286ebb7e2484b39554122eadc92de3df4ef4d95de9ff in / 
# Wed, 10 Apr 2024 00:57:55 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:42:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 21:07:19 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 21:07:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 21:07:38 GMT
ENV TELEGRAF_VERSION=1.29.5
# Wed, 10 Apr 2024 21:07:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 10 Apr 2024 21:07:50 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 10 Apr 2024 21:07:50 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Wed, 10 Apr 2024 21:07:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 21:07:51 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:debd7c42d7ee74277f743dba14187c21ed8be6cf4f57abbaeb7b88c779282f09`  
		Last Modified: Wed, 10 Apr 2024 01:03:59 GMT  
		Size: 45.2 MB (45158610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1564e42498f84ce1d5bb6808049f9c674335b23f95ba63cf15c09549e3990e59`  
		Last Modified: Wed, 10 Apr 2024 06:59:53 GMT  
		Size: 22.0 MB (21950348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539a4933e1ca11975efc637d7e77bdc64694d79c67486aad5a374fef984db85e`  
		Last Modified: Wed, 10 Apr 2024 21:08:28 GMT  
		Size: 17.9 MB (17929696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0aa4c7886b8f03ebf9c562814862ec2279f0f4f50bb586e092cfc3e945d44e`  
		Last Modified: Wed, 10 Apr 2024 21:08:22 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62c796fd0bd5ae49c83041b4a87023ef00a19634f6542b0a76495f10fb3d0e1`  
		Last Modified: Wed, 10 Apr 2024 21:08:55 GMT  
		Size: 58.0 MB (57985464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2019da979726c481978e4862e39b5ab5836def4820bea6dbb514235d28e176c9`  
		Last Modified: Wed, 10 Apr 2024 21:08:44 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.29` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:06406cff362dff2b89494ec0b82d0e6f06aadafc3ff926b14a5112d3e722e2bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149238359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d4b5d2f38ad4d36d382c9bb74b25b6cf6ab3117c8cd1d092cc6ccde6ea6a57d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:12 GMT
ADD file:d795219dc83a41b5bb4106e62eebd31ceef0aae1b81541156eae5fe98e89337c in / 
# Wed, 10 Apr 2024 00:40:13 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:22:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:35:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:35:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 13:35:47 GMT
ENV TELEGRAF_VERSION=1.29.5
# Wed, 10 Apr 2024 13:35:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 10 Apr 2024 13:35:55 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 10 Apr 2024 13:35:55 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Wed, 10 Apr 2024 13:35:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 13:35:55 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1e92f3a395ff98a929e797a3c392bb6d0f05531068d34b81d3cd41ed6ce82ca4`  
		Last Modified: Wed, 10 Apr 2024 00:43:42 GMT  
		Size: 49.6 MB (49596265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374850c6db1702573c7004d630027931be318b2d71cb28e890e2fcd0f0730712`  
		Last Modified: Wed, 10 Apr 2024 04:31:58 GMT  
		Size: 23.6 MB (23582868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c468dc23d21179efdf47892064269078a995fd2767b1e3d09765ba2418ebc69`  
		Last Modified: Wed, 10 Apr 2024 13:36:29 GMT  
		Size: 19.1 MB (19075482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6faae097dafbe140054f7608fe560fa16a117e207ea91b565b539d0c3a8970`  
		Last Modified: Wed, 10 Apr 2024 13:36:26 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e8a5e5e4a51cf9eeb69e9d9e610405d98ec63c3df062344f651b95aeadc30a`  
		Last Modified: Wed, 10 Apr 2024 13:36:49 GMT  
		Size: 57.0 MB (56981316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb51201e19650edfd9782db7e30a12084b6bafe5d3879d45cb2b9f7beed60770`  
		Last Modified: Wed, 10 Apr 2024 13:36:41 GMT  
		Size: 625.0 B  
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
$ docker pull telegraf@sha256:3932b00fa4ab52c4fe976b8dceb02c96a4a736c328bebbfc25fbbeee170260c1
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
$ docker pull telegraf@sha256:dc2f371884613576b3432608eef8a2775c9ea4dfac9461d66e25d86fed58c21a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143026555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5598d7873bb0826da0f080dc6220607f66f126d6fd0c17669ab9fa4a67a54369`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Apr 2024 00:57:54 GMT
ADD file:30e85746fe77290a5de7286ebb7e2484b39554122eadc92de3df4ef4d95de9ff in / 
# Wed, 10 Apr 2024 00:57:55 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:42:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 21:07:19 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 21:07:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 21:07:38 GMT
ENV TELEGRAF_VERSION=1.29.5
# Wed, 10 Apr 2024 21:07:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 10 Apr 2024 21:07:50 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 10 Apr 2024 21:07:50 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Wed, 10 Apr 2024 21:07:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 21:07:51 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:debd7c42d7ee74277f743dba14187c21ed8be6cf4f57abbaeb7b88c779282f09`  
		Last Modified: Wed, 10 Apr 2024 01:03:59 GMT  
		Size: 45.2 MB (45158610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1564e42498f84ce1d5bb6808049f9c674335b23f95ba63cf15c09549e3990e59`  
		Last Modified: Wed, 10 Apr 2024 06:59:53 GMT  
		Size: 22.0 MB (21950348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539a4933e1ca11975efc637d7e77bdc64694d79c67486aad5a374fef984db85e`  
		Last Modified: Wed, 10 Apr 2024 21:08:28 GMT  
		Size: 17.9 MB (17929696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0aa4c7886b8f03ebf9c562814862ec2279f0f4f50bb586e092cfc3e945d44e`  
		Last Modified: Wed, 10 Apr 2024 21:08:22 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62c796fd0bd5ae49c83041b4a87023ef00a19634f6542b0a76495f10fb3d0e1`  
		Last Modified: Wed, 10 Apr 2024 21:08:55 GMT  
		Size: 58.0 MB (57985464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2019da979726c481978e4862e39b5ab5836def4820bea6dbb514235d28e176c9`  
		Last Modified: Wed, 10 Apr 2024 21:08:44 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.29.5` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:06406cff362dff2b89494ec0b82d0e6f06aadafc3ff926b14a5112d3e722e2bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149238359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d4b5d2f38ad4d36d382c9bb74b25b6cf6ab3117c8cd1d092cc6ccde6ea6a57d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:12 GMT
ADD file:d795219dc83a41b5bb4106e62eebd31ceef0aae1b81541156eae5fe98e89337c in / 
# Wed, 10 Apr 2024 00:40:13 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:22:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:35:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:35:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 13:35:47 GMT
ENV TELEGRAF_VERSION=1.29.5
# Wed, 10 Apr 2024 13:35:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 10 Apr 2024 13:35:55 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 10 Apr 2024 13:35:55 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Wed, 10 Apr 2024 13:35:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 13:35:55 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1e92f3a395ff98a929e797a3c392bb6d0f05531068d34b81d3cd41ed6ce82ca4`  
		Last Modified: Wed, 10 Apr 2024 00:43:42 GMT  
		Size: 49.6 MB (49596265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374850c6db1702573c7004d630027931be318b2d71cb28e890e2fcd0f0730712`  
		Last Modified: Wed, 10 Apr 2024 04:31:58 GMT  
		Size: 23.6 MB (23582868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c468dc23d21179efdf47892064269078a995fd2767b1e3d09765ba2418ebc69`  
		Last Modified: Wed, 10 Apr 2024 13:36:29 GMT  
		Size: 19.1 MB (19075482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6faae097dafbe140054f7608fe560fa16a117e207ea91b565b539d0c3a8970`  
		Last Modified: Wed, 10 Apr 2024 13:36:26 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e8a5e5e4a51cf9eeb69e9d9e610405d98ec63c3df062344f651b95aeadc30a`  
		Last Modified: Wed, 10 Apr 2024 13:36:49 GMT  
		Size: 57.0 MB (56981316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb51201e19650edfd9782db7e30a12084b6bafe5d3879d45cb2b9f7beed60770`  
		Last Modified: Wed, 10 Apr 2024 13:36:41 GMT  
		Size: 625.0 B  
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
$ docker pull telegraf@sha256:e6dc07e758f8da7ec13305b2e0685a55e184b3fcc3883de62eceaf54a8fe1d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.30` - linux; amd64

```console
$ docker pull telegraf@sha256:149885403b5cf12e72e180853fdaec8e7ee4a660ad61111360842baa423db3ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154545849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e41758d8c2a3f29893e841125408c018c1263987f72faba27dc49368f980ce62`
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
# Wed, 10 Apr 2024 17:17:00 GMT
ENV TELEGRAF_VERSION=1.30.1
# Wed, 10 Apr 2024 17:17:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 10 Apr 2024 17:17:05 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 10 Apr 2024 17:17:05 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Wed, 10 Apr 2024 17:17:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 17:17:06 GMT
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
	-	`sha256:7edb069f29e362dea75c5d6e16d19b6d4bcfe4bd4f67135ea4bfbd3dfc5f1ff4`  
		Last Modified: Wed, 10 Apr 2024 17:18:11 GMT  
		Size: 61.8 MB (61785046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb5c87d050ba4069127428f51040385e84551d00b980e7d4d369008c43a9239c`  
		Last Modified: Wed, 10 Apr 2024 17:18:01 GMT  
		Size: 625.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.30` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:d18195976e943eda8266e7af45986119a0e6cbf1b878630344dd181dc4faa374
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142216864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7066bad7d954ccf1294ae9b40a862e1320d16392c2ff679a262a3ea1eb0417a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Apr 2024 00:57:54 GMT
ADD file:30e85746fe77290a5de7286ebb7e2484b39554122eadc92de3df4ef4d95de9ff in / 
# Wed, 10 Apr 2024 00:57:55 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:42:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 21:07:19 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 21:07:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 21:07:55 GMT
ENV TELEGRAF_VERSION=1.30.1
# Wed, 10 Apr 2024 21:08:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 10 Apr 2024 21:08:07 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 10 Apr 2024 21:08:08 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Wed, 10 Apr 2024 21:08:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 21:08:08 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:debd7c42d7ee74277f743dba14187c21ed8be6cf4f57abbaeb7b88c779282f09`  
		Last Modified: Wed, 10 Apr 2024 01:03:59 GMT  
		Size: 45.2 MB (45158610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1564e42498f84ce1d5bb6808049f9c674335b23f95ba63cf15c09549e3990e59`  
		Last Modified: Wed, 10 Apr 2024 06:59:53 GMT  
		Size: 22.0 MB (21950348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539a4933e1ca11975efc637d7e77bdc64694d79c67486aad5a374fef984db85e`  
		Last Modified: Wed, 10 Apr 2024 21:08:28 GMT  
		Size: 17.9 MB (17929696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0aa4c7886b8f03ebf9c562814862ec2279f0f4f50bb586e092cfc3e945d44e`  
		Last Modified: Wed, 10 Apr 2024 21:08:22 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1914c5df6e6614113daeee646f5ff8451a61f846a04e586670675dd72da2d36`  
		Last Modified: Wed, 10 Apr 2024 21:09:15 GMT  
		Size: 57.2 MB (57175773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0718046846941d7b2d4bc072c25f5a0337475bc1aa2d8036f3824a307404f6c0`  
		Last Modified: Wed, 10 Apr 2024 21:09:04 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.30` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:5a7d16833e66b6ec3f6d412736c488480c1afb6d9dee2363cd2aa31ffb3211b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148425917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97190f03ac08c391bb1f24baf7ccaf2034b5687cee24f4340a454027402ef132`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:12 GMT
ADD file:d795219dc83a41b5bb4106e62eebd31ceef0aae1b81541156eae5fe98e89337c in / 
# Wed, 10 Apr 2024 00:40:13 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:22:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:35:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:35:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 13:36:00 GMT
ENV TELEGRAF_VERSION=1.30.1
# Wed, 10 Apr 2024 13:36:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 10 Apr 2024 13:36:11 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 10 Apr 2024 13:36:11 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Wed, 10 Apr 2024 13:36:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 13:36:11 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1e92f3a395ff98a929e797a3c392bb6d0f05531068d34b81d3cd41ed6ce82ca4`  
		Last Modified: Wed, 10 Apr 2024 00:43:42 GMT  
		Size: 49.6 MB (49596265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374850c6db1702573c7004d630027931be318b2d71cb28e890e2fcd0f0730712`  
		Last Modified: Wed, 10 Apr 2024 04:31:58 GMT  
		Size: 23.6 MB (23582868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c468dc23d21179efdf47892064269078a995fd2767b1e3d09765ba2418ebc69`  
		Last Modified: Wed, 10 Apr 2024 13:36:29 GMT  
		Size: 19.1 MB (19075482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6faae097dafbe140054f7608fe560fa16a117e207ea91b565b539d0c3a8970`  
		Last Modified: Wed, 10 Apr 2024 13:36:26 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ca9b1c858780050401d58dd3cc45b9218ba6fc698f816d9b04f89b1df7d33f`  
		Last Modified: Wed, 10 Apr 2024 13:37:06 GMT  
		Size: 56.2 MB (56168877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c08e1d6e592d71a03495da302abfe9233121e1e40e1fa10d8e374b4afb21ecc`  
		Last Modified: Wed, 10 Apr 2024 13:36:58 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.30-alpine`

```console
$ docker pull telegraf@sha256:2e8da2041a8b3163d6039862aaeacf05420e9cb3dd4d334e96c7dd9971ae85cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:1.30-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:4e1101d6718d7e99d1ceddba0687186a4e76a30a097dbf34e4afda07a99c352a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67628051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e383f3e32d78ad2f6812dd3c8399b2d9e0c757b331b6d13749e5d6e246c916`
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
# Mon, 01 Apr 2024 19:52:47 GMT
ENV TELEGRAF_VERSION=1.30.1
# Mon, 01 Apr 2024 19:52:53 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Mon, 01 Apr 2024 19:52:54 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 01 Apr 2024 19:52:54 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Mon, 01 Apr 2024 19:52:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Apr 2024 19:52:54 GMT
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
	-	`sha256:9a7ef348089694c64746be53352084f76ff2a027e870e9e457021132b8f1dab2`  
		Last Modified: Mon, 01 Apr 2024 19:53:42 GMT  
		Size: 61.6 MB (61608255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35baddb4f9c16e6b2d3ee2828cd3f4c2fa8825edfe4e8236547fc43be03bb27`  
		Last Modified: Mon, 01 Apr 2024 19:53:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.30-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:3395f3b188cccef3c71bba84acac85db53a0c825ef601fce2e91dc63336de281
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62022034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d22374b3bcb08a9cfcd3edd4ffbb5f8d9cdace2870f0927f632c363681e24f05`
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
# Mon, 01 Apr 2024 20:17:30 GMT
ENV TELEGRAF_VERSION=1.30.1
# Mon, 01 Apr 2024 20:17:38 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Mon, 01 Apr 2024 20:17:40 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 01 Apr 2024 20:17:40 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Mon, 01 Apr 2024 20:17:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Apr 2024 20:17:40 GMT
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
	-	`sha256:0752fdc06623ef51aa94016d2b9d40e9cbdfda254fc20f531b54ea89eec318b5`  
		Last Modified: Mon, 01 Apr 2024 20:18:22 GMT  
		Size: 56.0 MB (55980774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b481c2fc94ecef71df2522db417d2f34aeac69a34cbcdabed7d6087de34eae4`  
		Last Modified: Mon, 01 Apr 2024 20:18:14 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.30.2`

**does not exist** (yet?)

## `telegraf:1.30.2-alpine`

**does not exist** (yet?)

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:2e8da2041a8b3163d6039862aaeacf05420e9cb3dd4d334e96c7dd9971ae85cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:4e1101d6718d7e99d1ceddba0687186a4e76a30a097dbf34e4afda07a99c352a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67628051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e383f3e32d78ad2f6812dd3c8399b2d9e0c757b331b6d13749e5d6e246c916`
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
# Mon, 01 Apr 2024 19:52:47 GMT
ENV TELEGRAF_VERSION=1.30.1
# Mon, 01 Apr 2024 19:52:53 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Mon, 01 Apr 2024 19:52:54 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 01 Apr 2024 19:52:54 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Mon, 01 Apr 2024 19:52:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Apr 2024 19:52:54 GMT
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
	-	`sha256:9a7ef348089694c64746be53352084f76ff2a027e870e9e457021132b8f1dab2`  
		Last Modified: Mon, 01 Apr 2024 19:53:42 GMT  
		Size: 61.6 MB (61608255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35baddb4f9c16e6b2d3ee2828cd3f4c2fa8825edfe4e8236547fc43be03bb27`  
		Last Modified: Mon, 01 Apr 2024 19:53:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:3395f3b188cccef3c71bba84acac85db53a0c825ef601fce2e91dc63336de281
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62022034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d22374b3bcb08a9cfcd3edd4ffbb5f8d9cdace2870f0927f632c363681e24f05`
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
# Mon, 01 Apr 2024 20:17:30 GMT
ENV TELEGRAF_VERSION=1.30.1
# Mon, 01 Apr 2024 20:17:38 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Mon, 01 Apr 2024 20:17:40 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 01 Apr 2024 20:17:40 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Mon, 01 Apr 2024 20:17:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Apr 2024 20:17:40 GMT
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
	-	`sha256:0752fdc06623ef51aa94016d2b9d40e9cbdfda254fc20f531b54ea89eec318b5`  
		Last Modified: Mon, 01 Apr 2024 20:18:22 GMT  
		Size: 56.0 MB (55980774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b481c2fc94ecef71df2522db417d2f34aeac69a34cbcdabed7d6087de34eae4`  
		Last Modified: Mon, 01 Apr 2024 20:18:14 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:e6dc07e758f8da7ec13305b2e0685a55e184b3fcc3883de62eceaf54a8fe1d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:149885403b5cf12e72e180853fdaec8e7ee4a660ad61111360842baa423db3ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154545849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e41758d8c2a3f29893e841125408c018c1263987f72faba27dc49368f980ce62`
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
# Wed, 10 Apr 2024 17:17:00 GMT
ENV TELEGRAF_VERSION=1.30.1
# Wed, 10 Apr 2024 17:17:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 10 Apr 2024 17:17:05 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 10 Apr 2024 17:17:05 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Wed, 10 Apr 2024 17:17:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 17:17:06 GMT
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
	-	`sha256:7edb069f29e362dea75c5d6e16d19b6d4bcfe4bd4f67135ea4bfbd3dfc5f1ff4`  
		Last Modified: Wed, 10 Apr 2024 17:18:11 GMT  
		Size: 61.8 MB (61785046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb5c87d050ba4069127428f51040385e84551d00b980e7d4d369008c43a9239c`  
		Last Modified: Wed, 10 Apr 2024 17:18:01 GMT  
		Size: 625.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:d18195976e943eda8266e7af45986119a0e6cbf1b878630344dd181dc4faa374
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142216864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7066bad7d954ccf1294ae9b40a862e1320d16392c2ff679a262a3ea1eb0417a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Apr 2024 00:57:54 GMT
ADD file:30e85746fe77290a5de7286ebb7e2484b39554122eadc92de3df4ef4d95de9ff in / 
# Wed, 10 Apr 2024 00:57:55 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:42:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 21:07:19 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 21:07:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 21:07:55 GMT
ENV TELEGRAF_VERSION=1.30.1
# Wed, 10 Apr 2024 21:08:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 10 Apr 2024 21:08:07 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 10 Apr 2024 21:08:08 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Wed, 10 Apr 2024 21:08:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 21:08:08 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:debd7c42d7ee74277f743dba14187c21ed8be6cf4f57abbaeb7b88c779282f09`  
		Last Modified: Wed, 10 Apr 2024 01:03:59 GMT  
		Size: 45.2 MB (45158610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1564e42498f84ce1d5bb6808049f9c674335b23f95ba63cf15c09549e3990e59`  
		Last Modified: Wed, 10 Apr 2024 06:59:53 GMT  
		Size: 22.0 MB (21950348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539a4933e1ca11975efc637d7e77bdc64694d79c67486aad5a374fef984db85e`  
		Last Modified: Wed, 10 Apr 2024 21:08:28 GMT  
		Size: 17.9 MB (17929696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0aa4c7886b8f03ebf9c562814862ec2279f0f4f50bb586e092cfc3e945d44e`  
		Last Modified: Wed, 10 Apr 2024 21:08:22 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1914c5df6e6614113daeee646f5ff8451a61f846a04e586670675dd72da2d36`  
		Last Modified: Wed, 10 Apr 2024 21:09:15 GMT  
		Size: 57.2 MB (57175773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0718046846941d7b2d4bc072c25f5a0337475bc1aa2d8036f3824a307404f6c0`  
		Last Modified: Wed, 10 Apr 2024 21:09:04 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:5a7d16833e66b6ec3f6d412736c488480c1afb6d9dee2363cd2aa31ffb3211b0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148425917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97190f03ac08c391bb1f24baf7ccaf2034b5687cee24f4340a454027402ef132`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:12 GMT
ADD file:d795219dc83a41b5bb4106e62eebd31ceef0aae1b81541156eae5fe98e89337c in / 
# Wed, 10 Apr 2024 00:40:13 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:22:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:35:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 13:35:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 10 Apr 2024 13:36:00 GMT
ENV TELEGRAF_VERSION=1.30.1
# Wed, 10 Apr 2024 13:36:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 10 Apr 2024 13:36:11 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 10 Apr 2024 13:36:11 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Wed, 10 Apr 2024 13:36:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Apr 2024 13:36:11 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:1e92f3a395ff98a929e797a3c392bb6d0f05531068d34b81d3cd41ed6ce82ca4`  
		Last Modified: Wed, 10 Apr 2024 00:43:42 GMT  
		Size: 49.6 MB (49596265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374850c6db1702573c7004d630027931be318b2d71cb28e890e2fcd0f0730712`  
		Last Modified: Wed, 10 Apr 2024 04:31:58 GMT  
		Size: 23.6 MB (23582868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c468dc23d21179efdf47892064269078a995fd2767b1e3d09765ba2418ebc69`  
		Last Modified: Wed, 10 Apr 2024 13:36:29 GMT  
		Size: 19.1 MB (19075482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf6faae097dafbe140054f7608fe560fa16a117e207ea91b565b539d0c3a8970`  
		Last Modified: Wed, 10 Apr 2024 13:36:26 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ca9b1c858780050401d58dd3cc45b9218ba6fc698f816d9b04f89b1df7d33f`  
		Last Modified: Wed, 10 Apr 2024 13:37:06 GMT  
		Size: 56.2 MB (56168877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c08e1d6e592d71a03495da302abfe9233121e1e40e1fa10d8e374b4afb21ecc`  
		Last Modified: Wed, 10 Apr 2024 13:36:58 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
