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
-	[`emqx:5.7`](#emqx57)
-	[`emqx:5.7.0`](#emqx570)
-	[`emqx:latest`](#emqxlatest)

## `emqx:5`

```console
$ docker pull emqx@sha256:1e3008739b2a9826d165563f2a01a37ba1512579a6e4962c1d6c12d2c5f33159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:b61169b9ea180b4b94e80e5270b70cc98d27f7403dbc6ab1862b67598c440c2f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125874711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a1ce4aea8d2a264875f19a6be895364b3c8d26b0323bd39d6303b4b872cf4e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 28 May 2024 22:51:01 GMT
ENV EMQX_VERSION=5.7.0
# Tue, 28 May 2024 22:51:01 GMT
ENV AMD64_SHA256=910d6ff5af8c36df9d15ae99a9ffe03a9690849fd952b7666b5809d9f9c42180
# Tue, 28 May 2024 22:51:01 GMT
ENV ARM64_SHA256=4e7c4e3f321f6ce8de5d9da93e96769a49174f62ffecc61451b2292e6f3e415f
# Tue, 28 May 2024 22:51:02 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 28 May 2024 22:51:17 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 28 May 2024 22:51:18 GMT
WORKDIR /opt/emqx
# Tue, 28 May 2024 22:51:18 GMT
USER emqx
# Tue, 28 May 2024 22:51:18 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 28 May 2024 22:51:18 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 28 May 2024 22:51:18 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 28 May 2024 22:51:18 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 28 May 2024 22:51:19 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895353a6d3adcc5ecde8b1b0282c168023c4c6632ca780317cc15a07f0b69a6c`  
		Last Modified: Tue, 28 May 2024 22:51:49 GMT  
		Size: 96.7 MB (96723267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24da20449b1d0b327b87538fbc3533b2ff0c0bb7e6c28e7c2378997904904781`  
		Last Modified: Tue, 28 May 2024 22:51:39 GMT  
		Size: 1.0 KB (1033 bytes)  
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
$ docker pull emqx@sha256:88e7a8f67e641974c8b773dc1db786fbc4c3a6764dc75d911942bd95ecd16eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.1` - linux; amd64

```console
$ docker pull emqx@sha256:abcbbcd9a30d408f543a6ef299bc7b353c633ac8e0b77a8d04e7ddb13b4ccb04
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102409711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c495d49e100699108f1fe4d768a39fd25081e455ca6f41a2e20d3f89b5097f2a`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:12:28 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 03:12:29 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 14 May 2024 03:12:29 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 14 May 2024 03:12:29 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 14 May 2024 03:12:29 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 14 May 2024 03:12:29 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 14 May 2024 03:12:36 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 14 May 2024 03:12:36 GMT
WORKDIR /opt/emqx
# Tue, 14 May 2024 03:12:36 GMT
USER emqx
# Tue, 14 May 2024 03:12:37 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 14 May 2024 03:12:37 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 14 May 2024 03:12:37 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 14 May 2024 03:12:37 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 14 May 2024 03:12:37 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02397ca234f0d94cb94b2cad18187869fb71bc89840bffc35d101f6dc3817301`  
		Last Modified: Tue, 14 May 2024 03:14:44 GMT  
		Size: 3.0 MB (2989515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b6c604730f1eba1bfd235f4a33a268d42210ef0ff0aa23af9cabd25a8d0124`  
		Last Modified: Tue, 14 May 2024 03:14:43 GMT  
		Size: 4.1 KB (4108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4bfbeaab4e0b9def977d823cdb5429d2de6086d83c846c40f459f29e0594ce5`  
		Last Modified: Tue, 14 May 2024 03:14:50 GMT  
		Size: 68.0 MB (67981255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5822bb4046041b64d0cf8774a8cb345c0f9305fb228a87d2044eb6007e03253f`  
		Last Modified: Tue, 14 May 2024 03:14:43 GMT  
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
$ docker pull emqx@sha256:88e7a8f67e641974c8b773dc1db786fbc4c3a6764dc75d911942bd95ecd16eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.1.6` - linux; amd64

```console
$ docker pull emqx@sha256:abcbbcd9a30d408f543a6ef299bc7b353c633ac8e0b77a8d04e7ddb13b4ccb04
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102409711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c495d49e100699108f1fe4d768a39fd25081e455ca6f41a2e20d3f89b5097f2a`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:12:28 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 03:12:29 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 14 May 2024 03:12:29 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 14 May 2024 03:12:29 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 14 May 2024 03:12:29 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 14 May 2024 03:12:29 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 14 May 2024 03:12:36 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 14 May 2024 03:12:36 GMT
WORKDIR /opt/emqx
# Tue, 14 May 2024 03:12:36 GMT
USER emqx
# Tue, 14 May 2024 03:12:37 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 14 May 2024 03:12:37 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 14 May 2024 03:12:37 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 14 May 2024 03:12:37 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 14 May 2024 03:12:37 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02397ca234f0d94cb94b2cad18187869fb71bc89840bffc35d101f6dc3817301`  
		Last Modified: Tue, 14 May 2024 03:14:44 GMT  
		Size: 3.0 MB (2989515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b6c604730f1eba1bfd235f4a33a268d42210ef0ff0aa23af9cabd25a8d0124`  
		Last Modified: Tue, 14 May 2024 03:14:43 GMT  
		Size: 4.1 KB (4108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4bfbeaab4e0b9def977d823cdb5429d2de6086d83c846c40f459f29e0594ce5`  
		Last Modified: Tue, 14 May 2024 03:14:50 GMT  
		Size: 68.0 MB (67981255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5822bb4046041b64d0cf8774a8cb345c0f9305fb228a87d2044eb6007e03253f`  
		Last Modified: Tue, 14 May 2024 03:14:43 GMT  
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
$ docker pull emqx@sha256:06732e4e371240168c41643f8c4b1c63e99217df01a02de9245e152ebdc9d523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.2` - linux; amd64

```console
$ docker pull emqx@sha256:0ed8f7f70d686feac69ebe7ecbe49ab5d7a90b71203afe818669a54f37566e90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101181287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f6cf483cf7deb26ca572339762a600ede9a866af4d37e608ba1459e2c2b62db`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:12:48 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 03:12:48 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 14 May 2024 03:12:48 GMT
ENV EMQX_VERSION=5.2.1
# Tue, 14 May 2024 03:12:48 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Tue, 14 May 2024 03:12:48 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Tue, 14 May 2024 03:12:49 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 14 May 2024 03:13:00 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Tue, 14 May 2024 03:13:01 GMT
WORKDIR /opt/emqx
# Tue, 14 May 2024 03:13:01 GMT
USER emqx
# Tue, 14 May 2024 03:13:01 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 14 May 2024 03:13:01 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 14 May 2024 03:13:01 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 14 May 2024 03:13:01 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 14 May 2024 03:13:01 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1712a347a599c16f58b171dedd831b0ca6d2c85c5481d19746463c96eb748e34`  
		Last Modified: Tue, 14 May 2024 03:14:59 GMT  
		Size: 1.6 MB (1631417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88a838608a2011895399f285fb9384fcac354df78ff0d6e11ac0903b0c8f63b`  
		Last Modified: Tue, 14 May 2024 03:14:58 GMT  
		Size: 4.1 KB (4108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bcb1160539e761cf50693e088c38665690cbf6f85a7976bb6a35ca5588bee21`  
		Last Modified: Tue, 14 May 2024 03:15:05 GMT  
		Size: 68.1 MB (68110930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8e9c2a291c8cc57ab056850b4e3368eaacef8a0e8092776c7dade8bf0a992f`  
		Last Modified: Tue, 14 May 2024 03:14:59 GMT  
		Size: 901.0 B  
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
$ docker pull emqx@sha256:06732e4e371240168c41643f8c4b1c63e99217df01a02de9245e152ebdc9d523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.2.1` - linux; amd64

```console
$ docker pull emqx@sha256:0ed8f7f70d686feac69ebe7ecbe49ab5d7a90b71203afe818669a54f37566e90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101181287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f6cf483cf7deb26ca572339762a600ede9a866af4d37e608ba1459e2c2b62db`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:12:48 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 03:12:48 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 14 May 2024 03:12:48 GMT
ENV EMQX_VERSION=5.2.1
# Tue, 14 May 2024 03:12:48 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Tue, 14 May 2024 03:12:48 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Tue, 14 May 2024 03:12:49 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 14 May 2024 03:13:00 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Tue, 14 May 2024 03:13:01 GMT
WORKDIR /opt/emqx
# Tue, 14 May 2024 03:13:01 GMT
USER emqx
# Tue, 14 May 2024 03:13:01 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 14 May 2024 03:13:01 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 14 May 2024 03:13:01 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 14 May 2024 03:13:01 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 14 May 2024 03:13:01 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1712a347a599c16f58b171dedd831b0ca6d2c85c5481d19746463c96eb748e34`  
		Last Modified: Tue, 14 May 2024 03:14:59 GMT  
		Size: 1.6 MB (1631417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88a838608a2011895399f285fb9384fcac354df78ff0d6e11ac0903b0c8f63b`  
		Last Modified: Tue, 14 May 2024 03:14:58 GMT  
		Size: 4.1 KB (4108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bcb1160539e761cf50693e088c38665690cbf6f85a7976bb6a35ca5588bee21`  
		Last Modified: Tue, 14 May 2024 03:15:05 GMT  
		Size: 68.1 MB (68110930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8e9c2a291c8cc57ab056850b4e3368eaacef8a0e8092776c7dade8bf0a992f`  
		Last Modified: Tue, 14 May 2024 03:14:59 GMT  
		Size: 901.0 B  
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
$ docker pull emqx@sha256:bfe5d3907d83ace3046e70fd34a016aed141c55d0af6828ac8a4ff9c00f309ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.3` - linux; amd64

```console
$ docker pull emqx@sha256:08ccb3003c3649110513361c59bdc1827003838fca2f2bda4c16943be8a72b3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101796635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f766d327facb103b452669b216b5fa27b0d0ffe06b937c1a14556ed0832cac73`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:13:07 GMT
ENV EMQX_VERSION=5.3.2
# Tue, 14 May 2024 03:13:07 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Tue, 14 May 2024 03:13:07 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Tue, 14 May 2024 03:13:07 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 14 May 2024 03:13:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 03:13:21 GMT
WORKDIR /opt/emqx
# Tue, 14 May 2024 03:13:22 GMT
USER emqx
# Tue, 14 May 2024 03:13:22 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 14 May 2024 03:13:22 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 14 May 2024 03:13:22 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 14 May 2024 03:13:22 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 14 May 2024 03:13:22 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5125f69351dd5593f39af7db945721fd2aee5a00298980f54f7ccfd0fbb541e`  
		Last Modified: Tue, 14 May 2024 03:15:21 GMT  
		Size: 70.4 MB (70361802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3842eb4ddb21b381471855f2e80f489d6139ba68f7199b8395da3b0e6723f2f0`  
		Last Modified: Tue, 14 May 2024 03:15:13 GMT  
		Size: 902.0 B  
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
$ docker pull emqx@sha256:bfe5d3907d83ace3046e70fd34a016aed141c55d0af6828ac8a4ff9c00f309ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.3.2` - linux; amd64

```console
$ docker pull emqx@sha256:08ccb3003c3649110513361c59bdc1827003838fca2f2bda4c16943be8a72b3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101796635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f766d327facb103b452669b216b5fa27b0d0ffe06b937c1a14556ed0832cac73`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:13:07 GMT
ENV EMQX_VERSION=5.3.2
# Tue, 14 May 2024 03:13:07 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Tue, 14 May 2024 03:13:07 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Tue, 14 May 2024 03:13:07 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 14 May 2024 03:13:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 03:13:21 GMT
WORKDIR /opt/emqx
# Tue, 14 May 2024 03:13:22 GMT
USER emqx
# Tue, 14 May 2024 03:13:22 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 14 May 2024 03:13:22 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 14 May 2024 03:13:22 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 14 May 2024 03:13:22 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 14 May 2024 03:13:22 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5125f69351dd5593f39af7db945721fd2aee5a00298980f54f7ccfd0fbb541e`  
		Last Modified: Tue, 14 May 2024 03:15:21 GMT  
		Size: 70.4 MB (70361802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3842eb4ddb21b381471855f2e80f489d6139ba68f7199b8395da3b0e6723f2f0`  
		Last Modified: Tue, 14 May 2024 03:15:13 GMT  
		Size: 902.0 B  
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
$ docker pull emqx@sha256:8432439cc61f94d9603577ed5862256b19354c2af83408037bf489ec5d472f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.4` - linux; amd64

```console
$ docker pull emqx@sha256:74b55f501e3437efe2ff0152b312627f4f34f80124c0c2d9a13a9516b2cdeecb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118710674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db7c727900238fd1cf8df1dd4315c22c860fc73795660f3936fedbb44640246`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:13:28 GMT
ENV EMQX_VERSION=5.4.1
# Tue, 14 May 2024 03:13:28 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Tue, 14 May 2024 03:13:28 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Tue, 14 May 2024 03:13:28 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 14 May 2024 03:13:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 03:13:43 GMT
WORKDIR /opt/emqx
# Tue, 14 May 2024 03:13:44 GMT
USER emqx
# Tue, 14 May 2024 03:13:44 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 14 May 2024 03:13:44 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 14 May 2024 03:13:44 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 14 May 2024 03:13:44 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 14 May 2024 03:13:44 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcdf98671cff1c4997112b049b58834a774de28f1ad0226b3e39df2249fdfed`  
		Last Modified: Tue, 14 May 2024 03:15:38 GMT  
		Size: 87.3 MB (87275844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff764705056e5095820a2933d1934fd14bc0bca37f961222275ad82d40d3dfd5`  
		Last Modified: Tue, 14 May 2024 03:15:29 GMT  
		Size: 899.0 B  
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
$ docker pull emqx@sha256:8432439cc61f94d9603577ed5862256b19354c2af83408037bf489ec5d472f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.4.1` - linux; amd64

```console
$ docker pull emqx@sha256:74b55f501e3437efe2ff0152b312627f4f34f80124c0c2d9a13a9516b2cdeecb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118710674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db7c727900238fd1cf8df1dd4315c22c860fc73795660f3936fedbb44640246`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:13:28 GMT
ENV EMQX_VERSION=5.4.1
# Tue, 14 May 2024 03:13:28 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Tue, 14 May 2024 03:13:28 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Tue, 14 May 2024 03:13:28 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 14 May 2024 03:13:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 03:13:43 GMT
WORKDIR /opt/emqx
# Tue, 14 May 2024 03:13:44 GMT
USER emqx
# Tue, 14 May 2024 03:13:44 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 14 May 2024 03:13:44 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 14 May 2024 03:13:44 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 14 May 2024 03:13:44 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 14 May 2024 03:13:44 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcdf98671cff1c4997112b049b58834a774de28f1ad0226b3e39df2249fdfed`  
		Last Modified: Tue, 14 May 2024 03:15:38 GMT  
		Size: 87.3 MB (87275844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff764705056e5095820a2933d1934fd14bc0bca37f961222275ad82d40d3dfd5`  
		Last Modified: Tue, 14 May 2024 03:15:29 GMT  
		Size: 899.0 B  
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
$ docker pull emqx@sha256:a29adb838dbec92f42d0dc00dc1c735fa745e3f1d06d16263d697129081b9a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.5` - linux; amd64

```console
$ docker pull emqx@sha256:11ab1ca9242648843216eeaa727691a55f2c50f8202a8211a0b8dc4e8537beb7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121275965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45376c5b892275060b751bae55e87e1e89076acf560b74e3b4bfce27d2b32fa2`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:13:48 GMT
ENV EMQX_VERSION=5.5.1
# Tue, 14 May 2024 03:13:48 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Tue, 14 May 2024 03:13:48 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Tue, 14 May 2024 03:13:49 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 14 May 2024 03:14:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 14 May 2024 03:14:04 GMT
WORKDIR /opt/emqx
# Tue, 14 May 2024 03:14:04 GMT
USER emqx
# Tue, 14 May 2024 03:14:04 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 14 May 2024 03:14:04 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 14 May 2024 03:14:04 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 14 May 2024 03:14:04 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 14 May 2024 03:14:04 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7fe03889b9ce31633ec5e1d1aa5c5a997db15a5f1f662f20d5e6fd114adaf46`  
		Last Modified: Tue, 14 May 2024 03:15:56 GMT  
		Size: 89.8 MB (89841002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4ea328c7a9d737c343eb56a3967b6651e00024489ef7ae168e0e675566cd31`  
		Last Modified: Tue, 14 May 2024 03:15:46 GMT  
		Size: 1.0 KB (1032 bytes)  
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
$ docker pull emqx@sha256:a29adb838dbec92f42d0dc00dc1c735fa745e3f1d06d16263d697129081b9a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.5.1` - linux; amd64

```console
$ docker pull emqx@sha256:11ab1ca9242648843216eeaa727691a55f2c50f8202a8211a0b8dc4e8537beb7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121275965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45376c5b892275060b751bae55e87e1e89076acf560b74e3b4bfce27d2b32fa2`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:13:48 GMT
ENV EMQX_VERSION=5.5.1
# Tue, 14 May 2024 03:13:48 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Tue, 14 May 2024 03:13:48 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Tue, 14 May 2024 03:13:49 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 14 May 2024 03:14:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 14 May 2024 03:14:04 GMT
WORKDIR /opt/emqx
# Tue, 14 May 2024 03:14:04 GMT
USER emqx
# Tue, 14 May 2024 03:14:04 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 14 May 2024 03:14:04 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 14 May 2024 03:14:04 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 14 May 2024 03:14:04 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 14 May 2024 03:14:04 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7fe03889b9ce31633ec5e1d1aa5c5a997db15a5f1f662f20d5e6fd114adaf46`  
		Last Modified: Tue, 14 May 2024 03:15:56 GMT  
		Size: 89.8 MB (89841002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4ea328c7a9d737c343eb56a3967b6651e00024489ef7ae168e0e675566cd31`  
		Last Modified: Tue, 14 May 2024 03:15:46 GMT  
		Size: 1.0 KB (1032 bytes)  
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
$ docker pull emqx@sha256:29bf2b22da93132ed11e004502bfdba34b444917519fd58eed3f6c989be29253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.6` - linux; amd64

```console
$ docker pull emqx@sha256:71934238778e46374f87e420f5196d6f7cde6510143aaf37b8d528f81233411f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124206364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071bc163dbf9ba3432e612a1f1152c753eb38df56eef3cba325b07294c91884d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:14:09 GMT
ENV EMQX_VERSION=5.6.1
# Tue, 14 May 2024 03:14:09 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Tue, 14 May 2024 03:14:09 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Tue, 14 May 2024 03:14:09 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 14 May 2024 03:14:23 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 14 May 2024 03:14:24 GMT
WORKDIR /opt/emqx
# Tue, 14 May 2024 03:14:24 GMT
USER emqx
# Tue, 14 May 2024 03:14:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 14 May 2024 03:14:24 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 14 May 2024 03:14:25 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 14 May 2024 03:14:25 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 14 May 2024 03:14:25 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cd2d3eaea6697a7f4d1c145557d5a3811392776897a23618ef97bf6c7e12b3`  
		Last Modified: Tue, 14 May 2024 03:16:13 GMT  
		Size: 95.1 MB (95054921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768eb3f36811f7e6afc757a3fbdbaf3011847b98d725d030994453845d9d3e99`  
		Last Modified: Tue, 14 May 2024 03:16:04 GMT  
		Size: 1.0 KB (1032 bytes)  
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
$ docker pull emqx@sha256:29bf2b22da93132ed11e004502bfdba34b444917519fd58eed3f6c989be29253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.6.1` - linux; amd64

```console
$ docker pull emqx@sha256:71934238778e46374f87e420f5196d6f7cde6510143aaf37b8d528f81233411f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124206364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071bc163dbf9ba3432e612a1f1152c753eb38df56eef3cba325b07294c91884d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 03:14:09 GMT
ENV EMQX_VERSION=5.6.1
# Tue, 14 May 2024 03:14:09 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Tue, 14 May 2024 03:14:09 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Tue, 14 May 2024 03:14:09 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 14 May 2024 03:14:23 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 14 May 2024 03:14:24 GMT
WORKDIR /opt/emqx
# Tue, 14 May 2024 03:14:24 GMT
USER emqx
# Tue, 14 May 2024 03:14:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 14 May 2024 03:14:24 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 14 May 2024 03:14:25 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 14 May 2024 03:14:25 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 14 May 2024 03:14:25 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cd2d3eaea6697a7f4d1c145557d5a3811392776897a23618ef97bf6c7e12b3`  
		Last Modified: Tue, 14 May 2024 03:16:13 GMT  
		Size: 95.1 MB (95054921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768eb3f36811f7e6afc757a3fbdbaf3011847b98d725d030994453845d9d3e99`  
		Last Modified: Tue, 14 May 2024 03:16:04 GMT  
		Size: 1.0 KB (1032 bytes)  
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

## `emqx:5.7`

```console
$ docker pull emqx@sha256:da3794273813b09a083cf07651b50f91f55dee4fb7b4bd5aafd303600c323877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `emqx:5.7` - linux; amd64

```console
$ docker pull emqx@sha256:b61169b9ea180b4b94e80e5270b70cc98d27f7403dbc6ab1862b67598c440c2f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125874711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a1ce4aea8d2a264875f19a6be895364b3c8d26b0323bd39d6303b4b872cf4e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 28 May 2024 22:51:01 GMT
ENV EMQX_VERSION=5.7.0
# Tue, 28 May 2024 22:51:01 GMT
ENV AMD64_SHA256=910d6ff5af8c36df9d15ae99a9ffe03a9690849fd952b7666b5809d9f9c42180
# Tue, 28 May 2024 22:51:01 GMT
ENV ARM64_SHA256=4e7c4e3f321f6ce8de5d9da93e96769a49174f62ffecc61451b2292e6f3e415f
# Tue, 28 May 2024 22:51:02 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 28 May 2024 22:51:17 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 28 May 2024 22:51:18 GMT
WORKDIR /opt/emqx
# Tue, 28 May 2024 22:51:18 GMT
USER emqx
# Tue, 28 May 2024 22:51:18 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 28 May 2024 22:51:18 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 28 May 2024 22:51:18 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 28 May 2024 22:51:18 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 28 May 2024 22:51:19 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895353a6d3adcc5ecde8b1b0282c168023c4c6632ca780317cc15a07f0b69a6c`  
		Last Modified: Tue, 28 May 2024 22:51:49 GMT  
		Size: 96.7 MB (96723267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24da20449b1d0b327b87538fbc3533b2ff0c0bb7e6c28e7c2378997904904781`  
		Last Modified: Tue, 28 May 2024 22:51:39 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.7.0`

```console
$ docker pull emqx@sha256:da3794273813b09a083cf07651b50f91f55dee4fb7b4bd5aafd303600c323877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `emqx:5.7.0` - linux; amd64

```console
$ docker pull emqx@sha256:b61169b9ea180b4b94e80e5270b70cc98d27f7403dbc6ab1862b67598c440c2f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125874711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a1ce4aea8d2a264875f19a6be895364b3c8d26b0323bd39d6303b4b872cf4e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 28 May 2024 22:51:01 GMT
ENV EMQX_VERSION=5.7.0
# Tue, 28 May 2024 22:51:01 GMT
ENV AMD64_SHA256=910d6ff5af8c36df9d15ae99a9ffe03a9690849fd952b7666b5809d9f9c42180
# Tue, 28 May 2024 22:51:01 GMT
ENV ARM64_SHA256=4e7c4e3f321f6ce8de5d9da93e96769a49174f62ffecc61451b2292e6f3e415f
# Tue, 28 May 2024 22:51:02 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 28 May 2024 22:51:17 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 28 May 2024 22:51:18 GMT
WORKDIR /opt/emqx
# Tue, 28 May 2024 22:51:18 GMT
USER emqx
# Tue, 28 May 2024 22:51:18 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 28 May 2024 22:51:18 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 28 May 2024 22:51:18 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 28 May 2024 22:51:18 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 28 May 2024 22:51:19 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895353a6d3adcc5ecde8b1b0282c168023c4c6632ca780317cc15a07f0b69a6c`  
		Last Modified: Tue, 28 May 2024 22:51:49 GMT  
		Size: 96.7 MB (96723267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24da20449b1d0b327b87538fbc3533b2ff0c0bb7e6c28e7c2378997904904781`  
		Last Modified: Tue, 28 May 2024 22:51:39 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:latest`

```console
$ docker pull emqx@sha256:1e3008739b2a9826d165563f2a01a37ba1512579a6e4962c1d6c12d2c5f33159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:b61169b9ea180b4b94e80e5270b70cc98d27f7403dbc6ab1862b67598c440c2f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125874711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a1ce4aea8d2a264875f19a6be895364b3c8d26b0323bd39d6303b4b872cf4e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 28 May 2024 22:51:01 GMT
ENV EMQX_VERSION=5.7.0
# Tue, 28 May 2024 22:51:01 GMT
ENV AMD64_SHA256=910d6ff5af8c36df9d15ae99a9ffe03a9690849fd952b7666b5809d9f9c42180
# Tue, 28 May 2024 22:51:01 GMT
ENV ARM64_SHA256=4e7c4e3f321f6ce8de5d9da93e96769a49174f62ffecc61451b2292e6f3e415f
# Tue, 28 May 2024 22:51:02 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 28 May 2024 22:51:17 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Tue, 28 May 2024 22:51:18 GMT
WORKDIR /opt/emqx
# Tue, 28 May 2024 22:51:18 GMT
USER emqx
# Tue, 28 May 2024 22:51:18 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 28 May 2024 22:51:18 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 28 May 2024 22:51:18 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 28 May 2024 22:51:18 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 28 May 2024 22:51:19 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895353a6d3adcc5ecde8b1b0282c168023c4c6632ca780317cc15a07f0b69a6c`  
		Last Modified: Tue, 28 May 2024 22:51:49 GMT  
		Size: 96.7 MB (96723267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24da20449b1d0b327b87538fbc3533b2ff0c0bb7e6c28e7c2378997904904781`  
		Last Modified: Tue, 28 May 2024 22:51:39 GMT  
		Size: 1.0 KB (1033 bytes)  
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
