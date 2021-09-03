<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.5`](#kapacitor15)
-	[`kapacitor:1.5-alpine`](#kapacitor15-alpine)
-	[`kapacitor:1.5.9`](#kapacitor159)
-	[`kapacitor:1.5.9-alpine`](#kapacitor159-alpine)
-	[`kapacitor:1.6`](#kapacitor16)
-	[`kapacitor:1.6-alpine`](#kapacitor16-alpine)
-	[`kapacitor:1.6.1`](#kapacitor161)
-	[`kapacitor:1.6.1-alpine`](#kapacitor161-alpine)
-	[`kapacitor:alpine`](#kapacitoralpine)
-	[`kapacitor:latest`](#kapacitorlatest)

## `kapacitor:1.5`

```console
$ docker pull kapacitor@sha256:a0b975b0cb738d3b2680eb3c47a786e74b26b95dbdf34ad7f85468848ee1c1dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.5` - linux; amd64

```console
$ docker pull kapacitor@sha256:bb089931dbaad2ef28526cd2c40a839e8c5995cd8265be3fb7e306e205191ef2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111563379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9184cdbff2473fc42ca22d4759d13be78d12c72a5f5f69d5a52dba423840cf4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 17 Aug 2021 01:25:56 GMT
ADD file:0d0aa1ebd07b0f301aaf1077d1e9f2e9be1859510dd8535e143571b347a2a379 in / 
# Tue, 17 Aug 2021 01:25:56 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:24:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:24:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 07:01:25 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 18 Aug 2021 07:01:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 07:01:29 GMT
ENV KAPACITOR_VERSION=1.5.9
# Wed, 18 Aug 2021 07:01:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 18 Aug 2021 07:01:33 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 18 Aug 2021 07:01:34 GMT
EXPOSE 9092
# Wed, 18 Aug 2021 07:01:34 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 18 Aug 2021 07:01:34 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 18 Aug 2021 07:01:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Aug 2021 07:01:34 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:eb18d230e067c240479c6a3f842e7f9d4ff1088e3072d0a3245829c4e356623f`  
		Last Modified: Tue, 17 Aug 2021 01:33:03 GMT  
		Size: 45.4 MB (45379966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83600c1b4583abb5830c6d4a039cbab9a102ac1a7b3b779854638a371bb7128f`  
		Last Modified: Tue, 17 Aug 2021 09:33:12 GMT  
		Size: 11.3 MB (11295906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae15c65bfa0fdc9053dcb734e6c034f5394ea0481dee3277f6e3e9fa07702d0`  
		Last Modified: Tue, 17 Aug 2021 09:33:11 GMT  
		Size: 4.3 MB (4342387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df9a81a6e6330b08dc4ea9322d4dbc9131ceb336f4f48222299992bee24d20c`  
		Last Modified: Wed, 18 Aug 2021 07:02:07 GMT  
		Size: 13.3 MB (13322522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ac9e7ace861b8fefc86ece32a745d3860247036ec12dca6a51e6436f64cfe6`  
		Last Modified: Wed, 18 Aug 2021 07:02:05 GMT  
		Size: 2.9 KB (2853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab51074876d326021dd844c3542120b88fe5845cec7e06e7631eda29afa627d7`  
		Last Modified: Wed, 18 Aug 2021 07:02:10 GMT  
		Size: 37.2 MB (37219290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74fd780d2c50b816d5db46a42f0c3070bcc223cb2aefb6fda90f693beed3a258`  
		Last Modified: Wed, 18 Aug 2021 07:02:05 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba2e7f59ac966696e08fada5b63ed25da9d0d601dc818ce4c230146eef21ac4`  
		Last Modified: Wed, 18 Aug 2021 07:02:05 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:ab6bbc7d7030a12cc1de1253a7c2a42e2cf2bc998774f959ed3303a41af521b6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104285309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46b57dd609214fefb28989704b619b335631d6e9d77611f11433dd507253d0a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 17 Aug 2021 02:19:00 GMT
ADD file:5e5e5a4e13ae8e36740009c29111838a32d9901b28809b485c841d25d550698b in / 
# Tue, 17 Aug 2021 02:19:01 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 15:28:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 15:28:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 22:45:26 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 18 Aug 2021 22:45:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 22:45:31 GMT
ENV KAPACITOR_VERSION=1.5.9
# Wed, 18 Aug 2021 22:45:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 18 Aug 2021 22:45:41 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 18 Aug 2021 22:45:41 GMT
EXPOSE 9092
# Wed, 18 Aug 2021 22:45:42 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 18 Aug 2021 22:45:42 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 18 Aug 2021 22:45:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Aug 2021 22:45:43 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:30d3c67f4f95a7d99559389477234b45c05024484d59cec2d66264610a623fe9`  
		Last Modified: Tue, 17 Aug 2021 02:36:17 GMT  
		Size: 42.1 MB (42119745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e002433047948d255f28ba7ee556c302875d03d4d84f4b30b34ed9aeb481ef27`  
		Last Modified: Tue, 17 Aug 2021 15:46:54 GMT  
		Size: 10.0 MB (9951645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9a501430415711f6cdd553e589abddd926f28b6f57669a8fafbbc06811a06d`  
		Last Modified: Tue, 17 Aug 2021 15:46:51 GMT  
		Size: 3.9 MB (3921237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd054fb54a132cb9e7f19bc9764a9434703dc3a2ee15a1d2f7ea39650eb3a411`  
		Last Modified: Wed, 18 Aug 2021 22:46:13 GMT  
		Size: 13.5 MB (13502661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d67efd24b51630c96bff1df01a207a55064c1eb3b987e15f1e7b8d6d080885`  
		Last Modified: Wed, 18 Aug 2021 22:46:08 GMT  
		Size: 2.9 KB (2857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b52f7d82af8ae34d00fe2994cfc18a978adf02d2547e2bd399cd386e77dbea`  
		Last Modified: Wed, 18 Aug 2021 22:46:25 GMT  
		Size: 34.8 MB (34786705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf01a5a9514a4bb4487c25036d80c6c3a2777407caec70697b1b2d7f296a0ed`  
		Last Modified: Wed, 18 Aug 2021 22:46:08 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf907a72c945feb1985ba745dc00c3d2bbc091b0cc0041bee18cfd3ac193787`  
		Last Modified: Wed, 18 Aug 2021 22:46:08 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:f8b39c756c34ad0f8d93ba52bf5063a8d6b38f6896951d3616167c8ecfaaaf8c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105082057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bdced8726fb032602398f24aff3461910ee613b713e9560d32e057b7a55d587`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 03 Sep 2021 00:42:34 GMT
ADD file:3a77488ae0a72e8fd504cb1354bd111f38a4fc9f3e541ee7ebce3ebc4eb9dc49 in / 
# Fri, 03 Sep 2021 00:42:34 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 04:36:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 04:36:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Sep 2021 21:07:59 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 03 Sep 2021 21:08:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 21:08:07 GMT
ENV KAPACITOR_VERSION=1.5.9
# Fri, 03 Sep 2021 21:08:11 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 03 Sep 2021 21:08:12 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 03 Sep 2021 21:08:12 GMT
EXPOSE 9092
# Fri, 03 Sep 2021 21:08:12 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 03 Sep 2021 21:08:12 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 03 Sep 2021 21:08:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 21:08:13 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:e98a9e31e599c3e38ecd12cf6b8493f4268c371026bae6d2280da418009b5bff`  
		Last Modified: Fri, 03 Sep 2021 00:52:57 GMT  
		Size: 43.2 MB (43177996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f698e334a0e8a436e04b2ef344b0ada5761244cf05829ece406e740b750b1bfa`  
		Last Modified: Fri, 03 Sep 2021 04:44:45 GMT  
		Size: 10.2 MB (10215862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62eef9137c22a6fa0d9b497479b8c3ba0d211b5f01fafd237e4dc3419146e22a`  
		Last Modified: Fri, 03 Sep 2021 04:44:44 GMT  
		Size: 4.1 MB (4096542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d524ec54ce2cc3514ffe7ba394bc8e3c9e9ba04493c6ba234d8be1645f4d4123`  
		Last Modified: Fri, 03 Sep 2021 21:08:49 GMT  
		Size: 13.0 MB (13027371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e6cba0468ee4e125ab0563615edf0f8999ef3a0275f4b80211c9cb7f22a5f0`  
		Last Modified: Fri, 03 Sep 2021 21:08:47 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0890c17de292f29100dd90ea1c389cc2c575ba8f4c14f1c8c177e3c7c418e91e`  
		Last Modified: Fri, 03 Sep 2021 21:08:52 GMT  
		Size: 34.6 MB (34560978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e34b568149ac1237fad5b220c1344b2ef7d9d5fdac1e40cbc7d96c301f3ac6`  
		Last Modified: Fri, 03 Sep 2021 21:08:47 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4492d6eb77bea77ec865f66ab33939ef68dd0af51650ff8f68cd1696ea6e90a2`  
		Last Modified: Fri, 03 Sep 2021 21:08:48 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5-alpine`

```console
$ docker pull kapacitor@sha256:2cdcab2a7797521e528a0a87065180d4f73c7822018996006320ef2b3e08b071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.5-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:aec3c23ef7bc93b5791141f8fe2793404aad85a1a11f6b8d7ee2fdc62d40b781
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22625231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c8f5a6c0287e53b4889d011df8971ef0630dce5ec50329c524d70043cf339cd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:23:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:23:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 01 Sep 2021 03:04:15 GMT
ENV KAPACITOR_VERSION=1.5.9
# Wed, 01 Sep 2021 03:04:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 01 Sep 2021 03:04:20 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 01 Sep 2021 03:04:20 GMT
EXPOSE 9092
# Wed, 01 Sep 2021 03:04:21 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 01 Sep 2021 03:04:21 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Wed, 01 Sep 2021 03:04:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 03:04:21 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69cd3502d3b453e253ea48e4ff56f5af4e25895a1bfa5e84cda59eaefce23be`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7087df4b29e442773e368f72aa50cd7765fd6e6b43879c83880b0038e62b9077`  
		Last Modified: Wed, 01 Sep 2021 00:25:29 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c781830543db249e742723c9ae5bdc70eb4c663278c7c28add837b5b20bc61e`  
		Last Modified: Wed, 01 Sep 2021 03:05:06 GMT  
		Size: 19.5 MB (19542013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ec0599af5a04b1b7dad3ff6168e9fdb159c02e3149f99abafd7819204a5fca`  
		Last Modified: Wed, 01 Sep 2021 03:05:02 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f39527004d52de4b800959b812c0cbc9c2167b67ac327f7416d90afbf6d1b7d`  
		Last Modified: Wed, 01 Sep 2021 03:05:02 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5.9`

```console
$ docker pull kapacitor@sha256:a0b975b0cb738d3b2680eb3c47a786e74b26b95dbdf34ad7f85468848ee1c1dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.5.9` - linux; amd64

```console
$ docker pull kapacitor@sha256:bb089931dbaad2ef28526cd2c40a839e8c5995cd8265be3fb7e306e205191ef2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111563379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9184cdbff2473fc42ca22d4759d13be78d12c72a5f5f69d5a52dba423840cf4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 17 Aug 2021 01:25:56 GMT
ADD file:0d0aa1ebd07b0f301aaf1077d1e9f2e9be1859510dd8535e143571b347a2a379 in / 
# Tue, 17 Aug 2021 01:25:56 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:24:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:24:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 07:01:25 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 18 Aug 2021 07:01:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 07:01:29 GMT
ENV KAPACITOR_VERSION=1.5.9
# Wed, 18 Aug 2021 07:01:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 18 Aug 2021 07:01:33 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 18 Aug 2021 07:01:34 GMT
EXPOSE 9092
# Wed, 18 Aug 2021 07:01:34 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 18 Aug 2021 07:01:34 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 18 Aug 2021 07:01:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Aug 2021 07:01:34 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:eb18d230e067c240479c6a3f842e7f9d4ff1088e3072d0a3245829c4e356623f`  
		Last Modified: Tue, 17 Aug 2021 01:33:03 GMT  
		Size: 45.4 MB (45379966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83600c1b4583abb5830c6d4a039cbab9a102ac1a7b3b779854638a371bb7128f`  
		Last Modified: Tue, 17 Aug 2021 09:33:12 GMT  
		Size: 11.3 MB (11295906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae15c65bfa0fdc9053dcb734e6c034f5394ea0481dee3277f6e3e9fa07702d0`  
		Last Modified: Tue, 17 Aug 2021 09:33:11 GMT  
		Size: 4.3 MB (4342387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df9a81a6e6330b08dc4ea9322d4dbc9131ceb336f4f48222299992bee24d20c`  
		Last Modified: Wed, 18 Aug 2021 07:02:07 GMT  
		Size: 13.3 MB (13322522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ac9e7ace861b8fefc86ece32a745d3860247036ec12dca6a51e6436f64cfe6`  
		Last Modified: Wed, 18 Aug 2021 07:02:05 GMT  
		Size: 2.9 KB (2853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab51074876d326021dd844c3542120b88fe5845cec7e06e7631eda29afa627d7`  
		Last Modified: Wed, 18 Aug 2021 07:02:10 GMT  
		Size: 37.2 MB (37219290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74fd780d2c50b816d5db46a42f0c3070bcc223cb2aefb6fda90f693beed3a258`  
		Last Modified: Wed, 18 Aug 2021 07:02:05 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba2e7f59ac966696e08fada5b63ed25da9d0d601dc818ce4c230146eef21ac4`  
		Last Modified: Wed, 18 Aug 2021 07:02:05 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5.9` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:ab6bbc7d7030a12cc1de1253a7c2a42e2cf2bc998774f959ed3303a41af521b6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104285309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46b57dd609214fefb28989704b619b335631d6e9d77611f11433dd507253d0a1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 17 Aug 2021 02:19:00 GMT
ADD file:5e5e5a4e13ae8e36740009c29111838a32d9901b28809b485c841d25d550698b in / 
# Tue, 17 Aug 2021 02:19:01 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 15:28:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 15:28:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 22:45:26 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 18 Aug 2021 22:45:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 22:45:31 GMT
ENV KAPACITOR_VERSION=1.5.9
# Wed, 18 Aug 2021 22:45:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 18 Aug 2021 22:45:41 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 18 Aug 2021 22:45:41 GMT
EXPOSE 9092
# Wed, 18 Aug 2021 22:45:42 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 18 Aug 2021 22:45:42 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 18 Aug 2021 22:45:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Aug 2021 22:45:43 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:30d3c67f4f95a7d99559389477234b45c05024484d59cec2d66264610a623fe9`  
		Last Modified: Tue, 17 Aug 2021 02:36:17 GMT  
		Size: 42.1 MB (42119745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e002433047948d255f28ba7ee556c302875d03d4d84f4b30b34ed9aeb481ef27`  
		Last Modified: Tue, 17 Aug 2021 15:46:54 GMT  
		Size: 10.0 MB (9951645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9a501430415711f6cdd553e589abddd926f28b6f57669a8fafbbc06811a06d`  
		Last Modified: Tue, 17 Aug 2021 15:46:51 GMT  
		Size: 3.9 MB (3921237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd054fb54a132cb9e7f19bc9764a9434703dc3a2ee15a1d2f7ea39650eb3a411`  
		Last Modified: Wed, 18 Aug 2021 22:46:13 GMT  
		Size: 13.5 MB (13502661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d67efd24b51630c96bff1df01a207a55064c1eb3b987e15f1e7b8d6d080885`  
		Last Modified: Wed, 18 Aug 2021 22:46:08 GMT  
		Size: 2.9 KB (2857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b52f7d82af8ae34d00fe2994cfc18a978adf02d2547e2bd399cd386e77dbea`  
		Last Modified: Wed, 18 Aug 2021 22:46:25 GMT  
		Size: 34.8 MB (34786705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf01a5a9514a4bb4487c25036d80c6c3a2777407caec70697b1b2d7f296a0ed`  
		Last Modified: Wed, 18 Aug 2021 22:46:08 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf907a72c945feb1985ba745dc00c3d2bbc091b0cc0041bee18cfd3ac193787`  
		Last Modified: Wed, 18 Aug 2021 22:46:08 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5.9` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:f8b39c756c34ad0f8d93ba52bf5063a8d6b38f6896951d3616167c8ecfaaaf8c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105082057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bdced8726fb032602398f24aff3461910ee613b713e9560d32e057b7a55d587`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 03 Sep 2021 00:42:34 GMT
ADD file:3a77488ae0a72e8fd504cb1354bd111f38a4fc9f3e541ee7ebce3ebc4eb9dc49 in / 
# Fri, 03 Sep 2021 00:42:34 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 04:36:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 04:36:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Sep 2021 21:07:59 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 03 Sep 2021 21:08:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 21:08:07 GMT
ENV KAPACITOR_VERSION=1.5.9
# Fri, 03 Sep 2021 21:08:11 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 03 Sep 2021 21:08:12 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 03 Sep 2021 21:08:12 GMT
EXPOSE 9092
# Fri, 03 Sep 2021 21:08:12 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 03 Sep 2021 21:08:12 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 03 Sep 2021 21:08:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 21:08:13 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:e98a9e31e599c3e38ecd12cf6b8493f4268c371026bae6d2280da418009b5bff`  
		Last Modified: Fri, 03 Sep 2021 00:52:57 GMT  
		Size: 43.2 MB (43177996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f698e334a0e8a436e04b2ef344b0ada5761244cf05829ece406e740b750b1bfa`  
		Last Modified: Fri, 03 Sep 2021 04:44:45 GMT  
		Size: 10.2 MB (10215862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62eef9137c22a6fa0d9b497479b8c3ba0d211b5f01fafd237e4dc3419146e22a`  
		Last Modified: Fri, 03 Sep 2021 04:44:44 GMT  
		Size: 4.1 MB (4096542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d524ec54ce2cc3514ffe7ba394bc8e3c9e9ba04493c6ba234d8be1645f4d4123`  
		Last Modified: Fri, 03 Sep 2021 21:08:49 GMT  
		Size: 13.0 MB (13027371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e6cba0468ee4e125ab0563615edf0f8999ef3a0275f4b80211c9cb7f22a5f0`  
		Last Modified: Fri, 03 Sep 2021 21:08:47 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0890c17de292f29100dd90ea1c389cc2c575ba8f4c14f1c8c177e3c7c418e91e`  
		Last Modified: Fri, 03 Sep 2021 21:08:52 GMT  
		Size: 34.6 MB (34560978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e34b568149ac1237fad5b220c1344b2ef7d9d5fdac1e40cbc7d96c301f3ac6`  
		Last Modified: Fri, 03 Sep 2021 21:08:47 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4492d6eb77bea77ec865f66ab33939ef68dd0af51650ff8f68cd1696ea6e90a2`  
		Last Modified: Fri, 03 Sep 2021 21:08:48 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.5.9-alpine`

```console
$ docker pull kapacitor@sha256:2cdcab2a7797521e528a0a87065180d4f73c7822018996006320ef2b3e08b071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.5.9-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:aec3c23ef7bc93b5791141f8fe2793404aad85a1a11f6b8d7ee2fdc62d40b781
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22625231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c8f5a6c0287e53b4889d011df8971ef0630dce5ec50329c524d70043cf339cd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:23:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:23:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 01 Sep 2021 03:04:15 GMT
ENV KAPACITOR_VERSION=1.5.9
# Wed, 01 Sep 2021 03:04:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 01 Sep 2021 03:04:20 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 01 Sep 2021 03:04:20 GMT
EXPOSE 9092
# Wed, 01 Sep 2021 03:04:21 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 01 Sep 2021 03:04:21 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Wed, 01 Sep 2021 03:04:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 03:04:21 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69cd3502d3b453e253ea48e4ff56f5af4e25895a1bfa5e84cda59eaefce23be`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7087df4b29e442773e368f72aa50cd7765fd6e6b43879c83880b0038e62b9077`  
		Last Modified: Wed, 01 Sep 2021 00:25:29 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c781830543db249e742723c9ae5bdc70eb4c663278c7c28add837b5b20bc61e`  
		Last Modified: Wed, 01 Sep 2021 03:05:06 GMT  
		Size: 19.5 MB (19542013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ec0599af5a04b1b7dad3ff6168e9fdb159c02e3149f99abafd7819204a5fca`  
		Last Modified: Wed, 01 Sep 2021 03:05:02 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f39527004d52de4b800959b812c0cbc9c2167b67ac327f7416d90afbf6d1b7d`  
		Last Modified: Wed, 01 Sep 2021 03:05:02 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.6`

```console
$ docker pull kapacitor@sha256:faed699d0a1a0d29e3b996b73375efaa229d133d4373f45d5ceef14e0e5ba5d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:1.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:7153c14ce9004d4389fc69f407311389e848df2e044c7c699b25ff1e9fa0b4fd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133606214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc13f62beab87315296150a800a4e1ba8dfc6bc1bf53ad6e6774cf958a1401a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 17 Aug 2021 01:25:56 GMT
ADD file:0d0aa1ebd07b0f301aaf1077d1e9f2e9be1859510dd8535e143571b347a2a379 in / 
# Tue, 17 Aug 2021 01:25:56 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:24:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:24:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 07:01:25 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 18 Aug 2021 07:01:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 07:01:40 GMT
ENV KAPACITOR_VERSION=1.6.1
# Wed, 18 Aug 2021 07:01:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 18 Aug 2021 07:01:45 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 18 Aug 2021 07:01:45 GMT
EXPOSE 9092
# Wed, 18 Aug 2021 07:01:45 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 18 Aug 2021 07:01:45 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 18 Aug 2021 07:01:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Aug 2021 07:01:46 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:eb18d230e067c240479c6a3f842e7f9d4ff1088e3072d0a3245829c4e356623f`  
		Last Modified: Tue, 17 Aug 2021 01:33:03 GMT  
		Size: 45.4 MB (45379966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83600c1b4583abb5830c6d4a039cbab9a102ac1a7b3b779854638a371bb7128f`  
		Last Modified: Tue, 17 Aug 2021 09:33:12 GMT  
		Size: 11.3 MB (11295906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae15c65bfa0fdc9053dcb734e6c034f5394ea0481dee3277f6e3e9fa07702d0`  
		Last Modified: Tue, 17 Aug 2021 09:33:11 GMT  
		Size: 4.3 MB (4342387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df9a81a6e6330b08dc4ea9322d4dbc9131ceb336f4f48222299992bee24d20c`  
		Last Modified: Wed, 18 Aug 2021 07:02:07 GMT  
		Size: 13.3 MB (13322522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ac9e7ace861b8fefc86ece32a745d3860247036ec12dca6a51e6436f64cfe6`  
		Last Modified: Wed, 18 Aug 2021 07:02:05 GMT  
		Size: 2.9 KB (2853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1cc761767c20764cf1890fd66d9fe9b0c73793ffd089bb7010d856e3379946`  
		Last Modified: Wed, 18 Aug 2021 07:02:29 GMT  
		Size: 59.3 MB (59262125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c31ea119f5e5d39540a41d2bd75569c0967d85b58e6af5592701e382cf3603`  
		Last Modified: Wed, 18 Aug 2021 07:02:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fb14f03d554baca4f313ccbaddb34e22c9da8d46e6a3aa2ff345503b0d9d06`  
		Last Modified: Wed, 18 Aug 2021 07:02:21 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:9c52d55020a0c2fa3865cb9dad8aa1ba1902489d2f9c80827fabbc6da7c847a4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 MB (126415227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e10e46e4144963c60e7c7c17197934352599c247f881567f6d5b5c738ff3f4a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 03 Sep 2021 00:42:34 GMT
ADD file:3a77488ae0a72e8fd504cb1354bd111f38a4fc9f3e541ee7ebce3ebc4eb9dc49 in / 
# Fri, 03 Sep 2021 00:42:34 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 04:36:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 04:36:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Sep 2021 21:07:59 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 03 Sep 2021 21:08:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 21:08:20 GMT
ENV KAPACITOR_VERSION=1.6.1
# Fri, 03 Sep 2021 21:08:26 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 03 Sep 2021 21:08:26 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 03 Sep 2021 21:08:26 GMT
EXPOSE 9092
# Fri, 03 Sep 2021 21:08:26 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 03 Sep 2021 21:08:27 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 03 Sep 2021 21:08:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 21:08:27 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:e98a9e31e599c3e38ecd12cf6b8493f4268c371026bae6d2280da418009b5bff`  
		Last Modified: Fri, 03 Sep 2021 00:52:57 GMT  
		Size: 43.2 MB (43177996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f698e334a0e8a436e04b2ef344b0ada5761244cf05829ece406e740b750b1bfa`  
		Last Modified: Fri, 03 Sep 2021 04:44:45 GMT  
		Size: 10.2 MB (10215862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62eef9137c22a6fa0d9b497479b8c3ba0d211b5f01fafd237e4dc3419146e22a`  
		Last Modified: Fri, 03 Sep 2021 04:44:44 GMT  
		Size: 4.1 MB (4096542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d524ec54ce2cc3514ffe7ba394bc8e3c9e9ba04493c6ba234d8be1645f4d4123`  
		Last Modified: Fri, 03 Sep 2021 21:08:49 GMT  
		Size: 13.0 MB (13027371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e6cba0468ee4e125ab0563615edf0f8999ef3a0275f4b80211c9cb7f22a5f0`  
		Last Modified: Fri, 03 Sep 2021 21:08:47 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f4dc5d2890c4f7d452390bfbcaf4a6c6c01fc1870bff8a9678760d952ecc49`  
		Last Modified: Fri, 03 Sep 2021 21:09:13 GMT  
		Size: 55.9 MB (55894146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4acf031730b9c6909438592b19bd91c23eca189ea86a1e3aabc0f5434ca0e2`  
		Last Modified: Fri, 03 Sep 2021 21:09:04 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:644a9eee361d6a8dd6c4324eaf8711e568e3f33c386174866840c15bbfcc1863`  
		Last Modified: Fri, 03 Sep 2021 21:09:04 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.6-alpine`

```console
$ docker pull kapacitor@sha256:7896801d6eeb35bbcbed36310760a3b1ff3120d16b23aaf20267a3e927b8936d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:b3c9c70bdad340a180f54ab64c17a420e8ea6544513bb86d1d5ee61c980c1f16
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62282802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c171de764c09f16e4ce559429bf58d7f552765083dabe7eeaff600d961ba3b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:23:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:23:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 01 Sep 2021 03:04:27 GMT
ENV KAPACITOR_VERSION=1.6.1
# Wed, 01 Sep 2021 03:04:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 01 Sep 2021 03:04:41 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 01 Sep 2021 03:04:41 GMT
EXPOSE 9092
# Wed, 01 Sep 2021 03:04:41 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 01 Sep 2021 03:04:42 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Wed, 01 Sep 2021 03:04:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 03:04:42 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69cd3502d3b453e253ea48e4ff56f5af4e25895a1bfa5e84cda59eaefce23be`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7087df4b29e442773e368f72aa50cd7765fd6e6b43879c83880b0038e62b9077`  
		Last Modified: Wed, 01 Sep 2021 00:25:29 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7cb5b6248de8e40cb59c8a172882bcf139b97f02ea65ba88919ed2aadef1e9`  
		Last Modified: Wed, 01 Sep 2021 03:05:26 GMT  
		Size: 59.2 MB (59199583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e72ce875cf5d94b0730927e9e97d3df95bdfb5651c544f52ac5c124f2f43e5`  
		Last Modified: Wed, 01 Sep 2021 03:05:17 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0b546e47c7e79bda5d79a7be609e9c46eedd0801b11be06c36d4c4bfde1b39`  
		Last Modified: Wed, 01 Sep 2021 03:05:17 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.6.1`

```console
$ docker pull kapacitor@sha256:faed699d0a1a0d29e3b996b73375efaa229d133d4373f45d5ceef14e0e5ba5d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:1.6.1` - linux; amd64

```console
$ docker pull kapacitor@sha256:7153c14ce9004d4389fc69f407311389e848df2e044c7c699b25ff1e9fa0b4fd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133606214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc13f62beab87315296150a800a4e1ba8dfc6bc1bf53ad6e6774cf958a1401a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 17 Aug 2021 01:25:56 GMT
ADD file:0d0aa1ebd07b0f301aaf1077d1e9f2e9be1859510dd8535e143571b347a2a379 in / 
# Tue, 17 Aug 2021 01:25:56 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:24:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:24:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 07:01:25 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 18 Aug 2021 07:01:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 07:01:40 GMT
ENV KAPACITOR_VERSION=1.6.1
# Wed, 18 Aug 2021 07:01:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 18 Aug 2021 07:01:45 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 18 Aug 2021 07:01:45 GMT
EXPOSE 9092
# Wed, 18 Aug 2021 07:01:45 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 18 Aug 2021 07:01:45 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 18 Aug 2021 07:01:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Aug 2021 07:01:46 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:eb18d230e067c240479c6a3f842e7f9d4ff1088e3072d0a3245829c4e356623f`  
		Last Modified: Tue, 17 Aug 2021 01:33:03 GMT  
		Size: 45.4 MB (45379966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83600c1b4583abb5830c6d4a039cbab9a102ac1a7b3b779854638a371bb7128f`  
		Last Modified: Tue, 17 Aug 2021 09:33:12 GMT  
		Size: 11.3 MB (11295906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae15c65bfa0fdc9053dcb734e6c034f5394ea0481dee3277f6e3e9fa07702d0`  
		Last Modified: Tue, 17 Aug 2021 09:33:11 GMT  
		Size: 4.3 MB (4342387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df9a81a6e6330b08dc4ea9322d4dbc9131ceb336f4f48222299992bee24d20c`  
		Last Modified: Wed, 18 Aug 2021 07:02:07 GMT  
		Size: 13.3 MB (13322522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ac9e7ace861b8fefc86ece32a745d3860247036ec12dca6a51e6436f64cfe6`  
		Last Modified: Wed, 18 Aug 2021 07:02:05 GMT  
		Size: 2.9 KB (2853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1cc761767c20764cf1890fd66d9fe9b0c73793ffd089bb7010d856e3379946`  
		Last Modified: Wed, 18 Aug 2021 07:02:29 GMT  
		Size: 59.3 MB (59262125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c31ea119f5e5d39540a41d2bd75569c0967d85b58e6af5592701e382cf3603`  
		Last Modified: Wed, 18 Aug 2021 07:02:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fb14f03d554baca4f313ccbaddb34e22c9da8d46e6a3aa2ff345503b0d9d06`  
		Last Modified: Wed, 18 Aug 2021 07:02:21 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.6.1` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:9c52d55020a0c2fa3865cb9dad8aa1ba1902489d2f9c80827fabbc6da7c847a4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 MB (126415227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e10e46e4144963c60e7c7c17197934352599c247f881567f6d5b5c738ff3f4a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 03 Sep 2021 00:42:34 GMT
ADD file:3a77488ae0a72e8fd504cb1354bd111f38a4fc9f3e541ee7ebce3ebc4eb9dc49 in / 
# Fri, 03 Sep 2021 00:42:34 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 04:36:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 04:36:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Sep 2021 21:07:59 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 03 Sep 2021 21:08:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 21:08:20 GMT
ENV KAPACITOR_VERSION=1.6.1
# Fri, 03 Sep 2021 21:08:26 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 03 Sep 2021 21:08:26 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 03 Sep 2021 21:08:26 GMT
EXPOSE 9092
# Fri, 03 Sep 2021 21:08:26 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 03 Sep 2021 21:08:27 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 03 Sep 2021 21:08:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 21:08:27 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:e98a9e31e599c3e38ecd12cf6b8493f4268c371026bae6d2280da418009b5bff`  
		Last Modified: Fri, 03 Sep 2021 00:52:57 GMT  
		Size: 43.2 MB (43177996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f698e334a0e8a436e04b2ef344b0ada5761244cf05829ece406e740b750b1bfa`  
		Last Modified: Fri, 03 Sep 2021 04:44:45 GMT  
		Size: 10.2 MB (10215862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62eef9137c22a6fa0d9b497479b8c3ba0d211b5f01fafd237e4dc3419146e22a`  
		Last Modified: Fri, 03 Sep 2021 04:44:44 GMT  
		Size: 4.1 MB (4096542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d524ec54ce2cc3514ffe7ba394bc8e3c9e9ba04493c6ba234d8be1645f4d4123`  
		Last Modified: Fri, 03 Sep 2021 21:08:49 GMT  
		Size: 13.0 MB (13027371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e6cba0468ee4e125ab0563615edf0f8999ef3a0275f4b80211c9cb7f22a5f0`  
		Last Modified: Fri, 03 Sep 2021 21:08:47 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f4dc5d2890c4f7d452390bfbcaf4a6c6c01fc1870bff8a9678760d952ecc49`  
		Last Modified: Fri, 03 Sep 2021 21:09:13 GMT  
		Size: 55.9 MB (55894146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4acf031730b9c6909438592b19bd91c23eca189ea86a1e3aabc0f5434ca0e2`  
		Last Modified: Fri, 03 Sep 2021 21:09:04 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:644a9eee361d6a8dd6c4324eaf8711e568e3f33c386174866840c15bbfcc1863`  
		Last Modified: Fri, 03 Sep 2021 21:09:04 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.6.1-alpine`

```console
$ docker pull kapacitor@sha256:7896801d6eeb35bbcbed36310760a3b1ff3120d16b23aaf20267a3e927b8936d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.6.1-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:b3c9c70bdad340a180f54ab64c17a420e8ea6544513bb86d1d5ee61c980c1f16
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62282802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c171de764c09f16e4ce559429bf58d7f552765083dabe7eeaff600d961ba3b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:23:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:23:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 01 Sep 2021 03:04:27 GMT
ENV KAPACITOR_VERSION=1.6.1
# Wed, 01 Sep 2021 03:04:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 01 Sep 2021 03:04:41 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 01 Sep 2021 03:04:41 GMT
EXPOSE 9092
# Wed, 01 Sep 2021 03:04:41 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 01 Sep 2021 03:04:42 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Wed, 01 Sep 2021 03:04:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 03:04:42 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69cd3502d3b453e253ea48e4ff56f5af4e25895a1bfa5e84cda59eaefce23be`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7087df4b29e442773e368f72aa50cd7765fd6e6b43879c83880b0038e62b9077`  
		Last Modified: Wed, 01 Sep 2021 00:25:29 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7cb5b6248de8e40cb59c8a172882bcf139b97f02ea65ba88919ed2aadef1e9`  
		Last Modified: Wed, 01 Sep 2021 03:05:26 GMT  
		Size: 59.2 MB (59199583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e72ce875cf5d94b0730927e9e97d3df95bdfb5651c544f52ac5c124f2f43e5`  
		Last Modified: Wed, 01 Sep 2021 03:05:17 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0b546e47c7e79bda5d79a7be609e9c46eedd0801b11be06c36d4c4bfde1b39`  
		Last Modified: Wed, 01 Sep 2021 03:05:17 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:7896801d6eeb35bbcbed36310760a3b1ff3120d16b23aaf20267a3e927b8936d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:b3c9c70bdad340a180f54ab64c17a420e8ea6544513bb86d1d5ee61c980c1f16
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62282802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c171de764c09f16e4ce559429bf58d7f552765083dabe7eeaff600d961ba3b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:23 GMT
ADD file:e3d2013df9d58cd9255c749dbd62e7b1b1bdf1c2ee644c17bb93e67d859f0815 in / 
# Tue, 31 Aug 2021 23:18:24 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 00:23:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 01 Sep 2021 00:23:43 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 01 Sep 2021 03:04:27 GMT
ENV KAPACITOR_VERSION=1.6.1
# Wed, 01 Sep 2021 03:04:40 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     rm -f /usr/src/kapacitor-*/kapacitor.conf &&     chmod +x /usr/src/kapacitor-*/* &&     cp -a /usr/src/kapacitor-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 01 Sep 2021 03:04:41 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 01 Sep 2021 03:04:41 GMT
EXPOSE 9092
# Wed, 01 Sep 2021 03:04:41 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 01 Sep 2021 03:04:42 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Wed, 01 Sep 2021 03:04:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 01 Sep 2021 03:04:42 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:e519532ddf75bafbbb0ad01d3fb678ef9395cd8554fa25bef4695bb6e11f39f1`  
		Last Modified: Tue, 31 Aug 2021 23:19:05 GMT  
		Size: 2.8 MB (2801707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69cd3502d3b453e253ea48e4ff56f5af4e25895a1bfa5e84cda59eaefce23be`  
		Last Modified: Wed, 01 Sep 2021 00:25:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7087df4b29e442773e368f72aa50cd7765fd6e6b43879c83880b0038e62b9077`  
		Last Modified: Wed, 01 Sep 2021 00:25:29 GMT  
		Size: 280.9 KB (280879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7cb5b6248de8e40cb59c8a172882bcf139b97f02ea65ba88919ed2aadef1e9`  
		Last Modified: Wed, 01 Sep 2021 03:05:26 GMT  
		Size: 59.2 MB (59199583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e72ce875cf5d94b0730927e9e97d3df95bdfb5651c544f52ac5c124f2f43e5`  
		Last Modified: Wed, 01 Sep 2021 03:05:17 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a0b546e47c7e79bda5d79a7be609e9c46eedd0801b11be06c36d4c4bfde1b39`  
		Last Modified: Wed, 01 Sep 2021 03:05:17 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:faed699d0a1a0d29e3b996b73375efaa229d133d4373f45d5ceef14e0e5ba5d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:7153c14ce9004d4389fc69f407311389e848df2e044c7c699b25ff1e9fa0b4fd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133606214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc13f62beab87315296150a800a4e1ba8dfc6bc1bf53ad6e6774cf958a1401a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 17 Aug 2021 01:25:56 GMT
ADD file:0d0aa1ebd07b0f301aaf1077d1e9f2e9be1859510dd8535e143571b347a2a379 in / 
# Tue, 17 Aug 2021 01:25:56 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 09:24:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 09:24:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 18 Aug 2021 07:01:25 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 18 Aug 2021 07:01:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 18 Aug 2021 07:01:40 GMT
ENV KAPACITOR_VERSION=1.6.1
# Wed, 18 Aug 2021 07:01:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 18 Aug 2021 07:01:45 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 18 Aug 2021 07:01:45 GMT
EXPOSE 9092
# Wed, 18 Aug 2021 07:01:45 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 18 Aug 2021 07:01:45 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 18 Aug 2021 07:01:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Aug 2021 07:01:46 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:eb18d230e067c240479c6a3f842e7f9d4ff1088e3072d0a3245829c4e356623f`  
		Last Modified: Tue, 17 Aug 2021 01:33:03 GMT  
		Size: 45.4 MB (45379966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83600c1b4583abb5830c6d4a039cbab9a102ac1a7b3b779854638a371bb7128f`  
		Last Modified: Tue, 17 Aug 2021 09:33:12 GMT  
		Size: 11.3 MB (11295906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae15c65bfa0fdc9053dcb734e6c034f5394ea0481dee3277f6e3e9fa07702d0`  
		Last Modified: Tue, 17 Aug 2021 09:33:11 GMT  
		Size: 4.3 MB (4342387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df9a81a6e6330b08dc4ea9322d4dbc9131ceb336f4f48222299992bee24d20c`  
		Last Modified: Wed, 18 Aug 2021 07:02:07 GMT  
		Size: 13.3 MB (13322522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ac9e7ace861b8fefc86ece32a745d3860247036ec12dca6a51e6436f64cfe6`  
		Last Modified: Wed, 18 Aug 2021 07:02:05 GMT  
		Size: 2.9 KB (2853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1cc761767c20764cf1890fd66d9fe9b0c73793ffd089bb7010d856e3379946`  
		Last Modified: Wed, 18 Aug 2021 07:02:29 GMT  
		Size: 59.3 MB (59262125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c31ea119f5e5d39540a41d2bd75569c0967d85b58e6af5592701e382cf3603`  
		Last Modified: Wed, 18 Aug 2021 07:02:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fb14f03d554baca4f313ccbaddb34e22c9da8d46e6a3aa2ff345503b0d9d06`  
		Last Modified: Wed, 18 Aug 2021 07:02:21 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:9c52d55020a0c2fa3865cb9dad8aa1ba1902489d2f9c80827fabbc6da7c847a4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.4 MB (126415227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e10e46e4144963c60e7c7c17197934352599c247f881567f6d5b5c738ff3f4a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 03 Sep 2021 00:42:34 GMT
ADD file:3a77488ae0a72e8fd504cb1354bd111f38a4fc9f3e541ee7ebce3ebc4eb9dc49 in / 
# Fri, 03 Sep 2021 00:42:34 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 04:36:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 04:36:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 03 Sep 2021 21:07:59 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Fri, 03 Sep 2021 21:08:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Sep 2021 21:08:20 GMT
ENV KAPACITOR_VERSION=1.6.1
# Fri, 03 Sep 2021 21:08:26 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Fri, 03 Sep 2021 21:08:26 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Fri, 03 Sep 2021 21:08:26 GMT
EXPOSE 9092
# Fri, 03 Sep 2021 21:08:26 GMT
VOLUME [/var/lib/kapacitor]
# Fri, 03 Sep 2021 21:08:27 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Fri, 03 Sep 2021 21:08:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Sep 2021 21:08:27 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:e98a9e31e599c3e38ecd12cf6b8493f4268c371026bae6d2280da418009b5bff`  
		Last Modified: Fri, 03 Sep 2021 00:52:57 GMT  
		Size: 43.2 MB (43177996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f698e334a0e8a436e04b2ef344b0ada5761244cf05829ece406e740b750b1bfa`  
		Last Modified: Fri, 03 Sep 2021 04:44:45 GMT  
		Size: 10.2 MB (10215862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62eef9137c22a6fa0d9b497479b8c3ba0d211b5f01fafd237e4dc3419146e22a`  
		Last Modified: Fri, 03 Sep 2021 04:44:44 GMT  
		Size: 4.1 MB (4096542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d524ec54ce2cc3514ffe7ba394bc8e3c9e9ba04493c6ba234d8be1645f4d4123`  
		Last Modified: Fri, 03 Sep 2021 21:08:49 GMT  
		Size: 13.0 MB (13027371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e6cba0468ee4e125ab0563615edf0f8999ef3a0275f4b80211c9cb7f22a5f0`  
		Last Modified: Fri, 03 Sep 2021 21:08:47 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f4dc5d2890c4f7d452390bfbcaf4a6c6c01fc1870bff8a9678760d952ecc49`  
		Last Modified: Fri, 03 Sep 2021 21:09:13 GMT  
		Size: 55.9 MB (55894146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4acf031730b9c6909438592b19bd91c23eca189ea86a1e3aabc0f5434ca0e2`  
		Last Modified: Fri, 03 Sep 2021 21:09:04 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:644a9eee361d6a8dd6c4324eaf8711e568e3f33c386174866840c15bbfcc1863`  
		Last Modified: Fri, 03 Sep 2021 21:09:04 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
