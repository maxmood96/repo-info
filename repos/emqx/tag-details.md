<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:4`](#emqx4)
-	[`emqx:4.3`](#emqx43)
-	[`emqx:4.3.15`](#emqx4315)
-	[`emqx:4.4`](#emqx44)
-	[`emqx:4.4.4`](#emqx444)
-	[`emqx:latest`](#emqxlatest)

## `emqx:4`

```console
$ docker pull emqx@sha256:04ecf66e6c70fcbd75b76fb586283913c76f5818ce1221aee59368dc83d51338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4` - linux; amd64

```console
$ docker pull emqx@sha256:fb2257b976208201d7e33177427e0be10a94168dfc39bb257de940e3e339317c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124836587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f34e0da055730b616341cff9eecc144f26b5d0df9a5c84e0d83c6957bed4ed`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 03:59:23 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:59:23 GMT
ENV EMQX_VERSION=4.4.4
# Tue, 13 Sep 2022 03:59:23 GMT
ENV OTP=otp24.1.5-3
# Tue, 13 Sep 2022 03:59:27 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 13 Sep 2022 03:59:33 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 13 Sep 2022 03:59:33 GMT
WORKDIR /opt/emqx
# Tue, 13 Sep 2022 03:59:33 GMT
USER emqx
# Tue, 13 Sep 2022 03:59:33 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Sep 2022 03:59:33 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 13 Sep 2022 03:59:34 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 13 Sep 2022 03:59:34 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 03:59:34 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1718cfc9ab1a66a45b214f22aad7acd47b0ee5360a06535c5c7108a46fbee1`  
		Last Modified: Tue, 13 Sep 2022 04:00:04 GMT  
		Size: 2.6 MB (2569503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9004193e42b45379e1def33644c4824ac57de3e65880a3316bb03d535de9fb`  
		Last Modified: Tue, 13 Sep 2022 04:00:08 GMT  
		Size: 45.4 MB (45424530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e1552a0b575c61fc3b386fa2dccef591129271e5914cec5e588908f4e26418`  
		Last Modified: Tue, 13 Sep 2022 04:00:08 GMT  
		Size: 45.4 MB (45437326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9dd750521fd7780e66dac97a3c8dc8ff81efc749ccf491617bdde85021e3dee`  
		Last Modified: Tue, 13 Sep 2022 04:00:03 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:b9b2be320c2a2469aa9c8de01a47db24c4b11d7d8980a59e39259a4976cfc49c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110033038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcabc472c20703152f5e87f687372023f66139abb5c82b7bdecb205d4139962f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:32 GMT
ADD file:90344130400909b0ad12bb54d439b0e4868fc5863f538f676e6fdfeaeb4dad51 in / 
# Tue, 23 Aug 2022 01:52:33 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:48:22 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:48:22 GMT
ENV EMQX_VERSION=4.4.4
# Tue, 23 Aug 2022 02:48:23 GMT
ENV OTP=otp24.1.5-3
# Tue, 23 Aug 2022 02:48:28 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 23 Aug 2022 02:48:30 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 23 Aug 2022 02:48:30 GMT
WORKDIR /opt/emqx
# Tue, 23 Aug 2022 02:48:31 GMT
USER emqx
# Tue, 23 Aug 2022 02:48:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 23 Aug 2022 02:48:33 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 23 Aug 2022 02:48:35 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 23 Aug 2022 02:48:35 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:48:36 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:5b142346550416c75ea412d21741de5eaf3e76857affc12fab789277f81f53b3`  
		Last Modified: Tue, 23 Aug 2022 01:58:00 GMT  
		Size: 30.1 MB (30063788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76875b2a2774be642d6a500995cffb336dc0b7fce71c6554e4415cc6df01a4b2`  
		Last Modified: Tue, 23 Aug 2022 02:49:14 GMT  
		Size: 2.4 MB (2353690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bd6d30cd6371bb62afaacfb03fb3dd2ea33d16d25087af221e21d238febfc9`  
		Last Modified: Tue, 23 Aug 2022 02:49:18 GMT  
		Size: 38.8 MB (38806760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cf00ca63decf520e5ab938da78a25d9ad2816babd18a8e5594cc877a2d4791`  
		Last Modified: Tue, 23 Aug 2022 02:49:18 GMT  
		Size: 38.8 MB (38807691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c5c2a2bac240c35e3c2ef46b56552e483b7324b2c74c09c78bc86d2a7e7b0b`  
		Last Modified: Tue, 23 Aug 2022 02:49:13 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.3`

```console
$ docker pull emqx@sha256:51db3d306ddeee3dd048df36a5d414c84621cd4f3cc1588d747855d760140017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.3` - linux; amd64

```console
$ docker pull emqx@sha256:32c4518a52c03e9d829291167d34d19874eadea0abe85e9d1b2ef00aa2d35f9b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103855150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51febc65abc7cc401b23f068a0bc6a1d7de5c07b275bcbf54828f0a0208f4578`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:48 GMT
ADD file:782d864aa72c2d5fb599311ebae56db4067d2e91ff532c1aaf1a291c3dbce5bb in / 
# Tue, 13 Sep 2022 00:56:49 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 03:59:04 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:59:04 GMT
ENV EMQX_VERSION=4.3.15
# Tue, 13 Sep 2022 03:59:08 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="8f44386aebf472297377d7b6b595638f323227347047d5278dce9c0cd04963bc"; fi;     if [ ${arch} = "arm64" ]; then sha256="b0094028d388684136be975c574d98295205dd5a343045f76f423a109535e016"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 13 Sep 2022 03:59:13 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 13 Sep 2022 03:59:14 GMT
WORKDIR /opt/emqx
# Tue, 13 Sep 2022 03:59:14 GMT
USER emqx
# Tue, 13 Sep 2022 03:59:14 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Sep 2022 03:59:14 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 13 Sep 2022 03:59:14 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Tue, 13 Sep 2022 03:59:14 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 03:59:14 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:4b7b4a8876e2f677668e51b8473f97a237d3d4df201b9df4031bcaa8068370b1`  
		Last Modified: Tue, 13 Sep 2022 01:01:16 GMT  
		Size: 27.1 MB (27130552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76cceb548f828bd9213a8cdc23f9bfaa531c7f1d73ccabbdfaadce43a352c0e0`  
		Last Modified: Tue, 13 Sep 2022 03:59:49 GMT  
		Size: 4.6 MB (4610632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07eca7a7df10e3eb8a591f9a51d6f53034b529d3dfa6ffc056fdbce0dcaff11`  
		Last Modified: Tue, 13 Sep 2022 03:59:53 GMT  
		Size: 36.1 MB (36056967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00867241da64c428bcc94c253fff65bfc0df3bd1bc7c4c38be22ac90db7dd957`  
		Last Modified: Tue, 13 Sep 2022 03:59:53 GMT  
		Size: 36.1 MB (36055960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba36560a74cdb0c834d5c092cee7c1b2a59f000b123d092237951250e0a973e7`  
		Last Modified: Tue, 13 Sep 2022 03:59:48 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.3` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:3ac92e082f78f6c79436d92a8bc0b02b223dc6e51f3362475630f57557b8256d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101934052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653d6bc567df59282c0e919f8da05ed6944db4c1dd664b56f0276722f1c7e4f4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:58 GMT
ADD file:4c5bca2d158b11314fb47a6d4b34239575621c2f00f92e77870f23aa02913fac in / 
# Tue, 23 Aug 2022 01:52:59 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:47:57 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:47:57 GMT
ENV EMQX_VERSION=4.3.15
# Tue, 23 Aug 2022 02:48:03 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="8f44386aebf472297377d7b6b595638f323227347047d5278dce9c0cd04963bc"; fi;     if [ ${arch} = "arm64" ]; then sha256="b0094028d388684136be975c574d98295205dd5a343045f76f423a109535e016"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 23 Aug 2022 02:48:04 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 23 Aug 2022 02:48:05 GMT
WORKDIR /opt/emqx
# Tue, 23 Aug 2022 02:48:05 GMT
USER emqx
# Tue, 23 Aug 2022 02:48:06 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 23 Aug 2022 02:48:07 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 23 Aug 2022 02:48:09 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Tue, 23 Aug 2022 02:48:09 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:48:10 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:a84b81edbdb892b3702892bbb01c240695b0b9d619fda43a9b951c9d2df1443c`  
		Last Modified: Tue, 23 Aug 2022 01:58:50 GMT  
		Size: 25.9 MB (25912515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4cfd2f8a927d82ae5d26d82ed5148ad6a2a04e77a07b7a8b09510f39a69d0b3`  
		Last Modified: Tue, 23 Aug 2022 02:48:59 GMT  
		Size: 4.5 MB (4485521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850adcf8056d1b068f8f7c9c4ac1bf58621a291060fffbcf0c53d16fd5ff690a`  
		Last Modified: Tue, 23 Aug 2022 02:49:02 GMT  
		Size: 35.8 MB (35761707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0121fab99e6fd1a8eef8c52ec64255cf4b03c04c6836e7d1bef8bc080d74a300`  
		Last Modified: Tue, 23 Aug 2022 02:49:02 GMT  
		Size: 35.8 MB (35773268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79194c5998efc0a6588755f766dae727b0bce61d7ee1c6ec94657fa7de17ae4`  
		Last Modified: Tue, 23 Aug 2022 02:48:58 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.3.15`

```console
$ docker pull emqx@sha256:51db3d306ddeee3dd048df36a5d414c84621cd4f3cc1588d747855d760140017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.3.15` - linux; amd64

```console
$ docker pull emqx@sha256:32c4518a52c03e9d829291167d34d19874eadea0abe85e9d1b2ef00aa2d35f9b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103855150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51febc65abc7cc401b23f068a0bc6a1d7de5c07b275bcbf54828f0a0208f4578`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:48 GMT
ADD file:782d864aa72c2d5fb599311ebae56db4067d2e91ff532c1aaf1a291c3dbce5bb in / 
# Tue, 13 Sep 2022 00:56:49 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 03:59:04 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:59:04 GMT
ENV EMQX_VERSION=4.3.15
# Tue, 13 Sep 2022 03:59:08 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="8f44386aebf472297377d7b6b595638f323227347047d5278dce9c0cd04963bc"; fi;     if [ ${arch} = "arm64" ]; then sha256="b0094028d388684136be975c574d98295205dd5a343045f76f423a109535e016"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 13 Sep 2022 03:59:13 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 13 Sep 2022 03:59:14 GMT
WORKDIR /opt/emqx
# Tue, 13 Sep 2022 03:59:14 GMT
USER emqx
# Tue, 13 Sep 2022 03:59:14 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Sep 2022 03:59:14 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 13 Sep 2022 03:59:14 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Tue, 13 Sep 2022 03:59:14 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 03:59:14 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:4b7b4a8876e2f677668e51b8473f97a237d3d4df201b9df4031bcaa8068370b1`  
		Last Modified: Tue, 13 Sep 2022 01:01:16 GMT  
		Size: 27.1 MB (27130552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76cceb548f828bd9213a8cdc23f9bfaa531c7f1d73ccabbdfaadce43a352c0e0`  
		Last Modified: Tue, 13 Sep 2022 03:59:49 GMT  
		Size: 4.6 MB (4610632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07eca7a7df10e3eb8a591f9a51d6f53034b529d3dfa6ffc056fdbce0dcaff11`  
		Last Modified: Tue, 13 Sep 2022 03:59:53 GMT  
		Size: 36.1 MB (36056967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00867241da64c428bcc94c253fff65bfc0df3bd1bc7c4c38be22ac90db7dd957`  
		Last Modified: Tue, 13 Sep 2022 03:59:53 GMT  
		Size: 36.1 MB (36055960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba36560a74cdb0c834d5c092cee7c1b2a59f000b123d092237951250e0a973e7`  
		Last Modified: Tue, 13 Sep 2022 03:59:48 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.3.15` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:3ac92e082f78f6c79436d92a8bc0b02b223dc6e51f3362475630f57557b8256d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101934052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653d6bc567df59282c0e919f8da05ed6944db4c1dd664b56f0276722f1c7e4f4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:58 GMT
ADD file:4c5bca2d158b11314fb47a6d4b34239575621c2f00f92e77870f23aa02913fac in / 
# Tue, 23 Aug 2022 01:52:59 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:47:57 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:47:57 GMT
ENV EMQX_VERSION=4.3.15
# Tue, 23 Aug 2022 02:48:03 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="8f44386aebf472297377d7b6b595638f323227347047d5278dce9c0cd04963bc"; fi;     if [ ${arch} = "arm64" ]; then sha256="b0094028d388684136be975c574d98295205dd5a343045f76f423a109535e016"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 23 Aug 2022 02:48:04 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 23 Aug 2022 02:48:05 GMT
WORKDIR /opt/emqx
# Tue, 23 Aug 2022 02:48:05 GMT
USER emqx
# Tue, 23 Aug 2022 02:48:06 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 23 Aug 2022 02:48:07 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 23 Aug 2022 02:48:09 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Tue, 23 Aug 2022 02:48:09 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:48:10 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:a84b81edbdb892b3702892bbb01c240695b0b9d619fda43a9b951c9d2df1443c`  
		Last Modified: Tue, 23 Aug 2022 01:58:50 GMT  
		Size: 25.9 MB (25912515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4cfd2f8a927d82ae5d26d82ed5148ad6a2a04e77a07b7a8b09510f39a69d0b3`  
		Last Modified: Tue, 23 Aug 2022 02:48:59 GMT  
		Size: 4.5 MB (4485521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850adcf8056d1b068f8f7c9c4ac1bf58621a291060fffbcf0c53d16fd5ff690a`  
		Last Modified: Tue, 23 Aug 2022 02:49:02 GMT  
		Size: 35.8 MB (35761707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0121fab99e6fd1a8eef8c52ec64255cf4b03c04c6836e7d1bef8bc080d74a300`  
		Last Modified: Tue, 23 Aug 2022 02:49:02 GMT  
		Size: 35.8 MB (35773268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a79194c5998efc0a6588755f766dae727b0bce61d7ee1c6ec94657fa7de17ae4`  
		Last Modified: Tue, 23 Aug 2022 02:48:58 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4`

```console
$ docker pull emqx@sha256:04ecf66e6c70fcbd75b76fb586283913c76f5818ce1221aee59368dc83d51338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.4` - linux; amd64

```console
$ docker pull emqx@sha256:fb2257b976208201d7e33177427e0be10a94168dfc39bb257de940e3e339317c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124836587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f34e0da055730b616341cff9eecc144f26b5d0df9a5c84e0d83c6957bed4ed`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 03:59:23 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:59:23 GMT
ENV EMQX_VERSION=4.4.4
# Tue, 13 Sep 2022 03:59:23 GMT
ENV OTP=otp24.1.5-3
# Tue, 13 Sep 2022 03:59:27 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 13 Sep 2022 03:59:33 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 13 Sep 2022 03:59:33 GMT
WORKDIR /opt/emqx
# Tue, 13 Sep 2022 03:59:33 GMT
USER emqx
# Tue, 13 Sep 2022 03:59:33 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Sep 2022 03:59:33 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 13 Sep 2022 03:59:34 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 13 Sep 2022 03:59:34 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 03:59:34 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1718cfc9ab1a66a45b214f22aad7acd47b0ee5360a06535c5c7108a46fbee1`  
		Last Modified: Tue, 13 Sep 2022 04:00:04 GMT  
		Size: 2.6 MB (2569503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9004193e42b45379e1def33644c4824ac57de3e65880a3316bb03d535de9fb`  
		Last Modified: Tue, 13 Sep 2022 04:00:08 GMT  
		Size: 45.4 MB (45424530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e1552a0b575c61fc3b386fa2dccef591129271e5914cec5e588908f4e26418`  
		Last Modified: Tue, 13 Sep 2022 04:00:08 GMT  
		Size: 45.4 MB (45437326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9dd750521fd7780e66dac97a3c8dc8ff81efc749ccf491617bdde85021e3dee`  
		Last Modified: Tue, 13 Sep 2022 04:00:03 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:b9b2be320c2a2469aa9c8de01a47db24c4b11d7d8980a59e39259a4976cfc49c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110033038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcabc472c20703152f5e87f687372023f66139abb5c82b7bdecb205d4139962f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:32 GMT
ADD file:90344130400909b0ad12bb54d439b0e4868fc5863f538f676e6fdfeaeb4dad51 in / 
# Tue, 23 Aug 2022 01:52:33 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:48:22 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:48:22 GMT
ENV EMQX_VERSION=4.4.4
# Tue, 23 Aug 2022 02:48:23 GMT
ENV OTP=otp24.1.5-3
# Tue, 23 Aug 2022 02:48:28 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 23 Aug 2022 02:48:30 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 23 Aug 2022 02:48:30 GMT
WORKDIR /opt/emqx
# Tue, 23 Aug 2022 02:48:31 GMT
USER emqx
# Tue, 23 Aug 2022 02:48:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 23 Aug 2022 02:48:33 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 23 Aug 2022 02:48:35 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 23 Aug 2022 02:48:35 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:48:36 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:5b142346550416c75ea412d21741de5eaf3e76857affc12fab789277f81f53b3`  
		Last Modified: Tue, 23 Aug 2022 01:58:00 GMT  
		Size: 30.1 MB (30063788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76875b2a2774be642d6a500995cffb336dc0b7fce71c6554e4415cc6df01a4b2`  
		Last Modified: Tue, 23 Aug 2022 02:49:14 GMT  
		Size: 2.4 MB (2353690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bd6d30cd6371bb62afaacfb03fb3dd2ea33d16d25087af221e21d238febfc9`  
		Last Modified: Tue, 23 Aug 2022 02:49:18 GMT  
		Size: 38.8 MB (38806760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cf00ca63decf520e5ab938da78a25d9ad2816babd18a8e5594cc877a2d4791`  
		Last Modified: Tue, 23 Aug 2022 02:49:18 GMT  
		Size: 38.8 MB (38807691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c5c2a2bac240c35e3c2ef46b56552e483b7324b2c74c09c78bc86d2a7e7b0b`  
		Last Modified: Tue, 23 Aug 2022 02:49:13 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4.4`

```console
$ docker pull emqx@sha256:04ecf66e6c70fcbd75b76fb586283913c76f5818ce1221aee59368dc83d51338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.4.4` - linux; amd64

```console
$ docker pull emqx@sha256:fb2257b976208201d7e33177427e0be10a94168dfc39bb257de940e3e339317c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124836587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f34e0da055730b616341cff9eecc144f26b5d0df9a5c84e0d83c6957bed4ed`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 03:59:23 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:59:23 GMT
ENV EMQX_VERSION=4.4.4
# Tue, 13 Sep 2022 03:59:23 GMT
ENV OTP=otp24.1.5-3
# Tue, 13 Sep 2022 03:59:27 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 13 Sep 2022 03:59:33 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 13 Sep 2022 03:59:33 GMT
WORKDIR /opt/emqx
# Tue, 13 Sep 2022 03:59:33 GMT
USER emqx
# Tue, 13 Sep 2022 03:59:33 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Sep 2022 03:59:33 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 13 Sep 2022 03:59:34 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 13 Sep 2022 03:59:34 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 03:59:34 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1718cfc9ab1a66a45b214f22aad7acd47b0ee5360a06535c5c7108a46fbee1`  
		Last Modified: Tue, 13 Sep 2022 04:00:04 GMT  
		Size: 2.6 MB (2569503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9004193e42b45379e1def33644c4824ac57de3e65880a3316bb03d535de9fb`  
		Last Modified: Tue, 13 Sep 2022 04:00:08 GMT  
		Size: 45.4 MB (45424530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e1552a0b575c61fc3b386fa2dccef591129271e5914cec5e588908f4e26418`  
		Last Modified: Tue, 13 Sep 2022 04:00:08 GMT  
		Size: 45.4 MB (45437326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9dd750521fd7780e66dac97a3c8dc8ff81efc749ccf491617bdde85021e3dee`  
		Last Modified: Tue, 13 Sep 2022 04:00:03 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.4.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:b9b2be320c2a2469aa9c8de01a47db24c4b11d7d8980a59e39259a4976cfc49c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110033038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcabc472c20703152f5e87f687372023f66139abb5c82b7bdecb205d4139962f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:32 GMT
ADD file:90344130400909b0ad12bb54d439b0e4868fc5863f538f676e6fdfeaeb4dad51 in / 
# Tue, 23 Aug 2022 01:52:33 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:48:22 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:48:22 GMT
ENV EMQX_VERSION=4.4.4
# Tue, 23 Aug 2022 02:48:23 GMT
ENV OTP=otp24.1.5-3
# Tue, 23 Aug 2022 02:48:28 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 23 Aug 2022 02:48:30 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 23 Aug 2022 02:48:30 GMT
WORKDIR /opt/emqx
# Tue, 23 Aug 2022 02:48:31 GMT
USER emqx
# Tue, 23 Aug 2022 02:48:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 23 Aug 2022 02:48:33 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 23 Aug 2022 02:48:35 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 23 Aug 2022 02:48:35 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:48:36 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:5b142346550416c75ea412d21741de5eaf3e76857affc12fab789277f81f53b3`  
		Last Modified: Tue, 23 Aug 2022 01:58:00 GMT  
		Size: 30.1 MB (30063788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76875b2a2774be642d6a500995cffb336dc0b7fce71c6554e4415cc6df01a4b2`  
		Last Modified: Tue, 23 Aug 2022 02:49:14 GMT  
		Size: 2.4 MB (2353690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bd6d30cd6371bb62afaacfb03fb3dd2ea33d16d25087af221e21d238febfc9`  
		Last Modified: Tue, 23 Aug 2022 02:49:18 GMT  
		Size: 38.8 MB (38806760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cf00ca63decf520e5ab938da78a25d9ad2816babd18a8e5594cc877a2d4791`  
		Last Modified: Tue, 23 Aug 2022 02:49:18 GMT  
		Size: 38.8 MB (38807691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c5c2a2bac240c35e3c2ef46b56552e483b7324b2c74c09c78bc86d2a7e7b0b`  
		Last Modified: Tue, 23 Aug 2022 02:49:13 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:latest`

```console
$ docker pull emqx@sha256:04ecf66e6c70fcbd75b76fb586283913c76f5818ce1221aee59368dc83d51338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:fb2257b976208201d7e33177427e0be10a94168dfc39bb257de940e3e339317c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.8 MB (124836587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f34e0da055730b616341cff9eecc144f26b5d0df9a5c84e0d83c6957bed4ed`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 13 Sep 2022 00:56:29 GMT
ADD file:5bd53bff884e470b3c12425132975ab9c6f99002c62c43bca1ff5cde9d863b92 in / 
# Tue, 13 Sep 2022 00:56:29 GMT
CMD ["bash"]
# Tue, 13 Sep 2022 03:59:23 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Sep 2022 03:59:23 GMT
ENV EMQX_VERSION=4.4.4
# Tue, 13 Sep 2022 03:59:23 GMT
ENV OTP=otp24.1.5-3
# Tue, 13 Sep 2022 03:59:27 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 13 Sep 2022 03:59:33 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 13 Sep 2022 03:59:33 GMT
WORKDIR /opt/emqx
# Tue, 13 Sep 2022 03:59:33 GMT
USER emqx
# Tue, 13 Sep 2022 03:59:33 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Sep 2022 03:59:33 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 13 Sep 2022 03:59:34 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 13 Sep 2022 03:59:34 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Sep 2022 03:59:34 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:31b3f1ad4ce1f369084d0f959813c51df0ca17d9877d5ee88c2db6ff88341430`  
		Last Modified: Tue, 13 Sep 2022 01:00:29 GMT  
		Size: 31.4 MB (31404121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1718cfc9ab1a66a45b214f22aad7acd47b0ee5360a06535c5c7108a46fbee1`  
		Last Modified: Tue, 13 Sep 2022 04:00:04 GMT  
		Size: 2.6 MB (2569503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9004193e42b45379e1def33644c4824ac57de3e65880a3316bb03d535de9fb`  
		Last Modified: Tue, 13 Sep 2022 04:00:08 GMT  
		Size: 45.4 MB (45424530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e1552a0b575c61fc3b386fa2dccef591129271e5914cec5e588908f4e26418`  
		Last Modified: Tue, 13 Sep 2022 04:00:08 GMT  
		Size: 45.4 MB (45437326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9dd750521fd7780e66dac97a3c8dc8ff81efc749ccf491617bdde85021e3dee`  
		Last Modified: Tue, 13 Sep 2022 04:00:03 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:b9b2be320c2a2469aa9c8de01a47db24c4b11d7d8980a59e39259a4976cfc49c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.0 MB (110033038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcabc472c20703152f5e87f687372023f66139abb5c82b7bdecb205d4139962f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 23 Aug 2022 01:52:32 GMT
ADD file:90344130400909b0ad12bb54d439b0e4868fc5863f538f676e6fdfeaeb4dad51 in / 
# Tue, 23 Aug 2022 01:52:33 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 02:48:22 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 23 Aug 2022 02:48:22 GMT
ENV EMQX_VERSION=4.4.4
# Tue, 23 Aug 2022 02:48:23 GMT
ENV OTP=otp24.1.5-3
# Tue, 23 Aug 2022 02:48:28 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="74a65d51ab60b044874f98e1dc4022f2932c7d70e68bc13ed5fe43be177ba515"; fi;     if [ ${arch} = "arm64" ]; then sha256="6aed1583bf96b53e6355e7431204fc8b09b89ffbce580f5031a77a542c53c5e8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 23 Aug 2022 02:48:30 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Tue, 23 Aug 2022 02:48:30 GMT
WORKDIR /opt/emqx
# Tue, 23 Aug 2022 02:48:31 GMT
USER emqx
# Tue, 23 Aug 2022 02:48:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 23 Aug 2022 02:48:33 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 23 Aug 2022 02:48:35 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 23 Aug 2022 02:48:35 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 23 Aug 2022 02:48:36 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:5b142346550416c75ea412d21741de5eaf3e76857affc12fab789277f81f53b3`  
		Last Modified: Tue, 23 Aug 2022 01:58:00 GMT  
		Size: 30.1 MB (30063788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76875b2a2774be642d6a500995cffb336dc0b7fce71c6554e4415cc6df01a4b2`  
		Last Modified: Tue, 23 Aug 2022 02:49:14 GMT  
		Size: 2.4 MB (2353690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bd6d30cd6371bb62afaacfb03fb3dd2ea33d16d25087af221e21d238febfc9`  
		Last Modified: Tue, 23 Aug 2022 02:49:18 GMT  
		Size: 38.8 MB (38806760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cf00ca63decf520e5ab938da78a25d9ad2816babd18a8e5594cc877a2d4791`  
		Last Modified: Tue, 23 Aug 2022 02:49:18 GMT  
		Size: 38.8 MB (38807691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c5c2a2bac240c35e3c2ef46b56552e483b7324b2c74c09c78bc86d2a7e7b0b`  
		Last Modified: Tue, 23 Aug 2022 02:49:13 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
