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
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
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
$ docker pull kapacitor@sha256:ebb90b3e164c66eca0d18ca8c0ce1bab206eef6ae7e1d1ec297688cc62453687
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:041da7b3e707fce68ac7c211b637d15f99907fc578b1d8df5ef8b40b878648c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69495651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f479c0ba0d452bf0a02d1711ed3eab3c1e28a6d308b860c39d93fdd056a791c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c6613e2cbcfa59dd247fd8b0a902d266dbad652c2217c1e38ccea88d68bb39`  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23906e0559c74e075b796888c5ddd1672b67895e20310fc5360d06aad170975d`  
		Last Modified: Tue, 12 Nov 2024 02:14:07 GMT  
		Size: 290.9 KB (290895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500f50d897b82d5464df0fc724eed3d5eb4e4ac5f1732c9f155ebb55350e516a`  
		Size: 65.6 MB (65580116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6b592c0a8f08c0ab6d7ea38ea57008e68e6d6dcc21e129c48332e7686c1130`  
		Last Modified: Tue, 12 Nov 2024 02:14:07 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4cec25e3e782fe3abc87e0d12fda70ac6170410b82063f4472cc8f81f5bd794`  
		Last Modified: Tue, 12 Nov 2024 02:14:08 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:64e0c22cbde75a304a2129166db29d262f66e1891d131cc23d17ab6078741dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.3 KB (370318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53c945561579ba098b03229ac7596f56b80fa33094aaecd70e08dd2b78156946`

```dockerfile
```

-	Layers:
	-	`sha256:88bf7dfb94b4a97c3273020ff327f5f596e4c1304da6b2cd6f133e3f1dca0ef0`  
		Size: 355.6 KB (355555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b07d986b435b3bd6590a9a1f01c096c341a6dc5648d0a59f6df0b081d51ae1b3`  
		Last Modified: Tue, 12 Nov 2024 02:14:07 GMT  
		Size: 14.8 KB (14763 bytes)  
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
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
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
$ docker pull kapacitor@sha256:ebb90b3e164c66eca0d18ca8c0ce1bab206eef6ae7e1d1ec297688cc62453687
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.6.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:041da7b3e707fce68ac7c211b637d15f99907fc578b1d8df5ef8b40b878648c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69495651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f479c0ba0d452bf0a02d1711ed3eab3c1e28a6d308b860c39d93fdd056a791c9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c6613e2cbcfa59dd247fd8b0a902d266dbad652c2217c1e38ccea88d68bb39`  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23906e0559c74e075b796888c5ddd1672b67895e20310fc5360d06aad170975d`  
		Last Modified: Tue, 12 Nov 2024 02:14:07 GMT  
		Size: 290.9 KB (290895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500f50d897b82d5464df0fc724eed3d5eb4e4ac5f1732c9f155ebb55350e516a`  
		Size: 65.6 MB (65580116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6b592c0a8f08c0ab6d7ea38ea57008e68e6d6dcc21e129c48332e7686c1130`  
		Last Modified: Tue, 12 Nov 2024 02:14:07 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4cec25e3e782fe3abc87e0d12fda70ac6170410b82063f4472cc8f81f5bd794`  
		Last Modified: Tue, 12 Nov 2024 02:14:08 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6.6-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:64e0c22cbde75a304a2129166db29d262f66e1891d131cc23d17ab6078741dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.3 KB (370318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53c945561579ba098b03229ac7596f56b80fa33094aaecd70e08dd2b78156946`

```dockerfile
```

-	Layers:
	-	`sha256:88bf7dfb94b4a97c3273020ff327f5f596e4c1304da6b2cd6f133e3f1dca0ef0`  
		Size: 355.6 KB (355555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b07d986b435b3bd6590a9a1f01c096c341a6dc5648d0a59f6df0b081d51ae1b3`  
		Last Modified: Tue, 12 Nov 2024 02:14:07 GMT  
		Size: 14.8 KB (14763 bytes)  
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
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8284ddf57c03d97884a998219f0fbd84edab303351cdba3ac1526a116e907210`  
		Last Modified: Sat, 19 Oct 2024 02:06:18 GMT  
		Size: 7.1 MB (7102850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df56e827619a8fb6da0a24519f0ce4465e5ea92183062cddea4fcfe92d548dca`  
		Last Modified: Mon, 28 Oct 2024 17:57:28 GMT  
		Size: 39.4 MB (39366403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0642dd44f5a4b0dc896f854e9689f9e4e2763fd4c0385361ba87348c7872558`  
		Last Modified: Mon, 28 Oct 2024 17:57:28 GMT  
		Size: 72.0 MB (72047234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b583b675d8473487b78bec0b60484b0045b1c41c0da69cd77fff304a82749ef6`  
		Last Modified: Mon, 28 Oct 2024 17:57:27 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bfa4793acdf6f4ecd3c2bec17b016dfe800982f15676e56822b6e2d6300c31`  
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
		Size: 3.6 MB (3557691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f42249fe2142067a94fd37435e4f4edb50e1ba587e013cdff7fc84f6224b77f9`  
		Last Modified: Mon, 28 Oct 2024 18:00:31 GMT  
		Size: 15.2 KB (15170 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7-alpine`

```console
$ docker pull kapacitor@sha256:54f2d2409a6c334ddeadf042d80e7c2348070bc9e99cf2f0a025f8625a57a8cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.7-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:086feffd7511df430538db51953f3b1aa97d993c6f354ddb47b30a28268c72d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75897933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153f69c84916f02f4a6dc6dea4288fbd5e0f117dbb28cc409a6c83d94b148960`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885590f1f7b0d800a74c7fafd930c3af61b5fe15daab2678bce790c7f2f9cd22`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac53a171ae4ce01f5e27baec3ad5f6f037a1881b346195983a643819a07b883`  
		Size: 292.6 KB (292605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888177041de4c96b1f68418e7bc5cd4687108fbcbc610cfc109e1ed4b0bda3c6`  
		Last Modified: Tue, 12 Nov 2024 02:14:05 GMT  
		Size: 72.0 MB (71980643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560f14c58286ce05ab80eb37c85d56c1be46dad43efe846b230ab9485fd49396`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8d341b2a713279282b63733cc3f66bea88f5d3f1a02213be85948833f8061d`  
		Last Modified: Tue, 12 Nov 2024 02:14:05 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:fd6657b7e90030fbb5a9534bffa32859cd913c81d638b9d597a0b4e53d93817c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.8 KB (380796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b0bdcc14d39feff37d8496fd2d25c12af54310733fcb8271d15baa6b2dc768b`

```dockerfile
```

-	Layers:
	-	`sha256:cba342c70ae180705b80a828265e8fa05932dee56ee3dcf1ec209aada94ec9d8`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 365.1 KB (365112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6097a085c6c0682ab3aec996dd441ead4d2d4f3eafed141ab953b589e3b790f2`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
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
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8284ddf57c03d97884a998219f0fbd84edab303351cdba3ac1526a116e907210`  
		Last Modified: Sat, 19 Oct 2024 02:06:18 GMT  
		Size: 7.1 MB (7102850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df56e827619a8fb6da0a24519f0ce4465e5ea92183062cddea4fcfe92d548dca`  
		Last Modified: Mon, 28 Oct 2024 17:57:28 GMT  
		Size: 39.4 MB (39366403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0642dd44f5a4b0dc896f854e9689f9e4e2763fd4c0385361ba87348c7872558`  
		Last Modified: Mon, 28 Oct 2024 17:57:28 GMT  
		Size: 72.0 MB (72047234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b583b675d8473487b78bec0b60484b0045b1c41c0da69cd77fff304a82749ef6`  
		Last Modified: Mon, 28 Oct 2024 17:57:27 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bfa4793acdf6f4ecd3c2bec17b016dfe800982f15676e56822b6e2d6300c31`  
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
		Size: 3.6 MB (3557691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f42249fe2142067a94fd37435e4f4edb50e1ba587e013cdff7fc84f6224b77f9`  
		Last Modified: Mon, 28 Oct 2024 18:00:31 GMT  
		Size: 15.2 KB (15170 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7.6-alpine`

```console
$ docker pull kapacitor@sha256:54f2d2409a6c334ddeadf042d80e7c2348070bc9e99cf2f0a025f8625a57a8cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.7.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:086feffd7511df430538db51953f3b1aa97d993c6f354ddb47b30a28268c72d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75897933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153f69c84916f02f4a6dc6dea4288fbd5e0f117dbb28cc409a6c83d94b148960`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885590f1f7b0d800a74c7fafd930c3af61b5fe15daab2678bce790c7f2f9cd22`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac53a171ae4ce01f5e27baec3ad5f6f037a1881b346195983a643819a07b883`  
		Size: 292.6 KB (292605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888177041de4c96b1f68418e7bc5cd4687108fbcbc610cfc109e1ed4b0bda3c6`  
		Last Modified: Tue, 12 Nov 2024 02:14:05 GMT  
		Size: 72.0 MB (71980643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560f14c58286ce05ab80eb37c85d56c1be46dad43efe846b230ab9485fd49396`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8d341b2a713279282b63733cc3f66bea88f5d3f1a02213be85948833f8061d`  
		Last Modified: Tue, 12 Nov 2024 02:14:05 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.6-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:fd6657b7e90030fbb5a9534bffa32859cd913c81d638b9d597a0b4e53d93817c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.8 KB (380796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b0bdcc14d39feff37d8496fd2d25c12af54310733fcb8271d15baa6b2dc768b`

```dockerfile
```

-	Layers:
	-	`sha256:cba342c70ae180705b80a828265e8fa05932dee56ee3dcf1ec209aada94ec9d8`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 365.1 KB (365112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6097a085c6c0682ab3aec996dd441ead4d2d4f3eafed141ab953b589e3b790f2`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 15.7 KB (15684 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:54f2d2409a6c334ddeadf042d80e7c2348070bc9e99cf2f0a025f8625a57a8cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:086feffd7511df430538db51953f3b1aa97d993c6f354ddb47b30a28268c72d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75897933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153f69c84916f02f4a6dc6dea4288fbd5e0f117dbb28cc409a6c83d94b148960`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885590f1f7b0d800a74c7fafd930c3af61b5fe15daab2678bce790c7f2f9cd22`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac53a171ae4ce01f5e27baec3ad5f6f037a1881b346195983a643819a07b883`  
		Size: 292.6 KB (292605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888177041de4c96b1f68418e7bc5cd4687108fbcbc610cfc109e1ed4b0bda3c6`  
		Last Modified: Tue, 12 Nov 2024 02:14:05 GMT  
		Size: 72.0 MB (71980643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560f14c58286ce05ab80eb37c85d56c1be46dad43efe846b230ab9485fd49396`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8d341b2a713279282b63733cc3f66bea88f5d3f1a02213be85948833f8061d`  
		Last Modified: Tue, 12 Nov 2024 02:14:05 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:fd6657b7e90030fbb5a9534bffa32859cd913c81d638b9d597a0b4e53d93817c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.8 KB (380796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b0bdcc14d39feff37d8496fd2d25c12af54310733fcb8271d15baa6b2dc768b`

```dockerfile
```

-	Layers:
	-	`sha256:cba342c70ae180705b80a828265e8fa05932dee56ee3dcf1ec209aada94ec9d8`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
		Size: 365.1 KB (365112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6097a085c6c0682ab3aec996dd441ead4d2d4f3eafed141ab953b589e3b790f2`  
		Last Modified: Tue, 12 Nov 2024 02:14:04 GMT  
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
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8284ddf57c03d97884a998219f0fbd84edab303351cdba3ac1526a116e907210`  
		Last Modified: Sat, 19 Oct 2024 02:06:18 GMT  
		Size: 7.1 MB (7102850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df56e827619a8fb6da0a24519f0ce4465e5ea92183062cddea4fcfe92d548dca`  
		Last Modified: Mon, 28 Oct 2024 17:57:28 GMT  
		Size: 39.4 MB (39366403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0642dd44f5a4b0dc896f854e9689f9e4e2763fd4c0385361ba87348c7872558`  
		Last Modified: Mon, 28 Oct 2024 17:57:28 GMT  
		Size: 72.0 MB (72047234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b583b675d8473487b78bec0b60484b0045b1c41c0da69cd77fff304a82749ef6`  
		Last Modified: Mon, 28 Oct 2024 17:57:27 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bfa4793acdf6f4ecd3c2bec17b016dfe800982f15676e56822b6e2d6300c31`  
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
		Size: 3.6 MB (3557691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f42249fe2142067a94fd37435e4f4edb50e1ba587e013cdff7fc84f6224b77f9`  
		Last Modified: Mon, 28 Oct 2024 18:00:31 GMT  
		Size: 15.2 KB (15170 bytes)  
		MIME: application/vnd.in-toto+json
