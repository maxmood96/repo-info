<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:5`](#emqx5)
-	[`emqx:5.1`](#emqx51)
-	[`emqx:5.1.6`](#emqx516)
-	[`emqx:5.2`](#emqx52)
-	[`emqx:5.2.1`](#emqx521)
-	[`emqx:5.3`](#emqx53)
-	[`emqx:5.3.2`](#emqx532)
-	[`emqx:5.4`](#emqx54)
-	[`emqx:5.4.1`](#emqx541)
-	[`emqx:5.5`](#emqx55)
-	[`emqx:5.5.1`](#emqx551)
-	[`emqx:5.6`](#emqx56)
-	[`emqx:5.6.1`](#emqx561)
-	[`emqx:latest`](#emqxlatest)

## `emqx:5`

```console
$ docker pull emqx@sha256:0d86fd2673cd6f6f7152e5a1f4f478dc816de1617bc23932ad91afb4c11738e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:45f51914bc6b28d0e23bea555679bd070a23277cd121e69f5ae5a2027655b417
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124206533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a6a473df1836e785190f4778273218fb396bf89c01b14f22523409d3126f2e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:28:20 GMT
ENV EMQX_VERSION=5.6.1
# Wed, 24 Apr 2024 04:28:20 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Wed, 24 Apr 2024 04:28:20 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Wed, 24 Apr 2024 04:28:20 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 04:28:36 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 24 Apr 2024 04:28:36 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 04:28:36 GMT
USER emqx
# Wed, 24 Apr 2024 04:28:37 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 04:28:37 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 04:28:37 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Wed, 24 Apr 2024 04:28:37 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 04:28:37 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb78d9b1d11aea4e48b11cf101ca79b8d05e2a6afeb220013793b7fc5bcfc7f`  
		Last Modified: Wed, 24 Apr 2024 04:30:21 GMT  
		Size: 95.1 MB (95055018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c721fad0602a66b21da5d838df97aa2132862eb7528e29342e2106e67029f6`  
		Last Modified: Wed, 24 Apr 2024 04:30:11 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:7c61793428a24df2865e8ef300c1321af59fa67ac8bce37e908e7e1c4e870e67
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120796711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb34410b1481c71541c6739753b550dc926ad71169013dcbc7f515ba790dc3ae`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 09:19:56 GMT
ENV EMQX_VERSION=5.6.1
# Wed, 24 Apr 2024 09:19:56 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Wed, 24 Apr 2024 09:19:56 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Wed, 24 Apr 2024 09:19:56 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 09:20:09 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 24 Apr 2024 09:20:10 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 09:20:11 GMT
USER emqx
# Wed, 24 Apr 2024 09:20:11 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 09:20:11 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 09:20:11 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Wed, 24 Apr 2024 09:20:11 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 09:20:11 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:256ee584cef5c909eb23cdc3bfc06fa8be5a0f8dca36c372dc6dbe5123b63a16`  
		Last Modified: Wed, 24 Apr 2024 09:21:43 GMT  
		Size: 91.6 MB (91615739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b392737eb6e10b4328f6ede370a3bc22425b050f2195e87c75995ae17348488`  
		Last Modified: Wed, 24 Apr 2024 09:21:35 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.1`

```console
$ docker pull emqx@sha256:83eb5327c302ff335802ffd862dc2c514c6bdde6d6cae08133a8312f6c40075b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.1` - linux; amd64

```console
$ docker pull emqx@sha256:003b4648e0d1b1e2c5aa897995391007eb54ac8b2ab977a4ef4ee3f2e5367c44
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102410084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f8e5e57fa4348fa42babe5411aff4e1cbee418d7811873667652a380bb98003`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:26:46 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:26:46 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 24 Apr 2024 04:26:47 GMT
ENV EMQX_VERSION=5.1.6
# Wed, 24 Apr 2024 04:26:47 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Wed, 24 Apr 2024 04:26:47 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Wed, 24 Apr 2024 04:26:47 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 04:26:54 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Wed, 24 Apr 2024 04:26:54 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 04:26:54 GMT
USER emqx
# Wed, 24 Apr 2024 04:26:55 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 04:26:55 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 04:26:55 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 24 Apr 2024 04:26:55 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 04:26:55 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45976b5fe7010690f90ffafb4e0238f46242f6d04abbb8b9e1f0af5b1d0a1c11`  
		Last Modified: Wed, 24 Apr 2024 04:28:51 GMT  
		Size: 3.0 MB (2989557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c0a3ba50ab1ac8902be9b5a546bf7c63f86aa47f495593cca165a263e1ab62`  
		Last Modified: Wed, 24 Apr 2024 04:28:50 GMT  
		Size: 4.1 KB (4110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692af07376113d51e6d2184cede678855da97260624d5f88a3ba32c93e0283ae`  
		Last Modified: Wed, 24 Apr 2024 04:28:58 GMT  
		Size: 68.0 MB (67981252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592be638672b7afe71cfa5a79337f2c460c4f25a53eb838507bf667daaa5dd1b`  
		Last Modified: Wed, 24 Apr 2024 04:28:51 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:56c16dc6b7648f650a37dce591c577ae21a0bfc5974014db3f139710831a8aa6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92723028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc74f997f1022d4b2705a5a42f7fe87950c02fcfbbe16e0871eab58580b3839`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 09:18:42 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 09:18:42 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 24 Apr 2024 09:18:42 GMT
ENV EMQX_VERSION=5.1.6
# Wed, 24 Apr 2024 09:18:42 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Wed, 24 Apr 2024 09:18:42 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Wed, 24 Apr 2024 09:18:42 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 09:18:48 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Wed, 24 Apr 2024 09:18:49 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 09:18:49 GMT
USER emqx
# Wed, 24 Apr 2024 09:18:49 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 09:18:49 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 09:18:49 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 24 Apr 2024 09:18:49 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 09:18:49 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110d03275061b16a7227fb0df8c7fff2657946609fbf03ccfe3cf5dd933d7599`  
		Last Modified: Wed, 24 Apr 2024 09:20:27 GMT  
		Size: 3.0 MB (3006052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8ec3c2447d244b82d97065986337e973748f76ab58f353c7c2772f9951e03b`  
		Last Modified: Wed, 24 Apr 2024 09:20:26 GMT  
		Size: 4.1 KB (4114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b49f9ff381cebbfdbc2bb7a9e1d735f4e5041f8325dab12a686b39a32e3719`  
		Last Modified: Wed, 24 Apr 2024 09:20:31 GMT  
		Size: 59.6 MB (59624621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c802a16146ad1f9adcb8e5301b12ff5e53c50aef4530412560afa6c72b363d2`  
		Last Modified: Wed, 24 Apr 2024 09:20:26 GMT  
		Size: 905.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.1.6`

```console
$ docker pull emqx@sha256:83eb5327c302ff335802ffd862dc2c514c6bdde6d6cae08133a8312f6c40075b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.1.6` - linux; amd64

```console
$ docker pull emqx@sha256:003b4648e0d1b1e2c5aa897995391007eb54ac8b2ab977a4ef4ee3f2e5367c44
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102410084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f8e5e57fa4348fa42babe5411aff4e1cbee418d7811873667652a380bb98003`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:26:46 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:26:46 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 24 Apr 2024 04:26:47 GMT
ENV EMQX_VERSION=5.1.6
# Wed, 24 Apr 2024 04:26:47 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Wed, 24 Apr 2024 04:26:47 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Wed, 24 Apr 2024 04:26:47 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 04:26:54 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Wed, 24 Apr 2024 04:26:54 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 04:26:54 GMT
USER emqx
# Wed, 24 Apr 2024 04:26:55 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 04:26:55 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 04:26:55 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 24 Apr 2024 04:26:55 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 04:26:55 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45976b5fe7010690f90ffafb4e0238f46242f6d04abbb8b9e1f0af5b1d0a1c11`  
		Last Modified: Wed, 24 Apr 2024 04:28:51 GMT  
		Size: 3.0 MB (2989557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c0a3ba50ab1ac8902be9b5a546bf7c63f86aa47f495593cca165a263e1ab62`  
		Last Modified: Wed, 24 Apr 2024 04:28:50 GMT  
		Size: 4.1 KB (4110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692af07376113d51e6d2184cede678855da97260624d5f88a3ba32c93e0283ae`  
		Last Modified: Wed, 24 Apr 2024 04:28:58 GMT  
		Size: 68.0 MB (67981252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592be638672b7afe71cfa5a79337f2c460c4f25a53eb838507bf667daaa5dd1b`  
		Last Modified: Wed, 24 Apr 2024 04:28:51 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.1.6` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:56c16dc6b7648f650a37dce591c577ae21a0bfc5974014db3f139710831a8aa6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92723028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc74f997f1022d4b2705a5a42f7fe87950c02fcfbbe16e0871eab58580b3839`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 09:18:42 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 09:18:42 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 24 Apr 2024 09:18:42 GMT
ENV EMQX_VERSION=5.1.6
# Wed, 24 Apr 2024 09:18:42 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Wed, 24 Apr 2024 09:18:42 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Wed, 24 Apr 2024 09:18:42 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 09:18:48 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Wed, 24 Apr 2024 09:18:49 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 09:18:49 GMT
USER emqx
# Wed, 24 Apr 2024 09:18:49 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 09:18:49 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 09:18:49 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 24 Apr 2024 09:18:49 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 09:18:49 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110d03275061b16a7227fb0df8c7fff2657946609fbf03ccfe3cf5dd933d7599`  
		Last Modified: Wed, 24 Apr 2024 09:20:27 GMT  
		Size: 3.0 MB (3006052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8ec3c2447d244b82d97065986337e973748f76ab58f353c7c2772f9951e03b`  
		Last Modified: Wed, 24 Apr 2024 09:20:26 GMT  
		Size: 4.1 KB (4114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b49f9ff381cebbfdbc2bb7a9e1d735f4e5041f8325dab12a686b39a32e3719`  
		Last Modified: Wed, 24 Apr 2024 09:20:31 GMT  
		Size: 59.6 MB (59624621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c802a16146ad1f9adcb8e5301b12ff5e53c50aef4530412560afa6c72b363d2`  
		Last Modified: Wed, 24 Apr 2024 09:20:26 GMT  
		Size: 905.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.2`

```console
$ docker pull emqx@sha256:a15aabc1472a30874252b1f66a02da731b8aaa61223b277e0249712b8196f652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.2` - linux; amd64

```console
$ docker pull emqx@sha256:995d3751fd4368091c838b98b180715eaadf94a6c718c9a5f41939e870bbb87c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101181640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5283b60dedc3b9998377c9c1c31ac9d342dac8d9a21d443a28a4af747144287`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:27:06 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:27:06 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 24 Apr 2024 04:27:06 GMT
ENV EMQX_VERSION=5.2.1
# Wed, 24 Apr 2024 04:27:06 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Wed, 24 Apr 2024 04:27:07 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Wed, 24 Apr 2024 04:27:07 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 04:27:17 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 04:27:18 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 04:27:18 GMT
USER emqx
# Wed, 24 Apr 2024 04:27:18 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 04:27:18 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 04:27:18 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 24 Apr 2024 04:27:18 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 04:27:18 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75790383ce9e9813e8d074e7dbb333b898e94c8cb92522050935fb77fa0f90aa`  
		Last Modified: Wed, 24 Apr 2024 04:29:07 GMT  
		Size: 1.6 MB (1631415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28049f7bce9a304fcdb3ebc51a65cfb6f3df3f829da9d33d8c94c4a27cb89ef9`  
		Last Modified: Wed, 24 Apr 2024 04:29:07 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dfcf27c5f29fcb7a5137bf1fa47b6dae66f05e1f0037d2a48dbfba8a7843220`  
		Last Modified: Wed, 24 Apr 2024 04:29:14 GMT  
		Size: 68.1 MB (68110948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30057c45291b51de1b91c0f716d2a5766ebc4403946282bec750ee6ff26f125`  
		Last Modified: Wed, 24 Apr 2024 04:29:07 GMT  
		Size: 905.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:f33260043de63c2a90305f83c74e02862457f8fa64623927bd3cecb5338618dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91489915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8fe7b446a7738259689762332907ced80695e7dd51258d1544da82b87044dc2`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 09:18:56 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 09:18:57 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 24 Apr 2024 09:18:57 GMT
ENV EMQX_VERSION=5.2.1
# Wed, 24 Apr 2024 09:18:57 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Wed, 24 Apr 2024 09:18:57 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Wed, 24 Apr 2024 09:18:57 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 09:19:06 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 09:19:06 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 09:19:06 GMT
USER emqx
# Wed, 24 Apr 2024 09:19:06 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 09:19:06 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 09:19:06 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 24 Apr 2024 09:19:06 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 09:19:07 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c91c80d0c4cb2508a7f2361c7b69f66ec60ca2bfb6fd9b8e7451e0712b3391b`  
		Last Modified: Wed, 24 Apr 2024 09:20:39 GMT  
		Size: 1.6 MB (1645777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8961451ec8d3d4a2f013ce6a7dda43dff7b585d1d753073eeaefe3d8b553fe0`  
		Last Modified: Wed, 24 Apr 2024 09:20:39 GMT  
		Size: 4.1 KB (4116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb17c93bd0170932607aaa6395208233306052538128d577b26c66230d8b138`  
		Last Modified: Wed, 24 Apr 2024 09:20:44 GMT  
		Size: 59.8 MB (59751781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6338d2cf4a8ae23593af26769cc6285e6e3866baa6aff84969295cd5b884fc`  
		Last Modified: Wed, 24 Apr 2024 09:20:39 GMT  
		Size: 905.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.2.1`

```console
$ docker pull emqx@sha256:a15aabc1472a30874252b1f66a02da731b8aaa61223b277e0249712b8196f652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.2.1` - linux; amd64

```console
$ docker pull emqx@sha256:995d3751fd4368091c838b98b180715eaadf94a6c718c9a5f41939e870bbb87c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101181640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5283b60dedc3b9998377c9c1c31ac9d342dac8d9a21d443a28a4af747144287`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:27:06 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:27:06 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 24 Apr 2024 04:27:06 GMT
ENV EMQX_VERSION=5.2.1
# Wed, 24 Apr 2024 04:27:06 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Wed, 24 Apr 2024 04:27:07 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Wed, 24 Apr 2024 04:27:07 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 04:27:17 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 04:27:18 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 04:27:18 GMT
USER emqx
# Wed, 24 Apr 2024 04:27:18 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 04:27:18 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 04:27:18 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 24 Apr 2024 04:27:18 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 04:27:18 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75790383ce9e9813e8d074e7dbb333b898e94c8cb92522050935fb77fa0f90aa`  
		Last Modified: Wed, 24 Apr 2024 04:29:07 GMT  
		Size: 1.6 MB (1631415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28049f7bce9a304fcdb3ebc51a65cfb6f3df3f829da9d33d8c94c4a27cb89ef9`  
		Last Modified: Wed, 24 Apr 2024 04:29:07 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dfcf27c5f29fcb7a5137bf1fa47b6dae66f05e1f0037d2a48dbfba8a7843220`  
		Last Modified: Wed, 24 Apr 2024 04:29:14 GMT  
		Size: 68.1 MB (68110948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30057c45291b51de1b91c0f716d2a5766ebc4403946282bec750ee6ff26f125`  
		Last Modified: Wed, 24 Apr 2024 04:29:07 GMT  
		Size: 905.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.2.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:f33260043de63c2a90305f83c74e02862457f8fa64623927bd3cecb5338618dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91489915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8fe7b446a7738259689762332907ced80695e7dd51258d1544da82b87044dc2`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 09:18:56 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 09:18:57 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 24 Apr 2024 09:18:57 GMT
ENV EMQX_VERSION=5.2.1
# Wed, 24 Apr 2024 09:18:57 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Wed, 24 Apr 2024 09:18:57 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Wed, 24 Apr 2024 09:18:57 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 09:19:06 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 09:19:06 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 09:19:06 GMT
USER emqx
# Wed, 24 Apr 2024 09:19:06 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 09:19:06 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 09:19:06 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 24 Apr 2024 09:19:06 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 09:19:07 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c91c80d0c4cb2508a7f2361c7b69f66ec60ca2bfb6fd9b8e7451e0712b3391b`  
		Last Modified: Wed, 24 Apr 2024 09:20:39 GMT  
		Size: 1.6 MB (1645777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8961451ec8d3d4a2f013ce6a7dda43dff7b585d1d753073eeaefe3d8b553fe0`  
		Last Modified: Wed, 24 Apr 2024 09:20:39 GMT  
		Size: 4.1 KB (4116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb17c93bd0170932607aaa6395208233306052538128d577b26c66230d8b138`  
		Last Modified: Wed, 24 Apr 2024 09:20:44 GMT  
		Size: 59.8 MB (59751781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6338d2cf4a8ae23593af26769cc6285e6e3866baa6aff84969295cd5b884fc`  
		Last Modified: Wed, 24 Apr 2024 09:20:39 GMT  
		Size: 905.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.3`

```console
$ docker pull emqx@sha256:6ede77b076b8d269a07cb23aa32f13dd3106c7cc8191ff164ef9e1b22253262a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.3` - linux; amd64

```console
$ docker pull emqx@sha256:f245db650f41c1aa7704dce0b2ba8508e71fe733f89633319d756ddea7eda48d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101797010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ce8bd3480b902853aeb4d7201881ee8a275212d2c4543835d2b65531da37b1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:27:21 GMT
ENV EMQX_VERSION=5.3.2
# Wed, 24 Apr 2024 04:27:21 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Wed, 24 Apr 2024 04:27:22 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Wed, 24 Apr 2024 04:27:22 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 04:27:35 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:27:35 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 04:27:35 GMT
USER emqx
# Wed, 24 Apr 2024 04:27:35 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 04:27:36 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 04:27:36 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 24 Apr 2024 04:27:36 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 04:27:36 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d73b737ffc0a772c1834b3343f18e8c065b4f1cfc3ab9dac0dd4e063afc552`  
		Last Modified: Wed, 24 Apr 2024 04:29:29 GMT  
		Size: 70.4 MB (70361843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9b106549774436fdf9f9cc7adbfeb8a409b98aabf141b2e244355a78b88d9f`  
		Last Modified: Wed, 24 Apr 2024 04:29:22 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.3` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:f25d01f58537dc391212785abad909c22a2b0e6691c660b3f478117c87d70991
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92103838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:863590a4a931493513266cd0c3e9a7dc970065dfada9a6c1b9c04a19ff329e08`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 09:19:09 GMT
ENV EMQX_VERSION=5.3.2
# Wed, 24 Apr 2024 09:19:09 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Wed, 24 Apr 2024 09:19:09 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Wed, 24 Apr 2024 09:19:09 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 09:19:19 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 09:19:20 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 09:19:20 GMT
USER emqx
# Wed, 24 Apr 2024 09:19:20 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 09:19:20 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 09:19:20 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 24 Apr 2024 09:19:20 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 09:19:20 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66fbc28a922ff6671a283b173c91f9e65ce4edd882c5af131f780e2c50569ac0`  
		Last Modified: Wed, 24 Apr 2024 09:20:57 GMT  
		Size: 62.0 MB (62015599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a27003e125d04c5d124c5e10fde174a70f1740b22df27db5d1151ebaaeeaad`  
		Last Modified: Wed, 24 Apr 2024 09:20:51 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.3.2`

```console
$ docker pull emqx@sha256:6ede77b076b8d269a07cb23aa32f13dd3106c7cc8191ff164ef9e1b22253262a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.3.2` - linux; amd64

```console
$ docker pull emqx@sha256:f245db650f41c1aa7704dce0b2ba8508e71fe733f89633319d756ddea7eda48d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101797010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ce8bd3480b902853aeb4d7201881ee8a275212d2c4543835d2b65531da37b1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:27:21 GMT
ENV EMQX_VERSION=5.3.2
# Wed, 24 Apr 2024 04:27:21 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Wed, 24 Apr 2024 04:27:22 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Wed, 24 Apr 2024 04:27:22 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 04:27:35 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:27:35 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 04:27:35 GMT
USER emqx
# Wed, 24 Apr 2024 04:27:35 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 04:27:36 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 04:27:36 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 24 Apr 2024 04:27:36 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 04:27:36 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d73b737ffc0a772c1834b3343f18e8c065b4f1cfc3ab9dac0dd4e063afc552`  
		Last Modified: Wed, 24 Apr 2024 04:29:29 GMT  
		Size: 70.4 MB (70361843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9b106549774436fdf9f9cc7adbfeb8a409b98aabf141b2e244355a78b88d9f`  
		Last Modified: Wed, 24 Apr 2024 04:29:22 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.3.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:f25d01f58537dc391212785abad909c22a2b0e6691c660b3f478117c87d70991
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92103838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:863590a4a931493513266cd0c3e9a7dc970065dfada9a6c1b9c04a19ff329e08`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 09:19:09 GMT
ENV EMQX_VERSION=5.3.2
# Wed, 24 Apr 2024 09:19:09 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Wed, 24 Apr 2024 09:19:09 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Wed, 24 Apr 2024 09:19:09 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 09:19:19 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 09:19:20 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 09:19:20 GMT
USER emqx
# Wed, 24 Apr 2024 09:19:20 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 09:19:20 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 09:19:20 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 24 Apr 2024 09:19:20 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 09:19:20 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66fbc28a922ff6671a283b173c91f9e65ce4edd882c5af131f780e2c50569ac0`  
		Last Modified: Wed, 24 Apr 2024 09:20:57 GMT  
		Size: 62.0 MB (62015599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a27003e125d04c5d124c5e10fde174a70f1740b22df27db5d1151ebaaeeaad`  
		Last Modified: Wed, 24 Apr 2024 09:20:51 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.4`

```console
$ docker pull emqx@sha256:6c920af374f987393a404ea6a73bf4ea98061fa8bf0811bac5d9e1254f6673e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.4` - linux; amd64

```console
$ docker pull emqx@sha256:744a46964365cfaf1d1e54aa8c1d422ff63d8ee38518b37867ff2805ac8b225d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118711283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a1c27c576ef23e02a7cd1f3a0f7ef133c13de78f3deb8454f4edf9a8d43d555`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:27:39 GMT
ENV EMQX_VERSION=5.4.1
# Wed, 24 Apr 2024 04:27:39 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Wed, 24 Apr 2024 04:27:39 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Wed, 24 Apr 2024 04:27:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 04:27:53 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:27:54 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 04:27:54 GMT
USER emqx
# Wed, 24 Apr 2024 04:27:54 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 04:27:54 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 04:27:54 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 24 Apr 2024 04:27:54 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 04:27:54 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29bf5b439acfbd6136715e0bf5598af603b7e76bc5eedf4c8294a470adfbaed0`  
		Last Modified: Wed, 24 Apr 2024 04:29:46 GMT  
		Size: 87.3 MB (87276116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45852421f49784c3e3d49bd5db714deb4f6e57cecb5efb9852554184c7d01f52`  
		Last Modified: Wed, 24 Apr 2024 04:29:37 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:57fcf5f858dcec5c6fd76cf0223d85f06985e3078efa57c385e4667d346605f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108499451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526f3d599bc091a3e3a3c76b7d6e8cf75746f486dcb4659a804a60bd5ae6293c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 09:19:23 GMT
ENV EMQX_VERSION=5.4.1
# Wed, 24 Apr 2024 09:19:23 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Wed, 24 Apr 2024 09:19:23 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Wed, 24 Apr 2024 09:19:23 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 09:19:34 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 09:19:35 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 09:19:35 GMT
USER emqx
# Wed, 24 Apr 2024 09:19:35 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 09:19:35 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 09:19:35 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 24 Apr 2024 09:19:35 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 09:19:35 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6899d03ca49513a0513896d602508fef5229714ec37371ac243d5d2b3ce20874`  
		Last Modified: Wed, 24 Apr 2024 09:21:12 GMT  
		Size: 78.4 MB (78411211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2790d4a5e807edd6efc06e75fbdccc938ac83c46b8a16f3d300fddb05565497f`  
		Last Modified: Wed, 24 Apr 2024 09:21:05 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.4.1`

```console
$ docker pull emqx@sha256:6c920af374f987393a404ea6a73bf4ea98061fa8bf0811bac5d9e1254f6673e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.4.1` - linux; amd64

```console
$ docker pull emqx@sha256:744a46964365cfaf1d1e54aa8c1d422ff63d8ee38518b37867ff2805ac8b225d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118711283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a1c27c576ef23e02a7cd1f3a0f7ef133c13de78f3deb8454f4edf9a8d43d555`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:27:39 GMT
ENV EMQX_VERSION=5.4.1
# Wed, 24 Apr 2024 04:27:39 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Wed, 24 Apr 2024 04:27:39 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Wed, 24 Apr 2024 04:27:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 04:27:53 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:27:54 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 04:27:54 GMT
USER emqx
# Wed, 24 Apr 2024 04:27:54 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 04:27:54 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 04:27:54 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 24 Apr 2024 04:27:54 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 04:27:54 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29bf5b439acfbd6136715e0bf5598af603b7e76bc5eedf4c8294a470adfbaed0`  
		Last Modified: Wed, 24 Apr 2024 04:29:46 GMT  
		Size: 87.3 MB (87276116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45852421f49784c3e3d49bd5db714deb4f6e57cecb5efb9852554184c7d01f52`  
		Last Modified: Wed, 24 Apr 2024 04:29:37 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.4.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:57fcf5f858dcec5c6fd76cf0223d85f06985e3078efa57c385e4667d346605f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108499451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526f3d599bc091a3e3a3c76b7d6e8cf75746f486dcb4659a804a60bd5ae6293c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 09:19:23 GMT
ENV EMQX_VERSION=5.4.1
# Wed, 24 Apr 2024 09:19:23 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Wed, 24 Apr 2024 09:19:23 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Wed, 24 Apr 2024 09:19:23 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 09:19:34 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 09:19:35 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 09:19:35 GMT
USER emqx
# Wed, 24 Apr 2024 09:19:35 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 09:19:35 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 09:19:35 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 24 Apr 2024 09:19:35 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 09:19:35 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6899d03ca49513a0513896d602508fef5229714ec37371ac243d5d2b3ce20874`  
		Last Modified: Wed, 24 Apr 2024 09:21:12 GMT  
		Size: 78.4 MB (78411211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2790d4a5e807edd6efc06e75fbdccc938ac83c46b8a16f3d300fddb05565497f`  
		Last Modified: Wed, 24 Apr 2024 09:21:05 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.5`

```console
$ docker pull emqx@sha256:e8873edb26b0d1de5a41be2b370c10500547a64461791582858bfcd9e6f31ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.5` - linux; amd64

```console
$ docker pull emqx@sha256:4414026061ac91ba5e7530cb6cbd59ff169ea521f67496893fa5a70884b39ae7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121276344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a7d2abf39e0bd7b5f2a27acb040e8ae63c8fa18a472b543cc253bf455c4f76`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:27:59 GMT
ENV EMQX_VERSION=5.5.1
# Wed, 24 Apr 2024 04:27:59 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Wed, 24 Apr 2024 04:27:59 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Wed, 24 Apr 2024 04:28:00 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 04:28:14 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 24 Apr 2024 04:28:15 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 04:28:15 GMT
USER emqx
# Wed, 24 Apr 2024 04:28:15 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 04:28:15 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 04:28:15 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Wed, 24 Apr 2024 04:28:15 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 04:28:15 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1473ab5946a2647810af01e92b9b740a67d435fbb6d0b22e7eaf0cc310a5f96e`  
		Last Modified: Wed, 24 Apr 2024 04:30:03 GMT  
		Size: 89.8 MB (89841047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54901cafd7674d3aaf7f5e367ab76ff45b764e0b68ae821126a6c417a34efe5`  
		Last Modified: Wed, 24 Apr 2024 04:29:53 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:a4b25e3fb9a967ddf0d2d9f858eaf344862a79bdf7ac95bb2f093bc1d4a590eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116797605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b6fac7f46d4a9d2af85a1faaaadc2462ee76f9a147187a4f5813910ff878fe8`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 09:19:39 GMT
ENV EMQX_VERSION=5.5.1
# Wed, 24 Apr 2024 09:19:39 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Wed, 24 Apr 2024 09:19:40 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Wed, 24 Apr 2024 09:19:40 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 09:19:51 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 24 Apr 2024 09:19:52 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 09:19:52 GMT
USER emqx
# Wed, 24 Apr 2024 09:19:52 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 09:19:52 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 09:19:52 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Wed, 24 Apr 2024 09:19:52 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 09:19:52 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5db917c8a2c30b85e1a8aea0eb7200061d68fde5bc3dcd9de1949002271cc39`  
		Last Modified: Wed, 24 Apr 2024 09:21:27 GMT  
		Size: 86.7 MB (86709233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f4061854dbff91c9b9a9c53cdcf7a7d1499ec24536cbd83dd828d1fcb53fa2b`  
		Last Modified: Wed, 24 Apr 2024 09:21:19 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.5.1`

```console
$ docker pull emqx@sha256:e8873edb26b0d1de5a41be2b370c10500547a64461791582858bfcd9e6f31ca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.5.1` - linux; amd64

```console
$ docker pull emqx@sha256:4414026061ac91ba5e7530cb6cbd59ff169ea521f67496893fa5a70884b39ae7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121276344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a7d2abf39e0bd7b5f2a27acb040e8ae63c8fa18a472b543cc253bf455c4f76`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:27:59 GMT
ENV EMQX_VERSION=5.5.1
# Wed, 24 Apr 2024 04:27:59 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Wed, 24 Apr 2024 04:27:59 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Wed, 24 Apr 2024 04:28:00 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 04:28:14 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 24 Apr 2024 04:28:15 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 04:28:15 GMT
USER emqx
# Wed, 24 Apr 2024 04:28:15 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 04:28:15 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 04:28:15 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Wed, 24 Apr 2024 04:28:15 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 04:28:15 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1473ab5946a2647810af01e92b9b740a67d435fbb6d0b22e7eaf0cc310a5f96e`  
		Last Modified: Wed, 24 Apr 2024 04:30:03 GMT  
		Size: 89.8 MB (89841047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54901cafd7674d3aaf7f5e367ab76ff45b764e0b68ae821126a6c417a34efe5`  
		Last Modified: Wed, 24 Apr 2024 04:29:53 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.5.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:a4b25e3fb9a967ddf0d2d9f858eaf344862a79bdf7ac95bb2f093bc1d4a590eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116797605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b6fac7f46d4a9d2af85a1faaaadc2462ee76f9a147187a4f5813910ff878fe8`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 09:19:39 GMT
ENV EMQX_VERSION=5.5.1
# Wed, 24 Apr 2024 09:19:39 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Wed, 24 Apr 2024 09:19:40 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Wed, 24 Apr 2024 09:19:40 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 09:19:51 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 24 Apr 2024 09:19:52 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 09:19:52 GMT
USER emqx
# Wed, 24 Apr 2024 09:19:52 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 09:19:52 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 09:19:52 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Wed, 24 Apr 2024 09:19:52 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 09:19:52 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5db917c8a2c30b85e1a8aea0eb7200061d68fde5bc3dcd9de1949002271cc39`  
		Last Modified: Wed, 24 Apr 2024 09:21:27 GMT  
		Size: 86.7 MB (86709233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f4061854dbff91c9b9a9c53cdcf7a7d1499ec24536cbd83dd828d1fcb53fa2b`  
		Last Modified: Wed, 24 Apr 2024 09:21:19 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.6`

```console
$ docker pull emqx@sha256:0d86fd2673cd6f6f7152e5a1f4f478dc816de1617bc23932ad91afb4c11738e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.6` - linux; amd64

```console
$ docker pull emqx@sha256:45f51914bc6b28d0e23bea555679bd070a23277cd121e69f5ae5a2027655b417
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124206533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a6a473df1836e785190f4778273218fb396bf89c01b14f22523409d3126f2e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:28:20 GMT
ENV EMQX_VERSION=5.6.1
# Wed, 24 Apr 2024 04:28:20 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Wed, 24 Apr 2024 04:28:20 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Wed, 24 Apr 2024 04:28:20 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 04:28:36 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 24 Apr 2024 04:28:36 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 04:28:36 GMT
USER emqx
# Wed, 24 Apr 2024 04:28:37 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 04:28:37 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 04:28:37 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Wed, 24 Apr 2024 04:28:37 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 04:28:37 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb78d9b1d11aea4e48b11cf101ca79b8d05e2a6afeb220013793b7fc5bcfc7f`  
		Last Modified: Wed, 24 Apr 2024 04:30:21 GMT  
		Size: 95.1 MB (95055018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c721fad0602a66b21da5d838df97aa2132862eb7528e29342e2106e67029f6`  
		Last Modified: Wed, 24 Apr 2024 04:30:11 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.6` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:7c61793428a24df2865e8ef300c1321af59fa67ac8bce37e908e7e1c4e870e67
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120796711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb34410b1481c71541c6739753b550dc926ad71169013dcbc7f515ba790dc3ae`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 09:19:56 GMT
ENV EMQX_VERSION=5.6.1
# Wed, 24 Apr 2024 09:19:56 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Wed, 24 Apr 2024 09:19:56 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Wed, 24 Apr 2024 09:19:56 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 09:20:09 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 24 Apr 2024 09:20:10 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 09:20:11 GMT
USER emqx
# Wed, 24 Apr 2024 09:20:11 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 09:20:11 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 09:20:11 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Wed, 24 Apr 2024 09:20:11 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 09:20:11 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:256ee584cef5c909eb23cdc3bfc06fa8be5a0f8dca36c372dc6dbe5123b63a16`  
		Last Modified: Wed, 24 Apr 2024 09:21:43 GMT  
		Size: 91.6 MB (91615739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b392737eb6e10b4328f6ede370a3bc22425b050f2195e87c75995ae17348488`  
		Last Modified: Wed, 24 Apr 2024 09:21:35 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.6.1`

```console
$ docker pull emqx@sha256:0d86fd2673cd6f6f7152e5a1f4f478dc816de1617bc23932ad91afb4c11738e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.6.1` - linux; amd64

```console
$ docker pull emqx@sha256:45f51914bc6b28d0e23bea555679bd070a23277cd121e69f5ae5a2027655b417
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124206533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a6a473df1836e785190f4778273218fb396bf89c01b14f22523409d3126f2e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:28:20 GMT
ENV EMQX_VERSION=5.6.1
# Wed, 24 Apr 2024 04:28:20 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Wed, 24 Apr 2024 04:28:20 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Wed, 24 Apr 2024 04:28:20 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 04:28:36 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 24 Apr 2024 04:28:36 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 04:28:36 GMT
USER emqx
# Wed, 24 Apr 2024 04:28:37 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 04:28:37 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 04:28:37 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Wed, 24 Apr 2024 04:28:37 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 04:28:37 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb78d9b1d11aea4e48b11cf101ca79b8d05e2a6afeb220013793b7fc5bcfc7f`  
		Last Modified: Wed, 24 Apr 2024 04:30:21 GMT  
		Size: 95.1 MB (95055018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c721fad0602a66b21da5d838df97aa2132862eb7528e29342e2106e67029f6`  
		Last Modified: Wed, 24 Apr 2024 04:30:11 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.6.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:7c61793428a24df2865e8ef300c1321af59fa67ac8bce37e908e7e1c4e870e67
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120796711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb34410b1481c71541c6739753b550dc926ad71169013dcbc7f515ba790dc3ae`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 09:19:56 GMT
ENV EMQX_VERSION=5.6.1
# Wed, 24 Apr 2024 09:19:56 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Wed, 24 Apr 2024 09:19:56 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Wed, 24 Apr 2024 09:19:56 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 09:20:09 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 24 Apr 2024 09:20:10 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 09:20:11 GMT
USER emqx
# Wed, 24 Apr 2024 09:20:11 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 09:20:11 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 09:20:11 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Wed, 24 Apr 2024 09:20:11 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 09:20:11 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:256ee584cef5c909eb23cdc3bfc06fa8be5a0f8dca36c372dc6dbe5123b63a16`  
		Last Modified: Wed, 24 Apr 2024 09:21:43 GMT  
		Size: 91.6 MB (91615739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b392737eb6e10b4328f6ede370a3bc22425b050f2195e87c75995ae17348488`  
		Last Modified: Wed, 24 Apr 2024 09:21:35 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:latest`

```console
$ docker pull emqx@sha256:0d86fd2673cd6f6f7152e5a1f4f478dc816de1617bc23932ad91afb4c11738e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:45f51914bc6b28d0e23bea555679bd070a23277cd121e69f5ae5a2027655b417
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124206533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a6a473df1836e785190f4778273218fb396bf89c01b14f22523409d3126f2e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:28:20 GMT
ENV EMQX_VERSION=5.6.1
# Wed, 24 Apr 2024 04:28:20 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Wed, 24 Apr 2024 04:28:20 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Wed, 24 Apr 2024 04:28:20 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 04:28:36 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 24 Apr 2024 04:28:36 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 04:28:36 GMT
USER emqx
# Wed, 24 Apr 2024 04:28:37 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 04:28:37 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 04:28:37 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Wed, 24 Apr 2024 04:28:37 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 04:28:37 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb78d9b1d11aea4e48b11cf101ca79b8d05e2a6afeb220013793b7fc5bcfc7f`  
		Last Modified: Wed, 24 Apr 2024 04:30:21 GMT  
		Size: 95.1 MB (95055018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c721fad0602a66b21da5d838df97aa2132862eb7528e29342e2106e67029f6`  
		Last Modified: Wed, 24 Apr 2024 04:30:11 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:7c61793428a24df2865e8ef300c1321af59fa67ac8bce37e908e7e1c4e870e67
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120796711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb34410b1481c71541c6739753b550dc926ad71169013dcbc7f515ba790dc3ae`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 09:19:56 GMT
ENV EMQX_VERSION=5.6.1
# Wed, 24 Apr 2024 09:19:56 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Wed, 24 Apr 2024 09:19:56 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Wed, 24 Apr 2024 09:19:56 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 24 Apr 2024 09:20:09 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Wed, 24 Apr 2024 09:20:10 GMT
WORKDIR /opt/emqx
# Wed, 24 Apr 2024 09:20:11 GMT
USER emqx
# Wed, 24 Apr 2024 09:20:11 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 24 Apr 2024 09:20:11 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 24 Apr 2024 09:20:11 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Wed, 24 Apr 2024 09:20:11 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 24 Apr 2024 09:20:11 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:256ee584cef5c909eb23cdc3bfc06fa8be5a0f8dca36c372dc6dbe5123b63a16`  
		Last Modified: Wed, 24 Apr 2024 09:21:43 GMT  
		Size: 91.6 MB (91615739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b392737eb6e10b4328f6ede370a3bc22425b050f2195e87c75995ae17348488`  
		Last Modified: Wed, 24 Apr 2024 09:21:35 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
