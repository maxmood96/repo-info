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
$ docker pull kapacitor@sha256:abf528b2d299a1fbf9959529b7d13214dd99ed7beaf51b1cc8b14e6a6a9d2074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.5` - linux; amd64

```console
$ docker pull kapacitor@sha256:98a7237cf5032535b285039654d280831775724bb46707554510bcb00a91c4ee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111566342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c589ca2b9e8663e421372f82355728e496cd155b9679217c3790d2923f26657`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 03 Sep 2021 01:23:33 GMT
ADD file:835effce8521d3a6cb00dc8bb358711e7a6ba1fd057b798681d9e006825dd3c1 in / 
# Fri, 03 Sep 2021 01:23:33 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 06:36:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 06:36:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 04 Sep 2021 09:18:28 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 04 Sep 2021 09:18:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 04 Sep 2021 09:18:37 GMT
ENV KAPACITOR_VERSION=1.5.9
# Sat, 04 Sep 2021 09:18:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 04 Sep 2021 09:18:42 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 04 Sep 2021 09:18:42 GMT
EXPOSE 9092
# Sat, 04 Sep 2021 09:18:42 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 04 Sep 2021 09:18:42 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 04 Sep 2021 09:18:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 04 Sep 2021 09:18:43 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:1c05d83e138cea8cb6ddd17442ab2138423db80e58408d93059f2ea25065952e`  
		Last Modified: Fri, 03 Sep 2021 01:31:39 GMT  
		Size: 45.4 MB (45379797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394ee1959bac9492a9fc64334844549eccd4274280678d81d6b5b19af703e2a6`  
		Last Modified: Fri, 03 Sep 2021 06:42:58 GMT  
		Size: 11.3 MB (11295763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5f175d1abbc6d4a7774bd2912a927aa78b90fb04fb43d591e3dda317c9bb96`  
		Last Modified: Fri, 03 Sep 2021 06:42:57 GMT  
		Size: 4.3 MB (4342391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96751b59d3825c066fe0b32c1411674b9b506ce92a115a446826d43b73a2e2f0`  
		Last Modified: Sat, 04 Sep 2021 09:19:20 GMT  
		Size: 13.3 MB (13325864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0bf8615443fb9e9e2d73c057719cb6942a9cf30264fdde513df2b95dff5dbf`  
		Last Modified: Sat, 04 Sep 2021 09:19:19 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ae74f23de4aa34388c5b35f810a9947edfcfb6f2f8c0f9d08ba2190e520ed7`  
		Last Modified: Sat, 04 Sep 2021 09:19:24 GMT  
		Size: 37.2 MB (37219216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f040d6447265e1c469e48f36a56b90b820839bb592eee8bec6a9ceb1c2ef044f`  
		Last Modified: Sat, 04 Sep 2021 09:19:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90957f97646e6e426c638ec5fa81cd0ba6c77bc53047e7826190ae316c548648`  
		Last Modified: Sat, 04 Sep 2021 09:19:19 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:4e952912d429ddb9a02309f69613d78feda6b6d358b26cf8964d3e68222a237b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104290097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67a020341cee6495c9694fe362cc49dd5b147adb9ee8d560ba595b7ef484775b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 03 Sep 2021 01:04:44 GMT
ADD file:f3526ca980237b2ca5289ca7a6c67760fc5726ce3c325de10f3f3111c1d4bdcd in / 
# Fri, 03 Sep 2021 01:04:45 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 03:03:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 03:03:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 04 Sep 2021 13:32:33 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 04 Sep 2021 13:32:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 04 Sep 2021 13:32:38 GMT
ENV KAPACITOR_VERSION=1.5.9
# Sat, 04 Sep 2021 13:32:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 04 Sep 2021 13:32:48 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 04 Sep 2021 13:32:48 GMT
EXPOSE 9092
# Sat, 04 Sep 2021 13:32:48 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 04 Sep 2021 13:32:49 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 04 Sep 2021 13:32:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 04 Sep 2021 13:32:50 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:aba3565275cf0ab544dbd3d27fb468b4682c0273b64b5f3d8c8fe06ca3467237`  
		Last Modified: Fri, 03 Sep 2021 01:21:57 GMT  
		Size: 42.1 MB (42119584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d7b8704af020029979f5a4bfc12eaea904235f452d75b61476aa90807ec20b`  
		Last Modified: Fri, 03 Sep 2021 03:22:05 GMT  
		Size: 10.0 MB (9951651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef77f0ed56b31ff8d57db5fd7149505dac04ef41f4919d6a59ed5e3725a6f4e`  
		Last Modified: Fri, 03 Sep 2021 03:22:03 GMT  
		Size: 3.9 MB (3921218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027fcbb3ca8a53134aeafa3066743973d0f31bf0bc40b01e608a24a7adc44437`  
		Last Modified: Sat, 04 Sep 2021 13:33:20 GMT  
		Size: 13.5 MB (13507617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8943aca7ea28bf50483db5dc53f94a2c969d18cb965804192c01470da261441`  
		Last Modified: Sat, 04 Sep 2021 13:33:15 GMT  
		Size: 2.9 KB (2850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8eb3cbaca98841323ceeea57bbbef9888cad3994b28c1e077b015837c3c2fa`  
		Last Modified: Sat, 04 Sep 2021 13:33:32 GMT  
		Size: 34.8 MB (34786720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c742aaabe5af204b046da4003781c43f0520eb05afeffb60fdf36508e346f907`  
		Last Modified: Sat, 04 Sep 2021 13:33:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091f453524c5f516f3476fce49962a05f83f7b3f7249c50ae14983c2659f53c1`  
		Last Modified: Sat, 04 Sep 2021 13:33:15 GMT  
		Size: 232.0 B  
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
$ docker pull kapacitor@sha256:abf528b2d299a1fbf9959529b7d13214dd99ed7beaf51b1cc8b14e6a6a9d2074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:1.5.9` - linux; amd64

```console
$ docker pull kapacitor@sha256:98a7237cf5032535b285039654d280831775724bb46707554510bcb00a91c4ee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111566342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c589ca2b9e8663e421372f82355728e496cd155b9679217c3790d2923f26657`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 03 Sep 2021 01:23:33 GMT
ADD file:835effce8521d3a6cb00dc8bb358711e7a6ba1fd057b798681d9e006825dd3c1 in / 
# Fri, 03 Sep 2021 01:23:33 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 06:36:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 06:36:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 04 Sep 2021 09:18:28 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 04 Sep 2021 09:18:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 04 Sep 2021 09:18:37 GMT
ENV KAPACITOR_VERSION=1.5.9
# Sat, 04 Sep 2021 09:18:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 04 Sep 2021 09:18:42 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 04 Sep 2021 09:18:42 GMT
EXPOSE 9092
# Sat, 04 Sep 2021 09:18:42 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 04 Sep 2021 09:18:42 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 04 Sep 2021 09:18:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 04 Sep 2021 09:18:43 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:1c05d83e138cea8cb6ddd17442ab2138423db80e58408d93059f2ea25065952e`  
		Last Modified: Fri, 03 Sep 2021 01:31:39 GMT  
		Size: 45.4 MB (45379797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394ee1959bac9492a9fc64334844549eccd4274280678d81d6b5b19af703e2a6`  
		Last Modified: Fri, 03 Sep 2021 06:42:58 GMT  
		Size: 11.3 MB (11295763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5f175d1abbc6d4a7774bd2912a927aa78b90fb04fb43d591e3dda317c9bb96`  
		Last Modified: Fri, 03 Sep 2021 06:42:57 GMT  
		Size: 4.3 MB (4342391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96751b59d3825c066fe0b32c1411674b9b506ce92a115a446826d43b73a2e2f0`  
		Last Modified: Sat, 04 Sep 2021 09:19:20 GMT  
		Size: 13.3 MB (13325864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0bf8615443fb9e9e2d73c057719cb6942a9cf30264fdde513df2b95dff5dbf`  
		Last Modified: Sat, 04 Sep 2021 09:19:19 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ae74f23de4aa34388c5b35f810a9947edfcfb6f2f8c0f9d08ba2190e520ed7`  
		Last Modified: Sat, 04 Sep 2021 09:19:24 GMT  
		Size: 37.2 MB (37219216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f040d6447265e1c469e48f36a56b90b820839bb592eee8bec6a9ceb1c2ef044f`  
		Last Modified: Sat, 04 Sep 2021 09:19:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90957f97646e6e426c638ec5fa81cd0ba6c77bc53047e7826190ae316c548648`  
		Last Modified: Sat, 04 Sep 2021 09:19:19 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.5.9` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:4e952912d429ddb9a02309f69613d78feda6b6d358b26cf8964d3e68222a237b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104290097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67a020341cee6495c9694fe362cc49dd5b147adb9ee8d560ba595b7ef484775b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 03 Sep 2021 01:04:44 GMT
ADD file:f3526ca980237b2ca5289ca7a6c67760fc5726ce3c325de10f3f3111c1d4bdcd in / 
# Fri, 03 Sep 2021 01:04:45 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 03:03:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 03:03:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 04 Sep 2021 13:32:33 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 04 Sep 2021 13:32:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 04 Sep 2021 13:32:38 GMT
ENV KAPACITOR_VERSION=1.5.9
# Sat, 04 Sep 2021 13:32:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 04 Sep 2021 13:32:48 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 04 Sep 2021 13:32:48 GMT
EXPOSE 9092
# Sat, 04 Sep 2021 13:32:48 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 04 Sep 2021 13:32:49 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 04 Sep 2021 13:32:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 04 Sep 2021 13:32:50 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:aba3565275cf0ab544dbd3d27fb468b4682c0273b64b5f3d8c8fe06ca3467237`  
		Last Modified: Fri, 03 Sep 2021 01:21:57 GMT  
		Size: 42.1 MB (42119584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d7b8704af020029979f5a4bfc12eaea904235f452d75b61476aa90807ec20b`  
		Last Modified: Fri, 03 Sep 2021 03:22:05 GMT  
		Size: 10.0 MB (9951651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef77f0ed56b31ff8d57db5fd7149505dac04ef41f4919d6a59ed5e3725a6f4e`  
		Last Modified: Fri, 03 Sep 2021 03:22:03 GMT  
		Size: 3.9 MB (3921218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027fcbb3ca8a53134aeafa3066743973d0f31bf0bc40b01e608a24a7adc44437`  
		Last Modified: Sat, 04 Sep 2021 13:33:20 GMT  
		Size: 13.5 MB (13507617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8943aca7ea28bf50483db5dc53f94a2c969d18cb965804192c01470da261441`  
		Last Modified: Sat, 04 Sep 2021 13:33:15 GMT  
		Size: 2.9 KB (2850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8eb3cbaca98841323ceeea57bbbef9888cad3994b28c1e077b015837c3c2fa`  
		Last Modified: Sat, 04 Sep 2021 13:33:32 GMT  
		Size: 34.8 MB (34786720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c742aaabe5af204b046da4003781c43f0520eb05afeffb60fdf36508e346f907`  
		Last Modified: Sat, 04 Sep 2021 13:33:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091f453524c5f516f3476fce49962a05f83f7b3f7249c50ae14983c2659f53c1`  
		Last Modified: Sat, 04 Sep 2021 13:33:15 GMT  
		Size: 232.0 B  
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
$ docker pull kapacitor@sha256:7ca9841052d79c42fc55744df1c8a3c4628455af55cf0e2e802806f7d526d2c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:1.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:c11f17dd18be88f37051ce3f83de15da8271027a11bca96c00461a17390e596d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133609177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cdcd91b8c7b48c316f0bc0eb809ca839159ea40d3b65364ad820d0cdf0440e8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 03 Sep 2021 01:23:33 GMT
ADD file:835effce8521d3a6cb00dc8bb358711e7a6ba1fd057b798681d9e006825dd3c1 in / 
# Fri, 03 Sep 2021 01:23:33 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 06:36:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 06:36:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 04 Sep 2021 09:18:28 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 04 Sep 2021 09:18:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 04 Sep 2021 09:18:51 GMT
ENV KAPACITOR_VERSION=1.6.1
# Sat, 04 Sep 2021 09:18:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 04 Sep 2021 09:18:57 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 04 Sep 2021 09:18:58 GMT
EXPOSE 9092
# Sat, 04 Sep 2021 09:18:58 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 04 Sep 2021 09:18:58 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 04 Sep 2021 09:18:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 04 Sep 2021 09:18:58 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:1c05d83e138cea8cb6ddd17442ab2138423db80e58408d93059f2ea25065952e`  
		Last Modified: Fri, 03 Sep 2021 01:31:39 GMT  
		Size: 45.4 MB (45379797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394ee1959bac9492a9fc64334844549eccd4274280678d81d6b5b19af703e2a6`  
		Last Modified: Fri, 03 Sep 2021 06:42:58 GMT  
		Size: 11.3 MB (11295763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5f175d1abbc6d4a7774bd2912a927aa78b90fb04fb43d591e3dda317c9bb96`  
		Last Modified: Fri, 03 Sep 2021 06:42:57 GMT  
		Size: 4.3 MB (4342391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96751b59d3825c066fe0b32c1411674b9b506ce92a115a446826d43b73a2e2f0`  
		Last Modified: Sat, 04 Sep 2021 09:19:20 GMT  
		Size: 13.3 MB (13325864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0bf8615443fb9e9e2d73c057719cb6942a9cf30264fdde513df2b95dff5dbf`  
		Last Modified: Sat, 04 Sep 2021 09:19:19 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67dfd66f818a41df9fa56676b83a9589b4113020628850279f0728763a4141bd`  
		Last Modified: Sat, 04 Sep 2021 09:19:43 GMT  
		Size: 59.3 MB (59262050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f619b25d6c94fb25c90635e3cba8b315eeae743d0b3db37e46659c0225a6ce`  
		Last Modified: Sat, 04 Sep 2021 09:19:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3772a60126f73b598f830c24fd6ffe2d2298c8be96913f64908180f023c3d8b1`  
		Last Modified: Sat, 04 Sep 2021 09:19:35 GMT  
		Size: 232.0 B  
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
$ docker pull kapacitor@sha256:7ca9841052d79c42fc55744df1c8a3c4628455af55cf0e2e802806f7d526d2c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:1.6.1` - linux; amd64

```console
$ docker pull kapacitor@sha256:c11f17dd18be88f37051ce3f83de15da8271027a11bca96c00461a17390e596d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133609177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cdcd91b8c7b48c316f0bc0eb809ca839159ea40d3b65364ad820d0cdf0440e8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 03 Sep 2021 01:23:33 GMT
ADD file:835effce8521d3a6cb00dc8bb358711e7a6ba1fd057b798681d9e006825dd3c1 in / 
# Fri, 03 Sep 2021 01:23:33 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 06:36:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 06:36:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 04 Sep 2021 09:18:28 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 04 Sep 2021 09:18:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 04 Sep 2021 09:18:51 GMT
ENV KAPACITOR_VERSION=1.6.1
# Sat, 04 Sep 2021 09:18:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 04 Sep 2021 09:18:57 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 04 Sep 2021 09:18:58 GMT
EXPOSE 9092
# Sat, 04 Sep 2021 09:18:58 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 04 Sep 2021 09:18:58 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 04 Sep 2021 09:18:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 04 Sep 2021 09:18:58 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:1c05d83e138cea8cb6ddd17442ab2138423db80e58408d93059f2ea25065952e`  
		Last Modified: Fri, 03 Sep 2021 01:31:39 GMT  
		Size: 45.4 MB (45379797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394ee1959bac9492a9fc64334844549eccd4274280678d81d6b5b19af703e2a6`  
		Last Modified: Fri, 03 Sep 2021 06:42:58 GMT  
		Size: 11.3 MB (11295763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5f175d1abbc6d4a7774bd2912a927aa78b90fb04fb43d591e3dda317c9bb96`  
		Last Modified: Fri, 03 Sep 2021 06:42:57 GMT  
		Size: 4.3 MB (4342391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96751b59d3825c066fe0b32c1411674b9b506ce92a115a446826d43b73a2e2f0`  
		Last Modified: Sat, 04 Sep 2021 09:19:20 GMT  
		Size: 13.3 MB (13325864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0bf8615443fb9e9e2d73c057719cb6942a9cf30264fdde513df2b95dff5dbf`  
		Last Modified: Sat, 04 Sep 2021 09:19:19 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67dfd66f818a41df9fa56676b83a9589b4113020628850279f0728763a4141bd`  
		Last Modified: Sat, 04 Sep 2021 09:19:43 GMT  
		Size: 59.3 MB (59262050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f619b25d6c94fb25c90635e3cba8b315eeae743d0b3db37e46659c0225a6ce`  
		Last Modified: Sat, 04 Sep 2021 09:19:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3772a60126f73b598f830c24fd6ffe2d2298c8be96913f64908180f023c3d8b1`  
		Last Modified: Sat, 04 Sep 2021 09:19:35 GMT  
		Size: 232.0 B  
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
$ docker pull kapacitor@sha256:7ca9841052d79c42fc55744df1c8a3c4628455af55cf0e2e802806f7d526d2c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:c11f17dd18be88f37051ce3f83de15da8271027a11bca96c00461a17390e596d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133609177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cdcd91b8c7b48c316f0bc0eb809ca839159ea40d3b65364ad820d0cdf0440e8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Fri, 03 Sep 2021 01:23:33 GMT
ADD file:835effce8521d3a6cb00dc8bb358711e7a6ba1fd057b798681d9e006825dd3c1 in / 
# Fri, 03 Sep 2021 01:23:33 GMT
CMD ["bash"]
# Fri, 03 Sep 2021 06:36:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 03 Sep 2021 06:36:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 04 Sep 2021 09:18:28 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Sat, 04 Sep 2021 09:18:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Sat, 04 Sep 2021 09:18:51 GMT
ENV KAPACITOR_VERSION=1.6.1
# Sat, 04 Sep 2021 09:18:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Sat, 04 Sep 2021 09:18:57 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Sat, 04 Sep 2021 09:18:58 GMT
EXPOSE 9092
# Sat, 04 Sep 2021 09:18:58 GMT
VOLUME [/var/lib/kapacitor]
# Sat, 04 Sep 2021 09:18:58 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Sat, 04 Sep 2021 09:18:58 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 04 Sep 2021 09:18:58 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:1c05d83e138cea8cb6ddd17442ab2138423db80e58408d93059f2ea25065952e`  
		Last Modified: Fri, 03 Sep 2021 01:31:39 GMT  
		Size: 45.4 MB (45379797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394ee1959bac9492a9fc64334844549eccd4274280678d81d6b5b19af703e2a6`  
		Last Modified: Fri, 03 Sep 2021 06:42:58 GMT  
		Size: 11.3 MB (11295763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5f175d1abbc6d4a7774bd2912a927aa78b90fb04fb43d591e3dda317c9bb96`  
		Last Modified: Fri, 03 Sep 2021 06:42:57 GMT  
		Size: 4.3 MB (4342391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96751b59d3825c066fe0b32c1411674b9b506ce92a115a446826d43b73a2e2f0`  
		Last Modified: Sat, 04 Sep 2021 09:19:20 GMT  
		Size: 13.3 MB (13325864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0bf8615443fb9e9e2d73c057719cb6942a9cf30264fdde513df2b95dff5dbf`  
		Last Modified: Sat, 04 Sep 2021 09:19:19 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67dfd66f818a41df9fa56676b83a9589b4113020628850279f0728763a4141bd`  
		Last Modified: Sat, 04 Sep 2021 09:19:43 GMT  
		Size: 59.3 MB (59262050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f619b25d6c94fb25c90635e3cba8b315eeae743d0b3db37e46659c0225a6ce`  
		Last Modified: Sat, 04 Sep 2021 09:19:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3772a60126f73b598f830c24fd6ffe2d2298c8be96913f64908180f023c3d8b1`  
		Last Modified: Sat, 04 Sep 2021 09:19:35 GMT  
		Size: 232.0 B  
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
