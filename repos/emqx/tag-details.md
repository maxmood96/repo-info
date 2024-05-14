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
$ docker pull emqx@sha256:2c8ba459aa700c553373f697cda1897c4c61ad889500f62f728eaa70786069ab
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
$ docker pull emqx@sha256:8468c03000265baff59f6e0b9672f48f3c6b97390dd5b4cdff617f5c97442f0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120796320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7ef707698df6918c8e04ee8441d77ec406bf81d94cc5c1d276a9180b446008`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:29:23 GMT
ENV EMQX_VERSION=5.6.1
# Tue, 14 May 2024 02:29:23 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Tue, 14 May 2024 02:29:23 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Tue, 14 May 2024 02:29:23 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 14 May 2024 02:29:36 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 14 May 2024 02:29:37 GMT
WORKDIR /opt/emqx
# Tue, 14 May 2024 02:29:37 GMT
USER emqx
# Tue, 14 May 2024 02:29:37 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 14 May 2024 02:29:37 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 14 May 2024 02:29:37 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 14 May 2024 02:29:37 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 14 May 2024 02:29:37 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0462ebe9d5a7da4209ef18c6868756f65c50af18ae6a0ab8b488ee547abd7dc1`  
		Last Modified: Tue, 14 May 2024 02:31:07 GMT  
		Size: 91.6 MB (91615783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa9fd0acdb66a85f8f5effb30d086ed735a003eb6fe434a2d47984fd6aa4c52`  
		Last Modified: Tue, 14 May 2024 02:30:59 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.1`

```console
$ docker pull emqx@sha256:6aeae6e7a0b2852ddbde75b6d8c9468d38ebe8f69ad56a283518358b74d62145
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
$ docker pull emqx@sha256:6d918cbe4d93a26b8277cc81c64cfb3043b54fedeb236f8ccf8c798381e60b6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92722662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565299c2bab277f1a5c99f75717ffd066b3042947f32d493df6bcbe6aa15789c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:28:08 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:28:09 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 14 May 2024 02:28:09 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 14 May 2024 02:28:09 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 14 May 2024 02:28:09 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 14 May 2024 02:28:09 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 14 May 2024 02:28:14 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 14 May 2024 02:28:15 GMT
WORKDIR /opt/emqx
# Tue, 14 May 2024 02:28:15 GMT
USER emqx
# Tue, 14 May 2024 02:28:15 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 14 May 2024 02:28:15 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 14 May 2024 02:28:15 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 14 May 2024 02:28:15 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 14 May 2024 02:28:15 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2335c9ad8fddf7f96c47075cd2601e30075a8a6be73151654fcae1eeb448c917`  
		Last Modified: Tue, 14 May 2024 02:29:51 GMT  
		Size: 3.0 MB (3006068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0ede5b19e6daa66212ba8878c1ed2f180a34e2a36efb70525ab33331ead792`  
		Last Modified: Tue, 14 May 2024 02:29:49 GMT  
		Size: 4.1 KB (4113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b960bb93130c3fa5d765900f22542f1268b7f05e852763d02f924acf9359a73`  
		Last Modified: Tue, 14 May 2024 02:29:54 GMT  
		Size: 59.6 MB (59624672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a624816eaede9b3600518abc57d53c292c3eb1f7c38fc8708c644b77b11868b7`  
		Last Modified: Tue, 14 May 2024 02:29:49 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.1.6`

```console
$ docker pull emqx@sha256:6aeae6e7a0b2852ddbde75b6d8c9468d38ebe8f69ad56a283518358b74d62145
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
$ docker pull emqx@sha256:6d918cbe4d93a26b8277cc81c64cfb3043b54fedeb236f8ccf8c798381e60b6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92722662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:565299c2bab277f1a5c99f75717ffd066b3042947f32d493df6bcbe6aa15789c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:28:08 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:28:09 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 14 May 2024 02:28:09 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 14 May 2024 02:28:09 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 14 May 2024 02:28:09 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 14 May 2024 02:28:09 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 14 May 2024 02:28:14 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 14 May 2024 02:28:15 GMT
WORKDIR /opt/emqx
# Tue, 14 May 2024 02:28:15 GMT
USER emqx
# Tue, 14 May 2024 02:28:15 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 14 May 2024 02:28:15 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 14 May 2024 02:28:15 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 14 May 2024 02:28:15 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 14 May 2024 02:28:15 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2335c9ad8fddf7f96c47075cd2601e30075a8a6be73151654fcae1eeb448c917`  
		Last Modified: Tue, 14 May 2024 02:29:51 GMT  
		Size: 3.0 MB (3006068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0ede5b19e6daa66212ba8878c1ed2f180a34e2a36efb70525ab33331ead792`  
		Last Modified: Tue, 14 May 2024 02:29:49 GMT  
		Size: 4.1 KB (4113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b960bb93130c3fa5d765900f22542f1268b7f05e852763d02f924acf9359a73`  
		Last Modified: Tue, 14 May 2024 02:29:54 GMT  
		Size: 59.6 MB (59624672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a624816eaede9b3600518abc57d53c292c3eb1f7c38fc8708c644b77b11868b7`  
		Last Modified: Tue, 14 May 2024 02:29:49 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.2`

```console
$ docker pull emqx@sha256:36a17b769b0c8a956a65dff6b3da4672b795a8feed79200ae33de52e40b6eaaa
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
$ docker pull emqx@sha256:e90a27e12f31ab0189ba3ba7fc2db6aea1e2894fe78698f2a973c25af54b0670
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91489505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e486f4ebce98e0ef0c136c6df2deb69e6aa365d4bf03e08c72e703901602bd37`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:28:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:28:22 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 14 May 2024 02:28:22 GMT
ENV EMQX_VERSION=5.2.1
# Tue, 14 May 2024 02:28:22 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Tue, 14 May 2024 02:28:22 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Tue, 14 May 2024 02:28:22 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 14 May 2024 02:28:30 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Tue, 14 May 2024 02:28:30 GMT
WORKDIR /opt/emqx
# Tue, 14 May 2024 02:28:31 GMT
USER emqx
# Tue, 14 May 2024 02:28:31 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 14 May 2024 02:28:31 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 14 May 2024 02:28:31 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 14 May 2024 02:28:31 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 14 May 2024 02:28:31 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50da094c8c9f74d40417ca5890caa50decfc401ccb62615d4964f089f8414d7`  
		Last Modified: Tue, 14 May 2024 02:30:03 GMT  
		Size: 1.6 MB (1645768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf5ba4147baf0f885674087f18b5fa265b6f62d2021eab2119561aa46661446`  
		Last Modified: Tue, 14 May 2024 02:30:02 GMT  
		Size: 4.1 KB (4113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c46ae639ea03377b7abb11520c62303b25c5d907216f19d76eacb0d07dec1a`  
		Last Modified: Tue, 14 May 2024 02:30:07 GMT  
		Size: 59.8 MB (59751815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca71f7321a4849b28e3a76c6068d0c19bba984ed2c03b55a3e88c164e46f09a9`  
		Last Modified: Tue, 14 May 2024 02:30:02 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.2.1`

```console
$ docker pull emqx@sha256:36a17b769b0c8a956a65dff6b3da4672b795a8feed79200ae33de52e40b6eaaa
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
$ docker pull emqx@sha256:e90a27e12f31ab0189ba3ba7fc2db6aea1e2894fe78698f2a973c25af54b0670
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91489505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e486f4ebce98e0ef0c136c6df2deb69e6aa365d4bf03e08c72e703901602bd37`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:28:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:28:22 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 14 May 2024 02:28:22 GMT
ENV EMQX_VERSION=5.2.1
# Tue, 14 May 2024 02:28:22 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Tue, 14 May 2024 02:28:22 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Tue, 14 May 2024 02:28:22 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 14 May 2024 02:28:30 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Tue, 14 May 2024 02:28:30 GMT
WORKDIR /opt/emqx
# Tue, 14 May 2024 02:28:31 GMT
USER emqx
# Tue, 14 May 2024 02:28:31 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 14 May 2024 02:28:31 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 14 May 2024 02:28:31 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 14 May 2024 02:28:31 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 14 May 2024 02:28:31 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50da094c8c9f74d40417ca5890caa50decfc401ccb62615d4964f089f8414d7`  
		Last Modified: Tue, 14 May 2024 02:30:03 GMT  
		Size: 1.6 MB (1645768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf5ba4147baf0f885674087f18b5fa265b6f62d2021eab2119561aa46661446`  
		Last Modified: Tue, 14 May 2024 02:30:02 GMT  
		Size: 4.1 KB (4113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c46ae639ea03377b7abb11520c62303b25c5d907216f19d76eacb0d07dec1a`  
		Last Modified: Tue, 14 May 2024 02:30:07 GMT  
		Size: 59.8 MB (59751815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca71f7321a4849b28e3a76c6068d0c19bba984ed2c03b55a3e88c164e46f09a9`  
		Last Modified: Tue, 14 May 2024 02:30:02 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.3`

```console
$ docker pull emqx@sha256:b6553a617a8f8b5071c89828a76c948493356dfce918b22670b082e1f60b77d8
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
$ docker pull emqx@sha256:65ddda3b8cb76dfdd7056d578672ad380e1a380b7af8e4c957a74f4155754878
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92103519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d66ccf57fde821b66ae8ca45d94ea583d9102deda527141b628d4bf30f6762`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:28:34 GMT
ENV EMQX_VERSION=5.3.2
# Tue, 14 May 2024 02:28:34 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Tue, 14 May 2024 02:28:34 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Tue, 14 May 2024 02:28:34 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 14 May 2024 02:28:45 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:28:45 GMT
WORKDIR /opt/emqx
# Tue, 14 May 2024 02:28:46 GMT
USER emqx
# Tue, 14 May 2024 02:28:46 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 14 May 2024 02:28:46 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 14 May 2024 02:28:46 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 14 May 2024 02:28:46 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 14 May 2024 02:28:46 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce4a5d65c9bc5b47cdcc4509f8fdb150273cba48bcacf24d9f9962e3e65a649`  
		Last Modified: Tue, 14 May 2024 02:30:21 GMT  
		Size: 62.0 MB (62015709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b2c4265e216c55749cdbce816f4f4d6b7973f559dd62c35ba9e6a5fe28f77b6`  
		Last Modified: Tue, 14 May 2024 02:30:16 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.3.2`

```console
$ docker pull emqx@sha256:b6553a617a8f8b5071c89828a76c948493356dfce918b22670b082e1f60b77d8
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
$ docker pull emqx@sha256:65ddda3b8cb76dfdd7056d578672ad380e1a380b7af8e4c957a74f4155754878
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92103519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d66ccf57fde821b66ae8ca45d94ea583d9102deda527141b628d4bf30f6762`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:28:34 GMT
ENV EMQX_VERSION=5.3.2
# Tue, 14 May 2024 02:28:34 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Tue, 14 May 2024 02:28:34 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Tue, 14 May 2024 02:28:34 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 14 May 2024 02:28:45 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:28:45 GMT
WORKDIR /opt/emqx
# Tue, 14 May 2024 02:28:46 GMT
USER emqx
# Tue, 14 May 2024 02:28:46 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 14 May 2024 02:28:46 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 14 May 2024 02:28:46 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 14 May 2024 02:28:46 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 14 May 2024 02:28:46 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce4a5d65c9bc5b47cdcc4509f8fdb150273cba48bcacf24d9f9962e3e65a649`  
		Last Modified: Tue, 14 May 2024 02:30:21 GMT  
		Size: 62.0 MB (62015709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b2c4265e216c55749cdbce816f4f4d6b7973f559dd62c35ba9e6a5fe28f77b6`  
		Last Modified: Tue, 14 May 2024 02:30:16 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.4`

```console
$ docker pull emqx@sha256:e83530043bf3e3f5ce5c8ff28d135429848ef001fb648ee0c42734c60165bfb1
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
$ docker pull emqx@sha256:72c3e56c8a087f07206f31ea34c88704a647dbd2cfebbfab53c70c044d3064d2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108498977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0cd6f626cbd4330e0b180acefb8ab3d639718afafd0907244c1aa5a1eb8d96d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:28:50 GMT
ENV EMQX_VERSION=5.4.1
# Tue, 14 May 2024 02:28:50 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Tue, 14 May 2024 02:28:50 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Tue, 14 May 2024 02:28:50 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 14 May 2024 02:29:02 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:29:02 GMT
WORKDIR /opt/emqx
# Tue, 14 May 2024 02:29:02 GMT
USER emqx
# Tue, 14 May 2024 02:29:03 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 14 May 2024 02:29:03 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 14 May 2024 02:29:03 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 14 May 2024 02:29:03 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 14 May 2024 02:29:03 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27aa141be48f2a2c8b73787e4c1c39fbce731c96a734771b1e5c1e3b3586eecb`  
		Last Modified: Tue, 14 May 2024 02:30:36 GMT  
		Size: 78.4 MB (78411167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7e5639736fa58ab4b9e66ef174c7f3348802775bff195dbec3ee938f634d37d`  
		Last Modified: Tue, 14 May 2024 02:30:29 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.4.1`

```console
$ docker pull emqx@sha256:e83530043bf3e3f5ce5c8ff28d135429848ef001fb648ee0c42734c60165bfb1
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
$ docker pull emqx@sha256:72c3e56c8a087f07206f31ea34c88704a647dbd2cfebbfab53c70c044d3064d2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108498977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0cd6f626cbd4330e0b180acefb8ab3d639718afafd0907244c1aa5a1eb8d96d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:28:50 GMT
ENV EMQX_VERSION=5.4.1
# Tue, 14 May 2024 02:28:50 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Tue, 14 May 2024 02:28:50 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Tue, 14 May 2024 02:28:50 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 14 May 2024 02:29:02 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:29:02 GMT
WORKDIR /opt/emqx
# Tue, 14 May 2024 02:29:02 GMT
USER emqx
# Tue, 14 May 2024 02:29:03 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 14 May 2024 02:29:03 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 14 May 2024 02:29:03 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 14 May 2024 02:29:03 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 14 May 2024 02:29:03 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27aa141be48f2a2c8b73787e4c1c39fbce731c96a734771b1e5c1e3b3586eecb`  
		Last Modified: Tue, 14 May 2024 02:30:36 GMT  
		Size: 78.4 MB (78411167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7e5639736fa58ab4b9e66ef174c7f3348802775bff195dbec3ee938f634d37d`  
		Last Modified: Tue, 14 May 2024 02:30:29 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.5`

```console
$ docker pull emqx@sha256:205caaab8420759af07f3160ca3aa8413dca2598f5b1d687c1ca60698fe5bdd8
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
$ docker pull emqx@sha256:cfcf813651006a0bddeb7bd2f1e890b95d26e798183572f2840f2043d20f2835
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116797041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e892a4723e35623f06908fe7d4174464065b39d72cc500bb460c7d2915b47c9`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:29:06 GMT
ENV EMQX_VERSION=5.5.1
# Tue, 14 May 2024 02:29:07 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Tue, 14 May 2024 02:29:07 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Tue, 14 May 2024 02:29:07 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 14 May 2024 02:29:19 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 14 May 2024 02:29:19 GMT
WORKDIR /opt/emqx
# Tue, 14 May 2024 02:29:19 GMT
USER emqx
# Tue, 14 May 2024 02:29:19 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 14 May 2024 02:29:20 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 14 May 2024 02:29:20 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 14 May 2024 02:29:20 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 14 May 2024 02:29:20 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dced50349d06784cb80c0dd528e2b72d7380cbc3967595f7baeb2364cf6fba5e`  
		Last Modified: Tue, 14 May 2024 02:30:51 GMT  
		Size: 86.7 MB (86709102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9dfc89c2cf5990485a088b7448d3b67bfe9bc60b118b423d05c71d393d1a05f`  
		Last Modified: Tue, 14 May 2024 02:30:44 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.5.1`

```console
$ docker pull emqx@sha256:205caaab8420759af07f3160ca3aa8413dca2598f5b1d687c1ca60698fe5bdd8
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
$ docker pull emqx@sha256:cfcf813651006a0bddeb7bd2f1e890b95d26e798183572f2840f2043d20f2835
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116797041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e892a4723e35623f06908fe7d4174464065b39d72cc500bb460c7d2915b47c9`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:29:06 GMT
ENV EMQX_VERSION=5.5.1
# Tue, 14 May 2024 02:29:07 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Tue, 14 May 2024 02:29:07 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Tue, 14 May 2024 02:29:07 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 14 May 2024 02:29:19 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 14 May 2024 02:29:19 GMT
WORKDIR /opt/emqx
# Tue, 14 May 2024 02:29:19 GMT
USER emqx
# Tue, 14 May 2024 02:29:19 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 14 May 2024 02:29:20 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 14 May 2024 02:29:20 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 14 May 2024 02:29:20 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 14 May 2024 02:29:20 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dced50349d06784cb80c0dd528e2b72d7380cbc3967595f7baeb2364cf6fba5e`  
		Last Modified: Tue, 14 May 2024 02:30:51 GMT  
		Size: 86.7 MB (86709102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9dfc89c2cf5990485a088b7448d3b67bfe9bc60b118b423d05c71d393d1a05f`  
		Last Modified: Tue, 14 May 2024 02:30:44 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.6`

```console
$ docker pull emqx@sha256:2c8ba459aa700c553373f697cda1897c4c61ad889500f62f728eaa70786069ab
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
$ docker pull emqx@sha256:8468c03000265baff59f6e0b9672f48f3c6b97390dd5b4cdff617f5c97442f0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120796320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7ef707698df6918c8e04ee8441d77ec406bf81d94cc5c1d276a9180b446008`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:29:23 GMT
ENV EMQX_VERSION=5.6.1
# Tue, 14 May 2024 02:29:23 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Tue, 14 May 2024 02:29:23 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Tue, 14 May 2024 02:29:23 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 14 May 2024 02:29:36 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 14 May 2024 02:29:37 GMT
WORKDIR /opt/emqx
# Tue, 14 May 2024 02:29:37 GMT
USER emqx
# Tue, 14 May 2024 02:29:37 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 14 May 2024 02:29:37 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 14 May 2024 02:29:37 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 14 May 2024 02:29:37 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 14 May 2024 02:29:37 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0462ebe9d5a7da4209ef18c6868756f65c50af18ae6a0ab8b488ee547abd7dc1`  
		Last Modified: Tue, 14 May 2024 02:31:07 GMT  
		Size: 91.6 MB (91615783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa9fd0acdb66a85f8f5effb30d086ed735a003eb6fe434a2d47984fd6aa4c52`  
		Last Modified: Tue, 14 May 2024 02:30:59 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.6.1`

```console
$ docker pull emqx@sha256:2c8ba459aa700c553373f697cda1897c4c61ad889500f62f728eaa70786069ab
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
$ docker pull emqx@sha256:8468c03000265baff59f6e0b9672f48f3c6b97390dd5b4cdff617f5c97442f0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120796320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7ef707698df6918c8e04ee8441d77ec406bf81d94cc5c1d276a9180b446008`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:29:23 GMT
ENV EMQX_VERSION=5.6.1
# Tue, 14 May 2024 02:29:23 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Tue, 14 May 2024 02:29:23 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Tue, 14 May 2024 02:29:23 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 14 May 2024 02:29:36 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 14 May 2024 02:29:37 GMT
WORKDIR /opt/emqx
# Tue, 14 May 2024 02:29:37 GMT
USER emqx
# Tue, 14 May 2024 02:29:37 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 14 May 2024 02:29:37 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 14 May 2024 02:29:37 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 14 May 2024 02:29:37 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 14 May 2024 02:29:37 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0462ebe9d5a7da4209ef18c6868756f65c50af18ae6a0ab8b488ee547abd7dc1`  
		Last Modified: Tue, 14 May 2024 02:31:07 GMT  
		Size: 91.6 MB (91615783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa9fd0acdb66a85f8f5effb30d086ed735a003eb6fe434a2d47984fd6aa4c52`  
		Last Modified: Tue, 14 May 2024 02:30:59 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:latest`

```console
$ docker pull emqx@sha256:2c8ba459aa700c553373f697cda1897c4c61ad889500f62f728eaa70786069ab
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
$ docker pull emqx@sha256:8468c03000265baff59f6e0b9672f48f3c6b97390dd5b4cdff617f5c97442f0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120796320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7ef707698df6918c8e04ee8441d77ec406bf81d94cc5c1d276a9180b446008`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:29:23 GMT
ENV EMQX_VERSION=5.6.1
# Tue, 14 May 2024 02:29:23 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Tue, 14 May 2024 02:29:23 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Tue, 14 May 2024 02:29:23 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 14 May 2024 02:29:36 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 14 May 2024 02:29:37 GMT
WORKDIR /opt/emqx
# Tue, 14 May 2024 02:29:37 GMT
USER emqx
# Tue, 14 May 2024 02:29:37 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 14 May 2024 02:29:37 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 14 May 2024 02:29:37 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 14 May 2024 02:29:37 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 14 May 2024 02:29:37 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0462ebe9d5a7da4209ef18c6868756f65c50af18ae6a0ab8b488ee547abd7dc1`  
		Last Modified: Tue, 14 May 2024 02:31:07 GMT  
		Size: 91.6 MB (91615783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa9fd0acdb66a85f8f5effb30d086ed735a003eb6fe434a2d47984fd6aa4c52`  
		Last Modified: Tue, 14 May 2024 02:30:59 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
