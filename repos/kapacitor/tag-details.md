<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.6`](#kapacitor16)
-	[`kapacitor:1.6-alpine`](#kapacitor16-alpine)
-	[`kapacitor:1.6.6`](#kapacitor166)
-	[`kapacitor:1.6.6-alpine`](#kapacitor166-alpine)
-	[`kapacitor:1.7`](#kapacitor17)
-	[`kapacitor:1.7-alpine`](#kapacitor17-alpine)
-	[`kapacitor:1.7.1`](#kapacitor171)
-	[`kapacitor:1.7.1-alpine`](#kapacitor171-alpine)
-	[`kapacitor:alpine`](#kapacitoralpine)
-	[`kapacitor:latest`](#kapacitorlatest)

## `kapacitor:1.6`

```console
$ docker pull kapacitor@sha256:3bc6ebdfc932fe5d96e13a4029094ab32d7c2e68c98b782941839d30a5b1d2b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:1.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:15c485e89e6aa04ccbb41973386fee60eca6951e73b20a22561192ccfec61868
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137106837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ed354479cdd4cf011b8e9907c5a439edb866273720ef2ccdc8184c61fd788c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 06:08:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 13:59:14 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 02 Feb 2024 13:59:14 GMT
ENV KAPACITOR_VERSION=1.6.6
# Fri, 02 Feb 2024 13:59:20 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 02 Feb 2024 13:59:21 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 02 Feb 2024 13:59:21 GMT
EXPOSE 9092
# Fri, 02 Feb 2024 13:59:21 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 02 Feb 2024 13:59:21 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 02 Feb 2024 13:59:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Feb 2024 13:59:21 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f878699563001dd13af8a2a2be4cb45e2cb471c031640febe317ce10fc2170`  
		Last Modified: Fri, 02 Feb 2024 06:23:56 GMT  
		Size: 7.1 MB (7124768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0635c3a4494e04f3f93cd0a10620b235c6c0d92a9e1bb7432147e012c97e005`  
		Last Modified: Fri, 02 Feb 2024 13:59:51 GMT  
		Size: 33.9 MB (33861084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3399e78162211c4cb73b607bbbfe8c6e4f21d8f3366452998452115b2c453e7c`  
		Last Modified: Fri, 02 Feb 2024 13:59:55 GMT  
		Size: 65.7 MB (65672647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd017919d0908ee4f4833c824e5451274dd25ed6fb8005e2c7bcdd80d5c936ab`  
		Last Modified: Fri, 02 Feb 2024 13:59:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435f10d21327119f767c4bf60e16cd38998541c24ffcd54ec762f72995f50ef8`  
		Last Modified: Fri, 02 Feb 2024 13:59:48 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:0de773d9e7d16d1ee20369e8bcd118dbb200aabf81e5b89878b9c7c3b9fb1ade
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128517142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2977e29d7425dd03f5fa2f3cd006f7f7a48685f2ea89be29001caf294325478d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:53:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 04:57:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 02 Feb 2024 04:57:58 GMT
ENV KAPACITOR_VERSION=1.6.6
# Fri, 02 Feb 2024 04:58:08 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 02 Feb 2024 04:58:09 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 02 Feb 2024 04:58:09 GMT
EXPOSE 9092
# Fri, 02 Feb 2024 04:58:09 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 02 Feb 2024 04:58:09 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 02 Feb 2024 04:58:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Feb 2024 04:58:09 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57615041bb837af81ea37dafb5ff3318adf1f465d1d0400b08861b7f4d941f26`  
		Last Modified: Fri, 02 Feb 2024 01:08:50 GMT  
		Size: 7.1 MB (7069612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6c4ee752a1d504e0a19443c6e1f382520b669f8dbb6c21903351b1c2b5ea63`  
		Last Modified: Fri, 02 Feb 2024 04:58:34 GMT  
		Size: 31.4 MB (31377429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d8598abf3a3de472fc0e10dc5e36321953962a1272249b320d85fb99a11b05`  
		Last Modified: Fri, 02 Feb 2024 04:58:38 GMT  
		Size: 61.7 MB (61669543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b469c51b0c2b1de59753828029058530fe0ff389bb605a1db2d4f4b98391f133`  
		Last Modified: Fri, 02 Feb 2024 04:58:32 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08978c95365a6280a0449076eb9df955e9afc8060ec27b364a5554d3bc5758b2`  
		Last Modified: Fri, 02 Feb 2024 04:58:32 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.6-alpine`

```console
$ docker pull kapacitor@sha256:f8903d066b21bf5e82d40aaeb58c7e68efc90ccd57ddb7e9c52e2cafafa09a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:06347afab43da8df027ff10947d6670aaabc2a2ca831279adc0b6068d3fc27c5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68673587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:757e5f922a3d3ba684a1da75d0b44453e7f67bb8d8de80bfccbe45babba1eb07`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:11:03 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 03:11:04 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 27 Jan 2024 03:11:04 GMT
ENV KAPACITOR_VERSION=1.6.6
# Sat, 27 Jan 2024 03:11:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 27 Jan 2024 03:11:12 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 27 Jan 2024 03:11:13 GMT
EXPOSE 9092
# Sat, 27 Jan 2024 03:11:13 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 27 Jan 2024 03:11:13 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Sat, 27 Jan 2024 03:11:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:11:13 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1981f85a6ddb3ff81c270c81d04678451bef3fb97b1fbe5b30df99cb229b83`  
		Last Modified: Sat, 27 Jan 2024 03:11:42 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d9b2f0b9e186c111bce293403aa46c8958add2c8ab737e0b0f535f808e00147`  
		Last Modified: Sat, 27 Jan 2024 03:11:42 GMT  
		Size: 284.9 KB (284903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45e8d5853d4f2abfcc668e3965ccc64dbb3fb610dde865a0c94604160618fc6`  
		Last Modified: Sat, 27 Jan 2024 03:11:50 GMT  
		Size: 65.6 MB (65580116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e218e640d15bd6edbc021db3afcc778eafea2a26b142d478f8c9baa6dbd06ad1`  
		Last Modified: Sat, 27 Jan 2024 03:11:42 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df2475d0a01cd1778c4037ab7779e906fdc57ec17db3e87763fbca5b4c5b1c0`  
		Last Modified: Sat, 27 Jan 2024 03:11:42 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.6.6`

```console
$ docker pull kapacitor@sha256:3bc6ebdfc932fe5d96e13a4029094ab32d7c2e68c98b782941839d30a5b1d2b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:1.6.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:15c485e89e6aa04ccbb41973386fee60eca6951e73b20a22561192ccfec61868
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137106837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ed354479cdd4cf011b8e9907c5a439edb866273720ef2ccdc8184c61fd788c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 06:08:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 13:59:14 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 02 Feb 2024 13:59:14 GMT
ENV KAPACITOR_VERSION=1.6.6
# Fri, 02 Feb 2024 13:59:20 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 02 Feb 2024 13:59:21 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 02 Feb 2024 13:59:21 GMT
EXPOSE 9092
# Fri, 02 Feb 2024 13:59:21 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 02 Feb 2024 13:59:21 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 02 Feb 2024 13:59:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Feb 2024 13:59:21 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f878699563001dd13af8a2a2be4cb45e2cb471c031640febe317ce10fc2170`  
		Last Modified: Fri, 02 Feb 2024 06:23:56 GMT  
		Size: 7.1 MB (7124768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0635c3a4494e04f3f93cd0a10620b235c6c0d92a9e1bb7432147e012c97e005`  
		Last Modified: Fri, 02 Feb 2024 13:59:51 GMT  
		Size: 33.9 MB (33861084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3399e78162211c4cb73b607bbbfe8c6e4f21d8f3366452998452115b2c453e7c`  
		Last Modified: Fri, 02 Feb 2024 13:59:55 GMT  
		Size: 65.7 MB (65672647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd017919d0908ee4f4833c824e5451274dd25ed6fb8005e2c7bcdd80d5c936ab`  
		Last Modified: Fri, 02 Feb 2024 13:59:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435f10d21327119f767c4bf60e16cd38998541c24ffcd54ec762f72995f50ef8`  
		Last Modified: Fri, 02 Feb 2024 13:59:48 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.6.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:0de773d9e7d16d1ee20369e8bcd118dbb200aabf81e5b89878b9c7c3b9fb1ade
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128517142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2977e29d7425dd03f5fa2f3cd006f7f7a48685f2ea89be29001caf294325478d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:53:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 04:57:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 02 Feb 2024 04:57:58 GMT
ENV KAPACITOR_VERSION=1.6.6
# Fri, 02 Feb 2024 04:58:08 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 02 Feb 2024 04:58:09 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 02 Feb 2024 04:58:09 GMT
EXPOSE 9092
# Fri, 02 Feb 2024 04:58:09 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 02 Feb 2024 04:58:09 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 02 Feb 2024 04:58:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Feb 2024 04:58:09 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57615041bb837af81ea37dafb5ff3318adf1f465d1d0400b08861b7f4d941f26`  
		Last Modified: Fri, 02 Feb 2024 01:08:50 GMT  
		Size: 7.1 MB (7069612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6c4ee752a1d504e0a19443c6e1f382520b669f8dbb6c21903351b1c2b5ea63`  
		Last Modified: Fri, 02 Feb 2024 04:58:34 GMT  
		Size: 31.4 MB (31377429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d8598abf3a3de472fc0e10dc5e36321953962a1272249b320d85fb99a11b05`  
		Last Modified: Fri, 02 Feb 2024 04:58:38 GMT  
		Size: 61.7 MB (61669543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b469c51b0c2b1de59753828029058530fe0ff389bb605a1db2d4f4b98391f133`  
		Last Modified: Fri, 02 Feb 2024 04:58:32 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08978c95365a6280a0449076eb9df955e9afc8060ec27b364a5554d3bc5758b2`  
		Last Modified: Fri, 02 Feb 2024 04:58:32 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.6.6-alpine`

```console
$ docker pull kapacitor@sha256:f8903d066b21bf5e82d40aaeb58c7e68efc90ccd57ddb7e9c52e2cafafa09a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.6.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:06347afab43da8df027ff10947d6670aaabc2a2ca831279adc0b6068d3fc27c5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68673587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:757e5f922a3d3ba684a1da75d0b44453e7f67bb8d8de80bfccbe45babba1eb07`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:11:03 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 03:11:04 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 27 Jan 2024 03:11:04 GMT
ENV KAPACITOR_VERSION=1.6.6
# Sat, 27 Jan 2024 03:11:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 27 Jan 2024 03:11:12 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 27 Jan 2024 03:11:13 GMT
EXPOSE 9092
# Sat, 27 Jan 2024 03:11:13 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 27 Jan 2024 03:11:13 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Sat, 27 Jan 2024 03:11:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:11:13 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1981f85a6ddb3ff81c270c81d04678451bef3fb97b1fbe5b30df99cb229b83`  
		Last Modified: Sat, 27 Jan 2024 03:11:42 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d9b2f0b9e186c111bce293403aa46c8958add2c8ab737e0b0f535f808e00147`  
		Last Modified: Sat, 27 Jan 2024 03:11:42 GMT  
		Size: 284.9 KB (284903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45e8d5853d4f2abfcc668e3965ccc64dbb3fb610dde865a0c94604160618fc6`  
		Last Modified: Sat, 27 Jan 2024 03:11:50 GMT  
		Size: 65.6 MB (65580116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e218e640d15bd6edbc021db3afcc778eafea2a26b142d478f8c9baa6dbd06ad1`  
		Last Modified: Sat, 27 Jan 2024 03:11:42 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df2475d0a01cd1778c4037ab7779e906fdc57ec17db3e87763fbca5b4c5b1c0`  
		Last Modified: Sat, 27 Jan 2024 03:11:42 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.7`

```console
$ docker pull kapacitor@sha256:ab04553c3b813f6851ad495e1a17afd0e83f9704524ae71098d5c18b37a06626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:1.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:b2223b6612d59723eba7535392f50b2674168328e5e02087ee76933c8635e6cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138183873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51fceffa235cf424ba03ace13feaef7f556c61dc4e1455f1ae0c8ab557748bed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 06:08:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 13:59:14 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 02 Feb 2024 13:59:28 GMT
ENV KAPACITOR_VERSION=1.7.1
# Fri, 02 Feb 2024 13:59:32 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 02 Feb 2024 13:59:32 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 02 Feb 2024 13:59:33 GMT
EXPOSE 9092
# Fri, 02 Feb 2024 13:59:33 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 02 Feb 2024 13:59:33 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 02 Feb 2024 13:59:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Feb 2024 13:59:33 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f878699563001dd13af8a2a2be4cb45e2cb471c031640febe317ce10fc2170`  
		Last Modified: Fri, 02 Feb 2024 06:23:56 GMT  
		Size: 7.1 MB (7124768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0635c3a4494e04f3f93cd0a10620b235c6c0d92a9e1bb7432147e012c97e005`  
		Last Modified: Fri, 02 Feb 2024 13:59:51 GMT  
		Size: 33.9 MB (33861084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b1cfb774f3a31da89c64677cb79af23a2bdc5f210a60ecdec7505df491b51b`  
		Last Modified: Fri, 02 Feb 2024 14:00:20 GMT  
		Size: 66.7 MB (66749685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc0ecdb761e6636b2b49461789485f1f7ef71c0d1b50ad2ff985c843cf52685`  
		Last Modified: Fri, 02 Feb 2024 14:00:12 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292db75fab5ccb43079b0890eae0245865bedb6ba0c2e93fa0ecdacf31ab27f9`  
		Last Modified: Fri, 02 Feb 2024 14:00:12 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:5e87deff84a56618a556f516f1aade22e36611861acaec89e386bd09c1b98d75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129155350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26174d81ebdf6fe35f69686ab89aacd1818edf0f808c286ca27405e198cfda64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:53:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 04:57:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 02 Feb 2024 04:58:12 GMT
ENV KAPACITOR_VERSION=1.7.1
# Fri, 02 Feb 2024 04:58:21 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 02 Feb 2024 04:58:22 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 02 Feb 2024 04:58:22 GMT
EXPOSE 9092
# Fri, 02 Feb 2024 04:58:22 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 02 Feb 2024 04:58:23 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 02 Feb 2024 04:58:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Feb 2024 04:58:23 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57615041bb837af81ea37dafb5ff3318adf1f465d1d0400b08861b7f4d941f26`  
		Last Modified: Fri, 02 Feb 2024 01:08:50 GMT  
		Size: 7.1 MB (7069612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6c4ee752a1d504e0a19443c6e1f382520b669f8dbb6c21903351b1c2b5ea63`  
		Last Modified: Fri, 02 Feb 2024 04:58:34 GMT  
		Size: 31.4 MB (31377429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c189723df11a77265f18e9e988eed49d25925bb4905764adce63e98f047405cf`  
		Last Modified: Fri, 02 Feb 2024 04:58:52 GMT  
		Size: 62.3 MB (62307750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6cd34ebe7c4f121cf11fd9aa60876fabf5d28b849cb8ced330135ad2ebe8a8`  
		Last Modified: Fri, 02 Feb 2024 04:58:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03aaed2c4b7d9a197da1ce10cc0fc7abb5edf1b54882509206ab68aabb718a68`  
		Last Modified: Fri, 02 Feb 2024 04:58:46 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.7-alpine`

```console
$ docker pull kapacitor@sha256:0975e5159996bac99267262826828ebf4f0c3de80f95459926f7fff6dd4b5399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.7-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:823242fda33427a4cff06232da73950071be503ab76bb69edc60f03590a6b466
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70368926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4079bd1231313ebde05598b665f9e0ab4bc42a865e4aeb08c41d4726a66e58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:11:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 03:11:21 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 27 Jan 2024 03:11:21 GMT
ENV KAPACITOR_VERSION=1.7.1
# Sat, 27 Jan 2024 03:11:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 27 Jan 2024 03:11:30 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 27 Jan 2024 03:11:30 GMT
EXPOSE 9092
# Sat, 27 Jan 2024 03:11:30 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 27 Jan 2024 03:11:30 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Sat, 27 Jan 2024 03:11:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:11:30 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27c0340c3b428b118deb541dd857e5413c0ea787e9ba56ae54589ea731c7730`  
		Last Modified: Sat, 27 Jan 2024 03:12:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24534ed772762b2bbf09082d1b3308d3f8c7dccd367ecbd54b5c74c15eeafde`  
		Last Modified: Sat, 27 Jan 2024 03:12:00 GMT  
		Size: 284.7 KB (284696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e1ec171cc850565cce60b31a46487fe3b130ba2370fa3a0a0ab57e1edd2cf7`  
		Last Modified: Sat, 27 Jan 2024 03:12:07 GMT  
		Size: 66.7 MB (66680952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c359b09645a3ee56afff4f6d4ae15b4b7a40b3b67cf97028ecda2383011055ac`  
		Last Modified: Sat, 27 Jan 2024 03:12:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d85f62ebbfd1b423d4f71800ec719cb0b1200d240fc38d24e791478aa09be1e`  
		Last Modified: Sat, 27 Jan 2024 03:12:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.7.1`

```console
$ docker pull kapacitor@sha256:ab04553c3b813f6851ad495e1a17afd0e83f9704524ae71098d5c18b37a06626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:1.7.1` - linux; amd64

```console
$ docker pull kapacitor@sha256:b2223b6612d59723eba7535392f50b2674168328e5e02087ee76933c8635e6cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138183873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51fceffa235cf424ba03ace13feaef7f556c61dc4e1455f1ae0c8ab557748bed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 06:08:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 13:59:14 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 02 Feb 2024 13:59:28 GMT
ENV KAPACITOR_VERSION=1.7.1
# Fri, 02 Feb 2024 13:59:32 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 02 Feb 2024 13:59:32 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 02 Feb 2024 13:59:33 GMT
EXPOSE 9092
# Fri, 02 Feb 2024 13:59:33 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 02 Feb 2024 13:59:33 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 02 Feb 2024 13:59:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Feb 2024 13:59:33 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f878699563001dd13af8a2a2be4cb45e2cb471c031640febe317ce10fc2170`  
		Last Modified: Fri, 02 Feb 2024 06:23:56 GMT  
		Size: 7.1 MB (7124768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0635c3a4494e04f3f93cd0a10620b235c6c0d92a9e1bb7432147e012c97e005`  
		Last Modified: Fri, 02 Feb 2024 13:59:51 GMT  
		Size: 33.9 MB (33861084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b1cfb774f3a31da89c64677cb79af23a2bdc5f210a60ecdec7505df491b51b`  
		Last Modified: Fri, 02 Feb 2024 14:00:20 GMT  
		Size: 66.7 MB (66749685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc0ecdb761e6636b2b49461789485f1f7ef71c0d1b50ad2ff985c843cf52685`  
		Last Modified: Fri, 02 Feb 2024 14:00:12 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292db75fab5ccb43079b0890eae0245865bedb6ba0c2e93fa0ecdacf31ab27f9`  
		Last Modified: Fri, 02 Feb 2024 14:00:12 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.7.1` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:5e87deff84a56618a556f516f1aade22e36611861acaec89e386bd09c1b98d75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129155350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26174d81ebdf6fe35f69686ab89aacd1818edf0f808c286ca27405e198cfda64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:53:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 04:57:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 02 Feb 2024 04:58:12 GMT
ENV KAPACITOR_VERSION=1.7.1
# Fri, 02 Feb 2024 04:58:21 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 02 Feb 2024 04:58:22 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 02 Feb 2024 04:58:22 GMT
EXPOSE 9092
# Fri, 02 Feb 2024 04:58:22 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 02 Feb 2024 04:58:23 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 02 Feb 2024 04:58:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Feb 2024 04:58:23 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57615041bb837af81ea37dafb5ff3318adf1f465d1d0400b08861b7f4d941f26`  
		Last Modified: Fri, 02 Feb 2024 01:08:50 GMT  
		Size: 7.1 MB (7069612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6c4ee752a1d504e0a19443c6e1f382520b669f8dbb6c21903351b1c2b5ea63`  
		Last Modified: Fri, 02 Feb 2024 04:58:34 GMT  
		Size: 31.4 MB (31377429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c189723df11a77265f18e9e988eed49d25925bb4905764adce63e98f047405cf`  
		Last Modified: Fri, 02 Feb 2024 04:58:52 GMT  
		Size: 62.3 MB (62307750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6cd34ebe7c4f121cf11fd9aa60876fabf5d28b849cb8ced330135ad2ebe8a8`  
		Last Modified: Fri, 02 Feb 2024 04:58:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03aaed2c4b7d9a197da1ce10cc0fc7abb5edf1b54882509206ab68aabb718a68`  
		Last Modified: Fri, 02 Feb 2024 04:58:46 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.7.1-alpine`

```console
$ docker pull kapacitor@sha256:0975e5159996bac99267262826828ebf4f0c3de80f95459926f7fff6dd4b5399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.7.1-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:823242fda33427a4cff06232da73950071be503ab76bb69edc60f03590a6b466
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70368926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4079bd1231313ebde05598b665f9e0ab4bc42a865e4aeb08c41d4726a66e58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:11:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 03:11:21 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 27 Jan 2024 03:11:21 GMT
ENV KAPACITOR_VERSION=1.7.1
# Sat, 27 Jan 2024 03:11:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 27 Jan 2024 03:11:30 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 27 Jan 2024 03:11:30 GMT
EXPOSE 9092
# Sat, 27 Jan 2024 03:11:30 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 27 Jan 2024 03:11:30 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Sat, 27 Jan 2024 03:11:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:11:30 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27c0340c3b428b118deb541dd857e5413c0ea787e9ba56ae54589ea731c7730`  
		Last Modified: Sat, 27 Jan 2024 03:12:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24534ed772762b2bbf09082d1b3308d3f8c7dccd367ecbd54b5c74c15eeafde`  
		Last Modified: Sat, 27 Jan 2024 03:12:00 GMT  
		Size: 284.7 KB (284696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e1ec171cc850565cce60b31a46487fe3b130ba2370fa3a0a0ab57e1edd2cf7`  
		Last Modified: Sat, 27 Jan 2024 03:12:07 GMT  
		Size: 66.7 MB (66680952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c359b09645a3ee56afff4f6d4ae15b4b7a40b3b67cf97028ecda2383011055ac`  
		Last Modified: Sat, 27 Jan 2024 03:12:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d85f62ebbfd1b423d4f71800ec719cb0b1200d240fc38d24e791478aa09be1e`  
		Last Modified: Sat, 27 Jan 2024 03:12:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:0975e5159996bac99267262826828ebf4f0c3de80f95459926f7fff6dd4b5399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:823242fda33427a4cff06232da73950071be503ab76bb69edc60f03590a6b466
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70368926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a4079bd1231313ebde05598b665f9e0ab4bc42a865e4aeb08c41d4726a66e58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:11:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 27 Jan 2024 03:11:21 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 27 Jan 2024 03:11:21 GMT
ENV KAPACITOR_VERSION=1.7.1
# Sat, 27 Jan 2024 03:11:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 27 Jan 2024 03:11:30 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 27 Jan 2024 03:11:30 GMT
EXPOSE 9092
# Sat, 27 Jan 2024 03:11:30 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 27 Jan 2024 03:11:30 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Sat, 27 Jan 2024 03:11:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 27 Jan 2024 03:11:30 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27c0340c3b428b118deb541dd857e5413c0ea787e9ba56ae54589ea731c7730`  
		Last Modified: Sat, 27 Jan 2024 03:12:00 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24534ed772762b2bbf09082d1b3308d3f8c7dccd367ecbd54b5c74c15eeafde`  
		Last Modified: Sat, 27 Jan 2024 03:12:00 GMT  
		Size: 284.7 KB (284696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76e1ec171cc850565cce60b31a46487fe3b130ba2370fa3a0a0ab57e1edd2cf7`  
		Last Modified: Sat, 27 Jan 2024 03:12:07 GMT  
		Size: 66.7 MB (66680952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c359b09645a3ee56afff4f6d4ae15b4b7a40b3b67cf97028ecda2383011055ac`  
		Last Modified: Sat, 27 Jan 2024 03:12:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d85f62ebbfd1b423d4f71800ec719cb0b1200d240fc38d24e791478aa09be1e`  
		Last Modified: Sat, 27 Jan 2024 03:12:00 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:ab04553c3b813f6851ad495e1a17afd0e83f9704524ae71098d5c18b37a06626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:b2223b6612d59723eba7535392f50b2674168328e5e02087ee76933c8635e6cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138183873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51fceffa235cf424ba03ace13feaef7f556c61dc4e1455f1ae0c8ab557748bed`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 06:08:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 13:59:14 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 02 Feb 2024 13:59:28 GMT
ENV KAPACITOR_VERSION=1.7.1
# Fri, 02 Feb 2024 13:59:32 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 02 Feb 2024 13:59:32 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 02 Feb 2024 13:59:33 GMT
EXPOSE 9092
# Fri, 02 Feb 2024 13:59:33 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 02 Feb 2024 13:59:33 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 02 Feb 2024 13:59:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Feb 2024 13:59:33 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f878699563001dd13af8a2a2be4cb45e2cb471c031640febe317ce10fc2170`  
		Last Modified: Fri, 02 Feb 2024 06:23:56 GMT  
		Size: 7.1 MB (7124768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0635c3a4494e04f3f93cd0a10620b235c6c0d92a9e1bb7432147e012c97e005`  
		Last Modified: Fri, 02 Feb 2024 13:59:51 GMT  
		Size: 33.9 MB (33861084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4b1cfb774f3a31da89c64677cb79af23a2bdc5f210a60ecdec7505df491b51b`  
		Last Modified: Fri, 02 Feb 2024 14:00:20 GMT  
		Size: 66.7 MB (66749685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc0ecdb761e6636b2b49461789485f1f7ef71c0d1b50ad2ff985c843cf52685`  
		Last Modified: Fri, 02 Feb 2024 14:00:12 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292db75fab5ccb43079b0890eae0245865bedb6ba0c2e93fa0ecdacf31ab27f9`  
		Last Modified: Fri, 02 Feb 2024 14:00:12 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:5e87deff84a56618a556f516f1aade22e36611861acaec89e386bd09c1b98d75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129155350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26174d81ebdf6fe35f69686ab89aacd1818edf0f808c286ca27405e198cfda64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:53:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Feb 2024 04:57:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 02 Feb 2024 04:58:12 GMT
ENV KAPACITOR_VERSION=1.7.1
# Fri, 02 Feb 2024 04:58:21 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 02 Feb 2024 04:58:22 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 02 Feb 2024 04:58:22 GMT
EXPOSE 9092
# Fri, 02 Feb 2024 04:58:22 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 02 Feb 2024 04:58:23 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 02 Feb 2024 04:58:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 02 Feb 2024 04:58:23 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57615041bb837af81ea37dafb5ff3318adf1f465d1d0400b08861b7f4d941f26`  
		Last Modified: Fri, 02 Feb 2024 01:08:50 GMT  
		Size: 7.1 MB (7069612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6c4ee752a1d504e0a19443c6e1f382520b669f8dbb6c21903351b1c2b5ea63`  
		Last Modified: Fri, 02 Feb 2024 04:58:34 GMT  
		Size: 31.4 MB (31377429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c189723df11a77265f18e9e988eed49d25925bb4905764adce63e98f047405cf`  
		Last Modified: Fri, 02 Feb 2024 04:58:52 GMT  
		Size: 62.3 MB (62307750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6cd34ebe7c4f121cf11fd9aa60876fabf5d28b849cb8ced330135ad2ebe8a8`  
		Last Modified: Fri, 02 Feb 2024 04:58:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03aaed2c4b7d9a197da1ce10cc0fc7abb5edf1b54882509206ab68aabb718a68`  
		Last Modified: Fri, 02 Feb 2024 04:58:46 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
