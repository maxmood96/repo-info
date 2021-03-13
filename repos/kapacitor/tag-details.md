<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.4`](#kapacitor14)
-	[`kapacitor:1.4-alpine`](#kapacitor14-alpine)
-	[`kapacitor:1.4.1`](#kapacitor141)
-	[`kapacitor:1.4.1-alpine`](#kapacitor141-alpine)
-	[`kapacitor:1.5`](#kapacitor15)
-	[`kapacitor:1.5-alpine`](#kapacitor15-alpine)
-	[`kapacitor:1.5.8`](#kapacitor158)
-	[`kapacitor:1.5.8-alpine`](#kapacitor158-alpine)
-	[`kapacitor:alpine`](#kapacitoralpine)
-	[`kapacitor:latest`](#kapacitorlatest)

## `kapacitor:1.4`

```console
$ docker pull kapacitor@sha256:b27baec76a2102beb00547266cef6b29a76c7e602023c06d45aafe4cb797a4af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.4` - linux; amd64

```console
$ docker pull kapacitor@sha256:3328e06a1e611ea0fac1db6bca91676bc89fcddbe31df1d09b29ad1b5652a2f0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96931656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd61c469695baf96523efcc9e0b989c84a6dbf288420c05fe0efaee46df04921`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:39:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 04:59:47 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 10 Feb 2021 04:59:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 04:59:51 GMT
ENV KAPACITOR_VERSION=1.4.1
# Wed, 10 Feb 2021 04:59:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Wed, 10 Feb 2021 04:59:55 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 10 Feb 2021 04:59:55 GMT
EXPOSE 9092
# Wed, 10 Feb 2021 04:59:55 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 10 Feb 2021 04:59:55 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 10 Feb 2021 04:59:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 04:59:56 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0edb687a3dadde6ae013f9b8f08340de1f105266abe3081bba8e8939267978a`  
		Last Modified: Tue, 09 Feb 2021 04:48:28 GMT  
		Size: 11.3 MB (11268653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891892cc2ec4337be73614b6c3eecd8f1a1ac16eae254d1e4b6090358dd6782`  
		Last Modified: Tue, 09 Feb 2021 04:48:27 GMT  
		Size: 4.3 MB (4341906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931c232d0d40a12d9a9dc45b75237e4928a282b52b7cf165e95bde4a88af4066`  
		Last Modified: Wed, 10 Feb 2021 05:00:30 GMT  
		Size: 13.2 MB (13242862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8167b286365fbadf9e276748beeb19bfa326bcc3910c95777e5d951011784bd9`  
		Last Modified: Wed, 10 Feb 2021 05:00:29 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a3eed0ccf99e83bcc602cc2f1218cf3f4b0aa5492c00795742bf0c00e7005c`  
		Last Modified: Wed, 10 Feb 2021 05:00:34 GMT  
		Size: 22.7 MB (22695068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bdac07579b64ac8027b1fa8a26c71b6d2b1522981cf477a8d9562131f42c79`  
		Last Modified: Wed, 10 Feb 2021 05:00:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b03ebae3b6d21bece921423ee51a1b523d6b7cc485408f80092b75a93e62314`  
		Last Modified: Wed, 10 Feb 2021 05:00:29 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:315122205d82c3a141e12d04ab488f835fc755bbb8cf08b4ef6efb666305bc00
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.7 MB (90704834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:044074873bf960ee0f902ae4d33d39e836ddbef21c5fa93137f9d33676736d70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 12 Mar 2021 02:05:10 GMT
ADD file:36669d020402a086f914d75419118f4daa1cbeeed645c1a77fe62cac0e804b59 in / 
# Fri, 12 Mar 2021 02:05:15 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 03:39:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 03:40:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 23:58:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 12 Mar 2021 23:58:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 12 Mar 2021 23:58:41 GMT
ENV KAPACITOR_VERSION=1.4.1
# Fri, 12 Mar 2021 23:58:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Fri, 12 Mar 2021 23:58:50 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 12 Mar 2021 23:58:51 GMT
EXPOSE 9092
# Fri, 12 Mar 2021 23:58:52 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 12 Mar 2021 23:58:53 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 12 Mar 2021 23:58:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 23:58:56 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:87fcebbbbffa651ca8743935928db6e5acd0bef83a84d1dcc331b6a5dd2dd3a5`  
		Last Modified: Fri, 12 Mar 2021 02:14:09 GMT  
		Size: 42.1 MB (42120188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23db22a6953922b4d37e712f7abfd57e9d0b445d547049f3ae1aff068cd82b05`  
		Last Modified: Fri, 12 Mar 2021 03:50:06 GMT  
		Size: 9.9 MB (9915047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd48c000dbbac1ab4f6cc2b3bbdbd339981893df53383b9f000686f4a1c445b9`  
		Last Modified: Fri, 12 Mar 2021 03:50:04 GMT  
		Size: 3.9 MB (3921108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809ad9aef132fceff7737281929a2db9bd3c196470e9aa36662cace1baa2f9ae`  
		Last Modified: Fri, 12 Mar 2021 23:59:34 GMT  
		Size: 13.4 MB (13436171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c539ca111b42453d64e74d66b56a0ab7482a12a6445afad66021058266e5456d`  
		Last Modified: Fri, 12 Mar 2021 23:59:33 GMT  
		Size: 2.9 KB (2853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319be6635f00b23440045b7bc3dd2d6263e39fd9409e11476f77b994d572bd12`  
		Last Modified: Fri, 12 Mar 2021 23:59:41 GMT  
		Size: 21.3 MB (21309012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abef753a7cf3e0101fe6df1f60f65437095ff7927db3f8a144b8fa2c91a799e7`  
		Last Modified: Fri, 12 Mar 2021 23:59:32 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804fbe01f66d3fd9ff775aa2582cc41d8f9bba8375f20aa79211976488f98581`  
		Last Modified: Fri, 12 Mar 2021 23:59:32 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:4398de26903cde0bc726e4921d8909897cc81df390b7aabfc60eb8ae8c91f16c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91734069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1715ab7f802b1c8c58f0fcf92ff7e9e8f5c6238b4296c1ac54a98446629480ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 12 Mar 2021 01:56:48 GMT
ADD file:3d59786321ef76584460518105748706e36cd0b833f1d542702f9e238073f63b in / 
# Fri, 12 Mar 2021 01:56:54 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:36:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:36:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 19:49:13 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 12 Mar 2021 19:49:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 12 Mar 2021 19:49:19 GMT
ENV KAPACITOR_VERSION=1.4.1
# Fri, 12 Mar 2021 19:49:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Fri, 12 Mar 2021 19:49:26 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 12 Mar 2021 19:49:27 GMT
EXPOSE 9092
# Fri, 12 Mar 2021 19:49:28 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 12 Mar 2021 19:49:29 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 12 Mar 2021 19:49:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 19:49:32 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:690bb835f855da2bebb5afc2671951a9cafcaae8e3751eaa3ef8536058581b9d`  
		Last Modified: Fri, 12 Mar 2021 02:03:51 GMT  
		Size: 43.2 MB (43177463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8900d8bfcdd8c3d3bf8eef705080ae89efe5d9b24294b7d39c1c0d44f93dd47f`  
		Last Modified: Fri, 12 Mar 2021 02:46:19 GMT  
		Size: 10.2 MB (10184079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f83540a087edd442573d6168d03eb7e83cef27a2e34ece682ea441233733ce`  
		Last Modified: Fri, 12 Mar 2021 02:46:17 GMT  
		Size: 4.1 MB (4096643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177964681cdd6d6d609585eddaaa18ef8ca13dc4f54f7a8bce44329b18b0f47c`  
		Last Modified: Fri, 12 Mar 2021 19:50:20 GMT  
		Size: 13.0 MB (12964015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f8e7103b15f435a438c8111f28c1a29871aed06795b952c9ed1f9827cdc822`  
		Last Modified: Fri, 12 Mar 2021 19:50:18 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1307305943643ac11712d67690ec9923d71f6a115f0ab69b3e844d1f12dc41c1`  
		Last Modified: Fri, 12 Mar 2021 19:50:24 GMT  
		Size: 21.3 MB (21308559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c61f0130c88777b09865eacd2723cc1402dfbcbdf1f6a81c56063bc37e3bd4`  
		Last Modified: Fri, 12 Mar 2021 19:50:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36299ac46be373b41ce5c5697ac0090679ca75e0ee7b7a14520a2518bef0a910`  
		Last Modified: Fri, 12 Mar 2021 19:50:18 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.4-alpine`

```console
$ docker pull kapacitor@sha256:124ad603ce050e2138af72bb1fe2d5705f6c79b7177728841a383c1dfc609383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.4-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:4989420d153605957004f4907afb0e13cf488516ace47e7c843895f4b0a59704
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19679530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d832a90c74ff195db8622ee2f79fad1cff98b4014d21190fc9a509e0d20c42`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:21:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:59:21 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 24 Feb 2021 23:53:29 GMT
ENV KAPACITOR_VERSION=1.4.1
# Wed, 24 Feb 2021 23:53:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 24 Feb 2021 23:53:33 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 24 Feb 2021 23:53:34 GMT
EXPOSE 9092
# Wed, 24 Feb 2021 23:53:34 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 24 Feb 2021 23:53:34 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Wed, 24 Feb 2021 23:53:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 23:53:34 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c3c544bdbd838411be7288d5c8bd23d77b89d00730ce0fa218fd7fd1694b04`  
		Last Modified: Wed, 24 Feb 2021 20:24:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b4c4e91c477308692065de267dedc098ac76d0b4d02f27d7d3ff2d2ff35287`  
		Last Modified: Wed, 24 Feb 2021 21:00:31 GMT  
		Size: 280.9 KB (280902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351253078883f51a4bb37d52e468af530d009e34aa658a19583ad687cd335e4`  
		Last Modified: Wed, 24 Feb 2021 23:54:09 GMT  
		Size: 16.6 MB (16598528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfe37c2cd56067acab471f98a40813ab9cb159e1b6b8e54a3781189bc54cd35`  
		Last Modified: Wed, 24 Feb 2021 23:54:04 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcd1bc3ab0991fae06cce6f281bb3c6f4b7b90a7a052ca0c594fca72fa3d0df`  
		Last Modified: Wed, 24 Feb 2021 23:54:04 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.4.1`

```console
$ docker pull kapacitor@sha256:b27baec76a2102beb00547266cef6b29a76c7e602023c06d45aafe4cb797a4af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.4.1` - linux; amd64

```console
$ docker pull kapacitor@sha256:3328e06a1e611ea0fac1db6bca91676bc89fcddbe31df1d09b29ad1b5652a2f0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96931656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd61c469695baf96523efcc9e0b989c84a6dbf288420c05fe0efaee46df04921`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:39:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 04:59:47 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 10 Feb 2021 04:59:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 04:59:51 GMT
ENV KAPACITOR_VERSION=1.4.1
# Wed, 10 Feb 2021 04:59:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Wed, 10 Feb 2021 04:59:55 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 10 Feb 2021 04:59:55 GMT
EXPOSE 9092
# Wed, 10 Feb 2021 04:59:55 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 10 Feb 2021 04:59:55 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 10 Feb 2021 04:59:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 04:59:56 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0edb687a3dadde6ae013f9b8f08340de1f105266abe3081bba8e8939267978a`  
		Last Modified: Tue, 09 Feb 2021 04:48:28 GMT  
		Size: 11.3 MB (11268653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891892cc2ec4337be73614b6c3eecd8f1a1ac16eae254d1e4b6090358dd6782`  
		Last Modified: Tue, 09 Feb 2021 04:48:27 GMT  
		Size: 4.3 MB (4341906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931c232d0d40a12d9a9dc45b75237e4928a282b52b7cf165e95bde4a88af4066`  
		Last Modified: Wed, 10 Feb 2021 05:00:30 GMT  
		Size: 13.2 MB (13242862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8167b286365fbadf9e276748beeb19bfa326bcc3910c95777e5d951011784bd9`  
		Last Modified: Wed, 10 Feb 2021 05:00:29 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a3eed0ccf99e83bcc602cc2f1218cf3f4b0aa5492c00795742bf0c00e7005c`  
		Last Modified: Wed, 10 Feb 2021 05:00:34 GMT  
		Size: 22.7 MB (22695068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bdac07579b64ac8027b1fa8a26c71b6d2b1522981cf477a8d9562131f42c79`  
		Last Modified: Wed, 10 Feb 2021 05:00:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b03ebae3b6d21bece921423ee51a1b523d6b7cc485408f80092b75a93e62314`  
		Last Modified: Wed, 10 Feb 2021 05:00:29 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4.1` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:315122205d82c3a141e12d04ab488f835fc755bbb8cf08b4ef6efb666305bc00
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.7 MB (90704834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:044074873bf960ee0f902ae4d33d39e836ddbef21c5fa93137f9d33676736d70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 12 Mar 2021 02:05:10 GMT
ADD file:36669d020402a086f914d75419118f4daa1cbeeed645c1a77fe62cac0e804b59 in / 
# Fri, 12 Mar 2021 02:05:15 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 03:39:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 03:40:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 23:58:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 12 Mar 2021 23:58:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 12 Mar 2021 23:58:41 GMT
ENV KAPACITOR_VERSION=1.4.1
# Fri, 12 Mar 2021 23:58:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Fri, 12 Mar 2021 23:58:50 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 12 Mar 2021 23:58:51 GMT
EXPOSE 9092
# Fri, 12 Mar 2021 23:58:52 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 12 Mar 2021 23:58:53 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 12 Mar 2021 23:58:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 23:58:56 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:87fcebbbbffa651ca8743935928db6e5acd0bef83a84d1dcc331b6a5dd2dd3a5`  
		Last Modified: Fri, 12 Mar 2021 02:14:09 GMT  
		Size: 42.1 MB (42120188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23db22a6953922b4d37e712f7abfd57e9d0b445d547049f3ae1aff068cd82b05`  
		Last Modified: Fri, 12 Mar 2021 03:50:06 GMT  
		Size: 9.9 MB (9915047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd48c000dbbac1ab4f6cc2b3bbdbd339981893df53383b9f000686f4a1c445b9`  
		Last Modified: Fri, 12 Mar 2021 03:50:04 GMT  
		Size: 3.9 MB (3921108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809ad9aef132fceff7737281929a2db9bd3c196470e9aa36662cace1baa2f9ae`  
		Last Modified: Fri, 12 Mar 2021 23:59:34 GMT  
		Size: 13.4 MB (13436171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c539ca111b42453d64e74d66b56a0ab7482a12a6445afad66021058266e5456d`  
		Last Modified: Fri, 12 Mar 2021 23:59:33 GMT  
		Size: 2.9 KB (2853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319be6635f00b23440045b7bc3dd2d6263e39fd9409e11476f77b994d572bd12`  
		Last Modified: Fri, 12 Mar 2021 23:59:41 GMT  
		Size: 21.3 MB (21309012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abef753a7cf3e0101fe6df1f60f65437095ff7927db3f8a144b8fa2c91a799e7`  
		Last Modified: Fri, 12 Mar 2021 23:59:32 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804fbe01f66d3fd9ff775aa2582cc41d8f9bba8375f20aa79211976488f98581`  
		Last Modified: Fri, 12 Mar 2021 23:59:32 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.4.1` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:4398de26903cde0bc726e4921d8909897cc81df390b7aabfc60eb8ae8c91f16c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91734069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1715ab7f802b1c8c58f0fcf92ff7e9e8f5c6238b4296c1ac54a98446629480ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 12 Mar 2021 01:56:48 GMT
ADD file:3d59786321ef76584460518105748706e36cd0b833f1d542702f9e238073f63b in / 
# Fri, 12 Mar 2021 01:56:54 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:36:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:36:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 19:49:13 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 12 Mar 2021 19:49:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 12 Mar 2021 19:49:19 GMT
ENV KAPACITOR_VERSION=1.4.1
# Fri, 12 Mar 2021 19:49:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}_${ARCH}.deb*
# Fri, 12 Mar 2021 19:49:26 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 12 Mar 2021 19:49:27 GMT
EXPOSE 9092
# Fri, 12 Mar 2021 19:49:28 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 12 Mar 2021 19:49:29 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 12 Mar 2021 19:49:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 19:49:32 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:690bb835f855da2bebb5afc2671951a9cafcaae8e3751eaa3ef8536058581b9d`  
		Last Modified: Fri, 12 Mar 2021 02:03:51 GMT  
		Size: 43.2 MB (43177463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8900d8bfcdd8c3d3bf8eef705080ae89efe5d9b24294b7d39c1c0d44f93dd47f`  
		Last Modified: Fri, 12 Mar 2021 02:46:19 GMT  
		Size: 10.2 MB (10184079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f83540a087edd442573d6168d03eb7e83cef27a2e34ece682ea441233733ce`  
		Last Modified: Fri, 12 Mar 2021 02:46:17 GMT  
		Size: 4.1 MB (4096643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177964681cdd6d6d609585eddaaa18ef8ca13dc4f54f7a8bce44329b18b0f47c`  
		Last Modified: Fri, 12 Mar 2021 19:50:20 GMT  
		Size: 13.0 MB (12964015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f8e7103b15f435a438c8111f28c1a29871aed06795b952c9ed1f9827cdc822`  
		Last Modified: Fri, 12 Mar 2021 19:50:18 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1307305943643ac11712d67690ec9923d71f6a115f0ab69b3e844d1f12dc41c1`  
		Last Modified: Fri, 12 Mar 2021 19:50:24 GMT  
		Size: 21.3 MB (21308559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c61f0130c88777b09865eacd2723cc1402dfbcbdf1f6a81c56063bc37e3bd4`  
		Last Modified: Fri, 12 Mar 2021 19:50:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36299ac46be373b41ce5c5697ac0090679ca75e0ee7b7a14520a2518bef0a910`  
		Last Modified: Fri, 12 Mar 2021 19:50:18 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.4.1-alpine`

```console
$ docker pull kapacitor@sha256:124ad603ce050e2138af72bb1fe2d5705f6c79b7177728841a383c1dfc609383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.4.1-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:4989420d153605957004f4907afb0e13cf488516ace47e7c843895f4b0a59704
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19679530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d832a90c74ff195db8622ee2f79fad1cff98b4014d21190fc9a509e0d20c42`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:21:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:59:21 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 24 Feb 2021 23:53:29 GMT
ENV KAPACITOR_VERSION=1.4.1
# Wed, 24 Feb 2021 23:53:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 24 Feb 2021 23:53:33 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 24 Feb 2021 23:53:34 GMT
EXPOSE 9092
# Wed, 24 Feb 2021 23:53:34 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 24 Feb 2021 23:53:34 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Wed, 24 Feb 2021 23:53:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 23:53:34 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c3c544bdbd838411be7288d5c8bd23d77b89d00730ce0fa218fd7fd1694b04`  
		Last Modified: Wed, 24 Feb 2021 20:24:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b4c4e91c477308692065de267dedc098ac76d0b4d02f27d7d3ff2d2ff35287`  
		Last Modified: Wed, 24 Feb 2021 21:00:31 GMT  
		Size: 280.9 KB (280902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351253078883f51a4bb37d52e468af530d009e34aa658a19583ad687cd335e4`  
		Last Modified: Wed, 24 Feb 2021 23:54:09 GMT  
		Size: 16.6 MB (16598528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfe37c2cd56067acab471f98a40813ab9cb159e1b6b8e54a3781189bc54cd35`  
		Last Modified: Wed, 24 Feb 2021 23:54:04 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcd1bc3ab0991fae06cce6f281bb3c6f4b7b90a7a052ca0c594fca72fa3d0df`  
		Last Modified: Wed, 24 Feb 2021 23:54:04 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5`

```console
$ docker pull kapacitor@sha256:41e6b5a493ec6c7e0a7d426bf3f782ff978454308df71584e3baabaeaa44b2c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.5` - linux; amd64

```console
$ docker pull kapacitor@sha256:0dd0bdcb6cc90a0fa29af6394171ec4b3f732006dc1360ee919c249a19a2b903
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111410644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95490156d6f247eb05ca7c872ff5c4d8c7f0e1f32417828bf04db462334d10f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:39:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 04:59:47 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 10 Feb 2021 04:59:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 05:00:04 GMT
ENV KAPACITOR_VERSION=1.5.8
# Wed, 10 Feb 2021 05:00:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 10 Feb 2021 05:00:08 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 10 Feb 2021 05:00:09 GMT
EXPOSE 9092
# Wed, 10 Feb 2021 05:00:09 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 10 Feb 2021 05:00:09 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 10 Feb 2021 05:00:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 05:00:09 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0edb687a3dadde6ae013f9b8f08340de1f105266abe3081bba8e8939267978a`  
		Last Modified: Tue, 09 Feb 2021 04:48:28 GMT  
		Size: 11.3 MB (11268653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891892cc2ec4337be73614b6c3eecd8f1a1ac16eae254d1e4b6090358dd6782`  
		Last Modified: Tue, 09 Feb 2021 04:48:27 GMT  
		Size: 4.3 MB (4341906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931c232d0d40a12d9a9dc45b75237e4928a282b52b7cf165e95bde4a88af4066`  
		Last Modified: Wed, 10 Feb 2021 05:00:30 GMT  
		Size: 13.2 MB (13242862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8167b286365fbadf9e276748beeb19bfa326bcc3910c95777e5d951011784bd9`  
		Last Modified: Wed, 10 Feb 2021 05:00:29 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6e3695b222963de8d9040148f53eb7409d085346f015b1fe7c3cca739063e8`  
		Last Modified: Wed, 10 Feb 2021 05:00:45 GMT  
		Size: 37.2 MB (37174057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ae48dc81d84946129d096d1a8b4b4e312fc6ad790ae2f0199bbcfafa18ea31`  
		Last Modified: Wed, 10 Feb 2021 05:00:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a850fafaaca216abeb02ecb45feca5d924f552090f1dabf4f65f64d2680cb6`  
		Last Modified: Wed, 10 Feb 2021 05:00:40 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:58ee9b103adbec8f98b4b720b6b1768212607e6aea904c0561b5b4f59eaeabe0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104134387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1e639b3cfef67a00f0c58bee42ea84c0bab8cb4cd399937b1e9b43f352448e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 12 Mar 2021 02:05:10 GMT
ADD file:36669d020402a086f914d75419118f4daa1cbeeed645c1a77fe62cac0e804b59 in / 
# Fri, 12 Mar 2021 02:05:15 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 03:39:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 03:40:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 23:58:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 12 Mar 2021 23:58:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 12 Mar 2021 23:59:05 GMT
ENV KAPACITOR_VERSION=1.5.8
# Fri, 12 Mar 2021 23:59:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 12 Mar 2021 23:59:14 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 12 Mar 2021 23:59:15 GMT
EXPOSE 9092
# Fri, 12 Mar 2021 23:59:16 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 12 Mar 2021 23:59:17 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 12 Mar 2021 23:59:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 23:59:19 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:87fcebbbbffa651ca8743935928db6e5acd0bef83a84d1dcc331b6a5dd2dd3a5`  
		Last Modified: Fri, 12 Mar 2021 02:14:09 GMT  
		Size: 42.1 MB (42120188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23db22a6953922b4d37e712f7abfd57e9d0b445d547049f3ae1aff068cd82b05`  
		Last Modified: Fri, 12 Mar 2021 03:50:06 GMT  
		Size: 9.9 MB (9915047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd48c000dbbac1ab4f6cc2b3bbdbd339981893df53383b9f000686f4a1c445b9`  
		Last Modified: Fri, 12 Mar 2021 03:50:04 GMT  
		Size: 3.9 MB (3921108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809ad9aef132fceff7737281929a2db9bd3c196470e9aa36662cace1baa2f9ae`  
		Last Modified: Fri, 12 Mar 2021 23:59:34 GMT  
		Size: 13.4 MB (13436171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c539ca111b42453d64e74d66b56a0ab7482a12a6445afad66021058266e5456d`  
		Last Modified: Fri, 12 Mar 2021 23:59:33 GMT  
		Size: 2.9 KB (2853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7504a92601448fea89e2d4bd9811ff72014c9884b2bdfa175473d9a8d2cdec`  
		Last Modified: Fri, 12 Mar 2021 23:59:57 GMT  
		Size: 34.7 MB (34738565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78b1ed2f5892b2a5664d96e8d10ebbe39b2655841ed81dca70f1293d793cf9a`  
		Last Modified: Fri, 12 Mar 2021 23:59:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0603e92321a7ebcebe69998e50b5038c6400da21834a1d21d640f39b15c942bb`  
		Last Modified: Fri, 12 Mar 2021 23:59:48 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:70a98cc2a5b1383ca4cd272f3a80488ed37d3a6d8b4fd4f532dcf95ced2d8ff7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (104956048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ba9a22131ba6ef611a858b5b84743158c0a2ec51528ceb9469c4e36c13ca67`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 12 Mar 2021 01:56:48 GMT
ADD file:3d59786321ef76584460518105748706e36cd0b833f1d542702f9e238073f63b in / 
# Fri, 12 Mar 2021 01:56:54 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:36:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:36:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 19:49:13 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 12 Mar 2021 19:49:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 12 Mar 2021 19:49:41 GMT
ENV KAPACITOR_VERSION=1.5.8
# Fri, 12 Mar 2021 19:49:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 12 Mar 2021 19:49:52 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 12 Mar 2021 19:49:54 GMT
EXPOSE 9092
# Fri, 12 Mar 2021 19:49:56 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 12 Mar 2021 19:49:58 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 12 Mar 2021 19:50:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 19:50:02 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:690bb835f855da2bebb5afc2671951a9cafcaae8e3751eaa3ef8536058581b9d`  
		Last Modified: Fri, 12 Mar 2021 02:03:51 GMT  
		Size: 43.2 MB (43177463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8900d8bfcdd8c3d3bf8eef705080ae89efe5d9b24294b7d39c1c0d44f93dd47f`  
		Last Modified: Fri, 12 Mar 2021 02:46:19 GMT  
		Size: 10.2 MB (10184079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f83540a087edd442573d6168d03eb7e83cef27a2e34ece682ea441233733ce`  
		Last Modified: Fri, 12 Mar 2021 02:46:17 GMT  
		Size: 4.1 MB (4096643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177964681cdd6d6d609585eddaaa18ef8ca13dc4f54f7a8bce44329b18b0f47c`  
		Last Modified: Fri, 12 Mar 2021 19:50:20 GMT  
		Size: 13.0 MB (12964015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f8e7103b15f435a438c8111f28c1a29871aed06795b952c9ed1f9827cdc822`  
		Last Modified: Fri, 12 Mar 2021 19:50:18 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ca8163a29990c822d8f62cfb3bf6070630b4ada98c6bf9f0ab5d2f4cb7dab3`  
		Last Modified: Fri, 12 Mar 2021 19:50:38 GMT  
		Size: 34.5 MB (34530537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775afa8d832dd476f9725b517911cefee1b3f9daa733bf8e4d55521311c96fc5`  
		Last Modified: Fri, 12 Mar 2021 19:50:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fc817d3fb61dec22dbcfc8067ea0381b89ce5e107f282bb7cc4aff5f800ecb`  
		Last Modified: Fri, 12 Mar 2021 19:50:31 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5-alpine`

```console
$ docker pull kapacitor@sha256:ec69744aaf176179f40e386c4256c616c53caae7179eea5f3c720a081db5a37c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.5-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:e2bff2b50787849bef696d21aaafafd7643c9364acee13b05b055357d93d0c01
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22597944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96dff431b0eb412b1317c4fee522e17ca39252704689e2ff595a680186fe423e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:21:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:59:21 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 24 Feb 2021 23:53:43 GMT
ENV KAPACITOR_VERSION=1.5.8
# Wed, 24 Feb 2021 23:53:47 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 24 Feb 2021 23:53:47 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 24 Feb 2021 23:53:47 GMT
EXPOSE 9092
# Wed, 24 Feb 2021 23:53:47 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 24 Feb 2021 23:53:48 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Wed, 24 Feb 2021 23:53:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 23:53:48 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c3c544bdbd838411be7288d5c8bd23d77b89d00730ce0fa218fd7fd1694b04`  
		Last Modified: Wed, 24 Feb 2021 20:24:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b4c4e91c477308692065de267dedc098ac76d0b4d02f27d7d3ff2d2ff35287`  
		Last Modified: Wed, 24 Feb 2021 21:00:31 GMT  
		Size: 280.9 KB (280902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363a9a912880ddc0373277b2b1a222d65300edfef56be3952190cd96bc5ebb42`  
		Last Modified: Wed, 24 Feb 2021 23:54:19 GMT  
		Size: 19.5 MB (19516942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c373e5fe99142bdfb38b1432a8e783b0fc587be68744930bc9cf687c9b4291`  
		Last Modified: Wed, 24 Feb 2021 23:54:15 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00435d99093fda5448773bae435ccc79c367b3fac6597bfaf9fec7d946f0f50b`  
		Last Modified: Wed, 24 Feb 2021 23:54:15 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5.8`

```console
$ docker pull kapacitor@sha256:41e6b5a493ec6c7e0a7d426bf3f782ff978454308df71584e3baabaeaa44b2c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.5.8` - linux; amd64

```console
$ docker pull kapacitor@sha256:0dd0bdcb6cc90a0fa29af6394171ec4b3f732006dc1360ee919c249a19a2b903
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111410644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95490156d6f247eb05ca7c872ff5c4d8c7f0e1f32417828bf04db462334d10f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:39:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 04:59:47 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 10 Feb 2021 04:59:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 05:00:04 GMT
ENV KAPACITOR_VERSION=1.5.8
# Wed, 10 Feb 2021 05:00:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 10 Feb 2021 05:00:08 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 10 Feb 2021 05:00:09 GMT
EXPOSE 9092
# Wed, 10 Feb 2021 05:00:09 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 10 Feb 2021 05:00:09 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 10 Feb 2021 05:00:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 05:00:09 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0edb687a3dadde6ae013f9b8f08340de1f105266abe3081bba8e8939267978a`  
		Last Modified: Tue, 09 Feb 2021 04:48:28 GMT  
		Size: 11.3 MB (11268653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891892cc2ec4337be73614b6c3eecd8f1a1ac16eae254d1e4b6090358dd6782`  
		Last Modified: Tue, 09 Feb 2021 04:48:27 GMT  
		Size: 4.3 MB (4341906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931c232d0d40a12d9a9dc45b75237e4928a282b52b7cf165e95bde4a88af4066`  
		Last Modified: Wed, 10 Feb 2021 05:00:30 GMT  
		Size: 13.2 MB (13242862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8167b286365fbadf9e276748beeb19bfa326bcc3910c95777e5d951011784bd9`  
		Last Modified: Wed, 10 Feb 2021 05:00:29 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6e3695b222963de8d9040148f53eb7409d085346f015b1fe7c3cca739063e8`  
		Last Modified: Wed, 10 Feb 2021 05:00:45 GMT  
		Size: 37.2 MB (37174057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ae48dc81d84946129d096d1a8b4b4e312fc6ad790ae2f0199bbcfafa18ea31`  
		Last Modified: Wed, 10 Feb 2021 05:00:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a850fafaaca216abeb02ecb45feca5d924f552090f1dabf4f65f64d2680cb6`  
		Last Modified: Wed, 10 Feb 2021 05:00:40 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5.8` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:58ee9b103adbec8f98b4b720b6b1768212607e6aea904c0561b5b4f59eaeabe0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104134387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1e639b3cfef67a00f0c58bee42ea84c0bab8cb4cd399937b1e9b43f352448e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 12 Mar 2021 02:05:10 GMT
ADD file:36669d020402a086f914d75419118f4daa1cbeeed645c1a77fe62cac0e804b59 in / 
# Fri, 12 Mar 2021 02:05:15 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 03:39:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 03:40:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 23:58:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 12 Mar 2021 23:58:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 12 Mar 2021 23:59:05 GMT
ENV KAPACITOR_VERSION=1.5.8
# Fri, 12 Mar 2021 23:59:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 12 Mar 2021 23:59:14 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 12 Mar 2021 23:59:15 GMT
EXPOSE 9092
# Fri, 12 Mar 2021 23:59:16 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 12 Mar 2021 23:59:17 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 12 Mar 2021 23:59:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 23:59:19 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:87fcebbbbffa651ca8743935928db6e5acd0bef83a84d1dcc331b6a5dd2dd3a5`  
		Last Modified: Fri, 12 Mar 2021 02:14:09 GMT  
		Size: 42.1 MB (42120188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23db22a6953922b4d37e712f7abfd57e9d0b445d547049f3ae1aff068cd82b05`  
		Last Modified: Fri, 12 Mar 2021 03:50:06 GMT  
		Size: 9.9 MB (9915047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd48c000dbbac1ab4f6cc2b3bbdbd339981893df53383b9f000686f4a1c445b9`  
		Last Modified: Fri, 12 Mar 2021 03:50:04 GMT  
		Size: 3.9 MB (3921108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809ad9aef132fceff7737281929a2db9bd3c196470e9aa36662cace1baa2f9ae`  
		Last Modified: Fri, 12 Mar 2021 23:59:34 GMT  
		Size: 13.4 MB (13436171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c539ca111b42453d64e74d66b56a0ab7482a12a6445afad66021058266e5456d`  
		Last Modified: Fri, 12 Mar 2021 23:59:33 GMT  
		Size: 2.9 KB (2853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7504a92601448fea89e2d4bd9811ff72014c9884b2bdfa175473d9a8d2cdec`  
		Last Modified: Fri, 12 Mar 2021 23:59:57 GMT  
		Size: 34.7 MB (34738565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78b1ed2f5892b2a5664d96e8d10ebbe39b2655841ed81dca70f1293d793cf9a`  
		Last Modified: Fri, 12 Mar 2021 23:59:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0603e92321a7ebcebe69998e50b5038c6400da21834a1d21d640f39b15c942bb`  
		Last Modified: Fri, 12 Mar 2021 23:59:48 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5.8` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:70a98cc2a5b1383ca4cd272f3a80488ed37d3a6d8b4fd4f532dcf95ced2d8ff7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (104956048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ba9a22131ba6ef611a858b5b84743158c0a2ec51528ceb9469c4e36c13ca67`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 12 Mar 2021 01:56:48 GMT
ADD file:3d59786321ef76584460518105748706e36cd0b833f1d542702f9e238073f63b in / 
# Fri, 12 Mar 2021 01:56:54 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:36:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:36:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 19:49:13 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 12 Mar 2021 19:49:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 12 Mar 2021 19:49:41 GMT
ENV KAPACITOR_VERSION=1.5.8
# Fri, 12 Mar 2021 19:49:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 12 Mar 2021 19:49:52 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 12 Mar 2021 19:49:54 GMT
EXPOSE 9092
# Fri, 12 Mar 2021 19:49:56 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 12 Mar 2021 19:49:58 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 12 Mar 2021 19:50:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 19:50:02 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:690bb835f855da2bebb5afc2671951a9cafcaae8e3751eaa3ef8536058581b9d`  
		Last Modified: Fri, 12 Mar 2021 02:03:51 GMT  
		Size: 43.2 MB (43177463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8900d8bfcdd8c3d3bf8eef705080ae89efe5d9b24294b7d39c1c0d44f93dd47f`  
		Last Modified: Fri, 12 Mar 2021 02:46:19 GMT  
		Size: 10.2 MB (10184079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f83540a087edd442573d6168d03eb7e83cef27a2e34ece682ea441233733ce`  
		Last Modified: Fri, 12 Mar 2021 02:46:17 GMT  
		Size: 4.1 MB (4096643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177964681cdd6d6d609585eddaaa18ef8ca13dc4f54f7a8bce44329b18b0f47c`  
		Last Modified: Fri, 12 Mar 2021 19:50:20 GMT  
		Size: 13.0 MB (12964015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f8e7103b15f435a438c8111f28c1a29871aed06795b952c9ed1f9827cdc822`  
		Last Modified: Fri, 12 Mar 2021 19:50:18 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ca8163a29990c822d8f62cfb3bf6070630b4ada98c6bf9f0ab5d2f4cb7dab3`  
		Last Modified: Fri, 12 Mar 2021 19:50:38 GMT  
		Size: 34.5 MB (34530537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775afa8d832dd476f9725b517911cefee1b3f9daa733bf8e4d55521311c96fc5`  
		Last Modified: Fri, 12 Mar 2021 19:50:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fc817d3fb61dec22dbcfc8067ea0381b89ce5e107f282bb7cc4aff5f800ecb`  
		Last Modified: Fri, 12 Mar 2021 19:50:31 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5.8-alpine`

```console
$ docker pull kapacitor@sha256:ec69744aaf176179f40e386c4256c616c53caae7179eea5f3c720a081db5a37c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:1.5.8-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:e2bff2b50787849bef696d21aaafafd7643c9364acee13b05b055357d93d0c01
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22597944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96dff431b0eb412b1317c4fee522e17ca39252704689e2ff595a680186fe423e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:21:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:59:21 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 24 Feb 2021 23:53:43 GMT
ENV KAPACITOR_VERSION=1.5.8
# Wed, 24 Feb 2021 23:53:47 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 24 Feb 2021 23:53:47 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 24 Feb 2021 23:53:47 GMT
EXPOSE 9092
# Wed, 24 Feb 2021 23:53:47 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 24 Feb 2021 23:53:48 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Wed, 24 Feb 2021 23:53:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 23:53:48 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c3c544bdbd838411be7288d5c8bd23d77b89d00730ce0fa218fd7fd1694b04`  
		Last Modified: Wed, 24 Feb 2021 20:24:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b4c4e91c477308692065de267dedc098ac76d0b4d02f27d7d3ff2d2ff35287`  
		Last Modified: Wed, 24 Feb 2021 21:00:31 GMT  
		Size: 280.9 KB (280902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363a9a912880ddc0373277b2b1a222d65300edfef56be3952190cd96bc5ebb42`  
		Last Modified: Wed, 24 Feb 2021 23:54:19 GMT  
		Size: 19.5 MB (19516942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c373e5fe99142bdfb38b1432a8e783b0fc587be68744930bc9cf687c9b4291`  
		Last Modified: Wed, 24 Feb 2021 23:54:15 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00435d99093fda5448773bae435ccc79c367b3fac6597bfaf9fec7d946f0f50b`  
		Last Modified: Wed, 24 Feb 2021 23:54:15 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:ec69744aaf176179f40e386c4256c616c53caae7179eea5f3c720a081db5a37c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:e2bff2b50787849bef696d21aaafafd7643c9364acee13b05b055357d93d0c01
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22597944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96dff431b0eb412b1317c4fee522e17ca39252704689e2ff595a680186fe423e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:21:14 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:59:21 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 24 Feb 2021 23:53:43 GMT
ENV KAPACITOR_VERSION=1.5.8
# Wed, 24 Feb 2021 23:53:47 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 24 Feb 2021 23:53:47 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 24 Feb 2021 23:53:47 GMT
EXPOSE 9092
# Wed, 24 Feb 2021 23:53:47 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 24 Feb 2021 23:53:48 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Wed, 24 Feb 2021 23:53:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 24 Feb 2021 23:53:48 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c3c544bdbd838411be7288d5c8bd23d77b89d00730ce0fa218fd7fd1694b04`  
		Last Modified: Wed, 24 Feb 2021 20:24:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b4c4e91c477308692065de267dedc098ac76d0b4d02f27d7d3ff2d2ff35287`  
		Last Modified: Wed, 24 Feb 2021 21:00:31 GMT  
		Size: 280.9 KB (280902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363a9a912880ddc0373277b2b1a222d65300edfef56be3952190cd96bc5ebb42`  
		Last Modified: Wed, 24 Feb 2021 23:54:19 GMT  
		Size: 19.5 MB (19516942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c373e5fe99142bdfb38b1432a8e783b0fc587be68744930bc9cf687c9b4291`  
		Last Modified: Wed, 24 Feb 2021 23:54:15 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00435d99093fda5448773bae435ccc79c367b3fac6597bfaf9fec7d946f0f50b`  
		Last Modified: Wed, 24 Feb 2021 23:54:15 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:41e6b5a493ec6c7e0a7d426bf3f782ff978454308df71584e3baabaeaa44b2c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:0dd0bdcb6cc90a0fa29af6394171ec4b3f732006dc1360ee919c249a19a2b903
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111410644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95490156d6f247eb05ca7c872ff5c4d8c7f0e1f32417828bf04db462334d10f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 09 Feb 2021 02:23:13 GMT
ADD file:e1e13145e23f170f2d55444019a2d18a8cecd6209bba9f4295a35632ad53fdde in / 
# Tue, 09 Feb 2021 02:23:14 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 04:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 04:39:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 10 Feb 2021 04:59:47 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 10 Feb 2021 04:59:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 10 Feb 2021 05:00:04 GMT
ENV KAPACITOR_VERSION=1.5.8
# Wed, 10 Feb 2021 05:00:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 10 Feb 2021 05:00:08 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 10 Feb 2021 05:00:09 GMT
EXPOSE 9092
# Wed, 10 Feb 2021 05:00:09 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 10 Feb 2021 05:00:09 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 10 Feb 2021 05:00:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 10 Feb 2021 05:00:09 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:1e987daa2432270bbfaf366f57583c93b48e0ee6c9fe54fe7f4030b84095627f`  
		Last Modified: Tue, 09 Feb 2021 02:29:20 GMT  
		Size: 45.4 MB (45379885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0edb687a3dadde6ae013f9b8f08340de1f105266abe3081bba8e8939267978a`  
		Last Modified: Tue, 09 Feb 2021 04:48:28 GMT  
		Size: 11.3 MB (11268653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891892cc2ec4337be73614b6c3eecd8f1a1ac16eae254d1e4b6090358dd6782`  
		Last Modified: Tue, 09 Feb 2021 04:48:27 GMT  
		Size: 4.3 MB (4341906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931c232d0d40a12d9a9dc45b75237e4928a282b52b7cf165e95bde4a88af4066`  
		Last Modified: Wed, 10 Feb 2021 05:00:30 GMT  
		Size: 13.2 MB (13242862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8167b286365fbadf9e276748beeb19bfa326bcc3910c95777e5d951011784bd9`  
		Last Modified: Wed, 10 Feb 2021 05:00:29 GMT  
		Size: 2.8 KB (2826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6e3695b222963de8d9040148f53eb7409d085346f015b1fe7c3cca739063e8`  
		Last Modified: Wed, 10 Feb 2021 05:00:45 GMT  
		Size: 37.2 MB (37174057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ae48dc81d84946129d096d1a8b4b4e312fc6ad790ae2f0199bbcfafa18ea31`  
		Last Modified: Wed, 10 Feb 2021 05:00:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24a850fafaaca216abeb02ecb45feca5d924f552090f1dabf4f65f64d2680cb6`  
		Last Modified: Wed, 10 Feb 2021 05:00:40 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:58ee9b103adbec8f98b4b720b6b1768212607e6aea904c0561b5b4f59eaeabe0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104134387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1e639b3cfef67a00f0c58bee42ea84c0bab8cb4cd399937b1e9b43f352448e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 12 Mar 2021 02:05:10 GMT
ADD file:36669d020402a086f914d75419118f4daa1cbeeed645c1a77fe62cac0e804b59 in / 
# Fri, 12 Mar 2021 02:05:15 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 03:39:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 03:40:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 23:58:35 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 12 Mar 2021 23:58:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 12 Mar 2021 23:59:05 GMT
ENV KAPACITOR_VERSION=1.5.8
# Fri, 12 Mar 2021 23:59:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 12 Mar 2021 23:59:14 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 12 Mar 2021 23:59:15 GMT
EXPOSE 9092
# Fri, 12 Mar 2021 23:59:16 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 12 Mar 2021 23:59:17 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 12 Mar 2021 23:59:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 23:59:19 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:87fcebbbbffa651ca8743935928db6e5acd0bef83a84d1dcc331b6a5dd2dd3a5`  
		Last Modified: Fri, 12 Mar 2021 02:14:09 GMT  
		Size: 42.1 MB (42120188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23db22a6953922b4d37e712f7abfd57e9d0b445d547049f3ae1aff068cd82b05`  
		Last Modified: Fri, 12 Mar 2021 03:50:06 GMT  
		Size: 9.9 MB (9915047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd48c000dbbac1ab4f6cc2b3bbdbd339981893df53383b9f000686f4a1c445b9`  
		Last Modified: Fri, 12 Mar 2021 03:50:04 GMT  
		Size: 3.9 MB (3921108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:809ad9aef132fceff7737281929a2db9bd3c196470e9aa36662cace1baa2f9ae`  
		Last Modified: Fri, 12 Mar 2021 23:59:34 GMT  
		Size: 13.4 MB (13436171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c539ca111b42453d64e74d66b56a0ab7482a12a6445afad66021058266e5456d`  
		Last Modified: Fri, 12 Mar 2021 23:59:33 GMT  
		Size: 2.9 KB (2853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7504a92601448fea89e2d4bd9811ff72014c9884b2bdfa175473d9a8d2cdec`  
		Last Modified: Fri, 12 Mar 2021 23:59:57 GMT  
		Size: 34.7 MB (34738565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78b1ed2f5892b2a5664d96e8d10ebbe39b2655841ed81dca70f1293d793cf9a`  
		Last Modified: Fri, 12 Mar 2021 23:59:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0603e92321a7ebcebe69998e50b5038c6400da21834a1d21d640f39b15c942bb`  
		Last Modified: Fri, 12 Mar 2021 23:59:48 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:70a98cc2a5b1383ca4cd272f3a80488ed37d3a6d8b4fd4f532dcf95ced2d8ff7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (104956048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ba9a22131ba6ef611a858b5b84743158c0a2ec51528ceb9469c4e36c13ca67`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 12 Mar 2021 01:56:48 GMT
ADD file:3d59786321ef76584460518105748706e36cd0b833f1d542702f9e238073f63b in / 
# Fri, 12 Mar 2021 01:56:54 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:36:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:36:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 12 Mar 2021 19:49:13 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 12 Mar 2021 19:49:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Fri, 12 Mar 2021 19:49:41 GMT
ENV KAPACITOR_VERSION=1.5.8
# Fri, 12 Mar 2021 19:49:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 12 Mar 2021 19:49:52 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 12 Mar 2021 19:49:54 GMT
EXPOSE 9092
# Fri, 12 Mar 2021 19:49:56 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 12 Mar 2021 19:49:58 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 12 Mar 2021 19:50:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Mar 2021 19:50:02 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:690bb835f855da2bebb5afc2671951a9cafcaae8e3751eaa3ef8536058581b9d`  
		Last Modified: Fri, 12 Mar 2021 02:03:51 GMT  
		Size: 43.2 MB (43177463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8900d8bfcdd8c3d3bf8eef705080ae89efe5d9b24294b7d39c1c0d44f93dd47f`  
		Last Modified: Fri, 12 Mar 2021 02:46:19 GMT  
		Size: 10.2 MB (10184079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f83540a087edd442573d6168d03eb7e83cef27a2e34ece682ea441233733ce`  
		Last Modified: Fri, 12 Mar 2021 02:46:17 GMT  
		Size: 4.1 MB (4096643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177964681cdd6d6d609585eddaaa18ef8ca13dc4f54f7a8bce44329b18b0f47c`  
		Last Modified: Fri, 12 Mar 2021 19:50:20 GMT  
		Size: 13.0 MB (12964015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f8e7103b15f435a438c8111f28c1a29871aed06795b952c9ed1f9827cdc822`  
		Last Modified: Fri, 12 Mar 2021 19:50:18 GMT  
		Size: 2.9 KB (2856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ca8163a29990c822d8f62cfb3bf6070630b4ada98c6bf9f0ab5d2f4cb7dab3`  
		Last Modified: Fri, 12 Mar 2021 19:50:38 GMT  
		Size: 34.5 MB (34530537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775afa8d832dd476f9725b517911cefee1b3f9daa733bf8e4d55521311c96fc5`  
		Last Modified: Fri, 12 Mar 2021 19:50:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8fc817d3fb61dec22dbcfc8067ea0381b89ce5e107f282bb7cc4aff5f800ecb`  
		Last Modified: Fri, 12 Mar 2021 19:50:31 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
