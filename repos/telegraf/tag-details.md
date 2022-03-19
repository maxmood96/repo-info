<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.19`](#telegraf119)
-	[`telegraf:1.19-alpine`](#telegraf119-alpine)
-	[`telegraf:1.19.3`](#telegraf1193)
-	[`telegraf:1.19.3-alpine`](#telegraf1193-alpine)
-	[`telegraf:1.20`](#telegraf120)
-	[`telegraf:1.20-alpine`](#telegraf120-alpine)
-	[`telegraf:1.20.4`](#telegraf1204)
-	[`telegraf:1.20.4-alpine`](#telegraf1204-alpine)
-	[`telegraf:1.21`](#telegraf121)
-	[`telegraf:1.21-alpine`](#telegraf121-alpine)
-	[`telegraf:1.21.4`](#telegraf1214)
-	[`telegraf:1.21.4-alpine`](#telegraf1214-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.19`

```console
$ docker pull telegraf@sha256:e3b4d450a136777e0bdd1f31b7eec5bc30cef34b01866b77a3c111383173ce6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.19` - linux; amd64

```console
$ docker pull telegraf@sha256:0ae72c62868b76d4841883e64325ffa3bf449347af187458db2ba5237635e6bc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123887524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06c4e5423cc4ef40c175979c458b0c9988a81c546121dc5fb47e9a7e4ddd7d5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:15 GMT
ADD file:9c4db2a9644ee3029a8e9cca58350efef660c3167e59b91f2bee9c303e592664 in / 
# Tue, 01 Mar 2022 02:13:15 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 06:25:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:26:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 02 Mar 2022 19:10:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 19:10:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 02 Mar 2022 19:10:40 GMT
ENV TELEGRAF_VERSION=1.19.3
# Wed, 02 Mar 2022 19:10:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 02 Mar 2022 19:10:44 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 02 Mar 2022 19:10:44 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 02 Mar 2022 19:10:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Mar 2022 19:10:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e4d61adff2077d048c6372d73c41b0bd68f525ad41f5530af05098a876683055`  
		Last Modified: Tue, 01 Mar 2022 02:18:55 GMT  
		Size: 54.9 MB (54917063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff1945c672b08a1791df62afaaf8aff14d3047155365f9c3646902937f7ffe6`  
		Last Modified: Tue, 01 Mar 2022 06:36:13 GMT  
		Size: 5.2 MB (5153034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5b10aec998344606441aec43a335ab6326f32aae331aab27da16a6bb4ec2be`  
		Last Modified: Tue, 01 Mar 2022 06:36:14 GMT  
		Size: 10.9 MB (10871885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7914280ffd1a89468d7300475f199f63daf36d7d310ca3e2f8a21424b6992e29`  
		Last Modified: Wed, 02 Mar 2022 19:11:29 GMT  
		Size: 18.8 MB (18760097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053949c9b19fa7512f69b5dc25fb96a03488191d90009ce09da1d77a5268b915`  
		Last Modified: Wed, 02 Mar 2022 19:11:25 GMT  
		Size: 2.9 KB (2905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc6da8b6866f4360f6dbb8347db954eb72e4dc6d636c3f1ff883c4ee6705d32`  
		Last Modified: Wed, 02 Mar 2022 19:11:32 GMT  
		Size: 34.2 MB (34182196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cc728be8fd7c689fbed576ea3e0ac8b415d98b4eae1409dcde85b8bca34f261`  
		Last Modified: Wed, 02 Mar 2022 19:11:25 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.19` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:a0b684f5aa0c2e8c0524aa749d5c1a8be415b697bf384ac2796b9a33738c7909
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.4 MB (114411149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20291514b2a89e2a5276623d0447d852bd091f441bd3ae8cb3005252c26c7a70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:17 GMT
ADD file:b388eaef074fa7cc4e0f6f0b6a56e4be6c69489b63477ab4469ff5415074b0c7 in / 
# Tue, 01 Mar 2022 02:02:18 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 09:26:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 09:26:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 03 Mar 2022 00:04:40 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 00:04:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 03 Mar 2022 00:04:54 GMT
ENV TELEGRAF_VERSION=1.19.3
# Thu, 03 Mar 2022 00:05:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 03 Mar 2022 00:05:05 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 03 Mar 2022 00:05:05 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 03 Mar 2022 00:05:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Mar 2022 00:05:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:17a41fc762495ca54ac53f271889bdf4ac8bea7cedfa3b585e4e42ef106935f1`  
		Last Modified: Tue, 01 Mar 2022 02:18:24 GMT  
		Size: 50.1 MB (50117069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9173ee01c42f46f1839650f0a56ee12ab74693f31dacccf586222ef98cb4ec19`  
		Last Modified: Tue, 01 Mar 2022 09:51:00 GMT  
		Size: 4.9 MB (4922642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f119f27841bdc8ee96fe83e4e2bb9b453db5a3a239036547b8e09c87f650befe`  
		Last Modified: Tue, 01 Mar 2022 09:51:01 GMT  
		Size: 10.2 MB (10216974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2baf44ae0880a128f8b5507925605cf1d2d330ad512283e027d0681a97e862`  
		Last Modified: Thu, 03 Mar 2022 00:06:55 GMT  
		Size: 17.5 MB (17462257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ac34fd4d174e3a615b556538c0faf99c0bea701cd679644b8b80bbbdec9614`  
		Last Modified: Thu, 03 Mar 2022 00:06:43 GMT  
		Size: 2.9 KB (2902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f94304fd072006bb9c490168f178f8523ffd0e3ee5c18d36140d347bf6ab4df3`  
		Last Modified: Thu, 03 Mar 2022 00:07:05 GMT  
		Size: 31.7 MB (31688963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c99e41a5874ac0eadb33cbf66a315829fc6e02543d916b02e1d15b4f96c810`  
		Last Modified: Thu, 03 Mar 2022 00:06:43 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.19` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:077be1f85f1c5528a526fcf17ba13cb0db5ada0b287fdff255107cb695d9254a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.6 MB (118557730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cec5c2ab17f10243e26e648fa27589716323aed2d856cc9679d800f49d02c78`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:41 GMT
ADD file:5effc7e0ab7312f14a7ee81c06c71400aae31219d477ebe1a4f7a9156797c42a in / 
# Thu, 17 Mar 2022 03:21:42 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:11:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 04:25:26 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 04:26:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 19 Mar 2022 04:26:11 GMT
ENV TELEGRAF_VERSION=1.19.3
# Sat, 19 Mar 2022 04:26:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Sat, 19 Mar 2022 04:26:17 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 19 Mar 2022 04:26:19 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Sat, 19 Mar 2022 04:26:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 19 Mar 2022 04:26:20 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:260ad8146ed2447d5587608b10fed4f80de80cdc559e619f3a235d3ba09eaf7b`  
		Last Modified: Thu, 17 Mar 2022 03:28:04 GMT  
		Size: 53.6 MB (53616308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1399f445da611be3789923cf26d158e3f4f80449b7295fa069a8eaecaaf137e6`  
		Last Modified: Thu, 17 Mar 2022 22:20:58 GMT  
		Size: 4.9 MB (4937558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd9e43777fa6c09c341f3aa922f47b5b3ace26de1d779124afd2f1d435731d9`  
		Last Modified: Thu, 17 Mar 2022 22:20:58 GMT  
		Size: 10.7 MB (10655858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab386e029a6d39b09f87391f007c31a225e7d347c44bae2e2fd64a04907880a`  
		Last Modified: Sat, 19 Mar 2022 04:27:19 GMT  
		Size: 18.4 MB (18382667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ddc7d0a6abc23254f7f6f0777da96117b906c81122c629c9c294a6037ef475`  
		Last Modified: Sat, 19 Mar 2022 04:27:15 GMT  
		Size: 2.9 KB (2877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bae1432cc5e92431beeaeaf9322df8b7fd09ee3d3a32ae33d18bfb5ebcf652`  
		Last Modified: Sat, 19 Mar 2022 04:27:21 GMT  
		Size: 31.0 MB (30962118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2802d42181b6912e7dde7e12daf9c4bba764249c82add8c791d65a64f01143b`  
		Last Modified: Sat, 19 Mar 2022 04:27:15 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.19-alpine`

```console
$ docker pull telegraf@sha256:eb3f824a6f91c5da546d0d0ba7cc0ffe13b05ff8698564018f0be3a6316e749a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:1.19-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:d3eb64e462f33a293d68a0bf9cd3a3442d30251316ccda8008778ea7790b5d48
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40231757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36814eac3e16e1d4ec3f65f63e24ee88ac046b57def2fac5edc6ddb1e4b6669f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 17 Mar 2022 04:01:58 GMT
ADD file:cf4b631a115c2bbfbd81cad2d3041bceb64a8136aac92ba8a63b6c51d60af764 in / 
# Thu, 17 Mar 2022 04:01:59 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 15:55:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Mar 2022 15:55:59 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Thu, 17 Mar 2022 15:55:59 GMT
ENV TELEGRAF_VERSION=1.19.3
# Thu, 17 Mar 2022 15:56:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Thu, 17 Mar 2022 15:56:42 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 17 Mar 2022 15:56:42 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Thu, 17 Mar 2022 15:56:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Mar 2022 15:56:42 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:3d243047344378e9b7136d552d48feb7ea8b6fe14ce0990e0cc011d5e369626a`  
		Last Modified: Thu, 17 Mar 2022 04:02:41 GMT  
		Size: 2.8 MB (2812636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c53ac0d2d7a9a6e5e1fbb7e66008a62369c80becca62a738e68c89542a878c6`  
		Last Modified: Thu, 17 Mar 2022 15:59:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5444d45dfde01b4fbe1e839fb426c861db8ec2678ed06e04deca9e259866b852`  
		Last Modified: Thu, 17 Mar 2022 15:59:09 GMT  
		Size: 3.4 MB (3372396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:673d942270e525efb9cde4f46649475a6682a90df37e967d2796fe5ab7bff57f`  
		Last Modified: Thu, 17 Mar 2022 15:59:15 GMT  
		Size: 34.0 MB (34046244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c689dd438aafa5df8aa8e8d1dd6fe490bda08670dcc1d00bf0ad2c018efa130d`  
		Last Modified: Thu, 17 Mar 2022 15:59:08 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.19.3`

```console
$ docker pull telegraf@sha256:e3b4d450a136777e0bdd1f31b7eec5bc30cef34b01866b77a3c111383173ce6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.19.3` - linux; amd64

```console
$ docker pull telegraf@sha256:0ae72c62868b76d4841883e64325ffa3bf449347af187458db2ba5237635e6bc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.9 MB (123887524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06c4e5423cc4ef40c175979c458b0c9988a81c546121dc5fb47e9a7e4ddd7d5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:15 GMT
ADD file:9c4db2a9644ee3029a8e9cca58350efef660c3167e59b91f2bee9c303e592664 in / 
# Tue, 01 Mar 2022 02:13:15 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 06:25:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:26:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 02 Mar 2022 19:10:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 19:10:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 02 Mar 2022 19:10:40 GMT
ENV TELEGRAF_VERSION=1.19.3
# Wed, 02 Mar 2022 19:10:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 02 Mar 2022 19:10:44 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 02 Mar 2022 19:10:44 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 02 Mar 2022 19:10:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Mar 2022 19:10:44 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e4d61adff2077d048c6372d73c41b0bd68f525ad41f5530af05098a876683055`  
		Last Modified: Tue, 01 Mar 2022 02:18:55 GMT  
		Size: 54.9 MB (54917063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff1945c672b08a1791df62afaaf8aff14d3047155365f9c3646902937f7ffe6`  
		Last Modified: Tue, 01 Mar 2022 06:36:13 GMT  
		Size: 5.2 MB (5153034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5b10aec998344606441aec43a335ab6326f32aae331aab27da16a6bb4ec2be`  
		Last Modified: Tue, 01 Mar 2022 06:36:14 GMT  
		Size: 10.9 MB (10871885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7914280ffd1a89468d7300475f199f63daf36d7d310ca3e2f8a21424b6992e29`  
		Last Modified: Wed, 02 Mar 2022 19:11:29 GMT  
		Size: 18.8 MB (18760097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053949c9b19fa7512f69b5dc25fb96a03488191d90009ce09da1d77a5268b915`  
		Last Modified: Wed, 02 Mar 2022 19:11:25 GMT  
		Size: 2.9 KB (2905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adc6da8b6866f4360f6dbb8347db954eb72e4dc6d636c3f1ff883c4ee6705d32`  
		Last Modified: Wed, 02 Mar 2022 19:11:32 GMT  
		Size: 34.2 MB (34182196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cc728be8fd7c689fbed576ea3e0ac8b415d98b4eae1409dcde85b8bca34f261`  
		Last Modified: Wed, 02 Mar 2022 19:11:25 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.19.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:a0b684f5aa0c2e8c0524aa749d5c1a8be415b697bf384ac2796b9a33738c7909
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.4 MB (114411149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20291514b2a89e2a5276623d0447d852bd091f441bd3ae8cb3005252c26c7a70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:17 GMT
ADD file:b388eaef074fa7cc4e0f6f0b6a56e4be6c69489b63477ab4469ff5415074b0c7 in / 
# Tue, 01 Mar 2022 02:02:18 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 09:26:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 09:26:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 03 Mar 2022 00:04:40 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 00:04:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 03 Mar 2022 00:04:54 GMT
ENV TELEGRAF_VERSION=1.19.3
# Thu, 03 Mar 2022 00:05:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 03 Mar 2022 00:05:05 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 03 Mar 2022 00:05:05 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 03 Mar 2022 00:05:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Mar 2022 00:05:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:17a41fc762495ca54ac53f271889bdf4ac8bea7cedfa3b585e4e42ef106935f1`  
		Last Modified: Tue, 01 Mar 2022 02:18:24 GMT  
		Size: 50.1 MB (50117069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9173ee01c42f46f1839650f0a56ee12ab74693f31dacccf586222ef98cb4ec19`  
		Last Modified: Tue, 01 Mar 2022 09:51:00 GMT  
		Size: 4.9 MB (4922642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f119f27841bdc8ee96fe83e4e2bb9b453db5a3a239036547b8e09c87f650befe`  
		Last Modified: Tue, 01 Mar 2022 09:51:01 GMT  
		Size: 10.2 MB (10216974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2baf44ae0880a128f8b5507925605cf1d2d330ad512283e027d0681a97e862`  
		Last Modified: Thu, 03 Mar 2022 00:06:55 GMT  
		Size: 17.5 MB (17462257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ac34fd4d174e3a615b556538c0faf99c0bea701cd679644b8b80bbbdec9614`  
		Last Modified: Thu, 03 Mar 2022 00:06:43 GMT  
		Size: 2.9 KB (2902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f94304fd072006bb9c490168f178f8523ffd0e3ee5c18d36140d347bf6ab4df3`  
		Last Modified: Thu, 03 Mar 2022 00:07:05 GMT  
		Size: 31.7 MB (31688963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c99e41a5874ac0eadb33cbf66a315829fc6e02543d916b02e1d15b4f96c810`  
		Last Modified: Thu, 03 Mar 2022 00:06:43 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.19.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:077be1f85f1c5528a526fcf17ba13cb0db5ada0b287fdff255107cb695d9254a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.6 MB (118557730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cec5c2ab17f10243e26e648fa27589716323aed2d856cc9679d800f49d02c78`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:41 GMT
ADD file:5effc7e0ab7312f14a7ee81c06c71400aae31219d477ebe1a4f7a9156797c42a in / 
# Thu, 17 Mar 2022 03:21:42 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:11:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 04:25:26 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 04:26:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 19 Mar 2022 04:26:11 GMT
ENV TELEGRAF_VERSION=1.19.3
# Sat, 19 Mar 2022 04:26:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Sat, 19 Mar 2022 04:26:17 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 19 Mar 2022 04:26:19 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Sat, 19 Mar 2022 04:26:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 19 Mar 2022 04:26:20 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:260ad8146ed2447d5587608b10fed4f80de80cdc559e619f3a235d3ba09eaf7b`  
		Last Modified: Thu, 17 Mar 2022 03:28:04 GMT  
		Size: 53.6 MB (53616308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1399f445da611be3789923cf26d158e3f4f80449b7295fa069a8eaecaaf137e6`  
		Last Modified: Thu, 17 Mar 2022 22:20:58 GMT  
		Size: 4.9 MB (4937558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd9e43777fa6c09c341f3aa922f47b5b3ace26de1d779124afd2f1d435731d9`  
		Last Modified: Thu, 17 Mar 2022 22:20:58 GMT  
		Size: 10.7 MB (10655858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab386e029a6d39b09f87391f007c31a225e7d347c44bae2e2fd64a04907880a`  
		Last Modified: Sat, 19 Mar 2022 04:27:19 GMT  
		Size: 18.4 MB (18382667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ddc7d0a6abc23254f7f6f0777da96117b906c81122c629c9c294a6037ef475`  
		Last Modified: Sat, 19 Mar 2022 04:27:15 GMT  
		Size: 2.9 KB (2877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12bae1432cc5e92431beeaeaf9322df8b7fd09ee3d3a32ae33d18bfb5ebcf652`  
		Last Modified: Sat, 19 Mar 2022 04:27:21 GMT  
		Size: 31.0 MB (30962118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2802d42181b6912e7dde7e12daf9c4bba764249c82add8c791d65a64f01143b`  
		Last Modified: Sat, 19 Mar 2022 04:27:15 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.19.3-alpine`

```console
$ docker pull telegraf@sha256:eb3f824a6f91c5da546d0d0ba7cc0ffe13b05ff8698564018f0be3a6316e749a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:1.19.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:d3eb64e462f33a293d68a0bf9cd3a3442d30251316ccda8008778ea7790b5d48
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40231757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36814eac3e16e1d4ec3f65f63e24ee88ac046b57def2fac5edc6ddb1e4b6669f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 17 Mar 2022 04:01:58 GMT
ADD file:cf4b631a115c2bbfbd81cad2d3041bceb64a8136aac92ba8a63b6c51d60af764 in / 
# Thu, 17 Mar 2022 04:01:59 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 15:55:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Mar 2022 15:55:59 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Thu, 17 Mar 2022 15:55:59 GMT
ENV TELEGRAF_VERSION=1.19.3
# Thu, 17 Mar 2022 15:56:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Thu, 17 Mar 2022 15:56:42 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 17 Mar 2022 15:56:42 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Thu, 17 Mar 2022 15:56:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Mar 2022 15:56:42 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:3d243047344378e9b7136d552d48feb7ea8b6fe14ce0990e0cc011d5e369626a`  
		Last Modified: Thu, 17 Mar 2022 04:02:41 GMT  
		Size: 2.8 MB (2812636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c53ac0d2d7a9a6e5e1fbb7e66008a62369c80becca62a738e68c89542a878c6`  
		Last Modified: Thu, 17 Mar 2022 15:59:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5444d45dfde01b4fbe1e839fb426c861db8ec2678ed06e04deca9e259866b852`  
		Last Modified: Thu, 17 Mar 2022 15:59:09 GMT  
		Size: 3.4 MB (3372396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:673d942270e525efb9cde4f46649475a6682a90df37e967d2796fe5ab7bff57f`  
		Last Modified: Thu, 17 Mar 2022 15:59:15 GMT  
		Size: 34.0 MB (34046244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c689dd438aafa5df8aa8e8d1dd6fe490bda08670dcc1d00bf0ad2c018efa130d`  
		Last Modified: Thu, 17 Mar 2022 15:59:08 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.20`

```console
$ docker pull telegraf@sha256:5f6db769cdcfac87a179f5067a5d26717fab0f51ea67df3d68ee55541e9d196d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.20` - linux; amd64

```console
$ docker pull telegraf@sha256:f6d0a32bdfb47b8152fb005674d2ba96ffc128681ccb3fe3902920c660820e74
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125333463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b61badd4df14653de467d262fcbd8231f80668a3fbcdf5164d86886ae76c2c20`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:15 GMT
ADD file:9c4db2a9644ee3029a8e9cca58350efef660c3167e59b91f2bee9c303e592664 in / 
# Tue, 01 Mar 2022 02:13:15 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 06:25:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:26:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 02 Mar 2022 19:10:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 19:10:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 02 Mar 2022 19:10:52 GMT
ENV TELEGRAF_VERSION=1.20.4
# Wed, 02 Mar 2022 19:10:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 02 Mar 2022 19:10:56 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 02 Mar 2022 19:10:56 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 02 Mar 2022 19:10:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Mar 2022 19:10:56 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e4d61adff2077d048c6372d73c41b0bd68f525ad41f5530af05098a876683055`  
		Last Modified: Tue, 01 Mar 2022 02:18:55 GMT  
		Size: 54.9 MB (54917063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff1945c672b08a1791df62afaaf8aff14d3047155365f9c3646902937f7ffe6`  
		Last Modified: Tue, 01 Mar 2022 06:36:13 GMT  
		Size: 5.2 MB (5153034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5b10aec998344606441aec43a335ab6326f32aae331aab27da16a6bb4ec2be`  
		Last Modified: Tue, 01 Mar 2022 06:36:14 GMT  
		Size: 10.9 MB (10871885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7914280ffd1a89468d7300475f199f63daf36d7d310ca3e2f8a21424b6992e29`  
		Last Modified: Wed, 02 Mar 2022 19:11:29 GMT  
		Size: 18.8 MB (18760097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053949c9b19fa7512f69b5dc25fb96a03488191d90009ce09da1d77a5268b915`  
		Last Modified: Wed, 02 Mar 2022 19:11:25 GMT  
		Size: 2.9 KB (2905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6153460c1cab6aa85a325673131b4f914d9c56f589aa115aaba81bae33b6397`  
		Last Modified: Wed, 02 Mar 2022 19:11:49 GMT  
		Size: 35.6 MB (35628138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2003c3dbc4356ac2234286e0dda9db4c1b8dc6b62cb079608f2a5981065cc373`  
		Last Modified: Wed, 02 Mar 2022 19:11:42 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.20` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:e3bc07d069c6f4eaaa0f319116705dbaead8f2742786d4d8d9a2601f935fa269
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115811730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1373a90062af4d2fc508eced16f7ef15cad2d982bafb53148b8d74e4ea0bb139`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:17 GMT
ADD file:b388eaef074fa7cc4e0f6f0b6a56e4be6c69489b63477ab4469ff5415074b0c7 in / 
# Tue, 01 Mar 2022 02:02:18 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 09:26:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 09:26:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 03 Mar 2022 00:04:40 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 00:04:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 03 Mar 2022 00:05:20 GMT
ENV TELEGRAF_VERSION=1.20.4
# Thu, 03 Mar 2022 00:05:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 03 Mar 2022 00:05:33 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 03 Mar 2022 00:05:33 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 03 Mar 2022 00:05:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Mar 2022 00:05:34 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:17a41fc762495ca54ac53f271889bdf4ac8bea7cedfa3b585e4e42ef106935f1`  
		Last Modified: Tue, 01 Mar 2022 02:18:24 GMT  
		Size: 50.1 MB (50117069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9173ee01c42f46f1839650f0a56ee12ab74693f31dacccf586222ef98cb4ec19`  
		Last Modified: Tue, 01 Mar 2022 09:51:00 GMT  
		Size: 4.9 MB (4922642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f119f27841bdc8ee96fe83e4e2bb9b453db5a3a239036547b8e09c87f650befe`  
		Last Modified: Tue, 01 Mar 2022 09:51:01 GMT  
		Size: 10.2 MB (10216974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2baf44ae0880a128f8b5507925605cf1d2d330ad512283e027d0681a97e862`  
		Last Modified: Thu, 03 Mar 2022 00:06:55 GMT  
		Size: 17.5 MB (17462257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ac34fd4d174e3a615b556538c0faf99c0bea701cd679644b8b80bbbdec9614`  
		Last Modified: Thu, 03 Mar 2022 00:06:43 GMT  
		Size: 2.9 KB (2902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dc2d2bc047442aa745ff8c7e2c199690977771cb24a363501fa34b10e43284`  
		Last Modified: Thu, 03 Mar 2022 00:07:40 GMT  
		Size: 33.1 MB (33089543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7d93192845e9e9765d1cf67f1d3044407d976a81e94570abfb3f854835aa09`  
		Last Modified: Thu, 03 Mar 2022 00:07:16 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.20` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:ec29b0767b5eb96155ae7c52a84ff0cd169d6dbbf0fbff45af795b4a4a210f80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (119959886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:758ba4c3ec69bf1deb848c8587595d294422ce6cf7d47807ec3829d4142606c0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:41 GMT
ADD file:5effc7e0ab7312f14a7ee81c06c71400aae31219d477ebe1a4f7a9156797c42a in / 
# Thu, 17 Mar 2022 03:21:42 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:11:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 04:25:26 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 04:26:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 19 Mar 2022 04:26:33 GMT
ENV TELEGRAF_VERSION=1.20.4
# Sat, 19 Mar 2022 04:26:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Sat, 19 Mar 2022 04:26:38 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 19 Mar 2022 04:26:39 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Sat, 19 Mar 2022 04:26:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 19 Mar 2022 04:26:40 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:260ad8146ed2447d5587608b10fed4f80de80cdc559e619f3a235d3ba09eaf7b`  
		Last Modified: Thu, 17 Mar 2022 03:28:04 GMT  
		Size: 53.6 MB (53616308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1399f445da611be3789923cf26d158e3f4f80449b7295fa069a8eaecaaf137e6`  
		Last Modified: Thu, 17 Mar 2022 22:20:58 GMT  
		Size: 4.9 MB (4937558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd9e43777fa6c09c341f3aa922f47b5b3ace26de1d779124afd2f1d435731d9`  
		Last Modified: Thu, 17 Mar 2022 22:20:58 GMT  
		Size: 10.7 MB (10655858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab386e029a6d39b09f87391f007c31a225e7d347c44bae2e2fd64a04907880a`  
		Last Modified: Sat, 19 Mar 2022 04:27:19 GMT  
		Size: 18.4 MB (18382667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ddc7d0a6abc23254f7f6f0777da96117b906c81122c629c9c294a6037ef475`  
		Last Modified: Sat, 19 Mar 2022 04:27:15 GMT  
		Size: 2.9 KB (2877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7890a160b1b9616ff27729d3d7be91fc563b23b70c4346d30e055e738e46b87`  
		Last Modified: Sat, 19 Mar 2022 04:27:40 GMT  
		Size: 32.4 MB (32364277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea989c17ecfbf2abf523ad9ab83abffe3bb013ca9cd3be830412308dc51e5abf`  
		Last Modified: Sat, 19 Mar 2022 04:27:34 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.20-alpine`

```console
$ docker pull telegraf@sha256:4a8050d3601ba71dfe9a94793a9fd9a80dc233c6e6b1147a71df22a312e05f78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:1.20-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:82ec236b8f1cbf80f32fe164d4f0edd0728ebcf3e677857ac9cc9f0be06ce112
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41655626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d562b9cc477b1033293ed75694b711b5e6c72b9141cadf12f054896dec588d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 17 Mar 2022 04:01:58 GMT
ADD file:cf4b631a115c2bbfbd81cad2d3041bceb64a8136aac92ba8a63b6c51d60af764 in / 
# Thu, 17 Mar 2022 04:01:59 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 15:55:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Mar 2022 15:55:59 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Thu, 17 Mar 2022 15:56:57 GMT
ENV TELEGRAF_VERSION=1.20.4
# Thu, 17 Mar 2022 15:57:51 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Thu, 17 Mar 2022 15:57:51 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 17 Mar 2022 15:57:51 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Thu, 17 Mar 2022 15:57:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Mar 2022 15:57:52 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:3d243047344378e9b7136d552d48feb7ea8b6fe14ce0990e0cc011d5e369626a`  
		Last Modified: Thu, 17 Mar 2022 04:02:41 GMT  
		Size: 2.8 MB (2812636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c53ac0d2d7a9a6e5e1fbb7e66008a62369c80becca62a738e68c89542a878c6`  
		Last Modified: Thu, 17 Mar 2022 15:59:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5444d45dfde01b4fbe1e839fb426c861db8ec2678ed06e04deca9e259866b852`  
		Last Modified: Thu, 17 Mar 2022 15:59:09 GMT  
		Size: 3.4 MB (3372396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fb75af43298c998005145c8ae8023715e94d3cd78ac592fb2858f6e4115c11`  
		Last Modified: Thu, 17 Mar 2022 15:59:32 GMT  
		Size: 35.5 MB (35470113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e96cd54f5045b1af32e9465c76258616252188ab8464c5dcfef4676a95f6f86`  
		Last Modified: Thu, 17 Mar 2022 15:59:26 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.20.4`

```console
$ docker pull telegraf@sha256:5f6db769cdcfac87a179f5067a5d26717fab0f51ea67df3d68ee55541e9d196d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.20.4` - linux; amd64

```console
$ docker pull telegraf@sha256:f6d0a32bdfb47b8152fb005674d2ba96ffc128681ccb3fe3902920c660820e74
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125333463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b61badd4df14653de467d262fcbd8231f80668a3fbcdf5164d86886ae76c2c20`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:15 GMT
ADD file:9c4db2a9644ee3029a8e9cca58350efef660c3167e59b91f2bee9c303e592664 in / 
# Tue, 01 Mar 2022 02:13:15 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 06:25:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:26:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 02 Mar 2022 19:10:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 19:10:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 02 Mar 2022 19:10:52 GMT
ENV TELEGRAF_VERSION=1.20.4
# Wed, 02 Mar 2022 19:10:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 02 Mar 2022 19:10:56 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 02 Mar 2022 19:10:56 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 02 Mar 2022 19:10:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Mar 2022 19:10:56 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e4d61adff2077d048c6372d73c41b0bd68f525ad41f5530af05098a876683055`  
		Last Modified: Tue, 01 Mar 2022 02:18:55 GMT  
		Size: 54.9 MB (54917063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff1945c672b08a1791df62afaaf8aff14d3047155365f9c3646902937f7ffe6`  
		Last Modified: Tue, 01 Mar 2022 06:36:13 GMT  
		Size: 5.2 MB (5153034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5b10aec998344606441aec43a335ab6326f32aae331aab27da16a6bb4ec2be`  
		Last Modified: Tue, 01 Mar 2022 06:36:14 GMT  
		Size: 10.9 MB (10871885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7914280ffd1a89468d7300475f199f63daf36d7d310ca3e2f8a21424b6992e29`  
		Last Modified: Wed, 02 Mar 2022 19:11:29 GMT  
		Size: 18.8 MB (18760097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053949c9b19fa7512f69b5dc25fb96a03488191d90009ce09da1d77a5268b915`  
		Last Modified: Wed, 02 Mar 2022 19:11:25 GMT  
		Size: 2.9 KB (2905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6153460c1cab6aa85a325673131b4f914d9c56f589aa115aaba81bae33b6397`  
		Last Modified: Wed, 02 Mar 2022 19:11:49 GMT  
		Size: 35.6 MB (35628138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2003c3dbc4356ac2234286e0dda9db4c1b8dc6b62cb079608f2a5981065cc373`  
		Last Modified: Wed, 02 Mar 2022 19:11:42 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.20.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:e3bc07d069c6f4eaaa0f319116705dbaead8f2742786d4d8d9a2601f935fa269
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.8 MB (115811730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1373a90062af4d2fc508eced16f7ef15cad2d982bafb53148b8d74e4ea0bb139`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:17 GMT
ADD file:b388eaef074fa7cc4e0f6f0b6a56e4be6c69489b63477ab4469ff5415074b0c7 in / 
# Tue, 01 Mar 2022 02:02:18 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 09:26:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 09:26:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 03 Mar 2022 00:04:40 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 00:04:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 03 Mar 2022 00:05:20 GMT
ENV TELEGRAF_VERSION=1.20.4
# Thu, 03 Mar 2022 00:05:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 03 Mar 2022 00:05:33 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 03 Mar 2022 00:05:33 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 03 Mar 2022 00:05:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Mar 2022 00:05:34 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:17a41fc762495ca54ac53f271889bdf4ac8bea7cedfa3b585e4e42ef106935f1`  
		Last Modified: Tue, 01 Mar 2022 02:18:24 GMT  
		Size: 50.1 MB (50117069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9173ee01c42f46f1839650f0a56ee12ab74693f31dacccf586222ef98cb4ec19`  
		Last Modified: Tue, 01 Mar 2022 09:51:00 GMT  
		Size: 4.9 MB (4922642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f119f27841bdc8ee96fe83e4e2bb9b453db5a3a239036547b8e09c87f650befe`  
		Last Modified: Tue, 01 Mar 2022 09:51:01 GMT  
		Size: 10.2 MB (10216974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2baf44ae0880a128f8b5507925605cf1d2d330ad512283e027d0681a97e862`  
		Last Modified: Thu, 03 Mar 2022 00:06:55 GMT  
		Size: 17.5 MB (17462257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ac34fd4d174e3a615b556538c0faf99c0bea701cd679644b8b80bbbdec9614`  
		Last Modified: Thu, 03 Mar 2022 00:06:43 GMT  
		Size: 2.9 KB (2902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dc2d2bc047442aa745ff8c7e2c199690977771cb24a363501fa34b10e43284`  
		Last Modified: Thu, 03 Mar 2022 00:07:40 GMT  
		Size: 33.1 MB (33089543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7d93192845e9e9765d1cf67f1d3044407d976a81e94570abfb3f854835aa09`  
		Last Modified: Thu, 03 Mar 2022 00:07:16 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.20.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:ec29b0767b5eb96155ae7c52a84ff0cd169d6dbbf0fbff45af795b4a4a210f80
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (119959886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:758ba4c3ec69bf1deb848c8587595d294422ce6cf7d47807ec3829d4142606c0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:41 GMT
ADD file:5effc7e0ab7312f14a7ee81c06c71400aae31219d477ebe1a4f7a9156797c42a in / 
# Thu, 17 Mar 2022 03:21:42 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:11:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 04:25:26 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 04:26:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 19 Mar 2022 04:26:33 GMT
ENV TELEGRAF_VERSION=1.20.4
# Sat, 19 Mar 2022 04:26:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Sat, 19 Mar 2022 04:26:38 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 19 Mar 2022 04:26:39 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Sat, 19 Mar 2022 04:26:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 19 Mar 2022 04:26:40 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:260ad8146ed2447d5587608b10fed4f80de80cdc559e619f3a235d3ba09eaf7b`  
		Last Modified: Thu, 17 Mar 2022 03:28:04 GMT  
		Size: 53.6 MB (53616308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1399f445da611be3789923cf26d158e3f4f80449b7295fa069a8eaecaaf137e6`  
		Last Modified: Thu, 17 Mar 2022 22:20:58 GMT  
		Size: 4.9 MB (4937558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd9e43777fa6c09c341f3aa922f47b5b3ace26de1d779124afd2f1d435731d9`  
		Last Modified: Thu, 17 Mar 2022 22:20:58 GMT  
		Size: 10.7 MB (10655858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab386e029a6d39b09f87391f007c31a225e7d347c44bae2e2fd64a04907880a`  
		Last Modified: Sat, 19 Mar 2022 04:27:19 GMT  
		Size: 18.4 MB (18382667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ddc7d0a6abc23254f7f6f0777da96117b906c81122c629c9c294a6037ef475`  
		Last Modified: Sat, 19 Mar 2022 04:27:15 GMT  
		Size: 2.9 KB (2877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7890a160b1b9616ff27729d3d7be91fc563b23b70c4346d30e055e738e46b87`  
		Last Modified: Sat, 19 Mar 2022 04:27:40 GMT  
		Size: 32.4 MB (32364277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea989c17ecfbf2abf523ad9ab83abffe3bb013ca9cd3be830412308dc51e5abf`  
		Last Modified: Sat, 19 Mar 2022 04:27:34 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.20.4-alpine`

```console
$ docker pull telegraf@sha256:4a8050d3601ba71dfe9a94793a9fd9a80dc233c6e6b1147a71df22a312e05f78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:1.20.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:82ec236b8f1cbf80f32fe164d4f0edd0728ebcf3e677857ac9cc9f0be06ce112
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41655626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d562b9cc477b1033293ed75694b711b5e6c72b9141cadf12f054896dec588d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 17 Mar 2022 04:01:58 GMT
ADD file:cf4b631a115c2bbfbd81cad2d3041bceb64a8136aac92ba8a63b6c51d60af764 in / 
# Thu, 17 Mar 2022 04:01:59 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 15:55:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Mar 2022 15:55:59 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Thu, 17 Mar 2022 15:56:57 GMT
ENV TELEGRAF_VERSION=1.20.4
# Thu, 17 Mar 2022 15:57:51 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Thu, 17 Mar 2022 15:57:51 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 17 Mar 2022 15:57:51 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Thu, 17 Mar 2022 15:57:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Mar 2022 15:57:52 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:3d243047344378e9b7136d552d48feb7ea8b6fe14ce0990e0cc011d5e369626a`  
		Last Modified: Thu, 17 Mar 2022 04:02:41 GMT  
		Size: 2.8 MB (2812636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c53ac0d2d7a9a6e5e1fbb7e66008a62369c80becca62a738e68c89542a878c6`  
		Last Modified: Thu, 17 Mar 2022 15:59:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5444d45dfde01b4fbe1e839fb426c861db8ec2678ed06e04deca9e259866b852`  
		Last Modified: Thu, 17 Mar 2022 15:59:09 GMT  
		Size: 3.4 MB (3372396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fb75af43298c998005145c8ae8023715e94d3cd78ac592fb2858f6e4115c11`  
		Last Modified: Thu, 17 Mar 2022 15:59:32 GMT  
		Size: 35.5 MB (35470113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e96cd54f5045b1af32e9465c76258616252188ab8464c5dcfef4676a95f6f86`  
		Last Modified: Thu, 17 Mar 2022 15:59:26 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.21`

```console
$ docker pull telegraf@sha256:f2b60dc7ca0d3ca72c96d7ecf410d7aff7f565a8e7c0ed8c5da32aa9763c762e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.21` - linux; amd64

```console
$ docker pull telegraf@sha256:2e97cb40492427d41c3839aba954a28b58e6409149fee23d78feae66a4896285
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127362512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c094fe86696b7cf134f2f8d080c04bac1a84ddf280a81d07ed693bc391a184`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:15 GMT
ADD file:9c4db2a9644ee3029a8e9cca58350efef660c3167e59b91f2bee9c303e592664 in / 
# Tue, 01 Mar 2022 02:13:15 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 06:25:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:26:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 02 Mar 2022 19:10:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 19:10:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 02 Mar 2022 19:11:01 GMT
ENV TELEGRAF_VERSION=1.21.4
# Wed, 02 Mar 2022 19:11:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 02 Mar 2022 19:11:05 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 02 Mar 2022 19:11:05 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 02 Mar 2022 19:11:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Mar 2022 19:11:05 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e4d61adff2077d048c6372d73c41b0bd68f525ad41f5530af05098a876683055`  
		Last Modified: Tue, 01 Mar 2022 02:18:55 GMT  
		Size: 54.9 MB (54917063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff1945c672b08a1791df62afaaf8aff14d3047155365f9c3646902937f7ffe6`  
		Last Modified: Tue, 01 Mar 2022 06:36:13 GMT  
		Size: 5.2 MB (5153034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5b10aec998344606441aec43a335ab6326f32aae331aab27da16a6bb4ec2be`  
		Last Modified: Tue, 01 Mar 2022 06:36:14 GMT  
		Size: 10.9 MB (10871885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7914280ffd1a89468d7300475f199f63daf36d7d310ca3e2f8a21424b6992e29`  
		Last Modified: Wed, 02 Mar 2022 19:11:29 GMT  
		Size: 18.8 MB (18760097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053949c9b19fa7512f69b5dc25fb96a03488191d90009ce09da1d77a5268b915`  
		Last Modified: Wed, 02 Mar 2022 19:11:25 GMT  
		Size: 2.9 KB (2905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bd08429cefa379c2130c2bbc37cf518e029cc5a580fc133e4555c5717f5488f`  
		Last Modified: Wed, 02 Mar 2022 19:12:06 GMT  
		Size: 37.7 MB (37657184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5eeecdd6b1c66697c0f908b51b00706d683bf323b051139b2592191f33ae176`  
		Last Modified: Wed, 02 Mar 2022 19:11:59 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.21` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:87f7a13e248efd9409ceaad9f6cca33f3944c9b7c9b45120678c48ef1a726592
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117652818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a955da099968006b0d86b8a625b1570dcf0d7e3278f78b3520c412ee4de25981`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:17 GMT
ADD file:b388eaef074fa7cc4e0f6f0b6a56e4be6c69489b63477ab4469ff5415074b0c7 in / 
# Tue, 01 Mar 2022 02:02:18 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 09:26:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 09:26:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 03 Mar 2022 00:04:40 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 00:04:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 03 Mar 2022 00:05:45 GMT
ENV TELEGRAF_VERSION=1.21.4
# Thu, 03 Mar 2022 00:05:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 03 Mar 2022 00:05:58 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 03 Mar 2022 00:05:58 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 03 Mar 2022 00:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Mar 2022 00:05:59 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:17a41fc762495ca54ac53f271889bdf4ac8bea7cedfa3b585e4e42ef106935f1`  
		Last Modified: Tue, 01 Mar 2022 02:18:24 GMT  
		Size: 50.1 MB (50117069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9173ee01c42f46f1839650f0a56ee12ab74693f31dacccf586222ef98cb4ec19`  
		Last Modified: Tue, 01 Mar 2022 09:51:00 GMT  
		Size: 4.9 MB (4922642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f119f27841bdc8ee96fe83e4e2bb9b453db5a3a239036547b8e09c87f650befe`  
		Last Modified: Tue, 01 Mar 2022 09:51:01 GMT  
		Size: 10.2 MB (10216974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2baf44ae0880a128f8b5507925605cf1d2d330ad512283e027d0681a97e862`  
		Last Modified: Thu, 03 Mar 2022 00:06:55 GMT  
		Size: 17.5 MB (17462257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ac34fd4d174e3a615b556538c0faf99c0bea701cd679644b8b80bbbdec9614`  
		Last Modified: Thu, 03 Mar 2022 00:06:43 GMT  
		Size: 2.9 KB (2902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78af0ff2764399c5ac4654e7ecf8374d6370f16412b5b965baaef2e93dbe519a`  
		Last Modified: Thu, 03 Mar 2022 00:08:17 GMT  
		Size: 34.9 MB (34930630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764912f088ed42e1b8fec9e5343f19fa630101af941fc597cf0091f230c7a502`  
		Last Modified: Thu, 03 Mar 2022 00:07:52 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.21` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:fc25bd2273a71b84b8c80d050a16ca7229fc1b52170cf0e5ce7c4cf587107c38
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121755839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4604947ef10a3a25c9219d40df9589122836c7badf5d83452235ae639209d7f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:41 GMT
ADD file:5effc7e0ab7312f14a7ee81c06c71400aae31219d477ebe1a4f7a9156797c42a in / 
# Thu, 17 Mar 2022 03:21:42 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:11:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 04:25:26 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 04:26:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 19 Mar 2022 04:26:46 GMT
ENV TELEGRAF_VERSION=1.21.4
# Sat, 19 Mar 2022 04:26:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Sat, 19 Mar 2022 04:26:51 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 19 Mar 2022 04:26:52 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Sat, 19 Mar 2022 04:26:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 19 Mar 2022 04:26:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:260ad8146ed2447d5587608b10fed4f80de80cdc559e619f3a235d3ba09eaf7b`  
		Last Modified: Thu, 17 Mar 2022 03:28:04 GMT  
		Size: 53.6 MB (53616308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1399f445da611be3789923cf26d158e3f4f80449b7295fa069a8eaecaaf137e6`  
		Last Modified: Thu, 17 Mar 2022 22:20:58 GMT  
		Size: 4.9 MB (4937558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd9e43777fa6c09c341f3aa922f47b5b3ace26de1d779124afd2f1d435731d9`  
		Last Modified: Thu, 17 Mar 2022 22:20:58 GMT  
		Size: 10.7 MB (10655858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab386e029a6d39b09f87391f007c31a225e7d347c44bae2e2fd64a04907880a`  
		Last Modified: Sat, 19 Mar 2022 04:27:19 GMT  
		Size: 18.4 MB (18382667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ddc7d0a6abc23254f7f6f0777da96117b906c81122c629c9c294a6037ef475`  
		Last Modified: Sat, 19 Mar 2022 04:27:15 GMT  
		Size: 2.9 KB (2877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae5b52735eafeede0a1ef84e6d9fd0012298f52c17bc6024ec61289d39fb994`  
		Last Modified: Sat, 19 Mar 2022 04:27:56 GMT  
		Size: 34.2 MB (34160230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d089bea26f35e2412926e3d60813d5f8d202dd1041197930ce5e33eec74f6eba`  
		Last Modified: Sat, 19 Mar 2022 04:27:50 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.21-alpine`

```console
$ docker pull telegraf@sha256:cd19eb23a5bfa7fe475cbb119208e6410fd6ad75df19e0d497ff6bcf5ab2e9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:1.21-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:606b358fff99431a02f9bcbea3db5c4ef9464ad3111705075fd8db235139dcdc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43683756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004383a3acac314ec26d30745cdd3ab1c17cadc034dedc1ad0391bd56cec8182`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 17 Mar 2022 04:01:58 GMT
ADD file:cf4b631a115c2bbfbd81cad2d3041bceb64a8136aac92ba8a63b6c51d60af764 in / 
# Thu, 17 Mar 2022 04:01:59 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 15:55:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Mar 2022 15:55:59 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Thu, 17 Mar 2022 15:57:59 GMT
ENV TELEGRAF_VERSION=1.21.4
# Thu, 17 Mar 2022 15:58:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Thu, 17 Mar 2022 15:58:38 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 17 Mar 2022 15:58:38 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Thu, 17 Mar 2022 15:58:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Mar 2022 15:58:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:3d243047344378e9b7136d552d48feb7ea8b6fe14ce0990e0cc011d5e369626a`  
		Last Modified: Thu, 17 Mar 2022 04:02:41 GMT  
		Size: 2.8 MB (2812636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c53ac0d2d7a9a6e5e1fbb7e66008a62369c80becca62a738e68c89542a878c6`  
		Last Modified: Thu, 17 Mar 2022 15:59:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5444d45dfde01b4fbe1e839fb426c861db8ec2678ed06e04deca9e259866b852`  
		Last Modified: Thu, 17 Mar 2022 15:59:09 GMT  
		Size: 3.4 MB (3372396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aac486096e722bec0fedc87784582e9e3da67903a057c33f336d2e656eb5214`  
		Last Modified: Thu, 17 Mar 2022 15:59:49 GMT  
		Size: 37.5 MB (37498244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18762e036fe31460f4b12af0ba3fd23d7c809cfae6fa7517776652d5166998af`  
		Last Modified: Thu, 17 Mar 2022 15:59:43 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.21.4`

```console
$ docker pull telegraf@sha256:f2b60dc7ca0d3ca72c96d7ecf410d7aff7f565a8e7c0ed8c5da32aa9763c762e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.21.4` - linux; amd64

```console
$ docker pull telegraf@sha256:2e97cb40492427d41c3839aba954a28b58e6409149fee23d78feae66a4896285
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127362512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c094fe86696b7cf134f2f8d080c04bac1a84ddf280a81d07ed693bc391a184`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:15 GMT
ADD file:9c4db2a9644ee3029a8e9cca58350efef660c3167e59b91f2bee9c303e592664 in / 
# Tue, 01 Mar 2022 02:13:15 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 06:25:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:26:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 02 Mar 2022 19:10:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 19:10:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 02 Mar 2022 19:11:01 GMT
ENV TELEGRAF_VERSION=1.21.4
# Wed, 02 Mar 2022 19:11:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 02 Mar 2022 19:11:05 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 02 Mar 2022 19:11:05 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 02 Mar 2022 19:11:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Mar 2022 19:11:05 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e4d61adff2077d048c6372d73c41b0bd68f525ad41f5530af05098a876683055`  
		Last Modified: Tue, 01 Mar 2022 02:18:55 GMT  
		Size: 54.9 MB (54917063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff1945c672b08a1791df62afaaf8aff14d3047155365f9c3646902937f7ffe6`  
		Last Modified: Tue, 01 Mar 2022 06:36:13 GMT  
		Size: 5.2 MB (5153034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5b10aec998344606441aec43a335ab6326f32aae331aab27da16a6bb4ec2be`  
		Last Modified: Tue, 01 Mar 2022 06:36:14 GMT  
		Size: 10.9 MB (10871885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7914280ffd1a89468d7300475f199f63daf36d7d310ca3e2f8a21424b6992e29`  
		Last Modified: Wed, 02 Mar 2022 19:11:29 GMT  
		Size: 18.8 MB (18760097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053949c9b19fa7512f69b5dc25fb96a03488191d90009ce09da1d77a5268b915`  
		Last Modified: Wed, 02 Mar 2022 19:11:25 GMT  
		Size: 2.9 KB (2905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bd08429cefa379c2130c2bbc37cf518e029cc5a580fc133e4555c5717f5488f`  
		Last Modified: Wed, 02 Mar 2022 19:12:06 GMT  
		Size: 37.7 MB (37657184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5eeecdd6b1c66697c0f908b51b00706d683bf323b051139b2592191f33ae176`  
		Last Modified: Wed, 02 Mar 2022 19:11:59 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.21.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:87f7a13e248efd9409ceaad9f6cca33f3944c9b7c9b45120678c48ef1a726592
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117652818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a955da099968006b0d86b8a625b1570dcf0d7e3278f78b3520c412ee4de25981`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:17 GMT
ADD file:b388eaef074fa7cc4e0f6f0b6a56e4be6c69489b63477ab4469ff5415074b0c7 in / 
# Tue, 01 Mar 2022 02:02:18 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 09:26:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 09:26:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 03 Mar 2022 00:04:40 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 00:04:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 03 Mar 2022 00:05:45 GMT
ENV TELEGRAF_VERSION=1.21.4
# Thu, 03 Mar 2022 00:05:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 03 Mar 2022 00:05:58 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 03 Mar 2022 00:05:58 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 03 Mar 2022 00:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Mar 2022 00:05:59 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:17a41fc762495ca54ac53f271889bdf4ac8bea7cedfa3b585e4e42ef106935f1`  
		Last Modified: Tue, 01 Mar 2022 02:18:24 GMT  
		Size: 50.1 MB (50117069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9173ee01c42f46f1839650f0a56ee12ab74693f31dacccf586222ef98cb4ec19`  
		Last Modified: Tue, 01 Mar 2022 09:51:00 GMT  
		Size: 4.9 MB (4922642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f119f27841bdc8ee96fe83e4e2bb9b453db5a3a239036547b8e09c87f650befe`  
		Last Modified: Tue, 01 Mar 2022 09:51:01 GMT  
		Size: 10.2 MB (10216974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2baf44ae0880a128f8b5507925605cf1d2d330ad512283e027d0681a97e862`  
		Last Modified: Thu, 03 Mar 2022 00:06:55 GMT  
		Size: 17.5 MB (17462257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ac34fd4d174e3a615b556538c0faf99c0bea701cd679644b8b80bbbdec9614`  
		Last Modified: Thu, 03 Mar 2022 00:06:43 GMT  
		Size: 2.9 KB (2902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78af0ff2764399c5ac4654e7ecf8374d6370f16412b5b965baaef2e93dbe519a`  
		Last Modified: Thu, 03 Mar 2022 00:08:17 GMT  
		Size: 34.9 MB (34930630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764912f088ed42e1b8fec9e5343f19fa630101af941fc597cf0091f230c7a502`  
		Last Modified: Thu, 03 Mar 2022 00:07:52 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.21.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:fc25bd2273a71b84b8c80d050a16ca7229fc1b52170cf0e5ce7c4cf587107c38
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121755839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4604947ef10a3a25c9219d40df9589122836c7badf5d83452235ae639209d7f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:41 GMT
ADD file:5effc7e0ab7312f14a7ee81c06c71400aae31219d477ebe1a4f7a9156797c42a in / 
# Thu, 17 Mar 2022 03:21:42 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:11:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 04:25:26 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 04:26:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 19 Mar 2022 04:26:46 GMT
ENV TELEGRAF_VERSION=1.21.4
# Sat, 19 Mar 2022 04:26:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Sat, 19 Mar 2022 04:26:51 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 19 Mar 2022 04:26:52 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Sat, 19 Mar 2022 04:26:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 19 Mar 2022 04:26:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:260ad8146ed2447d5587608b10fed4f80de80cdc559e619f3a235d3ba09eaf7b`  
		Last Modified: Thu, 17 Mar 2022 03:28:04 GMT  
		Size: 53.6 MB (53616308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1399f445da611be3789923cf26d158e3f4f80449b7295fa069a8eaecaaf137e6`  
		Last Modified: Thu, 17 Mar 2022 22:20:58 GMT  
		Size: 4.9 MB (4937558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd9e43777fa6c09c341f3aa922f47b5b3ace26de1d779124afd2f1d435731d9`  
		Last Modified: Thu, 17 Mar 2022 22:20:58 GMT  
		Size: 10.7 MB (10655858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab386e029a6d39b09f87391f007c31a225e7d347c44bae2e2fd64a04907880a`  
		Last Modified: Sat, 19 Mar 2022 04:27:19 GMT  
		Size: 18.4 MB (18382667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ddc7d0a6abc23254f7f6f0777da96117b906c81122c629c9c294a6037ef475`  
		Last Modified: Sat, 19 Mar 2022 04:27:15 GMT  
		Size: 2.9 KB (2877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae5b52735eafeede0a1ef84e6d9fd0012298f52c17bc6024ec61289d39fb994`  
		Last Modified: Sat, 19 Mar 2022 04:27:56 GMT  
		Size: 34.2 MB (34160230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d089bea26f35e2412926e3d60813d5f8d202dd1041197930ce5e33eec74f6eba`  
		Last Modified: Sat, 19 Mar 2022 04:27:50 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.21.4-alpine`

```console
$ docker pull telegraf@sha256:cd19eb23a5bfa7fe475cbb119208e6410fd6ad75df19e0d497ff6bcf5ab2e9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:1.21.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:606b358fff99431a02f9bcbea3db5c4ef9464ad3111705075fd8db235139dcdc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43683756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004383a3acac314ec26d30745cdd3ab1c17cadc034dedc1ad0391bd56cec8182`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 17 Mar 2022 04:01:58 GMT
ADD file:cf4b631a115c2bbfbd81cad2d3041bceb64a8136aac92ba8a63b6c51d60af764 in / 
# Thu, 17 Mar 2022 04:01:59 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 15:55:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Mar 2022 15:55:59 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Thu, 17 Mar 2022 15:57:59 GMT
ENV TELEGRAF_VERSION=1.21.4
# Thu, 17 Mar 2022 15:58:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Thu, 17 Mar 2022 15:58:38 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 17 Mar 2022 15:58:38 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Thu, 17 Mar 2022 15:58:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Mar 2022 15:58:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:3d243047344378e9b7136d552d48feb7ea8b6fe14ce0990e0cc011d5e369626a`  
		Last Modified: Thu, 17 Mar 2022 04:02:41 GMT  
		Size: 2.8 MB (2812636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c53ac0d2d7a9a6e5e1fbb7e66008a62369c80becca62a738e68c89542a878c6`  
		Last Modified: Thu, 17 Mar 2022 15:59:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5444d45dfde01b4fbe1e839fb426c861db8ec2678ed06e04deca9e259866b852`  
		Last Modified: Thu, 17 Mar 2022 15:59:09 GMT  
		Size: 3.4 MB (3372396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aac486096e722bec0fedc87784582e9e3da67903a057c33f336d2e656eb5214`  
		Last Modified: Thu, 17 Mar 2022 15:59:49 GMT  
		Size: 37.5 MB (37498244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18762e036fe31460f4b12af0ba3fd23d7c809cfae6fa7517776652d5166998af`  
		Last Modified: Thu, 17 Mar 2022 15:59:43 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:cd19eb23a5bfa7fe475cbb119208e6410fd6ad75df19e0d497ff6bcf5ab2e9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:606b358fff99431a02f9bcbea3db5c4ef9464ad3111705075fd8db235139dcdc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43683756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004383a3acac314ec26d30745cdd3ab1c17cadc034dedc1ad0391bd56cec8182`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 17 Mar 2022 04:01:58 GMT
ADD file:cf4b631a115c2bbfbd81cad2d3041bceb64a8136aac92ba8a63b6c51d60af764 in / 
# Thu, 17 Mar 2022 04:01:59 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 15:55:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 17 Mar 2022 15:55:59 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Thu, 17 Mar 2022 15:57:59 GMT
ENV TELEGRAF_VERSION=1.21.4
# Thu, 17 Mar 2022 15:58:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz.asc telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_static_linux_amd64.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Thu, 17 Mar 2022 15:58:38 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 17 Mar 2022 15:58:38 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Thu, 17 Mar 2022 15:58:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Mar 2022 15:58:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:3d243047344378e9b7136d552d48feb7ea8b6fe14ce0990e0cc011d5e369626a`  
		Last Modified: Thu, 17 Mar 2022 04:02:41 GMT  
		Size: 2.8 MB (2812636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c53ac0d2d7a9a6e5e1fbb7e66008a62369c80becca62a738e68c89542a878c6`  
		Last Modified: Thu, 17 Mar 2022 15:59:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5444d45dfde01b4fbe1e839fb426c861db8ec2678ed06e04deca9e259866b852`  
		Last Modified: Thu, 17 Mar 2022 15:59:09 GMT  
		Size: 3.4 MB (3372396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aac486096e722bec0fedc87784582e9e3da67903a057c33f336d2e656eb5214`  
		Last Modified: Thu, 17 Mar 2022 15:59:49 GMT  
		Size: 37.5 MB (37498244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18762e036fe31460f4b12af0ba3fd23d7c809cfae6fa7517776652d5166998af`  
		Last Modified: Thu, 17 Mar 2022 15:59:43 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:f2b60dc7ca0d3ca72c96d7ecf410d7aff7f565a8e7c0ed8c5da32aa9763c762e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:2e97cb40492427d41c3839aba954a28b58e6409149fee23d78feae66a4896285
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127362512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c094fe86696b7cf134f2f8d080c04bac1a84ddf280a81d07ed693bc391a184`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:15 GMT
ADD file:9c4db2a9644ee3029a8e9cca58350efef660c3167e59b91f2bee9c303e592664 in / 
# Tue, 01 Mar 2022 02:13:15 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 06:25:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 06:26:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 02 Mar 2022 19:10:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 19:10:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 02 Mar 2022 19:11:01 GMT
ENV TELEGRAF_VERSION=1.21.4
# Wed, 02 Mar 2022 19:11:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 02 Mar 2022 19:11:05 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 02 Mar 2022 19:11:05 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Wed, 02 Mar 2022 19:11:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 02 Mar 2022 19:11:05 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e4d61adff2077d048c6372d73c41b0bd68f525ad41f5530af05098a876683055`  
		Last Modified: Tue, 01 Mar 2022 02:18:55 GMT  
		Size: 54.9 MB (54917063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff1945c672b08a1791df62afaaf8aff14d3047155365f9c3646902937f7ffe6`  
		Last Modified: Tue, 01 Mar 2022 06:36:13 GMT  
		Size: 5.2 MB (5153034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5b10aec998344606441aec43a335ab6326f32aae331aab27da16a6bb4ec2be`  
		Last Modified: Tue, 01 Mar 2022 06:36:14 GMT  
		Size: 10.9 MB (10871885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7914280ffd1a89468d7300475f199f63daf36d7d310ca3e2f8a21424b6992e29`  
		Last Modified: Wed, 02 Mar 2022 19:11:29 GMT  
		Size: 18.8 MB (18760097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053949c9b19fa7512f69b5dc25fb96a03488191d90009ce09da1d77a5268b915`  
		Last Modified: Wed, 02 Mar 2022 19:11:25 GMT  
		Size: 2.9 KB (2905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bd08429cefa379c2130c2bbc37cf518e029cc5a580fc133e4555c5717f5488f`  
		Last Modified: Wed, 02 Mar 2022 19:12:06 GMT  
		Size: 37.7 MB (37657184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5eeecdd6b1c66697c0f908b51b00706d683bf323b051139b2592191f33ae176`  
		Last Modified: Wed, 02 Mar 2022 19:11:59 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:87f7a13e248efd9409ceaad9f6cca33f3944c9b7c9b45120678c48ef1a726592
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117652818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a955da099968006b0d86b8a625b1570dcf0d7e3278f78b3520c412ee4de25981`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:17 GMT
ADD file:b388eaef074fa7cc4e0f6f0b6a56e4be6c69489b63477ab4469ff5415074b0c7 in / 
# Tue, 01 Mar 2022 02:02:18 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 09:26:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 09:26:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 03 Mar 2022 00:04:40 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 00:04:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 03 Mar 2022 00:05:45 GMT
ENV TELEGRAF_VERSION=1.21.4
# Thu, 03 Mar 2022 00:05:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 03 Mar 2022 00:05:58 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 03 Mar 2022 00:05:58 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 03 Mar 2022 00:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 03 Mar 2022 00:05:59 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:17a41fc762495ca54ac53f271889bdf4ac8bea7cedfa3b585e4e42ef106935f1`  
		Last Modified: Tue, 01 Mar 2022 02:18:24 GMT  
		Size: 50.1 MB (50117069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9173ee01c42f46f1839650f0a56ee12ab74693f31dacccf586222ef98cb4ec19`  
		Last Modified: Tue, 01 Mar 2022 09:51:00 GMT  
		Size: 4.9 MB (4922642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f119f27841bdc8ee96fe83e4e2bb9b453db5a3a239036547b8e09c87f650befe`  
		Last Modified: Tue, 01 Mar 2022 09:51:01 GMT  
		Size: 10.2 MB (10216974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2baf44ae0880a128f8b5507925605cf1d2d330ad512283e027d0681a97e862`  
		Last Modified: Thu, 03 Mar 2022 00:06:55 GMT  
		Size: 17.5 MB (17462257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ac34fd4d174e3a615b556538c0faf99c0bea701cd679644b8b80bbbdec9614`  
		Last Modified: Thu, 03 Mar 2022 00:06:43 GMT  
		Size: 2.9 KB (2902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78af0ff2764399c5ac4654e7ecf8374d6370f16412b5b965baaef2e93dbe519a`  
		Last Modified: Thu, 03 Mar 2022 00:08:17 GMT  
		Size: 34.9 MB (34930630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764912f088ed42e1b8fec9e5343f19fa630101af941fc597cf0091f230c7a502`  
		Last Modified: Thu, 03 Mar 2022 00:07:52 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:fc25bd2273a71b84b8c80d050a16ca7229fc1b52170cf0e5ce7c4cf587107c38
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121755839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4604947ef10a3a25c9219d40df9589122836c7badf5d83452235ae639209d7f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:41 GMT
ADD file:5effc7e0ab7312f14a7ee81c06c71400aae31219d477ebe1a4f7a9156797c42a in / 
# Thu, 17 Mar 2022 03:21:42 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 22:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 22:11:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 04:25:26 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 04:26:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 19 Mar 2022 04:26:46 GMT
ENV TELEGRAF_VERSION=1.21.4
# Sat, 19 Mar 2022 04:26:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Sat, 19 Mar 2022 04:26:51 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 19 Mar 2022 04:26:52 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Sat, 19 Mar 2022 04:26:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 19 Mar 2022 04:26:53 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:260ad8146ed2447d5587608b10fed4f80de80cdc559e619f3a235d3ba09eaf7b`  
		Last Modified: Thu, 17 Mar 2022 03:28:04 GMT  
		Size: 53.6 MB (53616308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1399f445da611be3789923cf26d158e3f4f80449b7295fa069a8eaecaaf137e6`  
		Last Modified: Thu, 17 Mar 2022 22:20:58 GMT  
		Size: 4.9 MB (4937558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd9e43777fa6c09c341f3aa922f47b5b3ace26de1d779124afd2f1d435731d9`  
		Last Modified: Thu, 17 Mar 2022 22:20:58 GMT  
		Size: 10.7 MB (10655858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab386e029a6d39b09f87391f007c31a225e7d347c44bae2e2fd64a04907880a`  
		Last Modified: Sat, 19 Mar 2022 04:27:19 GMT  
		Size: 18.4 MB (18382667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ddc7d0a6abc23254f7f6f0777da96117b906c81122c629c9c294a6037ef475`  
		Last Modified: Sat, 19 Mar 2022 04:27:15 GMT  
		Size: 2.9 KB (2877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae5b52735eafeede0a1ef84e6d9fd0012298f52c17bc6024ec61289d39fb994`  
		Last Modified: Sat, 19 Mar 2022 04:27:56 GMT  
		Size: 34.2 MB (34160230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d089bea26f35e2412926e3d60813d5f8d202dd1041197930ce5e33eec74f6eba`  
		Last Modified: Sat, 19 Mar 2022 04:27:50 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
