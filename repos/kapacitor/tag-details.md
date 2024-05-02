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
$ docker pull kapacitor@sha256:77d4cdd95302c1d4d4c0cd3586f0cacdaddd09225fdf2bd13a113717c64e2f62
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:344edc7c39090bac569c7646d8d2517005ca93f989c2bb63d9ee2c6f3d506364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139041095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a98bf89d149b266a1233870451f4791c7b09f796aed7d8042b938ec2c72989`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 23 Apr 2024 15:38:09 GMT
ARG RELEASE
# Tue, 23 Apr 2024 15:38:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 15:38:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 15:38:09 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 23 Apr 2024 15:38:09 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Tue, 23 Apr 2024 15:38:09 GMT
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
	-	`sha256:4a023cab5400feb5c1ab725beb8345ddb0e3200314004b56677a5eee2e8c86cf`  
		Last Modified: Sat, 27 Apr 2024 20:07:18 GMT  
		Size: 30.4 MB (30439649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8913270111b4e4a97a0f6a88d63539a5173036496f7353de172d163f320caeea`  
		Last Modified: Thu, 02 May 2024 02:12:34 GMT  
		Size: 7.1 MB (7122522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc084f67b87a702b6b1d40dcc76f0e3973ba0d0070e1cf687ac83e00c726e35c`  
		Last Modified: Thu, 02 May 2024 02:50:13 GMT  
		Size: 35.8 MB (35805922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3eaffe66f1187caa8b2c5f419723406dbe912458a162a72ec7885b803472137`  
		Last Modified: Thu, 02 May 2024 02:50:13 GMT  
		Size: 65.7 MB (65672544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1375c40c8ade0b8e0fae98ad5596b74dd63d18855d487d93c63449c6420c158`  
		Last Modified: Thu, 02 May 2024 02:50:12 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795b94ffe9cf869e946bf353c79c2f04caa2cf9ccdd16d40413ee067ca83e57e`  
		Last Modified: Thu, 02 May 2024 02:50:13 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:7f5d0c96bf19fa796857fcfa46cd7a793539e39ef8408d7a96a04889635a9608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3484496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51144dceff98b7e8f2f53d88234a14480a42a29d6bc667e7028c92ff7cb6a66c`

```dockerfile
```

-	Layers:
	-	`sha256:65598e12e7be241873087fb83f65146e255a0c40b39d85ac77d29842f19a4789`  
		Last Modified: Thu, 02 May 2024 02:50:12 GMT  
		Size: 3.5 MB (3469611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adac4717f9ccb789556a67b4ef6f06b0fd40e37f233b066b64ec366a30ed21b0`  
		Last Modified: Thu, 02 May 2024 02:50:12 GMT  
		Size: 14.9 KB (14885 bytes)  
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
$ docker pull kapacitor@sha256:77d4cdd95302c1d4d4c0cd3586f0cacdaddd09225fdf2bd13a113717c64e2f62
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.6.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:344edc7c39090bac569c7646d8d2517005ca93f989c2bb63d9ee2c6f3d506364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139041095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86a98bf89d149b266a1233870451f4791c7b09f796aed7d8042b938ec2c72989`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 23 Apr 2024 15:38:09 GMT
ARG RELEASE
# Tue, 23 Apr 2024 15:38:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 15:38:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 15:38:09 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 23 Apr 2024 15:38:09 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Tue, 23 Apr 2024 15:38:09 GMT
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
	-	`sha256:4a023cab5400feb5c1ab725beb8345ddb0e3200314004b56677a5eee2e8c86cf`  
		Last Modified: Sat, 27 Apr 2024 20:07:18 GMT  
		Size: 30.4 MB (30439649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8913270111b4e4a97a0f6a88d63539a5173036496f7353de172d163f320caeea`  
		Last Modified: Thu, 02 May 2024 02:12:34 GMT  
		Size: 7.1 MB (7122522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc084f67b87a702b6b1d40dcc76f0e3973ba0d0070e1cf687ac83e00c726e35c`  
		Last Modified: Thu, 02 May 2024 02:50:13 GMT  
		Size: 35.8 MB (35805922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3eaffe66f1187caa8b2c5f419723406dbe912458a162a72ec7885b803472137`  
		Last Modified: Thu, 02 May 2024 02:50:13 GMT  
		Size: 65.7 MB (65672544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1375c40c8ade0b8e0fae98ad5596b74dd63d18855d487d93c63449c6420c158`  
		Last Modified: Thu, 02 May 2024 02:50:12 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795b94ffe9cf869e946bf353c79c2f04caa2cf9ccdd16d40413ee067ca83e57e`  
		Last Modified: Thu, 02 May 2024 02:50:13 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:7f5d0c96bf19fa796857fcfa46cd7a793539e39ef8408d7a96a04889635a9608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3484496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51144dceff98b7e8f2f53d88234a14480a42a29d6bc667e7028c92ff7cb6a66c`

```dockerfile
```

-	Layers:
	-	`sha256:65598e12e7be241873087fb83f65146e255a0c40b39d85ac77d29842f19a4789`  
		Last Modified: Thu, 02 May 2024 02:50:12 GMT  
		Size: 3.5 MB (3469611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adac4717f9ccb789556a67b4ef6f06b0fd40e37f233b066b64ec366a30ed21b0`  
		Last Modified: Thu, 02 May 2024 02:50:12 GMT  
		Size: 14.9 KB (14885 bytes)  
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
$ docker pull kapacitor@sha256:c8bd6f4fe2d3300b2def5833a4a9e55352134b17ebb7c369eebd5cb4133bc0a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:9e29c65d7cce20403fa60fda3bb20676e0114117e00e8e5a1e9db20325364c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144745532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4642c1c8fa504815cc6b07c419ad101a4188ef1b3d7de387a16d108216650816`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 23 Apr 2024 15:38:09 GMT
ARG RELEASE
# Tue, 23 Apr 2024 15:38:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 15:38:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 15:38:09 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 23 Apr 2024 15:38:09 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Tue, 23 Apr 2024 15:38:09 GMT
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
	-	`sha256:4a023cab5400feb5c1ab725beb8345ddb0e3200314004b56677a5eee2e8c86cf`  
		Last Modified: Sat, 27 Apr 2024 20:07:18 GMT  
		Size: 30.4 MB (30439649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8913270111b4e4a97a0f6a88d63539a5173036496f7353de172d163f320caeea`  
		Last Modified: Thu, 02 May 2024 02:12:34 GMT  
		Size: 7.1 MB (7122522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87313fa965417ba391ce07408ccbe83054803a00c49051a7076f51377d29d38c`  
		Last Modified: Thu, 02 May 2024 02:50:20 GMT  
		Size: 35.8 MB (35805929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2007ce9b8eb2f72ba954d2a45eeee5e3bdd7774bf085564f1316c7d9d7c951`  
		Last Modified: Thu, 02 May 2024 02:50:20 GMT  
		Size: 71.4 MB (71376909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa24c840ea8063339dcf9c4de5f56f206deac38bf9133a0b01d5a9b62767c13`  
		Last Modified: Thu, 02 May 2024 02:50:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630de2218858b322d6bdaac40f319dab7df2590b1acc06e12c7ee0a848fe2eee`  
		Last Modified: Thu, 02 May 2024 02:50:19 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:75adf98bc8cb838f54a5e942b519fb25ec3e209c39e33d0d2b5811bb922ef3f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3491333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f264c78c9d797464dde940f947b0505b1c21a94546d182f30754c9d089f1f62`

```dockerfile
```

-	Layers:
	-	`sha256:ac7eb494fe03f671bfe6edead3af707ef9f09c9bd32cc7ba897b3b583c84bb8c`  
		Last Modified: Thu, 02 May 2024 02:50:19 GMT  
		Size: 3.5 MB (3476143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57dc92befd674d97fe979339f40d322e0e500c15f2ae70764c9c8ba8bb3b00c0`  
		Last Modified: Thu, 02 May 2024 02:50:19 GMT  
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
$ docker pull kapacitor@sha256:c8bd6f4fe2d3300b2def5833a4a9e55352134b17ebb7c369eebd5cb4133bc0a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7.4` - linux; amd64

```console
$ docker pull kapacitor@sha256:9e29c65d7cce20403fa60fda3bb20676e0114117e00e8e5a1e9db20325364c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144745532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4642c1c8fa504815cc6b07c419ad101a4188ef1b3d7de387a16d108216650816`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 23 Apr 2024 15:38:09 GMT
ARG RELEASE
# Tue, 23 Apr 2024 15:38:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 15:38:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 15:38:09 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 23 Apr 2024 15:38:09 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Tue, 23 Apr 2024 15:38:09 GMT
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
	-	`sha256:4a023cab5400feb5c1ab725beb8345ddb0e3200314004b56677a5eee2e8c86cf`  
		Last Modified: Sat, 27 Apr 2024 20:07:18 GMT  
		Size: 30.4 MB (30439649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8913270111b4e4a97a0f6a88d63539a5173036496f7353de172d163f320caeea`  
		Last Modified: Thu, 02 May 2024 02:12:34 GMT  
		Size: 7.1 MB (7122522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87313fa965417ba391ce07408ccbe83054803a00c49051a7076f51377d29d38c`  
		Last Modified: Thu, 02 May 2024 02:50:20 GMT  
		Size: 35.8 MB (35805929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2007ce9b8eb2f72ba954d2a45eeee5e3bdd7774bf085564f1316c7d9d7c951`  
		Last Modified: Thu, 02 May 2024 02:50:20 GMT  
		Size: 71.4 MB (71376909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa24c840ea8063339dcf9c4de5f56f206deac38bf9133a0b01d5a9b62767c13`  
		Last Modified: Thu, 02 May 2024 02:50:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630de2218858b322d6bdaac40f319dab7df2590b1acc06e12c7ee0a848fe2eee`  
		Last Modified: Thu, 02 May 2024 02:50:19 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.4` - unknown; unknown

```console
$ docker pull kapacitor@sha256:75adf98bc8cb838f54a5e942b519fb25ec3e209c39e33d0d2b5811bb922ef3f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3491333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f264c78c9d797464dde940f947b0505b1c21a94546d182f30754c9d089f1f62`

```dockerfile
```

-	Layers:
	-	`sha256:ac7eb494fe03f671bfe6edead3af707ef9f09c9bd32cc7ba897b3b583c84bb8c`  
		Last Modified: Thu, 02 May 2024 02:50:19 GMT  
		Size: 3.5 MB (3476143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57dc92befd674d97fe979339f40d322e0e500c15f2ae70764c9c8ba8bb3b00c0`  
		Last Modified: Thu, 02 May 2024 02:50:19 GMT  
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
$ docker pull kapacitor@sha256:c8bd6f4fe2d3300b2def5833a4a9e55352134b17ebb7c369eebd5cb4133bc0a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:9e29c65d7cce20403fa60fda3bb20676e0114117e00e8e5a1e9db20325364c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144745532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4642c1c8fa504815cc6b07c419ad101a4188ef1b3d7de387a16d108216650816`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 23 Apr 2024 15:38:09 GMT
ARG RELEASE
# Tue, 23 Apr 2024 15:38:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Apr 2024 15:38:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Apr 2024 15:38:09 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 23 Apr 2024 15:38:09 GMT
ADD file:a5d32dc2ab15ff0d7dbd72af26e361eb1f3e87a0d29ec3a1ceab24ad7b3e6ba9 in / 
# Tue, 23 Apr 2024 15:38:09 GMT
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
	-	`sha256:4a023cab5400feb5c1ab725beb8345ddb0e3200314004b56677a5eee2e8c86cf`  
		Last Modified: Sat, 27 Apr 2024 20:07:18 GMT  
		Size: 30.4 MB (30439649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8913270111b4e4a97a0f6a88d63539a5173036496f7353de172d163f320caeea`  
		Last Modified: Thu, 02 May 2024 02:12:34 GMT  
		Size: 7.1 MB (7122522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87313fa965417ba391ce07408ccbe83054803a00c49051a7076f51377d29d38c`  
		Last Modified: Thu, 02 May 2024 02:50:20 GMT  
		Size: 35.8 MB (35805929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2007ce9b8eb2f72ba954d2a45eeee5e3bdd7774bf085564f1316c7d9d7c951`  
		Last Modified: Thu, 02 May 2024 02:50:20 GMT  
		Size: 71.4 MB (71376909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa24c840ea8063339dcf9c4de5f56f206deac38bf9133a0b01d5a9b62767c13`  
		Last Modified: Thu, 02 May 2024 02:50:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:630de2218858b322d6bdaac40f319dab7df2590b1acc06e12c7ee0a848fe2eee`  
		Last Modified: Thu, 02 May 2024 02:50:19 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:75adf98bc8cb838f54a5e942b519fb25ec3e209c39e33d0d2b5811bb922ef3f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3491333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f264c78c9d797464dde940f947b0505b1c21a94546d182f30754c9d089f1f62`

```dockerfile
```

-	Layers:
	-	`sha256:ac7eb494fe03f671bfe6edead3af707ef9f09c9bd32cc7ba897b3b583c84bb8c`  
		Last Modified: Thu, 02 May 2024 02:50:19 GMT  
		Size: 3.5 MB (3476143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57dc92befd674d97fe979339f40d322e0e500c15f2ae70764c9c8ba8bb3b00c0`  
		Last Modified: Thu, 02 May 2024 02:50:19 GMT  
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
