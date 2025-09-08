<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.7`](#kapacitor17)
-	[`kapacitor:1.7-alpine`](#kapacitor17-alpine)
-	[`kapacitor:1.7.7`](#kapacitor177)
-	[`kapacitor:1.7.7-alpine`](#kapacitor177-alpine)
-	[`kapacitor:1.8`](#kapacitor18)
-	[`kapacitor:1.8-alpine`](#kapacitor18-alpine)
-	[`kapacitor:1.8.1`](#kapacitor181)
-	[`kapacitor:1.8.1-alpine`](#kapacitor181-alpine)
-	[`kapacitor:alpine`](#kapacitoralpine)
-	[`kapacitor:latest`](#kapacitorlatest)

## `kapacitor:1.7`

```console
$ docker pull kapacitor@sha256:cf9cce1202f24d3e064129474e0421b391b3908345aed1f3262bcc419032afc9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:006d773860729c5f1e90d2cc4d62a8bde4cc7b4f7779f0f702735225a2a0a1d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (155045495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0128781a404598c2cf11f89ee516d9afb2edb834e133ffa33872a92f806353eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENV KAPACITOR_VERSION=1.7.7
# Tue, 08 Jul 2025 13:10:35 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 08 Jul 2025 13:10:35 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 08 Jul 2025 13:10:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Jul 2025 13:10:35 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6828c7dda7e5e4b9c82ddb483379bdc791aa9b7cecdce2c883c603e7806ea9a`  
		Last Modified: Mon, 01 Sep 2025 23:07:56 GMT  
		Size: 7.1 MB (7106278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32881a48c74b51c802296316fe2b2f03e47e9347b5f6417087bc09432cb53ddc`  
		Last Modified: Tue, 02 Sep 2025 01:30:56 GMT  
		Size: 46.4 MB (46350677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0188a806504ccda9df36d501bea1c4ebb8baf37174d52c0ecf39b9af8870a11`  
		Last Modified: Tue, 02 Sep 2025 01:31:12 GMT  
		Size: 72.1 MB (72051083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b487b31f7a1bdd30b4c89fc00295d69941e96e30c9da4a3a0ff01682dac426`  
		Last Modified: Tue, 02 Sep 2025 00:45:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78921c43e8c484fb34e0a56825570562c0dcb4c19971add75b89798e2d5eec8`  
		Last Modified: Tue, 02 Sep 2025 00:45:46 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:54756b3bf1fe1295f721192b00ab0716b78c2d9d13f36f469b30c6286e094396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b53bd391e0414373b94148a12bb7be6c75c47e2b48e5cde317ffd33548494f`

```dockerfile
```

-	Layers:
	-	`sha256:48f5957df489af1bb5a3efa7174f22032e7ad67946da50b30f6c574b63c42a5c`  
		Last Modified: Tue, 02 Sep 2025 04:21:18 GMT  
		Size: 3.7 MB (3716676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cad42473886de67fd0e589a291cb61c90d44a0634c2aed291bd27bfee5fbb77`  
		Last Modified: Tue, 02 Sep 2025 04:21:19 GMT  
		Size: 14.8 KB (14759 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:921dccc90592f4642528b8d9890d697131376ee76e6413958ed0ae657dc806b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146211907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45864afc67fa813b07870edcdaad96ea6549bb1a56a48afc2b4e45cca745070`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENV KAPACITOR_VERSION=1.7.7
# Tue, 08 Jul 2025 13:10:35 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 08 Jul 2025 13:10:35 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 08 Jul 2025 13:10:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Jul 2025 13:10:35 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573b56f55094f2d14930c686b1a46091f6f5d62cadec0da94af57c5297b32867`  
		Last Modified: Tue, 02 Sep 2025 01:18:59 GMT  
		Size: 7.1 MB (7051940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9638ee345f265593b563464cf568a673d0e98db70e231aef56afc0c86d6f286`  
		Last Modified: Tue, 02 Sep 2025 04:52:49 GMT  
		Size: 44.0 MB (43984242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6291543bbe0b72b0e5d9f237d35f7f024c833bdb4405f30dc0ab575c35cb76`  
		Last Modified: Tue, 02 Sep 2025 04:52:51 GMT  
		Size: 67.8 MB (67813732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5773250687d003ee80156d0e620e407d969f002daca34cfa8add5ccf06f0b5fb`  
		Last Modified: Tue, 02 Sep 2025 04:52:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201328e05e493519cd6c7517b376ae6159b0e7388c12b50e9c3411523ff1423d`  
		Last Modified: Tue, 02 Sep 2025 04:52:45 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:a605016a8754080f766675eeb49dbd5d81e7380dc7b3693e61c17fd887e2cc3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19cfa6079c006afd2bd1c619c16cb6ad5804b6d525fa8470c317fa671dae44a5`

```dockerfile
```

-	Layers:
	-	`sha256:1bd02e3f57a714de2a2f4b8688974b669e021d19c5ff7cb05dff913501670ed1`  
		Last Modified: Tue, 02 Sep 2025 07:21:19 GMT  
		Size: 3.7 MB (3716138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a94161ccfe107181438281ddc335f287b3b08d1243074ba6388442554640983`  
		Last Modified: Tue, 02 Sep 2025 07:21:20 GMT  
		Size: 14.9 KB (14853 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7-alpine`

```console
$ docker pull kapacitor@sha256:4a740c633b90375fc4613465ead786b393b1106ff2a748d895d51967f5c8eb55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.7-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:495481bc51bb09cd677a387761815568fac2fdf0165b74652e05308d252fc673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75887885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e6e758f84077ab7831577cf3aa0a3c1ee4fae198f9eee13120886d468b4d5e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 08 Jul 2025 13:10:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
CMD ["/bin/sh"]
# Tue, 08 Jul 2025 13:10:35 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENV KAPACITOR_VERSION=1.7.7
# Tue, 08 Jul 2025 13:10:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 08 Jul 2025 13:10:35 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 08 Jul 2025 13:10:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Jul 2025 13:10:35 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7cd59a170b5fff4759056f3021cd3a0f8b8b93fd86f3b540f889da699918c6`  
		Last Modified: Tue, 15 Jul 2025 20:46:46 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a6ffa563fb7d136af9cbd8379cf5ceacbf2926fadcd8e281c43b0cd52cb334`  
		Last Modified: Wed, 16 Jul 2025 06:05:34 GMT  
		Size: 283.8 KB (283794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd34a060f527e5af8a18b24cf3308e10ffd9c472cc20593e106f406d6efe7f1`  
		Last Modified: Wed, 16 Jul 2025 08:14:17 GMT  
		Size: 72.0 MB (71982834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b96d9ad903da395c8acc30237a367d0349015a659efa7b235443f051909f89`  
		Last Modified: Wed, 16 Jul 2025 05:59:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cba525bdf0c3a03182ebbbf50f501d2ad26bdbb63fb2e4bd01963a644155449`  
		Last Modified: Wed, 16 Jul 2025 05:59:25 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:2f1b54a2048c3a3b338544b0c408b33dd54dbc449f63a8dbde7990f697a68a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.6 KB (379593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf0662c60fc4bc189a7c968c0a97009e090f806295b18433651f515500f4bd1`

```dockerfile
```

-	Layers:
	-	`sha256:7129167326340ece8825cd0b82133d5059b3bceaaa807a7903b1c31ce09f5e9d`  
		Last Modified: Tue, 15 Jul 2025 22:21:18 GMT  
		Size: 363.9 KB (363909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e7c0e7967c42b262e03d986132f124a458856a89945a10b72681d79a9d610c`  
		Last Modified: Tue, 15 Jul 2025 22:21:19 GMT  
		Size: 15.7 KB (15684 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7.7`

```console
$ docker pull kapacitor@sha256:cf9cce1202f24d3e064129474e0421b391b3908345aed1f3262bcc419032afc9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:006d773860729c5f1e90d2cc4d62a8bde4cc7b4f7779f0f702735225a2a0a1d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (155045495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0128781a404598c2cf11f89ee516d9afb2edb834e133ffa33872a92f806353eb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENV KAPACITOR_VERSION=1.7.7
# Tue, 08 Jul 2025 13:10:35 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 08 Jul 2025 13:10:35 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 08 Jul 2025 13:10:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Jul 2025 13:10:35 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6828c7dda7e5e4b9c82ddb483379bdc791aa9b7cecdce2c883c603e7806ea9a`  
		Last Modified: Mon, 01 Sep 2025 23:07:56 GMT  
		Size: 7.1 MB (7106278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32881a48c74b51c802296316fe2b2f03e47e9347b5f6417087bc09432cb53ddc`  
		Last Modified: Tue, 02 Sep 2025 01:30:56 GMT  
		Size: 46.4 MB (46350677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0188a806504ccda9df36d501bea1c4ebb8baf37174d52c0ecf39b9af8870a11`  
		Last Modified: Tue, 02 Sep 2025 01:31:12 GMT  
		Size: 72.1 MB (72051083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b487b31f7a1bdd30b4c89fc00295d69941e96e30c9da4a3a0ff01682dac426`  
		Last Modified: Tue, 02 Sep 2025 00:45:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78921c43e8c484fb34e0a56825570562c0dcb4c19971add75b89798e2d5eec8`  
		Last Modified: Tue, 02 Sep 2025 00:45:46 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:54756b3bf1fe1295f721192b00ab0716b78c2d9d13f36f469b30c6286e094396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b53bd391e0414373b94148a12bb7be6c75c47e2b48e5cde317ffd33548494f`

```dockerfile
```

-	Layers:
	-	`sha256:48f5957df489af1bb5a3efa7174f22032e7ad67946da50b30f6c574b63c42a5c`  
		Last Modified: Tue, 02 Sep 2025 04:21:18 GMT  
		Size: 3.7 MB (3716676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cad42473886de67fd0e589a291cb61c90d44a0634c2aed291bd27bfee5fbb77`  
		Last Modified: Tue, 02 Sep 2025 04:21:19 GMT  
		Size: 14.8 KB (14759 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:921dccc90592f4642528b8d9890d697131376ee76e6413958ed0ae657dc806b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146211907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45864afc67fa813b07870edcdaad96ea6549bb1a56a48afc2b4e45cca745070`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENV KAPACITOR_VERSION=1.7.7
# Tue, 08 Jul 2025 13:10:35 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 08 Jul 2025 13:10:35 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 08 Jul 2025 13:10:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Jul 2025 13:10:35 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573b56f55094f2d14930c686b1a46091f6f5d62cadec0da94af57c5297b32867`  
		Last Modified: Tue, 02 Sep 2025 01:18:59 GMT  
		Size: 7.1 MB (7051940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9638ee345f265593b563464cf568a673d0e98db70e231aef56afc0c86d6f286`  
		Last Modified: Tue, 02 Sep 2025 04:52:49 GMT  
		Size: 44.0 MB (43984242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6291543bbe0b72b0e5d9f237d35f7f024c833bdb4405f30dc0ab575c35cb76`  
		Last Modified: Tue, 02 Sep 2025 04:52:51 GMT  
		Size: 67.8 MB (67813732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5773250687d003ee80156d0e620e407d969f002daca34cfa8add5ccf06f0b5fb`  
		Last Modified: Tue, 02 Sep 2025 04:52:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:201328e05e493519cd6c7517b376ae6159b0e7388c12b50e9c3411523ff1423d`  
		Last Modified: Tue, 02 Sep 2025 04:52:45 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:a605016a8754080f766675eeb49dbd5d81e7380dc7b3693e61c17fd887e2cc3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19cfa6079c006afd2bd1c619c16cb6ad5804b6d525fa8470c317fa671dae44a5`

```dockerfile
```

-	Layers:
	-	`sha256:1bd02e3f57a714de2a2f4b8688974b669e021d19c5ff7cb05dff913501670ed1`  
		Last Modified: Tue, 02 Sep 2025 07:21:19 GMT  
		Size: 3.7 MB (3716138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a94161ccfe107181438281ddc335f287b3b08d1243074ba6388442554640983`  
		Last Modified: Tue, 02 Sep 2025 07:21:20 GMT  
		Size: 14.9 KB (14853 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7.7-alpine`

```console
$ docker pull kapacitor@sha256:4a740c633b90375fc4613465ead786b393b1106ff2a748d895d51967f5c8eb55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.7.7-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:495481bc51bb09cd677a387761815568fac2fdf0165b74652e05308d252fc673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75887885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e6e758f84077ab7831577cf3aa0a3c1ee4fae198f9eee13120886d468b4d5e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 08 Jul 2025 13:10:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
CMD ["/bin/sh"]
# Tue, 08 Jul 2025 13:10:35 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENV KAPACITOR_VERSION=1.7.7
# Tue, 08 Jul 2025 13:10:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 08 Jul 2025 13:10:35 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 08 Jul 2025 13:10:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Jul 2025 13:10:35 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7cd59a170b5fff4759056f3021cd3a0f8b8b93fd86f3b540f889da699918c6`  
		Last Modified: Tue, 15 Jul 2025 20:46:46 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a6ffa563fb7d136af9cbd8379cf5ceacbf2926fadcd8e281c43b0cd52cb334`  
		Last Modified: Wed, 16 Jul 2025 06:05:34 GMT  
		Size: 283.8 KB (283794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd34a060f527e5af8a18b24cf3308e10ffd9c472cc20593e106f406d6efe7f1`  
		Last Modified: Wed, 16 Jul 2025 08:14:17 GMT  
		Size: 72.0 MB (71982834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b96d9ad903da395c8acc30237a367d0349015a659efa7b235443f051909f89`  
		Last Modified: Wed, 16 Jul 2025 05:59:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cba525bdf0c3a03182ebbbf50f501d2ad26bdbb63fb2e4bd01963a644155449`  
		Last Modified: Wed, 16 Jul 2025 05:59:25 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.7-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:2f1b54a2048c3a3b338544b0c408b33dd54dbc449f63a8dbde7990f697a68a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.6 KB (379593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf0662c60fc4bc189a7c968c0a97009e090f806295b18433651f515500f4bd1`

```dockerfile
```

-	Layers:
	-	`sha256:7129167326340ece8825cd0b82133d5059b3bceaaa807a7903b1c31ce09f5e9d`  
		Last Modified: Tue, 15 Jul 2025 22:21:18 GMT  
		Size: 363.9 KB (363909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e7c0e7967c42b262e03d986132f124a458856a89945a10b72681d79a9d610c`  
		Last Modified: Tue, 15 Jul 2025 22:21:19 GMT  
		Size: 15.7 KB (15684 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8`

```console
$ docker pull kapacitor@sha256:b8be732edc41153315b8dfb8c7c94f0ed38e3c441ed543331d1082b51f1b833f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.8` - linux; amd64

```console
$ docker pull kapacitor@sha256:9ad857f4671b2d6d36e940288f210d5a7b2c843ebf508a04f43c8fed273b6998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 MB (170360625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd67a078c6977d69b5cdbc7bfda9412a92d14f2c723ff61f586bdfb1cce0230`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENV KAPACITOR_VERSION=1.8.0
# Tue, 08 Jul 2025 13:10:35 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 08 Jul 2025 13:10:35 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 08 Jul 2025 13:10:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Jul 2025 13:10:35 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6828c7dda7e5e4b9c82ddb483379bdc791aa9b7cecdce2c883c603e7806ea9a`  
		Last Modified: Mon, 01 Sep 2025 23:07:56 GMT  
		Size: 7.1 MB (7106278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a3c2ea12fee40c9ef8e85effe39cf721a4c6498f95eddb0afb1e159616f661`  
		Last Modified: Tue, 02 Sep 2025 01:31:52 GMT  
		Size: 46.4 MB (46350670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620772e1697007c3420c88a3c03a710d225d20cfe3345d95d64018af0f17d304`  
		Last Modified: Tue, 02 Sep 2025 01:31:48 GMT  
		Size: 87.4 MB (87366216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee471b271ed6e3f6518684a183a8b2596cfd31e5426550246a85a8f6fb486e7`  
		Last Modified: Tue, 02 Sep 2025 01:31:43 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f140d92705977a4026aa6b9f96ad6f9e1623828b601ba429eb63c6e959e64d`  
		Last Modified: Tue, 02 Sep 2025 01:31:44 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8` - unknown; unknown

```console
$ docker pull kapacitor@sha256:7ccd2c6261d3a87a73c0935fdc18f46e589e888431fba9a846f4297fc335dd06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab9662f4672fe23139601b90ed778b2640c3aeb2f733b1a2198c85d8ad86c4e`

```dockerfile
```

-	Layers:
	-	`sha256:7fd29301d5f5aa8936394dd368bf34872373c439005766bdcfb207884cbed357`  
		Last Modified: Tue, 02 Sep 2025 04:21:24 GMT  
		Size: 3.7 MB (3731269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c74236d3c40e35cd008c0eccb49ca4cb3f1be3b4d3f6cb1ac7629ce8dcfe12b9`  
		Last Modified: Tue, 02 Sep 2025 04:21:25 GMT  
		Size: 15.1 KB (15062 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.8` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:34100f6f7977f8d021357b1a2ca36c97211c65825875426ab734dcc921ee64bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159861919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee2588efd929c3449bbaf353507e5bf4badc827ade6b0d888dfd248b15b858c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENV KAPACITOR_VERSION=1.8.0
# Tue, 08 Jul 2025 13:10:35 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 08 Jul 2025 13:10:35 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 08 Jul 2025 13:10:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Jul 2025 13:10:35 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573b56f55094f2d14930c686b1a46091f6f5d62cadec0da94af57c5297b32867`  
		Last Modified: Tue, 02 Sep 2025 01:18:59 GMT  
		Size: 7.1 MB (7051940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9638ee345f265593b563464cf568a673d0e98db70e231aef56afc0c86d6f286`  
		Last Modified: Tue, 02 Sep 2025 04:52:49 GMT  
		Size: 44.0 MB (43984242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f402fe2a98fccc20b255c74fc100f94277b4d06d76463132c72f7dafe4354c`  
		Last Modified: Tue, 02 Sep 2025 04:53:16 GMT  
		Size: 81.5 MB (81463748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39af266d7e47648a14fdb6b8830ffa7be8c484cc139c85f859afe809596f8a46`  
		Last Modified: Tue, 02 Sep 2025 04:53:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fde9ad70a06bb672ecbda12db9678a6169991c4b47437bcad91e8534b1da785`  
		Last Modified: Tue, 02 Sep 2025 04:53:11 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8` - unknown; unknown

```console
$ docker pull kapacitor@sha256:cfd4dedb60a41e390dfc9b85f77931871b8c969d9b9f2c66a2e4cd9b4710abe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52a169f7adcf5777253e75e49451f8f22ed2296184905887b4c37b3bbf0b9e8`

```dockerfile
```

-	Layers:
	-	`sha256:118e2379b18bbc6b19ac0580208229b47d3983d8e258bab1ab4daba884071bc1`  
		Last Modified: Tue, 02 Sep 2025 07:21:27 GMT  
		Size: 3.7 MB (3730743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5c7c8d6d7b816b935b3174bb953a63e4d5a9b1a5d8acc1a2861a6a198083d06`  
		Last Modified: Tue, 02 Sep 2025 07:21:27 GMT  
		Size: 15.2 KB (15170 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8-alpine`

```console
$ docker pull kapacitor@sha256:2825d7196fb304f3a04865fc4dec75870843bc4764300d6fde593d329478e7b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.8-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:4743478781d2a7c047ad95226eba4024a3de6d4d64c0bd967ec116be3343e643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91400915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4fa050f17c04c7e0f84978129ab42af6e09dd33d65b3b32f2277fb18a8c835`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 08 Jul 2025 13:10:35 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
CMD ["/bin/sh"]
# Tue, 08 Jul 2025 13:10:35 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENV KAPACITOR_VERSION=1.8.0
# Tue, 08 Jul 2025 13:10:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 08 Jul 2025 13:10:35 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 08 Jul 2025 13:10:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Jul 2025 13:10:35 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38e79fd324639f0fb04fac74b91a3fdd03f987bf17d22bf2e2f9e8fad895cd1`  
		Last Modified: Tue, 15 Jul 2025 19:27:45 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235c4218322a4624970ccfa65b12c9ddad2435ac444b450a39dc418785c8bc68`  
		Last Modified: Tue, 15 Jul 2025 19:27:45 GMT  
		Size: 305.9 KB (305883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50cd64a5b29e44b24472bd128a39c6b4cc1cc22d52e52e98d7ea1ce6468da965`  
		Last Modified: Tue, 15 Jul 2025 19:27:56 GMT  
		Size: 87.3 MB (87294543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc02c4b7af262620386fceaf1713b9e5849367fdcf1f5991f1e09c9426cceaf8`  
		Last Modified: Tue, 15 Jul 2025 19:27:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2132b1ef163276aa1d02da1827290d21bf76105bd972ebec937d0055ccf86c2`  
		Last Modified: Tue, 15 Jul 2025 19:27:46 GMT  
		Size: 295.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:958bb89f875d5bd08234cdab7e8380cda7dc4eea714aa5dd2163fd3464a49c22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.7 KB (403682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb6e26545a47362444044a81a947549427a112135537a3a393226508b9d00f8`

```dockerfile
```

-	Layers:
	-	`sha256:da8d3e8bf8525002c6b07e29f473dad97c32ab76bc541156db43124ee078d3bf`  
		Last Modified: Tue, 15 Jul 2025 22:21:23 GMT  
		Size: 388.3 KB (388303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b12fea95b71b3d4b8fc770dfe58e742da102df6dba1beb0c4f901e5b944b97a3`  
		Last Modified: Tue, 15 Jul 2025 22:21:24 GMT  
		Size: 15.4 KB (15379 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8.1`

```console
$ docker pull kapacitor@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `kapacitor:1.8.1-alpine`

```console
$ docker pull kapacitor@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:4a740c633b90375fc4613465ead786b393b1106ff2a748d895d51967f5c8eb55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:495481bc51bb09cd677a387761815568fac2fdf0165b74652e05308d252fc673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75887885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e6e758f84077ab7831577cf3aa0a3c1ee4fae198f9eee13120886d468b4d5e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 08 Jul 2025 13:10:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
CMD ["/bin/sh"]
# Tue, 08 Jul 2025 13:10:35 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENV KAPACITOR_VERSION=1.7.7
# Tue, 08 Jul 2025 13:10:35 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 08 Jul 2025 13:10:35 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 08 Jul 2025 13:10:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Jul 2025 13:10:35 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7cd59a170b5fff4759056f3021cd3a0f8b8b93fd86f3b540f889da699918c6`  
		Last Modified: Tue, 15 Jul 2025 20:46:46 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a6ffa563fb7d136af9cbd8379cf5ceacbf2926fadcd8e281c43b0cd52cb334`  
		Last Modified: Wed, 16 Jul 2025 06:05:34 GMT  
		Size: 283.8 KB (283794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd34a060f527e5af8a18b24cf3308e10ffd9c472cc20593e106f406d6efe7f1`  
		Last Modified: Wed, 16 Jul 2025 08:14:17 GMT  
		Size: 72.0 MB (71982834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b96d9ad903da395c8acc30237a367d0349015a659efa7b235443f051909f89`  
		Last Modified: Wed, 16 Jul 2025 05:59:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cba525bdf0c3a03182ebbbf50f501d2ad26bdbb63fb2e4bd01963a644155449`  
		Last Modified: Wed, 16 Jul 2025 05:59:25 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:2f1b54a2048c3a3b338544b0c408b33dd54dbc449f63a8dbde7990f697a68a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.6 KB (379593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf0662c60fc4bc189a7c968c0a97009e090f806295b18433651f515500f4bd1`

```dockerfile
```

-	Layers:
	-	`sha256:7129167326340ece8825cd0b82133d5059b3bceaaa807a7903b1c31ce09f5e9d`  
		Last Modified: Tue, 15 Jul 2025 22:21:18 GMT  
		Size: 363.9 KB (363909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e7c0e7967c42b262e03d986132f124a458856a89945a10b72681d79a9d610c`  
		Last Modified: Tue, 15 Jul 2025 22:21:19 GMT  
		Size: 15.7 KB (15684 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:b8be732edc41153315b8dfb8c7c94f0ed38e3c441ed543331d1082b51f1b833f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:9ad857f4671b2d6d36e940288f210d5a7b2c843ebf508a04f43c8fed273b6998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.4 MB (170360625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd67a078c6977d69b5cdbc7bfda9412a92d14f2c723ff61f586bdfb1cce0230`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENV KAPACITOR_VERSION=1.8.0
# Tue, 08 Jul 2025 13:10:35 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 08 Jul 2025 13:10:35 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 08 Jul 2025 13:10:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Jul 2025 13:10:35 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6828c7dda7e5e4b9c82ddb483379bdc791aa9b7cecdce2c883c603e7806ea9a`  
		Last Modified: Mon, 01 Sep 2025 23:07:56 GMT  
		Size: 7.1 MB (7106278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a3c2ea12fee40c9ef8e85effe39cf721a4c6498f95eddb0afb1e159616f661`  
		Last Modified: Tue, 02 Sep 2025 01:31:52 GMT  
		Size: 46.4 MB (46350670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620772e1697007c3420c88a3c03a710d225d20cfe3345d95d64018af0f17d304`  
		Last Modified: Tue, 02 Sep 2025 01:31:48 GMT  
		Size: 87.4 MB (87366216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee471b271ed6e3f6518684a183a8b2596cfd31e5426550246a85a8f6fb486e7`  
		Last Modified: Tue, 02 Sep 2025 01:31:43 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f140d92705977a4026aa6b9f96ad6f9e1623828b601ba429eb63c6e959e64d`  
		Last Modified: Tue, 02 Sep 2025 01:31:44 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:7ccd2c6261d3a87a73c0935fdc18f46e589e888431fba9a846f4297fc335dd06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab9662f4672fe23139601b90ed778b2640c3aeb2f733b1a2198c85d8ad86c4e`

```dockerfile
```

-	Layers:
	-	`sha256:7fd29301d5f5aa8936394dd368bf34872373c439005766bdcfb207884cbed357`  
		Last Modified: Tue, 02 Sep 2025 04:21:24 GMT  
		Size: 3.7 MB (3731269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c74236d3c40e35cd008c0eccb49ca4cb3f1be3b4d3f6cb1ac7629ce8dcfe12b9`  
		Last Modified: Tue, 02 Sep 2025 04:21:25 GMT  
		Size: 15.1 KB (15062 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:34100f6f7977f8d021357b1a2ca36c97211c65825875426ab734dcc921ee64bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159861919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee2588efd929c3449bbaf353507e5bf4badc827ade6b0d888dfd248b15b858c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENV KAPACITOR_VERSION=1.8.0
# Tue, 08 Jul 2025 13:10:35 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 08 Jul 2025 13:10:35 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 08 Jul 2025 13:10:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 08 Jul 2025 13:10:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Jul 2025 13:10:35 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573b56f55094f2d14930c686b1a46091f6f5d62cadec0da94af57c5297b32867`  
		Last Modified: Tue, 02 Sep 2025 01:18:59 GMT  
		Size: 7.1 MB (7051940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9638ee345f265593b563464cf568a673d0e98db70e231aef56afc0c86d6f286`  
		Last Modified: Tue, 02 Sep 2025 04:52:49 GMT  
		Size: 44.0 MB (43984242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f402fe2a98fccc20b255c74fc100f94277b4d06d76463132c72f7dafe4354c`  
		Last Modified: Tue, 02 Sep 2025 04:53:16 GMT  
		Size: 81.5 MB (81463748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39af266d7e47648a14fdb6b8830ffa7be8c484cc139c85f859afe809596f8a46`  
		Last Modified: Tue, 02 Sep 2025 04:53:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fde9ad70a06bb672ecbda12db9678a6169991c4b47437bcad91e8534b1da785`  
		Last Modified: Tue, 02 Sep 2025 04:53:11 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:cfd4dedb60a41e390dfc9b85f77931871b8c969d9b9f2c66a2e4cd9b4710abe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52a169f7adcf5777253e75e49451f8f22ed2296184905887b4c37b3bbf0b9e8`

```dockerfile
```

-	Layers:
	-	`sha256:118e2379b18bbc6b19ac0580208229b47d3983d8e258bab1ab4daba884071bc1`  
		Last Modified: Tue, 02 Sep 2025 07:21:27 GMT  
		Size: 3.7 MB (3730743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5c7c8d6d7b816b935b3174bb953a63e4d5a9b1a5d8acc1a2861a6a198083d06`  
		Last Modified: Tue, 02 Sep 2025 07:21:27 GMT  
		Size: 15.2 KB (15170 bytes)  
		MIME: application/vnd.in-toto+json
