<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.6`](#kapacitor16)
-	[`kapacitor:1.6-alpine`](#kapacitor16-alpine)
-	[`kapacitor:1.6.6`](#kapacitor166)
-	[`kapacitor:1.6.6-alpine`](#kapacitor166-alpine)
-	[`kapacitor:1.7`](#kapacitor17)
-	[`kapacitor:1.7-alpine`](#kapacitor17-alpine)
-	[`kapacitor:1.7.4`](#kapacitor174)
-	[`kapacitor:1.7.4-alpine`](#kapacitor174-alpine)
-	[`kapacitor:alpine`](#kapacitoralpine)
-	[`kapacitor:latest`](#kapacitorlatest)

## `kapacitor:1.6`

```console
$ docker pull kapacitor@sha256:7b6d8b47c83feb4a725f70c311a5c28f209f3604f37f1e0e35612c7999461447
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:36958c8ed037e8be696e3d5a937a412033a174c15ca3fa287996ac478ec09ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139040977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5ff5b388d1b2371be3ff4a7740f7752bf1f51c70eebdf2e152bcf43601edfd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 15:38:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Apr 2024 15:38:09 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
ENV KAPACITOR_VERSION=1.6.6
# Tue, 23 Apr 2024 15:38:09 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 23 Apr 2024 15:38:09 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 23 Apr 2024 15:38:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Apr 2024 15:38:09 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f244433f7fe311b3e464c8867b280a9e08d67224abbc58efbad8f856f027a0`  
		Last Modified: Thu, 25 Apr 2024 21:43:40 GMT  
		Size: 7.1 MB (7122312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0eb9f8cf8840d6d9e0a65609025400f67a608644e2b6e5115dd204332df67ef`  
		Last Modified: Wed, 01 May 2024 21:52:41 GMT  
		Size: 35.8 MB (35805920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ca5c9305ef7945a64757b66ae69885bcd35b0965229c205bb4688f084e15e9`  
		Last Modified: Wed, 01 May 2024 21:52:42 GMT  
		Size: 65.7 MB (65672560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf2deae0b12881a5178a3860097892b9c22bf2dfe91637854612fac923661da`  
		Last Modified: Wed, 01 May 2024 21:52:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f898d670cd24f776b95930239adf13fffecd8d812999248918e5e80912a001`  
		Last Modified: Wed, 01 May 2024 21:52:41 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:30d388c6e7b994f6bbc8fe3bb32714238dba2a3e68f1dba5acfc456d1a0cfdd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3484494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3934ff54a57dce382eff061ccd50974b0a4262b8e7f281278f713309f7de752f`

```dockerfile
```

-	Layers:
	-	`sha256:9bcaae2aa803c0f0877fbd34f9367601aa99942a9589e311b797fa3754b15449`  
		Last Modified: Wed, 01 May 2024 21:52:40 GMT  
		Size: 3.5 MB (3469611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b197bf53164d5687a79becfb5fd3a983f1490a2869c4a5fb62f8204a6d95b01`  
		Last Modified: Wed, 01 May 2024 21:52:41 GMT  
		Size: 14.9 KB (14883 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:2a5d4aa861042064f23aedb5a9322d97bc7bb97c56523a328a53b5de157b67fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.2 MB (130225974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932c1f218710789698ea636b715112430dce698517a2400f2e6528f262ce6daf`
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
# Tue, 23 Apr 2024 15:38:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Apr 2024 15:38:09 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
ENV KAPACITOR_VERSION=1.6.6
# Tue, 23 Apr 2024 15:38:09 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 23 Apr 2024 15:38:09 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 23 Apr 2024 15:38:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Apr 2024 15:38:09 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c6efd61b232e6060a5ae247be4a304ae261939d0814281b2db15ac1c5f6b35`  
		Last Modified: Thu, 25 Apr 2024 21:45:59 GMT  
		Size: 7.1 MB (7068156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96837400cded23378d9831512f08031152dca96a7de8e92d6991c6a1b87d686`  
		Last Modified: Wed, 01 May 2024 22:31:20 GMT  
		Size: 33.1 MB (33086496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94656a3c11a9d526b60d23133b496d1e129b82341aa73c368f01e784d386b1c9`  
		Last Modified: Wed, 01 May 2024 22:31:21 GMT  
		Size: 61.7 MB (61669865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711e2c98312f499e96a65c8c355e30356d324edbe9e58ee54d87205fd023c9f4`  
		Last Modified: Wed, 01 May 2024 22:31:19 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bba94bb000f426d68973143a39dbd88bff2fc36e89475fe8d3fdbfa6df67b7`  
		Last Modified: Wed, 01 May 2024 22:31:20 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:3d55f11762cc519e2744ed2a09b7043736a5711dff21daff8a7f18d2ac63d3c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3484744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f11d4e05d4c57650107de3185391b099f4efaa8c142c41191eb030056528eb1`

```dockerfile
```

-	Layers:
	-	`sha256:e64b1d2f755f8c5999cd0cba3c2766e1ec58bb8316aaf0cb195d0b5ad69ff447`  
		Last Modified: Wed, 01 May 2024 22:31:20 GMT  
		Size: 3.5 MB (3469852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf8583cf199bf9f4d85026fe090c4d19e8444490efd549558f03bb825778c24b`  
		Last Modified: Wed, 01 May 2024 22:31:19 GMT  
		Size: 14.9 KB (14892 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.6-alpine`

```console
$ docker pull kapacitor@sha256:b4cf85324a4e6b28aa431755d396b52c7d4d5317893f4c96236950adb3deb60a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:c838f780f23a429be87d9152d630073cbff9aad05af15d6dcb87d51dadea7032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68682453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d152c443ce44ecc25ae549deb0a56c9906fc5fa63324138daebc2604986a0504`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 15:38:09 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
ENV KAPACITOR_VERSION=1.6.6
# Tue, 23 Apr 2024 15:38:09 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 23 Apr 2024 15:38:09 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 23 Apr 2024 15:38:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Apr 2024 15:38:09 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66916d60fd220360ccf9f8ce7c7629a0f7b9c16e56dc879ed453c020a7ff8c8`  
		Last Modified: Wed, 01 May 2024 21:52:33 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f8a36a6f57d656e743d30557568a7b1e6b2dafb931cf225f756067aef759a3`  
		Last Modified: Wed, 01 May 2024 21:52:33 GMT  
		Size: 293.7 KB (293676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f25d6956e5cdd4dd969000511d7528eeaed8a268e3acb9ac90115d8e1d63b9b`  
		Last Modified: Wed, 01 May 2024 21:52:34 GMT  
		Size: 65.6 MB (65580207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bceb2a4e99c2e31f9af0ff598dc0f87c7e27eed1bb736e22d6c9874b208b7fe`  
		Last Modified: Wed, 01 May 2024 21:52:33 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8850cca1d0e9e5a1726eff2367774c4f202dc34f2fb9e79c36046c8352c085ff`  
		Last Modified: Wed, 01 May 2024 21:52:33 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:808386e21cc05af613cd8716995b2c88f44669bc24afb205d0e396f295c6f71b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 KB (338343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2161b1b402629d0570e430cfc36fbcf55748d51f5e3f7138bff374033616d8`

```dockerfile
```

-	Layers:
	-	`sha256:afdbd4030475182b28951bbebd9a65520473cf66aece8ff8a4c6d01556b5d75b`  
		Last Modified: Wed, 01 May 2024 21:52:33 GMT  
		Size: 323.7 KB (323684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fc80ab1608c52679a3ad3c744fc1e2358447e937841425e429e6e22e0f4371d`  
		Last Modified: Wed, 01 May 2024 21:52:33 GMT  
		Size: 14.7 KB (14659 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.6.6`

```console
$ docker pull kapacitor@sha256:7b6d8b47c83feb4a725f70c311a5c28f209f3604f37f1e0e35612c7999461447
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.6.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:36958c8ed037e8be696e3d5a937a412033a174c15ca3fa287996ac478ec09ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139040977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5ff5b388d1b2371be3ff4a7740f7752bf1f51c70eebdf2e152bcf43601edfd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 15:38:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Apr 2024 15:38:09 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
ENV KAPACITOR_VERSION=1.6.6
# Tue, 23 Apr 2024 15:38:09 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 23 Apr 2024 15:38:09 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 23 Apr 2024 15:38:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Apr 2024 15:38:09 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f244433f7fe311b3e464c8867b280a9e08d67224abbc58efbad8f856f027a0`  
		Last Modified: Thu, 25 Apr 2024 21:43:40 GMT  
		Size: 7.1 MB (7122312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0eb9f8cf8840d6d9e0a65609025400f67a608644e2b6e5115dd204332df67ef`  
		Last Modified: Wed, 01 May 2024 21:52:41 GMT  
		Size: 35.8 MB (35805920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ca5c9305ef7945a64757b66ae69885bcd35b0965229c205bb4688f084e15e9`  
		Last Modified: Wed, 01 May 2024 21:52:42 GMT  
		Size: 65.7 MB (65672560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf2deae0b12881a5178a3860097892b9c22bf2dfe91637854612fac923661da`  
		Last Modified: Wed, 01 May 2024 21:52:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f898d670cd24f776b95930239adf13fffecd8d812999248918e5e80912a001`  
		Last Modified: Wed, 01 May 2024 21:52:41 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:30d388c6e7b994f6bbc8fe3bb32714238dba2a3e68f1dba5acfc456d1a0cfdd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3484494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3934ff54a57dce382eff061ccd50974b0a4262b8e7f281278f713309f7de752f`

```dockerfile
```

-	Layers:
	-	`sha256:9bcaae2aa803c0f0877fbd34f9367601aa99942a9589e311b797fa3754b15449`  
		Last Modified: Wed, 01 May 2024 21:52:40 GMT  
		Size: 3.5 MB (3469611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b197bf53164d5687a79becfb5fd3a983f1490a2869c4a5fb62f8204a6d95b01`  
		Last Modified: Wed, 01 May 2024 21:52:41 GMT  
		Size: 14.9 KB (14883 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.6.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:2a5d4aa861042064f23aedb5a9322d97bc7bb97c56523a328a53b5de157b67fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.2 MB (130225974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932c1f218710789698ea636b715112430dce698517a2400f2e6528f262ce6daf`
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
# Tue, 23 Apr 2024 15:38:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Apr 2024 15:38:09 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
ENV KAPACITOR_VERSION=1.6.6
# Tue, 23 Apr 2024 15:38:09 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 23 Apr 2024 15:38:09 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 23 Apr 2024 15:38:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Apr 2024 15:38:09 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c6efd61b232e6060a5ae247be4a304ae261939d0814281b2db15ac1c5f6b35`  
		Last Modified: Thu, 25 Apr 2024 21:45:59 GMT  
		Size: 7.1 MB (7068156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96837400cded23378d9831512f08031152dca96a7de8e92d6991c6a1b87d686`  
		Last Modified: Wed, 01 May 2024 22:31:20 GMT  
		Size: 33.1 MB (33086496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94656a3c11a9d526b60d23133b496d1e129b82341aa73c368f01e784d386b1c9`  
		Last Modified: Wed, 01 May 2024 22:31:21 GMT  
		Size: 61.7 MB (61669865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711e2c98312f499e96a65c8c355e30356d324edbe9e58ee54d87205fd023c9f4`  
		Last Modified: Wed, 01 May 2024 22:31:19 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bba94bb000f426d68973143a39dbd88bff2fc36e89475fe8d3fdbfa6df67b7`  
		Last Modified: Wed, 01 May 2024 22:31:20 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:3d55f11762cc519e2744ed2a09b7043736a5711dff21daff8a7f18d2ac63d3c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3484744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f11d4e05d4c57650107de3185391b099f4efaa8c142c41191eb030056528eb1`

```dockerfile
```

-	Layers:
	-	`sha256:e64b1d2f755f8c5999cd0cba3c2766e1ec58bb8316aaf0cb195d0b5ad69ff447`  
		Last Modified: Wed, 01 May 2024 22:31:20 GMT  
		Size: 3.5 MB (3469852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf8583cf199bf9f4d85026fe090c4d19e8444490efd549558f03bb825778c24b`  
		Last Modified: Wed, 01 May 2024 22:31:19 GMT  
		Size: 14.9 KB (14892 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.6.6-alpine`

```console
$ docker pull kapacitor@sha256:b4cf85324a4e6b28aa431755d396b52c7d4d5317893f4c96236950adb3deb60a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.6.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:c838f780f23a429be87d9152d630073cbff9aad05af15d6dcb87d51dadea7032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68682453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d152c443ce44ecc25ae549deb0a56c9906fc5fa63324138daebc2604986a0504`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 15:38:09 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
ENV KAPACITOR_VERSION=1.6.6
# Tue, 23 Apr 2024 15:38:09 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 23 Apr 2024 15:38:09 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 23 Apr 2024 15:38:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Apr 2024 15:38:09 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66916d60fd220360ccf9f8ce7c7629a0f7b9c16e56dc879ed453c020a7ff8c8`  
		Last Modified: Wed, 01 May 2024 21:52:33 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41f8a36a6f57d656e743d30557568a7b1e6b2dafb931cf225f756067aef759a3`  
		Last Modified: Wed, 01 May 2024 21:52:33 GMT  
		Size: 293.7 KB (293676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f25d6956e5cdd4dd969000511d7528eeaed8a268e3acb9ac90115d8e1d63b9b`  
		Last Modified: Wed, 01 May 2024 21:52:34 GMT  
		Size: 65.6 MB (65580207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bceb2a4e99c2e31f9af0ff598dc0f87c7e27eed1bb736e22d6c9874b208b7fe`  
		Last Modified: Wed, 01 May 2024 21:52:33 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8850cca1d0e9e5a1726eff2367774c4f202dc34f2fb9e79c36046c8352c085ff`  
		Last Modified: Wed, 01 May 2024 21:52:33 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6.6-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:808386e21cc05af613cd8716995b2c88f44669bc24afb205d0e396f295c6f71b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 KB (338343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2161b1b402629d0570e430cfc36fbcf55748d51f5e3f7138bff374033616d8`

```dockerfile
```

-	Layers:
	-	`sha256:afdbd4030475182b28951bbebd9a65520473cf66aece8ff8a4c6d01556b5d75b`  
		Last Modified: Wed, 01 May 2024 21:52:33 GMT  
		Size: 323.7 KB (323684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fc80ab1608c52679a3ad3c744fc1e2358447e937841425e429e6e22e0f4371d`  
		Last Modified: Wed, 01 May 2024 21:52:33 GMT  
		Size: 14.7 KB (14659 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7`

```console
$ docker pull kapacitor@sha256:e582e61f5cd2eb07572a576e3006f0740076ffd2964acaf4ecdaa70d3e223c52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:f2a3abf145840d8384d6e6c26fe2a38b8dff0f3863514ec42ecd88bd64948457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144745387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ae99dcbfbc6d98a81ca558efc98306dc039cec339110e4d597e07939ac3e07`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 15:38:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Apr 2024 15:38:09 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
ENV KAPACITOR_VERSION=1.7.4
# Tue, 23 Apr 2024 15:38:09 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 23 Apr 2024 15:38:09 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 23 Apr 2024 15:38:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Apr 2024 15:38:09 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f244433f7fe311b3e464c8867b280a9e08d67224abbc58efbad8f856f027a0`  
		Last Modified: Thu, 25 Apr 2024 21:43:40 GMT  
		Size: 7.1 MB (7122312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32275dffc166317ba0f3c33faba8529b9fd9efd5a867a66d7bac3b7bdc467824`  
		Last Modified: Wed, 01 May 2024 21:52:44 GMT  
		Size: 35.8 MB (35805926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea23969ccb1c1a7dfe0eb009ca74f18abd38eafa7ed5cf88d67b54e07ea85c6`  
		Last Modified: Wed, 01 May 2024 21:52:45 GMT  
		Size: 71.4 MB (71376899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b60ff57bba1e21482d2c79f69accdf62a62f72d9c05c7612ce67eabe0f4948b`  
		Last Modified: Wed, 01 May 2024 21:52:43 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941d38210a09982c51b2324c21f51daaf475fe3af2752857cf162705e8a3555c`  
		Last Modified: Wed, 01 May 2024 21:52:43 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:482db4e67336da2e634ea748cd238080ad3c2ba75682ecef37cf5b1da969dffb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3491333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1235893df8d994c52bc9587ddd429bd335da95e9575faf34b4b3d5dc66f317c5`

```dockerfile
```

-	Layers:
	-	`sha256:420966fd6be96ab481cc656625f60b208e799b4ecd1f6955dd244aae5673e746`  
		Last Modified: Wed, 01 May 2024 21:52:44 GMT  
		Size: 3.5 MB (3476143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f6633f445bb984ecbea9a2ed79a38dae9713b8a39722b64289cacebbe7668d1`  
		Last Modified: Wed, 01 May 2024 21:52:43 GMT  
		Size: 15.2 KB (15190 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:5fc6789bae135d692275ce27d836ea4f6633a8debc2a59337956b59b7d254815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135651060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2dca17f068be1cd1a104d8bd8bc3dfe433ba9583e50e4611875b486d31cc3f2`
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
# Tue, 23 Apr 2024 15:38:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Apr 2024 15:38:09 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
ENV KAPACITOR_VERSION=1.7.4
# Tue, 23 Apr 2024 15:38:09 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 23 Apr 2024 15:38:09 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 23 Apr 2024 15:38:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Apr 2024 15:38:09 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c6efd61b232e6060a5ae247be4a304ae261939d0814281b2db15ac1c5f6b35`  
		Last Modified: Thu, 25 Apr 2024 21:45:59 GMT  
		Size: 7.1 MB (7068156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96837400cded23378d9831512f08031152dca96a7de8e92d6991c6a1b87d686`  
		Last Modified: Wed, 01 May 2024 22:31:20 GMT  
		Size: 33.1 MB (33086496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6df17cd1c790b351f8af8222222ecf7a33620381075a8a66b67752cbc0257f`  
		Last Modified: Wed, 01 May 2024 22:32:22 GMT  
		Size: 67.1 MB (67094882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66866e052b52cefd9be1c09ab9a2893d7aab75a5e95eaa4e6d49e534da60c315`  
		Last Modified: Wed, 01 May 2024 22:32:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c578433905e794395fab461306112019f1083518d0fb977af233065da7a38f46`  
		Last Modified: Wed, 01 May 2024 22:32:20 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:52a69495c045dc2ca841f0dae98c853e648cf75cd45aee4036883ace04afda8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3490601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f4580f1f8a29e1e64cc8e6946ed8860599ee41058bd9148a9855106e2cbf89`

```dockerfile
```

-	Layers:
	-	`sha256:1d4ca10d42ae583b106574df97ffe393fdc3e53d11a87be4658a7ddd8bfa979d`  
		Last Modified: Wed, 01 May 2024 22:32:20 GMT  
		Size: 3.5 MB (3475734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca53cdb39cd0c179f302f541412479f0a33b5bddd11502b105d9187a8cee17a2`  
		Last Modified: Wed, 01 May 2024 22:32:20 GMT  
		Size: 14.9 KB (14867 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7-alpine`

```console
$ docker pull kapacitor@sha256:9fc5e69e93d3515b9e85356ff85f6f4a1cb04da0ad5e22a0d3563db230f2825a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.7-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:8d995686429b888c25800c79144b7732198312aa1c443eb86ae25b532a7ad3a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75007076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3458399ce5523f622ab6567b3f46929f6145af7d181e8ec5379e883e35aeb39`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 15:38:09 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
ENV KAPACITOR_VERSION=1.7.4
# Tue, 23 Apr 2024 15:38:09 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 23 Apr 2024 15:38:09 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 23 Apr 2024 15:38:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Apr 2024 15:38:09 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f6c7b00e1c89be5e6275805938d1a5583dfd25fb27d5ef70ca4d297c72d133`  
		Last Modified: Wed, 01 May 2024 21:52:41 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f161ad4c2c7b9aeca4820e8bfcf7a440e4cc8b476a5e85fecc30c9091bb7db2f`  
		Last Modified: Wed, 01 May 2024 21:52:41 GMT  
		Size: 295.8 KB (295752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303ee935e98cea5d70feb392f3ec1c357816ab2476efbef8d3aa482152d3c7da`  
		Last Modified: Wed, 01 May 2024 21:52:44 GMT  
		Size: 71.3 MB (71308002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b533ae6c6a974972db5a3f9360562cbca52a5527bb2b2eb2e88b2e32c0e25a10`  
		Last Modified: Wed, 01 May 2024 21:52:41 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e069b3fc1475991b7c1aefa738806a7890279ac8e395706e31d33d32edbc2519`  
		Last Modified: Wed, 01 May 2024 21:52:42 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:80a5466fa2da29834fa7167a1525d288fbc89df33ea88f7b7d3b1b1bd25d8672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.9 KB (349942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6bab527acb241daa7d027e1e7f139025a3520607b0a4c3db61e9562b4fca4e`

```dockerfile
```

-	Layers:
	-	`sha256:8a1d0b0fc6d659ddf206298a9f8b65d112a6027bf5111317c1e8f65d092cdc8d`  
		Last Modified: Wed, 01 May 2024 21:52:41 GMT  
		Size: 334.4 KB (334362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:810e4fb4513fc4602b39a9efd5f38a72e37f02e01869b5c6c91672932124a207`  
		Last Modified: Wed, 01 May 2024 21:52:41 GMT  
		Size: 15.6 KB (15580 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7.4`

```console
$ docker pull kapacitor@sha256:e582e61f5cd2eb07572a576e3006f0740076ffd2964acaf4ecdaa70d3e223c52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7.4` - linux; amd64

```console
$ docker pull kapacitor@sha256:f2a3abf145840d8384d6e6c26fe2a38b8dff0f3863514ec42ecd88bd64948457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144745387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ae99dcbfbc6d98a81ca558efc98306dc039cec339110e4d597e07939ac3e07`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 15:38:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Apr 2024 15:38:09 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
ENV KAPACITOR_VERSION=1.7.4
# Tue, 23 Apr 2024 15:38:09 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 23 Apr 2024 15:38:09 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 23 Apr 2024 15:38:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Apr 2024 15:38:09 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f244433f7fe311b3e464c8867b280a9e08d67224abbc58efbad8f856f027a0`  
		Last Modified: Thu, 25 Apr 2024 21:43:40 GMT  
		Size: 7.1 MB (7122312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32275dffc166317ba0f3c33faba8529b9fd9efd5a867a66d7bac3b7bdc467824`  
		Last Modified: Wed, 01 May 2024 21:52:44 GMT  
		Size: 35.8 MB (35805926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea23969ccb1c1a7dfe0eb009ca74f18abd38eafa7ed5cf88d67b54e07ea85c6`  
		Last Modified: Wed, 01 May 2024 21:52:45 GMT  
		Size: 71.4 MB (71376899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b60ff57bba1e21482d2c79f69accdf62a62f72d9c05c7612ce67eabe0f4948b`  
		Last Modified: Wed, 01 May 2024 21:52:43 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941d38210a09982c51b2324c21f51daaf475fe3af2752857cf162705e8a3555c`  
		Last Modified: Wed, 01 May 2024 21:52:43 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.4` - unknown; unknown

```console
$ docker pull kapacitor@sha256:482db4e67336da2e634ea748cd238080ad3c2ba75682ecef37cf5b1da969dffb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3491333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1235893df8d994c52bc9587ddd429bd335da95e9575faf34b4b3d5dc66f317c5`

```dockerfile
```

-	Layers:
	-	`sha256:420966fd6be96ab481cc656625f60b208e799b4ecd1f6955dd244aae5673e746`  
		Last Modified: Wed, 01 May 2024 21:52:44 GMT  
		Size: 3.5 MB (3476143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f6633f445bb984ecbea9a2ed79a38dae9713b8a39722b64289cacebbe7668d1`  
		Last Modified: Wed, 01 May 2024 21:52:43 GMT  
		Size: 15.2 KB (15190 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7.4` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:5fc6789bae135d692275ce27d836ea4f6633a8debc2a59337956b59b7d254815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135651060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2dca17f068be1cd1a104d8bd8bc3dfe433ba9583e50e4611875b486d31cc3f2`
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
# Tue, 23 Apr 2024 15:38:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Apr 2024 15:38:09 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
ENV KAPACITOR_VERSION=1.7.4
# Tue, 23 Apr 2024 15:38:09 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 23 Apr 2024 15:38:09 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 23 Apr 2024 15:38:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Apr 2024 15:38:09 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c6efd61b232e6060a5ae247be4a304ae261939d0814281b2db15ac1c5f6b35`  
		Last Modified: Thu, 25 Apr 2024 21:45:59 GMT  
		Size: 7.1 MB (7068156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96837400cded23378d9831512f08031152dca96a7de8e92d6991c6a1b87d686`  
		Last Modified: Wed, 01 May 2024 22:31:20 GMT  
		Size: 33.1 MB (33086496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6df17cd1c790b351f8af8222222ecf7a33620381075a8a66b67752cbc0257f`  
		Last Modified: Wed, 01 May 2024 22:32:22 GMT  
		Size: 67.1 MB (67094882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66866e052b52cefd9be1c09ab9a2893d7aab75a5e95eaa4e6d49e534da60c315`  
		Last Modified: Wed, 01 May 2024 22:32:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c578433905e794395fab461306112019f1083518d0fb977af233065da7a38f46`  
		Last Modified: Wed, 01 May 2024 22:32:20 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.4` - unknown; unknown

```console
$ docker pull kapacitor@sha256:52a69495c045dc2ca841f0dae98c853e648cf75cd45aee4036883ace04afda8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3490601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f4580f1f8a29e1e64cc8e6946ed8860599ee41058bd9148a9855106e2cbf89`

```dockerfile
```

-	Layers:
	-	`sha256:1d4ca10d42ae583b106574df97ffe393fdc3e53d11a87be4658a7ddd8bfa979d`  
		Last Modified: Wed, 01 May 2024 22:32:20 GMT  
		Size: 3.5 MB (3475734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca53cdb39cd0c179f302f541412479f0a33b5bddd11502b105d9187a8cee17a2`  
		Last Modified: Wed, 01 May 2024 22:32:20 GMT  
		Size: 14.9 KB (14867 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7.4-alpine`

```console
$ docker pull kapacitor@sha256:9fc5e69e93d3515b9e85356ff85f6f4a1cb04da0ad5e22a0d3563db230f2825a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.7.4-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:8d995686429b888c25800c79144b7732198312aa1c443eb86ae25b532a7ad3a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75007076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3458399ce5523f622ab6567b3f46929f6145af7d181e8ec5379e883e35aeb39`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 15:38:09 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
ENV KAPACITOR_VERSION=1.7.4
# Tue, 23 Apr 2024 15:38:09 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 23 Apr 2024 15:38:09 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 23 Apr 2024 15:38:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Apr 2024 15:38:09 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f6c7b00e1c89be5e6275805938d1a5583dfd25fb27d5ef70ca4d297c72d133`  
		Last Modified: Wed, 01 May 2024 21:52:41 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f161ad4c2c7b9aeca4820e8bfcf7a440e4cc8b476a5e85fecc30c9091bb7db2f`  
		Last Modified: Wed, 01 May 2024 21:52:41 GMT  
		Size: 295.8 KB (295752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303ee935e98cea5d70feb392f3ec1c357816ab2476efbef8d3aa482152d3c7da`  
		Last Modified: Wed, 01 May 2024 21:52:44 GMT  
		Size: 71.3 MB (71308002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b533ae6c6a974972db5a3f9360562cbca52a5527bb2b2eb2e88b2e32c0e25a10`  
		Last Modified: Wed, 01 May 2024 21:52:41 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e069b3fc1475991b7c1aefa738806a7890279ac8e395706e31d33d32edbc2519`  
		Last Modified: Wed, 01 May 2024 21:52:42 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.4-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:80a5466fa2da29834fa7167a1525d288fbc89df33ea88f7b7d3b1b1bd25d8672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.9 KB (349942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6bab527acb241daa7d027e1e7f139025a3520607b0a4c3db61e9562b4fca4e`

```dockerfile
```

-	Layers:
	-	`sha256:8a1d0b0fc6d659ddf206298a9f8b65d112a6027bf5111317c1e8f65d092cdc8d`  
		Last Modified: Wed, 01 May 2024 21:52:41 GMT  
		Size: 334.4 KB (334362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:810e4fb4513fc4602b39a9efd5f38a72e37f02e01869b5c6c91672932124a207`  
		Last Modified: Wed, 01 May 2024 21:52:41 GMT  
		Size: 15.6 KB (15580 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:9fc5e69e93d3515b9e85356ff85f6f4a1cb04da0ad5e22a0d3563db230f2825a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:8d995686429b888c25800c79144b7732198312aa1c443eb86ae25b532a7ad3a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75007076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3458399ce5523f622ab6567b3f46929f6145af7d181e8ec5379e883e35aeb39`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 15:38:09 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
ENV KAPACITOR_VERSION=1.7.4
# Tue, 23 Apr 2024 15:38:09 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 23 Apr 2024 15:38:09 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 23 Apr 2024 15:38:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Apr 2024 15:38:09 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f6c7b00e1c89be5e6275805938d1a5583dfd25fb27d5ef70ca4d297c72d133`  
		Last Modified: Wed, 01 May 2024 21:52:41 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f161ad4c2c7b9aeca4820e8bfcf7a440e4cc8b476a5e85fecc30c9091bb7db2f`  
		Last Modified: Wed, 01 May 2024 21:52:41 GMT  
		Size: 295.8 KB (295752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303ee935e98cea5d70feb392f3ec1c357816ab2476efbef8d3aa482152d3c7da`  
		Last Modified: Wed, 01 May 2024 21:52:44 GMT  
		Size: 71.3 MB (71308002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b533ae6c6a974972db5a3f9360562cbca52a5527bb2b2eb2e88b2e32c0e25a10`  
		Last Modified: Wed, 01 May 2024 21:52:41 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e069b3fc1475991b7c1aefa738806a7890279ac8e395706e31d33d32edbc2519`  
		Last Modified: Wed, 01 May 2024 21:52:42 GMT  
		Size: 276.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:80a5466fa2da29834fa7167a1525d288fbc89df33ea88f7b7d3b1b1bd25d8672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.9 KB (349942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6bab527acb241daa7d027e1e7f139025a3520607b0a4c3db61e9562b4fca4e`

```dockerfile
```

-	Layers:
	-	`sha256:8a1d0b0fc6d659ddf206298a9f8b65d112a6027bf5111317c1e8f65d092cdc8d`  
		Last Modified: Wed, 01 May 2024 21:52:41 GMT  
		Size: 334.4 KB (334362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:810e4fb4513fc4602b39a9efd5f38a72e37f02e01869b5c6c91672932124a207`  
		Last Modified: Wed, 01 May 2024 21:52:41 GMT  
		Size: 15.6 KB (15580 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:e582e61f5cd2eb07572a576e3006f0740076ffd2964acaf4ecdaa70d3e223c52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:f2a3abf145840d8384d6e6c26fe2a38b8dff0f3863514ec42ecd88bd64948457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144745387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ae99dcbfbc6d98a81ca558efc98306dc039cec339110e4d597e07939ac3e07`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 17 Apr 2024 17:56:33 GMT
ARG RELEASE
# Wed, 17 Apr 2024 17:56:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Apr 2024 17:56:33 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Apr 2024 17:56:35 GMT
ADD file:aa631666e3d7f8925e1308c15b2b63b5649db2cfcb079cba8218af98a5966923 in / 
# Wed, 17 Apr 2024 17:56:35 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 15:38:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Apr 2024 15:38:09 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
ENV KAPACITOR_VERSION=1.7.4
# Tue, 23 Apr 2024 15:38:09 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 23 Apr 2024 15:38:09 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 23 Apr 2024 15:38:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Apr 2024 15:38:09 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:a271f97708e3f580cf6997962841fe468ee650379d940e567090a62dfa2997cf`  
		Last Modified: Wed, 17 Apr 2024 23:01:11 GMT  
		Size: 30.4 MB (30439728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f244433f7fe311b3e464c8867b280a9e08d67224abbc58efbad8f856f027a0`  
		Last Modified: Thu, 25 Apr 2024 21:43:40 GMT  
		Size: 7.1 MB (7122312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32275dffc166317ba0f3c33faba8529b9fd9efd5a867a66d7bac3b7bdc467824`  
		Last Modified: Wed, 01 May 2024 21:52:44 GMT  
		Size: 35.8 MB (35805926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea23969ccb1c1a7dfe0eb009ca74f18abd38eafa7ed5cf88d67b54e07ea85c6`  
		Last Modified: Wed, 01 May 2024 21:52:45 GMT  
		Size: 71.4 MB (71376899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b60ff57bba1e21482d2c79f69accdf62a62f72d9c05c7612ce67eabe0f4948b`  
		Last Modified: Wed, 01 May 2024 21:52:43 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941d38210a09982c51b2324c21f51daaf475fe3af2752857cf162705e8a3555c`  
		Last Modified: Wed, 01 May 2024 21:52:43 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:482db4e67336da2e634ea748cd238080ad3c2ba75682ecef37cf5b1da969dffb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3491333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1235893df8d994c52bc9587ddd429bd335da95e9575faf34b4b3d5dc66f317c5`

```dockerfile
```

-	Layers:
	-	`sha256:420966fd6be96ab481cc656625f60b208e799b4ecd1f6955dd244aae5673e746`  
		Last Modified: Wed, 01 May 2024 21:52:44 GMT  
		Size: 3.5 MB (3476143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f6633f445bb984ecbea9a2ed79a38dae9713b8a39722b64289cacebbe7668d1`  
		Last Modified: Wed, 01 May 2024 21:52:43 GMT  
		Size: 15.2 KB (15190 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:5fc6789bae135d692275ce27d836ea4f6633a8debc2a59337956b59b7d254815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135651060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2dca17f068be1cd1a104d8bd8bc3dfe433ba9583e50e4611875b486d31cc3f2`
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
# Tue, 23 Apr 2024 15:38:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Apr 2024 15:38:09 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
ENV KAPACITOR_VERSION=1.7.4
# Tue, 23 Apr 2024 15:38:09 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 23 Apr 2024 15:38:09 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 23 Apr 2024 15:38:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 23 Apr 2024 15:38:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Apr 2024 15:38:09 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c6efd61b232e6060a5ae247be4a304ae261939d0814281b2db15ac1c5f6b35`  
		Last Modified: Thu, 25 Apr 2024 21:45:59 GMT  
		Size: 7.1 MB (7068156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96837400cded23378d9831512f08031152dca96a7de8e92d6991c6a1b87d686`  
		Last Modified: Wed, 01 May 2024 22:31:20 GMT  
		Size: 33.1 MB (33086496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6df17cd1c790b351f8af8222222ecf7a33620381075a8a66b67752cbc0257f`  
		Last Modified: Wed, 01 May 2024 22:32:22 GMT  
		Size: 67.1 MB (67094882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66866e052b52cefd9be1c09ab9a2893d7aab75a5e95eaa4e6d49e534da60c315`  
		Last Modified: Wed, 01 May 2024 22:32:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c578433905e794395fab461306112019f1083518d0fb977af233065da7a38f46`  
		Last Modified: Wed, 01 May 2024 22:32:20 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:52a69495c045dc2ca841f0dae98c853e648cf75cd45aee4036883ace04afda8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3490601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f4580f1f8a29e1e64cc8e6946ed8860599ee41058bd9148a9855106e2cbf89`

```dockerfile
```

-	Layers:
	-	`sha256:1d4ca10d42ae583b106574df97ffe393fdc3e53d11a87be4658a7ddd8bfa979d`  
		Last Modified: Wed, 01 May 2024 22:32:20 GMT  
		Size: 3.5 MB (3475734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca53cdb39cd0c179f302f541412479f0a33b5bddd11502b105d9187a8cee17a2`  
		Last Modified: Wed, 01 May 2024 22:32:20 GMT  
		Size: 14.9 KB (14867 bytes)  
		MIME: application/vnd.in-toto+json
