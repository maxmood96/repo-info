<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.7`](#kapacitor17)
-	[`kapacitor:1.7-alpine`](#kapacitor17-alpine)
-	[`kapacitor:1.7.7`](#kapacitor177)
-	[`kapacitor:1.7.7-alpine`](#kapacitor177-alpine)
-	[`kapacitor:1.8`](#kapacitor18)
-	[`kapacitor:1.8-alpine`](#kapacitor18-alpine)
-	[`kapacitor:1.8.3`](#kapacitor183)
-	[`kapacitor:1.8.3-alpine`](#kapacitor183-alpine)
-	[`kapacitor:alpine`](#kapacitoralpine)
-	[`kapacitor:latest`](#kapacitorlatest)

## `kapacitor:1.7`

```console
$ docker pull kapacitor@sha256:40fb6162dcd29be456c41149b2685591720072dc0f1f1bf81254d2de36979696
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:5c46901d367ae7143fe3455db10140bfb8d085f235c14e23cae21b19b0de9a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.6 MB (158570881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c79115c2e418a18386f366af5d0f51c40b7a4afea7fde1ef5e403a500d0480f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:23:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 17 Feb 2026 21:23:39 GMT
ENV KAPACITOR_VERSION=1.7.7
# Tue, 17 Feb 2026 21:23:39 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 17 Feb 2026 21:23:39 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 17 Feb 2026 21:23:39 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 17 Feb 2026 21:23:39 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 17 Feb 2026 21:23:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 21:23:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 21:23:39 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541b91de6cf313637ee71aa147f2531502925472ffdf0e07e45b3dc2475d2a7b`  
		Last Modified: Tue, 17 Feb 2026 20:12:07 GMT  
		Size: 7.1 MB (7104256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3eca2ccf4130b93a1ece9256225bf1d6bd647ed453483996f716d30d580760`  
		Last Modified: Tue, 17 Feb 2026 21:23:54 GMT  
		Size: 49.9 MB (49877634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc2fff4af1c2640f9f32549e73908dfc9196c60211789c8aadbf4f99f4c96a8`  
		Last Modified: Tue, 17 Feb 2026 21:23:54 GMT  
		Size: 72.1 MB (72051102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b013081e5b5b9a6de4734a2c05ec7312681534ee5e54ca9213f8b1e68a97c24`  
		Last Modified: Tue, 17 Feb 2026 21:23:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8570cabab83eca284dd9a980e0d2485b4ff7970dec9a4c4e7e804ec394809468`  
		Last Modified: Tue, 17 Feb 2026 21:23:52 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:6557e8ff03ce6cf733d7852d5029ae33d9ad3cb84218264d2d3655a20343569c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04e4ec20902c72d6706baa763598785a0624c0e42547fd0802669da53476f7c`

```dockerfile
```

-	Layers:
	-	`sha256:58a4bf99cbd2e3c9a8d573df54ce7252001f9052589db43ed769c4919aa31a5e`  
		Last Modified: Tue, 17 Feb 2026 21:23:52 GMT  
		Size: 3.7 MB (3716676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82e843f8fd90e5a76b52bd9c2977b72a786b89a4d486b2cc64759311b1897c8b`  
		Last Modified: Tue, 17 Feb 2026 21:23:52 GMT  
		Size: 14.7 KB (14716 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:f0a60ecca8e7d832564619e8c6ee372648daaa7275d371e542d547c23d200129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.7 MB (150650979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ff7a3297445c0a112adec6270d0a8611f0cda4c646389db709505c603c7e2f8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:23:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 17 Feb 2026 21:23:47 GMT
ENV KAPACITOR_VERSION=1.7.7
# Tue, 17 Feb 2026 21:23:47 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 17 Feb 2026 21:23:47 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 17 Feb 2026 21:23:47 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 17 Feb 2026 21:23:47 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 17 Feb 2026 21:23:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 21:23:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 21:23:47 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4247dfca464006e30349fde79dc4e5d28c4c26f6afa234c81e4ce3fb42364f5a`  
		Last Modified: Tue, 17 Feb 2026 20:11:24 GMT  
		Size: 7.1 MB (7057616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93570daa6559db9070069d8508e42efed80a4084dcbd580309188d6cc3520c5`  
		Last Modified: Tue, 17 Feb 2026 21:24:03 GMT  
		Size: 48.4 MB (48394156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c918a2959c41f2c986db111207b63dc2b3c028890a80969a4011430083877f4e`  
		Last Modified: Tue, 17 Feb 2026 21:24:04 GMT  
		Size: 67.8 MB (67813740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def15cddc4224495ccf99afa50113c36e92e79b20538e7a8660b38f9112549bc`  
		Last Modified: Tue, 17 Feb 2026 21:24:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869e1cfae8860f1b7824bf7c409c1e03bd439031663f066b94781f11ae4d5cf1`  
		Last Modified: Tue, 17 Feb 2026 21:24:01 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:c3e7592e92680ece540c0d7a0724e7fbab3786f5f968a35e8e80da36207dd401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d8a647c957a4c44f5e46bde355d9d080375d72076bc3fb43c2b5350bb6cbc71`

```dockerfile
```

-	Layers:
	-	`sha256:27bbdc00766ecbcd0d43ec7836e0f2a16b270020e0fc72e044cac10ef30e151f`  
		Last Modified: Tue, 17 Feb 2026 21:24:01 GMT  
		Size: 3.7 MB (3716138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c07bdd3074933ac8a50f8f172d7e418db02457e9e94b080f0960b64115ad5b07`  
		Last Modified: Tue, 17 Feb 2026 21:24:01 GMT  
		Size: 14.8 KB (14810 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7-alpine`

```console
$ docker pull kapacitor@sha256:656c2dd86b1a11c9fa73c985a54bb4cb335be38e3b70e7d7a98b7dd6bb316c20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.7-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:b1d61f6c9d7eedf07f7f421c39d7f4ae7873feda2f507b638c5f41d926c3cf5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75903698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168fcf9b2f142305619b781d38caee32bb205260c8f6b488640d37f280ee3c4b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:27:05 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:27:05 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:27:11 GMT
ENV KAPACITOR_VERSION=1.7.7
# Wed, 28 Jan 2026 03:27:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Wed, 28 Jan 2026 03:27:12 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 28 Jan 2026 03:27:12 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 28 Jan 2026 03:27:12 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 28 Jan 2026 03:27:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:27:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:27:12 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a585510c235336f1b768ba7a6bf719de8862edd4de8bab4478f7143dd713ec`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09eb36c87d43883a2445c1cc908f02d656272af80af315350c48ed43226abf8`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 292.5 KB (292469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d03f75f30654c33dd087a69f5886f260f34677b2a96b36e3eea9c24463859ff`  
		Last Modified: Wed, 28 Jan 2026 03:27:24 GMT  
		Size: 72.0 MB (71982585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e37e8342e3694b5063b4991c1590a9422921ca7d4b546ef869d103f6fa04b9`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d21e4716448dd70a66c3fd55b61f1785b3d5986c261ed93b8ad038da9148135`  
		Last Modified: Wed, 28 Jan 2026 03:27:23 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:5003cd167566bb65defab27200a7d312c071e712e46749d5cdd35d3e1e3ceb13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.2 KB (382162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4f2c0991bc53bb04c83c53a02fd6a5c9242159e43ab17158ffb778aa343c8e`

```dockerfile
```

-	Layers:
	-	`sha256:88336f50a8e4328e09abfae2f573fc9edf649cfa0c6d3a785238d3b1c703b49f`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 366.5 KB (366522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff17a7f1d689f60bc9158243e3980a866fa6d4ce9b91ec9f4688fecbab497f60`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 15.6 KB (15640 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7.7`

```console
$ docker pull kapacitor@sha256:40fb6162dcd29be456c41149b2685591720072dc0f1f1bf81254d2de36979696
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:5c46901d367ae7143fe3455db10140bfb8d085f235c14e23cae21b19b0de9a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.6 MB (158570881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c79115c2e418a18386f366af5d0f51c40b7a4afea7fde1ef5e403a500d0480f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:23:36 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 17 Feb 2026 21:23:39 GMT
ENV KAPACITOR_VERSION=1.7.7
# Tue, 17 Feb 2026 21:23:39 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 17 Feb 2026 21:23:39 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 17 Feb 2026 21:23:39 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 17 Feb 2026 21:23:39 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 17 Feb 2026 21:23:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 21:23:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 21:23:39 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541b91de6cf313637ee71aa147f2531502925472ffdf0e07e45b3dc2475d2a7b`  
		Last Modified: Tue, 17 Feb 2026 20:12:07 GMT  
		Size: 7.1 MB (7104256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3eca2ccf4130b93a1ece9256225bf1d6bd647ed453483996f716d30d580760`  
		Last Modified: Tue, 17 Feb 2026 21:23:54 GMT  
		Size: 49.9 MB (49877634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc2fff4af1c2640f9f32549e73908dfc9196c60211789c8aadbf4f99f4c96a8`  
		Last Modified: Tue, 17 Feb 2026 21:23:54 GMT  
		Size: 72.1 MB (72051102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b013081e5b5b9a6de4734a2c05ec7312681534ee5e54ca9213f8b1e68a97c24`  
		Last Modified: Tue, 17 Feb 2026 21:23:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8570cabab83eca284dd9a980e0d2485b4ff7970dec9a4c4e7e804ec394809468`  
		Last Modified: Tue, 17 Feb 2026 21:23:52 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:6557e8ff03ce6cf733d7852d5029ae33d9ad3cb84218264d2d3655a20343569c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3731392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04e4ec20902c72d6706baa763598785a0624c0e42547fd0802669da53476f7c`

```dockerfile
```

-	Layers:
	-	`sha256:58a4bf99cbd2e3c9a8d573df54ce7252001f9052589db43ed769c4919aa31a5e`  
		Last Modified: Tue, 17 Feb 2026 21:23:52 GMT  
		Size: 3.7 MB (3716676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82e843f8fd90e5a76b52bd9c2977b72a786b89a4d486b2cc64759311b1897c8b`  
		Last Modified: Tue, 17 Feb 2026 21:23:52 GMT  
		Size: 14.7 KB (14716 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:f0a60ecca8e7d832564619e8c6ee372648daaa7275d371e542d547c23d200129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.7 MB (150650979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ff7a3297445c0a112adec6270d0a8611f0cda4c646389db709505c603c7e2f8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:23:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 17 Feb 2026 21:23:47 GMT
ENV KAPACITOR_VERSION=1.7.7
# Tue, 17 Feb 2026 21:23:47 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 17 Feb 2026 21:23:47 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 17 Feb 2026 21:23:47 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 17 Feb 2026 21:23:47 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 17 Feb 2026 21:23:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 21:23:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 21:23:47 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4247dfca464006e30349fde79dc4e5d28c4c26f6afa234c81e4ce3fb42364f5a`  
		Last Modified: Tue, 17 Feb 2026 20:11:24 GMT  
		Size: 7.1 MB (7057616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93570daa6559db9070069d8508e42efed80a4084dcbd580309188d6cc3520c5`  
		Last Modified: Tue, 17 Feb 2026 21:24:03 GMT  
		Size: 48.4 MB (48394156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c918a2959c41f2c986db111207b63dc2b3c028890a80969a4011430083877f4e`  
		Last Modified: Tue, 17 Feb 2026 21:24:04 GMT  
		Size: 67.8 MB (67813740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def15cddc4224495ccf99afa50113c36e92e79b20538e7a8660b38f9112549bc`  
		Last Modified: Tue, 17 Feb 2026 21:24:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869e1cfae8860f1b7824bf7c409c1e03bd439031663f066b94781f11ae4d5cf1`  
		Last Modified: Tue, 17 Feb 2026 21:24:01 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:c3e7592e92680ece540c0d7a0724e7fbab3786f5f968a35e8e80da36207dd401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3730948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d8a647c957a4c44f5e46bde355d9d080375d72076bc3fb43c2b5350bb6cbc71`

```dockerfile
```

-	Layers:
	-	`sha256:27bbdc00766ecbcd0d43ec7836e0f2a16b270020e0fc72e044cac10ef30e151f`  
		Last Modified: Tue, 17 Feb 2026 21:24:01 GMT  
		Size: 3.7 MB (3716138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c07bdd3074933ac8a50f8f172d7e418db02457e9e94b080f0960b64115ad5b07`  
		Last Modified: Tue, 17 Feb 2026 21:24:01 GMT  
		Size: 14.8 KB (14810 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7.7-alpine`

```console
$ docker pull kapacitor@sha256:656c2dd86b1a11c9fa73c985a54bb4cb335be38e3b70e7d7a98b7dd6bb316c20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.7.7-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:b1d61f6c9d7eedf07f7f421c39d7f4ae7873feda2f507b638c5f41d926c3cf5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75903698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168fcf9b2f142305619b781d38caee32bb205260c8f6b488640d37f280ee3c4b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:27:05 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:27:05 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:27:11 GMT
ENV KAPACITOR_VERSION=1.7.7
# Wed, 28 Jan 2026 03:27:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Wed, 28 Jan 2026 03:27:12 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 28 Jan 2026 03:27:12 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 28 Jan 2026 03:27:12 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 28 Jan 2026 03:27:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:27:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:27:12 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a585510c235336f1b768ba7a6bf719de8862edd4de8bab4478f7143dd713ec`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09eb36c87d43883a2445c1cc908f02d656272af80af315350c48ed43226abf8`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 292.5 KB (292469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d03f75f30654c33dd087a69f5886f260f34677b2a96b36e3eea9c24463859ff`  
		Last Modified: Wed, 28 Jan 2026 03:27:24 GMT  
		Size: 72.0 MB (71982585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e37e8342e3694b5063b4991c1590a9422921ca7d4b546ef869d103f6fa04b9`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d21e4716448dd70a66c3fd55b61f1785b3d5986c261ed93b8ad038da9148135`  
		Last Modified: Wed, 28 Jan 2026 03:27:23 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.7-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:5003cd167566bb65defab27200a7d312c071e712e46749d5cdd35d3e1e3ceb13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.2 KB (382162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4f2c0991bc53bb04c83c53a02fd6a5c9242159e43ab17158ffb778aa343c8e`

```dockerfile
```

-	Layers:
	-	`sha256:88336f50a8e4328e09abfae2f573fc9edf649cfa0c6d3a785238d3b1c703b49f`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 366.5 KB (366522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff17a7f1d689f60bc9158243e3980a866fa6d4ce9b91ec9f4688fecbab497f60`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 15.6 KB (15640 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8`

```console
$ docker pull kapacitor@sha256:a618b7837a8fa656d4039e977495f908d66c48f90f319461a9e1a572162f61e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.8` - linux; amd64

```console
$ docker pull kapacitor@sha256:d9cc8f6f0c0322ebf70bcaefd6c42f39b935aaa4cd02c8c8ba6799369b4de0bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172695148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17757a7bf8d501e42b3890fef8dc82f852911deb91db187cb92b62fbe41c23b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Mar 2026 18:15:12 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Wed, 11 Mar 2026 18:15:19 GMT
ENV KAPACITOR_VERSION=1.8.3
# Wed, 11 Mar 2026 18:15:19 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 11 Mar 2026 18:15:19 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 11 Mar 2026 18:15:19 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 11 Mar 2026 18:15:19 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 11 Mar 2026 18:15:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 11 Mar 2026 18:15:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Mar 2026 18:15:19 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541b91de6cf313637ee71aa147f2531502925472ffdf0e07e45b3dc2475d2a7b`  
		Last Modified: Tue, 17 Feb 2026 20:12:07 GMT  
		Size: 7.1 MB (7104256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b85bd15b3ec606cc6214eb1cf42df087af9b0d7e35d394044415a11eb242c6`  
		Last Modified: Wed, 11 Mar 2026 18:15:39 GMT  
		Size: 50.3 MB (50335757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96698c2130ed223cd2480b0b063a7d64572a57ad09b9216fb587efd41e32b9d4`  
		Last Modified: Wed, 11 Mar 2026 18:15:40 GMT  
		Size: 85.7 MB (85717248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a7a5644b2dbe2a382c64ac2aa592f9a6159953b86f2945fe2cbac9b11ea9bc`  
		Last Modified: Wed, 11 Mar 2026 18:15:37 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770213e9d3d8b58603527bea7a2525e932450a53fed61e0d72266fb22940842a`  
		Last Modified: Wed, 11 Mar 2026 18:15:37 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8` - unknown; unknown

```console
$ docker pull kapacitor@sha256:b3df88d06a4bf423029912709b30910996ca5266922c7e828b157c1119eeede1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3747046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59bd96b53ed67166744d3d5b88fb42950bfe1de8a6282b8d169db21d7680a5ee`

```dockerfile
```

-	Layers:
	-	`sha256:14f17cc39c23bf9f9ee83708ebbfe7171af603f4e76e93d716cfe85a7909d717`  
		Last Modified: Wed, 11 Mar 2026 18:15:37 GMT  
		Size: 3.7 MB (3732026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb0314381202be18c39f2547a8188612673ea78894384395a09c04c6ed682f14`  
		Last Modified: Wed, 11 Mar 2026 18:15:37 GMT  
		Size: 15.0 KB (15020 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.8` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:ba2d15e0e0701606ca04a4f328c28fb2a3636498a991e4c9860c9649de5aad3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 MB (163531596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f62a26a6b16ec8e0a4a845e110b594ad1bcf8a9524d7ac74589f01e2901447`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Mar 2026 18:15:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Wed, 11 Mar 2026 18:15:56 GMT
ENV KAPACITOR_VERSION=1.8.3
# Wed, 11 Mar 2026 18:15:56 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 11 Mar 2026 18:15:56 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 11 Mar 2026 18:15:56 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 11 Mar 2026 18:15:56 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 11 Mar 2026 18:15:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 11 Mar 2026 18:15:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Mar 2026 18:15:56 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4247dfca464006e30349fde79dc4e5d28c4c26f6afa234c81e4ce3fb42364f5a`  
		Last Modified: Tue, 17 Feb 2026 20:11:24 GMT  
		Size: 7.1 MB (7057616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ba0c2b4b790d5b53d3775fe8eb58e3942042c4918d57b53c634e6a451d529b`  
		Last Modified: Wed, 11 Mar 2026 18:16:16 GMT  
		Size: 48.9 MB (48944564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c2be56e0e0737c56ebdb64b0ca93699440d79f9f6e01530bf92c8e8f2cb1f7`  
		Last Modified: Wed, 11 Mar 2026 18:16:17 GMT  
		Size: 80.1 MB (80143951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52d8811656ec7a4e82b95582d34a0af9b0c591f2114574676ec8f9bb3c4424c`  
		Last Modified: Wed, 11 Mar 2026 18:16:14 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2c7bc879345937fe54133473126433893c79ab9a4b3a9f4dbc7394313bd4c2`  
		Last Modified: Wed, 11 Mar 2026 18:16:14 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8` - unknown; unknown

```console
$ docker pull kapacitor@sha256:8d86fe778ce93f712a97e64f5bc8da6ce18ebf13bf03a9435d74e7dba6ee0780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9489bf7b5c63a970d711207f6df7cc23517fd18f6b2a16d1b8cb2c6b7ba902ae`

```dockerfile
```

-	Layers:
	-	`sha256:09978dca27a3d6d66eff490a4facfe882b3cc48cb729dda9e821f51ad4ef9ab8`  
		Last Modified: Wed, 11 Mar 2026 18:16:15 GMT  
		Size: 3.7 MB (3731500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c574a0f017064683fc9ab6f2f1df290b8b917562b335968f6bb4ce3d3a0166b6`  
		Last Modified: Wed, 11 Mar 2026 18:16:14 GMT  
		Size: 15.1 KB (15127 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8-alpine`

```console
$ docker pull kapacitor@sha256:df40767f92f21632e43fcdea811a98a7155deba8ccbad1eb34d95276f028de89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.8-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:8032a02add12a7a4d55a9d1286c55621e2a49e67863c3a97f90af2775bdc1878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89768225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af40bddf792c673011b6d23a2414fc750bb23561d91c6ca7a2f3753afe2088dd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 11 Mar 2026 18:15:47 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 11 Mar 2026 18:15:47 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Wed, 11 Mar 2026 18:15:56 GMT
ENV KAPACITOR_VERSION=1.8.3
# Wed, 11 Mar 2026 18:15:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Wed, 11 Mar 2026 18:15:56 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 11 Mar 2026 18:15:56 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 11 Mar 2026 18:15:56 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 11 Mar 2026 18:15:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 11 Mar 2026 18:15:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Mar 2026 18:15:56 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3d23749b45de6d1bff188c596b64bf8cbc4571f640a0742fde8914fd06de31`  
		Last Modified: Wed, 11 Mar 2026 18:16:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318adb4486d9748c72594fac0d372a52e8c23ccc7b9b968b10c91c546aa20706`  
		Last Modified: Wed, 11 Mar 2026 18:16:11 GMT  
		Size: 314.6 KB (314631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ad5e5278bc2c70818690289be2d242b0b4c8c19a0e3760baee03e61a353f1b`  
		Last Modified: Wed, 11 Mar 2026 18:16:13 GMT  
		Size: 85.6 MB (85647918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0cc42bef465492e58bc45a66f45063734b6dfa2c35f122b2e4d727725fb078`  
		Last Modified: Wed, 11 Mar 2026 18:16:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a25094aa2b4871d5b57710ea8c2744cb8f6e6ae0925f30a54d1fdec23b11574`  
		Last Modified: Wed, 11 Mar 2026 18:16:13 GMT  
		Size: 295.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:2078676dd7e1327521aaf5f507135e1dfc297e9cde91d98d759f268ef4a2b7f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.0 KB (407010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bac43789d9959dd74126116e44626a56414434faf48d68ab2b7a1b12a037e04`

```dockerfile
```

-	Layers:
	-	`sha256:746d6873825a09596eb9871f68ce272afc4890afa70e6db536387eea343f78d7`  
		Last Modified: Wed, 11 Mar 2026 18:16:11 GMT  
		Size: 391.7 KB (391673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a6968954b0b936cfb18afe3e011b520c21cdddf0d857adbc50f887bc02fdf0f`  
		Last Modified: Wed, 11 Mar 2026 18:16:11 GMT  
		Size: 15.3 KB (15337 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8.3`

```console
$ docker pull kapacitor@sha256:a618b7837a8fa656d4039e977495f908d66c48f90f319461a9e1a572162f61e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.8.3` - linux; amd64

```console
$ docker pull kapacitor@sha256:d9cc8f6f0c0322ebf70bcaefd6c42f39b935aaa4cd02c8c8ba6799369b4de0bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172695148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17757a7bf8d501e42b3890fef8dc82f852911deb91db187cb92b62fbe41c23b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Mar 2026 18:15:12 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Wed, 11 Mar 2026 18:15:19 GMT
ENV KAPACITOR_VERSION=1.8.3
# Wed, 11 Mar 2026 18:15:19 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 11 Mar 2026 18:15:19 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 11 Mar 2026 18:15:19 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 11 Mar 2026 18:15:19 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 11 Mar 2026 18:15:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 11 Mar 2026 18:15:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Mar 2026 18:15:19 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541b91de6cf313637ee71aa147f2531502925472ffdf0e07e45b3dc2475d2a7b`  
		Last Modified: Tue, 17 Feb 2026 20:12:07 GMT  
		Size: 7.1 MB (7104256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b85bd15b3ec606cc6214eb1cf42df087af9b0d7e35d394044415a11eb242c6`  
		Last Modified: Wed, 11 Mar 2026 18:15:39 GMT  
		Size: 50.3 MB (50335757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96698c2130ed223cd2480b0b063a7d64572a57ad09b9216fb587efd41e32b9d4`  
		Last Modified: Wed, 11 Mar 2026 18:15:40 GMT  
		Size: 85.7 MB (85717248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a7a5644b2dbe2a382c64ac2aa592f9a6159953b86f2945fe2cbac9b11ea9bc`  
		Last Modified: Wed, 11 Mar 2026 18:15:37 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770213e9d3d8b58603527bea7a2525e932450a53fed61e0d72266fb22940842a`  
		Last Modified: Wed, 11 Mar 2026 18:15:37 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8.3` - unknown; unknown

```console
$ docker pull kapacitor@sha256:b3df88d06a4bf423029912709b30910996ca5266922c7e828b157c1119eeede1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3747046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59bd96b53ed67166744d3d5b88fb42950bfe1de8a6282b8d169db21d7680a5ee`

```dockerfile
```

-	Layers:
	-	`sha256:14f17cc39c23bf9f9ee83708ebbfe7171af603f4e76e93d716cfe85a7909d717`  
		Last Modified: Wed, 11 Mar 2026 18:15:37 GMT  
		Size: 3.7 MB (3732026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb0314381202be18c39f2547a8188612673ea78894384395a09c04c6ed682f14`  
		Last Modified: Wed, 11 Mar 2026 18:15:37 GMT  
		Size: 15.0 KB (15020 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.8.3` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:ba2d15e0e0701606ca04a4f328c28fb2a3636498a991e4c9860c9649de5aad3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 MB (163531596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f62a26a6b16ec8e0a4a845e110b594ad1bcf8a9524d7ac74589f01e2901447`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Mar 2026 18:15:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Wed, 11 Mar 2026 18:15:56 GMT
ENV KAPACITOR_VERSION=1.8.3
# Wed, 11 Mar 2026 18:15:56 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 11 Mar 2026 18:15:56 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 11 Mar 2026 18:15:56 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 11 Mar 2026 18:15:56 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 11 Mar 2026 18:15:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 11 Mar 2026 18:15:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Mar 2026 18:15:56 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4247dfca464006e30349fde79dc4e5d28c4c26f6afa234c81e4ce3fb42364f5a`  
		Last Modified: Tue, 17 Feb 2026 20:11:24 GMT  
		Size: 7.1 MB (7057616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ba0c2b4b790d5b53d3775fe8eb58e3942042c4918d57b53c634e6a451d529b`  
		Last Modified: Wed, 11 Mar 2026 18:16:16 GMT  
		Size: 48.9 MB (48944564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c2be56e0e0737c56ebdb64b0ca93699440d79f9f6e01530bf92c8e8f2cb1f7`  
		Last Modified: Wed, 11 Mar 2026 18:16:17 GMT  
		Size: 80.1 MB (80143951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52d8811656ec7a4e82b95582d34a0af9b0c591f2114574676ec8f9bb3c4424c`  
		Last Modified: Wed, 11 Mar 2026 18:16:14 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2c7bc879345937fe54133473126433893c79ab9a4b3a9f4dbc7394313bd4c2`  
		Last Modified: Wed, 11 Mar 2026 18:16:14 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8.3` - unknown; unknown

```console
$ docker pull kapacitor@sha256:8d86fe778ce93f712a97e64f5bc8da6ce18ebf13bf03a9435d74e7dba6ee0780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9489bf7b5c63a970d711207f6df7cc23517fd18f6b2a16d1b8cb2c6b7ba902ae`

```dockerfile
```

-	Layers:
	-	`sha256:09978dca27a3d6d66eff490a4facfe882b3cc48cb729dda9e821f51ad4ef9ab8`  
		Last Modified: Wed, 11 Mar 2026 18:16:15 GMT  
		Size: 3.7 MB (3731500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c574a0f017064683fc9ab6f2f1df290b8b917562b335968f6bb4ce3d3a0166b6`  
		Last Modified: Wed, 11 Mar 2026 18:16:14 GMT  
		Size: 15.1 KB (15127 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8.3-alpine`

```console
$ docker pull kapacitor@sha256:df40767f92f21632e43fcdea811a98a7155deba8ccbad1eb34d95276f028de89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.8.3-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:8032a02add12a7a4d55a9d1286c55621e2a49e67863c3a97f90af2775bdc1878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89768225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af40bddf792c673011b6d23a2414fc750bb23561d91c6ca7a2f3753afe2088dd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 11 Mar 2026 18:15:47 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 11 Mar 2026 18:15:47 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Wed, 11 Mar 2026 18:15:56 GMT
ENV KAPACITOR_VERSION=1.8.3
# Wed, 11 Mar 2026 18:15:56 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Wed, 11 Mar 2026 18:15:56 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 11 Mar 2026 18:15:56 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 11 Mar 2026 18:15:56 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 11 Mar 2026 18:15:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 11 Mar 2026 18:15:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Mar 2026 18:15:56 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3d23749b45de6d1bff188c596b64bf8cbc4571f640a0742fde8914fd06de31`  
		Last Modified: Wed, 11 Mar 2026 18:16:11 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318adb4486d9748c72594fac0d372a52e8c23ccc7b9b968b10c91c546aa20706`  
		Last Modified: Wed, 11 Mar 2026 18:16:11 GMT  
		Size: 314.6 KB (314631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ad5e5278bc2c70818690289be2d242b0b4c8c19a0e3760baee03e61a353f1b`  
		Last Modified: Wed, 11 Mar 2026 18:16:13 GMT  
		Size: 85.6 MB (85647918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc0cc42bef465492e58bc45a66f45063734b6dfa2c35f122b2e4d727725fb078`  
		Last Modified: Wed, 11 Mar 2026 18:16:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a25094aa2b4871d5b57710ea8c2744cb8f6e6ae0925f30a54d1fdec23b11574`  
		Last Modified: Wed, 11 Mar 2026 18:16:13 GMT  
		Size: 295.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8.3-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:2078676dd7e1327521aaf5f507135e1dfc297e9cde91d98d759f268ef4a2b7f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.0 KB (407010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bac43789d9959dd74126116e44626a56414434faf48d68ab2b7a1b12a037e04`

```dockerfile
```

-	Layers:
	-	`sha256:746d6873825a09596eb9871f68ce272afc4890afa70e6db536387eea343f78d7`  
		Last Modified: Wed, 11 Mar 2026 18:16:11 GMT  
		Size: 391.7 KB (391673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a6968954b0b936cfb18afe3e011b520c21cdddf0d857adbc50f887bc02fdf0f`  
		Last Modified: Wed, 11 Mar 2026 18:16:11 GMT  
		Size: 15.3 KB (15337 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:656c2dd86b1a11c9fa73c985a54bb4cb335be38e3b70e7d7a98b7dd6bb316c20
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:b1d61f6c9d7eedf07f7f421c39d7f4ae7873feda2f507b638c5f41d926c3cf5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75903698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168fcf9b2f142305619b781d38caee32bb205260c8f6b488640d37f280ee3c4b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:27:05 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 03:27:05 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:27:11 GMT
ENV KAPACITOR_VERSION=1.7.7
# Wed, 28 Jan 2026 03:27:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Wed, 28 Jan 2026 03:27:12 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 28 Jan 2026 03:27:12 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 28 Jan 2026 03:27:12 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 28 Jan 2026 03:27:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:27:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:27:12 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a585510c235336f1b768ba7a6bf719de8862edd4de8bab4478f7143dd713ec`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09eb36c87d43883a2445c1cc908f02d656272af80af315350c48ed43226abf8`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 292.5 KB (292469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d03f75f30654c33dd087a69f5886f260f34677b2a96b36e3eea9c24463859ff`  
		Last Modified: Wed, 28 Jan 2026 03:27:24 GMT  
		Size: 72.0 MB (71982585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e37e8342e3694b5063b4991c1590a9422921ca7d4b546ef869d103f6fa04b9`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d21e4716448dd70a66c3fd55b61f1785b3d5986c261ed93b8ad038da9148135`  
		Last Modified: Wed, 28 Jan 2026 03:27:23 GMT  
		Size: 274.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:5003cd167566bb65defab27200a7d312c071e712e46749d5cdd35d3e1e3ceb13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.2 KB (382162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b4f2c0991bc53bb04c83c53a02fd6a5c9242159e43ab17158ffb778aa343c8e`

```dockerfile
```

-	Layers:
	-	`sha256:88336f50a8e4328e09abfae2f573fc9edf649cfa0c6d3a785238d3b1c703b49f`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 366.5 KB (366522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff17a7f1d689f60bc9158243e3980a866fa6d4ce9b91ec9f4688fecbab497f60`  
		Last Modified: Wed, 28 Jan 2026 03:27:22 GMT  
		Size: 15.6 KB (15640 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:a618b7837a8fa656d4039e977495f908d66c48f90f319461a9e1a572162f61e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:d9cc8f6f0c0322ebf70bcaefd6c42f39b935aaa4cd02c8c8ba6799369b4de0bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.7 MB (172695148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17757a7bf8d501e42b3890fef8dc82f852911deb91db187cb92b62fbe41c23b5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Mar 2026 18:15:12 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Wed, 11 Mar 2026 18:15:19 GMT
ENV KAPACITOR_VERSION=1.8.3
# Wed, 11 Mar 2026 18:15:19 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 11 Mar 2026 18:15:19 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 11 Mar 2026 18:15:19 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 11 Mar 2026 18:15:19 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 11 Mar 2026 18:15:19 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 11 Mar 2026 18:15:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Mar 2026 18:15:19 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541b91de6cf313637ee71aa147f2531502925472ffdf0e07e45b3dc2475d2a7b`  
		Last Modified: Tue, 17 Feb 2026 20:12:07 GMT  
		Size: 7.1 MB (7104256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b85bd15b3ec606cc6214eb1cf42df087af9b0d7e35d394044415a11eb242c6`  
		Last Modified: Wed, 11 Mar 2026 18:15:39 GMT  
		Size: 50.3 MB (50335757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96698c2130ed223cd2480b0b063a7d64572a57ad09b9216fb587efd41e32b9d4`  
		Last Modified: Wed, 11 Mar 2026 18:15:40 GMT  
		Size: 85.7 MB (85717248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a7a5644b2dbe2a382c64ac2aa592f9a6159953b86f2945fe2cbac9b11ea9bc`  
		Last Modified: Wed, 11 Mar 2026 18:15:37 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770213e9d3d8b58603527bea7a2525e932450a53fed61e0d72266fb22940842a`  
		Last Modified: Wed, 11 Mar 2026 18:15:37 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:b3df88d06a4bf423029912709b30910996ca5266922c7e828b157c1119eeede1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3747046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59bd96b53ed67166744d3d5b88fb42950bfe1de8a6282b8d169db21d7680a5ee`

```dockerfile
```

-	Layers:
	-	`sha256:14f17cc39c23bf9f9ee83708ebbfe7171af603f4e76e93d716cfe85a7909d717`  
		Last Modified: Wed, 11 Mar 2026 18:15:37 GMT  
		Size: 3.7 MB (3732026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb0314381202be18c39f2547a8188612673ea78894384395a09c04c6ed682f14`  
		Last Modified: Wed, 11 Mar 2026 18:15:37 GMT  
		Size: 15.0 KB (15020 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:ba2d15e0e0701606ca04a4f328c28fb2a3636498a991e4c9860c9649de5aad3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 MB (163531596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f62a26a6b16ec8e0a4a845e110b594ad1bcf8a9524d7ac74589f01e2901447`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 11 Mar 2026 18:15:49 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Wed, 11 Mar 2026 18:15:56 GMT
ENV KAPACITOR_VERSION=1.8.3
# Wed, 11 Mar 2026 18:15:56 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Wed, 11 Mar 2026 18:15:56 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 11 Mar 2026 18:15:56 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 11 Mar 2026 18:15:56 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 11 Mar 2026 18:15:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 11 Mar 2026 18:15:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 11 Mar 2026 18:15:56 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4247dfca464006e30349fde79dc4e5d28c4c26f6afa234c81e4ce3fb42364f5a`  
		Last Modified: Tue, 17 Feb 2026 20:11:24 GMT  
		Size: 7.1 MB (7057616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ba0c2b4b790d5b53d3775fe8eb58e3942042c4918d57b53c634e6a451d529b`  
		Last Modified: Wed, 11 Mar 2026 18:16:16 GMT  
		Size: 48.9 MB (48944564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c2be56e0e0737c56ebdb64b0ca93699440d79f9f6e01530bf92c8e8f2cb1f7`  
		Last Modified: Wed, 11 Mar 2026 18:16:17 GMT  
		Size: 80.1 MB (80143951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52d8811656ec7a4e82b95582d34a0af9b0c591f2114574676ec8f9bb3c4424c`  
		Last Modified: Wed, 11 Mar 2026 18:16:14 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2c7bc879345937fe54133473126433893c79ab9a4b3a9f4dbc7394313bd4c2`  
		Last Modified: Wed, 11 Mar 2026 18:16:14 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:8d86fe778ce93f712a97e64f5bc8da6ce18ebf13bf03a9435d74e7dba6ee0780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9489bf7b5c63a970d711207f6df7cc23517fd18f6b2a16d1b8cb2c6b7ba902ae`

```dockerfile
```

-	Layers:
	-	`sha256:09978dca27a3d6d66eff490a4facfe882b3cc48cb729dda9e821f51ad4ef9ab8`  
		Last Modified: Wed, 11 Mar 2026 18:16:15 GMT  
		Size: 3.7 MB (3731500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c574a0f017064683fc9ab6f2f1df290b8b917562b335968f6bb4ce3d3a0166b6`  
		Last Modified: Wed, 11 Mar 2026 18:16:14 GMT  
		Size: 15.1 KB (15127 bytes)  
		MIME: application/vnd.in-toto+json
