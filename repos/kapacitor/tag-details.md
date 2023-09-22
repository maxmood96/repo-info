<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.6`](#kapacitor16)
-	[`kapacitor:1.6-alpine`](#kapacitor16-alpine)
-	[`kapacitor:1.6.6`](#kapacitor166)
-	[`kapacitor:1.6.6-alpine`](#kapacitor166-alpine)
-	[`kapacitor:1.7`](#kapacitor17)
-	[`kapacitor:1.7-alpine`](#kapacitor17-alpine)
-	[`kapacitor:1.7.0`](#kapacitor170)
-	[`kapacitor:1.7.0-alpine`](#kapacitor170-alpine)
-	[`kapacitor:alpine`](#kapacitoralpine)
-	[`kapacitor:latest`](#kapacitorlatest)

## `kapacitor:1.6`

```console
$ docker pull kapacitor@sha256:520348dc8b299d3a7737bc5b51f590a5dcce476d8591f379f398b18932e6fe62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:1.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:e5532a22c586db295b5ba8f8fc1d0ab04488ffb9ae59c89d5f07535970873bdd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.3 MB (134346761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6bb79581c557c7fc7bc79b27ba10a553afc5f5baa1b5f9d593e0b9ff82aaeb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 16 Aug 2023 06:01:52 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:01:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:01:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:01:52 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:01:54 GMT
ADD file:aa9b51e9f0067860cebbc9930374452d1384ec3c59badb5e4733130eedc90329 in / 
# Wed, 16 Aug 2023 06:01:54 GMT
CMD ["/bin/bash"]
# Fri, 01 Sep 2023 23:59:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 01:59:10 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 02 Sep 2023 01:59:22 GMT
ENV KAPACITOR_VERSION=1.6.6
# Sat, 02 Sep 2023 01:59:28 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 02 Sep 2023 01:59:29 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 02 Sep 2023 01:59:29 GMT
EXPOSE 9092
# Sat, 02 Sep 2023 01:59:29 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 02 Sep 2023 01:59:29 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 02 Sep 2023 01:59:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 02 Sep 2023 01:59:29 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:44ba2882f8eb14264e5f2f9f6ec55bcf5306527b637279f2cd9d4858762388af`  
		Last Modified: Wed, 16 Aug 2023 10:32:51 GMT  
		Size: 30.4 MB (30438977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f2863485daf42354483046b5e0003e2a3a615b04fb72dbbd0c9d005e0b8e4d`  
		Last Modified: Sat, 02 Sep 2023 00:11:43 GMT  
		Size: 7.1 MB (7119992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778c3e4da66453cd995d5771f62ca97741654b75dd62c84af18eb9bd336fb89a`  
		Last Modified: Sat, 02 Sep 2023 01:59:43 GMT  
		Size: 31.1 MB (31114808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60bba31dfe4b1cc1bd27728f57874b9170f75cfc108a96d4a7bc30254b0cffb1`  
		Last Modified: Sat, 02 Sep 2023 02:00:01 GMT  
		Size: 65.7 MB (65672526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99132f18f2a9b21fcbe4bfd1744e870afdb545a99f70275a88adc39fddb690e9`  
		Last Modified: Sat, 02 Sep 2023 01:59:54 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7732f2a523c538988feb70cc63f1c5995fd527f9840de4d7d3a8aa57e56f2f81`  
		Last Modified: Sat, 02 Sep 2023 01:59:54 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:f9c7033077e997cf4394669d1ae378feee54f753ffdae0e2040c23e1c033f8dd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126282119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06556ecfd59fdca5aab111533e9d023213928424fa78d8308318e028dafea324`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 16 Aug 2023 06:19:52 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:19:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:19:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:19:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:19:59 GMT
ADD file:3fcf00866c55150f1ea0a5ef7b8473c39275c1fdbf6aba0acd84cacb83d0c564 in / 
# Wed, 16 Aug 2023 06:19:59 GMT
CMD ["/bin/bash"]
# Fri, 01 Sep 2023 23:12:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 01:08:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 02 Sep 2023 01:09:08 GMT
ENV KAPACITOR_VERSION=1.6.6
# Sat, 02 Sep 2023 01:09:14 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 02 Sep 2023 01:09:14 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 02 Sep 2023 01:09:14 GMT
EXPOSE 9092
# Sat, 02 Sep 2023 01:09:15 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 02 Sep 2023 01:09:15 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 02 Sep 2023 01:09:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 02 Sep 2023 01:09:15 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:8b5db5f6400d85199afbfde601a9e3c2051ebceb1ed9cc0fe25fe6b91e79afa9`  
		Last Modified: Thu, 17 Aug 2023 19:55:40 GMT  
		Size: 28.4 MB (28392978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160267f0e1a72cee3068c4084f9e7550813b518eaba96794640ab0057dd0efda`  
		Last Modified: Fri, 01 Sep 2023 23:26:00 GMT  
		Size: 7.1 MB (7067547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5403f64e34a17eb27cbffaed322dfb387772c187a5f00895a9e86db8dbba8def`  
		Last Modified: Sat, 02 Sep 2023 01:09:26 GMT  
		Size: 29.1 MB (29149554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77baa563cd7fdfd2a61b45115730ed1be2c6b6ede70a59e1e8264ae4cd2c80b1`  
		Last Modified: Sat, 02 Sep 2023 01:09:42 GMT  
		Size: 61.7 MB (61671584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b18ccb35e3dbc84e5482c88d55c028b307a2555c054efc39b448914beb3351`  
		Last Modified: Sat, 02 Sep 2023 01:09:35 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cdc7ad636d6938218ae7c699b488aa3f594f7d51b80b6cc698a037887151cc0`  
		Last Modified: Sat, 02 Sep 2023 01:09:35 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.6-alpine`

```console
$ docker pull kapacitor@sha256:649a97fc6725f8320bc780e9559dadcbbae8b97e1bbed5d859e193b35f276b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:7b7418906094f3e66553c595956ece066860539debed2172bd0e97ccaf6b03ca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68673465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c0ab4b2e7a3e604797ddf2015c7b97fcdee7df4948f525dd75b3b8bebc96e8a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:31 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 07 Aug 2023 19:20:31 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 02:06:43 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 09 Aug 2023 02:06:44 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 09 Aug 2023 02:06:44 GMT
ENV KAPACITOR_VERSION=1.6.6
# Wed, 09 Aug 2023 02:06:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 09 Aug 2023 02:06:52 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 09 Aug 2023 02:06:52 GMT
EXPOSE 9092
# Wed, 09 Aug 2023 02:06:52 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 09 Aug 2023 02:06:52 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Wed, 09 Aug 2023 02:06:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 09 Aug 2023 02:06:53 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61398f0c26e32fcf30f1436e94600012d7b35bbf04bb4a0cf0304cf2d8ae065f`  
		Last Modified: Wed, 09 Aug 2023 02:07:08 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc02a84aa2e93219dad782abd5562f8d465bed2fb7769681d5c6a42a87db231`  
		Last Modified: Wed, 09 Aug 2023 02:07:08 GMT  
		Size: 284.9 KB (284895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2687f33019eea09dc53b5214c7b87d0c9bcb9a3898ad6ee9f316d7865c71c673`  
		Last Modified: Wed, 09 Aug 2023 02:07:16 GMT  
		Size: 65.6 MB (65580154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b00ae2bb82d25948398d6dcea1533849cc768d89ad5a61cd6ecf685c217b2fb`  
		Last Modified: Wed, 09 Aug 2023 02:07:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedb4317a123bd4dc6bb77c19a0f1ce1410a13a8926df49193aab5f9aecb78e3`  
		Last Modified: Wed, 09 Aug 2023 02:07:08 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.6.6`

```console
$ docker pull kapacitor@sha256:520348dc8b299d3a7737bc5b51f590a5dcce476d8591f379f398b18932e6fe62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:1.6.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:e5532a22c586db295b5ba8f8fc1d0ab04488ffb9ae59c89d5f07535970873bdd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.3 MB (134346761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6bb79581c557c7fc7bc79b27ba10a553afc5f5baa1b5f9d593e0b9ff82aaeb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 16 Aug 2023 06:01:52 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:01:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:01:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:01:52 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:01:54 GMT
ADD file:aa9b51e9f0067860cebbc9930374452d1384ec3c59badb5e4733130eedc90329 in / 
# Wed, 16 Aug 2023 06:01:54 GMT
CMD ["/bin/bash"]
# Fri, 01 Sep 2023 23:59:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 01:59:10 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 02 Sep 2023 01:59:22 GMT
ENV KAPACITOR_VERSION=1.6.6
# Sat, 02 Sep 2023 01:59:28 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 02 Sep 2023 01:59:29 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 02 Sep 2023 01:59:29 GMT
EXPOSE 9092
# Sat, 02 Sep 2023 01:59:29 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 02 Sep 2023 01:59:29 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 02 Sep 2023 01:59:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 02 Sep 2023 01:59:29 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:44ba2882f8eb14264e5f2f9f6ec55bcf5306527b637279f2cd9d4858762388af`  
		Last Modified: Wed, 16 Aug 2023 10:32:51 GMT  
		Size: 30.4 MB (30438977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f2863485daf42354483046b5e0003e2a3a615b04fb72dbbd0c9d005e0b8e4d`  
		Last Modified: Sat, 02 Sep 2023 00:11:43 GMT  
		Size: 7.1 MB (7119992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778c3e4da66453cd995d5771f62ca97741654b75dd62c84af18eb9bd336fb89a`  
		Last Modified: Sat, 02 Sep 2023 01:59:43 GMT  
		Size: 31.1 MB (31114808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60bba31dfe4b1cc1bd27728f57874b9170f75cfc108a96d4a7bc30254b0cffb1`  
		Last Modified: Sat, 02 Sep 2023 02:00:01 GMT  
		Size: 65.7 MB (65672526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99132f18f2a9b21fcbe4bfd1744e870afdb545a99f70275a88adc39fddb690e9`  
		Last Modified: Sat, 02 Sep 2023 01:59:54 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7732f2a523c538988feb70cc63f1c5995fd527f9840de4d7d3a8aa57e56f2f81`  
		Last Modified: Sat, 02 Sep 2023 01:59:54 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.6.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:f9c7033077e997cf4394669d1ae378feee54f753ffdae0e2040c23e1c033f8dd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126282119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06556ecfd59fdca5aab111533e9d023213928424fa78d8308318e028dafea324`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 16 Aug 2023 06:19:52 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:19:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:19:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:19:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:19:59 GMT
ADD file:3fcf00866c55150f1ea0a5ef7b8473c39275c1fdbf6aba0acd84cacb83d0c564 in / 
# Wed, 16 Aug 2023 06:19:59 GMT
CMD ["/bin/bash"]
# Fri, 01 Sep 2023 23:12:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 01:08:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 02 Sep 2023 01:09:08 GMT
ENV KAPACITOR_VERSION=1.6.6
# Sat, 02 Sep 2023 01:09:14 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 02 Sep 2023 01:09:14 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 02 Sep 2023 01:09:14 GMT
EXPOSE 9092
# Sat, 02 Sep 2023 01:09:15 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 02 Sep 2023 01:09:15 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 02 Sep 2023 01:09:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 02 Sep 2023 01:09:15 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:8b5db5f6400d85199afbfde601a9e3c2051ebceb1ed9cc0fe25fe6b91e79afa9`  
		Last Modified: Thu, 17 Aug 2023 19:55:40 GMT  
		Size: 28.4 MB (28392978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160267f0e1a72cee3068c4084f9e7550813b518eaba96794640ab0057dd0efda`  
		Last Modified: Fri, 01 Sep 2023 23:26:00 GMT  
		Size: 7.1 MB (7067547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5403f64e34a17eb27cbffaed322dfb387772c187a5f00895a9e86db8dbba8def`  
		Last Modified: Sat, 02 Sep 2023 01:09:26 GMT  
		Size: 29.1 MB (29149554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77baa563cd7fdfd2a61b45115730ed1be2c6b6ede70a59e1e8264ae4cd2c80b1`  
		Last Modified: Sat, 02 Sep 2023 01:09:42 GMT  
		Size: 61.7 MB (61671584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b18ccb35e3dbc84e5482c88d55c028b307a2555c054efc39b448914beb3351`  
		Last Modified: Sat, 02 Sep 2023 01:09:35 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cdc7ad636d6938218ae7c699b488aa3f594f7d51b80b6cc698a037887151cc0`  
		Last Modified: Sat, 02 Sep 2023 01:09:35 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.6.6-alpine`

```console
$ docker pull kapacitor@sha256:649a97fc6725f8320bc780e9559dadcbbae8b97e1bbed5d859e193b35f276b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.6.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:7b7418906094f3e66553c595956ece066860539debed2172bd0e97ccaf6b03ca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68673465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c0ab4b2e7a3e604797ddf2015c7b97fcdee7df4948f525dd75b3b8bebc96e8a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:31 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 07 Aug 2023 19:20:31 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 02:06:43 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 09 Aug 2023 02:06:44 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 09 Aug 2023 02:06:44 GMT
ENV KAPACITOR_VERSION=1.6.6
# Wed, 09 Aug 2023 02:06:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 09 Aug 2023 02:06:52 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 09 Aug 2023 02:06:52 GMT
EXPOSE 9092
# Wed, 09 Aug 2023 02:06:52 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 09 Aug 2023 02:06:52 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Wed, 09 Aug 2023 02:06:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 09 Aug 2023 02:06:53 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61398f0c26e32fcf30f1436e94600012d7b35bbf04bb4a0cf0304cf2d8ae065f`  
		Last Modified: Wed, 09 Aug 2023 02:07:08 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc02a84aa2e93219dad782abd5562f8d465bed2fb7769681d5c6a42a87db231`  
		Last Modified: Wed, 09 Aug 2023 02:07:08 GMT  
		Size: 284.9 KB (284895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2687f33019eea09dc53b5214c7b87d0c9bcb9a3898ad6ee9f316d7865c71c673`  
		Last Modified: Wed, 09 Aug 2023 02:07:16 GMT  
		Size: 65.6 MB (65580154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b00ae2bb82d25948398d6dcea1533849cc768d89ad5a61cd6ecf685c217b2fb`  
		Last Modified: Wed, 09 Aug 2023 02:07:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedb4317a123bd4dc6bb77c19a0f1ce1410a13a8926df49193aab5f9aecb78e3`  
		Last Modified: Wed, 09 Aug 2023 02:07:08 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.7`

```console
$ docker pull kapacitor@sha256:c019bd0f702ace8e8085988d6c6498a09310d761b4306e43d317abef4c35396f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `kapacitor:1.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:bc4454d97b09c6871b838fc4bdba4ee36fbf58b5df718e969eb8012c677a37ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126891646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9504d919122d9a0055e6fbcb054ea17f9b6c359abc1add34bd442f013ca0fb0c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 16 Aug 2023 06:19:52 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:19:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:19:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:19:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:19:59 GMT
ADD file:3fcf00866c55150f1ea0a5ef7b8473c39275c1fdbf6aba0acd84cacb83d0c564 in / 
# Wed, 16 Aug 2023 06:19:59 GMT
CMD ["/bin/bash"]
# Fri, 01 Sep 2023 23:12:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 01:08:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 21 Sep 2023 23:39:40 GMT
ENV KAPACITOR_VERSION=1.7.0
# Thu, 21 Sep 2023 23:39:47 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 21 Sep 2023 23:39:47 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 21 Sep 2023 23:39:47 GMT
EXPOSE 9092
# Thu, 21 Sep 2023 23:39:48 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 21 Sep 2023 23:39:48 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 21 Sep 2023 23:39:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 21 Sep 2023 23:39:48 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:8b5db5f6400d85199afbfde601a9e3c2051ebceb1ed9cc0fe25fe6b91e79afa9`  
		Last Modified: Thu, 17 Aug 2023 19:55:40 GMT  
		Size: 28.4 MB (28392978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160267f0e1a72cee3068c4084f9e7550813b518eaba96794640ab0057dd0efda`  
		Last Modified: Fri, 01 Sep 2023 23:26:00 GMT  
		Size: 7.1 MB (7067547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5403f64e34a17eb27cbffaed322dfb387772c187a5f00895a9e86db8dbba8def`  
		Last Modified: Sat, 02 Sep 2023 01:09:26 GMT  
		Size: 29.1 MB (29149554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2368125b3e083c936a4ea047d4cd5aa615238f79dbc269a9140fd95b19be7346`  
		Last Modified: Thu, 21 Sep 2023 23:40:07 GMT  
		Size: 62.3 MB (62281112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f7699756a55d5482bbc6f974ccb68ff0c64ba1e44a6a699d186b527ff1c1bc`  
		Last Modified: Thu, 21 Sep 2023 23:40:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b321b54b00bd67c66e780942cca469fb5b628f5288a436921c892e855d0456ca`  
		Last Modified: Thu, 21 Sep 2023 23:40:01 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.7-alpine`

```console
$ docker pull kapacitor@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `kapacitor:1.7.0`

```console
$ docker pull kapacitor@sha256:c019bd0f702ace8e8085988d6c6498a09310d761b4306e43d317abef4c35396f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `kapacitor:1.7.0` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:bc4454d97b09c6871b838fc4bdba4ee36fbf58b5df718e969eb8012c677a37ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126891646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9504d919122d9a0055e6fbcb054ea17f9b6c359abc1add34bd442f013ca0fb0c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 16 Aug 2023 06:19:52 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:19:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:19:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:19:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:19:59 GMT
ADD file:3fcf00866c55150f1ea0a5ef7b8473c39275c1fdbf6aba0acd84cacb83d0c564 in / 
# Wed, 16 Aug 2023 06:19:59 GMT
CMD ["/bin/bash"]
# Fri, 01 Sep 2023 23:12:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 01:08:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 21 Sep 2023 23:39:40 GMT
ENV KAPACITOR_VERSION=1.7.0
# Thu, 21 Sep 2023 23:39:47 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 21 Sep 2023 23:39:47 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 21 Sep 2023 23:39:47 GMT
EXPOSE 9092
# Thu, 21 Sep 2023 23:39:48 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 21 Sep 2023 23:39:48 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 21 Sep 2023 23:39:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 21 Sep 2023 23:39:48 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:8b5db5f6400d85199afbfde601a9e3c2051ebceb1ed9cc0fe25fe6b91e79afa9`  
		Last Modified: Thu, 17 Aug 2023 19:55:40 GMT  
		Size: 28.4 MB (28392978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160267f0e1a72cee3068c4084f9e7550813b518eaba96794640ab0057dd0efda`  
		Last Modified: Fri, 01 Sep 2023 23:26:00 GMT  
		Size: 7.1 MB (7067547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5403f64e34a17eb27cbffaed322dfb387772c187a5f00895a9e86db8dbba8def`  
		Last Modified: Sat, 02 Sep 2023 01:09:26 GMT  
		Size: 29.1 MB (29149554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2368125b3e083c936a4ea047d4cd5aa615238f79dbc269a9140fd95b19be7346`  
		Last Modified: Thu, 21 Sep 2023 23:40:07 GMT  
		Size: 62.3 MB (62281112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f7699756a55d5482bbc6f974ccb68ff0c64ba1e44a6a699d186b527ff1c1bc`  
		Last Modified: Thu, 21 Sep 2023 23:40:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b321b54b00bd67c66e780942cca469fb5b628f5288a436921c892e855d0456ca`  
		Last Modified: Thu, 21 Sep 2023 23:40:01 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.7.0-alpine`

```console
$ docker pull kapacitor@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:649a97fc6725f8320bc780e9559dadcbbae8b97e1bbed5d859e193b35f276b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:7b7418906094f3e66553c595956ece066860539debed2172bd0e97ccaf6b03ca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68673465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c0ab4b2e7a3e604797ddf2015c7b97fcdee7df4948f525dd75b3b8bebc96e8a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:31 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 07 Aug 2023 19:20:31 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 02:06:43 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 09 Aug 2023 02:06:44 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 09 Aug 2023 02:06:44 GMT
ENV KAPACITOR_VERSION=1.6.6
# Wed, 09 Aug 2023 02:06:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 09 Aug 2023 02:06:52 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 09 Aug 2023 02:06:52 GMT
EXPOSE 9092
# Wed, 09 Aug 2023 02:06:52 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 09 Aug 2023 02:06:52 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Wed, 09 Aug 2023 02:06:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 09 Aug 2023 02:06:53 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61398f0c26e32fcf30f1436e94600012d7b35bbf04bb4a0cf0304cf2d8ae065f`  
		Last Modified: Wed, 09 Aug 2023 02:07:08 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc02a84aa2e93219dad782abd5562f8d465bed2fb7769681d5c6a42a87db231`  
		Last Modified: Wed, 09 Aug 2023 02:07:08 GMT  
		Size: 284.9 KB (284895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2687f33019eea09dc53b5214c7b87d0c9bcb9a3898ad6ee9f316d7865c71c673`  
		Last Modified: Wed, 09 Aug 2023 02:07:16 GMT  
		Size: 65.6 MB (65580154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b00ae2bb82d25948398d6dcea1533849cc768d89ad5a61cd6ecf685c217b2fb`  
		Last Modified: Wed, 09 Aug 2023 02:07:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedb4317a123bd4dc6bb77c19a0f1ce1410a13a8926df49193aab5f9aecb78e3`  
		Last Modified: Wed, 09 Aug 2023 02:07:08 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:ae1d874556097c0a52893d4f8c8ec673e548c399335c39ae190f3711d06e9306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:e5532a22c586db295b5ba8f8fc1d0ab04488ffb9ae59c89d5f07535970873bdd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.3 MB (134346761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6bb79581c557c7fc7bc79b27ba10a553afc5f5baa1b5f9d593e0b9ff82aaeb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 16 Aug 2023 06:01:52 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:01:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:01:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:01:52 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:01:54 GMT
ADD file:aa9b51e9f0067860cebbc9930374452d1384ec3c59badb5e4733130eedc90329 in / 
# Wed, 16 Aug 2023 06:01:54 GMT
CMD ["/bin/bash"]
# Fri, 01 Sep 2023 23:59:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 01:59:10 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 02 Sep 2023 01:59:22 GMT
ENV KAPACITOR_VERSION=1.6.6
# Sat, 02 Sep 2023 01:59:28 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 02 Sep 2023 01:59:29 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 02 Sep 2023 01:59:29 GMT
EXPOSE 9092
# Sat, 02 Sep 2023 01:59:29 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 02 Sep 2023 01:59:29 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 02 Sep 2023 01:59:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 02 Sep 2023 01:59:29 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:44ba2882f8eb14264e5f2f9f6ec55bcf5306527b637279f2cd9d4858762388af`  
		Last Modified: Wed, 16 Aug 2023 10:32:51 GMT  
		Size: 30.4 MB (30438977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f2863485daf42354483046b5e0003e2a3a615b04fb72dbbd0c9d005e0b8e4d`  
		Last Modified: Sat, 02 Sep 2023 00:11:43 GMT  
		Size: 7.1 MB (7119992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778c3e4da66453cd995d5771f62ca97741654b75dd62c84af18eb9bd336fb89a`  
		Last Modified: Sat, 02 Sep 2023 01:59:43 GMT  
		Size: 31.1 MB (31114808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60bba31dfe4b1cc1bd27728f57874b9170f75cfc108a96d4a7bc30254b0cffb1`  
		Last Modified: Sat, 02 Sep 2023 02:00:01 GMT  
		Size: 65.7 MB (65672526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99132f18f2a9b21fcbe4bfd1744e870afdb545a99f70275a88adc39fddb690e9`  
		Last Modified: Sat, 02 Sep 2023 01:59:54 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7732f2a523c538988feb70cc63f1c5995fd527f9840de4d7d3a8aa57e56f2f81`  
		Last Modified: Sat, 02 Sep 2023 01:59:54 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:bc4454d97b09c6871b838fc4bdba4ee36fbf58b5df718e969eb8012c677a37ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126891646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9504d919122d9a0055e6fbcb054ea17f9b6c359abc1add34bd442f013ca0fb0c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 16 Aug 2023 06:19:52 GMT
ARG RELEASE
# Wed, 16 Aug 2023 06:19:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Aug 2023 06:19:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Aug 2023 06:19:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Aug 2023 06:19:59 GMT
ADD file:3fcf00866c55150f1ea0a5ef7b8473c39275c1fdbf6aba0acd84cacb83d0c564 in / 
# Wed, 16 Aug 2023 06:19:59 GMT
CMD ["/bin/bash"]
# Fri, 01 Sep 2023 23:12:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 01:08:56 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 21 Sep 2023 23:39:40 GMT
ENV KAPACITOR_VERSION=1.7.0
# Thu, 21 Sep 2023 23:39:47 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 21 Sep 2023 23:39:47 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 21 Sep 2023 23:39:47 GMT
EXPOSE 9092
# Thu, 21 Sep 2023 23:39:48 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 21 Sep 2023 23:39:48 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 21 Sep 2023 23:39:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 21 Sep 2023 23:39:48 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:8b5db5f6400d85199afbfde601a9e3c2051ebceb1ed9cc0fe25fe6b91e79afa9`  
		Last Modified: Thu, 17 Aug 2023 19:55:40 GMT  
		Size: 28.4 MB (28392978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160267f0e1a72cee3068c4084f9e7550813b518eaba96794640ab0057dd0efda`  
		Last Modified: Fri, 01 Sep 2023 23:26:00 GMT  
		Size: 7.1 MB (7067547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5403f64e34a17eb27cbffaed322dfb387772c187a5f00895a9e86db8dbba8def`  
		Last Modified: Sat, 02 Sep 2023 01:09:26 GMT  
		Size: 29.1 MB (29149554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2368125b3e083c936a4ea047d4cd5aa615238f79dbc269a9140fd95b19be7346`  
		Last Modified: Thu, 21 Sep 2023 23:40:07 GMT  
		Size: 62.3 MB (62281112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f7699756a55d5482bbc6f974ccb68ff0c64ba1e44a6a699d186b527ff1c1bc`  
		Last Modified: Thu, 21 Sep 2023 23:40:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b321b54b00bd67c66e780942cca469fb5b628f5288a436921c892e855d0456ca`  
		Last Modified: Thu, 21 Sep 2023 23:40:01 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
