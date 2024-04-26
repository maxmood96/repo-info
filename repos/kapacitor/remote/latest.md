## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:183a54fa9301dfe2bf7f079f2e55303edf9a15c296a03fc2fe3bcdd6e81b62d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:7ae309652b3943187aaa061eeb50666049d679b5492cb9c06df3a31a453e71f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.5 MB (144517171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:518016eaeae41df047016a611c1d3e8a8086aa16e234fe96ea1c6848570b822e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 10 Apr 2024 18:52:02 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:52:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:52:02 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:52:04 GMT
ADD file:3bd10da0673e2e72cb06a1f64a9df49a36341df39b0f762e3d1b38ee4de296fa in / 
# Wed, 10 Apr 2024 18:52:04 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 03:40:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 08:35:24 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 23 Apr 2024 17:27:36 GMT
ENV KAPACITOR_VERSION=1.7.4
# Tue, 23 Apr 2024 17:27:44 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 23 Apr 2024 17:27:44 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 23 Apr 2024 17:27:44 GMT
EXPOSE 9092
# Tue, 23 Apr 2024 17:27:44 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 23 Apr 2024 17:27:44 GMT
COPY file:d13199909208ae1b9e95c89c9f0f75ecda30911090da90e33a2c258a88927a06 in /entrypoint.sh 
# Tue, 23 Apr 2024 17:27:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Apr 2024 17:27:45 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:7021d1b70935851c95c45ed18156980b5024eda29b99564429025ea04f5ec109`  
		Last Modified: Thu, 11 Apr 2024 03:03:17 GMT  
		Size: 30.4 MB (30439778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249eb94103ac8f46c5e107614671e5472704b140376c4d3c1ab649f68b2a68e8`  
		Last Modified: Tue, 16 Apr 2024 03:53:38 GMT  
		Size: 7.1 MB (7122310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245d2a76044b55ac5ed9050a8baf3309a018b205002a5a7bf0585a647f9ac805`  
		Last Modified: Tue, 16 Apr 2024 08:36:04 GMT  
		Size: 35.6 MB (35577626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3c020d61d6731bfadbeec60244f23287c686e0181a150ab4f7e00fbda5c0fb`  
		Last Modified: Tue, 23 Apr 2024 17:28:23 GMT  
		Size: 71.4 MB (71376935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de9171898e67d23ff6a425a3d84a6dd701c7905cac0978f08b8a75de01e1085`  
		Last Modified: Tue, 23 Apr 2024 17:28:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fccb52ee5db43c6f53a730c5f55047db1fc77613231a3711ecbff7fad87f2d`  
		Last Modified: Tue, 23 Apr 2024 17:28:15 GMT  
		Size: 296.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:3ebdd391e42c9c18ffbf5bdb4953619b49c830e013e0bd53617453ecfb022c1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135847907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3beaa22b4863bbd0a0586ec588a3bf800735e8e92224b224be7fcb3ea6f63533`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 17 Apr 2024 18:24:57 GMT
ARG RELEASE
# Wed, 17 Apr 2024 18:24:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 18:24:57 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 18:24:59 GMT
ADD file:51afefc6be37e5e27507b9b77fca51df26536c9827fe51acac6a4f9c1ebd60e8 in / 
# Wed, 17 Apr 2024 18:24:59 GMT
CMD ["/bin/bash"]
# Thu, 25 Apr 2024 21:15:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Apr 2024 01:00:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 26 Apr 2024 01:00:53 GMT
ENV KAPACITOR_VERSION=1.7.4
# Fri, 26 Apr 2024 01:00:58 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 26 Apr 2024 01:00:59 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 26 Apr 2024 01:00:59 GMT
EXPOSE 9092
# Fri, 26 Apr 2024 01:00:59 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 26 Apr 2024 01:01:00 GMT
COPY file:d13199909208ae1b9e95c89c9f0f75ecda30911090da90e33a2c258a88927a06 in /entrypoint.sh 
# Fri, 26 Apr 2024 01:01:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 01:01:00 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c6efd61b232e6060a5ae247be4a304ae261939d0814281b2db15ac1c5f6b35`  
		Last Modified: Thu, 25 Apr 2024 21:45:59 GMT  
		Size: 7.1 MB (7068156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c573c773c94d8b8272cec2c0dafcce53fadb7bc25b04a1ac4fb3823c35f75aa7`  
		Last Modified: Fri, 26 Apr 2024 01:01:11 GMT  
		Size: 33.3 MB (33283190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c04a191c325921f14f601aff49ca006e06332113d4ac5d070c2619f45abb790`  
		Last Modified: Fri, 26 Apr 2024 01:01:30 GMT  
		Size: 67.1 MB (67095037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5cca6ca8dfe8e66d3f3581711649fc6b9d206e61be475de0ba3e049ab71c52`  
		Last Modified: Fri, 26 Apr 2024 01:01:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aef2b8d0a5afc1e1e350fc7bddc3a5672153b984279e6ad9dad667c06207311`  
		Last Modified: Fri, 26 Apr 2024 01:01:24 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
