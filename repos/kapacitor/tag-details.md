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
$ docker pull kapacitor@sha256:a96f8c9089094cf59319d7b59c0dc46cec98d9706d241df5fc5875460fedc85c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:2ed1c6d15e2756cb99ce5ae2faa7040a590413fc5c139a785ac0ef1c57dfa532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139563415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb176c32e30b4f88f5b5ec9bd64362c65cd6320d66069d55d5493c727de42d4`
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
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
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
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150f13846cf34d9eba8c200d495ef1665928c9e544e261c5a620a9da75d92943`  
		Last Modified: Wed, 05 Jun 2024 04:48:07 GMT  
		Size: 7.1 MB (7122433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8154d98e11b35d03ee339fe73f5d2ecac0be890268642890257a9222e97031d9`  
		Last Modified: Wed, 05 Jun 2024 06:10:50 GMT  
		Size: 36.3 MB (36328704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3f5246a53455cda64adde434be1548db9238450c833e5bf0a55f1afbbda144`  
		Last Modified: Wed, 05 Jun 2024 06:10:51 GMT  
		Size: 65.7 MB (65672539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a98bdc682d3900ac9169f502cfe72ee90a149c0b2f8ff622f6200e1a0930673`  
		Last Modified: Wed, 05 Jun 2024 06:10:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12604c27ae807a1fcb300e3106db4f539263081eefffc927590913618be709ac`  
		Last Modified: Wed, 05 Jun 2024 06:10:50 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:8754bd387dd0a9a78b71510bcd15eabec4396b722e479380e7d788eb660c1f38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3484169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf7aec8a6658f74996175b23f290fe1850b4a5c5917a2bcab1bdc4441702b0b`

```dockerfile
```

-	Layers:
	-	`sha256:b34b40aaad1f299c0c0b2d94e6b43c2b0995252e58835425299f428043f0b613`  
		Last Modified: Wed, 05 Jun 2024 06:10:49 GMT  
		Size: 3.5 MB (3469614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c7341a8fe25a6a9fc967f9b2c906bff21480703af33a6be1597cfb46c770876`  
		Last Modified: Wed, 05 Jun 2024 06:10:49 GMT  
		Size: 14.6 KB (14555 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:51120883ee973fe0dc47c3aace972b0297e212e98fdc3e3ff77ccc41067becd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130703192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e050873e59d0caef311d86d32eab778fadb068155c6f110c75a4db75a9163fd`
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
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
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
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcabcb4a251e4b62ad13d323b297294b00cea852546d1c5100426b1878922d0`  
		Last Modified: Wed, 05 Jun 2024 04:34:56 GMT  
		Size: 7.1 MB (7069836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e72fe24ef2672de47c9b0de8828736f6e91a277f77a934e04492fba463af40`  
		Last Modified: Wed, 05 Jun 2024 15:55:27 GMT  
		Size: 33.6 MB (33559354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f05fe05c08d5a0861b15cbb51d484bdd727a51ad9ec4f4c59d24b1fb262570e`  
		Last Modified: Wed, 05 Jun 2024 15:55:28 GMT  
		Size: 61.7 MB (61671238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97413aec071316cab1a7bff8fa7c3c307b6484dd8df66e659a8923b75e69a65c`  
		Last Modified: Wed, 05 Jun 2024 15:55:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6592856ee4803427cbf6fd0086ff419d5127cbe632019622f678cfa53080f6`  
		Last Modified: Wed, 05 Jun 2024 15:55:27 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:3375b9219d7311ac0c058851b38ac2811784031c0489a13ef21ff95fff664872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3484724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cca57e9f7e8ab8edc3cf3ee17c6ff9fc60dfe79a8af1caedf6dd736f4892c93`

```dockerfile
```

-	Layers:
	-	`sha256:cbf217e915d0802a5d7386a49403f73d65636907d4226391b07e840f12b53658`  
		Last Modified: Wed, 05 Jun 2024 15:55:26 GMT  
		Size: 3.5 MB (3469880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6f57ad7cf2438949db1c69e7881dd539051769f196f691edc183adb2ba22dee`  
		Last Modified: Wed, 05 Jun 2024 15:55:25 GMT  
		Size: 14.8 KB (14844 bytes)  
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
$ docker pull kapacitor@sha256:a96f8c9089094cf59319d7b59c0dc46cec98d9706d241df5fc5875460fedc85c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.6.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:2ed1c6d15e2756cb99ce5ae2faa7040a590413fc5c139a785ac0ef1c57dfa532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139563415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb176c32e30b4f88f5b5ec9bd64362c65cd6320d66069d55d5493c727de42d4`
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
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
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
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150f13846cf34d9eba8c200d495ef1665928c9e544e261c5a620a9da75d92943`  
		Last Modified: Wed, 05 Jun 2024 04:48:07 GMT  
		Size: 7.1 MB (7122433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8154d98e11b35d03ee339fe73f5d2ecac0be890268642890257a9222e97031d9`  
		Last Modified: Wed, 05 Jun 2024 06:10:50 GMT  
		Size: 36.3 MB (36328704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3f5246a53455cda64adde434be1548db9238450c833e5bf0a55f1afbbda144`  
		Last Modified: Wed, 05 Jun 2024 06:10:51 GMT  
		Size: 65.7 MB (65672539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a98bdc682d3900ac9169f502cfe72ee90a149c0b2f8ff622f6200e1a0930673`  
		Last Modified: Wed, 05 Jun 2024 06:10:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12604c27ae807a1fcb300e3106db4f539263081eefffc927590913618be709ac`  
		Last Modified: Wed, 05 Jun 2024 06:10:50 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:8754bd387dd0a9a78b71510bcd15eabec4396b722e479380e7d788eb660c1f38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3484169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf7aec8a6658f74996175b23f290fe1850b4a5c5917a2bcab1bdc4441702b0b`

```dockerfile
```

-	Layers:
	-	`sha256:b34b40aaad1f299c0c0b2d94e6b43c2b0995252e58835425299f428043f0b613`  
		Last Modified: Wed, 05 Jun 2024 06:10:49 GMT  
		Size: 3.5 MB (3469614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c7341a8fe25a6a9fc967f9b2c906bff21480703af33a6be1597cfb46c770876`  
		Last Modified: Wed, 05 Jun 2024 06:10:49 GMT  
		Size: 14.6 KB (14555 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.6.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:51120883ee973fe0dc47c3aace972b0297e212e98fdc3e3ff77ccc41067becd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130703192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e050873e59d0caef311d86d32eab778fadb068155c6f110c75a4db75a9163fd`
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
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
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
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcabcb4a251e4b62ad13d323b297294b00cea852546d1c5100426b1878922d0`  
		Last Modified: Wed, 05 Jun 2024 04:34:56 GMT  
		Size: 7.1 MB (7069836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e72fe24ef2672de47c9b0de8828736f6e91a277f77a934e04492fba463af40`  
		Last Modified: Wed, 05 Jun 2024 15:55:27 GMT  
		Size: 33.6 MB (33559354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f05fe05c08d5a0861b15cbb51d484bdd727a51ad9ec4f4c59d24b1fb262570e`  
		Last Modified: Wed, 05 Jun 2024 15:55:28 GMT  
		Size: 61.7 MB (61671238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97413aec071316cab1a7bff8fa7c3c307b6484dd8df66e659a8923b75e69a65c`  
		Last Modified: Wed, 05 Jun 2024 15:55:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6592856ee4803427cbf6fd0086ff419d5127cbe632019622f678cfa53080f6`  
		Last Modified: Wed, 05 Jun 2024 15:55:27 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:3375b9219d7311ac0c058851b38ac2811784031c0489a13ef21ff95fff664872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3484724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cca57e9f7e8ab8edc3cf3ee17c6ff9fc60dfe79a8af1caedf6dd736f4892c93`

```dockerfile
```

-	Layers:
	-	`sha256:cbf217e915d0802a5d7386a49403f73d65636907d4226391b07e840f12b53658`  
		Last Modified: Wed, 05 Jun 2024 15:55:26 GMT  
		Size: 3.5 MB (3469880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6f57ad7cf2438949db1c69e7881dd539051769f196f691edc183adb2ba22dee`  
		Last Modified: Wed, 05 Jun 2024 15:55:25 GMT  
		Size: 14.8 KB (14844 bytes)  
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
$ docker pull kapacitor@sha256:66456a22b94af63f839f27b7fc6d912cfd1ec87b6643d78d62bbe7b7e41efc64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:e3018a8439417ac955448a156b128ff299f31ff2d19975b0a9625e4359a71f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145267869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b8dd6c94dd237f3eff59f4b66708d679318d96d778ff2bdc5147a69d0048e7`
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
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
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
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150f13846cf34d9eba8c200d495ef1665928c9e544e261c5a620a9da75d92943`  
		Last Modified: Wed, 05 Jun 2024 04:48:07 GMT  
		Size: 7.1 MB (7122433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5be799cda588480c8300d57f69898f300466dae9eed73a1251b4c1d5a5005ea`  
		Last Modified: Wed, 05 Jun 2024 06:10:54 GMT  
		Size: 36.3 MB (36328715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db34f1ed1e53e0f2aa29d6edadfdb9b335d46bcf690d82039ee812272203cdfe`  
		Last Modified: Wed, 05 Jun 2024 06:10:55 GMT  
		Size: 71.4 MB (71376918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa72120dc2b93b6106ec5d17dcd5b6c133ba52245ef251acac1cd1bd133c4499`  
		Last Modified: Wed, 05 Jun 2024 06:10:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb3e6f643b101eae42db42901637907ed9631737a6ea9c932740a105fbb629a`  
		Last Modified: Wed, 05 Jun 2024 06:10:53 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:9294f45146b3dbfd2ac0f1f10b4370bc8d0502d704bd94835be0a7b232045783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3491005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e431049eebc769bcf1b8a800c8d0a11a7d56984fb98d474b9a55c38cffef2892`

```dockerfile
```

-	Layers:
	-	`sha256:d7da001761cde84cc702eb55bfa0270c5ef2c84e718aafc27722891cb2e997b5`  
		Last Modified: Wed, 05 Jun 2024 06:10:53 GMT  
		Size: 3.5 MB (3476146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d56609f319a72df820f7defe2bd8f9ea5805e3cb5f9be7ab7e6cfd836689ff9`  
		Last Modified: Wed, 05 Jun 2024 06:10:52 GMT  
		Size: 14.9 KB (14859 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:79c855874348360b6fe7c7344134ebb50d91754811985c778697079bd7bc0df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136127910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7e21b880802e167749d51a73f1322001a152a18bbe60c8cfb9a8f4925328cc`
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
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
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
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcabcb4a251e4b62ad13d323b297294b00cea852546d1c5100426b1878922d0`  
		Last Modified: Wed, 05 Jun 2024 04:34:56 GMT  
		Size: 7.1 MB (7069836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e72fe24ef2672de47c9b0de8828736f6e91a277f77a934e04492fba463af40`  
		Last Modified: Wed, 05 Jun 2024 15:55:27 GMT  
		Size: 33.6 MB (33559354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c996fe8b0649ef003b0955867b1ec03010f4da338f789d3640ca290bf5cdc35`  
		Last Modified: Wed, 05 Jun 2024 15:56:01 GMT  
		Size: 67.1 MB (67095892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ae4865a916c0de804eee5cce5c9d4de72d290a19f551f92bd34ed7785e0063`  
		Last Modified: Wed, 05 Jun 2024 15:55:58 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cca329916ad4c166d5e16607c82e3213f4240196ba223e84bb9a9e3747a5315`  
		Last Modified: Wed, 05 Jun 2024 15:55:58 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:cf14857f602e65b40ec9bf4618af7aa5d23e70aedec3682553a75aa9ba8198f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3490933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40656bdd81249c72eb8c0439c625a0ea346e4e100a557d973a440691d1b60962`

```dockerfile
```

-	Layers:
	-	`sha256:e9d62cde022322d52cbaaa864f04c3769eabbbccb44d771f0a80925cef13f7d3`  
		Last Modified: Wed, 05 Jun 2024 15:55:59 GMT  
		Size: 3.5 MB (3475772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebd9b3b94dac9ad5160636a18464ff9af90e098286a0a50e521cf2fc980702c0`  
		Last Modified: Wed, 05 Jun 2024 15:55:58 GMT  
		Size: 15.2 KB (15161 bytes)  
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
$ docker pull kapacitor@sha256:66456a22b94af63f839f27b7fc6d912cfd1ec87b6643d78d62bbe7b7e41efc64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7.4` - linux; amd64

```console
$ docker pull kapacitor@sha256:e3018a8439417ac955448a156b128ff299f31ff2d19975b0a9625e4359a71f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145267869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b8dd6c94dd237f3eff59f4b66708d679318d96d778ff2bdc5147a69d0048e7`
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
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
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
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150f13846cf34d9eba8c200d495ef1665928c9e544e261c5a620a9da75d92943`  
		Last Modified: Wed, 05 Jun 2024 04:48:07 GMT  
		Size: 7.1 MB (7122433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5be799cda588480c8300d57f69898f300466dae9eed73a1251b4c1d5a5005ea`  
		Last Modified: Wed, 05 Jun 2024 06:10:54 GMT  
		Size: 36.3 MB (36328715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db34f1ed1e53e0f2aa29d6edadfdb9b335d46bcf690d82039ee812272203cdfe`  
		Last Modified: Wed, 05 Jun 2024 06:10:55 GMT  
		Size: 71.4 MB (71376918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa72120dc2b93b6106ec5d17dcd5b6c133ba52245ef251acac1cd1bd133c4499`  
		Last Modified: Wed, 05 Jun 2024 06:10:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb3e6f643b101eae42db42901637907ed9631737a6ea9c932740a105fbb629a`  
		Last Modified: Wed, 05 Jun 2024 06:10:53 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.4` - unknown; unknown

```console
$ docker pull kapacitor@sha256:9294f45146b3dbfd2ac0f1f10b4370bc8d0502d704bd94835be0a7b232045783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3491005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e431049eebc769bcf1b8a800c8d0a11a7d56984fb98d474b9a55c38cffef2892`

```dockerfile
```

-	Layers:
	-	`sha256:d7da001761cde84cc702eb55bfa0270c5ef2c84e718aafc27722891cb2e997b5`  
		Last Modified: Wed, 05 Jun 2024 06:10:53 GMT  
		Size: 3.5 MB (3476146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d56609f319a72df820f7defe2bd8f9ea5805e3cb5f9be7ab7e6cfd836689ff9`  
		Last Modified: Wed, 05 Jun 2024 06:10:52 GMT  
		Size: 14.9 KB (14859 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7.4` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:79c855874348360b6fe7c7344134ebb50d91754811985c778697079bd7bc0df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136127910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7e21b880802e167749d51a73f1322001a152a18bbe60c8cfb9a8f4925328cc`
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
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
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
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcabcb4a251e4b62ad13d323b297294b00cea852546d1c5100426b1878922d0`  
		Last Modified: Wed, 05 Jun 2024 04:34:56 GMT  
		Size: 7.1 MB (7069836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e72fe24ef2672de47c9b0de8828736f6e91a277f77a934e04492fba463af40`  
		Last Modified: Wed, 05 Jun 2024 15:55:27 GMT  
		Size: 33.6 MB (33559354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c996fe8b0649ef003b0955867b1ec03010f4da338f789d3640ca290bf5cdc35`  
		Last Modified: Wed, 05 Jun 2024 15:56:01 GMT  
		Size: 67.1 MB (67095892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ae4865a916c0de804eee5cce5c9d4de72d290a19f551f92bd34ed7785e0063`  
		Last Modified: Wed, 05 Jun 2024 15:55:58 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cca329916ad4c166d5e16607c82e3213f4240196ba223e84bb9a9e3747a5315`  
		Last Modified: Wed, 05 Jun 2024 15:55:58 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.4` - unknown; unknown

```console
$ docker pull kapacitor@sha256:cf14857f602e65b40ec9bf4618af7aa5d23e70aedec3682553a75aa9ba8198f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3490933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40656bdd81249c72eb8c0439c625a0ea346e4e100a557d973a440691d1b60962`

```dockerfile
```

-	Layers:
	-	`sha256:e9d62cde022322d52cbaaa864f04c3769eabbbccb44d771f0a80925cef13f7d3`  
		Last Modified: Wed, 05 Jun 2024 15:55:59 GMT  
		Size: 3.5 MB (3475772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebd9b3b94dac9ad5160636a18464ff9af90e098286a0a50e521cf2fc980702c0`  
		Last Modified: Wed, 05 Jun 2024 15:55:58 GMT  
		Size: 15.2 KB (15161 bytes)  
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
$ docker pull kapacitor@sha256:66456a22b94af63f839f27b7fc6d912cfd1ec87b6643d78d62bbe7b7e41efc64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:e3018a8439417ac955448a156b128ff299f31ff2d19975b0a9625e4359a71f28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145267869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b8dd6c94dd237f3eff59f4b66708d679318d96d778ff2bdc5147a69d0048e7`
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
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
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
	-	`sha256:2ec76a50fe7c8d5db9ec25590b9217e14e3920513c6e7b5be55db72a16b55f7c`  
		Last Modified: Fri, 31 May 2024 03:03:19 GMT  
		Size: 30.4 MB (30439283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150f13846cf34d9eba8c200d495ef1665928c9e544e261c5a620a9da75d92943`  
		Last Modified: Wed, 05 Jun 2024 04:48:07 GMT  
		Size: 7.1 MB (7122433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5be799cda588480c8300d57f69898f300466dae9eed73a1251b4c1d5a5005ea`  
		Last Modified: Wed, 05 Jun 2024 06:10:54 GMT  
		Size: 36.3 MB (36328715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db34f1ed1e53e0f2aa29d6edadfdb9b335d46bcf690d82039ee812272203cdfe`  
		Last Modified: Wed, 05 Jun 2024 06:10:55 GMT  
		Size: 71.4 MB (71376918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa72120dc2b93b6106ec5d17dcd5b6c133ba52245ef251acac1cd1bd133c4499`  
		Last Modified: Wed, 05 Jun 2024 06:10:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb3e6f643b101eae42db42901637907ed9631737a6ea9c932740a105fbb629a`  
		Last Modified: Wed, 05 Jun 2024 06:10:53 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:9294f45146b3dbfd2ac0f1f10b4370bc8d0502d704bd94835be0a7b232045783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3491005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e431049eebc769bcf1b8a800c8d0a11a7d56984fb98d474b9a55c38cffef2892`

```dockerfile
```

-	Layers:
	-	`sha256:d7da001761cde84cc702eb55bfa0270c5ef2c84e718aafc27722891cb2e997b5`  
		Last Modified: Wed, 05 Jun 2024 06:10:53 GMT  
		Size: 3.5 MB (3476146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d56609f319a72df820f7defe2bd8f9ea5805e3cb5f9be7ab7e6cfd836689ff9`  
		Last Modified: Wed, 05 Jun 2024 06:10:52 GMT  
		Size: 14.9 KB (14859 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:79c855874348360b6fe7c7344134ebb50d91754811985c778697079bd7bc0df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136127910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7e21b880802e167749d51a73f1322001a152a18bbe60c8cfb9a8f4925328cc`
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
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
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
	-	`sha256:2741160b46783cff15aad1d825ac5be29d819aaa773f4270d133fb57683fbbd0`  
		Last Modified: Mon, 03 Jun 2024 13:49:15 GMT  
		Size: 28.4 MB (28402306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcabcb4a251e4b62ad13d323b297294b00cea852546d1c5100426b1878922d0`  
		Last Modified: Wed, 05 Jun 2024 04:34:56 GMT  
		Size: 7.1 MB (7069836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e72fe24ef2672de47c9b0de8828736f6e91a277f77a934e04492fba463af40`  
		Last Modified: Wed, 05 Jun 2024 15:55:27 GMT  
		Size: 33.6 MB (33559354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c996fe8b0649ef003b0955867b1ec03010f4da338f789d3640ca290bf5cdc35`  
		Last Modified: Wed, 05 Jun 2024 15:56:01 GMT  
		Size: 67.1 MB (67095892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ae4865a916c0de804eee5cce5c9d4de72d290a19f551f92bd34ed7785e0063`  
		Last Modified: Wed, 05 Jun 2024 15:55:58 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cca329916ad4c166d5e16607c82e3213f4240196ba223e84bb9a9e3747a5315`  
		Last Modified: Wed, 05 Jun 2024 15:55:58 GMT  
		Size: 296.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:cf14857f602e65b40ec9bf4618af7aa5d23e70aedec3682553a75aa9ba8198f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3490933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40656bdd81249c72eb8c0439c625a0ea346e4e100a557d973a440691d1b60962`

```dockerfile
```

-	Layers:
	-	`sha256:e9d62cde022322d52cbaaa864f04c3769eabbbccb44d771f0a80925cef13f7d3`  
		Last Modified: Wed, 05 Jun 2024 15:55:59 GMT  
		Size: 3.5 MB (3475772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebd9b3b94dac9ad5160636a18464ff9af90e098286a0a50e521cf2fc980702c0`  
		Last Modified: Wed, 05 Jun 2024 15:55:58 GMT  
		Size: 15.2 KB (15161 bytes)  
		MIME: application/vnd.in-toto+json
