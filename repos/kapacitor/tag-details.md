<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.7`](#kapacitor17)
-	[`kapacitor:1.7-alpine`](#kapacitor17-alpine)
-	[`kapacitor:1.7.7`](#kapacitor177)
-	[`kapacitor:1.7.7-alpine`](#kapacitor177-alpine)
-	[`kapacitor:1.8`](#kapacitor18)
-	[`kapacitor:1.8-alpine`](#kapacitor18-alpine)
-	[`kapacitor:1.8.2`](#kapacitor182)
-	[`kapacitor:1.8.2-alpine`](#kapacitor182-alpine)
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
$ docker pull kapacitor@sha256:7c0963201096a09318be3056c148a81359b1bc67cabbc72370a6c5573fda4c98
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.8` - linux; amd64

```console
$ docker pull kapacitor@sha256:64662f96d1a79000d87cc40e3351ddff98e9006c993678bc64433d652aac32c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174717519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ab83ad65a72e9ddbfba143f549a91ba791f114b5b1dc602c335ab0939af7381`
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
# Tue, 17 Feb 2026 21:23:40 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 17 Feb 2026 21:23:46 GMT
ENV KAPACITOR_VERSION=1.8.2
# Tue, 17 Feb 2026 21:23:46 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 17 Feb 2026 21:23:46 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 17 Feb 2026 21:23:46 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 17 Feb 2026 21:23:46 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 17 Feb 2026 21:23:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 21:23:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 21:23:46 GMT
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
	-	`sha256:4ab60e6561c6a7f9c21438b698ad15dcc4183be7610aa489d6068ef125debe89`  
		Last Modified: Tue, 17 Feb 2026 21:24:04 GMT  
		Size: 49.9 MB (49862612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1980b36be6d34e3df4657d184682066772b2fd592aa9bc41e93fbb4de35b5bb2`  
		Last Modified: Tue, 17 Feb 2026 21:24:06 GMT  
		Size: 88.2 MB (88212763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d17b7914e1280b7f8e2bee05ae18e7a76e83e8d4c0cf3127d27a613631b078`  
		Last Modified: Tue, 17 Feb 2026 21:24:02 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986ef5c1b9cfe6f61aa62954e1b0a398a3012f7867c3f3868fb96db505648bf0`  
		Last Modified: Tue, 17 Feb 2026 21:24:02 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8` - unknown; unknown

```console
$ docker pull kapacitor@sha256:e13d7fa2dd962dd80a3e1ec736efce7253711caeb7dc7399a9fff2c797a68d5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38596f1029eabd691eb81a89f2cac6340d4c6706cfdcba15ff860f5fc8e51e1`

```dockerfile
```

-	Layers:
	-	`sha256:d2f801e066cc30314e5c64f6b0939bb24f630f1cb76c9d114e97c9081f6c8e36`  
		Last Modified: Tue, 17 Feb 2026 21:24:02 GMT  
		Size: 3.7 MB (3731269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6f33345dc3b22c1f915be1c8b627246419f73d6d92225841b1935c595a8371d`  
		Last Modified: Tue, 17 Feb 2026 21:24:01 GMT  
		Size: 15.0 KB (15019 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.8` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:7e8cb209d61301c0484554791cc9fdce260b21a2fce6f49c11142ba73137f4c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.8 MB (164846960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e7a9af661a48a139254be235889424adb9f4aca129cfc2285daaa452bde00f`
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
# Tue, 17 Feb 2026 21:23:43 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 17 Feb 2026 21:23:49 GMT
ENV KAPACITOR_VERSION=1.8.2
# Tue, 17 Feb 2026 21:23:49 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 17 Feb 2026 21:23:49 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 17 Feb 2026 21:23:49 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 17 Feb 2026 21:23:49 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 17 Feb 2026 21:23:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 21:23:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 21:23:49 GMT
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
	-	`sha256:abe27530cabf66f1a2b0083fac3a2f24fab337b0cf0fbba537e9c79799306e97`  
		Last Modified: Tue, 17 Feb 2026 21:24:04 GMT  
		Size: 48.4 MB (48394168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb6ea0421fd0b281a72989a500c172318a53e71478a5cbd904758e8a9d05ffa`  
		Last Modified: Tue, 17 Feb 2026 21:24:05 GMT  
		Size: 82.0 MB (82009710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6a9e88f78d378ea4393de64e7e4ca1b4990913d65947090a140e8907f61b3d`  
		Last Modified: Tue, 17 Feb 2026 21:24:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa89b8b24717cac323da8cbef0d7808f06c623027f30ab428fc899d50312fc05`  
		Last Modified: Tue, 17 Feb 2026 21:24:03 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8` - unknown; unknown

```console
$ docker pull kapacitor@sha256:0b26bc42605e300608b8f40266aa7d2bc8f2eeea188a918a19d802eef114698a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:086af4aa3167421d2847526f9085f708f7bec77e4071a6aadd71c69e4264b088`

```dockerfile
```

-	Layers:
	-	`sha256:fb24e1bcfd3a664680c22ee1589456a84b760f5a919d8de365dfc53cf6d4dfce`  
		Last Modified: Tue, 17 Feb 2026 21:24:03 GMT  
		Size: 3.7 MB (3730743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45f84043aeafd2098ee082b05fbd2362e3fd9d57e782239b391a71dd531dd1d0`  
		Last Modified: Tue, 17 Feb 2026 21:24:02 GMT  
		Size: 15.1 KB (15127 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8-alpine`

```console
$ docker pull kapacitor@sha256:855acafe575119c61b8aa3a1590267081f83e69225cea4b61661f69232337447
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.8-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:f44bdf538a1c3cf60f32d663c0e866748755d4026c276c049b480d71920e34d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92252975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b17d24377e2e9f0b8631f3b5edce6c623c5e60dcc6d9dd7fe1e044609d70a42`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:55:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:55:21 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:27:53 GMT
ENV KAPACITOR_VERSION=1.8.2
# Wed, 28 Jan 2026 03:27:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Wed, 28 Jan 2026 03:27:53 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 28 Jan 2026 03:27:53 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 28 Jan 2026 03:27:53 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 28 Jan 2026 03:27:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:27:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:27:53 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591c993c7d9033fa7cd78076b049ddac7d6f79bb06902c7bca758812790bc053`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f6ae05ff7071010198493db629f7b76646c556858fc112d3810a1ff45e7f02`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 314.6 KB (314627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085801fe0b551c017ec55b67fc2b9da5116738b713cc527919618ca9ad3e9ae5`  
		Last Modified: Wed, 28 Jan 2026 03:28:08 GMT  
		Size: 88.1 MB (88132674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d5a77b32109f5a2d8065e3d27ef96c972cedf4a96e4307d30e02dfcbc5f0b6`  
		Last Modified: Wed, 28 Jan 2026 03:28:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb46f8cc26b337892b51bf260762b87f3db82fb83dc10fd3078b73098b15ef86`  
		Last Modified: Wed, 28 Jan 2026 03:28:06 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:7e60dfaa73c57ad9a325d266f4401f9f3c543fa60ea523eb41bb075948d5827b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.3 KB (406253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844842b357864934f15da3f35fa8436b4778711a876fc35142b9f827b160d69e`

```dockerfile
```

-	Layers:
	-	`sha256:c32909963dbc4228a173f333911bebca859c26aa22437d118adef1acdfa78164`  
		Last Modified: Wed, 28 Jan 2026 03:28:06 GMT  
		Size: 390.9 KB (390916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea6cf9fdc2130489dfc2d84bc7a13d0be7faab5932e0670eba58ed233371fb0c`  
		Last Modified: Wed, 28 Jan 2026 03:28:06 GMT  
		Size: 15.3 KB (15337 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8.2`

```console
$ docker pull kapacitor@sha256:7c0963201096a09318be3056c148a81359b1bc67cabbc72370a6c5573fda4c98
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.8.2` - linux; amd64

```console
$ docker pull kapacitor@sha256:64662f96d1a79000d87cc40e3351ddff98e9006c993678bc64433d652aac32c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174717519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ab83ad65a72e9ddbfba143f549a91ba791f114b5b1dc602c335ab0939af7381`
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
# Tue, 17 Feb 2026 21:23:40 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 17 Feb 2026 21:23:46 GMT
ENV KAPACITOR_VERSION=1.8.2
# Tue, 17 Feb 2026 21:23:46 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 17 Feb 2026 21:23:46 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 17 Feb 2026 21:23:46 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 17 Feb 2026 21:23:46 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 17 Feb 2026 21:23:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 21:23:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 21:23:46 GMT
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
	-	`sha256:4ab60e6561c6a7f9c21438b698ad15dcc4183be7610aa489d6068ef125debe89`  
		Last Modified: Tue, 17 Feb 2026 21:24:04 GMT  
		Size: 49.9 MB (49862612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1980b36be6d34e3df4657d184682066772b2fd592aa9bc41e93fbb4de35b5bb2`  
		Last Modified: Tue, 17 Feb 2026 21:24:06 GMT  
		Size: 88.2 MB (88212763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d17b7914e1280b7f8e2bee05ae18e7a76e83e8d4c0cf3127d27a613631b078`  
		Last Modified: Tue, 17 Feb 2026 21:24:02 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986ef5c1b9cfe6f61aa62954e1b0a398a3012f7867c3f3868fb96db505648bf0`  
		Last Modified: Tue, 17 Feb 2026 21:24:02 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8.2` - unknown; unknown

```console
$ docker pull kapacitor@sha256:e13d7fa2dd962dd80a3e1ec736efce7253711caeb7dc7399a9fff2c797a68d5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38596f1029eabd691eb81a89f2cac6340d4c6706cfdcba15ff860f5fc8e51e1`

```dockerfile
```

-	Layers:
	-	`sha256:d2f801e066cc30314e5c64f6b0939bb24f630f1cb76c9d114e97c9081f6c8e36`  
		Last Modified: Tue, 17 Feb 2026 21:24:02 GMT  
		Size: 3.7 MB (3731269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6f33345dc3b22c1f915be1c8b627246419f73d6d92225841b1935c595a8371d`  
		Last Modified: Tue, 17 Feb 2026 21:24:01 GMT  
		Size: 15.0 KB (15019 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.8.2` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:7e8cb209d61301c0484554791cc9fdce260b21a2fce6f49c11142ba73137f4c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.8 MB (164846960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e7a9af661a48a139254be235889424adb9f4aca129cfc2285daaa452bde00f`
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
# Tue, 17 Feb 2026 21:23:43 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 17 Feb 2026 21:23:49 GMT
ENV KAPACITOR_VERSION=1.8.2
# Tue, 17 Feb 2026 21:23:49 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 17 Feb 2026 21:23:49 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 17 Feb 2026 21:23:49 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 17 Feb 2026 21:23:49 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 17 Feb 2026 21:23:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 21:23:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 21:23:49 GMT
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
	-	`sha256:abe27530cabf66f1a2b0083fac3a2f24fab337b0cf0fbba537e9c79799306e97`  
		Last Modified: Tue, 17 Feb 2026 21:24:04 GMT  
		Size: 48.4 MB (48394168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb6ea0421fd0b281a72989a500c172318a53e71478a5cbd904758e8a9d05ffa`  
		Last Modified: Tue, 17 Feb 2026 21:24:05 GMT  
		Size: 82.0 MB (82009710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6a9e88f78d378ea4393de64e7e4ca1b4990913d65947090a140e8907f61b3d`  
		Last Modified: Tue, 17 Feb 2026 21:24:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa89b8b24717cac323da8cbef0d7808f06c623027f30ab428fc899d50312fc05`  
		Last Modified: Tue, 17 Feb 2026 21:24:03 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8.2` - unknown; unknown

```console
$ docker pull kapacitor@sha256:0b26bc42605e300608b8f40266aa7d2bc8f2eeea188a918a19d802eef114698a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:086af4aa3167421d2847526f9085f708f7bec77e4071a6aadd71c69e4264b088`

```dockerfile
```

-	Layers:
	-	`sha256:fb24e1bcfd3a664680c22ee1589456a84b760f5a919d8de365dfc53cf6d4dfce`  
		Last Modified: Tue, 17 Feb 2026 21:24:03 GMT  
		Size: 3.7 MB (3730743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45f84043aeafd2098ee082b05fbd2362e3fd9d57e782239b391a71dd531dd1d0`  
		Last Modified: Tue, 17 Feb 2026 21:24:02 GMT  
		Size: 15.1 KB (15127 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.8.2-alpine`

```console
$ docker pull kapacitor@sha256:855acafe575119c61b8aa3a1590267081f83e69225cea4b61661f69232337447
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.8.2-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:f44bdf538a1c3cf60f32d663c0e866748755d4026c276c049b480d71920e34d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92252975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b17d24377e2e9f0b8631f3b5edce6c623c5e60dcc6d9dd7fe1e044609d70a42`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:55:20 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Wed, 28 Jan 2026 02:55:21 GMT
RUN apk add --no-cache ca-certificates setpriv &&     update-ca-certificates # buildkit
# Wed, 28 Jan 2026 03:27:53 GMT
ENV KAPACITOR_VERSION=1.8.2
# Wed, 28 Jan 2026 03:27:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Wed, 28 Jan 2026 03:27:53 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Wed, 28 Jan 2026 03:27:53 GMT
EXPOSE map[9092/tcp:{}]
# Wed, 28 Jan 2026 03:27:53 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 28 Jan 2026 03:27:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 28 Jan 2026 03:27:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 28 Jan 2026 03:27:53 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591c993c7d9033fa7cd78076b049ddac7d6f79bb06902c7bca758812790bc053`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f6ae05ff7071010198493db629f7b76646c556858fc112d3810a1ff45e7f02`  
		Last Modified: Wed, 28 Jan 2026 02:55:34 GMT  
		Size: 314.6 KB (314627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085801fe0b551c017ec55b67fc2b9da5116738b713cc527919618ca9ad3e9ae5`  
		Last Modified: Wed, 28 Jan 2026 03:28:08 GMT  
		Size: 88.1 MB (88132674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d5a77b32109f5a2d8065e3d27ef96c972cedf4a96e4307d30e02dfcbc5f0b6`  
		Last Modified: Wed, 28 Jan 2026 03:28:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb46f8cc26b337892b51bf260762b87f3db82fb83dc10fd3078b73098b15ef86`  
		Last Modified: Wed, 28 Jan 2026 03:28:06 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.8.2-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:7e60dfaa73c57ad9a325d266f4401f9f3c543fa60ea523eb41bb075948d5827b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.3 KB (406253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844842b357864934f15da3f35fa8436b4778711a876fc35142b9f827b160d69e`

```dockerfile
```

-	Layers:
	-	`sha256:c32909963dbc4228a173f333911bebca859c26aa22437d118adef1acdfa78164`  
		Last Modified: Wed, 28 Jan 2026 03:28:06 GMT  
		Size: 390.9 KB (390916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea6cf9fdc2130489dfc2d84bc7a13d0be7faab5932e0670eba58ed233371fb0c`  
		Last Modified: Wed, 28 Jan 2026 03:28:06 GMT  
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
$ docker pull kapacitor@sha256:7c0963201096a09318be3056c148a81359b1bc67cabbc72370a6c5573fda4c98
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:64662f96d1a79000d87cc40e3351ddff98e9006c993678bc64433d652aac32c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.7 MB (174717519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ab83ad65a72e9ddbfba143f549a91ba791f114b5b1dc602c335ab0939af7381`
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
# Tue, 17 Feb 2026 21:23:40 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 17 Feb 2026 21:23:46 GMT
ENV KAPACITOR_VERSION=1.8.2
# Tue, 17 Feb 2026 21:23:46 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 17 Feb 2026 21:23:46 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 17 Feb 2026 21:23:46 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 17 Feb 2026 21:23:46 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 17 Feb 2026 21:23:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 21:23:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 21:23:46 GMT
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
	-	`sha256:4ab60e6561c6a7f9c21438b698ad15dcc4183be7610aa489d6068ef125debe89`  
		Last Modified: Tue, 17 Feb 2026 21:24:04 GMT  
		Size: 49.9 MB (49862612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1980b36be6d34e3df4657d184682066772b2fd592aa9bc41e93fbb4de35b5bb2`  
		Last Modified: Tue, 17 Feb 2026 21:24:06 GMT  
		Size: 88.2 MB (88212763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d17b7914e1280b7f8e2bee05ae18e7a76e83e8d4c0cf3127d27a613631b078`  
		Last Modified: Tue, 17 Feb 2026 21:24:02 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986ef5c1b9cfe6f61aa62954e1b0a398a3012f7867c3f3868fb96db505648bf0`  
		Last Modified: Tue, 17 Feb 2026 21:24:02 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:e13d7fa2dd962dd80a3e1ec736efce7253711caeb7dc7399a9fff2c797a68d5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3746288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38596f1029eabd691eb81a89f2cac6340d4c6706cfdcba15ff860f5fc8e51e1`

```dockerfile
```

-	Layers:
	-	`sha256:d2f801e066cc30314e5c64f6b0939bb24f630f1cb76c9d114e97c9081f6c8e36`  
		Last Modified: Tue, 17 Feb 2026 21:24:02 GMT  
		Size: 3.7 MB (3731269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6f33345dc3b22c1f915be1c8b627246419f73d6d92225841b1935c595a8371d`  
		Last Modified: Tue, 17 Feb 2026 21:24:01 GMT  
		Size: 15.0 KB (15019 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:7e8cb209d61301c0484554791cc9fdce260b21a2fce6f49c11142ba73137f4c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.8 MB (164846960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e7a9af661a48a139254be235889424adb9f4aca129cfc2285daaa452bde00f`
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
# Tue, 17 Feb 2026 21:23:43 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 17 Feb 2026 21:23:49 GMT
ENV KAPACITOR_VERSION=1.8.2
# Tue, 17 Feb 2026 21:23:49 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 24C975CBA61A024EE1B631787C3D57159FC2F927 &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 17 Feb 2026 21:23:49 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 17 Feb 2026 21:23:49 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 17 Feb 2026 21:23:49 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 17 Feb 2026 21:23:49 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 21:23:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 21:23:49 GMT
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
	-	`sha256:abe27530cabf66f1a2b0083fac3a2f24fab337b0cf0fbba537e9c79799306e97`  
		Last Modified: Tue, 17 Feb 2026 21:24:04 GMT  
		Size: 48.4 MB (48394168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb6ea0421fd0b281a72989a500c172318a53e71478a5cbd904758e8a9d05ffa`  
		Last Modified: Tue, 17 Feb 2026 21:24:05 GMT  
		Size: 82.0 MB (82009710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6a9e88f78d378ea4393de64e7e4ca1b4990913d65947090a140e8907f61b3d`  
		Last Modified: Tue, 17 Feb 2026 21:24:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa89b8b24717cac323da8cbef0d7808f06c623027f30ab428fc899d50312fc05`  
		Last Modified: Tue, 17 Feb 2026 21:24:03 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:0b26bc42605e300608b8f40266aa7d2bc8f2eeea188a918a19d802eef114698a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3745870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:086af4aa3167421d2847526f9085f708f7bec77e4071a6aadd71c69e4264b088`

```dockerfile
```

-	Layers:
	-	`sha256:fb24e1bcfd3a664680c22ee1589456a84b760f5a919d8de365dfc53cf6d4dfce`  
		Last Modified: Tue, 17 Feb 2026 21:24:03 GMT  
		Size: 3.7 MB (3730743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45f84043aeafd2098ee082b05fbd2362e3fd9d57e782239b391a71dd531dd1d0`  
		Last Modified: Tue, 17 Feb 2026 21:24:02 GMT  
		Size: 15.1 KB (15127 bytes)  
		MIME: application/vnd.in-toto+json
