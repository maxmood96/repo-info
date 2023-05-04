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
$ docker pull kapacitor@sha256:a3a78ac0449f54579ba5d69472c16fe75d2be19905393f83d08ba50f0da88331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.5` - linux; amd64

```console
$ docker pull kapacitor@sha256:a358d3a92e40341d8bc3023459b2a1992f6f5b34f6f8ae7d2289426a27d083e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.1 MB (106141288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10ae42c2ad0cbaa53ecfa9eb900cd773e4628a3ef6a47af12f95d309248914d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
# Tue, 02 May 2023 23:26:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 16:09:21 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 03 May 2023 16:09:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 03 May 2023 16:09:23 GMT
ENV KAPACITOR_VERSION=1.5.9
# Wed, 03 May 2023 16:09:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 03 May 2023 16:09:27 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 03 May 2023 16:09:27 GMT
EXPOSE 9092
# Wed, 03 May 2023 16:09:27 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 03 May 2023 16:09:27 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 03 May 2023 16:09:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 May 2023 16:09:27 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:74ac377868f863e123f24c409f79709f7563fa464557c36a09cf6f85c8b92b7f`  
		Last Modified: Wed, 08 Mar 2023 09:03:15 GMT  
		Size: 30.4 MB (30429963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade6d81308cf88645476bddfaa8c5c2be767c77660b156a2bc5e740cd906431b`  
		Last Modified: Tue, 02 May 2023 23:43:33 GMT  
		Size: 7.1 MB (7123825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb507a78420a94908f02595d22f75332c5c8693df6cd0154f4e78a78ec2c12f2`  
		Last Modified: Wed, 03 May 2023 16:09:58 GMT  
		Size: 31.4 MB (31351810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb81e302e1955811630efd33259ba9a8358b5e7c2558242943d7291ec0f8cd9f`  
		Last Modified: Wed, 03 May 2023 16:09:55 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab73c608a4d388fa3539471b9d70a72d0614cc0a8f220f4b32499d31f46bf85`  
		Last Modified: Wed, 03 May 2023 16:10:00 GMT  
		Size: 37.2 MB (37233440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1d9adada2985946ccf06d8a7231e31bebf58a0ddc2bb27aa53f70d6b543e616`  
		Last Modified: Wed, 03 May 2023 16:09:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81479b1c5175bfde4b5406c0a8b09e54bbffd7d85035badae694012d0d86b678`  
		Last Modified: Wed, 03 May 2023 16:09:55 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:6d419eb8cd7da150eb2b40fd4c700ba917538ef1cb830f5bbc6228022d21339e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96076818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4845cc4f47e03da19de5a0154d7d56745e6d26330a7be19cc566c65a90225b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 25 Apr 2023 17:36:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:36:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:36:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:36:58 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:37:01 GMT
ADD file:08f4534e90f8ffc3bdb6cf9c04b599190ea4e1d39328135a84f4ffcd614bacb4 in / 
# Tue, 25 Apr 2023 17:37:01 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 21:58:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:48:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 04 May 2023 07:48:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 04 May 2023 07:48:16 GMT
ENV KAPACITOR_VERSION=1.5.9
# Thu, 04 May 2023 07:48:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 04 May 2023 07:48:20 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 04 May 2023 07:48:20 GMT
EXPOSE 9092
# Thu, 04 May 2023 07:48:20 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 04 May 2023 07:48:20 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 04 May 2023 07:48:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 May 2023 07:48:20 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:2561bae7e5e30e2beaf0cb6907571e792834948f12d2a8923229e5ac85134ad4`  
		Last Modified: Wed, 26 Apr 2023 02:07:55 GMT  
		Size: 27.0 MB (27026323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1264745a6a9fbe384016935dc15692bcaf1145b27f43d85dc345298e09a97678`  
		Last Modified: Wed, 03 May 2023 22:12:00 GMT  
		Size: 7.0 MB (7023054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06f914ccd1e8ef7cfadba40edf53b6f2499e16182946494b363a3cdaf9292326`  
		Last Modified: Thu, 04 May 2023 07:48:31 GMT  
		Size: 27.2 MB (27224362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30c2132f12efc47a0534f2a4e607ccfc74bb079e2bc0e14072a920c80bb07e4`  
		Last Modified: Thu, 04 May 2023 07:48:28 GMT  
		Size: 1.8 KB (1810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc472e70dd728dd3752eff7dcb77c5d7e10128982a5004b11649788a46d29595`  
		Last Modified: Thu, 04 May 2023 07:48:33 GMT  
		Size: 34.8 MB (34800810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dfcd2b84022e88f516843f57a54a222d755c49454d8b7ffe6c781882add4652`  
		Last Modified: Thu, 04 May 2023 07:48:28 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b698c3d9cbf6d6d2bdb784a496ddfb35c2c64c5d068dadef6383585693649736`  
		Last Modified: Thu, 04 May 2023 07:48:28 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:5be2579948aa64f5825855f8b32b538ae5abe5b195aa3fc4875dd7488fe746ff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98906707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b219371ea93a3f1a5edf9d59acde3945f792dc644fe62520e4d65164d6e1e213`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 17:26:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 04:35:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 04 May 2023 04:35:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 04 May 2023 04:35:32 GMT
ENV KAPACITOR_VERSION=1.5.9
# Thu, 04 May 2023 04:35:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 04 May 2023 04:35:35 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 04 May 2023 04:35:35 GMT
EXPOSE 9092
# Thu, 04 May 2023 04:35:35 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 04 May 2023 04:35:35 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 04 May 2023 04:35:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 May 2023 04:35:35 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d63a83193f4bc7a9b83920cc4a68812d1d201a1835ad44e420fd5d3baed6c48`  
		Last Modified: Wed, 03 May 2023 17:39:44 GMT  
		Size: 7.1 MB (7066176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794d1c6b739e0fa8c10cf2cdb6bcd0289067a9890626fbfe83eba38df4bcdd60`  
		Last Modified: Thu, 04 May 2023 04:35:51 GMT  
		Size: 28.9 MB (28873025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7aae2717e2d0020561c6e06075f3030bb9c417fc6a8c4a30990f6f9f3662d5`  
		Last Modified: Thu, 04 May 2023 04:35:49 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea17e3d291719634a138d67b80fda9706ef88854ca23b1a023b87cccc89831fa`  
		Last Modified: Thu, 04 May 2023 04:35:53 GMT  
		Size: 34.6 MB (34575801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4d50619bf4a0b4f73b1760167cfb7ace2e7c7c5e73d791f93ef4bb7902b135`  
		Last Modified: Thu, 04 May 2023 04:35:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94008dea653f0fb4347483cf960622d6b7eaa140a2addbd67345dcd3c6d8b247`  
		Last Modified: Thu, 04 May 2023 04:35:49 GMT  
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
$ docker pull kapacitor@sha256:a3a78ac0449f54579ba5d69472c16fe75d2be19905393f83d08ba50f0da88331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.5.9` - linux; amd64

```console
$ docker pull kapacitor@sha256:a358d3a92e40341d8bc3023459b2a1992f6f5b34f6f8ae7d2289426a27d083e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.1 MB (106141288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10ae42c2ad0cbaa53ecfa9eb900cd773e4628a3ef6a47af12f95d309248914d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
# Tue, 02 May 2023 23:26:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 16:09:21 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 03 May 2023 16:09:23 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 03 May 2023 16:09:23 GMT
ENV KAPACITOR_VERSION=1.5.9
# Wed, 03 May 2023 16:09:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 03 May 2023 16:09:27 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 03 May 2023 16:09:27 GMT
EXPOSE 9092
# Wed, 03 May 2023 16:09:27 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 03 May 2023 16:09:27 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 03 May 2023 16:09:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 May 2023 16:09:27 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:74ac377868f863e123f24c409f79709f7563fa464557c36a09cf6f85c8b92b7f`  
		Last Modified: Wed, 08 Mar 2023 09:03:15 GMT  
		Size: 30.4 MB (30429963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade6d81308cf88645476bddfaa8c5c2be767c77660b156a2bc5e740cd906431b`  
		Last Modified: Tue, 02 May 2023 23:43:33 GMT  
		Size: 7.1 MB (7123825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb507a78420a94908f02595d22f75332c5c8693df6cd0154f4e78a78ec2c12f2`  
		Last Modified: Wed, 03 May 2023 16:09:58 GMT  
		Size: 31.4 MB (31351810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb81e302e1955811630efd33259ba9a8358b5e7c2558242943d7291ec0f8cd9f`  
		Last Modified: Wed, 03 May 2023 16:09:55 GMT  
		Size: 1.8 KB (1796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab73c608a4d388fa3539471b9d70a72d0614cc0a8f220f4b32499d31f46bf85`  
		Last Modified: Wed, 03 May 2023 16:10:00 GMT  
		Size: 37.2 MB (37233440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1d9adada2985946ccf06d8a7231e31bebf58a0ddc2bb27aa53f70d6b543e616`  
		Last Modified: Wed, 03 May 2023 16:09:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81479b1c5175bfde4b5406c0a8b09e54bbffd7d85035badae694012d0d86b678`  
		Last Modified: Wed, 03 May 2023 16:09:55 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5.9` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:6d419eb8cd7da150eb2b40fd4c700ba917538ef1cb830f5bbc6228022d21339e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96076818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4845cc4f47e03da19de5a0154d7d56745e6d26330a7be19cc566c65a90225b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 25 Apr 2023 17:36:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:36:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:36:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:36:58 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:37:01 GMT
ADD file:08f4534e90f8ffc3bdb6cf9c04b599190ea4e1d39328135a84f4ffcd614bacb4 in / 
# Tue, 25 Apr 2023 17:37:01 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 21:58:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 07:48:15 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 04 May 2023 07:48:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 04 May 2023 07:48:16 GMT
ENV KAPACITOR_VERSION=1.5.9
# Thu, 04 May 2023 07:48:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 04 May 2023 07:48:20 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 04 May 2023 07:48:20 GMT
EXPOSE 9092
# Thu, 04 May 2023 07:48:20 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 04 May 2023 07:48:20 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 04 May 2023 07:48:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 May 2023 07:48:20 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:2561bae7e5e30e2beaf0cb6907571e792834948f12d2a8923229e5ac85134ad4`  
		Last Modified: Wed, 26 Apr 2023 02:07:55 GMT  
		Size: 27.0 MB (27026323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1264745a6a9fbe384016935dc15692bcaf1145b27f43d85dc345298e09a97678`  
		Last Modified: Wed, 03 May 2023 22:12:00 GMT  
		Size: 7.0 MB (7023054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06f914ccd1e8ef7cfadba40edf53b6f2499e16182946494b363a3cdaf9292326`  
		Last Modified: Thu, 04 May 2023 07:48:31 GMT  
		Size: 27.2 MB (27224362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30c2132f12efc47a0534f2a4e607ccfc74bb079e2bc0e14072a920c80bb07e4`  
		Last Modified: Thu, 04 May 2023 07:48:28 GMT  
		Size: 1.8 KB (1810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc472e70dd728dd3752eff7dcb77c5d7e10128982a5004b11649788a46d29595`  
		Last Modified: Thu, 04 May 2023 07:48:33 GMT  
		Size: 34.8 MB (34800810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dfcd2b84022e88f516843f57a54a222d755c49454d8b7ffe6c781882add4652`  
		Last Modified: Thu, 04 May 2023 07:48:28 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b698c3d9cbf6d6d2bdb784a496ddfb35c2c64c5d068dadef6383585693649736`  
		Last Modified: Thu, 04 May 2023 07:48:28 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5.9` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:5be2579948aa64f5825855f8b32b538ae5abe5b195aa3fc4875dd7488fe746ff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.9 MB (98906707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b219371ea93a3f1a5edf9d59acde3945f792dc644fe62520e4d65164d6e1e213`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 17:26:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 04:35:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 04 May 2023 04:35:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 04 May 2023 04:35:32 GMT
ENV KAPACITOR_VERSION=1.5.9
# Thu, 04 May 2023 04:35:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 04 May 2023 04:35:35 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 04 May 2023 04:35:35 GMT
EXPOSE 9092
# Thu, 04 May 2023 04:35:35 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 04 May 2023 04:35:35 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 04 May 2023 04:35:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 May 2023 04:35:35 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d63a83193f4bc7a9b83920cc4a68812d1d201a1835ad44e420fd5d3baed6c48`  
		Last Modified: Wed, 03 May 2023 17:39:44 GMT  
		Size: 7.1 MB (7066176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794d1c6b739e0fa8c10cf2cdb6bcd0289067a9890626fbfe83eba38df4bcdd60`  
		Last Modified: Thu, 04 May 2023 04:35:51 GMT  
		Size: 28.9 MB (28873025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7aae2717e2d0020561c6e06075f3030bb9c417fc6a8c4a30990f6f9f3662d5`  
		Last Modified: Thu, 04 May 2023 04:35:49 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea17e3d291719634a138d67b80fda9706ef88854ca23b1a023b87cccc89831fa`  
		Last Modified: Thu, 04 May 2023 04:35:53 GMT  
		Size: 34.6 MB (34575801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4d50619bf4a0b4f73b1760167cfb7ace2e7c7c5e73d791f93ef4bb7902b135`  
		Last Modified: Thu, 04 May 2023 04:35:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94008dea653f0fb4347483cf960622d6b7eaa140a2addbd67345dcd3c6d8b247`  
		Last Modified: Thu, 04 May 2023 04:35:49 GMT  
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
$ docker pull kapacitor@sha256:85f4d66137e23ef33c68f0dc38344a78e4cf5c1b62a2cec6224e98aa35babfbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:1.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:a4b03b00a2a79ddd0030143fe32c39ec8722b5eb6262eaa3d6e0278b62e73696
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134578250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48dbd6cef9c910481ef128df68501a0650fcbfcccb27106f370336706132bc6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
# Tue, 02 May 2023 23:26:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 16:09:21 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 03 May 2023 16:09:31 GMT
ENV KAPACITOR_VERSION=1.6.6
# Wed, 03 May 2023 16:09:42 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 03 May 2023 16:09:42 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 03 May 2023 16:09:42 GMT
EXPOSE 9092
# Wed, 03 May 2023 16:09:42 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 03 May 2023 16:09:42 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 03 May 2023 16:09:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 May 2023 16:09:42 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:74ac377868f863e123f24c409f79709f7563fa464557c36a09cf6f85c8b92b7f`  
		Last Modified: Wed, 08 Mar 2023 09:03:15 GMT  
		Size: 30.4 MB (30429963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade6d81308cf88645476bddfaa8c5c2be767c77660b156a2bc5e740cd906431b`  
		Last Modified: Tue, 02 May 2023 23:43:33 GMT  
		Size: 7.1 MB (7123825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb507a78420a94908f02595d22f75332c5c8693df6cd0154f4e78a78ec2c12f2`  
		Last Modified: Wed, 03 May 2023 16:09:58 GMT  
		Size: 31.4 MB (31351810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e0cd46b31d30fa84eb9b19625e6f729983f718960a32c93c5fe9cc8bd2e50c`  
		Last Modified: Wed, 03 May 2023 16:10:23 GMT  
		Size: 65.7 MB (65672194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c120ea54647ec099a9b19129b4b91135f5ddb6073750d64a731feca9b2c2dfd8`  
		Last Modified: Wed, 03 May 2023 16:10:15 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7cee67f7a88d03d99a4e6bbbadfd77e7964a038d55adcdcbb3408582942834`  
		Last Modified: Wed, 03 May 2023 16:10:15 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:ccbad14f6f29e1359be205a1f44f7a8d7789a66e125b54957287eb1ec7fa53e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (125998583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6861c655d03d23bdedd6debba6a926bee408b88a8c43774d813d2c1ff158024`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 17:26:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 04:35:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 04 May 2023 04:35:38 GMT
ENV KAPACITOR_VERSION=1.6.6
# Thu, 04 May 2023 04:35:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 04 May 2023 04:35:42 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 04 May 2023 04:35:42 GMT
EXPOSE 9092
# Thu, 04 May 2023 04:35:42 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 04 May 2023 04:35:42 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 04 May 2023 04:35:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 May 2023 04:35:43 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d63a83193f4bc7a9b83920cc4a68812d1d201a1835ad44e420fd5d3baed6c48`  
		Last Modified: Wed, 03 May 2023 17:39:44 GMT  
		Size: 7.1 MB (7066176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794d1c6b739e0fa8c10cf2cdb6bcd0289067a9890626fbfe83eba38df4bcdd60`  
		Last Modified: Thu, 04 May 2023 04:35:51 GMT  
		Size: 28.9 MB (28873025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77839c427eb747173165dfbef973f408a6fe250fe6bae52e65086a1fd4daec2c`  
		Last Modified: Thu, 04 May 2023 04:36:06 GMT  
		Size: 61.7 MB (61669485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca67377d0bebb900806f71c47d1efff8d4b32967b3e177b77a06b99329dd58b8`  
		Last Modified: Thu, 04 May 2023 04:36:00 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2debaca8f8cfb74b0f5211a504bbb5d2ee1f607ee6531e87f49621ceda9b99`  
		Last Modified: Thu, 04 May 2023 04:36:00 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.6-alpine`

```console
$ docker pull kapacitor@sha256:ae18d242a2c3e38dab667b058e6e1c1c32db3985089eb07bbff7a1124749fc48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:73bb692306ea33eecba6040c0e63819c1ae048c49186a6f2c80c7d3eb6cc2c0a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68673446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084421861cb41acf17a0a5c19fa524a1cd1b2233e96cbb6554bcae217c7543b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:28 GMT
ADD file:970e6b2578ef73457ffed1189e8ba128b0211cabd3174b8c7d3afd8fb58ad614 in / 
# Wed, 29 Mar 2023 18:19:28 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 22:13:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 29 Mar 2023 22:13:56 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 28 Apr 2023 23:23:01 GMT
ENV KAPACITOR_VERSION=1.6.6
# Fri, 28 Apr 2023 23:23:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 28 Apr 2023 23:23:12 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 28 Apr 2023 23:23:12 GMT
EXPOSE 9092
# Fri, 28 Apr 2023 23:23:12 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 28 Apr 2023 23:23:12 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Fri, 28 Apr 2023 23:23:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Apr 2023 23:23:13 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:91d30c5bc19582de1415b18f1ec5bcbf52a558b62cf6cc201c9669df9f748c22`  
		Last Modified: Wed, 29 Mar 2023 18:20:09 GMT  
		Size: 2.8 MB (2807803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562ec21068704bb8efd8a6db94153756f2ea649fc15b7a3d8c5ae495403deaff`  
		Last Modified: Fri, 28 Apr 2023 23:24:06 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d500101053a8592e41f90d59292cd74a1d55daea7ae9ae255f54f3c3b0bafa0`  
		Last Modified: Fri, 28 Apr 2023 23:24:07 GMT  
		Size: 284.8 KB (284768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f632df2bffbd0c0aef5f148bd642609bbd3769c3a2f68af212c24569fe3059`  
		Last Modified: Fri, 28 Apr 2023 23:24:14 GMT  
		Size: 65.6 MB (65580141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe03849db0a97866932a7b703905538b0d9190b841dbc50e49d72d1840cf605`  
		Last Modified: Fri, 28 Apr 2023 23:24:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f533d079920207448963e4c621b57d4b0faad5d7eabc65bf0171e777ec58e465`  
		Last Modified: Fri, 28 Apr 2023 23:24:07 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.6.6`

```console
$ docker pull kapacitor@sha256:85f4d66137e23ef33c68f0dc38344a78e4cf5c1b62a2cec6224e98aa35babfbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:1.6.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:a4b03b00a2a79ddd0030143fe32c39ec8722b5eb6262eaa3d6e0278b62e73696
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134578250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48dbd6cef9c910481ef128df68501a0650fcbfcccb27106f370336706132bc6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
# Tue, 02 May 2023 23:26:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 16:09:21 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 03 May 2023 16:09:31 GMT
ENV KAPACITOR_VERSION=1.6.6
# Wed, 03 May 2023 16:09:42 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 03 May 2023 16:09:42 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 03 May 2023 16:09:42 GMT
EXPOSE 9092
# Wed, 03 May 2023 16:09:42 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 03 May 2023 16:09:42 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 03 May 2023 16:09:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 May 2023 16:09:42 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:74ac377868f863e123f24c409f79709f7563fa464557c36a09cf6f85c8b92b7f`  
		Last Modified: Wed, 08 Mar 2023 09:03:15 GMT  
		Size: 30.4 MB (30429963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade6d81308cf88645476bddfaa8c5c2be767c77660b156a2bc5e740cd906431b`  
		Last Modified: Tue, 02 May 2023 23:43:33 GMT  
		Size: 7.1 MB (7123825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb507a78420a94908f02595d22f75332c5c8693df6cd0154f4e78a78ec2c12f2`  
		Last Modified: Wed, 03 May 2023 16:09:58 GMT  
		Size: 31.4 MB (31351810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e0cd46b31d30fa84eb9b19625e6f729983f718960a32c93c5fe9cc8bd2e50c`  
		Last Modified: Wed, 03 May 2023 16:10:23 GMT  
		Size: 65.7 MB (65672194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c120ea54647ec099a9b19129b4b91135f5ddb6073750d64a731feca9b2c2dfd8`  
		Last Modified: Wed, 03 May 2023 16:10:15 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7cee67f7a88d03d99a4e6bbbadfd77e7964a038d55adcdcbb3408582942834`  
		Last Modified: Wed, 03 May 2023 16:10:15 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.6.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:ccbad14f6f29e1359be205a1f44f7a8d7789a66e125b54957287eb1ec7fa53e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (125998583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6861c655d03d23bdedd6debba6a926bee408b88a8c43774d813d2c1ff158024`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 17:26:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 04:35:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 04 May 2023 04:35:38 GMT
ENV KAPACITOR_VERSION=1.6.6
# Thu, 04 May 2023 04:35:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 04 May 2023 04:35:42 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 04 May 2023 04:35:42 GMT
EXPOSE 9092
# Thu, 04 May 2023 04:35:42 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 04 May 2023 04:35:42 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 04 May 2023 04:35:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 May 2023 04:35:43 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d63a83193f4bc7a9b83920cc4a68812d1d201a1835ad44e420fd5d3baed6c48`  
		Last Modified: Wed, 03 May 2023 17:39:44 GMT  
		Size: 7.1 MB (7066176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794d1c6b739e0fa8c10cf2cdb6bcd0289067a9890626fbfe83eba38df4bcdd60`  
		Last Modified: Thu, 04 May 2023 04:35:51 GMT  
		Size: 28.9 MB (28873025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77839c427eb747173165dfbef973f408a6fe250fe6bae52e65086a1fd4daec2c`  
		Last Modified: Thu, 04 May 2023 04:36:06 GMT  
		Size: 61.7 MB (61669485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca67377d0bebb900806f71c47d1efff8d4b32967b3e177b77a06b99329dd58b8`  
		Last Modified: Thu, 04 May 2023 04:36:00 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2debaca8f8cfb74b0f5211a504bbb5d2ee1f607ee6531e87f49621ceda9b99`  
		Last Modified: Thu, 04 May 2023 04:36:00 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.6.6-alpine`

```console
$ docker pull kapacitor@sha256:ae18d242a2c3e38dab667b058e6e1c1c32db3985089eb07bbff7a1124749fc48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.6.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:73bb692306ea33eecba6040c0e63819c1ae048c49186a6f2c80c7d3eb6cc2c0a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68673446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084421861cb41acf17a0a5c19fa524a1cd1b2233e96cbb6554bcae217c7543b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:28 GMT
ADD file:970e6b2578ef73457ffed1189e8ba128b0211cabd3174b8c7d3afd8fb58ad614 in / 
# Wed, 29 Mar 2023 18:19:28 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 22:13:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 29 Mar 2023 22:13:56 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 28 Apr 2023 23:23:01 GMT
ENV KAPACITOR_VERSION=1.6.6
# Fri, 28 Apr 2023 23:23:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 28 Apr 2023 23:23:12 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 28 Apr 2023 23:23:12 GMT
EXPOSE 9092
# Fri, 28 Apr 2023 23:23:12 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 28 Apr 2023 23:23:12 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Fri, 28 Apr 2023 23:23:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Apr 2023 23:23:13 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:91d30c5bc19582de1415b18f1ec5bcbf52a558b62cf6cc201c9669df9f748c22`  
		Last Modified: Wed, 29 Mar 2023 18:20:09 GMT  
		Size: 2.8 MB (2807803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562ec21068704bb8efd8a6db94153756f2ea649fc15b7a3d8c5ae495403deaff`  
		Last Modified: Fri, 28 Apr 2023 23:24:06 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d500101053a8592e41f90d59292cd74a1d55daea7ae9ae255f54f3c3b0bafa0`  
		Last Modified: Fri, 28 Apr 2023 23:24:07 GMT  
		Size: 284.8 KB (284768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f632df2bffbd0c0aef5f148bd642609bbd3769c3a2f68af212c24569fe3059`  
		Last Modified: Fri, 28 Apr 2023 23:24:14 GMT  
		Size: 65.6 MB (65580141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe03849db0a97866932a7b703905538b0d9190b841dbc50e49d72d1840cf605`  
		Last Modified: Fri, 28 Apr 2023 23:24:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f533d079920207448963e4c621b57d4b0faad5d7eabc65bf0171e777ec58e465`  
		Last Modified: Fri, 28 Apr 2023 23:24:07 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:ae18d242a2c3e38dab667b058e6e1c1c32db3985089eb07bbff7a1124749fc48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:73bb692306ea33eecba6040c0e63819c1ae048c49186a6f2c80c7d3eb6cc2c0a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68673446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084421861cb41acf17a0a5c19fa524a1cd1b2233e96cbb6554bcae217c7543b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:28 GMT
ADD file:970e6b2578ef73457ffed1189e8ba128b0211cabd3174b8c7d3afd8fb58ad614 in / 
# Wed, 29 Mar 2023 18:19:28 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 22:13:55 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 29 Mar 2023 22:13:56 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 28 Apr 2023 23:23:01 GMT
ENV KAPACITOR_VERSION=1.6.6
# Fri, 28 Apr 2023 23:23:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 28 Apr 2023 23:23:12 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 28 Apr 2023 23:23:12 GMT
EXPOSE 9092
# Fri, 28 Apr 2023 23:23:12 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 28 Apr 2023 23:23:12 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Fri, 28 Apr 2023 23:23:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Apr 2023 23:23:13 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:91d30c5bc19582de1415b18f1ec5bcbf52a558b62cf6cc201c9669df9f748c22`  
		Last Modified: Wed, 29 Mar 2023 18:20:09 GMT  
		Size: 2.8 MB (2807803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562ec21068704bb8efd8a6db94153756f2ea649fc15b7a3d8c5ae495403deaff`  
		Last Modified: Fri, 28 Apr 2023 23:24:06 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d500101053a8592e41f90d59292cd74a1d55daea7ae9ae255f54f3c3b0bafa0`  
		Last Modified: Fri, 28 Apr 2023 23:24:07 GMT  
		Size: 284.8 KB (284768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f632df2bffbd0c0aef5f148bd642609bbd3769c3a2f68af212c24569fe3059`  
		Last Modified: Fri, 28 Apr 2023 23:24:14 GMT  
		Size: 65.6 MB (65580141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe03849db0a97866932a7b703905538b0d9190b841dbc50e49d72d1840cf605`  
		Last Modified: Fri, 28 Apr 2023 23:24:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f533d079920207448963e4c621b57d4b0faad5d7eabc65bf0171e777ec58e465`  
		Last Modified: Fri, 28 Apr 2023 23:24:07 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:85f4d66137e23ef33c68f0dc38344a78e4cf5c1b62a2cec6224e98aa35babfbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:a4b03b00a2a79ddd0030143fe32c39ec8722b5eb6262eaa3d6e0278b62e73696
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134578250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48dbd6cef9c910481ef128df68501a0650fcbfcccb27106f370336706132bc6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 08 Mar 2023 04:44:25 GMT
ARG RELEASE
# Wed, 08 Mar 2023 04:44:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 08 Mar 2023 04:44:25 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 08 Mar 2023 04:44:27 GMT
ADD file:c8ef6447752cab2541ffca9e3cfa27d581f3491bc8f356f6eafd951243609341 in / 
# Wed, 08 Mar 2023 04:44:27 GMT
CMD ["/bin/bash"]
# Tue, 02 May 2023 23:26:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 16:09:21 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 03 May 2023 16:09:31 GMT
ENV KAPACITOR_VERSION=1.6.6
# Wed, 03 May 2023 16:09:42 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 03 May 2023 16:09:42 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 03 May 2023 16:09:42 GMT
EXPOSE 9092
# Wed, 03 May 2023 16:09:42 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 03 May 2023 16:09:42 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 03 May 2023 16:09:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 May 2023 16:09:42 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:74ac377868f863e123f24c409f79709f7563fa464557c36a09cf6f85c8b92b7f`  
		Last Modified: Wed, 08 Mar 2023 09:03:15 GMT  
		Size: 30.4 MB (30429963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade6d81308cf88645476bddfaa8c5c2be767c77660b156a2bc5e740cd906431b`  
		Last Modified: Tue, 02 May 2023 23:43:33 GMT  
		Size: 7.1 MB (7123825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb507a78420a94908f02595d22f75332c5c8693df6cd0154f4e78a78ec2c12f2`  
		Last Modified: Wed, 03 May 2023 16:09:58 GMT  
		Size: 31.4 MB (31351810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e0cd46b31d30fa84eb9b19625e6f729983f718960a32c93c5fe9cc8bd2e50c`  
		Last Modified: Wed, 03 May 2023 16:10:23 GMT  
		Size: 65.7 MB (65672194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c120ea54647ec099a9b19129b4b91135f5ddb6073750d64a731feca9b2c2dfd8`  
		Last Modified: Wed, 03 May 2023 16:10:15 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7cee67f7a88d03d99a4e6bbbadfd77e7964a038d55adcdcbb3408582942834`  
		Last Modified: Wed, 03 May 2023 16:10:15 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:ccbad14f6f29e1359be205a1f44f7a8d7789a66e125b54957287eb1ec7fa53e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.0 MB (125998583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6861c655d03d23bdedd6debba6a926bee408b88a8c43774d813d2c1ff158024`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 25 Apr 2023 17:31:58 GMT
ARG RELEASE
# Tue, 25 Apr 2023 17:31:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 25 Apr 2023 17:31:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 25 Apr 2023 17:31:59 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 25 Apr 2023 17:32:02 GMT
ADD file:aee0d7770ef2f24dc9697e86d391529d001a4013b6e30a3ac90a57932814a57e in / 
# Tue, 25 Apr 2023 17:32:02 GMT
CMD ["/bin/bash"]
# Wed, 03 May 2023 17:26:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 04 May 2023 04:35:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 04 May 2023 04:35:38 GMT
ENV KAPACITOR_VERSION=1.6.6
# Thu, 04 May 2023 04:35:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 04 May 2023 04:35:42 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 04 May 2023 04:35:42 GMT
EXPOSE 9092
# Thu, 04 May 2023 04:35:42 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 04 May 2023 04:35:42 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 04 May 2023 04:35:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 04 May 2023 04:35:43 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f3f60f415e9a03eed88bd5dd5268c841cde08dacf16911a3ef1e4e0fcdd76568`  
		Last Modified: Wed, 26 Apr 2023 02:08:37 GMT  
		Size: 28.4 MB (28389440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d63a83193f4bc7a9b83920cc4a68812d1d201a1835ad44e420fd5d3baed6c48`  
		Last Modified: Wed, 03 May 2023 17:39:44 GMT  
		Size: 7.1 MB (7066176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794d1c6b739e0fa8c10cf2cdb6bcd0289067a9890626fbfe83eba38df4bcdd60`  
		Last Modified: Thu, 04 May 2023 04:35:51 GMT  
		Size: 28.9 MB (28873025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77839c427eb747173165dfbef973f408a6fe250fe6bae52e65086a1fd4daec2c`  
		Last Modified: Thu, 04 May 2023 04:36:06 GMT  
		Size: 61.7 MB (61669485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca67377d0bebb900806f71c47d1efff8d4b32967b3e177b77a06b99329dd58b8`  
		Last Modified: Thu, 04 May 2023 04:36:00 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2debaca8f8cfb74b0f5211a504bbb5d2ee1f607ee6531e87f49621ceda9b99`  
		Last Modified: Thu, 04 May 2023 04:36:00 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
