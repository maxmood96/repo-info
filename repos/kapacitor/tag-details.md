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
$ docker pull kapacitor@sha256:a32b6b8c2c48cdfc1e46fafa63d050dbe58430406e3fff62c4f4077505b59bb2
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
$ docker pull kapacitor@sha256:c7fc436cba3cbecbfff532a6faf16503b536e939eca24b1a1215b32a15e47c70
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130422902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc90bf8495fe33a95a635fa31bc58f6775560fe464b230262d5ef3baad1256ff`
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
# Thu, 25 Apr 2024 21:15:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Apr 2024 01:00:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 26 Apr 2024 01:00:44 GMT
ENV KAPACITOR_VERSION=1.6.6
# Fri, 26 Apr 2024 01:00:50 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 26 Apr 2024 01:00:51 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 26 Apr 2024 01:00:51 GMT
EXPOSE 9092
# Fri, 26 Apr 2024 01:00:51 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 26 Apr 2024 01:00:51 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 26 Apr 2024 01:00:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 01:00:51 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c6efd61b232e6060a5ae247be4a304ae261939d0814281b2db15ac1c5f6b35`  
		Last Modified: Thu, 25 Apr 2024 21:45:59 GMT  
		Size: 7.1 MB (7068156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c573c773c94d8b8272cec2c0dafcce53fadb7bc25b04a1ac4fb3823c35f75aa7`  
		Last Modified: Fri, 26 Apr 2024 01:01:11 GMT  
		Size: 33.3 MB (33283190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f6137750f206a118b1721a2c09a1b16059272641a719de98f01d845c2fd3c6`  
		Last Modified: Fri, 26 Apr 2024 01:01:14 GMT  
		Size: 61.7 MB (61670098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5a7e8f01736851820e60f50958414bdf46a314c53da41ddc73ebaf91d365e6`  
		Last Modified: Fri, 26 Apr 2024 01:01:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2132cccd29241ed380fef28fba3a9b7d587f1a259300ca3e425d39866c0bf3b4`  
		Last Modified: Fri, 26 Apr 2024 01:01:09 GMT  
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
$ docker pull kapacitor@sha256:a32b6b8c2c48cdfc1e46fafa63d050dbe58430406e3fff62c4f4077505b59bb2
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
$ docker pull kapacitor@sha256:c7fc436cba3cbecbfff532a6faf16503b536e939eca24b1a1215b32a15e47c70
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130422902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc90bf8495fe33a95a635fa31bc58f6775560fe464b230262d5ef3baad1256ff`
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
# Thu, 25 Apr 2024 21:15:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Apr 2024 01:00:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 26 Apr 2024 01:00:44 GMT
ENV KAPACITOR_VERSION=1.6.6
# Fri, 26 Apr 2024 01:00:50 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 26 Apr 2024 01:00:51 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 26 Apr 2024 01:00:51 GMT
EXPOSE 9092
# Fri, 26 Apr 2024 01:00:51 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 26 Apr 2024 01:00:51 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 26 Apr 2024 01:00:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 01:00:51 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c6efd61b232e6060a5ae247be4a304ae261939d0814281b2db15ac1c5f6b35`  
		Last Modified: Thu, 25 Apr 2024 21:45:59 GMT  
		Size: 7.1 MB (7068156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c573c773c94d8b8272cec2c0dafcce53fadb7bc25b04a1ac4fb3823c35f75aa7`  
		Last Modified: Fri, 26 Apr 2024 01:01:11 GMT  
		Size: 33.3 MB (33283190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f6137750f206a118b1721a2c09a1b16059272641a719de98f01d845c2fd3c6`  
		Last Modified: Fri, 26 Apr 2024 01:01:14 GMT  
		Size: 61.7 MB (61670098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5a7e8f01736851820e60f50958414bdf46a314c53da41ddc73ebaf91d365e6`  
		Last Modified: Fri, 26 Apr 2024 01:01:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2132cccd29241ed380fef28fba3a9b7d587f1a259300ca3e425d39866c0bf3b4`  
		Last Modified: Fri, 26 Apr 2024 01:01:09 GMT  
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
$ docker pull kapacitor@sha256:183a54fa9301dfe2bf7f079f2e55303edf9a15c296a03fc2fe3bcdd6e81b62d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:1.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:7ae309652b3943187aaa061eeb50666049d679b5492cb9c06df3a31a453e71f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.5 MB (144517171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:518016eaeae41df047016a611c1d3e8a8086aa16e234fe96ea1c6848570b822e`
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
# Tue, 23 Apr 2024 17:27:36 GMT
ENV KAPACITOR_VERSION=1.7.4
# Tue, 23 Apr 2024 17:27:44 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 23 Apr 2024 17:27:44 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 23 Apr 2024 17:27:44 GMT
EXPOSE 9092
# Tue, 23 Apr 2024 17:27:44 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 23 Apr 2024 17:27:44 GMT
COPY file:d13199909208ae1b9e95c89c9f0f75ecda30911090da90e33a2c258a88927a06 in /entrypoint.sh 
# Tue, 23 Apr 2024 17:27:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Apr 2024 17:27:45 GMT
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
	-	`sha256:6b3c020d61d6731bfadbeec60244f23287c686e0181a150ab4f7e00fbda5c0fb`  
		Last Modified: Tue, 23 Apr 2024 17:28:23 GMT  
		Size: 71.4 MB (71376935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de9171898e67d23ff6a425a3d84a6dd701c7905cac0978f08b8a75de01e1085`  
		Last Modified: Tue, 23 Apr 2024 17:28:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fccb52ee5db43c6f53a730c5f55047db1fc77613231a3711ecbff7fad87f2d`  
		Last Modified: Tue, 23 Apr 2024 17:28:15 GMT  
		Size: 296.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:3ebdd391e42c9c18ffbf5bdb4953619b49c830e013e0bd53617453ecfb022c1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135847907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3beaa22b4863bbd0a0586ec588a3bf800735e8e92224b224be7fcb3ea6f63533`
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
# Thu, 25 Apr 2024 21:15:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Apr 2024 01:00:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 26 Apr 2024 01:00:53 GMT
ENV KAPACITOR_VERSION=1.7.4
# Fri, 26 Apr 2024 01:00:58 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 26 Apr 2024 01:00:59 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 26 Apr 2024 01:00:59 GMT
EXPOSE 9092
# Fri, 26 Apr 2024 01:00:59 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 26 Apr 2024 01:01:00 GMT
COPY file:d13199909208ae1b9e95c89c9f0f75ecda30911090da90e33a2c258a88927a06 in /entrypoint.sh 
# Fri, 26 Apr 2024 01:01:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 01:01:00 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c6efd61b232e6060a5ae247be4a304ae261939d0814281b2db15ac1c5f6b35`  
		Last Modified: Thu, 25 Apr 2024 21:45:59 GMT  
		Size: 7.1 MB (7068156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c573c773c94d8b8272cec2c0dafcce53fadb7bc25b04a1ac4fb3823c35f75aa7`  
		Last Modified: Fri, 26 Apr 2024 01:01:11 GMT  
		Size: 33.3 MB (33283190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c04a191c325921f14f601aff49ca006e06332113d4ac5d070c2619f45abb790`  
		Last Modified: Fri, 26 Apr 2024 01:01:30 GMT  
		Size: 67.1 MB (67095037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5cca6ca8dfe8e66d3f3581711649fc6b9d206e61be475de0ba3e049ab71c52`  
		Last Modified: Fri, 26 Apr 2024 01:01:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aef2b8d0a5afc1e1e350fc7bddc3a5672153b984279e6ad9dad667c06207311`  
		Last Modified: Fri, 26 Apr 2024 01:01:24 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.7-alpine`

```console
$ docker pull kapacitor@sha256:0c0d69e71c7c06640d8070a0b0f3f5fde0189dddc96db0b1c01110a399e384ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.7-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:a497098033685fecd13c84b9b58f5efc50773f24e5d90b1698be081170c9db64
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75007510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37013399c6e82dacd949c5cf924685ee39fb1cc6f3e598a3f984c8613f899f64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 23 Apr 2024 17:27:49 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates
# Tue, 23 Apr 2024 17:27:49 GMT
ENV KAPACITOR_VERSION=1.7.4
# Tue, 23 Apr 2024 17:27:59 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor
# Tue, 23 Apr 2024 17:28:00 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 23 Apr 2024 17:28:00 GMT
EXPOSE 9092
# Tue, 23 Apr 2024 17:28:00 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 23 Apr 2024 17:28:00 GMT
COPY file:dbdc6f7c673f89ed4cbe749d78c718ce4b8a68da716059d12c73398d097f8494 in /entrypoint.sh 
# Tue, 23 Apr 2024 17:28:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Apr 2024 17:28:00 GMT
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
	-	`sha256:9451ab070e66261dde2ccade99194ed606e0d2cfd54f79ada2502c394614520c`  
		Last Modified: Tue, 23 Apr 2024 17:28:34 GMT  
		Size: 295.9 KB (295868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1edbe84a8fc639dee62e1022c223214507413a4f9e6d7b944a6ef4d6b9a3e7d`  
		Last Modified: Tue, 23 Apr 2024 17:28:41 GMT  
		Size: 71.3 MB (71308313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c9194d92373bb555addd9b20334e572117ed1cbb50b23ffc016ae38a5dd981`  
		Last Modified: Tue, 23 Apr 2024 17:28:33 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1eb82dc1c771bded4043998630301d16b33569a0fb7343704c53fd8dacba472`  
		Last Modified: Tue, 23 Apr 2024 17:28:33 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.7.4`

```console
$ docker pull kapacitor@sha256:183a54fa9301dfe2bf7f079f2e55303edf9a15c296a03fc2fe3bcdd6e81b62d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:1.7.4` - linux; amd64

```console
$ docker pull kapacitor@sha256:7ae309652b3943187aaa061eeb50666049d679b5492cb9c06df3a31a453e71f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.5 MB (144517171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:518016eaeae41df047016a611c1d3e8a8086aa16e234fe96ea1c6848570b822e`
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
# Tue, 23 Apr 2024 17:27:36 GMT
ENV KAPACITOR_VERSION=1.7.4
# Tue, 23 Apr 2024 17:27:44 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 23 Apr 2024 17:27:44 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 23 Apr 2024 17:27:44 GMT
EXPOSE 9092
# Tue, 23 Apr 2024 17:27:44 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 23 Apr 2024 17:27:44 GMT
COPY file:d13199909208ae1b9e95c89c9f0f75ecda30911090da90e33a2c258a88927a06 in /entrypoint.sh 
# Tue, 23 Apr 2024 17:27:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Apr 2024 17:27:45 GMT
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
	-	`sha256:6b3c020d61d6731bfadbeec60244f23287c686e0181a150ab4f7e00fbda5c0fb`  
		Last Modified: Tue, 23 Apr 2024 17:28:23 GMT  
		Size: 71.4 MB (71376935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de9171898e67d23ff6a425a3d84a6dd701c7905cac0978f08b8a75de01e1085`  
		Last Modified: Tue, 23 Apr 2024 17:28:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fccb52ee5db43c6f53a730c5f55047db1fc77613231a3711ecbff7fad87f2d`  
		Last Modified: Tue, 23 Apr 2024 17:28:15 GMT  
		Size: 296.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.7.4` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:3ebdd391e42c9c18ffbf5bdb4953619b49c830e013e0bd53617453ecfb022c1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135847907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3beaa22b4863bbd0a0586ec588a3bf800735e8e92224b224be7fcb3ea6f63533`
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
# Thu, 25 Apr 2024 21:15:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Apr 2024 01:00:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 26 Apr 2024 01:00:53 GMT
ENV KAPACITOR_VERSION=1.7.4
# Fri, 26 Apr 2024 01:00:58 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 26 Apr 2024 01:00:59 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 26 Apr 2024 01:00:59 GMT
EXPOSE 9092
# Fri, 26 Apr 2024 01:00:59 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 26 Apr 2024 01:01:00 GMT
COPY file:d13199909208ae1b9e95c89c9f0f75ecda30911090da90e33a2c258a88927a06 in /entrypoint.sh 
# Fri, 26 Apr 2024 01:01:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 01:01:00 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c6efd61b232e6060a5ae247be4a304ae261939d0814281b2db15ac1c5f6b35`  
		Last Modified: Thu, 25 Apr 2024 21:45:59 GMT  
		Size: 7.1 MB (7068156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c573c773c94d8b8272cec2c0dafcce53fadb7bc25b04a1ac4fb3823c35f75aa7`  
		Last Modified: Fri, 26 Apr 2024 01:01:11 GMT  
		Size: 33.3 MB (33283190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c04a191c325921f14f601aff49ca006e06332113d4ac5d070c2619f45abb790`  
		Last Modified: Fri, 26 Apr 2024 01:01:30 GMT  
		Size: 67.1 MB (67095037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5cca6ca8dfe8e66d3f3581711649fc6b9d206e61be475de0ba3e049ab71c52`  
		Last Modified: Fri, 26 Apr 2024 01:01:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aef2b8d0a5afc1e1e350fc7bddc3a5672153b984279e6ad9dad667c06207311`  
		Last Modified: Fri, 26 Apr 2024 01:01:24 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.7.4-alpine`

```console
$ docker pull kapacitor@sha256:0c0d69e71c7c06640d8070a0b0f3f5fde0189dddc96db0b1c01110a399e384ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.7.4-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:a497098033685fecd13c84b9b58f5efc50773f24e5d90b1698be081170c9db64
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75007510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37013399c6e82dacd949c5cf924685ee39fb1cc6f3e598a3f984c8613f899f64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 23 Apr 2024 17:27:49 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates
# Tue, 23 Apr 2024 17:27:49 GMT
ENV KAPACITOR_VERSION=1.7.4
# Tue, 23 Apr 2024 17:27:59 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor
# Tue, 23 Apr 2024 17:28:00 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 23 Apr 2024 17:28:00 GMT
EXPOSE 9092
# Tue, 23 Apr 2024 17:28:00 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 23 Apr 2024 17:28:00 GMT
COPY file:dbdc6f7c673f89ed4cbe749d78c718ce4b8a68da716059d12c73398d097f8494 in /entrypoint.sh 
# Tue, 23 Apr 2024 17:28:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Apr 2024 17:28:00 GMT
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
	-	`sha256:9451ab070e66261dde2ccade99194ed606e0d2cfd54f79ada2502c394614520c`  
		Last Modified: Tue, 23 Apr 2024 17:28:34 GMT  
		Size: 295.9 KB (295868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1edbe84a8fc639dee62e1022c223214507413a4f9e6d7b944a6ef4d6b9a3e7d`  
		Last Modified: Tue, 23 Apr 2024 17:28:41 GMT  
		Size: 71.3 MB (71308313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c9194d92373bb555addd9b20334e572117ed1cbb50b23ffc016ae38a5dd981`  
		Last Modified: Tue, 23 Apr 2024 17:28:33 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1eb82dc1c771bded4043998630301d16b33569a0fb7343704c53fd8dacba472`  
		Last Modified: Tue, 23 Apr 2024 17:28:33 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:0c0d69e71c7c06640d8070a0b0f3f5fde0189dddc96db0b1c01110a399e384ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:a497098033685fecd13c84b9b58f5efc50773f24e5d90b1698be081170c9db64
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (75007510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37013399c6e82dacd949c5cf924685ee39fb1cc6f3e598a3f984c8613f899f64`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:20:46 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Tue, 23 Apr 2024 17:27:49 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates
# Tue, 23 Apr 2024 17:27:49 GMT
ENV KAPACITOR_VERSION=1.7.4
# Tue, 23 Apr 2024 17:27:59 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor
# Tue, 23 Apr 2024 17:28:00 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 23 Apr 2024 17:28:00 GMT
EXPOSE 9092
# Tue, 23 Apr 2024 17:28:00 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 23 Apr 2024 17:28:00 GMT
COPY file:dbdc6f7c673f89ed4cbe749d78c718ce4b8a68da716059d12c73398d097f8494 in /entrypoint.sh 
# Tue, 23 Apr 2024 17:28:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Apr 2024 17:28:00 GMT
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
	-	`sha256:9451ab070e66261dde2ccade99194ed606e0d2cfd54f79ada2502c394614520c`  
		Last Modified: Tue, 23 Apr 2024 17:28:34 GMT  
		Size: 295.9 KB (295868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1edbe84a8fc639dee62e1022c223214507413a4f9e6d7b944a6ef4d6b9a3e7d`  
		Last Modified: Tue, 23 Apr 2024 17:28:41 GMT  
		Size: 71.3 MB (71308313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c9194d92373bb555addd9b20334e572117ed1cbb50b23ffc016ae38a5dd981`  
		Last Modified: Tue, 23 Apr 2024 17:28:33 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1eb82dc1c771bded4043998630301d16b33569a0fb7343704c53fd8dacba472`  
		Last Modified: Tue, 23 Apr 2024 17:28:33 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:183a54fa9301dfe2bf7f079f2e55303edf9a15c296a03fc2fe3bcdd6e81b62d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:7ae309652b3943187aaa061eeb50666049d679b5492cb9c06df3a31a453e71f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.5 MB (144517171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:518016eaeae41df047016a611c1d3e8a8086aa16e234fe96ea1c6848570b822e`
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
# Tue, 23 Apr 2024 17:27:36 GMT
ENV KAPACITOR_VERSION=1.7.4
# Tue, 23 Apr 2024 17:27:44 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 23 Apr 2024 17:27:44 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 23 Apr 2024 17:27:44 GMT
EXPOSE 9092
# Tue, 23 Apr 2024 17:27:44 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 23 Apr 2024 17:27:44 GMT
COPY file:d13199909208ae1b9e95c89c9f0f75ecda30911090da90e33a2c258a88927a06 in /entrypoint.sh 
# Tue, 23 Apr 2024 17:27:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Apr 2024 17:27:45 GMT
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
	-	`sha256:6b3c020d61d6731bfadbeec60244f23287c686e0181a150ab4f7e00fbda5c0fb`  
		Last Modified: Tue, 23 Apr 2024 17:28:23 GMT  
		Size: 71.4 MB (71376935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de9171898e67d23ff6a425a3d84a6dd701c7905cac0978f08b8a75de01e1085`  
		Last Modified: Tue, 23 Apr 2024 17:28:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fccb52ee5db43c6f53a730c5f55047db1fc77613231a3711ecbff7fad87f2d`  
		Last Modified: Tue, 23 Apr 2024 17:28:15 GMT  
		Size: 296.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:3ebdd391e42c9c18ffbf5bdb4953619b49c830e013e0bd53617453ecfb022c1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.8 MB (135847907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3beaa22b4863bbd0a0586ec588a3bf800735e8e92224b224be7fcb3ea6f63533`
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
# Thu, 25 Apr 2024 21:15:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Apr 2024 01:00:44 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 26 Apr 2024 01:00:53 GMT
ENV KAPACITOR_VERSION=1.7.4
# Fri, 26 Apr 2024 01:00:58 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 26 Apr 2024 01:00:59 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 26 Apr 2024 01:00:59 GMT
EXPOSE 9092
# Fri, 26 Apr 2024 01:00:59 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 26 Apr 2024 01:01:00 GMT
COPY file:d13199909208ae1b9e95c89c9f0f75ecda30911090da90e33a2c258a88927a06 in /entrypoint.sh 
# Fri, 26 Apr 2024 01:01:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 26 Apr 2024 01:01:00 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:4e57ea70c49f36b38caa9ead687cc8b2a5e728636d925e2dca82de1b8e1b3088`  
		Last Modified: Wed, 17 Apr 2024 23:25:57 GMT  
		Size: 28.4 MB (28401002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c6efd61b232e6060a5ae247be4a304ae261939d0814281b2db15ac1c5f6b35`  
		Last Modified: Thu, 25 Apr 2024 21:45:59 GMT  
		Size: 7.1 MB (7068156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c573c773c94d8b8272cec2c0dafcce53fadb7bc25b04a1ac4fb3823c35f75aa7`  
		Last Modified: Fri, 26 Apr 2024 01:01:11 GMT  
		Size: 33.3 MB (33283190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c04a191c325921f14f601aff49ca006e06332113d4ac5d070c2619f45abb790`  
		Last Modified: Fri, 26 Apr 2024 01:01:30 GMT  
		Size: 67.1 MB (67095037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5cca6ca8dfe8e66d3f3581711649fc6b9d206e61be475de0ba3e049ab71c52`  
		Last Modified: Fri, 26 Apr 2024 01:01:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aef2b8d0a5afc1e1e350fc7bddc3a5672153b984279e6ad9dad667c06207311`  
		Last Modified: Fri, 26 Apr 2024 01:01:24 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
