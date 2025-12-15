<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.35`](#telegraf135)
-	[`telegraf:1.35-alpine`](#telegraf135-alpine)
-	[`telegraf:1.35.4`](#telegraf1354)
-	[`telegraf:1.35.4-alpine`](#telegraf1354-alpine)
-	[`telegraf:1.36`](#telegraf136)
-	[`telegraf:1.36-alpine`](#telegraf136-alpine)
-	[`telegraf:1.36.4`](#telegraf1364)
-	[`telegraf:1.36.4-alpine`](#telegraf1364-alpine)
-	[`telegraf:1.37`](#telegraf137)
-	[`telegraf:1.37-alpine`](#telegraf137-alpine)
-	[`telegraf:1.37.0`](#telegraf1370)
-	[`telegraf:1.37.0-alpine`](#telegraf1370-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.35`

```console
$ docker pull telegraf@sha256:bb45d5f558d85ad684b9bd599de36a8d20acca8d9970ecd96d86ae0fbc2697a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35` - linux; amd64

```console
$ docker pull telegraf@sha256:97f7c3e3a8a1f7ecc16380dc43dd0e992368615cc5cbf0a95bbb02ae30f659ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (171027967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2acde9393e8b927437cb33acbf319b5bb10784a57d7de637fd15e26547016788`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:21:05 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:21:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Dec 2025 00:21:09 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 09 Dec 2025 00:21:09 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 09 Dec 2025 00:21:09 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 09 Dec 2025 00:21:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:21:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:21:09 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae8659f7a8d357662281a0f87eb293725bb75ffa6c7356c38567f557d8a1f11`  
		Last Modified: Mon, 08 Dec 2025 23:07:04 GMT  
		Size: 24.0 MB (24029335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af5cd001bdcfbbcbae9eb4b77b3d11c4ae1b3dc9d8944b13bacb98c92aee03c`  
		Last Modified: Tue, 09 Dec 2025 00:21:42 GMT  
		Size: 18.9 MB (18943140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c876ce2648a8c605910faa39b6c38b5f6ab83ad36fa3d04467ce6a9470d05e`  
		Last Modified: Tue, 09 Dec 2025 00:21:40 GMT  
		Size: 3.4 KB (3439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b01a33137f34f514ba3fbb4f85e08d4b4c0fcdabd4361529037a070f2a3e3f`  
		Last Modified: Tue, 09 Dec 2025 00:21:50 GMT  
		Size: 79.6 MB (79570691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf07e6525add5ee667ef98c6d9cd3cafb0314d66bf73f1fc412eece2c7332ee`  
		Last Modified: Tue, 09 Dec 2025 00:21:40 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:72743da3808f373c17401c0817378b56b4bae37f43b74d02cb748f78df1e4427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6659373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dcc5d0ca7d60f50bd280a59c4d8a6cccdb2c6754c0a84b9040d695ca15f6f83`

```dockerfile
```

-	Layers:
	-	`sha256:06adb1dbdc21d849389c4102259e8022f7381bfc21104607c91424dd2ef1a3e7`  
		Last Modified: Tue, 09 Dec 2025 04:11:45 GMT  
		Size: 6.6 MB (6644946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0212fec168832c87832d0dd3c2928b9fd926e4715ef7c015b7197a8cba3dd694`  
		Last Modified: Tue, 09 Dec 2025 04:11:46 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:e63ae102c8310ff29af1e2d95e0263b201444a86c36442f925e497472361fa39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157148068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48cac5c7b69a6a1be1d6e5f26d398016125fc2df42a119a975547aa35334a380`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:04:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:48:23 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:48:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Dec 2025 01:48:29 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 09 Dec 2025 01:48:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 09 Dec 2025 01:48:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 09 Dec 2025 01:48:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 01:48:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 01:48:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c3d6a83e736aa77820543663b2d6579ddd98b0f465c0fcad8aa9bd98a5b72a9c`  
		Last Modified: Mon, 08 Dec 2025 22:16:46 GMT  
		Size: 44.2 MB (44196066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0a258ea9a718fb1bf2331996816ba335715a3c786bd79934d265fd78fb7f5a`  
		Last Modified: Tue, 09 Dec 2025 00:05:11 GMT  
		Size: 21.9 MB (21934635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3698bb5b910c62a3f2c561f3d13a35229bb36cf1e642e4071ddd5e5f62a01bb8`  
		Last Modified: Tue, 09 Dec 2025 01:48:57 GMT  
		Size: 17.7 MB (17722586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9968fb6a2394ae587886368b7b664660af3f0803e242ea72c6b46f2db5123573`  
		Last Modified: Tue, 09 Dec 2025 01:48:55 GMT  
		Size: 3.4 KB (3443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93796631f56e737e559004d892819937768187ad0d204cae677f1c9c0a5afd37`  
		Last Modified: Tue, 09 Dec 2025 01:49:02 GMT  
		Size: 73.3 MB (73290713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0844f0c17180492c2e3df6aa0aca24edb8eca41900a2d73ca8aa85238be18330`  
		Last Modified: Tue, 09 Dec 2025 01:48:55 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:44ca05577180c5ee712922db1d09fb22b50ee904de6b58d7a112aa5bc6e6ee06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6654060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fe2d3a544ee6c678b4c0aa3cb4901fe1ceb82323df421cefffc8670a6153c1`

```dockerfile
```

-	Layers:
	-	`sha256:1d94511cbeadc9ce9293ddbeb44626d80bdc6f74d304710427b9c031468b9fcc`  
		Last Modified: Tue, 09 Dec 2025 04:11:52 GMT  
		Size: 6.6 MB (6639543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:590d78319ccb3a3a26221fefb023698024f496781a255c429f26bf5ad43a70da`  
		Last Modified: Tue, 09 Dec 2025 04:11:53 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:f1248c75ce2798ec2b94d130f0870af37592cceb6f91fa346210db7814312347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162925258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c0a69415d4797395a98b2dc82d18e8d70348861c8d696f0579c462192e4fb0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:10:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:28:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:28:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Dec 2025 00:28:05 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 09 Dec 2025 00:28:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 09 Dec 2025 00:28:05 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 09 Dec 2025 00:28:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:28:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:28:05 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0da1fc24a51c3ab23b5143a2c67b43348114c11a8029b3483be57ab9fe54eb6`  
		Last Modified: Mon, 08 Dec 2025 23:10:26 GMT  
		Size: 23.6 MB (23598247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d112e16783accfc7fbca2b893435c99f7a6b8c782c783d78243ceaae5898d177`  
		Last Modified: Tue, 09 Dec 2025 00:28:31 GMT  
		Size: 18.9 MB (18884480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51eabf51a0a70b47455d99648fd3f3163dd14282ff0cc0915f188d740fc5c585`  
		Last Modified: Tue, 09 Dec 2025 00:28:33 GMT  
		Size: 3.5 KB (3451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6354e03b2c9ce4f85e2259f7db4194d27237882502beb688c9cc08f055f52ac8`  
		Last Modified: Tue, 09 Dec 2025 00:28:35 GMT  
		Size: 72.1 MB (72079385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc63bfd8923205f84e7a55b8572afb92ee069c4359534b390563907a425fe6a`  
		Last Modified: Tue, 09 Dec 2025 00:28:30 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35` - unknown; unknown

```console
$ docker pull telegraf@sha256:403a8a96a0c0866740293b7ec8d22d347fbd3404d6c9fa3762377efd86dc2b24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26f9b49e91e4376719c38d216b48ccb5274c70fe4312ba4f19865ca1428427a6`

```dockerfile
```

-	Layers:
	-	`sha256:9af21c538f109acf7d36311cb87811e8b05305bf582db0832250a371a9019f63`  
		Last Modified: Tue, 09 Dec 2025 04:11:58 GMT  
		Size: 6.6 MB (6645622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f3dd1b16aa8764ed7507a0968cd2c6196c4251b542c63eb4f7a2a6bd1011745`  
		Last Modified: Tue, 09 Dec 2025 04:11:59 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35-alpine`

```console
$ docker pull telegraf@sha256:07f7dcf2b3827f051657569751cb64d5faff3e5a72a868693ffb9120e8235879
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:218877c5f874e303ce9eff463bd641cd6524d5cb4bf594a918719ce7cb049492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85735517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c39d7be492e6591caa8ad4bed3b416b8e1b0012dabf4da111f2a659a79b3111`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Sep 2025 19:18:27 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.35.4
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 29 Sep 2025 19:18:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccca5a3c76061483f8823e5d77dd23416fdb6c1db125a11118301458c29897c`  
		Last Modified: Mon, 08 Dec 2025 00:08:06 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2332823178d0061e80a1f95c48765dbaf18df2dd31878bac57f31fc7e9a9feeb`  
		Last Modified: Mon, 08 Dec 2025 00:08:07 GMT  
		Size: 2.6 MB (2563472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251b8f38f4c764d714567e5ca660283254c5c1f76d6a3eb579385593c3db441f`  
		Last Modified: Mon, 08 Dec 2025 01:56:53 GMT  
		Size: 79.4 MB (79368696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2523c7a219f6fba7e1e9fd8f9a81fbc8fb21f84c41aa6b03e5f001f54fa7d4f`  
		Last Modified: Mon, 08 Dec 2025 00:08:07 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:d5f21a0772915320f389bebe6d06e7068c9cfb1211b785a9b3f6333c50c294c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1148969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc15951201cadcadb797550a067ab3695eb31ecadbb317a8dbb86766c39fb43f`

```dockerfile
```

-	Layers:
	-	`sha256:f609b510765575f46fd07751df9253b9e0bef412ef4d52e9f96a165469460ed0`  
		Last Modified: Fri, 12 Dec 2025 13:09:25 GMT  
		Size: 1.1 MB (1134008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85b8d9f56ca4b6828b99375d962b74da6a704fd9f3bb65cb4e937fc29576512b`  
		Last Modified: Fri, 12 Dec 2025 13:09:24 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:2dc98b18a3b682b4d47915f648c59570b29ce00624355c476e03ec8b7437e844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78643760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a73c4abccf0bdf3e9ed8b9eb7c3415a9215de1a7580eefdf2b21df5e598d2ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Sep 2025 19:18:27 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.35.4
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 29 Sep 2025 19:18:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb651d889db2dee7911408fa57f1d7539c6e6d834e35cef0953d16bae75bf92b`  
		Last Modified: Mon, 08 Dec 2025 11:40:45 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d79a0d11e911af062cf834a3903c2474ae8e732b43633aba958f2e6ad1016b9`  
		Last Modified: Mon, 08 Dec 2025 11:40:46 GMT  
		Size: 2.6 MB (2627489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564facf9ae36962cd5148a9e7a58a23d64ee343b817bdf79fbe0febc06402a3c`  
		Last Modified: Mon, 08 Dec 2025 11:40:48 GMT  
		Size: 71.9 MB (71877304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1f7ca04417cf2ffd90adfbbaee47bb81f8f7ebd0b7537bfd13f76b41d9bf2c`  
		Last Modified: Mon, 08 Dec 2025 11:40:45 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4753dbe48b97e81e45692abc4a4cc8c2bea6375210f9d3db090253c6327d3b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1144706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ef814572f43a3f8c71c902f5ec20cd44a4e27fb3aa10c609a6532bf95e196a`

```dockerfile
```

-	Layers:
	-	`sha256:eb88913d7607490638a82238d8cb692ac25949af926c0aae25a744e853aec341`  
		Last Modified: Mon, 15 Dec 2025 16:08:52 GMT  
		Size: 1.1 MB (1129635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5a5c5dcdefea06875f2d3c71b915b1573aa37fde54d0649aa9189ca1bc85d5a`  
		Last Modified: Mon, 15 Dec 2025 16:08:52 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35.4`

```console
$ docker pull telegraf@sha256:bb45d5f558d85ad684b9bd599de36a8d20acca8d9970ecd96d86ae0fbc2697a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35.4` - linux; amd64

```console
$ docker pull telegraf@sha256:97f7c3e3a8a1f7ecc16380dc43dd0e992368615cc5cbf0a95bbb02ae30f659ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (171027967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2acde9393e8b927437cb33acbf319b5bb10784a57d7de637fd15e26547016788`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:21:05 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:21:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Dec 2025 00:21:09 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 09 Dec 2025 00:21:09 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 09 Dec 2025 00:21:09 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 09 Dec 2025 00:21:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:21:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:21:09 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae8659f7a8d357662281a0f87eb293725bb75ffa6c7356c38567f557d8a1f11`  
		Last Modified: Mon, 08 Dec 2025 23:07:04 GMT  
		Size: 24.0 MB (24029335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af5cd001bdcfbbcbae9eb4b77b3d11c4ae1b3dc9d8944b13bacb98c92aee03c`  
		Last Modified: Tue, 09 Dec 2025 00:21:42 GMT  
		Size: 18.9 MB (18943140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c876ce2648a8c605910faa39b6c38b5f6ab83ad36fa3d04467ce6a9470d05e`  
		Last Modified: Tue, 09 Dec 2025 00:21:40 GMT  
		Size: 3.4 KB (3439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b01a33137f34f514ba3fbb4f85e08d4b4c0fcdabd4361529037a070f2a3e3f`  
		Last Modified: Tue, 09 Dec 2025 00:21:50 GMT  
		Size: 79.6 MB (79570691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf07e6525add5ee667ef98c6d9cd3cafb0314d66bf73f1fc412eece2c7332ee`  
		Last Modified: Tue, 09 Dec 2025 00:21:40 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:72743da3808f373c17401c0817378b56b4bae37f43b74d02cb748f78df1e4427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6659373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dcc5d0ca7d60f50bd280a59c4d8a6cccdb2c6754c0a84b9040d695ca15f6f83`

```dockerfile
```

-	Layers:
	-	`sha256:06adb1dbdc21d849389c4102259e8022f7381bfc21104607c91424dd2ef1a3e7`  
		Last Modified: Tue, 09 Dec 2025 04:11:45 GMT  
		Size: 6.6 MB (6644946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0212fec168832c87832d0dd3c2928b9fd926e4715ef7c015b7197a8cba3dd694`  
		Last Modified: Tue, 09 Dec 2025 04:11:46 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:e63ae102c8310ff29af1e2d95e0263b201444a86c36442f925e497472361fa39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157148068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48cac5c7b69a6a1be1d6e5f26d398016125fc2df42a119a975547aa35334a380`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:04:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:48:23 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:48:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Dec 2025 01:48:29 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 09 Dec 2025 01:48:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 09 Dec 2025 01:48:29 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 09 Dec 2025 01:48:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 01:48:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 01:48:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c3d6a83e736aa77820543663b2d6579ddd98b0f465c0fcad8aa9bd98a5b72a9c`  
		Last Modified: Mon, 08 Dec 2025 22:16:46 GMT  
		Size: 44.2 MB (44196066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0a258ea9a718fb1bf2331996816ba335715a3c786bd79934d265fd78fb7f5a`  
		Last Modified: Tue, 09 Dec 2025 00:05:11 GMT  
		Size: 21.9 MB (21934635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3698bb5b910c62a3f2c561f3d13a35229bb36cf1e642e4071ddd5e5f62a01bb8`  
		Last Modified: Tue, 09 Dec 2025 01:48:57 GMT  
		Size: 17.7 MB (17722586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9968fb6a2394ae587886368b7b664660af3f0803e242ea72c6b46f2db5123573`  
		Last Modified: Tue, 09 Dec 2025 01:48:55 GMT  
		Size: 3.4 KB (3443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93796631f56e737e559004d892819937768187ad0d204cae677f1c9c0a5afd37`  
		Last Modified: Tue, 09 Dec 2025 01:49:02 GMT  
		Size: 73.3 MB (73290713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0844f0c17180492c2e3df6aa0aca24edb8eca41900a2d73ca8aa85238be18330`  
		Last Modified: Tue, 09 Dec 2025 01:48:55 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:44ca05577180c5ee712922db1d09fb22b50ee904de6b58d7a112aa5bc6e6ee06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6654060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fe2d3a544ee6c678b4c0aa3cb4901fe1ceb82323df421cefffc8670a6153c1`

```dockerfile
```

-	Layers:
	-	`sha256:1d94511cbeadc9ce9293ddbeb44626d80bdc6f74d304710427b9c031468b9fcc`  
		Last Modified: Tue, 09 Dec 2025 04:11:52 GMT  
		Size: 6.6 MB (6639543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:590d78319ccb3a3a26221fefb023698024f496781a255c429f26bf5ad43a70da`  
		Last Modified: Tue, 09 Dec 2025 04:11:53 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:f1248c75ce2798ec2b94d130f0870af37592cceb6f91fa346210db7814312347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162925258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c0a69415d4797395a98b2dc82d18e8d70348861c8d696f0579c462192e4fb0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:10:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:28:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:28:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Dec 2025 00:28:05 GMT
ENV TELEGRAF_VERSION=1.35.4
# Tue, 09 Dec 2025 00:28:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 09 Dec 2025 00:28:05 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 09 Dec 2025 00:28:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:28:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:28:05 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0da1fc24a51c3ab23b5143a2c67b43348114c11a8029b3483be57ab9fe54eb6`  
		Last Modified: Mon, 08 Dec 2025 23:10:26 GMT  
		Size: 23.6 MB (23598247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d112e16783accfc7fbca2b893435c99f7a6b8c782c783d78243ceaae5898d177`  
		Last Modified: Tue, 09 Dec 2025 00:28:31 GMT  
		Size: 18.9 MB (18884480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51eabf51a0a70b47455d99648fd3f3163dd14282ff0cc0915f188d740fc5c585`  
		Last Modified: Tue, 09 Dec 2025 00:28:33 GMT  
		Size: 3.5 KB (3451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6354e03b2c9ce4f85e2259f7db4194d27237882502beb688c9cc08f055f52ac8`  
		Last Modified: Tue, 09 Dec 2025 00:28:35 GMT  
		Size: 72.1 MB (72079385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc63bfd8923205f84e7a55b8572afb92ee069c4359534b390563907a425fe6a`  
		Last Modified: Tue, 09 Dec 2025 00:28:30 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:403a8a96a0c0866740293b7ec8d22d347fbd3404d6c9fa3762377efd86dc2b24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26f9b49e91e4376719c38d216b48ccb5274c70fe4312ba4f19865ca1428427a6`

```dockerfile
```

-	Layers:
	-	`sha256:9af21c538f109acf7d36311cb87811e8b05305bf582db0832250a371a9019f63`  
		Last Modified: Tue, 09 Dec 2025 04:11:58 GMT  
		Size: 6.6 MB (6645622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f3dd1b16aa8764ed7507a0968cd2c6196c4251b542c63eb4f7a2a6bd1011745`  
		Last Modified: Tue, 09 Dec 2025 04:11:59 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.35.4-alpine`

```console
$ docker pull telegraf@sha256:07f7dcf2b3827f051657569751cb64d5faff3e5a72a868693ffb9120e8235879
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.35.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:218877c5f874e303ce9eff463bd641cd6524d5cb4bf594a918719ce7cb049492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85735517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c39d7be492e6591caa8ad4bed3b416b8e1b0012dabf4da111f2a659a79b3111`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Sep 2025 19:18:27 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.35.4
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 29 Sep 2025 19:18:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fccca5a3c76061483f8823e5d77dd23416fdb6c1db125a11118301458c29897c`  
		Last Modified: Mon, 08 Dec 2025 00:08:06 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2332823178d0061e80a1f95c48765dbaf18df2dd31878bac57f31fc7e9a9feeb`  
		Last Modified: Mon, 08 Dec 2025 00:08:07 GMT  
		Size: 2.6 MB (2563472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251b8f38f4c764d714567e5ca660283254c5c1f76d6a3eb579385593c3db441f`  
		Last Modified: Mon, 08 Dec 2025 01:56:53 GMT  
		Size: 79.4 MB (79368696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2523c7a219f6fba7e1e9fd8f9a81fbc8fb21f84c41aa6b03e5f001f54fa7d4f`  
		Last Modified: Mon, 08 Dec 2025 00:08:07 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:d5f21a0772915320f389bebe6d06e7068c9cfb1211b785a9b3f6333c50c294c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1148969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc15951201cadcadb797550a067ab3695eb31ecadbb317a8dbb86766c39fb43f`

```dockerfile
```

-	Layers:
	-	`sha256:f609b510765575f46fd07751df9253b9e0bef412ef4d52e9f96a165469460ed0`  
		Last Modified: Fri, 12 Dec 2025 13:09:25 GMT  
		Size: 1.1 MB (1134008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85b8d9f56ca4b6828b99375d962b74da6a704fd9f3bb65cb4e937fc29576512b`  
		Last Modified: Fri, 12 Dec 2025 13:09:24 GMT  
		Size: 15.0 KB (14961 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.35.4-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:2dc98b18a3b682b4d47915f648c59570b29ce00624355c476e03ec8b7437e844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78643760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a73c4abccf0bdf3e9ed8b9eb7c3415a9215de1a7580eefdf2b21df5e598d2ed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 29 Sep 2025 19:18:27 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["/bin/sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENV TELEGRAF_VERSION=1.35.4
# Mon, 29 Sep 2025 19:18:27 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 29 Sep 2025 19:18:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 29 Sep 2025 19:18:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 29 Sep 2025 19:18:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb651d889db2dee7911408fa57f1d7539c6e6d834e35cef0953d16bae75bf92b`  
		Last Modified: Mon, 08 Dec 2025 11:40:45 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d79a0d11e911af062cf834a3903c2474ae8e732b43633aba958f2e6ad1016b9`  
		Last Modified: Mon, 08 Dec 2025 11:40:46 GMT  
		Size: 2.6 MB (2627489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:564facf9ae36962cd5148a9e7a58a23d64ee343b817bdf79fbe0febc06402a3c`  
		Last Modified: Mon, 08 Dec 2025 11:40:48 GMT  
		Size: 71.9 MB (71877304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1f7ca04417cf2ffd90adfbbaee47bb81f8f7ebd0b7537bfd13f76b41d9bf2c`  
		Last Modified: Mon, 08 Dec 2025 11:40:45 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.35.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:4753dbe48b97e81e45692abc4a4cc8c2bea6375210f9d3db090253c6327d3b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1144706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ef814572f43a3f8c71c902f5ec20cd44a4e27fb3aa10c609a6532bf95e196a`

```dockerfile
```

-	Layers:
	-	`sha256:eb88913d7607490638a82238d8cb692ac25949af926c0aae25a744e853aec341`  
		Last Modified: Mon, 15 Dec 2025 16:08:52 GMT  
		Size: 1.1 MB (1129635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5a5c5dcdefea06875f2d3c71b915b1573aa37fde54d0649aa9189ca1bc85d5a`  
		Last Modified: Mon, 15 Dec 2025 16:08:52 GMT  
		Size: 15.1 KB (15071 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36`

```console
$ docker pull telegraf@sha256:b8b8e95a75820aabc7f100e9343964353cb050c572641f02ce211e28c0277a29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36` - linux; amd64

```console
$ docker pull telegraf@sha256:365856b588341e5f35777c34ad6e7ba56812eb06672eca57392771698d1a61f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171930651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2834a51ece7ef228aefce6736909089df10ad9c65ca2f94860dfd616b19b79b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:21:30 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:21:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Dec 2025 00:21:34 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 09 Dec 2025 00:21:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 09 Dec 2025 00:21:34 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 09 Dec 2025 00:21:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:21:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:21:34 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae8659f7a8d357662281a0f87eb293725bb75ffa6c7356c38567f557d8a1f11`  
		Last Modified: Mon, 08 Dec 2025 23:07:04 GMT  
		Size: 24.0 MB (24029335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01875e8f567304a636b919efe948aaa1b9d7bd7b122bee2bfd5db92e70bf8099`  
		Last Modified: Tue, 09 Dec 2025 00:22:06 GMT  
		Size: 18.9 MB (18943015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdcd8d16ee8d5ab3e69a3246782d6c677b8a3662bf0d5aa3303d88195cf2124`  
		Last Modified: Tue, 09 Dec 2025 00:22:07 GMT  
		Size: 3.4 KB (3440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458ae7498890fef89232acadfdb6f057aed3a71383e12cf441d657701a83b3f7`  
		Last Modified: Tue, 09 Dec 2025 00:22:20 GMT  
		Size: 80.5 MB (80473502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8370d25a290d6360ee91e5bac69dbbf29b198125a6a986200a9ba262058464`  
		Last Modified: Tue, 09 Dec 2025 00:22:05 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:3932fc57664f9630af51b7db0757313dd2fec5cc9a5ff46c0348ea2659fe8f25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6667673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7232d8070afdb3f3c5e564bb2ba4f5f431b1876e10cd3a3a6d9b41d40b1bc83`

```dockerfile
```

-	Layers:
	-	`sha256:9eb236958014372fd0e896c8966313db3845b080e7031b54605ad80c8b1f7ef5`  
		Last Modified: Tue, 09 Dec 2025 04:12:01 GMT  
		Size: 6.7 MB (6653246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc3fe32e2c60aa15d91ffd49186a86bdca3ef1c802a0ff3368bfa110c32b0781`  
		Last Modified: Tue, 09 Dec 2025 04:12:02 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:70a76584520b9722366dc262f4d036dc5e90bc4bf732e4af501fc1a3a38855e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157820802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11e02fe678aff8baa1b96ae7de2d0b5668cff1ec8ad14926dd14c69f2f69446b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:04:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:48:25 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:48:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Dec 2025 01:48:32 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 09 Dec 2025 01:48:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 09 Dec 2025 01:48:32 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 09 Dec 2025 01:48:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 01:48:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 01:48:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c3d6a83e736aa77820543663b2d6579ddd98b0f465c0fcad8aa9bd98a5b72a9c`  
		Last Modified: Mon, 08 Dec 2025 22:16:46 GMT  
		Size: 44.2 MB (44196066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0a258ea9a718fb1bf2331996816ba335715a3c786bd79934d265fd78fb7f5a`  
		Last Modified: Tue, 09 Dec 2025 00:05:11 GMT  
		Size: 21.9 MB (21934635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ec99a3f7601f805b52915430f02906f9ba871a3c9d45f9929ec44ade4192eb`  
		Last Modified: Tue, 09 Dec 2025 01:48:57 GMT  
		Size: 17.7 MB (17722507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a2814eaf0d6f7129d7d298c19e912ab167f201c749b3cd0e936e657725c37b`  
		Last Modified: Tue, 09 Dec 2025 01:49:04 GMT  
		Size: 3.4 KB (3444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f4d520629862d1187ead094b20139ace3fbb20c52b7aedadd8b84ce31b3465`  
		Last Modified: Tue, 09 Dec 2025 01:49:03 GMT  
		Size: 74.0 MB (73963528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852b7e849287d55f437e16a6910a0ed4c9f1dc61cdec97048668dfdb4e0f19ba`  
		Last Modified: Tue, 09 Dec 2025 01:48:56 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:157e33da935a7867778942275f00c2e2cf85ef8250dd883e46b456d66ff96226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05849a65e4391d54948f6800a041e93b5d587e5aeb80e060cd06c4d7f401ff7`

```dockerfile
```

-	Layers:
	-	`sha256:a7123a65eb90a5206836922da248dc7f5115e732e7eca6ec4889245114b144c5`  
		Last Modified: Tue, 09 Dec 2025 04:12:08 GMT  
		Size: 6.6 MB (6647843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bd2cec832812d0fd35ebe6871e4329757d052394a767f55b8e0777474f1bac6`  
		Last Modified: Tue, 09 Dec 2025 04:12:09 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:8a07b42c03278c156bc4348e64c1a85be7f73b9bcbdc63702cd6671cb8a41bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162646301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8345ecf0a86fd1ff463e23d414a415e9b9c62f77257ab5c61998ecfd3f1d97`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:10:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:28:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:28:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Dec 2025 00:28:05 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 09 Dec 2025 00:28:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 09 Dec 2025 00:28:05 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 09 Dec 2025 00:28:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:28:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:28:05 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0da1fc24a51c3ab23b5143a2c67b43348114c11a8029b3483be57ab9fe54eb6`  
		Last Modified: Mon, 08 Dec 2025 23:10:26 GMT  
		Size: 23.6 MB (23598247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0971ff3d94ef68860c6e3f09270a698ffc2675ce521ce8b151161cc32389b1f1`  
		Last Modified: Tue, 09 Dec 2025 00:28:37 GMT  
		Size: 18.9 MB (18884593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df041d0f7645d69298a669a53a2eeed1cf59e35cbe9a2f53a77c14168556635b`  
		Last Modified: Tue, 09 Dec 2025 00:28:36 GMT  
		Size: 3.4 KB (3441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edba92a797658f268ddfd02b95ed8216034c9bfccb11ff710b32bf66e5384e4`  
		Last Modified: Tue, 09 Dec 2025 00:28:41 GMT  
		Size: 71.8 MB (71800325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc63bfd8923205f84e7a55b8572afb92ee069c4359534b390563907a425fe6a`  
		Last Modified: Tue, 09 Dec 2025 00:28:30 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:f3db500fdbddc1aaa33b101a7ecdf7e67cc54d1f4798e7c0055c68df9ab612b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6668459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e774a37987b8a9d84444c5add9f747e2167a367f6422b3eb571c8a3713cc6a`

```dockerfile
```

-	Layers:
	-	`sha256:68b8c083e80f22df3dae676dfb79d2ecf1862b0b721338470f9f2337f5a16f40`  
		Last Modified: Tue, 09 Dec 2025 04:12:14 GMT  
		Size: 6.7 MB (6653922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:955c48ff7de3a34eec555bfaefc96d239150ac74673d14f8c1ae30d182bec5a5`  
		Last Modified: Tue, 09 Dec 2025 04:12:15 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36-alpine`

```console
$ docker pull telegraf@sha256:46cabb477e6e31268bad42966facd2d52c22561d3cfc8d4b0c112b5728ba2c19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:48407b552b16c564ccc47bae44b45ab122d4f48a5bd67d75735d24f586e3f124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86642882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0280f08a3c4aeff01bdbeb32bbf32ce8225d3a92ce6199bdfdfabb565fdee4f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 17 Nov 2025 18:59:59 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 17 Nov 2025 19:00:00 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 17 Nov 2025 19:00:08 GMT
ENV TELEGRAF_VERSION=1.36.4
# Mon, 17 Nov 2025 19:00:08 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 17 Nov 2025 19:00:08 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 17 Nov 2025 19:00:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 17 Nov 2025 19:00:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 17 Nov 2025 19:00:08 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb344b979ef9e3d6ea2f360ff66a3139d4cfcd9b863983621de8eefe5cd84aa6`  
		Last Modified: Mon, 17 Nov 2025 19:00:31 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5696b9b7585c20f57f20c3c7c460662abb184e8eab21a8d4cafd61afc3077a9f`  
		Last Modified: Mon, 17 Nov 2025 19:00:32 GMT  
		Size: 2.6 MB (2563494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff853a04372dd9d1360ee371deb684033ada876ca3c1a38e2d67fe3c5f992aba`  
		Last Modified: Mon, 17 Nov 2025 19:12:22 GMT  
		Size: 80.3 MB (80276038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21db64bfe323b246d3e17e70370a071cbe6e04b604f006cafc7c552ae2a84a58`  
		Last Modified: Mon, 17 Nov 2025 19:00:32 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c9db14f5b6e1db85cf120f8325e5c21fb4b6bc3952dec26a4da8e31845827cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1157830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d50f7a3066665cbeb8c985217e41c9d2c2f556ea806eb93be6998e153351815`

```dockerfile
```

-	Layers:
	-	`sha256:d104164b2bcc3c30f646afbdfb9f7942e9d74e4e2e583067261c32c2602a9f20`  
		Last Modified: Mon, 17 Nov 2025 19:10:34 GMT  
		Size: 1.1 MB (1142610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4946291a4533c865cd6bb8bff0320c5aa46fefdae9cb144749cee928ced7711d`  
		Last Modified: Mon, 17 Nov 2025 19:10:35 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:4d49d49f81612798363550052fd65d73706db1548e68e0f38576322706f00ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78365616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e73a3d881177da588f763fcd0ab17af8d7f22d8dbad194af635b0bae1274cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 17 Nov 2025 19:02:16 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 17 Nov 2025 19:02:18 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 17 Nov 2025 19:02:26 GMT
ENV TELEGRAF_VERSION=1.36.4
# Mon, 17 Nov 2025 19:02:26 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 17 Nov 2025 19:02:26 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 17 Nov 2025 19:02:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 17 Nov 2025 19:02:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 17 Nov 2025 19:02:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e686dad26a4c7f703dc366e1e60b14ae44807c190f97f04760640bb32361676`  
		Last Modified: Mon, 17 Nov 2025 19:02:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d3b38a4228f7da2c38dea9114166ad90b746642df4747865aa32a613fe8247`  
		Last Modified: Mon, 17 Nov 2025 19:02:48 GMT  
		Size: 2.6 MB (2627506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bca33979b5e4d10e8626da8ae6b21afab00ccbeef50beaf1bcd0ad868b8ce7`  
		Last Modified: Mon, 17 Nov 2025 19:02:55 GMT  
		Size: 71.6 MB (71599144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bfa9ad7ce4e4f025b9cfab73b412dc8c04760d6c3ace7fa607998ad9813725`  
		Last Modified: Mon, 17 Nov 2025 19:02:48 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:b73f976d36f57759d14866b99041351f2aeb2a0facca4b270cf46c7645d8b4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1153591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85106f70e2bf1311bea0e40536625bd137213ea7b96647b802c77c659d7b1b43`

```dockerfile
```

-	Layers:
	-	`sha256:0e40d6658c33f56500ab6ae63559dc1c965812fc29e9404fd354af08b46bc679`  
		Last Modified: Mon, 17 Nov 2025 19:10:39 GMT  
		Size: 1.1 MB (1138249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1b269496aa7a00647a4b8e38da5384d0924c563e868cab39620498cdc13c489`  
		Last Modified: Mon, 17 Nov 2025 19:10:40 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36.4`

```console
$ docker pull telegraf@sha256:b8b8e95a75820aabc7f100e9343964353cb050c572641f02ce211e28c0277a29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36.4` - linux; amd64

```console
$ docker pull telegraf@sha256:365856b588341e5f35777c34ad6e7ba56812eb06672eca57392771698d1a61f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171930651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2834a51ece7ef228aefce6736909089df10ad9c65ca2f94860dfd616b19b79b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:21:30 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:21:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Dec 2025 00:21:34 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 09 Dec 2025 00:21:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 09 Dec 2025 00:21:34 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 09 Dec 2025 00:21:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:21:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:21:34 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae8659f7a8d357662281a0f87eb293725bb75ffa6c7356c38567f557d8a1f11`  
		Last Modified: Mon, 08 Dec 2025 23:07:04 GMT  
		Size: 24.0 MB (24029335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01875e8f567304a636b919efe948aaa1b9d7bd7b122bee2bfd5db92e70bf8099`  
		Last Modified: Tue, 09 Dec 2025 00:22:06 GMT  
		Size: 18.9 MB (18943015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebdcd8d16ee8d5ab3e69a3246782d6c677b8a3662bf0d5aa3303d88195cf2124`  
		Last Modified: Tue, 09 Dec 2025 00:22:07 GMT  
		Size: 3.4 KB (3440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458ae7498890fef89232acadfdb6f057aed3a71383e12cf441d657701a83b3f7`  
		Last Modified: Tue, 09 Dec 2025 00:22:20 GMT  
		Size: 80.5 MB (80473502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b8370d25a290d6360ee91e5bac69dbbf29b198125a6a986200a9ba262058464`  
		Last Modified: Tue, 09 Dec 2025 00:22:05 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:3932fc57664f9630af51b7db0757313dd2fec5cc9a5ff46c0348ea2659fe8f25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6667673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7232d8070afdb3f3c5e564bb2ba4f5f431b1876e10cd3a3a6d9b41d40b1bc83`

```dockerfile
```

-	Layers:
	-	`sha256:9eb236958014372fd0e896c8966313db3845b080e7031b54605ad80c8b1f7ef5`  
		Last Modified: Tue, 09 Dec 2025 04:12:01 GMT  
		Size: 6.7 MB (6653246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc3fe32e2c60aa15d91ffd49186a86bdca3ef1c802a0ff3368bfa110c32b0781`  
		Last Modified: Tue, 09 Dec 2025 04:12:02 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:70a76584520b9722366dc262f4d036dc5e90bc4bf732e4af501fc1a3a38855e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157820802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11e02fe678aff8baa1b96ae7de2d0b5668cff1ec8ad14926dd14c69f2f69446b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:04:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:48:25 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:48:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Dec 2025 01:48:32 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 09 Dec 2025 01:48:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 09 Dec 2025 01:48:32 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 09 Dec 2025 01:48:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 01:48:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 01:48:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c3d6a83e736aa77820543663b2d6579ddd98b0f465c0fcad8aa9bd98a5b72a9c`  
		Last Modified: Mon, 08 Dec 2025 22:16:46 GMT  
		Size: 44.2 MB (44196066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0a258ea9a718fb1bf2331996816ba335715a3c786bd79934d265fd78fb7f5a`  
		Last Modified: Tue, 09 Dec 2025 00:05:11 GMT  
		Size: 21.9 MB (21934635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ec99a3f7601f805b52915430f02906f9ba871a3c9d45f9929ec44ade4192eb`  
		Last Modified: Tue, 09 Dec 2025 01:48:57 GMT  
		Size: 17.7 MB (17722507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a2814eaf0d6f7129d7d298c19e912ab167f201c749b3cd0e936e657725c37b`  
		Last Modified: Tue, 09 Dec 2025 01:49:04 GMT  
		Size: 3.4 KB (3444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f4d520629862d1187ead094b20139ace3fbb20c52b7aedadd8b84ce31b3465`  
		Last Modified: Tue, 09 Dec 2025 01:49:03 GMT  
		Size: 74.0 MB (73963528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852b7e849287d55f437e16a6910a0ed4c9f1dc61cdec97048668dfdb4e0f19ba`  
		Last Modified: Tue, 09 Dec 2025 01:48:56 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:157e33da935a7867778942275f00c2e2cf85ef8250dd883e46b456d66ff96226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6662360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05849a65e4391d54948f6800a041e93b5d587e5aeb80e060cd06c4d7f401ff7`

```dockerfile
```

-	Layers:
	-	`sha256:a7123a65eb90a5206836922da248dc7f5115e732e7eca6ec4889245114b144c5`  
		Last Modified: Tue, 09 Dec 2025 04:12:08 GMT  
		Size: 6.6 MB (6647843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bd2cec832812d0fd35ebe6871e4329757d052394a767f55b8e0777474f1bac6`  
		Last Modified: Tue, 09 Dec 2025 04:12:09 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:8a07b42c03278c156bc4348e64c1a85be7f73b9bcbdc63702cd6671cb8a41bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162646301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8345ecf0a86fd1ff463e23d414a415e9b9c62f77257ab5c61998ecfd3f1d97`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:10:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:28:01 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:28:01 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Dec 2025 00:28:05 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 09 Dec 2025 00:28:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 09 Dec 2025 00:28:05 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 09 Dec 2025 00:28:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:28:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:28:05 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0da1fc24a51c3ab23b5143a2c67b43348114c11a8029b3483be57ab9fe54eb6`  
		Last Modified: Mon, 08 Dec 2025 23:10:26 GMT  
		Size: 23.6 MB (23598247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0971ff3d94ef68860c6e3f09270a698ffc2675ce521ce8b151161cc32389b1f1`  
		Last Modified: Tue, 09 Dec 2025 00:28:37 GMT  
		Size: 18.9 MB (18884593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df041d0f7645d69298a669a53a2eeed1cf59e35cbe9a2f53a77c14168556635b`  
		Last Modified: Tue, 09 Dec 2025 00:28:36 GMT  
		Size: 3.4 KB (3441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edba92a797658f268ddfd02b95ed8216034c9bfccb11ff710b32bf66e5384e4`  
		Last Modified: Tue, 09 Dec 2025 00:28:41 GMT  
		Size: 71.8 MB (71800325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc63bfd8923205f84e7a55b8572afb92ee069c4359534b390563907a425fe6a`  
		Last Modified: Tue, 09 Dec 2025 00:28:30 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:f3db500fdbddc1aaa33b101a7ecdf7e67cc54d1f4798e7c0055c68df9ab612b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6668459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e774a37987b8a9d84444c5add9f747e2167a367f6422b3eb571c8a3713cc6a`

```dockerfile
```

-	Layers:
	-	`sha256:68b8c083e80f22df3dae676dfb79d2ecf1862b0b721338470f9f2337f5a16f40`  
		Last Modified: Tue, 09 Dec 2025 04:12:14 GMT  
		Size: 6.7 MB (6653922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:955c48ff7de3a34eec555bfaefc96d239150ac74673d14f8c1ae30d182bec5a5`  
		Last Modified: Tue, 09 Dec 2025 04:12:15 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36.4-alpine`

```console
$ docker pull telegraf@sha256:46cabb477e6e31268bad42966facd2d52c22561d3cfc8d4b0c112b5728ba2c19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:48407b552b16c564ccc47bae44b45ab122d4f48a5bd67d75735d24f586e3f124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86642882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0280f08a3c4aeff01bdbeb32bbf32ce8225d3a92ce6199bdfdfabb565fdee4f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 17 Nov 2025 18:59:59 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 17 Nov 2025 19:00:00 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 17 Nov 2025 19:00:08 GMT
ENV TELEGRAF_VERSION=1.36.4
# Mon, 17 Nov 2025 19:00:08 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 17 Nov 2025 19:00:08 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 17 Nov 2025 19:00:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 17 Nov 2025 19:00:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 17 Nov 2025 19:00:08 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb344b979ef9e3d6ea2f360ff66a3139d4cfcd9b863983621de8eefe5cd84aa6`  
		Last Modified: Mon, 17 Nov 2025 19:00:31 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5696b9b7585c20f57f20c3c7c460662abb184e8eab21a8d4cafd61afc3077a9f`  
		Last Modified: Mon, 17 Nov 2025 19:00:32 GMT  
		Size: 2.6 MB (2563494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff853a04372dd9d1360ee371deb684033ada876ca3c1a38e2d67fe3c5f992aba`  
		Last Modified: Mon, 17 Nov 2025 19:12:22 GMT  
		Size: 80.3 MB (80276038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21db64bfe323b246d3e17e70370a071cbe6e04b604f006cafc7c552ae2a84a58`  
		Last Modified: Mon, 17 Nov 2025 19:00:32 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c9db14f5b6e1db85cf120f8325e5c21fb4b6bc3952dec26a4da8e31845827cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1157830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d50f7a3066665cbeb8c985217e41c9d2c2f556ea806eb93be6998e153351815`

```dockerfile
```

-	Layers:
	-	`sha256:d104164b2bcc3c30f646afbdfb9f7942e9d74e4e2e583067261c32c2602a9f20`  
		Last Modified: Mon, 17 Nov 2025 19:10:34 GMT  
		Size: 1.1 MB (1142610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4946291a4533c865cd6bb8bff0320c5aa46fefdae9cb144749cee928ced7711d`  
		Last Modified: Mon, 17 Nov 2025 19:10:35 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.4-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:4d49d49f81612798363550052fd65d73706db1548e68e0f38576322706f00ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78365616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e73a3d881177da588f763fcd0ab17af8d7f22d8dbad194af635b0bae1274cb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 17 Nov 2025 19:02:16 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 17 Nov 2025 19:02:18 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 17 Nov 2025 19:02:26 GMT
ENV TELEGRAF_VERSION=1.36.4
# Mon, 17 Nov 2025 19:02:26 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 17 Nov 2025 19:02:26 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 17 Nov 2025 19:02:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 17 Nov 2025 19:02:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 17 Nov 2025 19:02:26 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e686dad26a4c7f703dc366e1e60b14ae44807c190f97f04760640bb32361676`  
		Last Modified: Mon, 17 Nov 2025 19:02:47 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d3b38a4228f7da2c38dea9114166ad90b746642df4747865aa32a613fe8247`  
		Last Modified: Mon, 17 Nov 2025 19:02:48 GMT  
		Size: 2.6 MB (2627506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bca33979b5e4d10e8626da8ae6b21afab00ccbeef50beaf1bcd0ad868b8ce7`  
		Last Modified: Mon, 17 Nov 2025 19:02:55 GMT  
		Size: 71.6 MB (71599144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bfa9ad7ce4e4f025b9cfab73b412dc8c04760d6c3ace7fa607998ad9813725`  
		Last Modified: Mon, 17 Nov 2025 19:02:48 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:b73f976d36f57759d14866b99041351f2aeb2a0facca4b270cf46c7645d8b4ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1153591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85106f70e2bf1311bea0e40536625bd137213ea7b96647b802c77c659d7b1b43`

```dockerfile
```

-	Layers:
	-	`sha256:0e40d6658c33f56500ab6ae63559dc1c965812fc29e9404fd354af08b46bc679`  
		Last Modified: Mon, 17 Nov 2025 19:10:39 GMT  
		Size: 1.1 MB (1138249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1b269496aa7a00647a4b8e38da5384d0924c563e868cab39620498cdc13c489`  
		Last Modified: Mon, 17 Nov 2025 19:10:40 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37`

```console
$ docker pull telegraf@sha256:0eb1fe2f9e7880ed7c253130a1cd19cf304db205d792de373c6880557871c285
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37` - linux; amd64

```console
$ docker pull telegraf@sha256:e4b8e53298eb9010a767be4dd1dd71318d6c961ba9f591ade30b192490d33d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172205109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cca2b7da8d63b1546c96ed22922394547fb24b57d799ce60610de0fe513c3f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:21:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:21:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Dec 2025 00:21:41 GMT
ENV TELEGRAF_VERSION=1.37.0
# Tue, 09 Dec 2025 00:21:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 09 Dec 2025 00:21:41 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 09 Dec 2025 00:21:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:21:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:21:41 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae8659f7a8d357662281a0f87eb293725bb75ffa6c7356c38567f557d8a1f11`  
		Last Modified: Mon, 08 Dec 2025 23:07:04 GMT  
		Size: 24.0 MB (24029335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2aeecb4eeecda488b1df6ae55d6f478613cab9cc872282d3b7f296627db2cd0`  
		Last Modified: Tue, 09 Dec 2025 00:22:13 GMT  
		Size: 18.9 MB (18942872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b77b7e9edfde861f06acf9ff562d4b38bd0efebf1f0e35b8eb064c5f72bcd0`  
		Last Modified: Tue, 09 Dec 2025 00:22:15 GMT  
		Size: 3.4 KB (3441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119a0a1fc7f6babc083328e22ab9a5bbc0f9a251fae9c0a26191d3ec2f109134`  
		Last Modified: Tue, 09 Dec 2025 00:22:28 GMT  
		Size: 80.7 MB (80748100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114361313a00a462962ed8d7118417a318a6df36e2e9ed232bd19732b32649d3`  
		Last Modified: Tue, 09 Dec 2025 00:22:10 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37` - unknown; unknown

```console
$ docker pull telegraf@sha256:44d9ab931c49163d688151b6c909692c3fc58ed26f555bd4cfe36c4b684d4c1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6679126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c5f9955948932c7f5d4ae3fa40ed97d3a7bec4755ada30d9a0d387d44cb1e0`

```dockerfile
```

-	Layers:
	-	`sha256:a2b262433b19c9946dbdef31f9fe9277f920c95c08b396b3fdfc00b245b002bd`  
		Last Modified: Tue, 09 Dec 2025 04:12:15 GMT  
		Size: 6.7 MB (6664397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbf517d0c253b47e60621b1d4b86358cf52688ae7b68f2d56688a1685bdb0daa`  
		Last Modified: Tue, 09 Dec 2025 04:12:16 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:d1054a23cfa9fdf2e6a82fe121734cc660b8e3fc3391ff39474f45981e0c9212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.4 MB (158440133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6a74728ed08f99c5ab28f0d0202cea08c77173f23b30292f5dd932a7978f9e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:04:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:48:23 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:48:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Dec 2025 01:48:28 GMT
ENV TELEGRAF_VERSION=1.37.0
# Tue, 09 Dec 2025 01:48:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 09 Dec 2025 01:48:28 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 09 Dec 2025 01:48:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 01:48:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 01:48:28 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c3d6a83e736aa77820543663b2d6579ddd98b0f465c0fcad8aa9bd98a5b72a9c`  
		Last Modified: Mon, 08 Dec 2025 22:16:46 GMT  
		Size: 44.2 MB (44196066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0a258ea9a718fb1bf2331996816ba335715a3c786bd79934d265fd78fb7f5a`  
		Last Modified: Tue, 09 Dec 2025 00:05:11 GMT  
		Size: 21.9 MB (21934635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addbc7a3c44f7665882beff4c49e45502e9fb086ad023115f2c3e91d7cdfb308`  
		Last Modified: Tue, 09 Dec 2025 01:48:57 GMT  
		Size: 17.7 MB (17722570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacdf48657d83df9453c75b8d0ae2cc2eb6337d6b2a294b5b9829fcf7ba82104`  
		Last Modified: Tue, 09 Dec 2025 01:48:56 GMT  
		Size: 3.4 KB (3441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b623dee6700db781d38f49ec231424f68a4fa77727935a3a9fc613ff75b358`  
		Last Modified: Tue, 09 Dec 2025 01:49:02 GMT  
		Size: 74.6 MB (74582799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852b7e849287d55f437e16a6910a0ed4c9f1dc61cdec97048668dfdb4e0f19ba`  
		Last Modified: Tue, 09 Dec 2025 01:48:56 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37` - unknown; unknown

```console
$ docker pull telegraf@sha256:f744a0b5df8b83d3cee2f917011b372f21f6038a4e1e4e4883f257c227085792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6673829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f440aff40e2ca56defed8fada21e0c8afb24eb78e882079f0b9b2846a680881`

```dockerfile
```

-	Layers:
	-	`sha256:2eb9701dec68c2e29ef68908290ab728bb4886d697c0fe65e885005ef5302fd3`  
		Last Modified: Tue, 09 Dec 2025 04:12:21 GMT  
		Size: 6.7 MB (6659002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dbb2923b893a2eea015eebd3e30941ce8e4acf542df3cb7886d3a700cd062d6`  
		Last Modified: Tue, 09 Dec 2025 04:12:22 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:5ab7c7cc853e488b90db43644dc989d7af623c9fbccb37bc0e98f97bb95e9d2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162859499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52cc0ce3f096d944f5ed77694d91ebffdca4e7b1e55439325670ae8de5c620f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:10:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:28:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:28:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Dec 2025 00:28:41 GMT
ENV TELEGRAF_VERSION=1.37.0
# Tue, 09 Dec 2025 00:28:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 09 Dec 2025 00:28:41 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 09 Dec 2025 00:28:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:28:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:28:41 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0da1fc24a51c3ab23b5143a2c67b43348114c11a8029b3483be57ab9fe54eb6`  
		Last Modified: Mon, 08 Dec 2025 23:10:26 GMT  
		Size: 23.6 MB (23598247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de78b019179df4648a42b63178c49a2c7a236ed995ea206703c5da07c2cdd09`  
		Last Modified: Tue, 09 Dec 2025 00:29:08 GMT  
		Size: 18.9 MB (18884503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1eda6442abebaf9ddcef10e6c0e6d552355aa304bf974fc1f7c3d38a511c9e`  
		Last Modified: Tue, 09 Dec 2025 00:29:06 GMT  
		Size: 3.5 KB (3452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3fc3bd5be77ad1d1b58abe32e7a0ed5a11b47ff2dad3cb2984bbaf7622ceed`  
		Last Modified: Tue, 09 Dec 2025 00:29:17 GMT  
		Size: 72.0 MB (72013603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4749d23e3c956b13f84e07f888f57fb7d0fb84cb571780e5aff32970dcb30a13`  
		Last Modified: Tue, 09 Dec 2025 00:29:06 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37` - unknown; unknown

```console
$ docker pull telegraf@sha256:08c1c964e8e07f6fc4e4ab5de6c5f5ba17a812951e1eb5b3b52687ecb7e44df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6679936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dad454fb440bbc5fee977d740565470d9575fabd88deeb440063c2a5c7823b9`

```dockerfile
```

-	Layers:
	-	`sha256:71b50cc9e0efe3956d41fb87c0c0903fb0e582f384d404fa455191837e49aad2`  
		Last Modified: Tue, 09 Dec 2025 04:12:28 GMT  
		Size: 6.7 MB (6665085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f1a655cfefd0c3650717001e9fb1b18671d8dcaed50a9520f508a5de0565b19`  
		Last Modified: Tue, 09 Dec 2025 04:12:29 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37-alpine`

```console
$ docker pull telegraf@sha256:9a4fc91b4abbeda71ed1b20eaf171fe050aa2ad2b21eb14ff703fc855c907c2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:c42df5ee945977249706b33cc61cc8078d2413faf02d3f9360e2d79f4cef23a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86908207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ad33aa6db544c71a9cb9ed7c3c8f1a9dbddd2a11da136741157e75b24c7e575`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 21:15:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 08 Dec 2025 21:15:53 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 08 Dec 2025 21:16:01 GMT
ENV TELEGRAF_VERSION=1.37.0
# Mon, 08 Dec 2025 21:16:01 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 08 Dec 2025 21:16:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Dec 2025 21:16:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 21:16:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 21:16:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a611c78d9bf6367a5ff1c0af825e87a9c688c32c6bd466b0152c8e55057d0ef8`  
		Last Modified: Mon, 08 Dec 2025 21:16:27 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6c6b437b30b508582494bc3659651fc006e6b317cb913bcfecb0c9cc43f903`  
		Last Modified: Mon, 08 Dec 2025 21:16:27 GMT  
		Size: 2.6 MB (2563450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae2bab86b5942106a04676b4bf7c91a0d29d2292a13f02bf6d4f36ddf622483`  
		Last Modified: Mon, 08 Dec 2025 21:16:44 GMT  
		Size: 80.5 MB (80541409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41706228cbe6d20f21947a6628baaf8686a316dde23a1af93d00244f957b3106`  
		Last Modified: Mon, 08 Dec 2025 21:16:27 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:22ea74f5e3a9e94dc1875a8b87f5cff2f305ab5255ca166688adef8cf7484649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1168679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6e2eabd715b17c5f68e5cdc67087023aeba7abc6487fba2e80f4ad65d55876`

```dockerfile
```

-	Layers:
	-	`sha256:6de4f753fda5fa2690b93557578e653e46294dd08d956c09b311ec9ebb6cfd38`  
		Last Modified: Mon, 08 Dec 2025 22:10:36 GMT  
		Size: 1.2 MB (1153459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97258d9d1ffd16f77651af3edcb551aad12dda21350c060371c7ebe7215d0e5b`  
		Last Modified: Mon, 08 Dec 2025 22:10:37 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6af586afcd09465b767fad06b4d75c562f9bf300cf196c9a2c00327d04f850dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78572340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4aff5bfdfec17e65cca78f8663b7051e50a8911fdfca5c4c3446a87f2a59a5c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 21:14:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 08 Dec 2025 21:14:24 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 08 Dec 2025 21:14:32 GMT
ENV TELEGRAF_VERSION=1.37.0
# Mon, 08 Dec 2025 21:14:32 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 08 Dec 2025 21:14:32 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Dec 2025 21:14:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 21:14:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 21:14:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b37a1a2b9598ec2c2a9163b74e038910a5495a3e5f255f76b1d3e83be45d64f`  
		Last Modified: Mon, 08 Dec 2025 21:14:53 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582eb84a33ab2260528ae7b8b512ca3a9d38048483a4ce48ba5fcfc4d779a551`  
		Last Modified: Mon, 08 Dec 2025 21:14:53 GMT  
		Size: 2.6 MB (2627517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41c305c71f628d11404eb52f4f468848edb0489ef820a2b9eb32aff5b996015`  
		Last Modified: Mon, 08 Dec 2025 21:15:02 GMT  
		Size: 71.8 MB (71805856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff24d143605b201c9e6d56010a5fb6bd81d9f301639b34dd6ab94ff439f83b6`  
		Last Modified: Mon, 08 Dec 2025 21:14:53 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:230c5af04901994545279302b5df587e34bf258e19ab60e53cb069a9ba652f73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1164440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22eafb95136ea3bf17561283dc6499af8c5feec12c67e57764c559e5a6597629`

```dockerfile
```

-	Layers:
	-	`sha256:57b8b1fcfb80ab3ba810659ce21ac5f533de482bb3d1da675785fe5db4ef76b8`  
		Last Modified: Mon, 08 Dec 2025 22:10:41 GMT  
		Size: 1.1 MB (1149098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dcc52c65be07218d787c7581acb9d9ce226c1501d5d81dac46405ac0fd75f63`  
		Last Modified: Mon, 08 Dec 2025 22:10:42 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37.0`

```console
$ docker pull telegraf@sha256:0eb1fe2f9e7880ed7c253130a1cd19cf304db205d792de373c6880557871c285
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37.0` - linux; amd64

```console
$ docker pull telegraf@sha256:e4b8e53298eb9010a767be4dd1dd71318d6c961ba9f591ade30b192490d33d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172205109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cca2b7da8d63b1546c96ed22922394547fb24b57d799ce60610de0fe513c3f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:21:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:21:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Dec 2025 00:21:41 GMT
ENV TELEGRAF_VERSION=1.37.0
# Tue, 09 Dec 2025 00:21:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 09 Dec 2025 00:21:41 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 09 Dec 2025 00:21:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:21:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:21:41 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae8659f7a8d357662281a0f87eb293725bb75ffa6c7356c38567f557d8a1f11`  
		Last Modified: Mon, 08 Dec 2025 23:07:04 GMT  
		Size: 24.0 MB (24029335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2aeecb4eeecda488b1df6ae55d6f478613cab9cc872282d3b7f296627db2cd0`  
		Last Modified: Tue, 09 Dec 2025 00:22:13 GMT  
		Size: 18.9 MB (18942872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b77b7e9edfde861f06acf9ff562d4b38bd0efebf1f0e35b8eb064c5f72bcd0`  
		Last Modified: Tue, 09 Dec 2025 00:22:15 GMT  
		Size: 3.4 KB (3441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119a0a1fc7f6babc083328e22ab9a5bbc0f9a251fae9c0a26191d3ec2f109134`  
		Last Modified: Tue, 09 Dec 2025 00:22:28 GMT  
		Size: 80.7 MB (80748100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114361313a00a462962ed8d7118417a318a6df36e2e9ed232bd19732b32649d3`  
		Last Modified: Tue, 09 Dec 2025 00:22:10 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.0` - unknown; unknown

```console
$ docker pull telegraf@sha256:44d9ab931c49163d688151b6c909692c3fc58ed26f555bd4cfe36c4b684d4c1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6679126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c5f9955948932c7f5d4ae3fa40ed97d3a7bec4755ada30d9a0d387d44cb1e0`

```dockerfile
```

-	Layers:
	-	`sha256:a2b262433b19c9946dbdef31f9fe9277f920c95c08b396b3fdfc00b245b002bd`  
		Last Modified: Tue, 09 Dec 2025 04:12:15 GMT  
		Size: 6.7 MB (6664397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbf517d0c253b47e60621b1d4b86358cf52688ae7b68f2d56688a1685bdb0daa`  
		Last Modified: Tue, 09 Dec 2025 04:12:16 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37.0` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:d1054a23cfa9fdf2e6a82fe121734cc660b8e3fc3391ff39474f45981e0c9212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.4 MB (158440133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6a74728ed08f99c5ab28f0d0202cea08c77173f23b30292f5dd932a7978f9e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:04:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:48:23 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:48:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Dec 2025 01:48:28 GMT
ENV TELEGRAF_VERSION=1.37.0
# Tue, 09 Dec 2025 01:48:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 09 Dec 2025 01:48:28 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 09 Dec 2025 01:48:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 01:48:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 01:48:28 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c3d6a83e736aa77820543663b2d6579ddd98b0f465c0fcad8aa9bd98a5b72a9c`  
		Last Modified: Mon, 08 Dec 2025 22:16:46 GMT  
		Size: 44.2 MB (44196066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0a258ea9a718fb1bf2331996816ba335715a3c786bd79934d265fd78fb7f5a`  
		Last Modified: Tue, 09 Dec 2025 00:05:11 GMT  
		Size: 21.9 MB (21934635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addbc7a3c44f7665882beff4c49e45502e9fb086ad023115f2c3e91d7cdfb308`  
		Last Modified: Tue, 09 Dec 2025 01:48:57 GMT  
		Size: 17.7 MB (17722570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacdf48657d83df9453c75b8d0ae2cc2eb6337d6b2a294b5b9829fcf7ba82104`  
		Last Modified: Tue, 09 Dec 2025 01:48:56 GMT  
		Size: 3.4 KB (3441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b623dee6700db781d38f49ec231424f68a4fa77727935a3a9fc613ff75b358`  
		Last Modified: Tue, 09 Dec 2025 01:49:02 GMT  
		Size: 74.6 MB (74582799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852b7e849287d55f437e16a6910a0ed4c9f1dc61cdec97048668dfdb4e0f19ba`  
		Last Modified: Tue, 09 Dec 2025 01:48:56 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.0` - unknown; unknown

```console
$ docker pull telegraf@sha256:f744a0b5df8b83d3cee2f917011b372f21f6038a4e1e4e4883f257c227085792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6673829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f440aff40e2ca56defed8fada21e0c8afb24eb78e882079f0b9b2846a680881`

```dockerfile
```

-	Layers:
	-	`sha256:2eb9701dec68c2e29ef68908290ab728bb4886d697c0fe65e885005ef5302fd3`  
		Last Modified: Tue, 09 Dec 2025 04:12:21 GMT  
		Size: 6.7 MB (6659002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dbb2923b893a2eea015eebd3e30941ce8e4acf542df3cb7886d3a700cd062d6`  
		Last Modified: Tue, 09 Dec 2025 04:12:22 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37.0` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:5ab7c7cc853e488b90db43644dc989d7af623c9fbccb37bc0e98f97bb95e9d2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162859499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52cc0ce3f096d944f5ed77694d91ebffdca4e7b1e55439325670ae8de5c620f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:10:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:28:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:28:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Dec 2025 00:28:41 GMT
ENV TELEGRAF_VERSION=1.37.0
# Tue, 09 Dec 2025 00:28:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 09 Dec 2025 00:28:41 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 09 Dec 2025 00:28:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:28:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:28:41 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0da1fc24a51c3ab23b5143a2c67b43348114c11a8029b3483be57ab9fe54eb6`  
		Last Modified: Mon, 08 Dec 2025 23:10:26 GMT  
		Size: 23.6 MB (23598247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de78b019179df4648a42b63178c49a2c7a236ed995ea206703c5da07c2cdd09`  
		Last Modified: Tue, 09 Dec 2025 00:29:08 GMT  
		Size: 18.9 MB (18884503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1eda6442abebaf9ddcef10e6c0e6d552355aa304bf974fc1f7c3d38a511c9e`  
		Last Modified: Tue, 09 Dec 2025 00:29:06 GMT  
		Size: 3.5 KB (3452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3fc3bd5be77ad1d1b58abe32e7a0ed5a11b47ff2dad3cb2984bbaf7622ceed`  
		Last Modified: Tue, 09 Dec 2025 00:29:17 GMT  
		Size: 72.0 MB (72013603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4749d23e3c956b13f84e07f888f57fb7d0fb84cb571780e5aff32970dcb30a13`  
		Last Modified: Tue, 09 Dec 2025 00:29:06 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.0` - unknown; unknown

```console
$ docker pull telegraf@sha256:08c1c964e8e07f6fc4e4ab5de6c5f5ba17a812951e1eb5b3b52687ecb7e44df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6679936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dad454fb440bbc5fee977d740565470d9575fabd88deeb440063c2a5c7823b9`

```dockerfile
```

-	Layers:
	-	`sha256:71b50cc9e0efe3956d41fb87c0c0903fb0e582f384d404fa455191837e49aad2`  
		Last Modified: Tue, 09 Dec 2025 04:12:28 GMT  
		Size: 6.7 MB (6665085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f1a655cfefd0c3650717001e9fb1b18671d8dcaed50a9520f508a5de0565b19`  
		Last Modified: Tue, 09 Dec 2025 04:12:29 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37.0-alpine`

```console
$ docker pull telegraf@sha256:9a4fc91b4abbeda71ed1b20eaf171fe050aa2ad2b21eb14ff703fc855c907c2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37.0-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:c42df5ee945977249706b33cc61cc8078d2413faf02d3f9360e2d79f4cef23a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86908207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ad33aa6db544c71a9cb9ed7c3c8f1a9dbddd2a11da136741157e75b24c7e575`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 21:15:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 08 Dec 2025 21:15:53 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 08 Dec 2025 21:16:01 GMT
ENV TELEGRAF_VERSION=1.37.0
# Mon, 08 Dec 2025 21:16:01 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 08 Dec 2025 21:16:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Dec 2025 21:16:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 21:16:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 21:16:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a611c78d9bf6367a5ff1c0af825e87a9c688c32c6bd466b0152c8e55057d0ef8`  
		Last Modified: Mon, 08 Dec 2025 21:16:27 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6c6b437b30b508582494bc3659651fc006e6b317cb913bcfecb0c9cc43f903`  
		Last Modified: Mon, 08 Dec 2025 21:16:27 GMT  
		Size: 2.6 MB (2563450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae2bab86b5942106a04676b4bf7c91a0d29d2292a13f02bf6d4f36ddf622483`  
		Last Modified: Mon, 08 Dec 2025 21:16:44 GMT  
		Size: 80.5 MB (80541409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41706228cbe6d20f21947a6628baaf8686a316dde23a1af93d00244f957b3106`  
		Last Modified: Mon, 08 Dec 2025 21:16:27 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.0-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:22ea74f5e3a9e94dc1875a8b87f5cff2f305ab5255ca166688adef8cf7484649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1168679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6e2eabd715b17c5f68e5cdc67087023aeba7abc6487fba2e80f4ad65d55876`

```dockerfile
```

-	Layers:
	-	`sha256:6de4f753fda5fa2690b93557578e653e46294dd08d956c09b311ec9ebb6cfd38`  
		Last Modified: Mon, 08 Dec 2025 22:10:36 GMT  
		Size: 1.2 MB (1153459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97258d9d1ffd16f77651af3edcb551aad12dda21350c060371c7ebe7215d0e5b`  
		Last Modified: Mon, 08 Dec 2025 22:10:37 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37.0-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6af586afcd09465b767fad06b4d75c562f9bf300cf196c9a2c00327d04f850dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78572340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4aff5bfdfec17e65cca78f8663b7051e50a8911fdfca5c4c3446a87f2a59a5c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 21:14:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 08 Dec 2025 21:14:24 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 08 Dec 2025 21:14:32 GMT
ENV TELEGRAF_VERSION=1.37.0
# Mon, 08 Dec 2025 21:14:32 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 08 Dec 2025 21:14:32 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Dec 2025 21:14:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 21:14:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 21:14:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b37a1a2b9598ec2c2a9163b74e038910a5495a3e5f255f76b1d3e83be45d64f`  
		Last Modified: Mon, 08 Dec 2025 21:14:53 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582eb84a33ab2260528ae7b8b512ca3a9d38048483a4ce48ba5fcfc4d779a551`  
		Last Modified: Mon, 08 Dec 2025 21:14:53 GMT  
		Size: 2.6 MB (2627517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41c305c71f628d11404eb52f4f468848edb0489ef820a2b9eb32aff5b996015`  
		Last Modified: Mon, 08 Dec 2025 21:15:02 GMT  
		Size: 71.8 MB (71805856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff24d143605b201c9e6d56010a5fb6bd81d9f301639b34dd6ab94ff439f83b6`  
		Last Modified: Mon, 08 Dec 2025 21:14:53 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.0-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:230c5af04901994545279302b5df587e34bf258e19ab60e53cb069a9ba652f73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1164440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22eafb95136ea3bf17561283dc6499af8c5feec12c67e57764c559e5a6597629`

```dockerfile
```

-	Layers:
	-	`sha256:57b8b1fcfb80ab3ba810659ce21ac5f533de482bb3d1da675785fe5db4ef76b8`  
		Last Modified: Mon, 08 Dec 2025 22:10:41 GMT  
		Size: 1.1 MB (1149098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dcc52c65be07218d787c7581acb9d9ce226c1501d5d81dac46405ac0fd75f63`  
		Last Modified: Mon, 08 Dec 2025 22:10:42 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:9a4fc91b4abbeda71ed1b20eaf171fe050aa2ad2b21eb14ff703fc855c907c2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:c42df5ee945977249706b33cc61cc8078d2413faf02d3f9360e2d79f4cef23a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86908207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ad33aa6db544c71a9cb9ed7c3c8f1a9dbddd2a11da136741157e75b24c7e575`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 21:15:52 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 08 Dec 2025 21:15:53 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 08 Dec 2025 21:16:01 GMT
ENV TELEGRAF_VERSION=1.37.0
# Mon, 08 Dec 2025 21:16:01 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 08 Dec 2025 21:16:01 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Dec 2025 21:16:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 21:16:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 21:16:01 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a611c78d9bf6367a5ff1c0af825e87a9c688c32c6bd466b0152c8e55057d0ef8`  
		Last Modified: Mon, 08 Dec 2025 21:16:27 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6c6b437b30b508582494bc3659651fc006e6b317cb913bcfecb0c9cc43f903`  
		Last Modified: Mon, 08 Dec 2025 21:16:27 GMT  
		Size: 2.6 MB (2563450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae2bab86b5942106a04676b4bf7c91a0d29d2292a13f02bf6d4f36ddf622483`  
		Last Modified: Mon, 08 Dec 2025 21:16:44 GMT  
		Size: 80.5 MB (80541409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41706228cbe6d20f21947a6628baaf8686a316dde23a1af93d00244f957b3106`  
		Last Modified: Mon, 08 Dec 2025 21:16:27 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:22ea74f5e3a9e94dc1875a8b87f5cff2f305ab5255ca166688adef8cf7484649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1168679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f6e2eabd715b17c5f68e5cdc67087023aeba7abc6487fba2e80f4ad65d55876`

```dockerfile
```

-	Layers:
	-	`sha256:6de4f753fda5fa2690b93557578e653e46294dd08d956c09b311ec9ebb6cfd38`  
		Last Modified: Mon, 08 Dec 2025 22:10:36 GMT  
		Size: 1.2 MB (1153459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97258d9d1ffd16f77651af3edcb551aad12dda21350c060371c7ebe7215d0e5b`  
		Last Modified: Mon, 08 Dec 2025 22:10:37 GMT  
		Size: 15.2 KB (15220 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:6af586afcd09465b767fad06b4d75c562f9bf300cf196c9a2c00327d04f850dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78572340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4aff5bfdfec17e65cca78f8663b7051e50a8911fdfca5c4c3446a87f2a59a5c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 21:14:23 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 08 Dec 2025 21:14:24 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 08 Dec 2025 21:14:32 GMT
ENV TELEGRAF_VERSION=1.37.0
# Mon, 08 Dec 2025 21:14:32 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 08 Dec 2025 21:14:32 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 08 Dec 2025 21:14:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 08 Dec 2025 21:14:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 08 Dec 2025 21:14:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b37a1a2b9598ec2c2a9163b74e038910a5495a3e5f255f76b1d3e83be45d64f`  
		Last Modified: Mon, 08 Dec 2025 21:14:53 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582eb84a33ab2260528ae7b8b512ca3a9d38048483a4ce48ba5fcfc4d779a551`  
		Last Modified: Mon, 08 Dec 2025 21:14:53 GMT  
		Size: 2.6 MB (2627517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41c305c71f628d11404eb52f4f468848edb0489ef820a2b9eb32aff5b996015`  
		Last Modified: Mon, 08 Dec 2025 21:15:02 GMT  
		Size: 71.8 MB (71805856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff24d143605b201c9e6d56010a5fb6bd81d9f301639b34dd6ab94ff439f83b6`  
		Last Modified: Mon, 08 Dec 2025 21:14:53 GMT  
		Size: 619.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:230c5af04901994545279302b5df587e34bf258e19ab60e53cb069a9ba652f73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1164440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22eafb95136ea3bf17561283dc6499af8c5feec12c67e57764c559e5a6597629`

```dockerfile
```

-	Layers:
	-	`sha256:57b8b1fcfb80ab3ba810659ce21ac5f533de482bb3d1da675785fe5db4ef76b8`  
		Last Modified: Mon, 08 Dec 2025 22:10:41 GMT  
		Size: 1.1 MB (1149098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dcc52c65be07218d787c7581acb9d9ce226c1501d5d81dac46405ac0fd75f63`  
		Last Modified: Mon, 08 Dec 2025 22:10:42 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:0eb1fe2f9e7880ed7c253130a1cd19cf304db205d792de373c6880557871c285
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:e4b8e53298eb9010a767be4dd1dd71318d6c961ba9f591ade30b192490d33d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172205109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cca2b7da8d63b1546c96ed22922394547fb24b57d799ce60610de0fe513c3f0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:06:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:21:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:21:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Dec 2025 00:21:41 GMT
ENV TELEGRAF_VERSION=1.37.0
# Tue, 09 Dec 2025 00:21:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 09 Dec 2025 00:21:41 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 09 Dec 2025 00:21:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:21:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:21:41 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae8659f7a8d357662281a0f87eb293725bb75ffa6c7356c38567f557d8a1f11`  
		Last Modified: Mon, 08 Dec 2025 23:07:04 GMT  
		Size: 24.0 MB (24029335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2aeecb4eeecda488b1df6ae55d6f478613cab9cc872282d3b7f296627db2cd0`  
		Last Modified: Tue, 09 Dec 2025 00:22:13 GMT  
		Size: 18.9 MB (18942872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b77b7e9edfde861f06acf9ff562d4b38bd0efebf1f0e35b8eb064c5f72bcd0`  
		Last Modified: Tue, 09 Dec 2025 00:22:15 GMT  
		Size: 3.4 KB (3441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119a0a1fc7f6babc083328e22ab9a5bbc0f9a251fae9c0a26191d3ec2f109134`  
		Last Modified: Tue, 09 Dec 2025 00:22:28 GMT  
		Size: 80.7 MB (80748100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114361313a00a462962ed8d7118417a318a6df36e2e9ed232bd19732b32649d3`  
		Last Modified: Tue, 09 Dec 2025 00:22:10 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:44d9ab931c49163d688151b6c909692c3fc58ed26f555bd4cfe36c4b684d4c1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6679126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c5f9955948932c7f5d4ae3fa40ed97d3a7bec4755ada30d9a0d387d44cb1e0`

```dockerfile
```

-	Layers:
	-	`sha256:a2b262433b19c9946dbdef31f9fe9277f920c95c08b396b3fdfc00b245b002bd`  
		Last Modified: Tue, 09 Dec 2025 04:12:15 GMT  
		Size: 6.7 MB (6664397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbf517d0c253b47e60621b1d4b86358cf52688ae7b68f2d56688a1685bdb0daa`  
		Last Modified: Tue, 09 Dec 2025 04:12:16 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:d1054a23cfa9fdf2e6a82fe121734cc660b8e3fc3391ff39474f45981e0c9212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.4 MB (158440133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb6a74728ed08f99c5ab28f0d0202cea08c77173f23b30292f5dd932a7978f9e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:04:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:48:23 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:48:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Dec 2025 01:48:28 GMT
ENV TELEGRAF_VERSION=1.37.0
# Tue, 09 Dec 2025 01:48:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 09 Dec 2025 01:48:28 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 09 Dec 2025 01:48:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 01:48:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 01:48:28 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c3d6a83e736aa77820543663b2d6579ddd98b0f465c0fcad8aa9bd98a5b72a9c`  
		Last Modified: Mon, 08 Dec 2025 22:16:46 GMT  
		Size: 44.2 MB (44196066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0a258ea9a718fb1bf2331996816ba335715a3c786bd79934d265fd78fb7f5a`  
		Last Modified: Tue, 09 Dec 2025 00:05:11 GMT  
		Size: 21.9 MB (21934635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addbc7a3c44f7665882beff4c49e45502e9fb086ad023115f2c3e91d7cdfb308`  
		Last Modified: Tue, 09 Dec 2025 01:48:57 GMT  
		Size: 17.7 MB (17722570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacdf48657d83df9453c75b8d0ae2cc2eb6337d6b2a294b5b9829fcf7ba82104`  
		Last Modified: Tue, 09 Dec 2025 01:48:56 GMT  
		Size: 3.4 KB (3441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b623dee6700db781d38f49ec231424f68a4fa77727935a3a9fc613ff75b358`  
		Last Modified: Tue, 09 Dec 2025 01:49:02 GMT  
		Size: 74.6 MB (74582799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852b7e849287d55f437e16a6910a0ed4c9f1dc61cdec97048668dfdb4e0f19ba`  
		Last Modified: Tue, 09 Dec 2025 01:48:56 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:f744a0b5df8b83d3cee2f917011b372f21f6038a4e1e4e4883f257c227085792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6673829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f440aff40e2ca56defed8fada21e0c8afb24eb78e882079f0b9b2846a680881`

```dockerfile
```

-	Layers:
	-	`sha256:2eb9701dec68c2e29ef68908290ab728bb4886d697c0fe65e885005ef5302fd3`  
		Last Modified: Tue, 09 Dec 2025 04:12:21 GMT  
		Size: 6.7 MB (6659002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dbb2923b893a2eea015eebd3e30941ce8e4acf542df3cb7886d3a700cd062d6`  
		Last Modified: Tue, 09 Dec 2025 04:12:22 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:5ab7c7cc853e488b90db43644dc989d7af623c9fbccb37bc0e98f97bb95e9d2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162859499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52cc0ce3f096d944f5ed77694d91ebffdca4e7b1e55439325670ae8de5c620f1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:10:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:28:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:28:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 09 Dec 2025 00:28:41 GMT
ENV TELEGRAF_VERSION=1.37.0
# Tue, 09 Dec 2025 00:28:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 09 Dec 2025 00:28:41 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 09 Dec 2025 00:28:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 09 Dec 2025 00:28:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Dec 2025 00:28:41 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0da1fc24a51c3ab23b5143a2c67b43348114c11a8029b3483be57ab9fe54eb6`  
		Last Modified: Mon, 08 Dec 2025 23:10:26 GMT  
		Size: 23.6 MB (23598247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de78b019179df4648a42b63178c49a2c7a236ed995ea206703c5da07c2cdd09`  
		Last Modified: Tue, 09 Dec 2025 00:29:08 GMT  
		Size: 18.9 MB (18884503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1eda6442abebaf9ddcef10e6c0e6d552355aa304bf974fc1f7c3d38a511c9e`  
		Last Modified: Tue, 09 Dec 2025 00:29:06 GMT  
		Size: 3.5 KB (3452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3fc3bd5be77ad1d1b58abe32e7a0ed5a11b47ff2dad3cb2984bbaf7622ceed`  
		Last Modified: Tue, 09 Dec 2025 00:29:17 GMT  
		Size: 72.0 MB (72013603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4749d23e3c956b13f84e07f888f57fb7d0fb84cb571780e5aff32970dcb30a13`  
		Last Modified: Tue, 09 Dec 2025 00:29:06 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:08c1c964e8e07f6fc4e4ab5de6c5f5ba17a812951e1eb5b3b52687ecb7e44df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6679936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dad454fb440bbc5fee977d740565470d9575fabd88deeb440063c2a5c7823b9`

```dockerfile
```

-	Layers:
	-	`sha256:71b50cc9e0efe3956d41fb87c0c0903fb0e582f384d404fa455191837e49aad2`  
		Last Modified: Tue, 09 Dec 2025 04:12:28 GMT  
		Size: 6.7 MB (6665085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f1a655cfefd0c3650717001e9fb1b18671d8dcaed50a9520f508a5de0565b19`  
		Last Modified: Tue, 09 Dec 2025 04:12:29 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json
