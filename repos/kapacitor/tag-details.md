<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.6`](#kapacitor16)
-	[`kapacitor:1.6-alpine`](#kapacitor16-alpine)
-	[`kapacitor:1.6.6`](#kapacitor166)
-	[`kapacitor:1.6.6-alpine`](#kapacitor166-alpine)
-	[`kapacitor:1.7`](#kapacitor17)
-	[`kapacitor:1.7-alpine`](#kapacitor17-alpine)
-	[`kapacitor:1.7.5`](#kapacitor175)
-	[`kapacitor:1.7.5-alpine`](#kapacitor175-alpine)
-	[`kapacitor:alpine`](#kapacitoralpine)
-	[`kapacitor:latest`](#kapacitorlatest)

## `kapacitor:1.6`

```console
$ docker pull kapacitor@sha256:5ec3a89a27cfb84460951f86f92e77eaf7d41c1526d8af2046baffe38fc069c7
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
$ docker pull kapacitor@sha256:7eaf00cf6b0a9b1de56fb30a9641f55eb4a8b3b44b4dfc3a23a671f36bfc3247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (132988480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02a73156243561d64b5d6b91ab75aadae29e90618400c953627bf2094e57932d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ARG RELEASE
# Tue, 18 Jun 2024 15:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c173a9b22d9f65dbf24e1900a1e0ba416d3ca49774ccbd2b27d4d6a3556ce26`  
		Last Modified: Tue, 17 Sep 2024 01:28:48 GMT  
		Size: 7.0 MB (7033470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27489f5e7eb09e805e9e80a9adf4d5c3ca4bfa7d67ec2def103717d2461003d`  
		Last Modified: Tue, 17 Sep 2024 02:17:22 GMT  
		Size: 35.9 MB (35887629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1138340beb1779ab7c0e663b708eaf3f69a41a9aa5a5534b966dc661738a035a`  
		Last Modified: Tue, 17 Sep 2024 02:17:23 GMT  
		Size: 61.7 MB (61669815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba872265f89032ec8b1ad2f057cc841b7a71a2b53c3962c1ba81acc0630929c`  
		Last Modified: Tue, 17 Sep 2024 02:17:23 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bca5d4e91fcba1df9d6c7ce54f1c27e446c9e7862cf33ce23a4b0b2ebe4c14f`  
		Last Modified: Tue, 17 Sep 2024 02:17:23 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:c9ca3a12900f1664c2cc3ef77bd57d7029b119a9455e8f2f95f723c4a958752c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3542350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47dc8243e3e5a1ac1fe12aa4472fd5b499f3f0ed2ef0e58a636666724d3cf747`

```dockerfile
```

-	Layers:
	-	`sha256:57864d7d503892d0cf70b1453b16dbe6dd6f071eadf25f1177dce8da22f24a47`  
		Last Modified: Tue, 17 Sep 2024 02:17:22 GMT  
		Size: 3.5 MB (3527456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62b2de62027ab9ee4bbfa16c3db31bc59cc88a98b767a51986883b3fcee974ac`  
		Last Modified: Tue, 17 Sep 2024 02:17:21 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.6-alpine`

```console
$ docker pull kapacitor@sha256:12b189c83fb4dab397decb627ef94084aba1bb0ff0829938e38d4722bf5fa7fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:e0423ff48b6442c9468543ec16e4240851e84bdd6134ce6ab1552cf497c9cbf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69495535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f00bb014cc36f227c90f56e097ed7f9de8b8724b73d68c594f88dd946a0638e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.6.6
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c268f670c0a685634b444d29fc97e3690f73ca6fc0331600124f5c2753103280`  
		Last Modified: Fri, 06 Sep 2024 23:21:55 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0af18220bb82572dc04f254e71bdb704c3372a49ea537e8d34863a5ccab8e2c`  
		Last Modified: Fri, 06 Sep 2024 23:21:55 GMT  
		Size: 290.9 KB (290882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd619dd3107ddd326fa373840fbb338bd094926a04b095383105b764c3bf07c`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 65.6 MB (65580114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa5f74b3ac49e3fce6a494b7c0a68ab26210242a79515b2f25f77b9ca84bc37`  
		Last Modified: Fri, 06 Sep 2024 23:21:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be98bcea12b74baadc4a3825910fd115dc87bf6510a79349f98e51b9d46815fe`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:094c344947948fbc136c238c5e7866ad6274b87dd403b2deff7a1da39b5516c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.7 KB (369673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85611d22f7f851e6609fd70425f84c2e27f7e0dc0daa0f4066916f98a65e7374`

```dockerfile
```

-	Layers:
	-	`sha256:636f1e95eb7402813159744e6a574302270a4fab364a1af4a77d82638cc6d546`  
		Last Modified: Fri, 06 Sep 2024 23:21:55 GMT  
		Size: 355.1 KB (355131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:018e702035c9209905acb839464a6b65f50bed07d5b028b5aabee575529c0d1d`  
		Last Modified: Fri, 06 Sep 2024 23:21:55 GMT  
		Size: 14.5 KB (14542 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.6.6`

```console
$ docker pull kapacitor@sha256:5ec3a89a27cfb84460951f86f92e77eaf7d41c1526d8af2046baffe38fc069c7
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
$ docker pull kapacitor@sha256:7eaf00cf6b0a9b1de56fb30a9641f55eb4a8b3b44b4dfc3a23a671f36bfc3247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (132988480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02a73156243561d64b5d6b91ab75aadae29e90618400c953627bf2094e57932d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ARG RELEASE
# Tue, 18 Jun 2024 15:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c173a9b22d9f65dbf24e1900a1e0ba416d3ca49774ccbd2b27d4d6a3556ce26`  
		Last Modified: Tue, 17 Sep 2024 01:28:48 GMT  
		Size: 7.0 MB (7033470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27489f5e7eb09e805e9e80a9adf4d5c3ca4bfa7d67ec2def103717d2461003d`  
		Last Modified: Tue, 17 Sep 2024 02:17:22 GMT  
		Size: 35.9 MB (35887629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1138340beb1779ab7c0e663b708eaf3f69a41a9aa5a5534b966dc661738a035a`  
		Last Modified: Tue, 17 Sep 2024 02:17:23 GMT  
		Size: 61.7 MB (61669815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba872265f89032ec8b1ad2f057cc841b7a71a2b53c3962c1ba81acc0630929c`  
		Last Modified: Tue, 17 Sep 2024 02:17:23 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bca5d4e91fcba1df9d6c7ce54f1c27e446c9e7862cf33ce23a4b0b2ebe4c14f`  
		Last Modified: Tue, 17 Sep 2024 02:17:23 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:c9ca3a12900f1664c2cc3ef77bd57d7029b119a9455e8f2f95f723c4a958752c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3542350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47dc8243e3e5a1ac1fe12aa4472fd5b499f3f0ed2ef0e58a636666724d3cf747`

```dockerfile
```

-	Layers:
	-	`sha256:57864d7d503892d0cf70b1453b16dbe6dd6f071eadf25f1177dce8da22f24a47`  
		Last Modified: Tue, 17 Sep 2024 02:17:22 GMT  
		Size: 3.5 MB (3527456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62b2de62027ab9ee4bbfa16c3db31bc59cc88a98b767a51986883b3fcee974ac`  
		Last Modified: Tue, 17 Sep 2024 02:17:21 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.6.6-alpine`

```console
$ docker pull kapacitor@sha256:12b189c83fb4dab397decb627ef94084aba1bb0ff0829938e38d4722bf5fa7fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.6.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:e0423ff48b6442c9468543ec16e4240851e84bdd6134ce6ab1552cf497c9cbf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69495535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f00bb014cc36f227c90f56e097ed7f9de8b8724b73d68c594f88dd946a0638e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.6.6
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c268f670c0a685634b444d29fc97e3690f73ca6fc0331600124f5c2753103280`  
		Last Modified: Fri, 06 Sep 2024 23:21:55 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0af18220bb82572dc04f254e71bdb704c3372a49ea537e8d34863a5ccab8e2c`  
		Last Modified: Fri, 06 Sep 2024 23:21:55 GMT  
		Size: 290.9 KB (290882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd619dd3107ddd326fa373840fbb338bd094926a04b095383105b764c3bf07c`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 65.6 MB (65580114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa5f74b3ac49e3fce6a494b7c0a68ab26210242a79515b2f25f77b9ca84bc37`  
		Last Modified: Fri, 06 Sep 2024 23:21:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be98bcea12b74baadc4a3825910fd115dc87bf6510a79349f98e51b9d46815fe`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6.6-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:094c344947948fbc136c238c5e7866ad6274b87dd403b2deff7a1da39b5516c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.7 KB (369673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85611d22f7f851e6609fd70425f84c2e27f7e0dc0daa0f4066916f98a65e7374`

```dockerfile
```

-	Layers:
	-	`sha256:636f1e95eb7402813159744e6a574302270a4fab364a1af4a77d82638cc6d546`  
		Last Modified: Fri, 06 Sep 2024 23:21:55 GMT  
		Size: 355.1 KB (355131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:018e702035c9209905acb839464a6b65f50bed07d5b028b5aabee575529c0d1d`  
		Last Modified: Fri, 06 Sep 2024 23:21:55 GMT  
		Size: 14.5 KB (14542 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7`

```console
$ docker pull kapacitor@sha256:5c85dc4887476cbfeeb893e053d3aeec2323d50cba1f100a5633a31c470c2999
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:4f425108ab59080a16468e86daa1b577fdcd97277e24a510788e59439a380018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147369771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02494a19ec2a00724831e1c571bcb8327f3c09911a0bc779f50b09e5aff329ad`
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
ENV KAPACITOR_VERSION=1.7.5
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
	-	`sha256:4f251e17dca5f10cbea526a8e0b763ec5968e38f323b69ef4c64ebb49a1e96ae`  
		Last Modified: Sat, 19 Oct 2024 02:54:09 GMT  
		Size: 39.3 MB (39341346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c30c9009a395568837469b0f46cdac41ba056442eb61d9846dd78c936dcc4cc`  
		Last Modified: Sat, 19 Oct 2024 02:54:10 GMT  
		Size: 71.4 MB (71389364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788028ae066ebb118c4f03ebeabbcab1f9cccb83681b5e5a86ec0038b7fdda16`  
		Last Modified: Sat, 19 Oct 2024 02:54:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fa12f222631b1824afc7dd28bf4bfc5709e8c523f82a0b96b0fb0e1ae9a3b3`  
		Last Modified: Sat, 19 Oct 2024 02:54:08 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:377eb5fae3107d54641ab69dccd953cad9f498f62f2c219bc46f6d1df8b2e801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4974f5c58206d730c0803834995ffc1d857f32693490fbfa03f1b85af25364d3`

```dockerfile
```

-	Layers:
	-	`sha256:19d92c297a175f2c09abbccbb3199571a80288f6b83ceded0f1aa18945ba3d2a`  
		Last Modified: Sat, 19 Oct 2024 02:54:08 GMT  
		Size: 3.6 MB (3558218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78b8f0c5773a9ed7dbcf1dcad479895c25c71eb6a7c51b28d146e358b66353e0`  
		Last Modified: Sat, 19 Oct 2024 02:54:08 GMT  
		Size: 15.1 KB (15063 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:b7828c88f6edcc31fd04df5a426378bcfcc618ca83e2ab3e98aab9ca1165a340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138433752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e857f1cd065e2f998ca40ac70d18225c4b18b7de94e4adec365b1e0a3bfc60fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ARG RELEASE
# Tue, 18 Jun 2024 15:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Jun 2024 15:52:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.7.5
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
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c173a9b22d9f65dbf24e1900a1e0ba416d3ca49774ccbd2b27d4d6a3556ce26`  
		Last Modified: Tue, 17 Sep 2024 01:28:48 GMT  
		Size: 7.0 MB (7033470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27489f5e7eb09e805e9e80a9adf4d5c3ca4bfa7d67ec2def103717d2461003d`  
		Last Modified: Tue, 17 Sep 2024 02:17:22 GMT  
		Size: 35.9 MB (35887629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5045434a1919d32f800bc8a7650344ea82339545ef2d2351fe4d1252dadb378`  
		Last Modified: Tue, 17 Sep 2024 02:18:02 GMT  
		Size: 67.1 MB (67115024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:399a7209d13f605a26d2cad117215a875dd1c3698f2738325063bde43629509a`  
		Last Modified: Tue, 17 Sep 2024 02:18:00 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ddad4b311468f4ba154e92d0d1a00398522ac935ac1448de4de703008963ec`  
		Last Modified: Tue, 17 Sep 2024 02:18:00 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:d9d048d24158bc7176c01aa80c07e4b346ef0522c7f32c645e7fb428a666e92a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3549849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4b62ef949cd299a9c3bbc62d719d0a6444bc226e097a2002fccda608c72f70b`

```dockerfile
```

-	Layers:
	-	`sha256:0b8cb9f18efeb50f218ddc7f09c7e0be40d757cf4745620d0212ef2b2b116522`  
		Last Modified: Tue, 17 Sep 2024 02:18:00 GMT  
		Size: 3.5 MB (3534639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1e5251618e04f77a8c7618564b33975109744a65112a3f2e2ef862b4e86c3ee`  
		Last Modified: Tue, 17 Sep 2024 02:18:00 GMT  
		Size: 15.2 KB (15210 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7-alpine`

```console
$ docker pull kapacitor@sha256:f7e1b5a11518134085443d57633ca0003d6209160799cc76b632673e2715ced9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.7-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:a7eb292d00e949e753cf601f1aa459c6e3b90fa71a5333e613c3e32220e97ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75236586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e79a2267ecefc2a687bcb1b688a856d4f07e86a4c6bb99eb2738093c222354`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.7.5
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230d75275092d3e053c8f298afa3cf2cd9bd213f547c234cf89c85e1ddc7206e`  
		Last Modified: Fri, 06 Sep 2024 23:22:10 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0460a680b1925da179fafe048f8fe0d62be248fb243a328cee52a157fee0752a`  
		Last Modified: Fri, 06 Sep 2024 23:22:10 GMT  
		Size: 292.6 KB (292599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb917e1ee259d651521e9ea0d8f4bc3f8fad8e54367adbd0459abe6f150e70dc`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 71.3 MB (71319398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1316a611ed7cbd7df20a7d953ded552204d4a5bebfb8380da29c2e9b5c076cdb`  
		Last Modified: Fri, 06 Sep 2024 23:22:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ee63ec1d6ab9869e89b97caf3c2ea9dab9a77bad93b44530ace58cfb09c04d`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:26fb73f1b0e9f1853dc0633946f0679e282f0d0d39bcb21c9089aa895116fcdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.2 KB (380161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e31f8772d2655d00ed42681be3b7356b9c8367558aa71f0ad50339c4cc1c6c`

```dockerfile
```

-	Layers:
	-	`sha256:a0ea976bb0730523b5df0d6b08a1a70872e5b881add3c3d2abce8ac6e9f67548`  
		Last Modified: Fri, 06 Sep 2024 23:22:10 GMT  
		Size: 364.7 KB (364698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31112cd797ae22f53dc744d61673a35a886a7f27f6a5dbd454f29e8f19aa5454`  
		Last Modified: Fri, 06 Sep 2024 23:22:10 GMT  
		Size: 15.5 KB (15463 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7.5`

```console
$ docker pull kapacitor@sha256:5c85dc4887476cbfeeb893e053d3aeec2323d50cba1f100a5633a31c470c2999
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7.5` - linux; amd64

```console
$ docker pull kapacitor@sha256:4f425108ab59080a16468e86daa1b577fdcd97277e24a510788e59439a380018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147369771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02494a19ec2a00724831e1c571bcb8327f3c09911a0bc779f50b09e5aff329ad`
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
ENV KAPACITOR_VERSION=1.7.5
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
	-	`sha256:4f251e17dca5f10cbea526a8e0b763ec5968e38f323b69ef4c64ebb49a1e96ae`  
		Last Modified: Sat, 19 Oct 2024 02:54:09 GMT  
		Size: 39.3 MB (39341346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c30c9009a395568837469b0f46cdac41ba056442eb61d9846dd78c936dcc4cc`  
		Last Modified: Sat, 19 Oct 2024 02:54:10 GMT  
		Size: 71.4 MB (71389364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788028ae066ebb118c4f03ebeabbcab1f9cccb83681b5e5a86ec0038b7fdda16`  
		Last Modified: Sat, 19 Oct 2024 02:54:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fa12f222631b1824afc7dd28bf4bfc5709e8c523f82a0b96b0fb0e1ae9a3b3`  
		Last Modified: Sat, 19 Oct 2024 02:54:08 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.5` - unknown; unknown

```console
$ docker pull kapacitor@sha256:377eb5fae3107d54641ab69dccd953cad9f498f62f2c219bc46f6d1df8b2e801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4974f5c58206d730c0803834995ffc1d857f32693490fbfa03f1b85af25364d3`

```dockerfile
```

-	Layers:
	-	`sha256:19d92c297a175f2c09abbccbb3199571a80288f6b83ceded0f1aa18945ba3d2a`  
		Last Modified: Sat, 19 Oct 2024 02:54:08 GMT  
		Size: 3.6 MB (3558218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78b8f0c5773a9ed7dbcf1dcad479895c25c71eb6a7c51b28d146e358b66353e0`  
		Last Modified: Sat, 19 Oct 2024 02:54:08 GMT  
		Size: 15.1 KB (15063 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7.5` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:b7828c88f6edcc31fd04df5a426378bcfcc618ca83e2ab3e98aab9ca1165a340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138433752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e857f1cd065e2f998ca40ac70d18225c4b18b7de94e4adec365b1e0a3bfc60fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ARG RELEASE
# Tue, 18 Jun 2024 15:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Jun 2024 15:52:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.7.5
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
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c173a9b22d9f65dbf24e1900a1e0ba416d3ca49774ccbd2b27d4d6a3556ce26`  
		Last Modified: Tue, 17 Sep 2024 01:28:48 GMT  
		Size: 7.0 MB (7033470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27489f5e7eb09e805e9e80a9adf4d5c3ca4bfa7d67ec2def103717d2461003d`  
		Last Modified: Tue, 17 Sep 2024 02:17:22 GMT  
		Size: 35.9 MB (35887629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5045434a1919d32f800bc8a7650344ea82339545ef2d2351fe4d1252dadb378`  
		Last Modified: Tue, 17 Sep 2024 02:18:02 GMT  
		Size: 67.1 MB (67115024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:399a7209d13f605a26d2cad117215a875dd1c3698f2738325063bde43629509a`  
		Last Modified: Tue, 17 Sep 2024 02:18:00 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ddad4b311468f4ba154e92d0d1a00398522ac935ac1448de4de703008963ec`  
		Last Modified: Tue, 17 Sep 2024 02:18:00 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.5` - unknown; unknown

```console
$ docker pull kapacitor@sha256:d9d048d24158bc7176c01aa80c07e4b346ef0522c7f32c645e7fb428a666e92a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3549849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4b62ef949cd299a9c3bbc62d719d0a6444bc226e097a2002fccda608c72f70b`

```dockerfile
```

-	Layers:
	-	`sha256:0b8cb9f18efeb50f218ddc7f09c7e0be40d757cf4745620d0212ef2b2b116522`  
		Last Modified: Tue, 17 Sep 2024 02:18:00 GMT  
		Size: 3.5 MB (3534639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1e5251618e04f77a8c7618564b33975109744a65112a3f2e2ef862b4e86c3ee`  
		Last Modified: Tue, 17 Sep 2024 02:18:00 GMT  
		Size: 15.2 KB (15210 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7.5-alpine`

```console
$ docker pull kapacitor@sha256:f7e1b5a11518134085443d57633ca0003d6209160799cc76b632673e2715ced9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.7.5-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:a7eb292d00e949e753cf601f1aa459c6e3b90fa71a5333e613c3e32220e97ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75236586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e79a2267ecefc2a687bcb1b688a856d4f07e86a4c6bb99eb2738093c222354`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.7.5
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230d75275092d3e053c8f298afa3cf2cd9bd213f547c234cf89c85e1ddc7206e`  
		Last Modified: Fri, 06 Sep 2024 23:22:10 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0460a680b1925da179fafe048f8fe0d62be248fb243a328cee52a157fee0752a`  
		Last Modified: Fri, 06 Sep 2024 23:22:10 GMT  
		Size: 292.6 KB (292599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb917e1ee259d651521e9ea0d8f4bc3f8fad8e54367adbd0459abe6f150e70dc`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 71.3 MB (71319398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1316a611ed7cbd7df20a7d953ded552204d4a5bebfb8380da29c2e9b5c076cdb`  
		Last Modified: Fri, 06 Sep 2024 23:22:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ee63ec1d6ab9869e89b97caf3c2ea9dab9a77bad93b44530ace58cfb09c04d`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.5-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:26fb73f1b0e9f1853dc0633946f0679e282f0d0d39bcb21c9089aa895116fcdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.2 KB (380161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e31f8772d2655d00ed42681be3b7356b9c8367558aa71f0ad50339c4cc1c6c`

```dockerfile
```

-	Layers:
	-	`sha256:a0ea976bb0730523b5df0d6b08a1a70872e5b881add3c3d2abce8ac6e9f67548`  
		Last Modified: Fri, 06 Sep 2024 23:22:10 GMT  
		Size: 364.7 KB (364698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31112cd797ae22f53dc744d61673a35a886a7f27f6a5dbd454f29e8f19aa5454`  
		Last Modified: Fri, 06 Sep 2024 23:22:10 GMT  
		Size: 15.5 KB (15463 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:f7e1b5a11518134085443d57633ca0003d6209160799cc76b632673e2715ced9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:a7eb292d00e949e753cf601f1aa459c6e3b90fa71a5333e613c3e32220e97ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75236586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e79a2267ecefc2a687bcb1b688a856d4f07e86a4c6bb99eb2738093c222354`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.7.5
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
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
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230d75275092d3e053c8f298afa3cf2cd9bd213f547c234cf89c85e1ddc7206e`  
		Last Modified: Fri, 06 Sep 2024 23:22:10 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0460a680b1925da179fafe048f8fe0d62be248fb243a328cee52a157fee0752a`  
		Last Modified: Fri, 06 Sep 2024 23:22:10 GMT  
		Size: 292.6 KB (292599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb917e1ee259d651521e9ea0d8f4bc3f8fad8e54367adbd0459abe6f150e70dc`  
		Last Modified: Fri, 06 Sep 2024 23:22:12 GMT  
		Size: 71.3 MB (71319398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1316a611ed7cbd7df20a7d953ded552204d4a5bebfb8380da29c2e9b5c076cdb`  
		Last Modified: Fri, 06 Sep 2024 23:22:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ee63ec1d6ab9869e89b97caf3c2ea9dab9a77bad93b44530ace58cfb09c04d`  
		Last Modified: Fri, 06 Sep 2024 23:22:11 GMT  
		Size: 278.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:26fb73f1b0e9f1853dc0633946f0679e282f0d0d39bcb21c9089aa895116fcdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.2 KB (380161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e31f8772d2655d00ed42681be3b7356b9c8367558aa71f0ad50339c4cc1c6c`

```dockerfile
```

-	Layers:
	-	`sha256:a0ea976bb0730523b5df0d6b08a1a70872e5b881add3c3d2abce8ac6e9f67548`  
		Last Modified: Fri, 06 Sep 2024 23:22:10 GMT  
		Size: 364.7 KB (364698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31112cd797ae22f53dc744d61673a35a886a7f27f6a5dbd454f29e8f19aa5454`  
		Last Modified: Fri, 06 Sep 2024 23:22:10 GMT  
		Size: 15.5 KB (15463 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:5c85dc4887476cbfeeb893e053d3aeec2323d50cba1f100a5633a31c470c2999
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:4f425108ab59080a16468e86daa1b577fdcd97277e24a510788e59439a380018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147369771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02494a19ec2a00724831e1c571bcb8327f3c09911a0bc779f50b09e5aff329ad`
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
ENV KAPACITOR_VERSION=1.7.5
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
	-	`sha256:4f251e17dca5f10cbea526a8e0b763ec5968e38f323b69ef4c64ebb49a1e96ae`  
		Last Modified: Sat, 19 Oct 2024 02:54:09 GMT  
		Size: 39.3 MB (39341346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c30c9009a395568837469b0f46cdac41ba056442eb61d9846dd78c936dcc4cc`  
		Last Modified: Sat, 19 Oct 2024 02:54:10 GMT  
		Size: 71.4 MB (71389364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788028ae066ebb118c4f03ebeabbcab1f9cccb83681b5e5a86ec0038b7fdda16`  
		Last Modified: Sat, 19 Oct 2024 02:54:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fa12f222631b1824afc7dd28bf4bfc5709e8c523f82a0b96b0fb0e1ae9a3b3`  
		Last Modified: Sat, 19 Oct 2024 02:54:08 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:377eb5fae3107d54641ab69dccd953cad9f498f62f2c219bc46f6d1df8b2e801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4974f5c58206d730c0803834995ffc1d857f32693490fbfa03f1b85af25364d3`

```dockerfile
```

-	Layers:
	-	`sha256:19d92c297a175f2c09abbccbb3199571a80288f6b83ceded0f1aa18945ba3d2a`  
		Last Modified: Sat, 19 Oct 2024 02:54:08 GMT  
		Size: 3.6 MB (3558218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78b8f0c5773a9ed7dbcf1dcad479895c25c71eb6a7c51b28d146e358b66353e0`  
		Last Modified: Sat, 19 Oct 2024 02:54:08 GMT  
		Size: 15.1 KB (15063 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:b7828c88f6edcc31fd04df5a426378bcfcc618ca83e2ab3e98aab9ca1165a340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138433752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e857f1cd065e2f998ca40ac70d18225c4b18b7de94e4adec365b1e0a3bfc60fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ARG RELEASE
# Tue, 18 Jun 2024 15:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Jun 2024 15:52:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.7.5
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
	-	`sha256:4be1db8bbbebdd00e047c599d9aa2ee2ac533600bee2ac25a86573e42598d326`  
		Last Modified: Thu, 12 Sep 2024 07:29:35 GMT  
		Size: 28.4 MB (28397107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c173a9b22d9f65dbf24e1900a1e0ba416d3ca49774ccbd2b27d4d6a3556ce26`  
		Last Modified: Tue, 17 Sep 2024 01:28:48 GMT  
		Size: 7.0 MB (7033470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27489f5e7eb09e805e9e80a9adf4d5c3ca4bfa7d67ec2def103717d2461003d`  
		Last Modified: Tue, 17 Sep 2024 02:17:22 GMT  
		Size: 35.9 MB (35887629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5045434a1919d32f800bc8a7650344ea82339545ef2d2351fe4d1252dadb378`  
		Last Modified: Tue, 17 Sep 2024 02:18:02 GMT  
		Size: 67.1 MB (67115024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:399a7209d13f605a26d2cad117215a875dd1c3698f2738325063bde43629509a`  
		Last Modified: Tue, 17 Sep 2024 02:18:00 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ddad4b311468f4ba154e92d0d1a00398522ac935ac1448de4de703008963ec`  
		Last Modified: Tue, 17 Sep 2024 02:18:00 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:d9d048d24158bc7176c01aa80c07e4b346ef0522c7f32c645e7fb428a666e92a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3549849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4b62ef949cd299a9c3bbc62d719d0a6444bc226e097a2002fccda608c72f70b`

```dockerfile
```

-	Layers:
	-	`sha256:0b8cb9f18efeb50f218ddc7f09c7e0be40d757cf4745620d0212ef2b2b116522`  
		Last Modified: Tue, 17 Sep 2024 02:18:00 GMT  
		Size: 3.5 MB (3534639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1e5251618e04f77a8c7618564b33975109744a65112a3f2e2ef862b4e86c3ee`  
		Last Modified: Tue, 17 Sep 2024 02:18:00 GMT  
		Size: 15.2 KB (15210 bytes)  
		MIME: application/vnd.in-toto+json
