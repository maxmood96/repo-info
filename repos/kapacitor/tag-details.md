<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.7`](#kapacitor17)
-	[`kapacitor:1.7-alpine`](#kapacitor17-alpine)
-	[`kapacitor:1.7.7`](#kapacitor177)
-	[`kapacitor:1.7.7-alpine`](#kapacitor177-alpine)
-	[`kapacitor:1.8`](#kapacitor18)
-	[`kapacitor:1.8-alpine`](#kapacitor18-alpine)
-	[`kapacitor:1.8.5`](#kapacitor185)
-	[`kapacitor:1.8.5-alpine`](#kapacitor185-alpine)
-	[`kapacitor:alpine`](#kapacitoralpine)
-	[`kapacitor:latest`](#kapacitorlatest)

## `kapacitor:1.7`

```console
$ docker pull kapacitor@sha256:312ba26cc9a706fd53e5730d652bf313c7e8cf45516cd76abb8d80817223569e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:9bd284ce40688f5db6621b92eb6a11906143d3025fea6a0cde2fca5fe26a8a24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160810444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71e96ab55580a5b9e8f836dc80c9b28ee1cc630316284df33903408e8cadaeb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:10:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:46:16 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Fri, 15 May 2026 21:46:20 GMT
ENV KAPACITOR_VERSION=1.7.7
# Fri, 15 May 2026 21:46:20 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 15 May 2026 21:46:20 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 15 May 2026 21:46:20 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 15 May 2026 21:46:20 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 15 May 2026 21:46:20 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:46:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 May 2026 21:46:20 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0aeb1f8fc5f0c234e2220faa9320cdfd32528ee5a33d4b932677603206a1e8`  
		Last Modified: Fri, 15 May 2026 21:11:00 GMT  
		Size: 7.1 MB (7106733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759447bddbece7991ca4f8c19065fbd1e1714d0c1186a1f639d8ea881de51de2`  
		Last Modified: Fri, 15 May 2026 21:46:36 GMT  
		Size: 51.9 MB (51915370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b1ec915e63eeb9e06d62bed18ec9825c172cddf9096ad01b3e0348daa3906b`  
		Last Modified: Fri, 15 May 2026 21:46:36 GMT  
		Size: 72.1 MB (72051135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821aa197ff82a1a5c5c899e63acd4afbf07ef91758179d52eabf88923cebd09b`  
		Last Modified: Fri, 15 May 2026 21:46:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00591eeda4037577ea91ed4eaaeea05c0eb7dbe95d46fc3162a8e4766281be0`  
		Last Modified: Fri, 15 May 2026 21:46:33 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:f5f8045a379ca0a079c5a13fd0bf62bec2f591e8fe301baa54e9ffc2ea0d052d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69bc04f75fbc02d727d0574dc9e8187e11c018e012a8a4f9a957dcabadaf535`

```dockerfile
```

-	Layers:
	-	`sha256:3c3e144d44012403976ac6eccafcfb60fcaac1a0a5d5af9e7a1a471a13e00bd9`  
		Last Modified: Fri, 15 May 2026 21:46:33 GMT  
		Size: 3.7 MB (3716680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8293303aab10413791330a5957360c5d3051cb2bc0a3e58dce5db3a8397b36bf`  
		Last Modified: Fri, 15 May 2026 21:46:33 GMT  
		Size: 14.7 KB (14716 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:5416c486947f9968c3321c3f64f31fe15e2673ef0236e943a9389991920df6e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153475251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52601b69f600077c3937b84ff317a0edbb83ac7229a5985ced68f8e7584c6556`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:10:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:47:26 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Fri, 15 May 2026 21:47:29 GMT
ENV KAPACITOR_VERSION=1.7.7
# Fri, 15 May 2026 21:47:29 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 15 May 2026 21:47:29 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 15 May 2026 21:47:29 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 15 May 2026 21:47:29 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 15 May 2026 21:47:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:47:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 May 2026 21:47:29 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c3443b99bfd9ba84dc508ac1e64f30df03b505f391957f7bb18008ddaa77c1`  
		Last Modified: Fri, 15 May 2026 21:11:07 GMT  
		Size: 7.1 MB (7061756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b275e5893e8509aa7a1e4693477c515710e0ff7e6206533d2949ec9e59646ba6`  
		Last Modified: Fri, 15 May 2026 21:47:45 GMT  
		Size: 51.0 MB (50992628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e3c11e943178740102531666e52b701108cdde527b89786f7b823885263c75`  
		Last Modified: Fri, 15 May 2026 21:47:45 GMT  
		Size: 67.8 MB (67813723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9008f6ae090bb1d2393e20a96485208041507bf6187025cad7b03385a544e14a`  
		Last Modified: Fri, 15 May 2026 21:47:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea9eac2e987f716e7e99e84c7492d00a16507c4b3c6e175d62034974ea4266d`  
		Last Modified: Fri, 15 May 2026 21:47:42 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:522495cde65cceec575cbb46fcf4ad4879970fd3678632161071bbf6a9f881cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d66a521a24c101cd1b0976f5182dbf9b9304079d43b4a5a00829be596621da`

```dockerfile
```

-	Layers:
	-	`sha256:74e5987b52d0840f7298254f03fe223c5038d5d04039c0cc9958bdda67c2275b`  
		Last Modified: Fri, 15 May 2026 21:47:42 GMT  
		Size: 3.7 MB (3716142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9bc269889537845a4f7fea176f36ec6cb833505bd2bdd42c83517058d8ef0bd`  
		Last Modified: Fri, 15 May 2026 21:47:42 GMT  
		Size: 14.8 KB (14811 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7-alpine`

```console
$ docker pull kapacitor@sha256:d413cc02810588e8c459ea5be842408894d80457fd6bf3d17c76054bd4fbeba6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.7-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:7dd27bf99a95c88a227895984474aed5a5acd9e005ee8c4ca5d230c5adce430d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75904570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3afb14c37dc00503a0e3d186c16cca67e6e6cf79f380e0768c83b473ab21723`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:28 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:29:59 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:30:05 GMT
ENV KAPACITOR_VERSION=1.7.7
# Fri, 17 Apr 2026 00:30:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Fri, 17 Apr 2026 00:30:05 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 17 Apr 2026 00:30:05 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 17 Apr 2026 00:30:05 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 17 Apr 2026 00:30:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:30:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:30:05 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16e69077797f1a90c5b8946765d6547bd0bbe62c5edf87016fc687d8691b62a`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d26afc56a247d157e5130fafb0c3e1596d90cb798a74bcd18085a2e60f5e83`  
		Last Modified: Fri, 17 Apr 2026 00:30:17 GMT  
		Size: 290.8 KB (290778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62dd12f58262d16aa469c538fe54969fbd41faab46b0c454ce33250afdb5cf9`  
		Last Modified: Fri, 17 Apr 2026 00:30:19 GMT  
		Size: 72.0 MB (71982697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55baa52346461779ddbbe16b9bcbe892cdd293e258d25759833687ed332ec26f`  
		Last Modified: Fri, 17 Apr 2026 00:30:17 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b697b2c16e0d0a74ce9cec7f52e70573e6c357c63cea20d805fa64c4bd2a984c`  
		Last Modified: Fri, 17 Apr 2026 00:30:17 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:c43b268a38b55473ac82d1c64d91b2abf473cfd8498dadaf61b7b610b7a0a384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.5 KB (381476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8c6c8a59270545d801e93fbec290d5e3507d4c0ef7d1b17af7ac1a44b9f91e2`

```dockerfile
```

-	Layers:
	-	`sha256:5e93c3927eafe526f00d32bfce704d302d02d4cbe2d4104d9f70f6c2132c0cee`  
		Last Modified: Fri, 17 Apr 2026 00:30:17 GMT  
		Size: 365.8 KB (365835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d021a80b9241fd4aceb41e3907131caf439210759adcdaa248d89c1e12091d7`  
		Last Modified: Fri, 17 Apr 2026 00:30:17 GMT  
		Size: 15.6 KB (15641 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7.7`

```console
$ docker pull kapacitor@sha256:312ba26cc9a706fd53e5730d652bf313c7e8cf45516cd76abb8d80817223569e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:9bd284ce40688f5db6621b92eb6a11906143d3025fea6a0cde2fca5fe26a8a24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160810444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71e96ab55580a5b9e8f836dc80c9b28ee1cc630316284df33903408e8cadaeb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:10:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:46:16 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Fri, 15 May 2026 21:46:20 GMT
ENV KAPACITOR_VERSION=1.7.7
# Fri, 15 May 2026 21:46:20 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 15 May 2026 21:46:20 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 15 May 2026 21:46:20 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 15 May 2026 21:46:20 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 15 May 2026 21:46:20 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:46:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 May 2026 21:46:20 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0aeb1f8fc5f0c234e2220faa9320cdfd32528ee5a33d4b932677603206a1e8`  
		Last Modified: Fri, 15 May 2026 21:11:00 GMT  
		Size: 7.1 MB (7106733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759447bddbece7991ca4f8c19065fbd1e1714d0c1186a1f639d8ea881de51de2`  
		Last Modified: Fri, 15 May 2026 21:46:36 GMT  
		Size: 51.9 MB (51915370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b1ec915e63eeb9e06d62bed18ec9825c172cddf9096ad01b3e0348daa3906b`  
		Last Modified: Fri, 15 May 2026 21:46:36 GMT  
		Size: 72.1 MB (72051135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821aa197ff82a1a5c5c899e63acd4afbf07ef91758179d52eabf88923cebd09b`  
		Last Modified: Fri, 15 May 2026 21:46:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00591eeda4037577ea91ed4eaaeea05c0eb7dbe95d46fc3162a8e4766281be0`  
		Last Modified: Fri, 15 May 2026 21:46:33 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:f5f8045a379ca0a079c5a13fd0bf62bec2f591e8fe301baa54e9ffc2ea0d052d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69bc04f75fbc02d727d0574dc9e8187e11c018e012a8a4f9a957dcabadaf535`

```dockerfile
```

-	Layers:
	-	`sha256:3c3e144d44012403976ac6eccafcfb60fcaac1a0a5d5af9e7a1a471a13e00bd9`  
		Last Modified: Fri, 15 May 2026 21:46:33 GMT  
		Size: 3.7 MB (3716680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8293303aab10413791330a5957360c5d3051cb2bc0a3e58dce5db3a8397b36bf`  
		Last Modified: Fri, 15 May 2026 21:46:33 GMT  
		Size: 14.7 KB (14716 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:5416c486947f9968c3321c3f64f31fe15e2673ef0236e943a9389991920df6e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153475251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52601b69f600077c3937b84ff317a0edbb83ac7229a5985ced68f8e7584c6556`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:10:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:47:26 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Fri, 15 May 2026 21:47:29 GMT
ENV KAPACITOR_VERSION=1.7.7
# Fri, 15 May 2026 21:47:29 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 15 May 2026 21:47:29 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 15 May 2026 21:47:29 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 15 May 2026 21:47:29 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 15 May 2026 21:47:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:47:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 May 2026 21:47:29 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c3443b99bfd9ba84dc508ac1e64f30df03b505f391957f7bb18008ddaa77c1`  
		Last Modified: Fri, 15 May 2026 21:11:07 GMT  
		Size: 7.1 MB (7061756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b275e5893e8509aa7a1e4693477c515710e0ff7e6206533d2949ec9e59646ba6`  
		Last Modified: Fri, 15 May 2026 21:47:45 GMT  
		Size: 51.0 MB (50992628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e3c11e943178740102531666e52b701108cdde527b89786f7b823885263c75`  
		Last Modified: Fri, 15 May 2026 21:47:45 GMT  
		Size: 67.8 MB (67813723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9008f6ae090bb1d2393e20a96485208041507bf6187025cad7b03385a544e14a`  
		Last Modified: Fri, 15 May 2026 21:47:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea9eac2e987f716e7e99e84c7492d00a16507c4b3c6e175d62034974ea4266d`  
		Last Modified: Fri, 15 May 2026 21:47:42 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:522495cde65cceec575cbb46fcf4ad4879970fd3678632161071bbf6a9f881cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d66a521a24c101cd1b0976f5182dbf9b9304079d43b4a5a00829be596621da`

```dockerfile
```

-	Layers:
	-	`sha256:74e5987b52d0840f7298254f03fe223c5038d5d04039c0cc9958bdda67c2275b`  
		Last Modified: Fri, 15 May 2026 21:47:42 GMT  
		Size: 3.7 MB (3716142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9bc269889537845a4f7fea176f36ec6cb833505bd2bdd42c83517058d8ef0bd`  
		Last Modified: Fri, 15 May 2026 21:47:42 GMT  
		Size: 14.8 KB (14811 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7.7-alpine`

```console
$ docker pull kapacitor@sha256:d413cc02810588e8c459ea5be842408894d80457fd6bf3d17c76054bd4fbeba6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.7.7-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:7dd27bf99a95c88a227895984474aed5a5acd9e005ee8c4ca5d230c5adce430d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75904570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3afb14c37dc00503a0e3d186c16cca67e6e6cf79f380e0768c83b473ab21723`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:28 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:29:59 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:30:05 GMT
ENV KAPACITOR_VERSION=1.7.7
# Fri, 17 Apr 2026 00:30:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Fri, 17 Apr 2026 00:30:05 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 17 Apr 2026 00:30:05 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 17 Apr 2026 00:30:05 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 17 Apr 2026 00:30:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:30:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:30:05 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16e69077797f1a90c5b8946765d6547bd0bbe62c5edf87016fc687d8691b62a`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d26afc56a247d157e5130fafb0c3e1596d90cb798a74bcd18085a2e60f5e83`  
		Last Modified: Fri, 17 Apr 2026 00:30:17 GMT  
		Size: 290.8 KB (290778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62dd12f58262d16aa469c538fe54969fbd41faab46b0c454ce33250afdb5cf9`  
		Last Modified: Fri, 17 Apr 2026 00:30:19 GMT  
		Size: 72.0 MB (71982697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55baa52346461779ddbbe16b9bcbe892cdd293e258d25759833687ed332ec26f`  
		Last Modified: Fri, 17 Apr 2026 00:30:17 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b697b2c16e0d0a74ce9cec7f52e70573e6c357c63cea20d805fa64c4bd2a984c`  
		Last Modified: Fri, 17 Apr 2026 00:30:17 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.7-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:c43b268a38b55473ac82d1c64d91b2abf473cfd8498dadaf61b7b610b7a0a384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.5 KB (381476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8c6c8a59270545d801e93fbec290d5e3507d4c0ef7d1b17af7ac1a44b9f91e2`

```dockerfile
```

-	Layers:
	-	`sha256:5e93c3927eafe526f00d32bfce704d302d02d4cbe2d4104d9f70f6c2132c0cee`  
		Last Modified: Fri, 17 Apr 2026 00:30:17 GMT  
		Size: 365.8 KB (365835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d021a80b9241fd4aceb41e3907131caf439210759adcdaa248d89c1e12091d7`  
		Last Modified: Fri, 17 Apr 2026 00:30:17 GMT  
		Size: 15.6 KB (15641 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8`

```console
$ docker pull kapacitor@sha256:f61630a45ec685fea67125dcfff2a1c0adb48f4e507783912f435f9c39e94505
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.8` - linux; amd64

```console
$ docker pull kapacitor@sha256:21ab0cafa733815b533de71700e6144ac4b1a7667088d50cf322f303b3f25565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174503064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbf68ce343bed6b6feec26179d886e7e0ea241656472c2478f8db8ee64daca0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:10:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:46:18 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Fri, 15 May 2026 21:46:23 GMT
ENV KAPACITOR_VERSION=1.8.5
# Fri, 15 May 2026 21:46:23 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 15 May 2026 21:46:23 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 15 May 2026 21:46:23 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 15 May 2026 21:46:23 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 15 May 2026 21:46:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:46:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 May 2026 21:46:23 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0aeb1f8fc5f0c234e2220faa9320cdfd32528ee5a33d4b932677603206a1e8`  
		Last Modified: Fri, 15 May 2026 21:11:00 GMT  
		Size: 7.1 MB (7106733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46159866ad82a5c777187ff50c453289ebed543b8f9f68248be6d79202aa9f4d`  
		Last Modified: Fri, 15 May 2026 21:46:41 GMT  
		Size: 51.9 MB (51915346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f3cf074a7121762bbb3538695a60b3625b8df65a296c33336433c170ffdf1d`  
		Last Modified: Fri, 15 May 2026 21:46:42 GMT  
		Size: 85.7 MB (85743781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fedcc49bf04169eda6042ca14d5a99c7bc1db25cebc554ba4a3f4f0e8170b8e`  
		Last Modified: Fri, 15 May 2026 21:46:39 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f5a0a593fce94b8ea0fe8759d01793ee19a4ca10a238ef57851d0d51821412`  
		Last Modified: Fri, 15 May 2026 21:46:39 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8` - unknown; unknown

```console
$ docker pull kapacitor@sha256:6ceb89dc0a0a4dbd4128e60d5e9f79361d95bc3b19b32f60de5526dd70ebee7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3747048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7a6f1288f18d09acc218ea06c754f5fa45c4241417833bcbfbfb753ae8cc3b`

```dockerfile
```

-	Layers:
	-	`sha256:06a3fdb6cbe0f3a9d43f449222c4a3dc5e6f789dde3ba366fe9b1518ef414ddb`  
		Last Modified: Fri, 15 May 2026 21:46:39 GMT  
		Size: 3.7 MB (3732028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e5e61e6aaaa0faa0a4a1424e949c788bb835290992273fe49911d193a945dfe`  
		Last Modified: Fri, 15 May 2026 21:46:39 GMT  
		Size: 15.0 KB (15020 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.8` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:276a60d51dd87d293c5337310870b0dc42d499a35f9c23ea69f4c970a9c04e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.8 MB (165824584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435a681c29f0f50a5607588df1153c012a29c0d5e92b52ce759ffbdc9d1af154`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:10:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:47:24 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Fri, 15 May 2026 21:47:29 GMT
ENV KAPACITOR_VERSION=1.8.5
# Fri, 15 May 2026 21:47:29 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 15 May 2026 21:47:29 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 15 May 2026 21:47:29 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 15 May 2026 21:47:29 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 15 May 2026 21:47:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:47:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 May 2026 21:47:29 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c3443b99bfd9ba84dc508ac1e64f30df03b505f391957f7bb18008ddaa77c1`  
		Last Modified: Fri, 15 May 2026 21:11:07 GMT  
		Size: 7.1 MB (7061756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca325b534f8e5bf28c4acc9719dbc6ebf82c802117c93c633569c5bc7c73dc14`  
		Last Modified: Fri, 15 May 2026 21:47:49 GMT  
		Size: 51.0 MB (50992580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ae8658efa64ea5aa54a5dc2789327c0ef6a3b926e75c4d838856b23139b000`  
		Last Modified: Fri, 15 May 2026 21:47:49 GMT  
		Size: 80.2 MB (80163104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3d874ec011cb8cf46d4b10a5f672a7a09fb3bd7a5f56da0821837c8e0d79d3`  
		Last Modified: Fri, 15 May 2026 21:47:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea9eac2e987f716e7e99e84c7492d00a16507c4b3c6e175d62034974ea4266d`  
		Last Modified: Fri, 15 May 2026 21:47:42 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8` - unknown; unknown

```console
$ docker pull kapacitor@sha256:6021f0c0b5eaf82a9a51acf8cdbe31f693a9ad4313675794cb57305d8bd36296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6a004b36323e9dc276d74ca38239db3033b03f2a2e1aa249a8a7e521af7170`

```dockerfile
```

-	Layers:
	-	`sha256:a43558c11e4caf94a2a8e22556c366dd33713e9ce886b76d3eeb7bcedb64c2e0`  
		Last Modified: Fri, 15 May 2026 21:47:47 GMT  
		Size: 3.7 MB (3731502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e4d7e727e2fb7205e7d775288c96a70868edd027d1b9892bf49cb13401c0c8a`  
		Last Modified: Fri, 15 May 2026 21:47:46 GMT  
		Size: 15.1 KB (15127 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8-alpine`

```console
$ docker pull kapacitor@sha256:1b75a0c5384c9119b8bb3a639c4814f12e19463de38d9bb15ef687aafb47d04b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.8-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:3509230863377e606f65fbd6809441dd62d204bddcfff04271b9161a3ba1af84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89771455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5251c9f1ab9b747463275a95a7dabac0cd63c98621b8bd73514395659a769340`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:00:24 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jun 2026 20:00:56 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Mon, 22 Jun 2026 20:01:02 GMT
ENV KAPACITOR_VERSION=1.8.5
# Mon, 22 Jun 2026 20:01:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Mon, 22 Jun 2026 20:01:02 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 22 Jun 2026 20:01:02 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 22 Jun 2026 20:01:02 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 22 Jun 2026 20:01:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jun 2026 20:01:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 20:01:02 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2de596e6e58599b275563cd7971ad9ea4ebcee65d366f85d02114624fbf249`  
		Last Modified: Mon, 22 Jun 2026 20:00:39 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785b16a71c5eb5f314877e3da7831546e9823f148c3999f2786921a93f577763`  
		Last Modified: Mon, 22 Jun 2026 20:01:18 GMT  
		Size: 268.7 KB (268744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1523b495d7cf6997d542eafaa1221ad3872d783762474eb434dbc9790ef8cd1c`  
		Last Modified: Mon, 22 Jun 2026 20:01:19 GMT  
		Size: 85.7 MB (85657489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778108c2cf4ac343a0f57711f8198f004221b3ea3a9bf4da6a1dea293e72f39b`  
		Last Modified: Mon, 22 Jun 2026 20:01:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f57a8773eb946420bc883d5195990b81b30564ae3e1ff6722f4d8282af2deb9`  
		Last Modified: Mon, 22 Jun 2026 20:01:17 GMT  
		Size: 295.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:dbce504b9838621b932ebda9e22428814f1eeeaac16316b1f264367585650494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.2 KB (388158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97da902bbd0aed582adc787ad350ce85c8d3984482e2332a80177cf0ca368d5`

```dockerfile
```

-	Layers:
	-	`sha256:8e7bfa57590764500221a9df884e4a1d2e3a20441cd9a4e8809ed89784196fa2`  
		Last Modified: Mon, 22 Jun 2026 20:01:16 GMT  
		Size: 372.8 KB (372821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebaeed4adde14f5dd75418ddbb6926cdef500524a230a7ddb46feef537dd5df9`  
		Last Modified: Mon, 22 Jun 2026 20:01:17 GMT  
		Size: 15.3 KB (15337 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8.5`

```console
$ docker pull kapacitor@sha256:f61630a45ec685fea67125dcfff2a1c0adb48f4e507783912f435f9c39e94505
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.8.5` - linux; amd64

```console
$ docker pull kapacitor@sha256:21ab0cafa733815b533de71700e6144ac4b1a7667088d50cf322f303b3f25565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174503064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbf68ce343bed6b6feec26179d886e7e0ea241656472c2478f8db8ee64daca0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:10:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:46:18 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Fri, 15 May 2026 21:46:23 GMT
ENV KAPACITOR_VERSION=1.8.5
# Fri, 15 May 2026 21:46:23 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 15 May 2026 21:46:23 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 15 May 2026 21:46:23 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 15 May 2026 21:46:23 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 15 May 2026 21:46:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:46:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 May 2026 21:46:23 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0aeb1f8fc5f0c234e2220faa9320cdfd32528ee5a33d4b932677603206a1e8`  
		Last Modified: Fri, 15 May 2026 21:11:00 GMT  
		Size: 7.1 MB (7106733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46159866ad82a5c777187ff50c453289ebed543b8f9f68248be6d79202aa9f4d`  
		Last Modified: Fri, 15 May 2026 21:46:41 GMT  
		Size: 51.9 MB (51915346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f3cf074a7121762bbb3538695a60b3625b8df65a296c33336433c170ffdf1d`  
		Last Modified: Fri, 15 May 2026 21:46:42 GMT  
		Size: 85.7 MB (85743781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fedcc49bf04169eda6042ca14d5a99c7bc1db25cebc554ba4a3f4f0e8170b8e`  
		Last Modified: Fri, 15 May 2026 21:46:39 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f5a0a593fce94b8ea0fe8759d01793ee19a4ca10a238ef57851d0d51821412`  
		Last Modified: Fri, 15 May 2026 21:46:39 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8.5` - unknown; unknown

```console
$ docker pull kapacitor@sha256:6ceb89dc0a0a4dbd4128e60d5e9f79361d95bc3b19b32f60de5526dd70ebee7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3747048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7a6f1288f18d09acc218ea06c754f5fa45c4241417833bcbfbfb753ae8cc3b`

```dockerfile
```

-	Layers:
	-	`sha256:06a3fdb6cbe0f3a9d43f449222c4a3dc5e6f789dde3ba366fe9b1518ef414ddb`  
		Last Modified: Fri, 15 May 2026 21:46:39 GMT  
		Size: 3.7 MB (3732028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e5e61e6aaaa0faa0a4a1424e949c788bb835290992273fe49911d193a945dfe`  
		Last Modified: Fri, 15 May 2026 21:46:39 GMT  
		Size: 15.0 KB (15020 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.8.5` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:276a60d51dd87d293c5337310870b0dc42d499a35f9c23ea69f4c970a9c04e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.8 MB (165824584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435a681c29f0f50a5607588df1153c012a29c0d5e92b52ce759ffbdc9d1af154`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:10:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:47:24 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Fri, 15 May 2026 21:47:29 GMT
ENV KAPACITOR_VERSION=1.8.5
# Fri, 15 May 2026 21:47:29 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 15 May 2026 21:47:29 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 15 May 2026 21:47:29 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 15 May 2026 21:47:29 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 15 May 2026 21:47:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:47:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 May 2026 21:47:29 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c3443b99bfd9ba84dc508ac1e64f30df03b505f391957f7bb18008ddaa77c1`  
		Last Modified: Fri, 15 May 2026 21:11:07 GMT  
		Size: 7.1 MB (7061756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca325b534f8e5bf28c4acc9719dbc6ebf82c802117c93c633569c5bc7c73dc14`  
		Last Modified: Fri, 15 May 2026 21:47:49 GMT  
		Size: 51.0 MB (50992580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ae8658efa64ea5aa54a5dc2789327c0ef6a3b926e75c4d838856b23139b000`  
		Last Modified: Fri, 15 May 2026 21:47:49 GMT  
		Size: 80.2 MB (80163104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3d874ec011cb8cf46d4b10a5f672a7a09fb3bd7a5f56da0821837c8e0d79d3`  
		Last Modified: Fri, 15 May 2026 21:47:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea9eac2e987f716e7e99e84c7492d00a16507c4b3c6e175d62034974ea4266d`  
		Last Modified: Fri, 15 May 2026 21:47:42 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8.5` - unknown; unknown

```console
$ docker pull kapacitor@sha256:6021f0c0b5eaf82a9a51acf8cdbe31f693a9ad4313675794cb57305d8bd36296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6a004b36323e9dc276d74ca38239db3033b03f2a2e1aa249a8a7e521af7170`

```dockerfile
```

-	Layers:
	-	`sha256:a43558c11e4caf94a2a8e22556c366dd33713e9ce886b76d3eeb7bcedb64c2e0`  
		Last Modified: Fri, 15 May 2026 21:47:47 GMT  
		Size: 3.7 MB (3731502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e4d7e727e2fb7205e7d775288c96a70868edd027d1b9892bf49cb13401c0c8a`  
		Last Modified: Fri, 15 May 2026 21:47:46 GMT  
		Size: 15.1 KB (15127 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8.5-alpine`

```console
$ docker pull kapacitor@sha256:1b75a0c5384c9119b8bb3a639c4814f12e19463de38d9bb15ef687aafb47d04b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.8.5-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:3509230863377e606f65fbd6809441dd62d204bddcfff04271b9161a3ba1af84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89771455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5251c9f1ab9b747463275a95a7dabac0cd63c98621b8bd73514395659a769340`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:00:24 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 22 Jun 2026 20:00:56 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Mon, 22 Jun 2026 20:01:02 GMT
ENV KAPACITOR_VERSION=1.8.5
# Mon, 22 Jun 2026 20:01:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Mon, 22 Jun 2026 20:01:02 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 22 Jun 2026 20:01:02 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 22 Jun 2026 20:01:02 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 22 Jun 2026 20:01:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 22 Jun 2026 20:01:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jun 2026 20:01:02 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2de596e6e58599b275563cd7971ad9ea4ebcee65d366f85d02114624fbf249`  
		Last Modified: Mon, 22 Jun 2026 20:00:39 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785b16a71c5eb5f314877e3da7831546e9823f148c3999f2786921a93f577763`  
		Last Modified: Mon, 22 Jun 2026 20:01:18 GMT  
		Size: 268.7 KB (268744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1523b495d7cf6997d542eafaa1221ad3872d783762474eb434dbc9790ef8cd1c`  
		Last Modified: Mon, 22 Jun 2026 20:01:19 GMT  
		Size: 85.7 MB (85657489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778108c2cf4ac343a0f57711f8198f004221b3ea3a9bf4da6a1dea293e72f39b`  
		Last Modified: Mon, 22 Jun 2026 20:01:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f57a8773eb946420bc883d5195990b81b30564ae3e1ff6722f4d8282af2deb9`  
		Last Modified: Mon, 22 Jun 2026 20:01:17 GMT  
		Size: 295.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8.5-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:dbce504b9838621b932ebda9e22428814f1eeeaac16316b1f264367585650494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.2 KB (388158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97da902bbd0aed582adc787ad350ce85c8d3984482e2332a80177cf0ca368d5`

```dockerfile
```

-	Layers:
	-	`sha256:8e7bfa57590764500221a9df884e4a1d2e3a20441cd9a4e8809ed89784196fa2`  
		Last Modified: Mon, 22 Jun 2026 20:01:16 GMT  
		Size: 372.8 KB (372821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebaeed4adde14f5dd75418ddbb6926cdef500524a230a7ddb46feef537dd5df9`  
		Last Modified: Mon, 22 Jun 2026 20:01:17 GMT  
		Size: 15.3 KB (15337 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:d413cc02810588e8c459ea5be842408894d80457fd6bf3d17c76054bd4fbeba6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:7dd27bf99a95c88a227895984474aed5a5acd9e005ee8c4ca5d230c5adce430d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75904570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3afb14c37dc00503a0e3d186c16cca67e6e6cf79f380e0768c83b473ab21723`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:28 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Fri, 17 Apr 2026 00:29:59 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Fri, 17 Apr 2026 00:30:05 GMT
ENV KAPACITOR_VERSION=1.7.7
# Fri, 17 Apr 2026 00:30:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Fri, 17 Apr 2026 00:30:05 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 17 Apr 2026 00:30:05 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 17 Apr 2026 00:30:05 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 17 Apr 2026 00:30:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 00:30:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 17 Apr 2026 00:30:05 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16e69077797f1a90c5b8946765d6547bd0bbe62c5edf87016fc687d8691b62a`  
		Last Modified: Fri, 17 Apr 2026 00:23:39 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d26afc56a247d157e5130fafb0c3e1596d90cb798a74bcd18085a2e60f5e83`  
		Last Modified: Fri, 17 Apr 2026 00:30:17 GMT  
		Size: 290.8 KB (290778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62dd12f58262d16aa469c538fe54969fbd41faab46b0c454ce33250afdb5cf9`  
		Last Modified: Fri, 17 Apr 2026 00:30:19 GMT  
		Size: 72.0 MB (71982697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55baa52346461779ddbbe16b9bcbe892cdd293e258d25759833687ed332ec26f`  
		Last Modified: Fri, 17 Apr 2026 00:30:17 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b697b2c16e0d0a74ce9cec7f52e70573e6c357c63cea20d805fa64c4bd2a984c`  
		Last Modified: Fri, 17 Apr 2026 00:30:17 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:c43b268a38b55473ac82d1c64d91b2abf473cfd8498dadaf61b7b610b7a0a384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.5 KB (381476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8c6c8a59270545d801e93fbec290d5e3507d4c0ef7d1b17af7ac1a44b9f91e2`

```dockerfile
```

-	Layers:
	-	`sha256:5e93c3927eafe526f00d32bfce704d302d02d4cbe2d4104d9f70f6c2132c0cee`  
		Last Modified: Fri, 17 Apr 2026 00:30:17 GMT  
		Size: 365.8 KB (365835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d021a80b9241fd4aceb41e3907131caf439210759adcdaa248d89c1e12091d7`  
		Last Modified: Fri, 17 Apr 2026 00:30:17 GMT  
		Size: 15.6 KB (15641 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:f61630a45ec685fea67125dcfff2a1c0adb48f4e507783912f435f9c39e94505
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:21ab0cafa733815b533de71700e6144ac4b1a7667088d50cf322f303b3f25565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174503064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbf68ce343bed6b6feec26179d886e7e0ea241656472c2478f8db8ee64daca0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:10:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:46:18 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Fri, 15 May 2026 21:46:23 GMT
ENV KAPACITOR_VERSION=1.8.5
# Fri, 15 May 2026 21:46:23 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 15 May 2026 21:46:23 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 15 May 2026 21:46:23 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 15 May 2026 21:46:23 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 15 May 2026 21:46:23 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:46:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 May 2026 21:46:23 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0aeb1f8fc5f0c234e2220faa9320cdfd32528ee5a33d4b932677603206a1e8`  
		Last Modified: Fri, 15 May 2026 21:11:00 GMT  
		Size: 7.1 MB (7106733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46159866ad82a5c777187ff50c453289ebed543b8f9f68248be6d79202aa9f4d`  
		Last Modified: Fri, 15 May 2026 21:46:41 GMT  
		Size: 51.9 MB (51915346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f3cf074a7121762bbb3538695a60b3625b8df65a296c33336433c170ffdf1d`  
		Last Modified: Fri, 15 May 2026 21:46:42 GMT  
		Size: 85.7 MB (85743781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fedcc49bf04169eda6042ca14d5a99c7bc1db25cebc554ba4a3f4f0e8170b8e`  
		Last Modified: Fri, 15 May 2026 21:46:39 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f5a0a593fce94b8ea0fe8759d01793ee19a4ca10a238ef57851d0d51821412`  
		Last Modified: Fri, 15 May 2026 21:46:39 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:6ceb89dc0a0a4dbd4128e60d5e9f79361d95bc3b19b32f60de5526dd70ebee7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3747048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7a6f1288f18d09acc218ea06c754f5fa45c4241417833bcbfbfb753ae8cc3b`

```dockerfile
```

-	Layers:
	-	`sha256:06a3fdb6cbe0f3a9d43f449222c4a3dc5e6f789dde3ba366fe9b1518ef414ddb`  
		Last Modified: Fri, 15 May 2026 21:46:39 GMT  
		Size: 3.7 MB (3732028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e5e61e6aaaa0faa0a4a1424e949c788bb835290992273fe49911d193a945dfe`  
		Last Modified: Fri, 15 May 2026 21:46:39 GMT  
		Size: 15.0 KB (15020 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:276a60d51dd87d293c5337310870b0dc42d499a35f9c23ea69f4c970a9c04e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.8 MB (165824584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435a681c29f0f50a5607588df1153c012a29c0d5e92b52ce759ffbdc9d1af154`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:10:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:47:24 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Fri, 15 May 2026 21:47:29 GMT
ENV KAPACITOR_VERSION=1.8.5
# Fri, 15 May 2026 21:47:29 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Fri, 15 May 2026 21:47:29 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Fri, 15 May 2026 21:47:29 GMT
EXPOSE map[9092/tcp:{}]
# Fri, 15 May 2026 21:47:29 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 15 May 2026 21:47:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:47:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 15 May 2026 21:47:29 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c3443b99bfd9ba84dc508ac1e64f30df03b505f391957f7bb18008ddaa77c1`  
		Last Modified: Fri, 15 May 2026 21:11:07 GMT  
		Size: 7.1 MB (7061756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca325b534f8e5bf28c4acc9719dbc6ebf82c802117c93c633569c5bc7c73dc14`  
		Last Modified: Fri, 15 May 2026 21:47:49 GMT  
		Size: 51.0 MB (50992580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ae8658efa64ea5aa54a5dc2789327c0ef6a3b926e75c4d838856b23139b000`  
		Last Modified: Fri, 15 May 2026 21:47:49 GMT  
		Size: 80.2 MB (80163104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3d874ec011cb8cf46d4b10a5f672a7a09fb3bd7a5f56da0821837c8e0d79d3`  
		Last Modified: Fri, 15 May 2026 21:47:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea9eac2e987f716e7e99e84c7492d00a16507c4b3c6e175d62034974ea4266d`  
		Last Modified: Fri, 15 May 2026 21:47:42 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:6021f0c0b5eaf82a9a51acf8cdbe31f693a9ad4313675794cb57305d8bd36296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6a004b36323e9dc276d74ca38239db3033b03f2a2e1aa249a8a7e521af7170`

```dockerfile
```

-	Layers:
	-	`sha256:a43558c11e4caf94a2a8e22556c366dd33713e9ce886b76d3eeb7bcedb64c2e0`  
		Last Modified: Fri, 15 May 2026 21:47:47 GMT  
		Size: 3.7 MB (3731502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e4d7e727e2fb7205e7d775288c96a70868edd027d1b9892bf49cb13401c0c8a`  
		Last Modified: Fri, 15 May 2026 21:47:46 GMT  
		Size: 15.1 KB (15127 bytes)  
		MIME: application/vnd.in-toto+json
