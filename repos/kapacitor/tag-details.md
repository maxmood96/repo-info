<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.6`](#kapacitor16)
-	[`kapacitor:1.6-alpine`](#kapacitor16-alpine)
-	[`kapacitor:1.6.6`](#kapacitor166)
-	[`kapacitor:1.6.6-alpine`](#kapacitor166-alpine)
-	[`kapacitor:1.7`](#kapacitor17)
-	[`kapacitor:1.7-alpine`](#kapacitor17-alpine)
-	[`kapacitor:1.7.2`](#kapacitor172)
-	[`kapacitor:1.7.2-alpine`](#kapacitor172-alpine)
-	[`kapacitor:alpine`](#kapacitoralpine)
-	[`kapacitor:latest`](#kapacitorlatest)

## `kapacitor:1.6`

```console
$ docker pull kapacitor@sha256:a422edcb391128aadd1557383dcee19bf01682d5eb1f0884c3f20be9835d96bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:1.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:039114952e142a6098712c968fc7ad0dc9904509cc1d75ebc608ed860ff729c8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138813166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c36704571880a64a336f3b2c4820e2c20eb6b2960a173e37bd2063c631a98e53`
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
# Tue, 16 Apr 2024 08:35:25 GMT
ENV KAPACITOR_VERSION=1.6.6
# Tue, 16 Apr 2024 08:35:30 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 16 Apr 2024 08:35:31 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 16 Apr 2024 08:35:31 GMT
EXPOSE 9092
# Tue, 16 Apr 2024 08:35:31 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 16 Apr 2024 08:35:31 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 16 Apr 2024 08:35:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 08:35:31 GMT
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
	-	`sha256:e91e50296299115a77a2509bc815a1b258c4f23d8830d179d9e89f8e8ae29dc5`  
		Last Modified: Tue, 16 Apr 2024 08:36:09 GMT  
		Size: 65.7 MB (65672997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a7d687c4ff065151fefa7b8113106b874e6d5dfde405f027396dfd40b994d6`  
		Last Modified: Tue, 16 Apr 2024 08:36:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:125ab2ac41bcd2c554dd0bb0d7d5e99f43a31c103b74513cc673fb05f4b6f149`  
		Last Modified: Tue, 16 Apr 2024 08:36:01 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:45e616f6edf38ef84fde114e87a85505b5c6d602b89a663542ffd4a9dbb9fdcb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129999598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c72d972a236171fb6b880ba18c623d3661f839be965890498469ff0ca13e679f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 01:55:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:27:21 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 16 Apr 2024 05:27:21 GMT
ENV KAPACITOR_VERSION=1.6.6
# Tue, 16 Apr 2024 05:27:31 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 16 Apr 2024 05:27:32 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 16 Apr 2024 05:27:32 GMT
EXPOSE 9092
# Tue, 16 Apr 2024 05:27:32 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 16 Apr 2024 05:27:32 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 16 Apr 2024 05:27:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 05:27:32 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895c42abeb4df7fe7e0293498c3dacd85ab82f5b16b6a3b5ef980731419983b2`  
		Last Modified: Tue, 16 Apr 2024 02:11:19 GMT  
		Size: 7.1 MB (7068419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509b748565ee4f38df11041e760b533e2480b107e72a61a3962a7d52a7d35c3d`  
		Last Modified: Tue, 16 Apr 2024 05:27:54 GMT  
		Size: 32.9 MB (32860037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e59b9ce11674de6bf51b21d6f25b4ca5fc3c3705cac92869dff9c72b8451018`  
		Last Modified: Tue, 16 Apr 2024 05:27:57 GMT  
		Size: 61.7 MB (61670387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f478fb63e491cc11b422386404604b93d2dab137863f400e0c92a3405d9f4eec`  
		Last Modified: Tue, 16 Apr 2024 05:27:52 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8e3370f8ada2a8e124902d1ed864d2126379798d6168e2cd47a1697ecc9384`  
		Last Modified: Tue, 16 Apr 2024 05:27:51 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.6-alpine`

```console
$ docker pull kapacitor@sha256:0d94e0e894983869b098b752b7cf9795a321f03d13b4225237e63c3fb0a010af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:09ca22830bc4ab483c3baf63de8d600e67fbce8eaa6897ae82d7253ce2a2f051
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68673653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1ce24b2e48f7c4a718b28cf1f0a08db3f9c3bfa8b1b1aeb5eb1d7f759df2e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:40:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 08:40:42 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 16 Mar 2024 08:40:42 GMT
ENV KAPACITOR_VERSION=1.6.6
# Sat, 16 Mar 2024 08:40:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 16 Mar 2024 08:40:50 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 16 Mar 2024 08:40:50 GMT
EXPOSE 9092
# Sat, 16 Mar 2024 08:40:50 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 16 Mar 2024 08:40:50 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Sat, 16 Mar 2024 08:40:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 08:40:50 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9053983e91fabe0346bbf777708c8d6730da66d0369d8eb60028e5ebeb54ed`  
		Last Modified: Sat, 16 Mar 2024 08:41:16 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2a80141b499f1b8d6d7d1fcc5f2c0ffe586561e759af2959a331c3beda3467`  
		Last Modified: Sat, 16 Mar 2024 08:41:16 GMT  
		Size: 284.9 KB (284906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f428062761aca8eb2204eca2683dc0e98cb621670943a3fa255f75773e0794`  
		Last Modified: Sat, 16 Mar 2024 08:41:23 GMT  
		Size: 65.6 MB (65580179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a8f5339498d1101269c4202f353f5f90ec7d67f0deb69f549ac790489f602d`  
		Last Modified: Sat, 16 Mar 2024 08:41:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d573df60a2f35e472c32099c11e7fcaeb6c93a97f3ca461e189d33d9dc05e394`  
		Last Modified: Sat, 16 Mar 2024 08:41:16 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.6.6`

```console
$ docker pull kapacitor@sha256:a422edcb391128aadd1557383dcee19bf01682d5eb1f0884c3f20be9835d96bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:1.6.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:039114952e142a6098712c968fc7ad0dc9904509cc1d75ebc608ed860ff729c8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138813166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c36704571880a64a336f3b2c4820e2c20eb6b2960a173e37bd2063c631a98e53`
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
# Tue, 16 Apr 2024 08:35:25 GMT
ENV KAPACITOR_VERSION=1.6.6
# Tue, 16 Apr 2024 08:35:30 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 16 Apr 2024 08:35:31 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 16 Apr 2024 08:35:31 GMT
EXPOSE 9092
# Tue, 16 Apr 2024 08:35:31 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 16 Apr 2024 08:35:31 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 16 Apr 2024 08:35:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 08:35:31 GMT
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
	-	`sha256:e91e50296299115a77a2509bc815a1b258c4f23d8830d179d9e89f8e8ae29dc5`  
		Last Modified: Tue, 16 Apr 2024 08:36:09 GMT  
		Size: 65.7 MB (65672997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0a7d687c4ff065151fefa7b8113106b874e6d5dfde405f027396dfd40b994d6`  
		Last Modified: Tue, 16 Apr 2024 08:36:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:125ab2ac41bcd2c554dd0bb0d7d5e99f43a31c103b74513cc673fb05f4b6f149`  
		Last Modified: Tue, 16 Apr 2024 08:36:01 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.6.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:45e616f6edf38ef84fde114e87a85505b5c6d602b89a663542ffd4a9dbb9fdcb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129999598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c72d972a236171fb6b880ba18c623d3661f839be965890498469ff0ca13e679f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 01:55:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:27:21 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 16 Apr 2024 05:27:21 GMT
ENV KAPACITOR_VERSION=1.6.6
# Tue, 16 Apr 2024 05:27:31 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 16 Apr 2024 05:27:32 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 16 Apr 2024 05:27:32 GMT
EXPOSE 9092
# Tue, 16 Apr 2024 05:27:32 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 16 Apr 2024 05:27:32 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 16 Apr 2024 05:27:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 05:27:32 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895c42abeb4df7fe7e0293498c3dacd85ab82f5b16b6a3b5ef980731419983b2`  
		Last Modified: Tue, 16 Apr 2024 02:11:19 GMT  
		Size: 7.1 MB (7068419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509b748565ee4f38df11041e760b533e2480b107e72a61a3962a7d52a7d35c3d`  
		Last Modified: Tue, 16 Apr 2024 05:27:54 GMT  
		Size: 32.9 MB (32860037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e59b9ce11674de6bf51b21d6f25b4ca5fc3c3705cac92869dff9c72b8451018`  
		Last Modified: Tue, 16 Apr 2024 05:27:57 GMT  
		Size: 61.7 MB (61670387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f478fb63e491cc11b422386404604b93d2dab137863f400e0c92a3405d9f4eec`  
		Last Modified: Tue, 16 Apr 2024 05:27:52 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8e3370f8ada2a8e124902d1ed864d2126379798d6168e2cd47a1697ecc9384`  
		Last Modified: Tue, 16 Apr 2024 05:27:51 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.6.6-alpine`

```console
$ docker pull kapacitor@sha256:0d94e0e894983869b098b752b7cf9795a321f03d13b4225237e63c3fb0a010af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.6.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:09ca22830bc4ab483c3baf63de8d600e67fbce8eaa6897ae82d7253ce2a2f051
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68673653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1ce24b2e48f7c4a718b28cf1f0a08db3f9c3bfa8b1b1aeb5eb1d7f759df2e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:40:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 08:40:42 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 16 Mar 2024 08:40:42 GMT
ENV KAPACITOR_VERSION=1.6.6
# Sat, 16 Mar 2024 08:40:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 16 Mar 2024 08:40:50 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 16 Mar 2024 08:40:50 GMT
EXPOSE 9092
# Sat, 16 Mar 2024 08:40:50 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 16 Mar 2024 08:40:50 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Sat, 16 Mar 2024 08:40:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 08:40:50 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9053983e91fabe0346bbf777708c8d6730da66d0369d8eb60028e5ebeb54ed`  
		Last Modified: Sat, 16 Mar 2024 08:41:16 GMT  
		Size: 277.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2a80141b499f1b8d6d7d1fcc5f2c0ffe586561e759af2959a331c3beda3467`  
		Last Modified: Sat, 16 Mar 2024 08:41:16 GMT  
		Size: 284.9 KB (284906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f428062761aca8eb2204eca2683dc0e98cb621670943a3fa255f75773e0794`  
		Last Modified: Sat, 16 Mar 2024 08:41:23 GMT  
		Size: 65.6 MB (65580179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a8f5339498d1101269c4202f353f5f90ec7d67f0deb69f549ac790489f602d`  
		Last Modified: Sat, 16 Mar 2024 08:41:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d573df60a2f35e472c32099c11e7fcaeb6c93a97f3ca461e189d33d9dc05e394`  
		Last Modified: Sat, 16 Mar 2024 08:41:16 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.7`

```console
$ docker pull kapacitor@sha256:343d4b05070a2f96e15b6df58b1e6d940d2c25a975b212f2749aaae284220ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:1.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:913027953f2d843dbefd33f76221b455b33e2a8b27b12c7ac5d83aa8793bb121
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142788105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa6a0dfcf8158ef45be9e14968a5a8619c78dedfc06b173c1bd8b43443c3558`
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
# Tue, 16 Apr 2024 08:35:39 GMT
ENV KAPACITOR_VERSION=1.7.2
# Tue, 16 Apr 2024 08:35:46 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 16 Apr 2024 08:35:46 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 16 Apr 2024 08:35:46 GMT
EXPOSE 9092
# Tue, 16 Apr 2024 08:35:46 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 16 Apr 2024 08:35:46 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 16 Apr 2024 08:35:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 08:35:47 GMT
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
	-	`sha256:3247d4e87d041433e4cbc81ecba5791a2e9121c091ebb82688c9d1f90bc7191e`  
		Last Modified: Tue, 16 Apr 2024 08:36:27 GMT  
		Size: 69.6 MB (69647935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c368c6e492610024afdbc9fc290ad95623c42c4e690f34201b77481f43ef7e8`  
		Last Modified: Tue, 16 Apr 2024 08:36:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a246c5bd7aad48348ffa4a0d641d4cfb8580cc0e7b17b41a8ddbb5ab4242f33`  
		Last Modified: Tue, 16 Apr 2024 08:36:18 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:ce15093189ca1d230b33de84c905ba2672d905ceef27df8ff17bb580c465ad43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133477720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff359bc276a9d40705834307c0d0d9a25e8cbc2d0de20949140ffa4b27f1f15`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 01:55:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:27:21 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 16 Apr 2024 05:27:35 GMT
ENV KAPACITOR_VERSION=1.7.2
# Tue, 16 Apr 2024 05:27:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 16 Apr 2024 05:27:42 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 16 Apr 2024 05:27:42 GMT
EXPOSE 9092
# Tue, 16 Apr 2024 05:27:42 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 16 Apr 2024 05:27:42 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 16 Apr 2024 05:27:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 05:27:42 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895c42abeb4df7fe7e0293498c3dacd85ab82f5b16b6a3b5ef980731419983b2`  
		Last Modified: Tue, 16 Apr 2024 02:11:19 GMT  
		Size: 7.1 MB (7068419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509b748565ee4f38df11041e760b533e2480b107e72a61a3962a7d52a7d35c3d`  
		Last Modified: Tue, 16 Apr 2024 05:27:54 GMT  
		Size: 32.9 MB (32860037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6edf52129f51f008f7509fd709cbe1ec2829801333c4e423156582d83d5fbd6`  
		Last Modified: Tue, 16 Apr 2024 05:28:12 GMT  
		Size: 65.1 MB (65148511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e4729782adc6e76b2a981328e64f0dad5b03408ed75e98ecd24b2e04f7eed2`  
		Last Modified: Tue, 16 Apr 2024 05:28:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f643b4370280edd1cdf7720ef21345a578ae3075038d83ed4d056029d95523`  
		Last Modified: Tue, 16 Apr 2024 05:28:06 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.7-alpine`

```console
$ docker pull kapacitor@sha256:de920d976943324f0864c43f6604ef3fef3289de86e438bacc1cc7303d4f0ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.7-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:15fe2710813a436e9228237dd1da7e78c0699eddf25bd3e78553be06bda2903e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73255026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a76d1c0d1e9febbaf01821ba71af05f44cec841c985b97373fa4a071a41b1e9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 03:20:47 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 16 Mar 2024 08:40:57 GMT
ENV KAPACITOR_VERSION=1.7.2
# Sat, 16 Mar 2024 08:41:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 16 Mar 2024 08:41:04 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 16 Mar 2024 08:41:04 GMT
EXPOSE 9092
# Sat, 16 Mar 2024 08:41:04 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 16 Mar 2024 08:41:04 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Sat, 16 Mar 2024 08:41:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 08:41:04 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec84f8c4b4c91fcb32de58f4c3ad4f074277a222c69804bc60e3dc52fb9edb0`  
		Last Modified: Sat, 16 Mar 2024 03:21:48 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377633fb5fdd007c0931220a6d839bb8682cccad8022dfb9d9a6a13f48bbcb31`  
		Last Modified: Sat, 16 Mar 2024 03:21:47 GMT  
		Size: 284.7 KB (284701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66604b48a56949070909cf36add8341782765583ffee33dab4f951d58e1f0032`  
		Last Modified: Sat, 16 Mar 2024 08:41:40 GMT  
		Size: 69.6 MB (69567046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed37ba0f96ce248f221fa22342b8a7122705ce4f59695cdaaddfc7b083d38ed8`  
		Last Modified: Sat, 16 Mar 2024 08:41:32 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0ef027374ae9de66a89225afc876a3984220ca369d21394c2a20f2705e0a81`  
		Last Modified: Sat, 16 Mar 2024 08:41:32 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.7.2`

```console
$ docker pull kapacitor@sha256:343d4b05070a2f96e15b6df58b1e6d940d2c25a975b212f2749aaae284220ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:1.7.2` - linux; amd64

```console
$ docker pull kapacitor@sha256:913027953f2d843dbefd33f76221b455b33e2a8b27b12c7ac5d83aa8793bb121
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142788105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa6a0dfcf8158ef45be9e14968a5a8619c78dedfc06b173c1bd8b43443c3558`
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
# Tue, 16 Apr 2024 08:35:39 GMT
ENV KAPACITOR_VERSION=1.7.2
# Tue, 16 Apr 2024 08:35:46 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 16 Apr 2024 08:35:46 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 16 Apr 2024 08:35:46 GMT
EXPOSE 9092
# Tue, 16 Apr 2024 08:35:46 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 16 Apr 2024 08:35:46 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 16 Apr 2024 08:35:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 08:35:47 GMT
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
	-	`sha256:3247d4e87d041433e4cbc81ecba5791a2e9121c091ebb82688c9d1f90bc7191e`  
		Last Modified: Tue, 16 Apr 2024 08:36:27 GMT  
		Size: 69.6 MB (69647935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c368c6e492610024afdbc9fc290ad95623c42c4e690f34201b77481f43ef7e8`  
		Last Modified: Tue, 16 Apr 2024 08:36:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a246c5bd7aad48348ffa4a0d641d4cfb8580cc0e7b17b41a8ddbb5ab4242f33`  
		Last Modified: Tue, 16 Apr 2024 08:36:18 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.7.2` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:ce15093189ca1d230b33de84c905ba2672d905ceef27df8ff17bb580c465ad43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133477720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff359bc276a9d40705834307c0d0d9a25e8cbc2d0de20949140ffa4b27f1f15`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 01:55:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:27:21 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 16 Apr 2024 05:27:35 GMT
ENV KAPACITOR_VERSION=1.7.2
# Tue, 16 Apr 2024 05:27:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 16 Apr 2024 05:27:42 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 16 Apr 2024 05:27:42 GMT
EXPOSE 9092
# Tue, 16 Apr 2024 05:27:42 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 16 Apr 2024 05:27:42 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 16 Apr 2024 05:27:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 05:27:42 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895c42abeb4df7fe7e0293498c3dacd85ab82f5b16b6a3b5ef980731419983b2`  
		Last Modified: Tue, 16 Apr 2024 02:11:19 GMT  
		Size: 7.1 MB (7068419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509b748565ee4f38df11041e760b533e2480b107e72a61a3962a7d52a7d35c3d`  
		Last Modified: Tue, 16 Apr 2024 05:27:54 GMT  
		Size: 32.9 MB (32860037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6edf52129f51f008f7509fd709cbe1ec2829801333c4e423156582d83d5fbd6`  
		Last Modified: Tue, 16 Apr 2024 05:28:12 GMT  
		Size: 65.1 MB (65148511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e4729782adc6e76b2a981328e64f0dad5b03408ed75e98ecd24b2e04f7eed2`  
		Last Modified: Tue, 16 Apr 2024 05:28:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f643b4370280edd1cdf7720ef21345a578ae3075038d83ed4d056029d95523`  
		Last Modified: Tue, 16 Apr 2024 05:28:06 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.7.2-alpine`

```console
$ docker pull kapacitor@sha256:de920d976943324f0864c43f6604ef3fef3289de86e438bacc1cc7303d4f0ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.7.2-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:15fe2710813a436e9228237dd1da7e78c0699eddf25bd3e78553be06bda2903e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73255026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a76d1c0d1e9febbaf01821ba71af05f44cec841c985b97373fa4a071a41b1e9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 03:20:47 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 16 Mar 2024 08:40:57 GMT
ENV KAPACITOR_VERSION=1.7.2
# Sat, 16 Mar 2024 08:41:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 16 Mar 2024 08:41:04 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 16 Mar 2024 08:41:04 GMT
EXPOSE 9092
# Sat, 16 Mar 2024 08:41:04 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 16 Mar 2024 08:41:04 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Sat, 16 Mar 2024 08:41:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 08:41:04 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec84f8c4b4c91fcb32de58f4c3ad4f074277a222c69804bc60e3dc52fb9edb0`  
		Last Modified: Sat, 16 Mar 2024 03:21:48 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377633fb5fdd007c0931220a6d839bb8682cccad8022dfb9d9a6a13f48bbcb31`  
		Last Modified: Sat, 16 Mar 2024 03:21:47 GMT  
		Size: 284.7 KB (284701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66604b48a56949070909cf36add8341782765583ffee33dab4f951d58e1f0032`  
		Last Modified: Sat, 16 Mar 2024 08:41:40 GMT  
		Size: 69.6 MB (69567046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed37ba0f96ce248f221fa22342b8a7122705ce4f59695cdaaddfc7b083d38ed8`  
		Last Modified: Sat, 16 Mar 2024 08:41:32 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0ef027374ae9de66a89225afc876a3984220ca369d21394c2a20f2705e0a81`  
		Last Modified: Sat, 16 Mar 2024 08:41:32 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:de920d976943324f0864c43f6604ef3fef3289de86e438bacc1cc7303d4f0ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:15fe2710813a436e9228237dd1da7e78c0699eddf25bd3e78553be06bda2903e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73255026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a76d1c0d1e9febbaf01821ba71af05f44cec841c985b97373fa4a071a41b1e9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 03:20:47 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Sat, 16 Mar 2024 08:40:57 GMT
ENV KAPACITOR_VERSION=1.7.2
# Sat, 16 Mar 2024 08:41:04 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Sat, 16 Mar 2024 08:41:04 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 16 Mar 2024 08:41:04 GMT
EXPOSE 9092
# Sat, 16 Mar 2024 08:41:04 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 16 Mar 2024 08:41:04 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Sat, 16 Mar 2024 08:41:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 08:41:04 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec84f8c4b4c91fcb32de58f4c3ad4f074277a222c69804bc60e3dc52fb9edb0`  
		Last Modified: Sat, 16 Mar 2024 03:21:48 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377633fb5fdd007c0931220a6d839bb8682cccad8022dfb9d9a6a13f48bbcb31`  
		Last Modified: Sat, 16 Mar 2024 03:21:47 GMT  
		Size: 284.7 KB (284701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66604b48a56949070909cf36add8341782765583ffee33dab4f951d58e1f0032`  
		Last Modified: Sat, 16 Mar 2024 08:41:40 GMT  
		Size: 69.6 MB (69567046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed37ba0f96ce248f221fa22342b8a7122705ce4f59695cdaaddfc7b083d38ed8`  
		Last Modified: Sat, 16 Mar 2024 08:41:32 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0ef027374ae9de66a89225afc876a3984220ca369d21394c2a20f2705e0a81`  
		Last Modified: Sat, 16 Mar 2024 08:41:32 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:343d4b05070a2f96e15b6df58b1e6d940d2c25a975b212f2749aaae284220ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:913027953f2d843dbefd33f76221b455b33e2a8b27b12c7ac5d83aa8793bb121
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142788105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa6a0dfcf8158ef45be9e14968a5a8619c78dedfc06b173c1bd8b43443c3558`
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
# Tue, 16 Apr 2024 08:35:39 GMT
ENV KAPACITOR_VERSION=1.7.2
# Tue, 16 Apr 2024 08:35:46 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 16 Apr 2024 08:35:46 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 16 Apr 2024 08:35:46 GMT
EXPOSE 9092
# Tue, 16 Apr 2024 08:35:46 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 16 Apr 2024 08:35:46 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 16 Apr 2024 08:35:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 08:35:47 GMT
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
	-	`sha256:3247d4e87d041433e4cbc81ecba5791a2e9121c091ebb82688c9d1f90bc7191e`  
		Last Modified: Tue, 16 Apr 2024 08:36:27 GMT  
		Size: 69.6 MB (69647935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c368c6e492610024afdbc9fc290ad95623c42c4e690f34201b77481f43ef7e8`  
		Last Modified: Tue, 16 Apr 2024 08:36:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a246c5bd7aad48348ffa4a0d641d4cfb8580cc0e7b17b41a8ddbb5ab4242f33`  
		Last Modified: Tue, 16 Apr 2024 08:36:18 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:ce15093189ca1d230b33de84c905ba2672d905ceef27df8ff17bb580c465ad43
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133477720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff359bc276a9d40705834307c0d0d9a25e8cbc2d0de20949140ffa4b27f1f15`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 10 Apr 2024 18:26:15 GMT
ARG RELEASE
# Wed, 10 Apr 2024 18:26:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Apr 2024 18:26:15 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 10 Apr 2024 18:26:17 GMT
ADD file:5523c8e2dfa5286893a32b66bdb3395b76e282d86d79b7320a5855e8f55481e1 in / 
# Wed, 10 Apr 2024 18:26:17 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 01:55:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 16 Apr 2024 05:27:21 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 16 Apr 2024 05:27:35 GMT
ENV KAPACITOR_VERSION=1.7.2
# Tue, 16 Apr 2024 05:27:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 16 Apr 2024 05:27:42 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 16 Apr 2024 05:27:42 GMT
EXPOSE 9092
# Tue, 16 Apr 2024 05:27:42 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 16 Apr 2024 05:27:42 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 16 Apr 2024 05:27:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 16 Apr 2024 05:27:42 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:89412e4d2f8b52822269bdfcea7664caa02251913b423e2ede06eb268ff39557`  
		Last Modified: Fri, 12 Apr 2024 01:35:29 GMT  
		Size: 28.4 MB (28400298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895c42abeb4df7fe7e0293498c3dacd85ab82f5b16b6a3b5ef980731419983b2`  
		Last Modified: Tue, 16 Apr 2024 02:11:19 GMT  
		Size: 7.1 MB (7068419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509b748565ee4f38df11041e760b533e2480b107e72a61a3962a7d52a7d35c3d`  
		Last Modified: Tue, 16 Apr 2024 05:27:54 GMT  
		Size: 32.9 MB (32860037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6edf52129f51f008f7509fd709cbe1ec2829801333c4e423156582d83d5fbd6`  
		Last Modified: Tue, 16 Apr 2024 05:28:12 GMT  
		Size: 65.1 MB (65148511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08e4729782adc6e76b2a981328e64f0dad5b03408ed75e98ecd24b2e04f7eed2`  
		Last Modified: Tue, 16 Apr 2024 05:28:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f643b4370280edd1cdf7720ef21345a578ae3075038d83ed4d056029d95523`  
		Last Modified: Tue, 16 Apr 2024 05:28:06 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
