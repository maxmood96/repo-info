<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.6`](#kapacitor16)
-	[`kapacitor:1.6-alpine`](#kapacitor16-alpine)
-	[`kapacitor:1.6.6`](#kapacitor166)
-	[`kapacitor:1.6.6-alpine`](#kapacitor166-alpine)
-	[`kapacitor:1.7`](#kapacitor17)
-	[`kapacitor:1.7-alpine`](#kapacitor17-alpine)
-	[`kapacitor:1.7.6`](#kapacitor176)
-	[`kapacitor:1.7.6-alpine`](#kapacitor176-alpine)
-	[`kapacitor:alpine`](#kapacitoralpine)
-	[`kapacitor:latest`](#kapacitorlatest)

## `kapacitor:1.6`

```console
$ docker pull kapacitor@sha256:fad75df82f29b97808cc3e15366af69c1edf3ac5b71ef01fb77b7c355282c9e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:948ea5cc66a64b825d771f203210d209fbea57760deb23cdd5e8b7b7140486dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141652829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda219f7420b3eb254bf340cf7f53c3f8f33919703052c56427b5b5fd4313eee`
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
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.6.6
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 08 Jan 2025 07:56:27 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8284ddf57c03d97884a998219f0fbd84edab303351cdba3ac1526a116e907210`  
		Last Modified: Sat, 19 Oct 2024 02:06:18 GMT  
		Size: 7.1 MB (7102850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31374502893792a31db584800ad37a8a541b54d0e30c206096d825a30574a30`  
		Last Modified: Sat, 19 Oct 2024 02:54:02 GMT  
		Size: 39.3 MB (39341279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315cc682eb42b199026ce3e64d0418ea12b812ac21133fda9e723fae616b9e42`  
		Last Modified: Sat, 19 Oct 2024 02:54:02 GMT  
		Size: 65.7 MB (65672554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f6f3acd66b85be15c6add078c145ee01234c38b30d3c701eb08f271c01dc66`  
		Last Modified: Sat, 19 Oct 2024 02:54:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098bccfec1724c823ff4c7a2414148d001b1cecad4d61ab440bf226d2bdbae22`  
		Last Modified: Sat, 19 Oct 2024 02:54:01 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:8850132cbde3a544a05ac1f8b59e85045c8ba00f93e9affd41ac6d65b4b6fb5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3565011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e99b44c60ad521a246cceabbd32db5cd7b1778bcbda3759d8c080788011318`

```dockerfile
```

-	Layers:
	-	`sha256:a1be9c3cf079bde45e4caea455d8295b89283842708e0e9d3eb0b4749cd31b8d`  
		Last Modified: Sat, 19 Oct 2024 02:54:01 GMT  
		Size: 3.6 MB (3550252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9466d241ff8c3adfa7213179989e03c26b0ba00e6099f59ed59740d3de8447ea`  
		Last Modified: Sat, 19 Oct 2024 02:54:01 GMT  
		Size: 14.8 KB (14759 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:47d8a973098b502ee702eb7e92c21c01c7744c1bf41f20a08d3b94221ee818c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132450612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aabb79192c1e91e6e1f6cbfa9335200f17cc54ba1447da0801cb201b0cd54cc3`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.6.6
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee2b4e5eab18cf336bf82b89529f3587544f710c5e1a0aa67e5ed1fdec85146`  
		Last Modified: Sat, 19 Oct 2024 05:22:20 GMT  
		Size: 7.0 MB (7049559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f108269d10135dbd4b3363075d4ac7f8a1e25a29362481a579a58a391634221`  
		Last Modified: Sat, 19 Oct 2024 08:36:38 GMT  
		Size: 36.4 MB (36372409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e44c854c5d337d53cbc3c7f42f791f1233430183f0aafa4c9f33c0c6f475c4`  
		Last Modified: Sat, 19 Oct 2024 08:36:38 GMT  
		Size: 61.7 MB (61669857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac37d402eadd0376717aa931ef0c5ae96d6da5b3cb8498e3014237a1384c95b9`  
		Last Modified: Sat, 19 Oct 2024 08:36:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45c278df38b191289aade2efef73c72baa10bc09f03ecc093dc6da96ed882ab`  
		Last Modified: Sat, 19 Oct 2024 08:36:37 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:15f20c366dc9dae85363efdae2a95b9da54ee56f822bdf5e3549e2d3fe8eb2e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3565372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c417e4a2505776601ff419c7544f12ff8bc8739a8dd82953dd80f22747743966`

```dockerfile
```

-	Layers:
	-	`sha256:45935f1cd8c9de13e29256bc3adf3990af6b2db7db11800e22b5a4d5082db242`  
		Last Modified: Sat, 19 Oct 2024 08:36:37 GMT  
		Size: 3.6 MB (3550518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90ed25fda9974e52c249605b05c1ebcc632f7f525730c78989f5ad225672f34f`  
		Last Modified: Sat, 19 Oct 2024 08:36:37 GMT  
		Size: 14.9 KB (14854 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.6-alpine`

```console
$ docker pull kapacitor@sha256:9d864dd84610e0003f1ef971be5a8a10f82d1b958e41d4b394f66e989d62549b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:fc0e19cd0b73fec31899ac8a0b1f54de96d56c3362f79427795196104a8db1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69473448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5c7e58c04040627fff17fdd662ba154babecc28b45a1b469494949cb7063fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 28 Oct 2024 16:40:55 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 16:40:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENV KAPACITOR_VERSION=1.6.6
# Mon, 28 Oct 2024 16:40:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 28 Oct 2024 16:40:55 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 28 Oct 2024 16:40:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 16:40:55 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3f24775b003b69a5526d11e76d24505b5df9b1318b998deb762dc39f2a45fd`  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1406daba834afb8a4dadde2da62f7252316ed45ce13d61c3004b49eb697a1c`  
		Last Modified: Tue, 07 Jan 2025 03:32:48 GMT  
		Size: 279.1 KB (279145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2dfea80bca268daf2bc3d162a2802e81376c167b2975157e1df3312afd8278d`  
		Last Modified: Tue, 07 Jan 2025 03:32:49 GMT  
		Size: 65.6 MB (65579573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e7ce44a406375f195a6eeb3d5a5f5de88507e82c61e749938cb97164b41ef7`  
		Last Modified: Tue, 07 Jan 2025 03:32:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69791b79aa8a54d6fbc6e187b32e5a9265c8eae416a853cf7d49c5f57f5cc118`  
		Last Modified: Tue, 07 Jan 2025 03:32:49 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:5daae18aba149cd35b03fe11e1d6f73fa56b46df0c08d2de2ac9a74e9ea3d666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.6 KB (367562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2456fd6e86ed5a543da7f67fc019b0ec6949f6c2293d3941945b681cf90b731b`

```dockerfile
```

-	Layers:
	-	`sha256:e0e30e704b06d8312367852ac0b74b4480a9bf44e447e9713f099f82b1245c27`  
		Last Modified: Tue, 07 Jan 2025 03:32:48 GMT  
		Size: 352.8 KB (352800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41d909e63778af62596a279dbe784b4f6460d99802dff1d11a2a9d2eefbe2250`  
		Last Modified: Tue, 07 Jan 2025 03:32:48 GMT  
		Size: 14.8 KB (14762 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.6.6`

```console
$ docker pull kapacitor@sha256:fad75df82f29b97808cc3e15366af69c1edf3ac5b71ef01fb77b7c355282c9e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.6.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:948ea5cc66a64b825d771f203210d209fbea57760deb23cdd5e8b7b7140486dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141652829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cda219f7420b3eb254bf340cf7f53c3f8f33919703052c56427b5b5fd4313eee`
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
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.6.6
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 08 Jan 2025 07:56:27 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8284ddf57c03d97884a998219f0fbd84edab303351cdba3ac1526a116e907210`  
		Last Modified: Sat, 19 Oct 2024 02:06:18 GMT  
		Size: 7.1 MB (7102850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31374502893792a31db584800ad37a8a541b54d0e30c206096d825a30574a30`  
		Last Modified: Sat, 19 Oct 2024 02:54:02 GMT  
		Size: 39.3 MB (39341279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315cc682eb42b199026ce3e64d0418ea12b812ac21133fda9e723fae616b9e42`  
		Last Modified: Sat, 19 Oct 2024 02:54:02 GMT  
		Size: 65.7 MB (65672554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f6f3acd66b85be15c6add078c145ee01234c38b30d3c701eb08f271c01dc66`  
		Last Modified: Sat, 19 Oct 2024 02:54:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098bccfec1724c823ff4c7a2414148d001b1cecad4d61ab440bf226d2bdbae22`  
		Last Modified: Sat, 19 Oct 2024 02:54:01 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:8850132cbde3a544a05ac1f8b59e85045c8ba00f93e9affd41ac6d65b4b6fb5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3565011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e99b44c60ad521a246cceabbd32db5cd7b1778bcbda3759d8c080788011318`

```dockerfile
```

-	Layers:
	-	`sha256:a1be9c3cf079bde45e4caea455d8295b89283842708e0e9d3eb0b4749cd31b8d`  
		Last Modified: Sat, 19 Oct 2024 02:54:01 GMT  
		Size: 3.6 MB (3550252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9466d241ff8c3adfa7213179989e03c26b0ba00e6099f59ed59740d3de8447ea`  
		Last Modified: Sat, 19 Oct 2024 02:54:01 GMT  
		Size: 14.8 KB (14759 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.6.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:47d8a973098b502ee702eb7e92c21c01c7744c1bf41f20a08d3b94221ee818c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132450612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aabb79192c1e91e6e1f6cbfa9335200f17cc54ba1447da0801cb201b0cd54cc3`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.6.6
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee2b4e5eab18cf336bf82b89529f3587544f710c5e1a0aa67e5ed1fdec85146`  
		Last Modified: Sat, 19 Oct 2024 05:22:20 GMT  
		Size: 7.0 MB (7049559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f108269d10135dbd4b3363075d4ac7f8a1e25a29362481a579a58a391634221`  
		Last Modified: Sat, 19 Oct 2024 08:36:38 GMT  
		Size: 36.4 MB (36372409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e44c854c5d337d53cbc3c7f42f791f1233430183f0aafa4c9f33c0c6f475c4`  
		Last Modified: Sat, 19 Oct 2024 08:36:38 GMT  
		Size: 61.7 MB (61669857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac37d402eadd0376717aa931ef0c5ae96d6da5b3cb8498e3014237a1384c95b9`  
		Last Modified: Sat, 19 Oct 2024 08:36:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45c278df38b191289aade2efef73c72baa10bc09f03ecc093dc6da96ed882ab`  
		Last Modified: Sat, 19 Oct 2024 08:36:37 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:15f20c366dc9dae85363efdae2a95b9da54ee56f822bdf5e3549e2d3fe8eb2e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3565372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c417e4a2505776601ff419c7544f12ff8bc8739a8dd82953dd80f22747743966`

```dockerfile
```

-	Layers:
	-	`sha256:45935f1cd8c9de13e29256bc3adf3990af6b2db7db11800e22b5a4d5082db242`  
		Last Modified: Sat, 19 Oct 2024 08:36:37 GMT  
		Size: 3.6 MB (3550518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90ed25fda9974e52c249605b05c1ebcc632f7f525730c78989f5ad225672f34f`  
		Last Modified: Sat, 19 Oct 2024 08:36:37 GMT  
		Size: 14.9 KB (14854 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.6.6-alpine`

```console
$ docker pull kapacitor@sha256:9d864dd84610e0003f1ef971be5a8a10f82d1b958e41d4b394f66e989d62549b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.6.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:fc0e19cd0b73fec31899ac8a0b1f54de96d56c3362f79427795196104a8db1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69473448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5c7e58c04040627fff17fdd662ba154babecc28b45a1b469494949cb7063fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 28 Oct 2024 16:40:55 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 16:40:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENV KAPACITOR_VERSION=1.6.6
# Mon, 28 Oct 2024 16:40:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 28 Oct 2024 16:40:55 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 28 Oct 2024 16:40:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 16:40:55 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3f24775b003b69a5526d11e76d24505b5df9b1318b998deb762dc39f2a45fd`  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1406daba834afb8a4dadde2da62f7252316ed45ce13d61c3004b49eb697a1c`  
		Last Modified: Tue, 07 Jan 2025 03:32:48 GMT  
		Size: 279.1 KB (279145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2dfea80bca268daf2bc3d162a2802e81376c167b2975157e1df3312afd8278d`  
		Last Modified: Tue, 07 Jan 2025 03:32:49 GMT  
		Size: 65.6 MB (65579573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e7ce44a406375f195a6eeb3d5a5f5de88507e82c61e749938cb97164b41ef7`  
		Last Modified: Tue, 07 Jan 2025 03:32:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69791b79aa8a54d6fbc6e187b32e5a9265c8eae416a853cf7d49c5f57f5cc118`  
		Last Modified: Tue, 07 Jan 2025 03:32:49 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6.6-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:5daae18aba149cd35b03fe11e1d6f73fa56b46df0c08d2de2ac9a74e9ea3d666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.6 KB (367562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2456fd6e86ed5a543da7f67fc019b0ec6949f6c2293d3941945b681cf90b731b`

```dockerfile
```

-	Layers:
	-	`sha256:e0e30e704b06d8312367852ac0b74b4480a9bf44e447e9713f099f82b1245c27`  
		Last Modified: Tue, 07 Jan 2025 03:32:48 GMT  
		Size: 352.8 KB (352800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41d909e63778af62596a279dbe784b4f6460d99802dff1d11a2a9d2eefbe2250`  
		Last Modified: Tue, 07 Jan 2025 03:32:48 GMT  
		Size: 14.8 KB (14762 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7`

```console
$ docker pull kapacitor@sha256:f6e635fa0941005fe16a4bd14164e009226fbee0579a22372ff390228a8cc630
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:9739f88fde1e2dacbeabfdaa58a5195804b81fcb76dd474b4ea8e46bd7d7641c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.1 MB (148052695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83447930c54621bbc4681d7122a155341835c9e878d8bb8fe49fc14f0fc45a54`
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
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENV KAPACITOR_VERSION=1.7.6
# Mon, 28 Oct 2024 16:40:55 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 28 Oct 2024 16:40:55 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 28 Oct 2024 16:40:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 16:40:55 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 08 Jan 2025 07:56:27 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8284ddf57c03d97884a998219f0fbd84edab303351cdba3ac1526a116e907210`  
		Last Modified: Sat, 19 Oct 2024 02:06:18 GMT  
		Size: 7.1 MB (7102850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df56e827619a8fb6da0a24519f0ce4465e5ea92183062cddea4fcfe92d548dca`  
		Size: 39.4 MB (39366403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0642dd44f5a4b0dc896f854e9689f9e4e2763fd4c0385361ba87348c7872558`  
		Last Modified: Mon, 28 Oct 2024 17:57:28 GMT  
		Size: 72.0 MB (72047234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b583b675d8473487b78bec0b60484b0045b1c41c0da69cd77fff304a82749ef6`  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bfa4793acdf6f4ecd3c2bec17b016dfe800982f15676e56822b6e2d6300c31`  
		Last Modified: Mon, 28 Oct 2024 17:57:27 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:d79d8985adbba054947f41b563714a4a711947d9ee8fbb621d1df061d502d370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9834f59514a211f8ac46503771209c68359602f2ee3ecc9b66d89cf2e570cf51`

```dockerfile
```

-	Layers:
	-	`sha256:15b66889746a6519923422c83cc5851fe9bf2ea0d4399221c7f7d43aad829d7a`  
		Size: 3.6 MB (3558208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a1b59fc636e119fda6a8a8384166ed7b8a7d5d1214839c0d46a6e643a4e0823`  
		Last Modified: Mon, 28 Oct 2024 17:57:27 GMT  
		Size: 15.1 KB (15063 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:455d8810abbdcf76f21629d4032b060a586d6e57ea9f2b9e6f8519a96985cdba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138620010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643fca6b41a8acced90879840bd6e8b12af952a23033f435a4036daadf4b961c`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENV KAPACITOR_VERSION=1.7.6
# Mon, 28 Oct 2024 16:40:55 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 28 Oct 2024 16:40:55 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 28 Oct 2024 16:40:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 16:40:55 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee2b4e5eab18cf336bf82b89529f3587544f710c5e1a0aa67e5ed1fdec85146`  
		Last Modified: Sat, 19 Oct 2024 05:22:20 GMT  
		Size: 7.0 MB (7049559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56450686787eef42d2d8303b7ad5e724b5f247ffd66c187984bc8427445cb31`  
		Last Modified: Mon, 28 Oct 2024 18:00:32 GMT  
		Size: 36.4 MB (36389576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634c45466d4e6828fe17d0f2b71e63c7d093da3b2453e59d53a29db0009ee8e7`  
		Last Modified: Mon, 28 Oct 2024 18:00:33 GMT  
		Size: 67.8 MB (67822024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34771b86c1d3ad4939ac7fd39a5cc7abd79efb4d9175389fcb6ac5cff0a846d9`  
		Last Modified: Mon, 28 Oct 2024 18:00:31 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9cca3ffb481c2e26b551a92a3bf8d7fc5eaeea50d65f7d122a72f3f802c62b6`  
		Last Modified: Mon, 28 Oct 2024 18:00:31 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:24a674e39c6a9c2343c48c66b3e52b739c00bce9e1b02d981428fa7d4f0935c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8c7e97dca8e7a967b45f3afde9a859b5d68a78bd41613f51796b9c10aeb8a7`

```dockerfile
```

-	Layers:
	-	`sha256:4a47d5d67c314f2ea559bcf73354a2ab0760f4c6db95e70f1e1b6cf367331917`  
		Last Modified: Mon, 28 Oct 2024 18:00:31 GMT  
		Size: 3.6 MB (3557691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f42249fe2142067a94fd37435e4f4edb50e1ba587e013cdff7fc84f6224b77f9`  
		Last Modified: Mon, 28 Oct 2024 18:00:31 GMT  
		Size: 15.2 KB (15170 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7-alpine`

```console
$ docker pull kapacitor@sha256:081d04ede1850615af084ddcd0533c80601a7c955d5fc108dea71a566e66de22
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.7-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:19a2c4a2177a17db510b3455aeccaf09b26b34dfc1904eb93d24076c46655e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75875874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:448235eeb4366369184bd504faa3fd3a9144ec0b951459d82a4767994244e810`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 28 Oct 2024 16:40:55 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 16:40:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENV KAPACITOR_VERSION=1.7.6
# Mon, 28 Oct 2024 16:40:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 28 Oct 2024 16:40:55 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 28 Oct 2024 16:40:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 16:40:55 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5042cc15aa3f084ef338d138f4818ca1a6de97e4f056987d94bfae59511bd41d`  
		Last Modified: Tue, 07 Jan 2025 03:33:03 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a2dd5a3edbe3bb3d9f02ffb7d7691bc81f91cfa00a93e8d5096998173e052b`  
		Last Modified: Tue, 07 Jan 2025 03:33:03 GMT  
		Size: 280.9 KB (280855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac70ef3a37829d19665351ec2e30694e568a500ac0fef3da9dcc3d8c346e89e`  
		Last Modified: Tue, 07 Jan 2025 03:33:05 GMT  
		Size: 72.0 MB (71980244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ccb0c3b6c2c7cc173409f6cd25dedf19c44baf1d42efd74190b546c096a189`  
		Last Modified: Tue, 07 Jan 2025 03:33:03 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcc157a0695c33742bdaae44173f5f7f430937ae371216bfb70ee625ffc60eb`  
		Last Modified: Tue, 07 Jan 2025 03:33:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:3d10d048c07d3b656f05ef64c0220215256c6c2fe4b6cd266b58ee39dd787640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.1 KB (378139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1ef06c20907dd546d4a786d7512f5e4cc36892b93bce3ee1b708804c81b6212`

```dockerfile
```

-	Layers:
	-	`sha256:8b600c398ef76b5f1a3cff321d8a58c0e1b015a650d197f3e4104ba2b1e6e6df`  
		Last Modified: Tue, 07 Jan 2025 03:33:03 GMT  
		Size: 362.5 KB (362455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6b7930a4990a1c8c6579173d0e6b66b60e07a85ad5c72737ec18923d092101a`  
		Last Modified: Tue, 07 Jan 2025 03:33:03 GMT  
		Size: 15.7 KB (15684 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7.6`

```console
$ docker pull kapacitor@sha256:f6e635fa0941005fe16a4bd14164e009226fbee0579a22372ff390228a8cc630
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:9739f88fde1e2dacbeabfdaa58a5195804b81fcb76dd474b4ea8e46bd7d7641c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.1 MB (148052695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83447930c54621bbc4681d7122a155341835c9e878d8bb8fe49fc14f0fc45a54`
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
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENV KAPACITOR_VERSION=1.7.6
# Mon, 28 Oct 2024 16:40:55 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 28 Oct 2024 16:40:55 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 28 Oct 2024 16:40:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 16:40:55 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 08 Jan 2025 07:56:27 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8284ddf57c03d97884a998219f0fbd84edab303351cdba3ac1526a116e907210`  
		Last Modified: Sat, 19 Oct 2024 02:06:18 GMT  
		Size: 7.1 MB (7102850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df56e827619a8fb6da0a24519f0ce4465e5ea92183062cddea4fcfe92d548dca`  
		Size: 39.4 MB (39366403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0642dd44f5a4b0dc896f854e9689f9e4e2763fd4c0385361ba87348c7872558`  
		Last Modified: Mon, 28 Oct 2024 17:57:28 GMT  
		Size: 72.0 MB (72047234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b583b675d8473487b78bec0b60484b0045b1c41c0da69cd77fff304a82749ef6`  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bfa4793acdf6f4ecd3c2bec17b016dfe800982f15676e56822b6e2d6300c31`  
		Last Modified: Mon, 28 Oct 2024 17:57:27 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:d79d8985adbba054947f41b563714a4a711947d9ee8fbb621d1df061d502d370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9834f59514a211f8ac46503771209c68359602f2ee3ecc9b66d89cf2e570cf51`

```dockerfile
```

-	Layers:
	-	`sha256:15b66889746a6519923422c83cc5851fe9bf2ea0d4399221c7f7d43aad829d7a`  
		Size: 3.6 MB (3558208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a1b59fc636e119fda6a8a8384166ed7b8a7d5d1214839c0d46a6e643a4e0823`  
		Last Modified: Mon, 28 Oct 2024 17:57:27 GMT  
		Size: 15.1 KB (15063 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:455d8810abbdcf76f21629d4032b060a586d6e57ea9f2b9e6f8519a96985cdba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138620010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643fca6b41a8acced90879840bd6e8b12af952a23033f435a4036daadf4b961c`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENV KAPACITOR_VERSION=1.7.6
# Mon, 28 Oct 2024 16:40:55 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 28 Oct 2024 16:40:55 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 28 Oct 2024 16:40:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 16:40:55 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee2b4e5eab18cf336bf82b89529f3587544f710c5e1a0aa67e5ed1fdec85146`  
		Last Modified: Sat, 19 Oct 2024 05:22:20 GMT  
		Size: 7.0 MB (7049559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56450686787eef42d2d8303b7ad5e724b5f247ffd66c187984bc8427445cb31`  
		Last Modified: Mon, 28 Oct 2024 18:00:32 GMT  
		Size: 36.4 MB (36389576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634c45466d4e6828fe17d0f2b71e63c7d093da3b2453e59d53a29db0009ee8e7`  
		Last Modified: Mon, 28 Oct 2024 18:00:33 GMT  
		Size: 67.8 MB (67822024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34771b86c1d3ad4939ac7fd39a5cc7abd79efb4d9175389fcb6ac5cff0a846d9`  
		Last Modified: Mon, 28 Oct 2024 18:00:31 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9cca3ffb481c2e26b551a92a3bf8d7fc5eaeea50d65f7d122a72f3f802c62b6`  
		Last Modified: Mon, 28 Oct 2024 18:00:31 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:24a674e39c6a9c2343c48c66b3e52b739c00bce9e1b02d981428fa7d4f0935c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8c7e97dca8e7a967b45f3afde9a859b5d68a78bd41613f51796b9c10aeb8a7`

```dockerfile
```

-	Layers:
	-	`sha256:4a47d5d67c314f2ea559bcf73354a2ab0760f4c6db95e70f1e1b6cf367331917`  
		Last Modified: Mon, 28 Oct 2024 18:00:31 GMT  
		Size: 3.6 MB (3557691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f42249fe2142067a94fd37435e4f4edb50e1ba587e013cdff7fc84f6224b77f9`  
		Last Modified: Mon, 28 Oct 2024 18:00:31 GMT  
		Size: 15.2 KB (15170 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7.6-alpine`

```console
$ docker pull kapacitor@sha256:081d04ede1850615af084ddcd0533c80601a7c955d5fc108dea71a566e66de22
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.7.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:19a2c4a2177a17db510b3455aeccaf09b26b34dfc1904eb93d24076c46655e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75875874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:448235eeb4366369184bd504faa3fd3a9144ec0b951459d82a4767994244e810`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 28 Oct 2024 16:40:55 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 16:40:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENV KAPACITOR_VERSION=1.7.6
# Mon, 28 Oct 2024 16:40:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 28 Oct 2024 16:40:55 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 28 Oct 2024 16:40:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 16:40:55 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5042cc15aa3f084ef338d138f4818ca1a6de97e4f056987d94bfae59511bd41d`  
		Last Modified: Tue, 07 Jan 2025 03:33:03 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a2dd5a3edbe3bb3d9f02ffb7d7691bc81f91cfa00a93e8d5096998173e052b`  
		Last Modified: Tue, 07 Jan 2025 03:33:03 GMT  
		Size: 280.9 KB (280855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac70ef3a37829d19665351ec2e30694e568a500ac0fef3da9dcc3d8c346e89e`  
		Last Modified: Tue, 07 Jan 2025 03:33:05 GMT  
		Size: 72.0 MB (71980244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ccb0c3b6c2c7cc173409f6cd25dedf19c44baf1d42efd74190b546c096a189`  
		Last Modified: Tue, 07 Jan 2025 03:33:03 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcc157a0695c33742bdaae44173f5f7f430937ae371216bfb70ee625ffc60eb`  
		Last Modified: Tue, 07 Jan 2025 03:33:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.6-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:3d10d048c07d3b656f05ef64c0220215256c6c2fe4b6cd266b58ee39dd787640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.1 KB (378139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1ef06c20907dd546d4a786d7512f5e4cc36892b93bce3ee1b708804c81b6212`

```dockerfile
```

-	Layers:
	-	`sha256:8b600c398ef76b5f1a3cff321d8a58c0e1b015a650d197f3e4104ba2b1e6e6df`  
		Last Modified: Tue, 07 Jan 2025 03:33:03 GMT  
		Size: 362.5 KB (362455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6b7930a4990a1c8c6579173d0e6b66b60e07a85ad5c72737ec18923d092101a`  
		Last Modified: Tue, 07 Jan 2025 03:33:03 GMT  
		Size: 15.7 KB (15684 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:081d04ede1850615af084ddcd0533c80601a7c955d5fc108dea71a566e66de22
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:19a2c4a2177a17db510b3455aeccaf09b26b34dfc1904eb93d24076c46655e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75875874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:448235eeb4366369184bd504faa3fd3a9144ec0b951459d82a4767994244e810`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 28 Oct 2024 16:40:55 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
CMD ["/bin/sh"]
# Mon, 28 Oct 2024 16:40:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENV KAPACITOR_VERSION=1.7.6
# Mon, 28 Oct 2024 16:40:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 28 Oct 2024 16:40:55 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 28 Oct 2024 16:40:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 16:40:55 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5042cc15aa3f084ef338d138f4818ca1a6de97e4f056987d94bfae59511bd41d`  
		Last Modified: Tue, 07 Jan 2025 03:33:03 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a2dd5a3edbe3bb3d9f02ffb7d7691bc81f91cfa00a93e8d5096998173e052b`  
		Last Modified: Tue, 07 Jan 2025 03:33:03 GMT  
		Size: 280.9 KB (280855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac70ef3a37829d19665351ec2e30694e568a500ac0fef3da9dcc3d8c346e89e`  
		Last Modified: Tue, 07 Jan 2025 03:33:05 GMT  
		Size: 72.0 MB (71980244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ccb0c3b6c2c7cc173409f6cd25dedf19c44baf1d42efd74190b546c096a189`  
		Last Modified: Tue, 07 Jan 2025 03:33:03 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bcc157a0695c33742bdaae44173f5f7f430937ae371216bfb70ee625ffc60eb`  
		Last Modified: Tue, 07 Jan 2025 03:33:04 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:3d10d048c07d3b656f05ef64c0220215256c6c2fe4b6cd266b58ee39dd787640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.1 KB (378139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1ef06c20907dd546d4a786d7512f5e4cc36892b93bce3ee1b708804c81b6212`

```dockerfile
```

-	Layers:
	-	`sha256:8b600c398ef76b5f1a3cff321d8a58c0e1b015a650d197f3e4104ba2b1e6e6df`  
		Last Modified: Tue, 07 Jan 2025 03:33:03 GMT  
		Size: 362.5 KB (362455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6b7930a4990a1c8c6579173d0e6b66b60e07a85ad5c72737ec18923d092101a`  
		Last Modified: Tue, 07 Jan 2025 03:33:03 GMT  
		Size: 15.7 KB (15684 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:f6e635fa0941005fe16a4bd14164e009226fbee0579a22372ff390228a8cc630
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:9739f88fde1e2dacbeabfdaa58a5195804b81fcb76dd474b4ea8e46bd7d7641c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.1 MB (148052695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83447930c54621bbc4681d7122a155341835c9e878d8bb8fe49fc14f0fc45a54`
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
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENV KAPACITOR_VERSION=1.7.6
# Mon, 28 Oct 2024 16:40:55 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 28 Oct 2024 16:40:55 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 28 Oct 2024 16:40:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 16:40:55 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 08 Jan 2025 07:56:27 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8284ddf57c03d97884a998219f0fbd84edab303351cdba3ac1526a116e907210`  
		Last Modified: Sat, 19 Oct 2024 02:06:18 GMT  
		Size: 7.1 MB (7102850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df56e827619a8fb6da0a24519f0ce4465e5ea92183062cddea4fcfe92d548dca`  
		Size: 39.4 MB (39366403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0642dd44f5a4b0dc896f854e9689f9e4e2763fd4c0385361ba87348c7872558`  
		Last Modified: Mon, 28 Oct 2024 17:57:28 GMT  
		Size: 72.0 MB (72047234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b583b675d8473487b78bec0b60484b0045b1c41c0da69cd77fff304a82749ef6`  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bfa4793acdf6f4ecd3c2bec17b016dfe800982f15676e56822b6e2d6300c31`  
		Last Modified: Mon, 28 Oct 2024 17:57:27 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:d79d8985adbba054947f41b563714a4a711947d9ee8fbb621d1df061d502d370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9834f59514a211f8ac46503771209c68359602f2ee3ecc9b66d89cf2e570cf51`

```dockerfile
```

-	Layers:
	-	`sha256:15b66889746a6519923422c83cc5851fe9bf2ea0d4399221c7f7d43aad829d7a`  
		Size: 3.6 MB (3558208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a1b59fc636e119fda6a8a8384166ed7b8a7d5d1214839c0d46a6e643a4e0823`  
		Last Modified: Mon, 28 Oct 2024 17:57:27 GMT  
		Size: 15.1 KB (15063 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:455d8810abbdcf76f21629d4032b060a586d6e57ea9f2b9e6f8519a96985cdba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.6 MB (138620010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643fca6b41a8acced90879840bd6e8b12af952a23033f435a4036daadf4b961c`
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
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENV KAPACITOR_VERSION=1.7.6
# Mon, 28 Oct 2024 16:40:55 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
EXPOSE map[9092/tcp:{}]
# Mon, 28 Oct 2024 16:40:55 GMT
VOLUME [/var/lib/kapacitor]
# Mon, 28 Oct 2024 16:40:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 28 Oct 2024 16:40:55 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee2b4e5eab18cf336bf82b89529f3587544f710c5e1a0aa67e5ed1fdec85146`  
		Last Modified: Sat, 19 Oct 2024 05:22:20 GMT  
		Size: 7.0 MB (7049559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56450686787eef42d2d8303b7ad5e724b5f247ffd66c187984bc8427445cb31`  
		Last Modified: Mon, 28 Oct 2024 18:00:32 GMT  
		Size: 36.4 MB (36389576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634c45466d4e6828fe17d0f2b71e63c7d093da3b2453e59d53a29db0009ee8e7`  
		Last Modified: Mon, 28 Oct 2024 18:00:33 GMT  
		Size: 67.8 MB (67822024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34771b86c1d3ad4939ac7fd39a5cc7abd79efb4d9175389fcb6ac5cff0a846d9`  
		Last Modified: Mon, 28 Oct 2024 18:00:31 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9cca3ffb481c2e26b551a92a3bf8d7fc5eaeea50d65f7d122a72f3f802c62b6`  
		Last Modified: Mon, 28 Oct 2024 18:00:31 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:24a674e39c6a9c2343c48c66b3e52b739c00bce9e1b02d981428fa7d4f0935c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3572861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8c7e97dca8e7a967b45f3afde9a859b5d68a78bd41613f51796b9c10aeb8a7`

```dockerfile
```

-	Layers:
	-	`sha256:4a47d5d67c314f2ea559bcf73354a2ab0760f4c6db95e70f1e1b6cf367331917`  
		Last Modified: Mon, 28 Oct 2024 18:00:31 GMT  
		Size: 3.6 MB (3557691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f42249fe2142067a94fd37435e4f4edb50e1ba587e013cdff7fc84f6224b77f9`  
		Last Modified: Mon, 28 Oct 2024 18:00:31 GMT  
		Size: 15.2 KB (15170 bytes)  
		MIME: application/vnd.in-toto+json
