<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.5`](#kapacitor15)
-	[`kapacitor:1.5-alpine`](#kapacitor15-alpine)
-	[`kapacitor:1.5.9`](#kapacitor159)
-	[`kapacitor:1.5.9-alpine`](#kapacitor159-alpine)
-	[`kapacitor:1.6`](#kapacitor16)
-	[`kapacitor:1.6-alpine`](#kapacitor16-alpine)
-	[`kapacitor:1.6.6`](#kapacitor166)
-	[`kapacitor:1.6.6-alpine`](#kapacitor166-alpine)
-	[`kapacitor:alpine`](#kapacitoralpine)
-	[`kapacitor:latest`](#kapacitorlatest)

## `kapacitor:1.5`

```console
$ docker pull kapacitor@sha256:60ee3a59dac9f6c2e84868fb155be44f64ac709bd97e32a505b80ecbd72b67af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.5` - linux; amd64

```console
$ docker pull kapacitor@sha256:55578eb4f2e49e4d61ff15af35392be9ba1793e356cd59e2de72131361f13cf2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105545860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a896f193230ea407a067190030be7bdc620e1763d812b1894cec307bd7c9288`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 04 Aug 2023 04:52:57 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:52:59 GMT
ADD file:bb1fa1d9d012ae826908afdce8c9fa2feebf221b2ab032e1535255905144411a in / 
# Fri, 04 Aug 2023 04:53:00 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 07:04:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 00:56:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 17 Aug 2023 00:56:59 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 17 Aug 2023 00:56:59 GMT
ENV KAPACITOR_VERSION=1.5.9
# Thu, 17 Aug 2023 00:57:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 17 Aug 2023 00:57:04 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 17 Aug 2023 00:57:04 GMT
EXPOSE 9092
# Thu, 17 Aug 2023 00:57:04 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 17 Aug 2023 00:57:04 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 17 Aug 2023 00:57:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Aug 2023 00:57:04 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:99de9192b4afd13ed65aeae58d55b38e5231eb97a743921357b7d5b4c0c903c4`  
		Last Modified: Fri, 04 Aug 2023 09:25:19 GMT  
		Size: 30.4 MB (30437960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20f6742b7f13e48b26c74db979ec9995cd72f6fdc3a6b12a961ade1b6f63bf0`  
		Last Modified: Wed, 16 Aug 2023 07:16:45 GMT  
		Size: 7.1 MB (7119955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97294567ad405a596b8dc90345ba1a5007ef7b68d732a89ed4bf47793cc83a77`  
		Last Modified: Thu, 17 Aug 2023 00:57:33 GMT  
		Size: 30.8 MB (30751936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe018c5dda6ec4a52a3a7b6eefbc61a4be90bb9cd8c45233dfbf7fd6d8f20f2`  
		Last Modified: Thu, 17 Aug 2023 00:57:31 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752a1e8424e652cf7da548e3185b3ffa14d952db9241797459b8fe9387d67629`  
		Last Modified: Thu, 17 Aug 2023 00:57:35 GMT  
		Size: 37.2 MB (37233738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8011c61d64189689fe3c43676d20c89e391b5a946450dfe501b7046a07458bd`  
		Last Modified: Thu, 17 Aug 2023 00:57:30 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c94b327e18af1c9dbd35f25a486b74fea538d6d73fa56cfd37819357fc3076`  
		Last Modified: Thu, 17 Aug 2023 00:57:30 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:24596e0a78c74086b37ba3849d8ff0a8996a7c8e36debd69d7c134803422d375
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96178702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4547f6bfddeb7dbac716e3b8086d2fc79ada3d114f1c2a43a2b859cd99b5f4b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 04 Aug 2023 05:03:19 GMT
ARG RELEASE
# Fri, 04 Aug 2023 05:03:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 05:03:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 05:03:19 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 05:03:24 GMT
ADD file:ca783750060711e8590ab362921bae8d7b02201c48fa3d2cb3fdf6aac045a793 in / 
# Fri, 04 Aug 2023 05:03:25 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 05:37:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 21:47:40 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 16 Aug 2023 21:47:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 16 Aug 2023 21:47:41 GMT
ENV KAPACITOR_VERSION=1.5.9
# Wed, 16 Aug 2023 21:47:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 16 Aug 2023 21:47:46 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 16 Aug 2023 21:47:46 GMT
EXPOSE 9092
# Wed, 16 Aug 2023 21:47:46 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 16 Aug 2023 21:47:47 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 16 Aug 2023 21:47:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Aug 2023 21:47:47 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:24758824a30b6e1f6132a6b6740dec1fc5723821f0f2b5b6513379480e0f74f9`  
		Last Modified: Sat, 05 Aug 2023 02:03:56 GMT  
		Size: 27.0 MB (27029194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2bbdb113a0790e21df8c0b5f40836a9900213d1d697e6ea968456f1516e8ec`  
		Last Modified: Wed, 16 Aug 2023 05:51:53 GMT  
		Size: 7.0 MB (7019692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844457192377d239138f75424c4dc4c98759879601d71e1094e92fa6b7db7030`  
		Last Modified: Wed, 16 Aug 2023 21:47:58 GMT  
		Size: 27.3 MB (27326637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971a8d833e52d932189fcf10d3c4992ce5b80d148476db0081db9a0a5d2be746`  
		Last Modified: Wed, 16 Aug 2023 21:47:56 GMT  
		Size: 1.8 KB (1819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fd9c6c77def3e0950ebc781513abed5db8d72bc501b00affd9911b3f03121c`  
		Last Modified: Wed, 16 Aug 2023 21:48:00 GMT  
		Size: 34.8 MB (34800902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08eb617a76af3c28479072cf97bee02462cd9edb0e65add6527ae8bb18927da5`  
		Last Modified: Wed, 16 Aug 2023 21:47:56 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c98b84606b6c662e5212be144157c348ca884d1b1143a2db5bc8f79a605042a`  
		Last Modified: Wed, 16 Aug 2023 21:47:55 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:8ad598eaf9107118e08eb9e3c598271acfee0afd62ea5ce358c5a19f677870dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98886453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d5e0399af95e16d58b1f5c7990e658916b3afbfe099d2c640f85e9f9e07ee0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 04 Aug 2023 04:51:14 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:51:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:51:18 GMT
ADD file:5cf7797cf86362218d2bd85debeff136ee897af7eef95a0b8baab9f9457c3e89 in / 
# Fri, 04 Aug 2023 04:51:18 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 01:28:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 23:20:47 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 16 Aug 2023 23:20:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 16 Aug 2023 23:20:48 GMT
ENV KAPACITOR_VERSION=1.5.9
# Wed, 16 Aug 2023 23:20:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 16 Aug 2023 23:20:52 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 16 Aug 2023 23:20:53 GMT
EXPOSE 9092
# Wed, 16 Aug 2023 23:20:53 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 16 Aug 2023 23:20:53 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 16 Aug 2023 23:20:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Aug 2023 23:20:53 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:9ea365e1e52efb9567c56f02f2200f0e95ddffd579225cc5b20a6333119d2811`  
		Last Modified: Fri, 04 Aug 2023 13:35:19 GMT  
		Size: 28.4 MB (28391903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a1fcb60c8beda77ecd71dcfb3b3564d3a6ac8f00400bfb5b94c463aa514292`  
		Last Modified: Wed, 16 Aug 2023 01:42:00 GMT  
		Size: 7.1 MB (7066534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac657cdd1f3b8a02fb53faa61ea9ae7e08b98aeeab797018c7940fa481bff626`  
		Last Modified: Wed, 16 Aug 2023 23:21:13 GMT  
		Size: 28.8 MB (28848789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7983bc8f3d5f14e5c627b4781d313a90a21f89f6a893b685e70334ff269c05e8`  
		Last Modified: Wed, 16 Aug 2023 23:21:10 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135c1d3b459aeebb472b458fc08673d67567d4a751a80a5a25833641931f05d7`  
		Last Modified: Wed, 16 Aug 2023 23:21:14 GMT  
		Size: 34.6 MB (34576967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d426b48994812953befe3e7b1d0a9e5959dfa2c4fa305f3b7e31cbab3c079a`  
		Last Modified: Wed, 16 Aug 2023 23:21:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed6c911bd8eb6896a0868032eb732a9e04b90924faf187d3de2fa67d9e26500`  
		Last Modified: Wed, 16 Aug 2023 23:21:11 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5-alpine`

```console
$ docker pull kapacitor@sha256:2d4571bbd7f39b054949f82034b3d529b2bc0ccf3889e2e72a592d8560d57f7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.5-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:32b8cb0e1e1e3fda8e954b79cbe4e15272e04ba7427f841b22dff8cf0818ffcd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22655711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552ce7bbe44c57a5913883fc98455db619d77b2a7bd7fdd412bbaa408e6b1f70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:37 GMT
ADD file:9663235f252e072c52b0f9e25845841e4321cce2caa7467a0d736c6003b05c00 in / 
# Wed, 29 Mar 2023 18:19:37 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 22:13:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 29 Mar 2023 22:13:18 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 29 Mar 2023 22:13:18 GMT
ENV KAPACITOR_VERSION=1.5.9
# Fri, 28 Apr 2023 23:22:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 28 Apr 2023 23:22:49 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 28 Apr 2023 23:22:49 GMT
EXPOSE 9092
# Fri, 28 Apr 2023 23:22:49 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 28 Apr 2023 23:22:49 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Fri, 28 Apr 2023 23:22:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Apr 2023 23:22:49 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f7dab3ab2d6ec29aa28769bec35331fb485b5837501b1e8556413d8b5a79c9c8`  
		Last Modified: Wed, 29 Mar 2023 18:20:25 GMT  
		Size: 2.8 MB (2829647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4def2ae1fee272a0a418749677679ac1c48b9f3e46f04d5e3d55629dbd23b873`  
		Last Modified: Fri, 28 Apr 2023 23:23:37 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3f0ea5f775510249983621f9e6d068315844c260e3ba78b54aa1e37c75da71`  
		Last Modified: Fri, 28 Apr 2023 23:23:37 GMT  
		Size: 284.6 KB (284590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e220a492f7218c87ce3c9e0650aadb41b9e6d0be6381444ca3cf4179c7096910`  
		Last Modified: Fri, 28 Apr 2023 23:23:40 GMT  
		Size: 19.5 MB (19540839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fbec329944aaf6c9f89ae7cece3270108a31045736265d990cb08932d5df88`  
		Last Modified: Fri, 28 Apr 2023 23:23:37 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9883d7baa7fdbc3080e127193f17ee34fa171270d67405174661e523128960fe`  
		Last Modified: Fri, 28 Apr 2023 23:23:37 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5.9`

```console
$ docker pull kapacitor@sha256:60ee3a59dac9f6c2e84868fb155be44f64ac709bd97e32a505b80ecbd72b67af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.5.9` - linux; amd64

```console
$ docker pull kapacitor@sha256:55578eb4f2e49e4d61ff15af35392be9ba1793e356cd59e2de72131361f13cf2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105545860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a896f193230ea407a067190030be7bdc620e1763d812b1894cec307bd7c9288`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 04 Aug 2023 04:52:57 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:52:59 GMT
ADD file:bb1fa1d9d012ae826908afdce8c9fa2feebf221b2ab032e1535255905144411a in / 
# Fri, 04 Aug 2023 04:53:00 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 07:04:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 00:56:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 17 Aug 2023 00:56:59 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 17 Aug 2023 00:56:59 GMT
ENV KAPACITOR_VERSION=1.5.9
# Thu, 17 Aug 2023 00:57:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 17 Aug 2023 00:57:04 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 17 Aug 2023 00:57:04 GMT
EXPOSE 9092
# Thu, 17 Aug 2023 00:57:04 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 17 Aug 2023 00:57:04 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 17 Aug 2023 00:57:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Aug 2023 00:57:04 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:99de9192b4afd13ed65aeae58d55b38e5231eb97a743921357b7d5b4c0c903c4`  
		Last Modified: Fri, 04 Aug 2023 09:25:19 GMT  
		Size: 30.4 MB (30437960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20f6742b7f13e48b26c74db979ec9995cd72f6fdc3a6b12a961ade1b6f63bf0`  
		Last Modified: Wed, 16 Aug 2023 07:16:45 GMT  
		Size: 7.1 MB (7119955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97294567ad405a596b8dc90345ba1a5007ef7b68d732a89ed4bf47793cc83a77`  
		Last Modified: Thu, 17 Aug 2023 00:57:33 GMT  
		Size: 30.8 MB (30751936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe018c5dda6ec4a52a3a7b6eefbc61a4be90bb9cd8c45233dfbf7fd6d8f20f2`  
		Last Modified: Thu, 17 Aug 2023 00:57:31 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752a1e8424e652cf7da548e3185b3ffa14d952db9241797459b8fe9387d67629`  
		Last Modified: Thu, 17 Aug 2023 00:57:35 GMT  
		Size: 37.2 MB (37233738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8011c61d64189689fe3c43676d20c89e391b5a946450dfe501b7046a07458bd`  
		Last Modified: Thu, 17 Aug 2023 00:57:30 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c94b327e18af1c9dbd35f25a486b74fea538d6d73fa56cfd37819357fc3076`  
		Last Modified: Thu, 17 Aug 2023 00:57:30 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5.9` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:24596e0a78c74086b37ba3849d8ff0a8996a7c8e36debd69d7c134803422d375
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96178702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4547f6bfddeb7dbac716e3b8086d2fc79ada3d114f1c2a43a2b859cd99b5f4b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 04 Aug 2023 05:03:19 GMT
ARG RELEASE
# Fri, 04 Aug 2023 05:03:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 05:03:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 05:03:19 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 05:03:24 GMT
ADD file:ca783750060711e8590ab362921bae8d7b02201c48fa3d2cb3fdf6aac045a793 in / 
# Fri, 04 Aug 2023 05:03:25 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 05:37:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 21:47:40 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 16 Aug 2023 21:47:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 16 Aug 2023 21:47:41 GMT
ENV KAPACITOR_VERSION=1.5.9
# Wed, 16 Aug 2023 21:47:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 16 Aug 2023 21:47:46 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 16 Aug 2023 21:47:46 GMT
EXPOSE 9092
# Wed, 16 Aug 2023 21:47:46 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 16 Aug 2023 21:47:47 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 16 Aug 2023 21:47:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Aug 2023 21:47:47 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:24758824a30b6e1f6132a6b6740dec1fc5723821f0f2b5b6513379480e0f74f9`  
		Last Modified: Sat, 05 Aug 2023 02:03:56 GMT  
		Size: 27.0 MB (27029194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca2bbdb113a0790e21df8c0b5f40836a9900213d1d697e6ea968456f1516e8ec`  
		Last Modified: Wed, 16 Aug 2023 05:51:53 GMT  
		Size: 7.0 MB (7019692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844457192377d239138f75424c4dc4c98759879601d71e1094e92fa6b7db7030`  
		Last Modified: Wed, 16 Aug 2023 21:47:58 GMT  
		Size: 27.3 MB (27326637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:971a8d833e52d932189fcf10d3c4992ce5b80d148476db0081db9a0a5d2be746`  
		Last Modified: Wed, 16 Aug 2023 21:47:56 GMT  
		Size: 1.8 KB (1819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fd9c6c77def3e0950ebc781513abed5db8d72bc501b00affd9911b3f03121c`  
		Last Modified: Wed, 16 Aug 2023 21:48:00 GMT  
		Size: 34.8 MB (34800902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08eb617a76af3c28479072cf97bee02462cd9edb0e65add6527ae8bb18927da5`  
		Last Modified: Wed, 16 Aug 2023 21:47:56 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c98b84606b6c662e5212be144157c348ca884d1b1143a2db5bc8f79a605042a`  
		Last Modified: Wed, 16 Aug 2023 21:47:55 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5.9` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:8ad598eaf9107118e08eb9e3c598271acfee0afd62ea5ce358c5a19f677870dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98886453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d5e0399af95e16d58b1f5c7990e658916b3afbfe099d2c640f85e9f9e07ee0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 04 Aug 2023 04:51:14 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:51:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:51:18 GMT
ADD file:5cf7797cf86362218d2bd85debeff136ee897af7eef95a0b8baab9f9457c3e89 in / 
# Fri, 04 Aug 2023 04:51:18 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 01:28:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 23:20:47 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 16 Aug 2023 23:20:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 16 Aug 2023 23:20:48 GMT
ENV KAPACITOR_VERSION=1.5.9
# Wed, 16 Aug 2023 23:20:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 16 Aug 2023 23:20:52 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 16 Aug 2023 23:20:53 GMT
EXPOSE 9092
# Wed, 16 Aug 2023 23:20:53 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 16 Aug 2023 23:20:53 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 16 Aug 2023 23:20:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Aug 2023 23:20:53 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:9ea365e1e52efb9567c56f02f2200f0e95ddffd579225cc5b20a6333119d2811`  
		Last Modified: Fri, 04 Aug 2023 13:35:19 GMT  
		Size: 28.4 MB (28391903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a1fcb60c8beda77ecd71dcfb3b3564d3a6ac8f00400bfb5b94c463aa514292`  
		Last Modified: Wed, 16 Aug 2023 01:42:00 GMT  
		Size: 7.1 MB (7066534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac657cdd1f3b8a02fb53faa61ea9ae7e08b98aeeab797018c7940fa481bff626`  
		Last Modified: Wed, 16 Aug 2023 23:21:13 GMT  
		Size: 28.8 MB (28848789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7983bc8f3d5f14e5c627b4781d313a90a21f89f6a893b685e70334ff269c05e8`  
		Last Modified: Wed, 16 Aug 2023 23:21:10 GMT  
		Size: 1.8 KB (1804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135c1d3b459aeebb472b458fc08673d67567d4a751a80a5a25833641931f05d7`  
		Last Modified: Wed, 16 Aug 2023 23:21:14 GMT  
		Size: 34.6 MB (34576967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d426b48994812953befe3e7b1d0a9e5959dfa2c4fa305f3b7e31cbab3c079a`  
		Last Modified: Wed, 16 Aug 2023 23:21:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed6c911bd8eb6896a0868032eb732a9e04b90924faf187d3de2fa67d9e26500`  
		Last Modified: Wed, 16 Aug 2023 23:21:11 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5.9-alpine`

```console
$ docker pull kapacitor@sha256:2d4571bbd7f39b054949f82034b3d529b2bc0ccf3889e2e72a592d8560d57f7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.5.9-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:32b8cb0e1e1e3fda8e954b79cbe4e15272e04ba7427f841b22dff8cf0818ffcd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22655711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552ce7bbe44c57a5913883fc98455db619d77b2a7bd7fdd412bbaa408e6b1f70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:37 GMT
ADD file:9663235f252e072c52b0f9e25845841e4321cce2caa7467a0d736c6003b05c00 in / 
# Wed, 29 Mar 2023 18:19:37 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 22:13:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 29 Mar 2023 22:13:18 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 29 Mar 2023 22:13:18 GMT
ENV KAPACITOR_VERSION=1.5.9
# Fri, 28 Apr 2023 23:22:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 28 Apr 2023 23:22:49 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 28 Apr 2023 23:22:49 GMT
EXPOSE 9092
# Fri, 28 Apr 2023 23:22:49 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 28 Apr 2023 23:22:49 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Fri, 28 Apr 2023 23:22:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Apr 2023 23:22:49 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f7dab3ab2d6ec29aa28769bec35331fb485b5837501b1e8556413d8b5a79c9c8`  
		Last Modified: Wed, 29 Mar 2023 18:20:25 GMT  
		Size: 2.8 MB (2829647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4def2ae1fee272a0a418749677679ac1c48b9f3e46f04d5e3d55629dbd23b873`  
		Last Modified: Fri, 28 Apr 2023 23:23:37 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3f0ea5f775510249983621f9e6d068315844c260e3ba78b54aa1e37c75da71`  
		Last Modified: Fri, 28 Apr 2023 23:23:37 GMT  
		Size: 284.6 KB (284590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e220a492f7218c87ce3c9e0650aadb41b9e6d0be6381444ca3cf4179c7096910`  
		Last Modified: Fri, 28 Apr 2023 23:23:40 GMT  
		Size: 19.5 MB (19540839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32fbec329944aaf6c9f89ae7cece3270108a31045736265d990cb08932d5df88`  
		Last Modified: Fri, 28 Apr 2023 23:23:37 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9883d7baa7fdbc3080e127193f17ee34fa171270d67405174661e523128960fe`  
		Last Modified: Fri, 28 Apr 2023 23:23:37 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.6`

```console
$ docker pull kapacitor@sha256:14de02ca326bec8f0642c044a92f39196c799f57cca1f7f41c34ed7677576ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:1.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:bf2da4c6bf2cf6379f169df8c09448662de55bf6623c7927e223b6c5b86807f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (133982815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54f8fbaf68a1ea9f9b6ae4462ff15e779854bb765fe7c571238f7d173086e6c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 04 Aug 2023 04:52:57 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:52:59 GMT
ADD file:bb1fa1d9d012ae826908afdce8c9fa2feebf221b2ab032e1535255905144411a in / 
# Fri, 04 Aug 2023 04:53:00 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 07:04:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 00:56:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 17 Aug 2023 00:57:10 GMT
ENV KAPACITOR_VERSION=1.6.6
# Thu, 17 Aug 2023 00:57:15 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 17 Aug 2023 00:57:15 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 17 Aug 2023 00:57:15 GMT
EXPOSE 9092
# Thu, 17 Aug 2023 00:57:15 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 17 Aug 2023 00:57:15 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 17 Aug 2023 00:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Aug 2023 00:57:16 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:99de9192b4afd13ed65aeae58d55b38e5231eb97a743921357b7d5b4c0c903c4`  
		Last Modified: Fri, 04 Aug 2023 09:25:19 GMT  
		Size: 30.4 MB (30437960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20f6742b7f13e48b26c74db979ec9995cd72f6fdc3a6b12a961ade1b6f63bf0`  
		Last Modified: Wed, 16 Aug 2023 07:16:45 GMT  
		Size: 7.1 MB (7119955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97294567ad405a596b8dc90345ba1a5007ef7b68d732a89ed4bf47793cc83a77`  
		Last Modified: Thu, 17 Aug 2023 00:57:33 GMT  
		Size: 30.8 MB (30751936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca019051ea2d85c5ca9b24e5eaa31f017f7ca24983e5086b82fad93ef7e9f34`  
		Last Modified: Thu, 17 Aug 2023 00:57:52 GMT  
		Size: 65.7 MB (65672508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585d774b8a33b2a7bea064f7a923add1fb128295c564324ecb03b122217ebfb6`  
		Last Modified: Thu, 17 Aug 2023 00:57:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbf8ecc1e0c4deeb7b79e4ec8acb7b1dc455ebcf4222aad4e6582edd880f36c`  
		Last Modified: Thu, 17 Aug 2023 00:57:45 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:49a9316c3f28f9970f7f224ff419ca3740fbd61497577abec233d2403ecd823e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (125978378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20b9285789cab2f19c569523933039b1eeb4d621a29c8b335b50898d6f17d28`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 04 Aug 2023 04:51:14 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:51:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:51:18 GMT
ADD file:5cf7797cf86362218d2bd85debeff136ee897af7eef95a0b8baab9f9457c3e89 in / 
# Fri, 04 Aug 2023 04:51:18 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 01:28:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 23:20:47 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 16 Aug 2023 23:20:56 GMT
ENV KAPACITOR_VERSION=1.6.6
# Wed, 16 Aug 2023 23:21:00 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 16 Aug 2023 23:21:01 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 16 Aug 2023 23:21:01 GMT
EXPOSE 9092
# Wed, 16 Aug 2023 23:21:01 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 16 Aug 2023 23:21:01 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 16 Aug 2023 23:21:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Aug 2023 23:21:01 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:9ea365e1e52efb9567c56f02f2200f0e95ddffd579225cc5b20a6333119d2811`  
		Last Modified: Fri, 04 Aug 2023 13:35:19 GMT  
		Size: 28.4 MB (28391903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a1fcb60c8beda77ecd71dcfb3b3564d3a6ac8f00400bfb5b94c463aa514292`  
		Last Modified: Wed, 16 Aug 2023 01:42:00 GMT  
		Size: 7.1 MB (7066534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac657cdd1f3b8a02fb53faa61ea9ae7e08b98aeeab797018c7940fa481bff626`  
		Last Modified: Wed, 16 Aug 2023 23:21:13 GMT  
		Size: 28.8 MB (28848789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5336f1f7ec59b2bb8362bab5387f0106444c28d3e12b6405a7e6880ac66d302f`  
		Last Modified: Wed, 16 Aug 2023 23:21:28 GMT  
		Size: 61.7 MB (61670697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8d8857c0728d2104cd4af42748ac6d99817ba5f545b21fcff03ba477857403`  
		Last Modified: Wed, 16 Aug 2023 23:21:22 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434e8eac20ad56b77ef7e1d16615c866cb3d5aa525ee00f967c1b16bfbce9517`  
		Last Modified: Wed, 16 Aug 2023 23:21:22 GMT  
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
$ docker pull kapacitor@sha256:14de02ca326bec8f0642c044a92f39196c799f57cca1f7f41c34ed7677576ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:1.6.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:bf2da4c6bf2cf6379f169df8c09448662de55bf6623c7927e223b6c5b86807f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (133982815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54f8fbaf68a1ea9f9b6ae4462ff15e779854bb765fe7c571238f7d173086e6c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 04 Aug 2023 04:52:57 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:52:59 GMT
ADD file:bb1fa1d9d012ae826908afdce8c9fa2feebf221b2ab032e1535255905144411a in / 
# Fri, 04 Aug 2023 04:53:00 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 07:04:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 00:56:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 17 Aug 2023 00:57:10 GMT
ENV KAPACITOR_VERSION=1.6.6
# Thu, 17 Aug 2023 00:57:15 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 17 Aug 2023 00:57:15 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 17 Aug 2023 00:57:15 GMT
EXPOSE 9092
# Thu, 17 Aug 2023 00:57:15 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 17 Aug 2023 00:57:15 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 17 Aug 2023 00:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Aug 2023 00:57:16 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:99de9192b4afd13ed65aeae58d55b38e5231eb97a743921357b7d5b4c0c903c4`  
		Last Modified: Fri, 04 Aug 2023 09:25:19 GMT  
		Size: 30.4 MB (30437960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20f6742b7f13e48b26c74db979ec9995cd72f6fdc3a6b12a961ade1b6f63bf0`  
		Last Modified: Wed, 16 Aug 2023 07:16:45 GMT  
		Size: 7.1 MB (7119955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97294567ad405a596b8dc90345ba1a5007ef7b68d732a89ed4bf47793cc83a77`  
		Last Modified: Thu, 17 Aug 2023 00:57:33 GMT  
		Size: 30.8 MB (30751936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca019051ea2d85c5ca9b24e5eaa31f017f7ca24983e5086b82fad93ef7e9f34`  
		Last Modified: Thu, 17 Aug 2023 00:57:52 GMT  
		Size: 65.7 MB (65672508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585d774b8a33b2a7bea064f7a923add1fb128295c564324ecb03b122217ebfb6`  
		Last Modified: Thu, 17 Aug 2023 00:57:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbf8ecc1e0c4deeb7b79e4ec8acb7b1dc455ebcf4222aad4e6582edd880f36c`  
		Last Modified: Thu, 17 Aug 2023 00:57:45 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.6.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:49a9316c3f28f9970f7f224ff419ca3740fbd61497577abec233d2403ecd823e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (125978378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20b9285789cab2f19c569523933039b1eeb4d621a29c8b335b50898d6f17d28`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 04 Aug 2023 04:51:14 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:51:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:51:18 GMT
ADD file:5cf7797cf86362218d2bd85debeff136ee897af7eef95a0b8baab9f9457c3e89 in / 
# Fri, 04 Aug 2023 04:51:18 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 01:28:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 23:20:47 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 16 Aug 2023 23:20:56 GMT
ENV KAPACITOR_VERSION=1.6.6
# Wed, 16 Aug 2023 23:21:00 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 16 Aug 2023 23:21:01 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 16 Aug 2023 23:21:01 GMT
EXPOSE 9092
# Wed, 16 Aug 2023 23:21:01 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 16 Aug 2023 23:21:01 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 16 Aug 2023 23:21:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Aug 2023 23:21:01 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:9ea365e1e52efb9567c56f02f2200f0e95ddffd579225cc5b20a6333119d2811`  
		Last Modified: Fri, 04 Aug 2023 13:35:19 GMT  
		Size: 28.4 MB (28391903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a1fcb60c8beda77ecd71dcfb3b3564d3a6ac8f00400bfb5b94c463aa514292`  
		Last Modified: Wed, 16 Aug 2023 01:42:00 GMT  
		Size: 7.1 MB (7066534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac657cdd1f3b8a02fb53faa61ea9ae7e08b98aeeab797018c7940fa481bff626`  
		Last Modified: Wed, 16 Aug 2023 23:21:13 GMT  
		Size: 28.8 MB (28848789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5336f1f7ec59b2bb8362bab5387f0106444c28d3e12b6405a7e6880ac66d302f`  
		Last Modified: Wed, 16 Aug 2023 23:21:28 GMT  
		Size: 61.7 MB (61670697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8d8857c0728d2104cd4af42748ac6d99817ba5f545b21fcff03ba477857403`  
		Last Modified: Wed, 16 Aug 2023 23:21:22 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434e8eac20ad56b77ef7e1d16615c866cb3d5aa525ee00f967c1b16bfbce9517`  
		Last Modified: Wed, 16 Aug 2023 23:21:22 GMT  
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
$ docker pull kapacitor@sha256:14de02ca326bec8f0642c044a92f39196c799f57cca1f7f41c34ed7677576ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:bf2da4c6bf2cf6379f169df8c09448662de55bf6623c7927e223b6c5b86807f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (133982815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54f8fbaf68a1ea9f9b6ae4462ff15e779854bb765fe7c571238f7d173086e6c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 04 Aug 2023 04:52:57 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:52:58 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:52:59 GMT
ADD file:bb1fa1d9d012ae826908afdce8c9fa2feebf221b2ab032e1535255905144411a in / 
# Fri, 04 Aug 2023 04:53:00 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 07:04:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Aug 2023 00:56:58 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 17 Aug 2023 00:57:10 GMT
ENV KAPACITOR_VERSION=1.6.6
# Thu, 17 Aug 2023 00:57:15 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 17 Aug 2023 00:57:15 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 17 Aug 2023 00:57:15 GMT
EXPOSE 9092
# Thu, 17 Aug 2023 00:57:15 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 17 Aug 2023 00:57:15 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 17 Aug 2023 00:57:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 17 Aug 2023 00:57:16 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:99de9192b4afd13ed65aeae58d55b38e5231eb97a743921357b7d5b4c0c903c4`  
		Last Modified: Fri, 04 Aug 2023 09:25:19 GMT  
		Size: 30.4 MB (30437960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c20f6742b7f13e48b26c74db979ec9995cd72f6fdc3a6b12a961ade1b6f63bf0`  
		Last Modified: Wed, 16 Aug 2023 07:16:45 GMT  
		Size: 7.1 MB (7119955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97294567ad405a596b8dc90345ba1a5007ef7b68d732a89ed4bf47793cc83a77`  
		Last Modified: Thu, 17 Aug 2023 00:57:33 GMT  
		Size: 30.8 MB (30751936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca019051ea2d85c5ca9b24e5eaa31f017f7ca24983e5086b82fad93ef7e9f34`  
		Last Modified: Thu, 17 Aug 2023 00:57:52 GMT  
		Size: 65.7 MB (65672508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585d774b8a33b2a7bea064f7a923add1fb128295c564324ecb03b122217ebfb6`  
		Last Modified: Thu, 17 Aug 2023 00:57:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbf8ecc1e0c4deeb7b79e4ec8acb7b1dc455ebcf4222aad4e6582edd880f36c`  
		Last Modified: Thu, 17 Aug 2023 00:57:45 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:49a9316c3f28f9970f7f224ff419ca3740fbd61497577abec233d2403ecd823e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (125978378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20b9285789cab2f19c569523933039b1eeb4d621a29c8b335b50898d6f17d28`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 04 Aug 2023 04:51:14 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:51:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:51:18 GMT
ADD file:5cf7797cf86362218d2bd85debeff136ee897af7eef95a0b8baab9f9457c3e89 in / 
# Fri, 04 Aug 2023 04:51:18 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 01:28:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 23:20:47 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 16 Aug 2023 23:20:56 GMT
ENV KAPACITOR_VERSION=1.6.6
# Wed, 16 Aug 2023 23:21:00 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 16 Aug 2023 23:21:01 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 16 Aug 2023 23:21:01 GMT
EXPOSE 9092
# Wed, 16 Aug 2023 23:21:01 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 16 Aug 2023 23:21:01 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 16 Aug 2023 23:21:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Aug 2023 23:21:01 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:9ea365e1e52efb9567c56f02f2200f0e95ddffd579225cc5b20a6333119d2811`  
		Last Modified: Fri, 04 Aug 2023 13:35:19 GMT  
		Size: 28.4 MB (28391903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a1fcb60c8beda77ecd71dcfb3b3564d3a6ac8f00400bfb5b94c463aa514292`  
		Last Modified: Wed, 16 Aug 2023 01:42:00 GMT  
		Size: 7.1 MB (7066534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac657cdd1f3b8a02fb53faa61ea9ae7e08b98aeeab797018c7940fa481bff626`  
		Last Modified: Wed, 16 Aug 2023 23:21:13 GMT  
		Size: 28.8 MB (28848789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5336f1f7ec59b2bb8362bab5387f0106444c28d3e12b6405a7e6880ac66d302f`  
		Last Modified: Wed, 16 Aug 2023 23:21:28 GMT  
		Size: 61.7 MB (61670697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8d8857c0728d2104cd4af42748ac6d99817ba5f545b21fcff03ba477857403`  
		Last Modified: Wed, 16 Aug 2023 23:21:22 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434e8eac20ad56b77ef7e1d16615c866cb3d5aa525ee00f967c1b16bfbce9517`  
		Last Modified: Wed, 16 Aug 2023 23:21:22 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
