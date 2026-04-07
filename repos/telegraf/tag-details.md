<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.36`](#telegraf136)
-	[`telegraf:1.36-alpine`](#telegraf136-alpine)
-	[`telegraf:1.36.4`](#telegraf1364)
-	[`telegraf:1.36.4-alpine`](#telegraf1364-alpine)
-	[`telegraf:1.37`](#telegraf137)
-	[`telegraf:1.37-alpine`](#telegraf137-alpine)
-	[`telegraf:1.37.3`](#telegraf1373)
-	[`telegraf:1.37.3-alpine`](#telegraf1373-alpine)
-	[`telegraf:1.38`](#telegraf138)
-	[`telegraf:1.38-alpine`](#telegraf138-alpine)
-	[`telegraf:1.38.2`](#telegraf1382)
-	[`telegraf:1.38.2-alpine`](#telegraf1382-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.36`

```console
$ docker pull telegraf@sha256:b8b78323f272928584310161a293dc3dfcf89a65e019890e5543781fe6a926eb
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
$ docker pull telegraf@sha256:6d235481ebd1f2b9f47fdb09a731dcc41696985a5b74ea439b22a475b6afb4bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.0 MB (171950866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d545d215ddd3c2c123edea474af09d885614921199b175adf42484d3639caf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:08:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:08:58 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 03:09:02 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 07 Apr 2026 03:09:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 07 Apr 2026 03:09:02 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 07 Apr 2026 03:09:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 03:09:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 03:09:02 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c3414b1d6b49c54c305584faac46aad75c67644cf4f8495e8145206d28e416`  
		Last Modified: Tue, 07 Apr 2026 01:47:02 GMT  
		Size: 24.0 MB (24038269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33783d9cba990ea068fd7b11de7ac26da4e0e7e412f7802b50d66f837c8f77e6`  
		Last Modified: Tue, 07 Apr 2026 03:09:23 GMT  
		Size: 18.9 MB (18944499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2914360d962562f729d89e57142ce9620abe1fea7f9f9064b300d64ecfccbd35`  
		Last Modified: Tue, 07 Apr 2026 03:09:22 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234c31214cb9692aefbc72448ea300445113323bddeca3f722891ffc97db61fc`  
		Last Modified: Tue, 07 Apr 2026 03:09:24 GMT  
		Size: 80.5 MB (80473597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f52cb2ca9cd952a6dd8f75a3dc608a824db3da8ad4e5fc8e36ab1d251a6ed1d`  
		Last Modified: Tue, 07 Apr 2026 03:09:22 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:a74f2eaab34ec0bd044d25f9ecf89d141410526560c0a2ec09527887b8fd7089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6670530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac22ed98a335a2c1791dfa31216f2bf80a4bd910321a051acac3364b29220416`

```dockerfile
```

-	Layers:
	-	`sha256:d6fe1417cf5b288262401bd7d92bb9f76147bc29c2169661145e5685a7c3b838`  
		Last Modified: Tue, 07 Apr 2026 03:09:22 GMT  
		Size: 6.7 MB (6656103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59ea5810b48af39ad6a8d54a1721094c0e9f47f8bb2b9a612cabd96566b2b1c9`  
		Last Modified: Tue, 07 Apr 2026 03:09:22 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:15fc82113bb56ecb61a38be93e57652129172402e5925586a704c88fad51958d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157818846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a3b5bc6eeab29c04d6f1b17ecc04caefe54778e4e806135ee9df0883e68faa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:00:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:04:20 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:04:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 04:04:27 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 07 Apr 2026 04:04:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 07 Apr 2026 04:04:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 07 Apr 2026 04:04:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 04:04:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 04:04:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a99a9abe3964725d9016ffc8402d9cffc28e94f404db8e764ca9583f2090145e`  
		Last Modified: Tue, 07 Apr 2026 00:58:42 GMT  
		Size: 44.2 MB (44207817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2a6632e49a08fc68f1ee0ec0fb4b6f38a03db30dc5ff33b611dc705110ee36`  
		Last Modified: Tue, 07 Apr 2026 02:00:47 GMT  
		Size: 21.9 MB (21942083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a771ebfd7afc5eca9ff2ad80a3ba411bb2e5946ec065365a53c7a9eaf5acdac`  
		Last Modified: Tue, 07 Apr 2026 04:04:45 GMT  
		Size: 17.7 MB (17699627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a891bb2f2058cba8c4a8bd430fe391b46be672d463afd41bf61acce0416b72d6`  
		Last Modified: Tue, 07 Apr 2026 04:04:44 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17268f16d13db6654617820e032ecbe91cf92c64ce9d19805f98154114b16f2`  
		Last Modified: Tue, 07 Apr 2026 04:04:46 GMT  
		Size: 74.0 MB (73963640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c6c50cc02c6ecb2a576608f1692aa8afdf9dacdd36567f9b604478c276e132`  
		Last Modified: Tue, 07 Apr 2026 04:04:44 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:a626c00cb88f84187b8ce2f2b745a6a27895ab464ff6e5be9cb12e0ec42b699a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6665217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:315acb8c2d98bce4d0ea209d241a3a7c03f5202326ef44520188c092a8eba18e`

```dockerfile
```

-	Layers:
	-	`sha256:3fb7f617d73ad59cfead76b7709654652d987918dce1559d945f6854adef295c`  
		Last Modified: Tue, 07 Apr 2026 04:04:44 GMT  
		Size: 6.7 MB (6650700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e92cc254c72949abc0195f93d49adf27296116745ff6d6e85dbecf8f5fbcecf8`  
		Last Modified: Tue, 07 Apr 2026 04:04:44 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:dcdf91f273c4ef463af86692ddfe909156c7446c0f21127efe4bca3f9839e635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162669961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cefcd94ab4b2fd0117f2b61eef0f14db8d451483db16b2ce08d8be6caf84232`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:19:24 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:19:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 03:19:28 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 07 Apr 2026 03:19:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 07 Apr 2026 03:19:28 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 07 Apr 2026 03:19:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 03:19:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 03:19:28 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af98f0879b367460715b477e9118922ba24f17d9a4ad8d70e595a9c4cf56990`  
		Last Modified: Tue, 07 Apr 2026 01:49:50 GMT  
		Size: 23.6 MB (23604705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717b13f7a2834f96d950d53a1f74c70953d30597ff61a07458413359fc723064`  
		Last Modified: Tue, 07 Apr 2026 03:19:47 GMT  
		Size: 18.9 MB (18885928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc064ce34ffb9a2d01ef8453f647784c2a4daffcb14cbb4970dc150bd58b590`  
		Last Modified: Tue, 07 Apr 2026 03:19:46 GMT  
		Size: 5.1 KB (5073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e453bbb0525bdbd717ff66723ec90915960f225e77eec6be25bf91c02fdbed9`  
		Last Modified: Tue, 07 Apr 2026 03:19:49 GMT  
		Size: 71.8 MB (71800372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa923b9a0bd31076366d661d4912909bf4a5009fa474e4b18052df6aa07699d`  
		Last Modified: Tue, 07 Apr 2026 03:19:46 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36` - unknown; unknown

```console
$ docker pull telegraf@sha256:2d9d8a436aa721777e3b0d4d9eca2c84c0355098c766c5da684fe222ead3d271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ced8eef6f6cd80642425eb9ddd9377a0d7a26c7b62d0d367f856d1db0ab3bf4`

```dockerfile
```

-	Layers:
	-	`sha256:997f9547f394a52b8ed228d51854c8c4e6e35e21d35969176f86ba2021ce85b7`  
		Last Modified: Tue, 07 Apr 2026 03:19:46 GMT  
		Size: 6.7 MB (6656779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b52911127fa7518d20f3577b818589649e1ea92044699b0d4aaebc44a285882`  
		Last Modified: Tue, 07 Apr 2026 03:19:46 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36-alpine`

```console
$ docker pull telegraf@sha256:74614dd18bd8c984d8d5423d6c362da8b9a0c32543f9932660f03c1e8ae22893
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:7e104d74dd7644a3f52e10b68cf4972907df0e16d541772b9da2cd987768f243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86645547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:541b370deeda7910ea7253b472ecc2c000614befbc68504928d0ace6afb8ac2d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:49:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:49:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:49:47 GMT
ENV TELEGRAF_VERSION=1.36.4
# Wed, 28 Jan 2026 03:49:47 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:49:47 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:49:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:49:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:49:47 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b7d7273f9660e4714a4f3a80280881a133da7a4b266dd62099a308eb162f72`  
		Last Modified: Wed, 28 Jan 2026 03:50:00 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28aadc15040b0a36abb07e3769a9f303cb26e56ef3f0d93b8d67305467d8fd`  
		Last Modified: Wed, 28 Jan 2026 03:50:03 GMT  
		Size: 2.6 MB (2563616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc81e34cf097b50b7dd067c2614b05e26095fb2414a929a91855343b1d90a521`  
		Last Modified: Wed, 28 Jan 2026 03:50:04 GMT  
		Size: 80.3 MB (80276156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b661496d98862b6bcadcc878a91c0481a10a977bd7484506964f0fa597e847e4`  
		Last Modified: Wed, 28 Jan 2026 03:50:01 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:a58b7e8c82dd5051261d6c864d491aeea150486c9e1f27c7ee855fb6a31203aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1157226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48411f51293ab3606c49c94104046ecf052e493bbfcfe2f480129ab5409030c`

```dockerfile
```

-	Layers:
	-	`sha256:da625155b1394d0acc62042503f8abc1c81a442603c6d3593589a8d4a55f6341`  
		Last Modified: Wed, 28 Jan 2026 03:50:02 GMT  
		Size: 1.1 MB (1142308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de3d21cf0caad0d90bd450ac8df7e7d30e8f0aad489474e9e436f77f5ade2fca`  
		Last Modified: Wed, 28 Jan 2026 03:50:02 GMT  
		Size: 14.9 KB (14918 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:83bc8287ed0eb1b80b20475a90d070e187731561e718f2dd3895fe06431022eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78367221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54eb1f6fb6136da60a3f40864a08a135e84bee5208c5d660116eebe674366a33`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:56:03 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:56:05 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:56:13 GMT
ENV TELEGRAF_VERSION=1.36.4
# Wed, 28 Jan 2026 03:56:13 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:56:13 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:56:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:56:13 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091ad53e26795247908fee75f1fec45378bfe7b9ed2893274f93b24025ac8c82`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9006dcde8e9ae246bba52f47cf327cff96c0b85caea2b7bb7c9054ff07b9d3`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 2.6 MB (2627637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9571296956dfa14bf2102b6281cfc90613780a517750c02daae06df9c48984`  
		Last Modified: Wed, 28 Jan 2026 03:56:29 GMT  
		Size: 71.6 MB (71599165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c402cd3a778e5774ca08af5f6640eaf81bb54e3bf015248f992dc3bedf0c94b6`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:8ae6952c3c19ba215996ca8b6bd4634c696319744b633dceb09a71bf50bdd603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1152962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71490915f7d134e9704e5bc89bfda33a5b8c3561ce98c890715d964fc114d237`

```dockerfile
```

-	Layers:
	-	`sha256:df6dda659050fe9d9dda0bd1f9f03b6be5573bf09cac3651532af6a2c3d3d82a`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 1.1 MB (1137935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56c95dceab1d5fe3c1330859a4271ff252f83fe230c9b155b95b00d6ee2a76c2`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 15.0 KB (15027 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36.4`

```console
$ docker pull telegraf@sha256:b8b78323f272928584310161a293dc3dfcf89a65e019890e5543781fe6a926eb
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
$ docker pull telegraf@sha256:6d235481ebd1f2b9f47fdb09a731dcc41696985a5b74ea439b22a475b6afb4bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.0 MB (171950866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d545d215ddd3c2c123edea474af09d885614921199b175adf42484d3639caf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:08:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:08:58 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 03:09:02 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 07 Apr 2026 03:09:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 07 Apr 2026 03:09:02 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 07 Apr 2026 03:09:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 03:09:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 03:09:02 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c3414b1d6b49c54c305584faac46aad75c67644cf4f8495e8145206d28e416`  
		Last Modified: Tue, 07 Apr 2026 01:47:02 GMT  
		Size: 24.0 MB (24038269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33783d9cba990ea068fd7b11de7ac26da4e0e7e412f7802b50d66f837c8f77e6`  
		Last Modified: Tue, 07 Apr 2026 03:09:23 GMT  
		Size: 18.9 MB (18944499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2914360d962562f729d89e57142ce9620abe1fea7f9f9064b300d64ecfccbd35`  
		Last Modified: Tue, 07 Apr 2026 03:09:22 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234c31214cb9692aefbc72448ea300445113323bddeca3f722891ffc97db61fc`  
		Last Modified: Tue, 07 Apr 2026 03:09:24 GMT  
		Size: 80.5 MB (80473597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f52cb2ca9cd952a6dd8f75a3dc608a824db3da8ad4e5fc8e36ab1d251a6ed1d`  
		Last Modified: Tue, 07 Apr 2026 03:09:22 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:a74f2eaab34ec0bd044d25f9ecf89d141410526560c0a2ec09527887b8fd7089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6670530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac22ed98a335a2c1791dfa31216f2bf80a4bd910321a051acac3364b29220416`

```dockerfile
```

-	Layers:
	-	`sha256:d6fe1417cf5b288262401bd7d92bb9f76147bc29c2169661145e5685a7c3b838`  
		Last Modified: Tue, 07 Apr 2026 03:09:22 GMT  
		Size: 6.7 MB (6656103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59ea5810b48af39ad6a8d54a1721094c0e9f47f8bb2b9a612cabd96566b2b1c9`  
		Last Modified: Tue, 07 Apr 2026 03:09:22 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:15fc82113bb56ecb61a38be93e57652129172402e5925586a704c88fad51958d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157818846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a3b5bc6eeab29c04d6f1b17ecc04caefe54778e4e806135ee9df0883e68faa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:00:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:04:20 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:04:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 04:04:27 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 07 Apr 2026 04:04:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 07 Apr 2026 04:04:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 07 Apr 2026 04:04:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 04:04:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 04:04:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a99a9abe3964725d9016ffc8402d9cffc28e94f404db8e764ca9583f2090145e`  
		Last Modified: Tue, 07 Apr 2026 00:58:42 GMT  
		Size: 44.2 MB (44207817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2a6632e49a08fc68f1ee0ec0fb4b6f38a03db30dc5ff33b611dc705110ee36`  
		Last Modified: Tue, 07 Apr 2026 02:00:47 GMT  
		Size: 21.9 MB (21942083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a771ebfd7afc5eca9ff2ad80a3ba411bb2e5946ec065365a53c7a9eaf5acdac`  
		Last Modified: Tue, 07 Apr 2026 04:04:45 GMT  
		Size: 17.7 MB (17699627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a891bb2f2058cba8c4a8bd430fe391b46be672d463afd41bf61acce0416b72d6`  
		Last Modified: Tue, 07 Apr 2026 04:04:44 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17268f16d13db6654617820e032ecbe91cf92c64ce9d19805f98154114b16f2`  
		Last Modified: Tue, 07 Apr 2026 04:04:46 GMT  
		Size: 74.0 MB (73963640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c6c50cc02c6ecb2a576608f1692aa8afdf9dacdd36567f9b604478c276e132`  
		Last Modified: Tue, 07 Apr 2026 04:04:44 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:a626c00cb88f84187b8ce2f2b745a6a27895ab464ff6e5be9cb12e0ec42b699a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6665217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:315acb8c2d98bce4d0ea209d241a3a7c03f5202326ef44520188c092a8eba18e`

```dockerfile
```

-	Layers:
	-	`sha256:3fb7f617d73ad59cfead76b7709654652d987918dce1559d945f6854adef295c`  
		Last Modified: Tue, 07 Apr 2026 04:04:44 GMT  
		Size: 6.7 MB (6650700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e92cc254c72949abc0195f93d49adf27296116745ff6d6e85dbecf8f5fbcecf8`  
		Last Modified: Tue, 07 Apr 2026 04:04:44 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:dcdf91f273c4ef463af86692ddfe909156c7446c0f21127efe4bca3f9839e635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162669961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cefcd94ab4b2fd0117f2b61eef0f14db8d451483db16b2ce08d8be6caf84232`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:19:24 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:19:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 03:19:28 GMT
ENV TELEGRAF_VERSION=1.36.4
# Tue, 07 Apr 2026 03:19:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 07 Apr 2026 03:19:28 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 07 Apr 2026 03:19:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 03:19:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 03:19:28 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af98f0879b367460715b477e9118922ba24f17d9a4ad8d70e595a9c4cf56990`  
		Last Modified: Tue, 07 Apr 2026 01:49:50 GMT  
		Size: 23.6 MB (23604705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717b13f7a2834f96d950d53a1f74c70953d30597ff61a07458413359fc723064`  
		Last Modified: Tue, 07 Apr 2026 03:19:47 GMT  
		Size: 18.9 MB (18885928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc064ce34ffb9a2d01ef8453f647784c2a4daffcb14cbb4970dc150bd58b590`  
		Last Modified: Tue, 07 Apr 2026 03:19:46 GMT  
		Size: 5.1 KB (5073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e453bbb0525bdbd717ff66723ec90915960f225e77eec6be25bf91c02fdbed9`  
		Last Modified: Tue, 07 Apr 2026 03:19:49 GMT  
		Size: 71.8 MB (71800372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa923b9a0bd31076366d661d4912909bf4a5009fa474e4b18052df6aa07699d`  
		Last Modified: Tue, 07 Apr 2026 03:19:46 GMT  
		Size: 621.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4` - unknown; unknown

```console
$ docker pull telegraf@sha256:2d9d8a436aa721777e3b0d4d9eca2c84c0355098c766c5da684fe222ead3d271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6671316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ced8eef6f6cd80642425eb9ddd9377a0d7a26c7b62d0d367f856d1db0ab3bf4`

```dockerfile
```

-	Layers:
	-	`sha256:997f9547f394a52b8ed228d51854c8c4e6e35e21d35969176f86ba2021ce85b7`  
		Last Modified: Tue, 07 Apr 2026 03:19:46 GMT  
		Size: 6.7 MB (6656779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b52911127fa7518d20f3577b818589649e1ea92044699b0d4aaebc44a285882`  
		Last Modified: Tue, 07 Apr 2026 03:19:46 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.36.4-alpine`

```console
$ docker pull telegraf@sha256:74614dd18bd8c984d8d5423d6c362da8b9a0c32543f9932660f03c1e8ae22893
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.36.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:7e104d74dd7644a3f52e10b68cf4972907df0e16d541772b9da2cd987768f243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86645547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:541b370deeda7910ea7253b472ecc2c000614befbc68504928d0ace6afb8ac2d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:49:38 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:49:39 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:49:47 GMT
ENV TELEGRAF_VERSION=1.36.4
# Wed, 28 Jan 2026 03:49:47 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:49:47 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:49:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:49:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:49:47 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b7d7273f9660e4714a4f3a80280881a133da7a4b266dd62099a308eb162f72`  
		Last Modified: Wed, 28 Jan 2026 03:50:00 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a28aadc15040b0a36abb07e3769a9f303cb26e56ef3f0d93b8d67305467d8fd`  
		Last Modified: Wed, 28 Jan 2026 03:50:03 GMT  
		Size: 2.6 MB (2563616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc81e34cf097b50b7dd067c2614b05e26095fb2414a929a91855343b1d90a521`  
		Last Modified: Wed, 28 Jan 2026 03:50:04 GMT  
		Size: 80.3 MB (80276156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b661496d98862b6bcadcc878a91c0481a10a977bd7484506964f0fa597e847e4`  
		Last Modified: Wed, 28 Jan 2026 03:50:01 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:a58b7e8c82dd5051261d6c864d491aeea150486c9e1f27c7ee855fb6a31203aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1157226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48411f51293ab3606c49c94104046ecf052e493bbfcfe2f480129ab5409030c`

```dockerfile
```

-	Layers:
	-	`sha256:da625155b1394d0acc62042503f8abc1c81a442603c6d3593589a8d4a55f6341`  
		Last Modified: Wed, 28 Jan 2026 03:50:02 GMT  
		Size: 1.1 MB (1142308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de3d21cf0caad0d90bd450ac8df7e7d30e8f0aad489474e9e436f77f5ade2fca`  
		Last Modified: Wed, 28 Jan 2026 03:50:02 GMT  
		Size: 14.9 KB (14918 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.36.4-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:83bc8287ed0eb1b80b20475a90d070e187731561e718f2dd3895fe06431022eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78367221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54eb1f6fb6136da60a3f40864a08a135e84bee5208c5d660116eebe674366a33`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:56:03 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:56:05 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:56:13 GMT
ENV TELEGRAF_VERSION=1.36.4
# Wed, 28 Jan 2026 03:56:13 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Wed, 28 Jan 2026 03:56:13 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Wed, 28 Jan 2026 03:56:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:56:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:56:13 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091ad53e26795247908fee75f1fec45378bfe7b9ed2893274f93b24025ac8c82`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9006dcde8e9ae246bba52f47cf327cff96c0b85caea2b7bb7c9054ff07b9d3`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 2.6 MB (2627637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9571296956dfa14bf2102b6281cfc90613780a517750c02daae06df9c48984`  
		Last Modified: Wed, 28 Jan 2026 03:56:29 GMT  
		Size: 71.6 MB (71599165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c402cd3a778e5774ca08af5f6640eaf81bb54e3bf015248f992dc3bedf0c94b6`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.36.4-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:8ae6952c3c19ba215996ca8b6bd4634c696319744b633dceb09a71bf50bdd603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1152962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71490915f7d134e9704e5bc89bfda33a5b8c3561ce98c890715d964fc114d237`

```dockerfile
```

-	Layers:
	-	`sha256:df6dda659050fe9d9dda0bd1f9f03b6be5573bf09cac3651532af6a2c3d3d82a`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 1.1 MB (1137935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56c95dceab1d5fe3c1330859a4271ff252f83fe230c9b155b95b00d6ee2a76c2`  
		Last Modified: Wed, 28 Jan 2026 03:56:27 GMT  
		Size: 15.0 KB (15027 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37`

```console
$ docker pull telegraf@sha256:7a0c2d3734c8e75760b52923090d16a625894d3b72ddd06c7ef8f6c37ae511da
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
$ docker pull telegraf@sha256:a7447ab3f6608f98c7a71bb55e5347d6fd8ca47a40dbaaf025eb2054fe1df552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172260234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2edb33d7fcd51950f4403c97fbee2141ccbab547e8c97b938948d6ab819f7efd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:09:26 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:09:26 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 03:09:30 GMT
ENV TELEGRAF_VERSION=1.37.3
# Tue, 07 Apr 2026 03:09:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 07 Apr 2026 03:09:30 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 07 Apr 2026 03:09:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 03:09:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 03:09:30 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c3414b1d6b49c54c305584faac46aad75c67644cf4f8495e8145206d28e416`  
		Last Modified: Tue, 07 Apr 2026 01:47:02 GMT  
		Size: 24.0 MB (24038269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44701367aa8e34f60859e0fefef6b2ebc108b1288605f9c6abbc727e96b27ec9`  
		Last Modified: Tue, 07 Apr 2026 03:09:53 GMT  
		Size: 18.9 MB (18944276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054f81f35ad102cb7b16ba5234ce250c481c9b9e8fc02329f2644dba7d9a2c05`  
		Last Modified: Tue, 07 Apr 2026 03:09:52 GMT  
		Size: 5.1 KB (5056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afc544e0dd72ec67daf420f9e0cff28e5137df7b7358e7d4fd2f1ac8d47aed0`  
		Last Modified: Tue, 07 Apr 2026 03:09:55 GMT  
		Size: 80.8 MB (80783185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b3d2ed370f8f1e109cf3ab691708b4ad6447397c85b321fb49c3d250e038b5`  
		Last Modified: Tue, 07 Apr 2026 03:09:52 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37` - unknown; unknown

```console
$ docker pull telegraf@sha256:791043f8b5da6f223fe6a7962a1f0cb5a7c60ca30cc41e4d1a543170743fd6a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6681385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1291cde4ac36178f52bc8da2ae85d19fd93565b92ef9db4d0c47a027a7653e97`

```dockerfile
```

-	Layers:
	-	`sha256:4626d1f2042977341cc81f363493c10a86a2fe544bc89a566eda84273ee8a0f7`  
		Last Modified: Tue, 07 Apr 2026 03:09:53 GMT  
		Size: 6.7 MB (6666958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d210f0f76e42b13ae29f0b25de8c52367543eda26bd8410f2ec142ae991d255`  
		Last Modified: Tue, 07 Apr 2026 03:09:52 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:979a9d8363d7eb9c23dfa00f4e8649b4ce8ae6f8ed1c06a52dba12eb83d850a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.5 MB (158472872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b5ffbd0760502c3afe443c1e6500bf8d36089832d934be0aa9c75e41f94d541`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:00:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:04:24 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:04:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 04:04:31 GMT
ENV TELEGRAF_VERSION=1.37.3
# Tue, 07 Apr 2026 04:04:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 07 Apr 2026 04:04:31 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 07 Apr 2026 04:04:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 04:04:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 04:04:31 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a99a9abe3964725d9016ffc8402d9cffc28e94f404db8e764ca9583f2090145e`  
		Last Modified: Tue, 07 Apr 2026 00:58:42 GMT  
		Size: 44.2 MB (44207817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2a6632e49a08fc68f1ee0ec0fb4b6f38a03db30dc5ff33b611dc705110ee36`  
		Last Modified: Tue, 07 Apr 2026 02:00:47 GMT  
		Size: 21.9 MB (21942083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98255551961ffc9e87f09095aac921b5ddac76bfd6ab944f029a2c4ad480582d`  
		Last Modified: Tue, 07 Apr 2026 04:04:48 GMT  
		Size: 17.7 MB (17699869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85645cc2523cfa211e21e06702241b8cedafa94ebf642229aad6578f42c1290d`  
		Last Modified: Tue, 07 Apr 2026 04:04:47 GMT  
		Size: 5.1 KB (5054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0068fbb4b31d537c1c78e7cabe1435ad0f8c64be48e345ea04462fd6ed28afc0`  
		Last Modified: Tue, 07 Apr 2026 04:04:50 GMT  
		Size: 74.6 MB (74617425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525bc0728c1cf018057b8d785441d52a03a78d45065703382dad571ad73aa0d8`  
		Last Modified: Tue, 07 Apr 2026 04:04:47 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37` - unknown; unknown

```console
$ docker pull telegraf@sha256:aa0943df08e200e37ba9d092c558006d768827f6ea5eebdf6fb6b982e2d84f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e74b4143faf27c3d2172b737b9fe5d69c8deddc5844a88f7b6452b264832f50d`

```dockerfile
```

-	Layers:
	-	`sha256:a6ce20b130c1df8ca839ecf6bfd5a2a98e50b6d2e6dc48ba9cd596e7f5b0a599`  
		Last Modified: Tue, 07 Apr 2026 04:04:48 GMT  
		Size: 6.7 MB (6661555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:291fee3fb25654a9e519beb199761ffef57ee9e68d5f9d0c172a353066ff8e09`  
		Last Modified: Tue, 07 Apr 2026 04:04:48 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:0c9cb52c29753d5da5ceb88ec0983aee5ee3e90a0bd49a9bc0a04c23a9aeec56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (163040608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b333dbe1a719bdfa9a39a7a501e734e5befb9650426cc0ae2918951a328da5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:19:24 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:19:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 03:20:00 GMT
ENV TELEGRAF_VERSION=1.37.3
# Tue, 07 Apr 2026 03:20:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 07 Apr 2026 03:20:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 07 Apr 2026 03:20:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 03:20:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 03:20:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af98f0879b367460715b477e9118922ba24f17d9a4ad8d70e595a9c4cf56990`  
		Last Modified: Tue, 07 Apr 2026 01:49:50 GMT  
		Size: 23.6 MB (23604705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717b13f7a2834f96d950d53a1f74c70953d30597ff61a07458413359fc723064`  
		Last Modified: Tue, 07 Apr 2026 03:19:47 GMT  
		Size: 18.9 MB (18885928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc064ce34ffb9a2d01ef8453f647784c2a4daffcb14cbb4970dc150bd58b590`  
		Last Modified: Tue, 07 Apr 2026 03:19:46 GMT  
		Size: 5.1 KB (5073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359f65ed31a0843525337d1c4bd9610fb83245eada776097808171eeb572d0fd`  
		Last Modified: Tue, 07 Apr 2026 03:20:19 GMT  
		Size: 72.2 MB (72171017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d7498b00ee7ba1930b778a03ec7850e2e2c6aeab74c53f65ddb3afcbafb35f`  
		Last Modified: Tue, 07 Apr 2026 03:20:17 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37` - unknown; unknown

```console
$ docker pull telegraf@sha256:f92cb28181c91e2d6338fbf9152f9d8a5f10759937052dfdb1928392d3a0f41b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6682171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d2bbd4d84d24f8ef2f97bd95463d641f65d0e4ca09f51b81578974eb6b39849`

```dockerfile
```

-	Layers:
	-	`sha256:f0f9ec1afc26896279e26c464372faaba5e6c9788d1fda36c95ebf7ec59e86fe`  
		Last Modified: Tue, 07 Apr 2026 03:20:17 GMT  
		Size: 6.7 MB (6667634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d51cda79175852026462e46076a0ad5c3aaab7357cd68e7bc121f0dc93add12`  
		Last Modified: Tue, 07 Apr 2026 03:20:17 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37-alpine`

```console
$ docker pull telegraf@sha256:a550e63a2efbea4b49596e475f0fcd3b057ff2ab0dfc8102357de289ee342a37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:fba66fd8b08dc6e56336289fd91c0b9c055b5431b1ac6f0cb3c5b0203b24d450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86946044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38efb96d204dcce61a2419f13705ddf967966bbf6c20b8dc214d6cd4917df5cc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 22:13:06 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 23 Feb 2026 22:13:07 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 23 Feb 2026 22:13:15 GMT
ENV TELEGRAF_VERSION=1.37.3
# Mon, 23 Feb 2026 22:13:15 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 23 Feb 2026 22:13:15 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Feb 2026 22:13:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Feb 2026 22:13:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 22:13:15 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2b56c151750e24306076f9157dce93616ec037d271702f125dc64fbf3376f8`  
		Last Modified: Mon, 23 Feb 2026 22:13:30 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff331311971b9e1b3df00d187242872c6a7167b0fa5eb1b83bf07f57f6bd227`  
		Last Modified: Mon, 23 Feb 2026 22:13:30 GMT  
		Size: 2.6 MB (2563613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749b176fa3df8ddfa0c79b45cb78b9caf938ca77b7d56b923cdb8d9280c85548`  
		Last Modified: Mon, 23 Feb 2026 22:13:33 GMT  
		Size: 80.6 MB (80576658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a622797146e400edbb8a20860c8044210bb4ddf360b881dd59f657a0178e56`  
		Last Modified: Mon, 23 Feb 2026 22:13:30 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:dbaf7ed8916c29f7e0e480a7ad699dbc11e6ff21f59b298ac7bc4c687f919ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1168683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b161c64ca482da5f21d71566f132f54ee64beb84f28a79454afce77c61e7ad74`

```dockerfile
```

-	Layers:
	-	`sha256:0ad1ed01319ca47cfb93e453ec6fce2996425a3ef91fb812891757a8a27d72c6`  
		Last Modified: Mon, 23 Feb 2026 22:13:30 GMT  
		Size: 1.2 MB (1153465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:841e3534e20e0f7236187feb211ea64b35f00fbef79dd247d04d44865d348a5d`  
		Last Modified: Mon, 23 Feb 2026 22:13:30 GMT  
		Size: 15.2 KB (15218 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:f27c6f05cce7d68495838dcbbe51d1995f3ba235846d6753718f5b2cd8a7f603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78730556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5048f1f9cdf423929349c19bb659110cd4c7e1ab38dff7597763063c5a1978b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 22:12:02 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 23 Feb 2026 22:12:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 23 Feb 2026 22:12:09 GMT
ENV TELEGRAF_VERSION=1.37.3
# Mon, 23 Feb 2026 22:12:09 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 23 Feb 2026 22:12:09 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Feb 2026 22:12:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Feb 2026 22:12:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 22:12:09 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f365fa2017a849f86d84f3f3776e527b8ff2fb4628dfa52b2e2726747ba9a5f`  
		Last Modified: Mon, 23 Feb 2026 22:12:22 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01dde69daba6471771a33e89fc18e2ef827eac0bbebbfa518372b5614a4c5072`  
		Last Modified: Mon, 23 Feb 2026 22:12:23 GMT  
		Size: 2.6 MB (2627610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83fb53f42b0075065a38f3acdda1775b06ee78f844307d7125a10b6688253f62`  
		Last Modified: Mon, 23 Feb 2026 22:12:24 GMT  
		Size: 72.0 MB (71962529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d896748b58358906c78fda48ddade4bd1df0e660097580f49b6f08d0bb041131`  
		Last Modified: Mon, 23 Feb 2026 22:12:22 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:f2ad750ecb35ac8a316aa4496da66885dfc42a651a503859707823f2d6f4ca2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1164446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b3b3372362c4275569df86547f57711280021d198691725283f623157d5487`

```dockerfile
```

-	Layers:
	-	`sha256:84a7770deb78578c6e010d0e4268d870b145b32e787666e68441fd2377878852`  
		Last Modified: Mon, 23 Feb 2026 22:12:22 GMT  
		Size: 1.1 MB (1149104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b83295c00d09abd5a3a9c39ebd649a814a4169ff62cc5041580c6c7c1bfd6e5`  
		Last Modified: Mon, 23 Feb 2026 22:12:23 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37.3`

```console
$ docker pull telegraf@sha256:7a0c2d3734c8e75760b52923090d16a625894d3b72ddd06c7ef8f6c37ae511da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37.3` - linux; amd64

```console
$ docker pull telegraf@sha256:a7447ab3f6608f98c7a71bb55e5347d6fd8ca47a40dbaaf025eb2054fe1df552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172260234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2edb33d7fcd51950f4403c97fbee2141ccbab547e8c97b938948d6ab819f7efd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:09:26 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:09:26 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 03:09:30 GMT
ENV TELEGRAF_VERSION=1.37.3
# Tue, 07 Apr 2026 03:09:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 07 Apr 2026 03:09:30 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 07 Apr 2026 03:09:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 03:09:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 03:09:30 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c3414b1d6b49c54c305584faac46aad75c67644cf4f8495e8145206d28e416`  
		Last Modified: Tue, 07 Apr 2026 01:47:02 GMT  
		Size: 24.0 MB (24038269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44701367aa8e34f60859e0fefef6b2ebc108b1288605f9c6abbc727e96b27ec9`  
		Last Modified: Tue, 07 Apr 2026 03:09:53 GMT  
		Size: 18.9 MB (18944276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054f81f35ad102cb7b16ba5234ce250c481c9b9e8fc02329f2644dba7d9a2c05`  
		Last Modified: Tue, 07 Apr 2026 03:09:52 GMT  
		Size: 5.1 KB (5056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afc544e0dd72ec67daf420f9e0cff28e5137df7b7358e7d4fd2f1ac8d47aed0`  
		Last Modified: Tue, 07 Apr 2026 03:09:55 GMT  
		Size: 80.8 MB (80783185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b3d2ed370f8f1e109cf3ab691708b4ad6447397c85b321fb49c3d250e038b5`  
		Last Modified: Tue, 07 Apr 2026 03:09:52 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:791043f8b5da6f223fe6a7962a1f0cb5a7c60ca30cc41e4d1a543170743fd6a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6681385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1291cde4ac36178f52bc8da2ae85d19fd93565b92ef9db4d0c47a027a7653e97`

```dockerfile
```

-	Layers:
	-	`sha256:4626d1f2042977341cc81f363493c10a86a2fe544bc89a566eda84273ee8a0f7`  
		Last Modified: Tue, 07 Apr 2026 03:09:53 GMT  
		Size: 6.7 MB (6666958 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d210f0f76e42b13ae29f0b25de8c52367543eda26bd8410f2ec142ae991d255`  
		Last Modified: Tue, 07 Apr 2026 03:09:52 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:979a9d8363d7eb9c23dfa00f4e8649b4ce8ae6f8ed1c06a52dba12eb83d850a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.5 MB (158472872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b5ffbd0760502c3afe443c1e6500bf8d36089832d934be0aa9c75e41f94d541`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:00:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:04:24 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:04:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 04:04:31 GMT
ENV TELEGRAF_VERSION=1.37.3
# Tue, 07 Apr 2026 04:04:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 07 Apr 2026 04:04:31 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 07 Apr 2026 04:04:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 04:04:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 04:04:31 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a99a9abe3964725d9016ffc8402d9cffc28e94f404db8e764ca9583f2090145e`  
		Last Modified: Tue, 07 Apr 2026 00:58:42 GMT  
		Size: 44.2 MB (44207817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2a6632e49a08fc68f1ee0ec0fb4b6f38a03db30dc5ff33b611dc705110ee36`  
		Last Modified: Tue, 07 Apr 2026 02:00:47 GMT  
		Size: 21.9 MB (21942083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98255551961ffc9e87f09095aac921b5ddac76bfd6ab944f029a2c4ad480582d`  
		Last Modified: Tue, 07 Apr 2026 04:04:48 GMT  
		Size: 17.7 MB (17699869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85645cc2523cfa211e21e06702241b8cedafa94ebf642229aad6578f42c1290d`  
		Last Modified: Tue, 07 Apr 2026 04:04:47 GMT  
		Size: 5.1 KB (5054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0068fbb4b31d537c1c78e7cabe1435ad0f8c64be48e345ea04462fd6ed28afc0`  
		Last Modified: Tue, 07 Apr 2026 04:04:50 GMT  
		Size: 74.6 MB (74617425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525bc0728c1cf018057b8d785441d52a03a78d45065703382dad571ad73aa0d8`  
		Last Modified: Tue, 07 Apr 2026 04:04:47 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:aa0943df08e200e37ba9d092c558006d768827f6ea5eebdf6fb6b982e2d84f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6676072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e74b4143faf27c3d2172b737b9fe5d69c8deddc5844a88f7b6452b264832f50d`

```dockerfile
```

-	Layers:
	-	`sha256:a6ce20b130c1df8ca839ecf6bfd5a2a98e50b6d2e6dc48ba9cd596e7f5b0a599`  
		Last Modified: Tue, 07 Apr 2026 04:04:48 GMT  
		Size: 6.7 MB (6661555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:291fee3fb25654a9e519beb199761ffef57ee9e68d5f9d0c172a353066ff8e09`  
		Last Modified: Tue, 07 Apr 2026 04:04:48 GMT  
		Size: 14.5 KB (14517 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:0c9cb52c29753d5da5ceb88ec0983aee5ee3e90a0bd49a9bc0a04c23a9aeec56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (163040608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b333dbe1a719bdfa9a39a7a501e734e5befb9650426cc0ae2918951a328da5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:19:24 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:19:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 03:20:00 GMT
ENV TELEGRAF_VERSION=1.37.3
# Tue, 07 Apr 2026 03:20:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 07 Apr 2026 03:20:00 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 07 Apr 2026 03:20:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 03:20:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 03:20:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af98f0879b367460715b477e9118922ba24f17d9a4ad8d70e595a9c4cf56990`  
		Last Modified: Tue, 07 Apr 2026 01:49:50 GMT  
		Size: 23.6 MB (23604705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717b13f7a2834f96d950d53a1f74c70953d30597ff61a07458413359fc723064`  
		Last Modified: Tue, 07 Apr 2026 03:19:47 GMT  
		Size: 18.9 MB (18885928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc064ce34ffb9a2d01ef8453f647784c2a4daffcb14cbb4970dc150bd58b590`  
		Last Modified: Tue, 07 Apr 2026 03:19:46 GMT  
		Size: 5.1 KB (5073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:359f65ed31a0843525337d1c4bd9610fb83245eada776097808171eeb572d0fd`  
		Last Modified: Tue, 07 Apr 2026 03:20:19 GMT  
		Size: 72.2 MB (72171017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d7498b00ee7ba1930b778a03ec7850e2e2c6aeab74c53f65ddb3afcbafb35f`  
		Last Modified: Tue, 07 Apr 2026 03:20:17 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.3` - unknown; unknown

```console
$ docker pull telegraf@sha256:f92cb28181c91e2d6338fbf9152f9d8a5f10759937052dfdb1928392d3a0f41b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6682171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d2bbd4d84d24f8ef2f97bd95463d641f65d0e4ca09f51b81578974eb6b39849`

```dockerfile
```

-	Layers:
	-	`sha256:f0f9ec1afc26896279e26c464372faaba5e6c9788d1fda36c95ebf7ec59e86fe`  
		Last Modified: Tue, 07 Apr 2026 03:20:17 GMT  
		Size: 6.7 MB (6667634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d51cda79175852026462e46076a0ad5c3aaab7357cd68e7bc121f0dc93add12`  
		Last Modified: Tue, 07 Apr 2026 03:20:17 GMT  
		Size: 14.5 KB (14537 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.37.3-alpine`

```console
$ docker pull telegraf@sha256:a550e63a2efbea4b49596e475f0fcd3b057ff2ab0dfc8102357de289ee342a37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.37.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:fba66fd8b08dc6e56336289fd91c0b9c055b5431b1ac6f0cb3c5b0203b24d450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86946044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38efb96d204dcce61a2419f13705ddf967966bbf6c20b8dc214d6cd4917df5cc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 22:13:06 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 23 Feb 2026 22:13:07 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 23 Feb 2026 22:13:15 GMT
ENV TELEGRAF_VERSION=1.37.3
# Mon, 23 Feb 2026 22:13:15 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 23 Feb 2026 22:13:15 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Feb 2026 22:13:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Feb 2026 22:13:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 22:13:15 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2b56c151750e24306076f9157dce93616ec037d271702f125dc64fbf3376f8`  
		Last Modified: Mon, 23 Feb 2026 22:13:30 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff331311971b9e1b3df00d187242872c6a7167b0fa5eb1b83bf07f57f6bd227`  
		Last Modified: Mon, 23 Feb 2026 22:13:30 GMT  
		Size: 2.6 MB (2563613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749b176fa3df8ddfa0c79b45cb78b9caf938ca77b7d56b923cdb8d9280c85548`  
		Last Modified: Mon, 23 Feb 2026 22:13:33 GMT  
		Size: 80.6 MB (80576658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a622797146e400edbb8a20860c8044210bb4ddf360b881dd59f657a0178e56`  
		Last Modified: Mon, 23 Feb 2026 22:13:30 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:dbaf7ed8916c29f7e0e480a7ad699dbc11e6ff21f59b298ac7bc4c687f919ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1168683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b161c64ca482da5f21d71566f132f54ee64beb84f28a79454afce77c61e7ad74`

```dockerfile
```

-	Layers:
	-	`sha256:0ad1ed01319ca47cfb93e453ec6fce2996425a3ef91fb812891757a8a27d72c6`  
		Last Modified: Mon, 23 Feb 2026 22:13:30 GMT  
		Size: 1.2 MB (1153465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:841e3534e20e0f7236187feb211ea64b35f00fbef79dd247d04d44865d348a5d`  
		Last Modified: Mon, 23 Feb 2026 22:13:30 GMT  
		Size: 15.2 KB (15218 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.37.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:f27c6f05cce7d68495838dcbbe51d1995f3ba235846d6753718f5b2cd8a7f603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.7 MB (78730556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5048f1f9cdf423929349c19bb659110cd4c7e1ab38dff7597763063c5a1978b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Mon, 23 Feb 2026 22:12:02 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 23 Feb 2026 22:12:04 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 23 Feb 2026 22:12:09 GMT
ENV TELEGRAF_VERSION=1.37.3
# Mon, 23 Feb 2026 22:12:09 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 23 Feb 2026 22:12:09 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 23 Feb 2026 22:12:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 23 Feb 2026 22:12:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 23 Feb 2026 22:12:09 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f365fa2017a849f86d84f3f3776e527b8ff2fb4628dfa52b2e2726747ba9a5f`  
		Last Modified: Mon, 23 Feb 2026 22:12:22 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01dde69daba6471771a33e89fc18e2ef827eac0bbebbfa518372b5614a4c5072`  
		Last Modified: Mon, 23 Feb 2026 22:12:23 GMT  
		Size: 2.6 MB (2627610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83fb53f42b0075065a38f3acdda1775b06ee78f844307d7125a10b6688253f62`  
		Last Modified: Mon, 23 Feb 2026 22:12:24 GMT  
		Size: 72.0 MB (71962529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d896748b58358906c78fda48ddade4bd1df0e660097580f49b6f08d0bb041131`  
		Last Modified: Mon, 23 Feb 2026 22:12:22 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.37.3-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:f2ad750ecb35ac8a316aa4496da66885dfc42a651a503859707823f2d6f4ca2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1164446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b3b3372362c4275569df86547f57711280021d198691725283f623157d5487`

```dockerfile
```

-	Layers:
	-	`sha256:84a7770deb78578c6e010d0e4268d870b145b32e787666e68441fd2377878852`  
		Last Modified: Mon, 23 Feb 2026 22:12:22 GMT  
		Size: 1.1 MB (1149104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b83295c00d09abd5a3a9c39ebd649a814a4169ff62cc5041580c6c7c1bfd6e5`  
		Last Modified: Mon, 23 Feb 2026 22:12:23 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.38`

```console
$ docker pull telegraf@sha256:74fa2ce3d3e0eba543bf67d022c1c6bd7e7716f0cabb53641b5696a4bd915c6f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.38` - linux; amd64

```console
$ docker pull telegraf@sha256:17b8db94dc0db85b9e63b5854186dd6814604cc062315ec6cda62eebd95b197f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.0 MB (172992401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d909a4eb1b3349f8d033f3a16e144b2544a748098322efb34072be188aa825eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:08:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:08:58 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 03:09:38 GMT
ENV TELEGRAF_VERSION=1.38.2
# Tue, 07 Apr 2026 03:09:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 07 Apr 2026 03:09:38 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 07 Apr 2026 03:09:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 03:09:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 03:09:38 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c3414b1d6b49c54c305584faac46aad75c67644cf4f8495e8145206d28e416`  
		Last Modified: Tue, 07 Apr 2026 01:47:02 GMT  
		Size: 24.0 MB (24038269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33783d9cba990ea068fd7b11de7ac26da4e0e7e412f7802b50d66f837c8f77e6`  
		Last Modified: Tue, 07 Apr 2026 03:09:23 GMT  
		Size: 18.9 MB (18944499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2914360d962562f729d89e57142ce9620abe1fea7f9f9064b300d64ecfccbd35`  
		Last Modified: Tue, 07 Apr 2026 03:09:22 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f21f12f1a5be3b7b94fc249297def9dc29522f795c5133f18b6a232fdbd1b9`  
		Last Modified: Tue, 07 Apr 2026 03:09:58 GMT  
		Size: 81.5 MB (81515133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063d9ba824d7baba0fc96f43b2b2f68552320f7aab90377d104b7aa5f4e15ab6`  
		Last Modified: Tue, 07 Apr 2026 03:09:55 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38` - unknown; unknown

```console
$ docker pull telegraf@sha256:901c98af60f94359ae6148a5b61b028c6eedcc2281739ab6896b1e229f7ce122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6690035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f01e105f8304a9be0d4072b1cb915fa618282ceab9001c4b46dd5410627b10d`

```dockerfile
```

-	Layers:
	-	`sha256:cb15165e332ae744a86b2b698d6d36a9e1b59392effb48116d1c512840516a1a`  
		Last Modified: Tue, 07 Apr 2026 03:09:56 GMT  
		Size: 6.7 MB (6675306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:517668c9c7cb30a0989eb10ec5e2e58abaea85698ac205cf4ccf3dab2b091cd9`  
		Last Modified: Tue, 07 Apr 2026 03:09:55 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:73eb27b50ecd1d595f8e376dcabed624247fb6409d6ce68605b6f3dd0ba3ff2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159178851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fbcfba407b4d2a60bf7018485a3544151914ed4f06aeafb80f9f66ffca88c12`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:00:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:04:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:04:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 04:04:43 GMT
ENV TELEGRAF_VERSION=1.38.2
# Tue, 07 Apr 2026 04:04:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 07 Apr 2026 04:04:43 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 07 Apr 2026 04:04:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 04:04:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 04:04:43 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a99a9abe3964725d9016ffc8402d9cffc28e94f404db8e764ca9583f2090145e`  
		Last Modified: Tue, 07 Apr 2026 00:58:42 GMT  
		Size: 44.2 MB (44207817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2a6632e49a08fc68f1ee0ec0fb4b6f38a03db30dc5ff33b611dc705110ee36`  
		Last Modified: Tue, 07 Apr 2026 02:00:47 GMT  
		Size: 21.9 MB (21942083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7064aee1b881fe04020815950097ba6772db2636b02e8935f9c796a09e796a79`  
		Last Modified: Tue, 07 Apr 2026 04:05:04 GMT  
		Size: 17.7 MB (17699660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9900d1dbddf68ca748bccdf8d31399c4ca7dc7ea5b3c55162425bb6e089b125`  
		Last Modified: Tue, 07 Apr 2026 04:05:03 GMT  
		Size: 5.1 KB (5069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393b0bb5ab0f51cddec2eddf26669b13eb02c3b9983b6462412ebe82b5b32aff`  
		Last Modified: Tue, 07 Apr 2026 04:05:06 GMT  
		Size: 75.3 MB (75323599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac2c2d5867bde037f0b47e61bd6ffd30115b0990bb4380e909484972b1b750c`  
		Last Modified: Tue, 07 Apr 2026 04:05:03 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38` - unknown; unknown

```console
$ docker pull telegraf@sha256:8c4c66654609a89100eef26c438f4577c0c3174e56fb7de10c3ac8bca88b74d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6684738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676e28d9f450becb09d5169b4ea63eb95d8d35fa476521fc9e84344bcf1f8546`

```dockerfile
```

-	Layers:
	-	`sha256:9957d7ca43a202adae172de2acf656d58953b46d5afd8db2f4749cb6181d4821`  
		Last Modified: Tue, 07 Apr 2026 04:05:04 GMT  
		Size: 6.7 MB (6669911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e11abba1d2c7436d90ee2bc25b60a3238a2757de4a91846db7f9ae8b77abd1cc`  
		Last Modified: Tue, 07 Apr 2026 04:05:03 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:3d7c496c2bcb9590de0849d0d3d70bbcf157d0c9cbef9ae9dfc1830a91a15621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163724198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:164847084d33466f2bf9d1f8f00e29cb7f32daec30e6f4e341271393a27bf425`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:20:23 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:20:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 03:20:27 GMT
ENV TELEGRAF_VERSION=1.38.2
# Tue, 07 Apr 2026 03:20:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 07 Apr 2026 03:20:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 07 Apr 2026 03:20:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 03:20:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 03:20:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af98f0879b367460715b477e9118922ba24f17d9a4ad8d70e595a9c4cf56990`  
		Last Modified: Tue, 07 Apr 2026 01:49:50 GMT  
		Size: 23.6 MB (23604705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053aa2f9ecb5253e7f30ffdda533ae9361ea13704b633656b1038c8af8b5ec87`  
		Last Modified: Tue, 07 Apr 2026 03:20:49 GMT  
		Size: 18.9 MB (18885921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49086742a58fe18731758318a8d8c92bcb86f8fe223c0b2381630a55ae284cdf`  
		Last Modified: Tue, 07 Apr 2026 03:20:48 GMT  
		Size: 5.1 KB (5073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d204d82c3153763626d0596b405467834c7a2c3308e4258b90de7de44948aa4`  
		Last Modified: Tue, 07 Apr 2026 03:20:50 GMT  
		Size: 72.9 MB (72854613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41550f6dbf91ed385e676570e8b5450dba4252bd1ebeb3dccc7277c9e5cbb3b5`  
		Last Modified: Tue, 07 Apr 2026 03:20:48 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38` - unknown; unknown

```console
$ docker pull telegraf@sha256:4b27d1b213c48659610976f3a14fa75495ef62b4c69da25a18623903a676d22b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6690845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7324c416edb25f1de66cb95c043b7229c62b2636257de46ce07b3315ed29ea3c`

```dockerfile
```

-	Layers:
	-	`sha256:393e1eed36170b31e4170499743574ce62ba19d3e131e28e4bbd1981ec192389`  
		Last Modified: Tue, 07 Apr 2026 03:20:49 GMT  
		Size: 6.7 MB (6675994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c154c7bf13b7ca0105a6cb1205162bc1ae5eb9d34a0622f97e0e624199fb1d6d`  
		Last Modified: Tue, 07 Apr 2026 03:20:48 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.38-alpine`

```console
$ docker pull telegraf@sha256:811335001118729cd2bdbcf0aaa88fae62102ab85745bf5f4a0ed60cba56de4e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.38-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:15c787ed509753ff1c98af9c858bc4e79a8838e2f97f9da94808690f237954a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87671535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d74b6eeb9d11ffd3cf0526e2dfd611c3f1a047bee5ab27f89f68f30cce3a66`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Mon, 30 Mar 2026 20:22:43 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 30 Mar 2026 20:22:44 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 30 Mar 2026 20:22:52 GMT
ENV TELEGRAF_VERSION=1.38.2
# Mon, 30 Mar 2026 20:22:52 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 30 Mar 2026 20:22:52 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 30 Mar 2026 20:22:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 30 Mar 2026 20:22:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 30 Mar 2026 20:22:52 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f3ac74f06ef64597e0008d5b58e2d631cbc2a1c7c8d7827de7f6084ffd1384`  
		Last Modified: Mon, 30 Mar 2026 20:23:07 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841b2cba4b94e9cabe8821efc5c269224dc910b9f66659d5a0118790408f9f64`  
		Last Modified: Mon, 30 Mar 2026 20:23:08 GMT  
		Size: 2.6 MB (2563409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22318848ab211de8fbcfbd33472f3c9a9f45e5bf40b3964fd587be331ef0cfff`  
		Last Modified: Mon, 30 Mar 2026 20:23:10 GMT  
		Size: 81.3 MB (81302351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f3b3d70a34cca73560581366bf1aa5a7a571294392984eb390146e1a80a300`  
		Last Modified: Mon, 30 Mar 2026 20:23:07 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c45de09e7ba9157e9b403a2dd99453df7bee97206572dabc5092a953691be95a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1176730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03720b29716f6c0b29dbdaaee3000ef67a64556f9a2281d4cac081d6d996656`

```dockerfile
```

-	Layers:
	-	`sha256:98f0364ff7dd919bdcd1b7b1403d67ffa52a2b0edc4c62886b0e5011b3d3fc09`  
		Last Modified: Mon, 30 Mar 2026 20:23:07 GMT  
		Size: 1.2 MB (1161511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ee92bd2e1843be3aaa75cc44cd91b73eaba636edd0cc70546201ffdd09dd9d0`  
		Last Modified: Mon, 30 Mar 2026 20:23:07 GMT  
		Size: 15.2 KB (15219 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:fb0afd49cd58018b245cea4961f220c244fc777aa1ca0753135afd7c1f59a630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79408705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc70a72097954c4dd9b3106a74912f37b0a24e864006c9d69d2d1dcbbde7e87`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Mon, 30 Mar 2026 20:23:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 30 Mar 2026 20:23:01 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 30 Mar 2026 20:23:09 GMT
ENV TELEGRAF_VERSION=1.38.2
# Mon, 30 Mar 2026 20:23:09 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 30 Mar 2026 20:23:09 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 30 Mar 2026 20:23:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 30 Mar 2026 20:23:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 30 Mar 2026 20:23:09 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929ce7d3c4f4050324790939845bf90248d29e90794fd46af445c1b82fa8e3ea`  
		Last Modified: Mon, 30 Mar 2026 20:23:23 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2376aa1e3858066a43b2936816204d70c2b668fa25a029d43112bb6fde89fc0e`  
		Last Modified: Mon, 30 Mar 2026 20:23:23 GMT  
		Size: 2.6 MB (2627416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572e1b4bba075fe67f8adfc96feb476ce9866df13a73405592fb7efc167a67a3`  
		Last Modified: Mon, 30 Mar 2026 20:23:25 GMT  
		Size: 72.6 MB (72640871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b84aaa694985c4eda65e869bf5da5464e1a8a2d08ceb445751e354912483b0`  
		Last Modified: Mon, 30 Mar 2026 20:23:23 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:936b6b08489b822579b383270e0805734d6dfceff3312eb28064c847078d400e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1172492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97cf381f8dcb2b3c9f182fa9c1b572003933f561a664db9074cf1c6ae7afb654`

```dockerfile
```

-	Layers:
	-	`sha256:4a8a6a2dc5feb376c8b91acda685d81ccc02f798d46c259afc3890bbe6e1601d`  
		Last Modified: Mon, 30 Mar 2026 20:23:23 GMT  
		Size: 1.2 MB (1157150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:020ec74ea2d5779e6a975977b3f564113afe329c270a94159417df24fb421131`  
		Last Modified: Mon, 30 Mar 2026 20:23:23 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.38.2`

```console
$ docker pull telegraf@sha256:74fa2ce3d3e0eba543bf67d022c1c6bd7e7716f0cabb53641b5696a4bd915c6f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.38.2` - linux; amd64

```console
$ docker pull telegraf@sha256:17b8db94dc0db85b9e63b5854186dd6814604cc062315ec6cda62eebd95b197f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.0 MB (172992401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d909a4eb1b3349f8d033f3a16e144b2544a748098322efb34072be188aa825eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:08:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:08:58 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 03:09:38 GMT
ENV TELEGRAF_VERSION=1.38.2
# Tue, 07 Apr 2026 03:09:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 07 Apr 2026 03:09:38 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 07 Apr 2026 03:09:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 03:09:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 03:09:38 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c3414b1d6b49c54c305584faac46aad75c67644cf4f8495e8145206d28e416`  
		Last Modified: Tue, 07 Apr 2026 01:47:02 GMT  
		Size: 24.0 MB (24038269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33783d9cba990ea068fd7b11de7ac26da4e0e7e412f7802b50d66f837c8f77e6`  
		Last Modified: Tue, 07 Apr 2026 03:09:23 GMT  
		Size: 18.9 MB (18944499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2914360d962562f729d89e57142ce9620abe1fea7f9f9064b300d64ecfccbd35`  
		Last Modified: Tue, 07 Apr 2026 03:09:22 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f21f12f1a5be3b7b94fc249297def9dc29522f795c5133f18b6a232fdbd1b9`  
		Last Modified: Tue, 07 Apr 2026 03:09:58 GMT  
		Size: 81.5 MB (81515133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063d9ba824d7baba0fc96f43b2b2f68552320f7aab90377d104b7aa5f4e15ab6`  
		Last Modified: Tue, 07 Apr 2026 03:09:55 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38.2` - unknown; unknown

```console
$ docker pull telegraf@sha256:901c98af60f94359ae6148a5b61b028c6eedcc2281739ab6896b1e229f7ce122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6690035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f01e105f8304a9be0d4072b1cb915fa618282ceab9001c4b46dd5410627b10d`

```dockerfile
```

-	Layers:
	-	`sha256:cb15165e332ae744a86b2b698d6d36a9e1b59392effb48116d1c512840516a1a`  
		Last Modified: Tue, 07 Apr 2026 03:09:56 GMT  
		Size: 6.7 MB (6675306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:517668c9c7cb30a0989eb10ec5e2e58abaea85698ac205cf4ccf3dab2b091cd9`  
		Last Modified: Tue, 07 Apr 2026 03:09:55 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38.2` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:73eb27b50ecd1d595f8e376dcabed624247fb6409d6ce68605b6f3dd0ba3ff2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159178851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fbcfba407b4d2a60bf7018485a3544151914ed4f06aeafb80f9f66ffca88c12`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:00:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:04:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:04:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 04:04:43 GMT
ENV TELEGRAF_VERSION=1.38.2
# Tue, 07 Apr 2026 04:04:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 07 Apr 2026 04:04:43 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 07 Apr 2026 04:04:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 04:04:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 04:04:43 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a99a9abe3964725d9016ffc8402d9cffc28e94f404db8e764ca9583f2090145e`  
		Last Modified: Tue, 07 Apr 2026 00:58:42 GMT  
		Size: 44.2 MB (44207817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2a6632e49a08fc68f1ee0ec0fb4b6f38a03db30dc5ff33b611dc705110ee36`  
		Last Modified: Tue, 07 Apr 2026 02:00:47 GMT  
		Size: 21.9 MB (21942083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7064aee1b881fe04020815950097ba6772db2636b02e8935f9c796a09e796a79`  
		Last Modified: Tue, 07 Apr 2026 04:05:04 GMT  
		Size: 17.7 MB (17699660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9900d1dbddf68ca748bccdf8d31399c4ca7dc7ea5b3c55162425bb6e089b125`  
		Last Modified: Tue, 07 Apr 2026 04:05:03 GMT  
		Size: 5.1 KB (5069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393b0bb5ab0f51cddec2eddf26669b13eb02c3b9983b6462412ebe82b5b32aff`  
		Last Modified: Tue, 07 Apr 2026 04:05:06 GMT  
		Size: 75.3 MB (75323599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac2c2d5867bde037f0b47e61bd6ffd30115b0990bb4380e909484972b1b750c`  
		Last Modified: Tue, 07 Apr 2026 04:05:03 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38.2` - unknown; unknown

```console
$ docker pull telegraf@sha256:8c4c66654609a89100eef26c438f4577c0c3174e56fb7de10c3ac8bca88b74d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6684738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676e28d9f450becb09d5169b4ea63eb95d8d35fa476521fc9e84344bcf1f8546`

```dockerfile
```

-	Layers:
	-	`sha256:9957d7ca43a202adae172de2acf656d58953b46d5afd8db2f4749cb6181d4821`  
		Last Modified: Tue, 07 Apr 2026 04:05:04 GMT  
		Size: 6.7 MB (6669911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e11abba1d2c7436d90ee2bc25b60a3238a2757de4a91846db7f9ae8b77abd1cc`  
		Last Modified: Tue, 07 Apr 2026 04:05:03 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38.2` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:3d7c496c2bcb9590de0849d0d3d70bbcf157d0c9cbef9ae9dfc1830a91a15621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163724198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:164847084d33466f2bf9d1f8f00e29cb7f32daec30e6f4e341271393a27bf425`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:20:23 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:20:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 03:20:27 GMT
ENV TELEGRAF_VERSION=1.38.2
# Tue, 07 Apr 2026 03:20:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 07 Apr 2026 03:20:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 07 Apr 2026 03:20:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 03:20:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 03:20:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af98f0879b367460715b477e9118922ba24f17d9a4ad8d70e595a9c4cf56990`  
		Last Modified: Tue, 07 Apr 2026 01:49:50 GMT  
		Size: 23.6 MB (23604705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053aa2f9ecb5253e7f30ffdda533ae9361ea13704b633656b1038c8af8b5ec87`  
		Last Modified: Tue, 07 Apr 2026 03:20:49 GMT  
		Size: 18.9 MB (18885921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49086742a58fe18731758318a8d8c92bcb86f8fe223c0b2381630a55ae284cdf`  
		Last Modified: Tue, 07 Apr 2026 03:20:48 GMT  
		Size: 5.1 KB (5073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d204d82c3153763626d0596b405467834c7a2c3308e4258b90de7de44948aa4`  
		Last Modified: Tue, 07 Apr 2026 03:20:50 GMT  
		Size: 72.9 MB (72854613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41550f6dbf91ed385e676570e8b5450dba4252bd1ebeb3dccc7277c9e5cbb3b5`  
		Last Modified: Tue, 07 Apr 2026 03:20:48 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38.2` - unknown; unknown

```console
$ docker pull telegraf@sha256:4b27d1b213c48659610976f3a14fa75495ef62b4c69da25a18623903a676d22b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6690845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7324c416edb25f1de66cb95c043b7229c62b2636257de46ce07b3315ed29ea3c`

```dockerfile
```

-	Layers:
	-	`sha256:393e1eed36170b31e4170499743574ce62ba19d3e131e28e4bbd1981ec192389`  
		Last Modified: Tue, 07 Apr 2026 03:20:49 GMT  
		Size: 6.7 MB (6675994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c154c7bf13b7ca0105a6cb1205162bc1ae5eb9d34a0622f97e0e624199fb1d6d`  
		Last Modified: Tue, 07 Apr 2026 03:20:48 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:1.38.2-alpine`

```console
$ docker pull telegraf@sha256:811335001118729cd2bdbcf0aaa88fae62102ab85745bf5f4a0ed60cba56de4e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:1.38.2-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:15c787ed509753ff1c98af9c858bc4e79a8838e2f97f9da94808690f237954a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87671535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d74b6eeb9d11ffd3cf0526e2dfd611c3f1a047bee5ab27f89f68f30cce3a66`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Mon, 30 Mar 2026 20:22:43 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 30 Mar 2026 20:22:44 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 30 Mar 2026 20:22:52 GMT
ENV TELEGRAF_VERSION=1.38.2
# Mon, 30 Mar 2026 20:22:52 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 30 Mar 2026 20:22:52 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 30 Mar 2026 20:22:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 30 Mar 2026 20:22:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 30 Mar 2026 20:22:52 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f3ac74f06ef64597e0008d5b58e2d631cbc2a1c7c8d7827de7f6084ffd1384`  
		Last Modified: Mon, 30 Mar 2026 20:23:07 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841b2cba4b94e9cabe8821efc5c269224dc910b9f66659d5a0118790408f9f64`  
		Last Modified: Mon, 30 Mar 2026 20:23:08 GMT  
		Size: 2.6 MB (2563409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22318848ab211de8fbcfbd33472f3c9a9f45e5bf40b3964fd587be331ef0cfff`  
		Last Modified: Mon, 30 Mar 2026 20:23:10 GMT  
		Size: 81.3 MB (81302351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f3b3d70a34cca73560581366bf1aa5a7a571294392984eb390146e1a80a300`  
		Last Modified: Mon, 30 Mar 2026 20:23:07 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38.2-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c45de09e7ba9157e9b403a2dd99453df7bee97206572dabc5092a953691be95a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1176730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03720b29716f6c0b29dbdaaee3000ef67a64556f9a2281d4cac081d6d996656`

```dockerfile
```

-	Layers:
	-	`sha256:98f0364ff7dd919bdcd1b7b1403d67ffa52a2b0edc4c62886b0e5011b3d3fc09`  
		Last Modified: Mon, 30 Mar 2026 20:23:07 GMT  
		Size: 1.2 MB (1161511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ee92bd2e1843be3aaa75cc44cd91b73eaba636edd0cc70546201ffdd09dd9d0`  
		Last Modified: Mon, 30 Mar 2026 20:23:07 GMT  
		Size: 15.2 KB (15219 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:1.38.2-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:fb0afd49cd58018b245cea4961f220c244fc777aa1ca0753135afd7c1f59a630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79408705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc70a72097954c4dd9b3106a74912f37b0a24e864006c9d69d2d1dcbbde7e87`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Mon, 30 Mar 2026 20:23:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 30 Mar 2026 20:23:01 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 30 Mar 2026 20:23:09 GMT
ENV TELEGRAF_VERSION=1.38.2
# Mon, 30 Mar 2026 20:23:09 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 30 Mar 2026 20:23:09 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 30 Mar 2026 20:23:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 30 Mar 2026 20:23:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 30 Mar 2026 20:23:09 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929ce7d3c4f4050324790939845bf90248d29e90794fd46af445c1b82fa8e3ea`  
		Last Modified: Mon, 30 Mar 2026 20:23:23 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2376aa1e3858066a43b2936816204d70c2b668fa25a029d43112bb6fde89fc0e`  
		Last Modified: Mon, 30 Mar 2026 20:23:23 GMT  
		Size: 2.6 MB (2627416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572e1b4bba075fe67f8adfc96feb476ce9866df13a73405592fb7efc167a67a3`  
		Last Modified: Mon, 30 Mar 2026 20:23:25 GMT  
		Size: 72.6 MB (72640871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b84aaa694985c4eda65e869bf5da5464e1a8a2d08ceb445751e354912483b0`  
		Last Modified: Mon, 30 Mar 2026 20:23:23 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:1.38.2-alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:936b6b08489b822579b383270e0805734d6dfceff3312eb28064c847078d400e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1172492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97cf381f8dcb2b3c9f182fa9c1b572003933f561a664db9074cf1c6ae7afb654`

```dockerfile
```

-	Layers:
	-	`sha256:4a8a6a2dc5feb376c8b91acda685d81ccc02f798d46c259afc3890bbe6e1601d`  
		Last Modified: Mon, 30 Mar 2026 20:23:23 GMT  
		Size: 1.2 MB (1157150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:020ec74ea2d5779e6a975977b3f564113afe329c270a94159417df24fb421131`  
		Last Modified: Mon, 30 Mar 2026 20:23:23 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:811335001118729cd2bdbcf0aaa88fae62102ab85745bf5f4a0ed60cba56de4e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:15c787ed509753ff1c98af9c858bc4e79a8838e2f97f9da94808690f237954a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87671535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d74b6eeb9d11ffd3cf0526e2dfd611c3f1a047bee5ab27f89f68f30cce3a66`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Mon, 30 Mar 2026 20:22:43 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 30 Mar 2026 20:22:44 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 30 Mar 2026 20:22:52 GMT
ENV TELEGRAF_VERSION=1.38.2
# Mon, 30 Mar 2026 20:22:52 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 30 Mar 2026 20:22:52 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 30 Mar 2026 20:22:52 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 30 Mar 2026 20:22:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 30 Mar 2026 20:22:52 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f3ac74f06ef64597e0008d5b58e2d631cbc2a1c7c8d7827de7f6084ffd1384`  
		Last Modified: Mon, 30 Mar 2026 20:23:07 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841b2cba4b94e9cabe8821efc5c269224dc910b9f66659d5a0118790408f9f64`  
		Last Modified: Mon, 30 Mar 2026 20:23:08 GMT  
		Size: 2.6 MB (2563409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22318848ab211de8fbcfbd33472f3c9a9f45e5bf40b3964fd587be331ef0cfff`  
		Last Modified: Mon, 30 Mar 2026 20:23:10 GMT  
		Size: 81.3 MB (81302351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f3b3d70a34cca73560581366bf1aa5a7a571294392984eb390146e1a80a300`  
		Last Modified: Mon, 30 Mar 2026 20:23:07 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:c45de09e7ba9157e9b403a2dd99453df7bee97206572dabc5092a953691be95a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1176730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03720b29716f6c0b29dbdaaee3000ef67a64556f9a2281d4cac081d6d996656`

```dockerfile
```

-	Layers:
	-	`sha256:98f0364ff7dd919bdcd1b7b1403d67ffa52a2b0edc4c62886b0e5011b3d3fc09`  
		Last Modified: Mon, 30 Mar 2026 20:23:07 GMT  
		Size: 1.2 MB (1161511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ee92bd2e1843be3aaa75cc44cd91b73eaba636edd0cc70546201ffdd09dd9d0`  
		Last Modified: Mon, 30 Mar 2026 20:23:07 GMT  
		Size: 15.2 KB (15219 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:fb0afd49cd58018b245cea4961f220c244fc777aa1ca0753135afd7c1f59a630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79408705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc70a72097954c4dd9b3106a74912f37b0a24e864006c9d69d2d1dcbbde7e87`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Mon, 30 Mar 2026 20:23:00 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 30 Mar 2026 20:23:01 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata setpriv libcap &&     update-ca-certificates # buildkit
# Mon, 30 Mar 2026 20:23:09 GMT
ENV TELEGRAF_VERSION=1.38.2
# Mon, 30 Mar 2026 20:23:09 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf # buildkit
# Mon, 30 Mar 2026 20:23:09 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Mon, 30 Mar 2026 20:23:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 30 Mar 2026 20:23:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 30 Mar 2026 20:23:09 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929ce7d3c4f4050324790939845bf90248d29e90794fd46af445c1b82fa8e3ea`  
		Last Modified: Mon, 30 Mar 2026 20:23:23 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2376aa1e3858066a43b2936816204d70c2b668fa25a029d43112bb6fde89fc0e`  
		Last Modified: Mon, 30 Mar 2026 20:23:23 GMT  
		Size: 2.6 MB (2627416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572e1b4bba075fe67f8adfc96feb476ce9866df13a73405592fb7efc167a67a3`  
		Last Modified: Mon, 30 Mar 2026 20:23:25 GMT  
		Size: 72.6 MB (72640871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b84aaa694985c4eda65e869bf5da5464e1a8a2d08ceb445751e354912483b0`  
		Last Modified: Mon, 30 Mar 2026 20:23:23 GMT  
		Size: 620.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:alpine` - unknown; unknown

```console
$ docker pull telegraf@sha256:936b6b08489b822579b383270e0805734d6dfceff3312eb28064c847078d400e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1172492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97cf381f8dcb2b3c9f182fa9c1b572003933f561a664db9074cf1c6ae7afb654`

```dockerfile
```

-	Layers:
	-	`sha256:4a8a6a2dc5feb376c8b91acda685d81ccc02f798d46c259afc3890bbe6e1601d`  
		Last Modified: Mon, 30 Mar 2026 20:23:23 GMT  
		Size: 1.2 MB (1157150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:020ec74ea2d5779e6a975977b3f564113afe329c270a94159417df24fb421131`  
		Last Modified: Mon, 30 Mar 2026 20:23:23 GMT  
		Size: 15.3 KB (15342 bytes)  
		MIME: application/vnd.in-toto+json

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:74fa2ce3d3e0eba543bf67d022c1c6bd7e7716f0cabb53641b5696a4bd915c6f
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
$ docker pull telegraf@sha256:17b8db94dc0db85b9e63b5854186dd6814604cc062315ec6cda62eebd95b197f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.0 MB (172992401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d909a4eb1b3349f8d033f3a16e144b2544a748098322efb34072be188aa825eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:46:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:08:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:08:58 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 03:09:38 GMT
ENV TELEGRAF_VERSION=1.38.2
# Tue, 07 Apr 2026 03:09:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 07 Apr 2026 03:09:38 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 07 Apr 2026 03:09:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 03:09:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 03:09:38 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c3414b1d6b49c54c305584faac46aad75c67644cf4f8495e8145206d28e416`  
		Last Modified: Tue, 07 Apr 2026 01:47:02 GMT  
		Size: 24.0 MB (24038269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33783d9cba990ea068fd7b11de7ac26da4e0e7e412f7802b50d66f837c8f77e6`  
		Last Modified: Tue, 07 Apr 2026 03:09:23 GMT  
		Size: 18.9 MB (18944499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2914360d962562f729d89e57142ce9620abe1fea7f9f9064b300d64ecfccbd35`  
		Last Modified: Tue, 07 Apr 2026 03:09:22 GMT  
		Size: 5.1 KB (5055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f21f12f1a5be3b7b94fc249297def9dc29522f795c5133f18b6a232fdbd1b9`  
		Last Modified: Tue, 07 Apr 2026 03:09:58 GMT  
		Size: 81.5 MB (81515133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063d9ba824d7baba0fc96f43b2b2f68552320f7aab90377d104b7aa5f4e15ab6`  
		Last Modified: Tue, 07 Apr 2026 03:09:55 GMT  
		Size: 622.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:901c98af60f94359ae6148a5b61b028c6eedcc2281739ab6896b1e229f7ce122
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6690035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f01e105f8304a9be0d4072b1cb915fa618282ceab9001c4b46dd5410627b10d`

```dockerfile
```

-	Layers:
	-	`sha256:cb15165e332ae744a86b2b698d6d36a9e1b59392effb48116d1c512840516a1a`  
		Last Modified: Tue, 07 Apr 2026 03:09:56 GMT  
		Size: 6.7 MB (6675306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:517668c9c7cb30a0989eb10ec5e2e58abaea85698ac205cf4ccf3dab2b091cd9`  
		Last Modified: Tue, 07 Apr 2026 03:09:55 GMT  
		Size: 14.7 KB (14729 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:73eb27b50ecd1d595f8e376dcabed624247fb6409d6ce68605b6f3dd0ba3ff2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159178851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fbcfba407b4d2a60bf7018485a3544151914ed4f06aeafb80f9f66ffca88c12`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:00:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:04:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 04:04:36 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 04:04:43 GMT
ENV TELEGRAF_VERSION=1.38.2
# Tue, 07 Apr 2026 04:04:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 07 Apr 2026 04:04:43 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 07 Apr 2026 04:04:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 04:04:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 04:04:43 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:a99a9abe3964725d9016ffc8402d9cffc28e94f404db8e764ca9583f2090145e`  
		Last Modified: Tue, 07 Apr 2026 00:58:42 GMT  
		Size: 44.2 MB (44207817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2a6632e49a08fc68f1ee0ec0fb4b6f38a03db30dc5ff33b611dc705110ee36`  
		Last Modified: Tue, 07 Apr 2026 02:00:47 GMT  
		Size: 21.9 MB (21942083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7064aee1b881fe04020815950097ba6772db2636b02e8935f9c796a09e796a79`  
		Last Modified: Tue, 07 Apr 2026 04:05:04 GMT  
		Size: 17.7 MB (17699660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9900d1dbddf68ca748bccdf8d31399c4ca7dc7ea5b3c55162425bb6e089b125`  
		Last Modified: Tue, 07 Apr 2026 04:05:03 GMT  
		Size: 5.1 KB (5069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393b0bb5ab0f51cddec2eddf26669b13eb02c3b9983b6462412ebe82b5b32aff`  
		Last Modified: Tue, 07 Apr 2026 04:05:06 GMT  
		Size: 75.3 MB (75323599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac2c2d5867bde037f0b47e61bd6ffd30115b0990bb4380e909484972b1b750c`  
		Last Modified: Tue, 07 Apr 2026 04:05:03 GMT  
		Size: 623.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:8c4c66654609a89100eef26c438f4577c0c3174e56fb7de10c3ac8bca88b74d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6684738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676e28d9f450becb09d5169b4ea63eb95d8d35fa476521fc9e84344bcf1f8546`

```dockerfile
```

-	Layers:
	-	`sha256:9957d7ca43a202adae172de2acf656d58953b46d5afd8db2f4749cb6181d4821`  
		Last Modified: Tue, 07 Apr 2026 04:05:04 GMT  
		Size: 6.7 MB (6669911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e11abba1d2c7436d90ee2bc25b60a3238a2757de4a91846db7f9ae8b77abd1cc`  
		Last Modified: Tue, 07 Apr 2026 04:05:03 GMT  
		Size: 14.8 KB (14827 bytes)  
		MIME: application/vnd.in-toto+json

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:3d7c496c2bcb9590de0849d0d3d70bbcf157d0c9cbef9ae9dfc1830a91a15621
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163724198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:164847084d33466f2bf9d1f8f00e29cb7f32daec30e6f4e341271393a27bf425`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:49:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:20:23 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 03:20:24 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 03:20:27 GMT
ENV TELEGRAF_VERSION=1.38.2
# Tue, 07 Apr 2026 03:20:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 07 Apr 2026 03:20:27 GMT
EXPOSE map[8092/udp:{} 8094/tcp:{} 8125/udp:{}]
# Tue, 07 Apr 2026 03:20:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 03:20:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 03:20:27 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af98f0879b367460715b477e9118922ba24f17d9a4ad8d70e595a9c4cf56990`  
		Last Modified: Tue, 07 Apr 2026 01:49:50 GMT  
		Size: 23.6 MB (23604705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053aa2f9ecb5253e7f30ffdda533ae9361ea13704b633656b1038c8af8b5ec87`  
		Last Modified: Tue, 07 Apr 2026 03:20:49 GMT  
		Size: 18.9 MB (18885921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49086742a58fe18731758318a8d8c92bcb86f8fe223c0b2381630a55ae284cdf`  
		Last Modified: Tue, 07 Apr 2026 03:20:48 GMT  
		Size: 5.1 KB (5073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d204d82c3153763626d0596b405467834c7a2c3308e4258b90de7de44948aa4`  
		Last Modified: Tue, 07 Apr 2026 03:20:50 GMT  
		Size: 72.9 MB (72854613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41550f6dbf91ed385e676570e8b5450dba4252bd1ebeb3dccc7277c9e5cbb3b5`  
		Last Modified: Tue, 07 Apr 2026 03:20:48 GMT  
		Size: 624.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `telegraf:latest` - unknown; unknown

```console
$ docker pull telegraf@sha256:4b27d1b213c48659610976f3a14fa75495ef62b4c69da25a18623903a676d22b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6690845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7324c416edb25f1de66cb95c043b7229c62b2636257de46ce07b3315ed29ea3c`

```dockerfile
```

-	Layers:
	-	`sha256:393e1eed36170b31e4170499743574ce62ba19d3e131e28e4bbd1981ec192389`  
		Last Modified: Tue, 07 Apr 2026 03:20:49 GMT  
		Size: 6.7 MB (6675994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c154c7bf13b7ca0105a6cb1205162bc1ae5eb9d34a0622f97e0e624199fb1d6d`  
		Last Modified: Tue, 07 Apr 2026 03:20:48 GMT  
		Size: 14.9 KB (14851 bytes)  
		MIME: application/vnd.in-toto+json
