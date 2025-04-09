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
$ docker pull kapacitor@sha256:5936fe5cf0fe1729c9ced012f162c5b738f17c58360122903873ed832f84c356
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:8616a3a9fdcc2d6f4090cd3a94da009efab963bb83bb0a75cdfbb0f999327d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144584700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaea0dfca0b24abbeeb8ff36350596506762053e961a485525efde7bbe4195ad`
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
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENV KAPACITOR_VERSION=1.6.6
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4340d07249a0b63b75c4a83ce1639f4f99213cb0868bed6fe3ee40cc7d6ba08d`  
		Last Modified: Wed, 09 Apr 2025 01:11:28 GMT  
		Size: 7.1 MB (7102787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2ba133f53a45e1179ac4319593620c2d37be20cfa01149556451e217f80714`  
		Last Modified: Wed, 09 Apr 2025 02:13:53 GMT  
		Size: 42.3 MB (42276127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6088fd9224b8f1be59b6917587563250ddb3ac554ff9a00cd37fbab387b9f0`  
		Last Modified: Wed, 09 Apr 2025 02:13:53 GMT  
		Size: 65.7 MB (65672964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a672954e0faf766678a800855d38fed23562aaf111f586b71e4898b5bf0b182e`  
		Last Modified: Wed, 09 Apr 2025 02:13:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788e7ed7c0f4ed23a32b52014906917a7f788839a6613a534e59329bd295d282`  
		Last Modified: Wed, 09 Apr 2025 02:13:52 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:54b0abc143b4dbf349970057ee0738e9194bc1ce16b6255054fccbfa880437fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3563240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e7a0a9ded54f6cde324050062744071753cc3ddcf3fece73cd64a806f9756a`

```dockerfile
```

-	Layers:
	-	`sha256:03298ce1362b62c2bc2d8cce0576fc3043092538f19231ce73e6301fa902552e`  
		Last Modified: Wed, 09 Apr 2025 02:13:52 GMT  
		Size: 3.5 MB (3548481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a337a19865a443462b225275c94d7aaa467b589eaf9982e64ec42bf1649a36a`  
		Last Modified: Wed, 09 Apr 2025 02:13:52 GMT  
		Size: 14.8 KB (14759 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:6f643dfa16ff0560207e542bdaa90aad7c0ce2dbc089e897d4d1ee267805863f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135405377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b841b93a37449d9f80b3a08ba28da20f391755eee26dd22df5e034727766f4`
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
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENV KAPACITOR_VERSION=1.6.6
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
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc402370d6ae517f6c8127317462bd2a2fbadfc4283d28383223f04c7fe7f028`  
		Last Modified: Wed, 09 Apr 2025 06:09:41 GMT  
		Size: 7.0 MB (7048964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84134d11fd4f324b6d348c78c76e0161b0ebedcab69e53e205b1a93583172556`  
		Last Modified: Wed, 09 Apr 2025 15:07:53 GMT  
		Size: 39.3 MB (39331572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a0ca38d080655054093f8f59000abdcd2b39c3a94b0ae59199cda94bce56f7`  
		Last Modified: Wed, 09 Apr 2025 15:07:54 GMT  
		Size: 61.7 MB (61670153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70376743068d36321d36bc65abc29cd2a24287733b4f2d361cc7668350b01856`  
		Last Modified: Wed, 09 Apr 2025 15:07:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679410b01ad3e842ecaaf5d5687724b1762508097b82cdebaa0b306367130ab0`  
		Last Modified: Wed, 09 Apr 2025 15:07:52 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:661b905709fb722118167d939a31bdc1cec86dca9595becf9cf3fb39b8e083ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3563602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05093eccc1b355815238d5a0b274d44ac52b4049bd791233ff0742fa169d6db1`

```dockerfile
```

-	Layers:
	-	`sha256:7ab2561989331aa3e9798ac8ab4f29e9ff7754ece7b84f96011b66f47c173600`  
		Last Modified: Wed, 09 Apr 2025 15:07:52 GMT  
		Size: 3.5 MB (3548748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10e8cffa9d0371335af79f75634afe2eead16a641c0b328b5f4439283100b21e`  
		Last Modified: Wed, 09 Apr 2025 15:07:52 GMT  
		Size: 14.9 KB (14854 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.6-alpine`

```console
$ docker pull kapacitor@sha256:eabd8acf11d549814eaca65a093747b22d7f056e8b8695ba6ba89ecb0eb368c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:acf95a57ee1bd5344bb08d22e94189d38735725f0d445a5e20e321975ac5824e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69502141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6c1556e33f80dbbeb72c104bd18352d9bfcef58d892e69e363d02cdf78f02a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 28 Oct 2024 16:40:55 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b7c4bcd6376f58b15fa52176845abf5128e2c9151d217518b4bc0dbae467c4`  
		Last Modified: Fri, 14 Feb 2025 19:26:30 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11769bb0f663d8458ef7ce2717f85df6f471c6a3e71503f4f42dc8b3a04edbde`  
		Last Modified: Fri, 14 Feb 2025 19:26:30 GMT  
		Size: 294.4 KB (294381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab92cf72361b0dade2ad8c0daee300e7282d512572968ad88ad12a30a66ce40a`  
		Last Modified: Fri, 14 Feb 2025 19:26:31 GMT  
		Size: 65.6 MB (65580130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec75cc769591ab3223bacd6530eb8ec0a52abaa396705ca766e48998fa8ab5e3`  
		Last Modified: Fri, 14 Feb 2025 19:26:30 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce9bbc84973835a4410eb3dbe59f08279662eccd66fa3d75c37d98ee926b949`  
		Last Modified: Fri, 14 Feb 2025 19:26:31 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:96a7504fd082256e9460b4656393509609395679ca29ee244ef0616f5af19565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.4 KB (373441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc92318d6da0674edbeb7f030464518d1c466d4ceb96293a271417108654e6e`

```dockerfile
```

-	Layers:
	-	`sha256:12a7f472e13033d632c5cdb7aab55ab918a7bee2548ea56b8469b34b12a37bf3`  
		Last Modified: Fri, 14 Feb 2025 19:26:30 GMT  
		Size: 358.7 KB (358678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae98ee822f327180c826fe1fbbf733f6098cdc27f8b4684d23c7a6d8bb116831`  
		Last Modified: Fri, 14 Feb 2025 19:26:30 GMT  
		Size: 14.8 KB (14763 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.6.6`

```console
$ docker pull kapacitor@sha256:5936fe5cf0fe1729c9ced012f162c5b738f17c58360122903873ed832f84c356
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.6.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:8616a3a9fdcc2d6f4090cd3a94da009efab963bb83bb0a75cdfbb0f999327d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144584700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaea0dfca0b24abbeeb8ff36350596506762053e961a485525efde7bbe4195ad`
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
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENV KAPACITOR_VERSION=1.6.6
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4340d07249a0b63b75c4a83ce1639f4f99213cb0868bed6fe3ee40cc7d6ba08d`  
		Last Modified: Wed, 09 Apr 2025 01:11:28 GMT  
		Size: 7.1 MB (7102787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2ba133f53a45e1179ac4319593620c2d37be20cfa01149556451e217f80714`  
		Last Modified: Wed, 09 Apr 2025 02:13:53 GMT  
		Size: 42.3 MB (42276127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6088fd9224b8f1be59b6917587563250ddb3ac554ff9a00cd37fbab387b9f0`  
		Last Modified: Wed, 09 Apr 2025 02:13:53 GMT  
		Size: 65.7 MB (65672964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a672954e0faf766678a800855d38fed23562aaf111f586b71e4898b5bf0b182e`  
		Last Modified: Wed, 09 Apr 2025 02:13:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788e7ed7c0f4ed23a32b52014906917a7f788839a6613a534e59329bd295d282`  
		Last Modified: Wed, 09 Apr 2025 02:13:52 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:54b0abc143b4dbf349970057ee0738e9194bc1ce16b6255054fccbfa880437fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3563240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92e7a0a9ded54f6cde324050062744071753cc3ddcf3fece73cd64a806f9756a`

```dockerfile
```

-	Layers:
	-	`sha256:03298ce1362b62c2bc2d8cce0576fc3043092538f19231ce73e6301fa902552e`  
		Last Modified: Wed, 09 Apr 2025 02:13:52 GMT  
		Size: 3.5 MB (3548481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a337a19865a443462b225275c94d7aaa467b589eaf9982e64ec42bf1649a36a`  
		Last Modified: Wed, 09 Apr 2025 02:13:52 GMT  
		Size: 14.8 KB (14759 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.6.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:6f643dfa16ff0560207e542bdaa90aad7c0ce2dbc089e897d4d1ee267805863f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135405377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b841b93a37449d9f80b3a08ba28da20f391755eee26dd22df5e034727766f4`
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
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Mon, 28 Oct 2024 16:40:55 GMT
ENV KAPACITOR_VERSION=1.6.6
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
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc402370d6ae517f6c8127317462bd2a2fbadfc4283d28383223f04c7fe7f028`  
		Last Modified: Wed, 09 Apr 2025 06:09:41 GMT  
		Size: 7.0 MB (7048964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84134d11fd4f324b6d348c78c76e0161b0ebedcab69e53e205b1a93583172556`  
		Last Modified: Wed, 09 Apr 2025 15:07:53 GMT  
		Size: 39.3 MB (39331572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a0ca38d080655054093f8f59000abdcd2b39c3a94b0ae59199cda94bce56f7`  
		Last Modified: Wed, 09 Apr 2025 15:07:54 GMT  
		Size: 61.7 MB (61670153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70376743068d36321d36bc65abc29cd2a24287733b4f2d361cc7668350b01856`  
		Last Modified: Wed, 09 Apr 2025 15:07:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679410b01ad3e842ecaaf5d5687724b1762508097b82cdebaa0b306367130ab0`  
		Last Modified: Wed, 09 Apr 2025 15:07:52 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:661b905709fb722118167d939a31bdc1cec86dca9595becf9cf3fb39b8e083ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3563602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05093eccc1b355815238d5a0b274d44ac52b4049bd791233ff0742fa169d6db1`

```dockerfile
```

-	Layers:
	-	`sha256:7ab2561989331aa3e9798ac8ab4f29e9ff7754ece7b84f96011b66f47c173600`  
		Last Modified: Wed, 09 Apr 2025 15:07:52 GMT  
		Size: 3.5 MB (3548748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10e8cffa9d0371335af79f75634afe2eead16a641c0b328b5f4439283100b21e`  
		Last Modified: Wed, 09 Apr 2025 15:07:52 GMT  
		Size: 14.9 KB (14854 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.6.6-alpine`

```console
$ docker pull kapacitor@sha256:eabd8acf11d549814eaca65a093747b22d7f056e8b8695ba6ba89ecb0eb368c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.6.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:acf95a57ee1bd5344bb08d22e94189d38735725f0d445a5e20e321975ac5824e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69502141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6c1556e33f80dbbeb72c104bd18352d9bfcef58d892e69e363d02cdf78f02a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 28 Oct 2024 16:40:55 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b7c4bcd6376f58b15fa52176845abf5128e2c9151d217518b4bc0dbae467c4`  
		Last Modified: Fri, 14 Feb 2025 19:26:30 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11769bb0f663d8458ef7ce2717f85df6f471c6a3e71503f4f42dc8b3a04edbde`  
		Last Modified: Fri, 14 Feb 2025 19:26:30 GMT  
		Size: 294.4 KB (294381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab92cf72361b0dade2ad8c0daee300e7282d512572968ad88ad12a30a66ce40a`  
		Last Modified: Fri, 14 Feb 2025 19:26:31 GMT  
		Size: 65.6 MB (65580130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec75cc769591ab3223bacd6530eb8ec0a52abaa396705ca766e48998fa8ab5e3`  
		Last Modified: Fri, 14 Feb 2025 19:26:30 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce9bbc84973835a4410eb3dbe59f08279662eccd66fa3d75c37d98ee926b949`  
		Last Modified: Fri, 14 Feb 2025 19:26:31 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6.6-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:96a7504fd082256e9460b4656393509609395679ca29ee244ef0616f5af19565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.4 KB (373441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc92318d6da0674edbeb7f030464518d1c466d4ceb96293a271417108654e6e`

```dockerfile
```

-	Layers:
	-	`sha256:12a7f472e13033d632c5cdb7aab55ab918a7bee2548ea56b8469b34b12a37bf3`  
		Last Modified: Fri, 14 Feb 2025 19:26:30 GMT  
		Size: 358.7 KB (358678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae98ee822f327180c826fe1fbbf733f6098cdc27f8b4684d23c7a6d8bb116831`  
		Last Modified: Fri, 14 Feb 2025 19:26:30 GMT  
		Size: 14.8 KB (14763 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7`

```console
$ docker pull kapacitor@sha256:8a79536f1f1744bcd4b9356a354ae092334fd877cfe6ac540144e98c2271e481
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:29cb6cf1a1ede373aa2944cfeb38dbee5de84782a8cbb5030a66a70e82ddeb7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (150959324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5abc078621dd31ed7a236e9100a473792957f2e09dbb95859b8411f6e964b7d`
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
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4340d07249a0b63b75c4a83ce1639f4f99213cb0868bed6fe3ee40cc7d6ba08d`  
		Last Modified: Wed, 09 Apr 2025 01:11:28 GMT  
		Size: 7.1 MB (7102787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d56c49f0ed363e759e0009e8fdcb80fa1ff7b4818e126aba6a10d3e7ceb9d4`  
		Last Modified: Wed, 09 Apr 2025 02:13:57 GMT  
		Size: 42.3 MB (42276077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c9d6fbae44b2ef8ff86c890545ba7338dbc7906cbd39ad2d5e62e75c47aa40`  
		Last Modified: Wed, 09 Apr 2025 02:13:58 GMT  
		Size: 72.0 MB (72047574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa221b0d06fd82c9fd7b3a732a74ef70ce45ee5b724d421f8acdc02a1064600b`  
		Last Modified: Wed, 09 Apr 2025 02:13:57 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0de94031135c43d6cc32af50a42153e2e10578e8e43c0808d597b8a712d2b97`  
		Last Modified: Wed, 09 Apr 2025 02:13:56 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:0002ff813fbc7f55579745e024af21542811a3738a4ebd72d65ea9107575b74c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3571600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f04d75337d8c93aa0b80f0b6fb5e59a4203ae216774b3b55c409431ce0814b64`

```dockerfile
```

-	Layers:
	-	`sha256:8a656e0d2cd8a29fd6ef37979db54778ade8f162cf831925890cf734b59ffcba`  
		Last Modified: Wed, 09 Apr 2025 02:13:57 GMT  
		Size: 3.6 MB (3556537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca955fb240af169287921809e97f619a527a57561f026fb4a9d5a7600744ebb1`  
		Last Modified: Wed, 09 Apr 2025 02:13:56 GMT  
		Size: 15.1 KB (15063 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:7968802b11027efd75585fd5c67b401dc6b66b6719b103867e469567349ae7e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141557625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b2faf5388ca995467f72490e01e97c771d5befa1216812e60ca4bcba97a03f`
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
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
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
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc402370d6ae517f6c8127317462bd2a2fbadfc4283d28383223f04c7fe7f028`  
		Last Modified: Wed, 09 Apr 2025 06:09:41 GMT  
		Size: 7.0 MB (7048964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84134d11fd4f324b6d348c78c76e0161b0ebedcab69e53e205b1a93583172556`  
		Last Modified: Wed, 09 Apr 2025 15:07:53 GMT  
		Size: 39.3 MB (39331572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7438d6e5d76f4ba6e77463626bd4c17626ef5cbef5c077d14643f9cc4ab68f32`  
		Last Modified: Wed, 09 Apr 2025 15:08:22 GMT  
		Size: 67.8 MB (67822336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405f3c2dc9bdc0052c108f160a8ac18361644e71946657eb2b1f903985185eae`  
		Last Modified: Wed, 09 Apr 2025 15:08:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f62b69160052bf66e94cff1b9fad11a7654eb37b08e7175a5dd8750e696dfcf`  
		Last Modified: Wed, 09 Apr 2025 15:08:20 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:8c04f410d250a21da66a36ec0616d33926b1dea03519b1d40f568578980f0dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3571180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276be6b62852263681cb396ee272a3551513be0871bd17aaba14a267cb12b61b`

```dockerfile
```

-	Layers:
	-	`sha256:859519599cb85ac1966941075c45a9e4494a6efc6061f95fe07ff07b49d9f756`  
		Last Modified: Wed, 09 Apr 2025 15:08:20 GMT  
		Size: 3.6 MB (3556011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4cdf2c52d1fff236dc644c19a405aab2ac8e67fee57f5be90b4d29924398b30`  
		Last Modified: Wed, 09 Apr 2025 15:08:20 GMT  
		Size: 15.2 KB (15169 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7-alpine`

```console
$ docker pull kapacitor@sha256:ab41660e813c337788470adabc9bdc83014a9a838591b5a84e2bea5420dfff0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.7-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:d80de5fb0b681e20ec4639fa4f833fe0b2ba22debc1be07411e80f39c8378592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75905011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bfd8adc999d9645747e81838530954dcc7416818771d3f40743b7298ae567fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 28 Oct 2024 16:40:55 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb66ce059e2c58cd1bca56470e6a25e8e94d630ab09f2c0cc3141d879c460143`  
		Last Modified: Fri, 14 Feb 2025 19:13:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff82a75234ac7a2c67a34f6e7192f115d5e12e206035e59917e47237ca12cae`  
		Last Modified: Fri, 14 Feb 2025 19:13:06 GMT  
		Size: 296.5 KB (296501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f13695363bccb9f665399c139ff913d5a2ed7e4ee6208ef774f829ea457c6c`  
		Last Modified: Fri, 14 Feb 2025 19:13:08 GMT  
		Size: 72.0 MB (71980833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667ef208e5bab47062223cab49f2e19071361ea8eedad28a206903e51d10b243`  
		Last Modified: Fri, 14 Feb 2025 19:13:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f630e2ff04bbb88b3e31e88074207828bdf03061654955964de05e394c36e557`  
		Last Modified: Fri, 14 Feb 2025 19:13:07 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:7739053a142992f3b94e50635d0eb198c83110a26140d4b75852ba1ce0c51c51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.0 KB (384016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590c2694bf70026c8fa8dd67c50dfb9bfa11d0c679791667a23ac1ff5db64258`

```dockerfile
```

-	Layers:
	-	`sha256:584b24fbdeb04a9522b2ac6b8dcd6834cd4ed8406d9f9d3c986d800cc727731d`  
		Last Modified: Fri, 14 Feb 2025 19:13:06 GMT  
		Size: 368.3 KB (368333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b16553670a0a3cb59971f6f10e1686b74c1a3804c0b81eb3d9860df537a4c177`  
		Last Modified: Fri, 14 Feb 2025 19:13:06 GMT  
		Size: 15.7 KB (15683 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7.6`

```console
$ docker pull kapacitor@sha256:8a79536f1f1744bcd4b9356a354ae092334fd877cfe6ac540144e98c2271e481
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:29cb6cf1a1ede373aa2944cfeb38dbee5de84782a8cbb5030a66a70e82ddeb7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (150959324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5abc078621dd31ed7a236e9100a473792957f2e09dbb95859b8411f6e964b7d`
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
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4340d07249a0b63b75c4a83ce1639f4f99213cb0868bed6fe3ee40cc7d6ba08d`  
		Last Modified: Wed, 09 Apr 2025 01:11:28 GMT  
		Size: 7.1 MB (7102787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d56c49f0ed363e759e0009e8fdcb80fa1ff7b4818e126aba6a10d3e7ceb9d4`  
		Last Modified: Wed, 09 Apr 2025 02:13:57 GMT  
		Size: 42.3 MB (42276077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c9d6fbae44b2ef8ff86c890545ba7338dbc7906cbd39ad2d5e62e75c47aa40`  
		Last Modified: Wed, 09 Apr 2025 02:13:58 GMT  
		Size: 72.0 MB (72047574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa221b0d06fd82c9fd7b3a732a74ef70ce45ee5b724d421f8acdc02a1064600b`  
		Last Modified: Wed, 09 Apr 2025 02:13:57 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0de94031135c43d6cc32af50a42153e2e10578e8e43c0808d597b8a712d2b97`  
		Last Modified: Wed, 09 Apr 2025 02:13:56 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:0002ff813fbc7f55579745e024af21542811a3738a4ebd72d65ea9107575b74c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3571600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f04d75337d8c93aa0b80f0b6fb5e59a4203ae216774b3b55c409431ce0814b64`

```dockerfile
```

-	Layers:
	-	`sha256:8a656e0d2cd8a29fd6ef37979db54778ade8f162cf831925890cf734b59ffcba`  
		Last Modified: Wed, 09 Apr 2025 02:13:57 GMT  
		Size: 3.6 MB (3556537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca955fb240af169287921809e97f619a527a57561f026fb4a9d5a7600744ebb1`  
		Last Modified: Wed, 09 Apr 2025 02:13:56 GMT  
		Size: 15.1 KB (15063 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:7968802b11027efd75585fd5c67b401dc6b66b6719b103867e469567349ae7e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141557625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b2faf5388ca995467f72490e01e97c771d5befa1216812e60ca4bcba97a03f`
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
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
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
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc402370d6ae517f6c8127317462bd2a2fbadfc4283d28383223f04c7fe7f028`  
		Last Modified: Wed, 09 Apr 2025 06:09:41 GMT  
		Size: 7.0 MB (7048964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84134d11fd4f324b6d348c78c76e0161b0ebedcab69e53e205b1a93583172556`  
		Last Modified: Wed, 09 Apr 2025 15:07:53 GMT  
		Size: 39.3 MB (39331572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7438d6e5d76f4ba6e77463626bd4c17626ef5cbef5c077d14643f9cc4ab68f32`  
		Last Modified: Wed, 09 Apr 2025 15:08:22 GMT  
		Size: 67.8 MB (67822336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405f3c2dc9bdc0052c108f160a8ac18361644e71946657eb2b1f903985185eae`  
		Last Modified: Wed, 09 Apr 2025 15:08:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f62b69160052bf66e94cff1b9fad11a7654eb37b08e7175a5dd8750e696dfcf`  
		Last Modified: Wed, 09 Apr 2025 15:08:20 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:8c04f410d250a21da66a36ec0616d33926b1dea03519b1d40f568578980f0dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3571180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276be6b62852263681cb396ee272a3551513be0871bd17aaba14a267cb12b61b`

```dockerfile
```

-	Layers:
	-	`sha256:859519599cb85ac1966941075c45a9e4494a6efc6061f95fe07ff07b49d9f756`  
		Last Modified: Wed, 09 Apr 2025 15:08:20 GMT  
		Size: 3.6 MB (3556011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4cdf2c52d1fff236dc644c19a405aab2ac8e67fee57f5be90b4d29924398b30`  
		Last Modified: Wed, 09 Apr 2025 15:08:20 GMT  
		Size: 15.2 KB (15169 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7.6-alpine`

```console
$ docker pull kapacitor@sha256:ab41660e813c337788470adabc9bdc83014a9a838591b5a84e2bea5420dfff0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.7.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:d80de5fb0b681e20ec4639fa4f833fe0b2ba22debc1be07411e80f39c8378592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75905011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bfd8adc999d9645747e81838530954dcc7416818771d3f40743b7298ae567fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 28 Oct 2024 16:40:55 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb66ce059e2c58cd1bca56470e6a25e8e94d630ab09f2c0cc3141d879c460143`  
		Last Modified: Fri, 14 Feb 2025 19:13:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff82a75234ac7a2c67a34f6e7192f115d5e12e206035e59917e47237ca12cae`  
		Last Modified: Fri, 14 Feb 2025 19:13:06 GMT  
		Size: 296.5 KB (296501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f13695363bccb9f665399c139ff913d5a2ed7e4ee6208ef774f829ea457c6c`  
		Last Modified: Fri, 14 Feb 2025 19:13:08 GMT  
		Size: 72.0 MB (71980833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667ef208e5bab47062223cab49f2e19071361ea8eedad28a206903e51d10b243`  
		Last Modified: Fri, 14 Feb 2025 19:13:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f630e2ff04bbb88b3e31e88074207828bdf03061654955964de05e394c36e557`  
		Last Modified: Fri, 14 Feb 2025 19:13:07 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.6-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:7739053a142992f3b94e50635d0eb198c83110a26140d4b75852ba1ce0c51c51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.0 KB (384016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590c2694bf70026c8fa8dd67c50dfb9bfa11d0c679791667a23ac1ff5db64258`

```dockerfile
```

-	Layers:
	-	`sha256:584b24fbdeb04a9522b2ac6b8dcd6834cd4ed8406d9f9d3c986d800cc727731d`  
		Last Modified: Fri, 14 Feb 2025 19:13:06 GMT  
		Size: 368.3 KB (368333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b16553670a0a3cb59971f6f10e1686b74c1a3804c0b81eb3d9860df537a4c177`  
		Last Modified: Fri, 14 Feb 2025 19:13:06 GMT  
		Size: 15.7 KB (15683 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:ab41660e813c337788470adabc9bdc83014a9a838591b5a84e2bea5420dfff0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:d80de5fb0b681e20ec4639fa4f833fe0b2ba22debc1be07411e80f39c8378592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75905011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bfd8adc999d9645747e81838530954dcc7416818771d3f40743b7298ae567fc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 28 Oct 2024 16:40:55 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb66ce059e2c58cd1bca56470e6a25e8e94d630ab09f2c0cc3141d879c460143`  
		Last Modified: Fri, 14 Feb 2025 19:13:06 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff82a75234ac7a2c67a34f6e7192f115d5e12e206035e59917e47237ca12cae`  
		Last Modified: Fri, 14 Feb 2025 19:13:06 GMT  
		Size: 296.5 KB (296501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f13695363bccb9f665399c139ff913d5a2ed7e4ee6208ef774f829ea457c6c`  
		Last Modified: Fri, 14 Feb 2025 19:13:08 GMT  
		Size: 72.0 MB (71980833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667ef208e5bab47062223cab49f2e19071361ea8eedad28a206903e51d10b243`  
		Last Modified: Fri, 14 Feb 2025 19:13:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f630e2ff04bbb88b3e31e88074207828bdf03061654955964de05e394c36e557`  
		Last Modified: Fri, 14 Feb 2025 19:13:07 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:7739053a142992f3b94e50635d0eb198c83110a26140d4b75852ba1ce0c51c51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.0 KB (384016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590c2694bf70026c8fa8dd67c50dfb9bfa11d0c679791667a23ac1ff5db64258`

```dockerfile
```

-	Layers:
	-	`sha256:584b24fbdeb04a9522b2ac6b8dcd6834cd4ed8406d9f9d3c986d800cc727731d`  
		Last Modified: Fri, 14 Feb 2025 19:13:06 GMT  
		Size: 368.3 KB (368333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b16553670a0a3cb59971f6f10e1686b74c1a3804c0b81eb3d9860df537a4c177`  
		Last Modified: Fri, 14 Feb 2025 19:13:06 GMT  
		Size: 15.7 KB (15683 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:8a79536f1f1744bcd4b9356a354ae092334fd877cfe6ac540144e98c2271e481
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:29cb6cf1a1ede373aa2944cfeb38dbee5de84782a8cbb5030a66a70e82ddeb7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (150959324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5abc078621dd31ed7a236e9100a473792957f2e09dbb95859b8411f6e964b7d`
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
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4340d07249a0b63b75c4a83ce1639f4f99213cb0868bed6fe3ee40cc7d6ba08d`  
		Last Modified: Wed, 09 Apr 2025 01:11:28 GMT  
		Size: 7.1 MB (7102787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d56c49f0ed363e759e0009e8fdcb80fa1ff7b4818e126aba6a10d3e7ceb9d4`  
		Last Modified: Wed, 09 Apr 2025 02:13:57 GMT  
		Size: 42.3 MB (42276077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c9d6fbae44b2ef8ff86c890545ba7338dbc7906cbd39ad2d5e62e75c47aa40`  
		Last Modified: Wed, 09 Apr 2025 02:13:58 GMT  
		Size: 72.0 MB (72047574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa221b0d06fd82c9fd7b3a732a74ef70ce45ee5b724d421f8acdc02a1064600b`  
		Last Modified: Wed, 09 Apr 2025 02:13:57 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0de94031135c43d6cc32af50a42153e2e10578e8e43c0808d597b8a712d2b97`  
		Last Modified: Wed, 09 Apr 2025 02:13:56 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:0002ff813fbc7f55579745e024af21542811a3738a4ebd72d65ea9107575b74c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3571600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f04d75337d8c93aa0b80f0b6fb5e59a4203ae216774b3b55c409431ce0814b64`

```dockerfile
```

-	Layers:
	-	`sha256:8a656e0d2cd8a29fd6ef37979db54778ade8f162cf831925890cf734b59ffcba`  
		Last Modified: Wed, 09 Apr 2025 02:13:57 GMT  
		Size: 3.6 MB (3556537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca955fb240af169287921809e97f619a527a57561f026fb4a9d5a7600744ebb1`  
		Last Modified: Wed, 09 Apr 2025 02:13:56 GMT  
		Size: 15.1 KB (15063 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:7968802b11027efd75585fd5c67b401dc6b66b6719b103867e469567349ae7e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141557625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b2faf5388ca995467f72490e01e97c771d5befa1216812e60ca4bcba97a03f`
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
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
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
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc402370d6ae517f6c8127317462bd2a2fbadfc4283d28383223f04c7fe7f028`  
		Last Modified: Wed, 09 Apr 2025 06:09:41 GMT  
		Size: 7.0 MB (7048964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84134d11fd4f324b6d348c78c76e0161b0ebedcab69e53e205b1a93583172556`  
		Last Modified: Wed, 09 Apr 2025 15:07:53 GMT  
		Size: 39.3 MB (39331572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7438d6e5d76f4ba6e77463626bd4c17626ef5cbef5c077d14643f9cc4ab68f32`  
		Last Modified: Wed, 09 Apr 2025 15:08:22 GMT  
		Size: 67.8 MB (67822336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405f3c2dc9bdc0052c108f160a8ac18361644e71946657eb2b1f903985185eae`  
		Last Modified: Wed, 09 Apr 2025 15:08:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f62b69160052bf66e94cff1b9fad11a7654eb37b08e7175a5dd8750e696dfcf`  
		Last Modified: Wed, 09 Apr 2025 15:08:20 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:8c04f410d250a21da66a36ec0616d33926b1dea03519b1d40f568578980f0dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3571180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276be6b62852263681cb396ee272a3551513be0871bd17aaba14a267cb12b61b`

```dockerfile
```

-	Layers:
	-	`sha256:859519599cb85ac1966941075c45a9e4494a6efc6061f95fe07ff07b49d9f756`  
		Last Modified: Wed, 09 Apr 2025 15:08:20 GMT  
		Size: 3.6 MB (3556011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4cdf2c52d1fff236dc644c19a405aab2ac8e67fee57f5be90b4d29924398b30`  
		Last Modified: Wed, 09 Apr 2025 15:08:20 GMT  
		Size: 15.2 KB (15169 bytes)  
		MIME: application/vnd.in-toto+json
