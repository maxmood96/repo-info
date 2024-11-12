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
-	[`emqx:5.7.2`](#emqx572)
-	[`emqx:5.8`](#emqx58)
-	[`emqx:5.8.1`](#emqx581)
-	[`emqx:latest`](#emqxlatest)

## `emqx:5`

```console
$ docker pull emqx@sha256:decc1d0f5d41d2f1c4eb6f627404ed20ba42fde086cb028edaf8974ee65cee21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:60384f7e0afce136ad3fc5e57a4616720d5e5cf1083570301955c6bf8b943ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109911598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1b4c407ac1e4415796e5e02b662f753d7d482a03262e58d2a141012d533f4d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Sat, 19 Oct 2024 08:18:43 GMT
ADD rootfs.tar.xz / # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
CMD ["bash"]
# Sat, 19 Oct 2024 08:18:43 GMT
ENV EMQX_VERSION=5.8.1
# Sat, 19 Oct 2024 08:18:43 GMT
ENV AMD64_SHA256=5d7173169216f0af0cb6058387d8132dfa2cca901d684957f7b5ff75ae9ed6d8
# Sat, 19 Oct 2024 08:18:43 GMT
ENV ARM64_SHA256=fa404a444baeb8f67a4fdf1edbc3a16ea7f1249df8a43107fd54b8c02afcb167
# Sat, 19 Oct 2024 08:18:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Sat, 19 Oct 2024 08:18:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
WORKDIR /opt/emqx
# Sat, 19 Oct 2024 08:18:43 GMT
USER emqx
# Sat, 19 Oct 2024 08:18:43 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 19 Oct 2024 08:18:43 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Sat, 19 Oct 2024 08:18:43 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 19 Oct 2024 08:18:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3411c98fdf0a87bfa9c602bd68d8f3c97b43171b38b76d1359aa50a1b9a6fddb`  
		Last Modified: Tue, 12 Nov 2024 02:14:55 GMT  
		Size: 80.8 MB (80782541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6c3a751b4cd2ffbd05ad84e4817a59b00c30eeaf5af43352bcc747ebb5afda`  
		Last Modified: Tue, 12 Nov 2024 02:14:54 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:576eb49ecbf8a0a0649fed6d551d21144a90a68fc8f80182a2180ac476a027dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f74d1ca98d1e8c51cef06a64cf3621e8dc460279988a76c7feb8217f654e398`

```dockerfile
```

-	Layers:
	-	`sha256:aa34fea48a2d1a4629118d5daa681d0bd0ed894ffc2929b8d729590ad05b4aa2`  
		Last Modified: Tue, 12 Nov 2024 02:14:54 GMT  
		Size: 2.6 MB (2624750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8219044b35c6840dfdbc37b4d0c04b2c88df30be8e0722561941244969d466c`  
		Last Modified: Tue, 12 Nov 2024 02:14:54 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:26d0a2a274b6544735682c5c6b0fa79228aa7116107a8e641b10078352226e96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107099280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bffb3299ca78f97d0e7b8af7ae0f4263b23336165bc264ef2245fe9532ce1e60`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Sat, 19 Oct 2024 08:18:43 GMT
ADD rootfs.tar.xz / # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
CMD ["bash"]
# Sat, 19 Oct 2024 08:18:43 GMT
ENV EMQX_VERSION=5.8.1
# Sat, 19 Oct 2024 08:18:43 GMT
ENV AMD64_SHA256=5d7173169216f0af0cb6058387d8132dfa2cca901d684957f7b5ff75ae9ed6d8
# Sat, 19 Oct 2024 08:18:43 GMT
ENV ARM64_SHA256=fa404a444baeb8f67a4fdf1edbc3a16ea7f1249df8a43107fd54b8c02afcb167
# Sat, 19 Oct 2024 08:18:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Sat, 19 Oct 2024 08:18:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
WORKDIR /opt/emqx
# Sat, 19 Oct 2024 08:18:43 GMT
USER emqx
# Sat, 19 Oct 2024 08:18:43 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 19 Oct 2024 08:18:43 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Sat, 19 Oct 2024 08:18:43 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 19 Oct 2024 08:18:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1213e8941a1d725c8135186c642ce11321dfbce484861d16bbac4c0257f72936`  
		Last Modified: Tue, 12 Nov 2024 02:41:28 GMT  
		Size: 77.9 MB (77940861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0613112341eb4a876b533274a0c30bc7aea14ebe44ed4dde3609e0fe85835bde`  
		Last Modified: Tue, 12 Nov 2024 02:41:25 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:3c653c150236b3bd8bdbd1eab140b272178aaca27e7cef076786f1cdb5b45b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da20b0757e0d879de0d9a518eef254e2f20383f6c8c9996c1dcbabb72e735aa5`

```dockerfile
```

-	Layers:
	-	`sha256:3d67ea5997e278c74f766db587db9fee37836cb35dc2ab1344068a7a2e5987cb`  
		Last Modified: Tue, 12 Nov 2024 02:41:26 GMT  
		Size: 2.6 MB (2625029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b11bbf5e707341528c4fb7bcb32af45cfe08ceb39a2059720e2541d31e490f5a`  
		Last Modified: Tue, 12 Nov 2024 02:41:25 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.1`

```console
$ docker pull emqx@sha256:a910f06d2fcd50fecd3750e8002fd229695f19a72e6fd95efffad51ce13dd919
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.1` - linux; amd64

```console
$ docker pull emqx@sha256:fa95753e56e6d92a0bcff761bee646e94d1c8420525a8c93224f9c68b744f0c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.2 MB (102220475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38984fdf8596d80fbe3ae818ad966b6f6c880ca565f829b52eb18f6068f07077`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 05 Sep 2023 13:05:03 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
CMD ["bash"]
# Tue, 05 Sep 2023 13:05:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx; # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 05 Sep 2023 13:05:03 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 05 Sep 2023 13:05:03 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 05 Sep 2023 13:05:03 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 05 Sep 2023 13:05:03 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
WORKDIR /opt/emqx
# Tue, 05 Sep 2023 13:05:03 GMT
USER emqx
# Tue, 05 Sep 2023 13:05:03 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 05 Sep 2023 13:05:03 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 05 Sep 2023 13:05:03 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 05 Sep 2023 13:05:03 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe262f411763046f03e7cb5b5edc64fe69085bf0a4a43aff3c36a70dac71c81`  
		Last Modified: Tue, 12 Nov 2024 02:10:40 GMT  
		Size: 2.8 MB (2783409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d45dd1da0d87982fe79f5a2e2bdc7af8588698aea8fa74f3f83f496f0c15d2`  
		Last Modified: Tue, 12 Nov 2024 02:10:40 GMT  
		Size: 4.0 KB (3990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03891019e7e35efcb8b92d412d7acab757c3e9fedf32f13e8bc56607d2e8daf5`  
		Last Modified: Tue, 12 Nov 2024 02:10:41 GMT  
		Size: 68.0 MB (67980582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c0d9dce51b044b36e9780718734c763bf5c5e3a0ddee9a9330a09da414785a`  
		Last Modified: Tue, 12 Nov 2024 02:10:40 GMT  
		Size: 901.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.1` - unknown; unknown

```console
$ docker pull emqx@sha256:43e0f4008c0f502200e2edb1810610b062ecd5cb04d43c36bd3f421004572b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2903528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3290d67a8dfba7b0f14fbab456f77a759cf83d2ac920f68d25d1160fe76be2bc`

```dockerfile
```

-	Layers:
	-	`sha256:e8f728b72faa8db7e34a479301b2e1ebc3580c30b1729137e6f9365109f91d9f`  
		Last Modified: Tue, 12 Nov 2024 02:10:40 GMT  
		Size: 2.9 MB (2888188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0863ad8704166df43864f506c2942c53a492fe2bdbf22df7e5ef172465ac3509`  
		Last Modified: Tue, 12 Nov 2024 02:10:40 GMT  
		Size: 15.3 KB (15340 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:d6f7526d815e6265ba0564715236d94ec988434346f13a491a004266f3776a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92516340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e366e035523aca7960f92e900bd1a4120d9d30be51f39b9d3403cf3084ae3eec`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 05 Sep 2023 13:05:03 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
CMD ["bash"]
# Tue, 05 Sep 2023 13:05:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx; # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 05 Sep 2023 13:05:03 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 05 Sep 2023 13:05:03 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 05 Sep 2023 13:05:03 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 05 Sep 2023 13:05:03 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
WORKDIR /opt/emqx
# Tue, 05 Sep 2023 13:05:03 GMT
USER emqx
# Tue, 05 Sep 2023 13:05:03 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 05 Sep 2023 13:05:03 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 05 Sep 2023 13:05:03 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 05 Sep 2023 13:05:03 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13365d1c8260326a4a5c8b311ebe4b31014213a22432c27bb80ce0d93d6dbc4d`  
		Last Modified: Tue, 12 Nov 2024 02:36:31 GMT  
		Size: 2.8 MB (2799477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a63451378ea6c4afe39cdd3b88aa4a726cbbbe9d0294406135302a65e8f7f3`  
		Last Modified: Tue, 12 Nov 2024 02:36:30 GMT  
		Size: 4.0 KB (3993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdc4709307be3ffe23cf4ef41c3d064e8c4f2aa8632209f046b4faea920be47`  
		Last Modified: Tue, 12 Nov 2024 02:36:36 GMT  
		Size: 59.6 MB (59620339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deadc2716054a0d6901c8e279caf86a964b89fc29bb534114243df8ce3a0b78e`  
		Last Modified: Tue, 12 Nov 2024 02:36:30 GMT  
		Size: 899.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.1` - unknown; unknown

```console
$ docker pull emqx@sha256:318100bfaf70c6b660fda8b61a61309a4f2387373a2fabf78e853e1aa7cdff9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2903885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a513a6ece27dfea7a3b4b85a85788725d2b7b6b735e857b6cbdb47d4585682f5`

```dockerfile
```

-	Layers:
	-	`sha256:e315e801f7455508d7569cc7e91f4f5f68689029ba1ab4029a9513525bd87791`  
		Last Modified: Tue, 12 Nov 2024 02:36:30 GMT  
		Size: 2.9 MB (2888435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a2fd9343a1ca3cc8016f7418e4dc0ea3d99305929e3011485d9ca6056d5600b`  
		Last Modified: Tue, 12 Nov 2024 02:36:30 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.1.6`

```console
$ docker pull emqx@sha256:a910f06d2fcd50fecd3750e8002fd229695f19a72e6fd95efffad51ce13dd919
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.1.6` - linux; amd64

```console
$ docker pull emqx@sha256:fa95753e56e6d92a0bcff761bee646e94d1c8420525a8c93224f9c68b744f0c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.2 MB (102220475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38984fdf8596d80fbe3ae818ad966b6f6c880ca565f829b52eb18f6068f07077`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 05 Sep 2023 13:05:03 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
CMD ["bash"]
# Tue, 05 Sep 2023 13:05:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx; # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 05 Sep 2023 13:05:03 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 05 Sep 2023 13:05:03 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 05 Sep 2023 13:05:03 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 05 Sep 2023 13:05:03 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
WORKDIR /opt/emqx
# Tue, 05 Sep 2023 13:05:03 GMT
USER emqx
# Tue, 05 Sep 2023 13:05:03 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 05 Sep 2023 13:05:03 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 05 Sep 2023 13:05:03 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 05 Sep 2023 13:05:03 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe262f411763046f03e7cb5b5edc64fe69085bf0a4a43aff3c36a70dac71c81`  
		Last Modified: Tue, 12 Nov 2024 02:10:40 GMT  
		Size: 2.8 MB (2783409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d45dd1da0d87982fe79f5a2e2bdc7af8588698aea8fa74f3f83f496f0c15d2`  
		Last Modified: Tue, 12 Nov 2024 02:10:40 GMT  
		Size: 4.0 KB (3990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03891019e7e35efcb8b92d412d7acab757c3e9fedf32f13e8bc56607d2e8daf5`  
		Last Modified: Tue, 12 Nov 2024 02:10:41 GMT  
		Size: 68.0 MB (67980582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c0d9dce51b044b36e9780718734c763bf5c5e3a0ddee9a9330a09da414785a`  
		Last Modified: Tue, 12 Nov 2024 02:10:40 GMT  
		Size: 901.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.1.6` - unknown; unknown

```console
$ docker pull emqx@sha256:43e0f4008c0f502200e2edb1810610b062ecd5cb04d43c36bd3f421004572b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2903528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3290d67a8dfba7b0f14fbab456f77a759cf83d2ac920f68d25d1160fe76be2bc`

```dockerfile
```

-	Layers:
	-	`sha256:e8f728b72faa8db7e34a479301b2e1ebc3580c30b1729137e6f9365109f91d9f`  
		Last Modified: Tue, 12 Nov 2024 02:10:40 GMT  
		Size: 2.9 MB (2888188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0863ad8704166df43864f506c2942c53a492fe2bdbf22df7e5ef172465ac3509`  
		Last Modified: Tue, 12 Nov 2024 02:10:40 GMT  
		Size: 15.3 KB (15340 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.1.6` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:d6f7526d815e6265ba0564715236d94ec988434346f13a491a004266f3776a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92516340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e366e035523aca7960f92e900bd1a4120d9d30be51f39b9d3403cf3084ae3eec`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 05 Sep 2023 13:05:03 GMT
ADD rootfs.tar.xz / # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
CMD ["bash"]
# Tue, 05 Sep 2023 13:05:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx; # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 05 Sep 2023 13:05:03 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 05 Sep 2023 13:05:03 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 05 Sep 2023 13:05:03 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 05 Sep 2023 13:05:03 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
WORKDIR /opt/emqx
# Tue, 05 Sep 2023 13:05:03 GMT
USER emqx
# Tue, 05 Sep 2023 13:05:03 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 05 Sep 2023 13:05:03 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 05 Sep 2023 13:05:03 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 05 Sep 2023 13:05:03 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 05 Sep 2023 13:05:03 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13365d1c8260326a4a5c8b311ebe4b31014213a22432c27bb80ce0d93d6dbc4d`  
		Last Modified: Tue, 12 Nov 2024 02:36:31 GMT  
		Size: 2.8 MB (2799477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a63451378ea6c4afe39cdd3b88aa4a726cbbbe9d0294406135302a65e8f7f3`  
		Last Modified: Tue, 12 Nov 2024 02:36:30 GMT  
		Size: 4.0 KB (3993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdc4709307be3ffe23cf4ef41c3d064e8c4f2aa8632209f046b4faea920be47`  
		Last Modified: Tue, 12 Nov 2024 02:36:36 GMT  
		Size: 59.6 MB (59620339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deadc2716054a0d6901c8e279caf86a964b89fc29bb534114243df8ce3a0b78e`  
		Last Modified: Tue, 12 Nov 2024 02:36:30 GMT  
		Size: 899.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.1.6` - unknown; unknown

```console
$ docker pull emqx@sha256:318100bfaf70c6b660fda8b61a61309a4f2387373a2fabf78e853e1aa7cdff9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2903885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a513a6ece27dfea7a3b4b85a85788725d2b7b6b735e857b6cbdb47d4585682f5`

```dockerfile
```

-	Layers:
	-	`sha256:e315e801f7455508d7569cc7e91f4f5f68689029ba1ab4029a9513525bd87791`  
		Last Modified: Tue, 12 Nov 2024 02:36:30 GMT  
		Size: 2.9 MB (2888435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a2fd9343a1ca3cc8016f7418e4dc0ea3d99305929e3011485d9ca6056d5600b`  
		Last Modified: Tue, 12 Nov 2024 02:36:30 GMT  
		Size: 15.4 KB (15450 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.2`

```console
$ docker pull emqx@sha256:cb28977d5bb0e9b72a897116ceee0de923302092e4a038c22e2863f8553801b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.2` - linux; amd64

```console
$ docker pull emqx@sha256:4b4f1170ccfd1f165ccdfda91c397d9eded306027882658f5e5325502e4508c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.8 MB (100774714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8ccbc15b91e8356489482489737c88e5d9b6184118271ae17a3b147f870049`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 25 Sep 2023 09:53:58 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
CMD ["bash"]
# Mon, 25 Sep 2023 09:53:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx; # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
ENV EMQX_VERSION=5.2.1
# Mon, 25 Sep 2023 09:53:58 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Mon, 25 Sep 2023 09:53:58 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Mon, 25 Sep 2023 09:53:58 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 25 Sep 2023 09:53:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
WORKDIR /opt/emqx
# Mon, 25 Sep 2023 09:53:58 GMT
USER emqx
# Mon, 25 Sep 2023 09:53:58 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 25 Sep 2023 09:53:58 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 25 Sep 2023 09:53:58 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 25 Sep 2023 09:53:58 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428b970105e944635a3cd4c16ac06795925563715826d3120d5e62f24dd8b1cf`  
		Last Modified: Tue, 12 Nov 2024 02:12:41 GMT  
		Size: 1.4 MB (1424446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975a1341c7b7788042c2c9e4bc30f6a34ef5afeeb0665a8bcb07dac736d6ea2e`  
		Last Modified: Tue, 12 Nov 2024 02:12:41 GMT  
		Size: 4.0 KB (3991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070c82d7ed36127e9d0ff6ecb92e1b595a87f105e00e50f4b178b09ac5fc6612`  
		Last Modified: Tue, 12 Nov 2024 02:12:42 GMT  
		Size: 67.9 MB (67893785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ddbc1cc95a97f00b27e944a314f6ba99fdd731354aea36fdba36c2dffe6f1d`  
		Last Modified: Tue, 12 Nov 2024 02:12:41 GMT  
		Size: 899.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.2` - unknown; unknown

```console
$ docker pull emqx@sha256:91e590a45d791bace507ca47b9f8ceecc5ccd595bea5b6f1943487b4d783d65e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2847150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c078df80017f0f78023fd6d7200193f25785f2fa7ce3d03645d2894f35f296`

```dockerfile
```

-	Layers:
	-	`sha256:ed75388ccc9ed575e0c2d8354443c1c70046f4d61c39d0a671667bc51cf29665`  
		Last Modified: Tue, 12 Nov 2024 02:12:41 GMT  
		Size: 2.8 MB (2831308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59b1f18d01dc1c0c8d2f933b4a63e6a038c4f8014bfd2b47c8b9ee3b79ebb8c9`  
		Last Modified: Tue, 12 Nov 2024 02:12:41 GMT  
		Size: 15.8 KB (15842 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:011af9a242ba200cb2ab38ed44f566415965271a2b1fb261c39397db0566a345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91072372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dbd9e915b37b17f1bd515f44b7ed6f29854f55a80c06d7bc5e2b9400674333e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 25 Sep 2023 09:53:58 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
CMD ["bash"]
# Mon, 25 Sep 2023 09:53:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx; # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
ENV EMQX_VERSION=5.2.1
# Mon, 25 Sep 2023 09:53:58 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Mon, 25 Sep 2023 09:53:58 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Mon, 25 Sep 2023 09:53:58 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 25 Sep 2023 09:53:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
WORKDIR /opt/emqx
# Mon, 25 Sep 2023 09:53:58 GMT
USER emqx
# Mon, 25 Sep 2023 09:53:58 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 25 Sep 2023 09:53:58 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 25 Sep 2023 09:53:58 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 25 Sep 2023 09:53:58 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970e68f674111ab1ca1300ba730483f6f02491bc0edc6c8e31151ac9b1598a3d`  
		Last Modified: Tue, 12 Nov 2024 02:37:20 GMT  
		Size: 1.4 MB (1438714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffa0abe444a277eaca04b53ee843c4dff12bc55dd16a25c14d1a5ec1bc8a773`  
		Last Modified: Tue, 12 Nov 2024 02:37:20 GMT  
		Size: 4.0 KB (3989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f096c7cbed8175f39218fd73fca431ccc072da9b79e894025af8d241d0c10ef3`  
		Last Modified: Tue, 12 Nov 2024 02:37:22 GMT  
		Size: 59.5 MB (59537139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fdf0dd19c16dfcddcb9ee85af9bd34c537c4cb6e82bc84553e3da6712c6899`  
		Last Modified: Tue, 12 Nov 2024 02:37:20 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.2` - unknown; unknown

```console
$ docker pull emqx@sha256:20319f9ccc39ed7ee2b5062e24c3f5073e96cbf26ab579d101010d02ce3d1bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2847494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ba2c2f6fd7b823db373be4ad4febb2aec020966c263fcf58299f3051dd3f6b`

```dockerfile
```

-	Layers:
	-	`sha256:8f859ca08ccd2e046f088b7ba36e26e7b65945a462f211f91ad1fe2b11a1943a`  
		Last Modified: Tue, 12 Nov 2024 02:37:20 GMT  
		Size: 2.8 MB (2831543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d2bc12f806421c63852aaab525a4dd11d8a421e9dcf8c7931c4b54b997b954c`  
		Last Modified: Tue, 12 Nov 2024 02:37:20 GMT  
		Size: 16.0 KB (15951 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.2.1`

```console
$ docker pull emqx@sha256:cb28977d5bb0e9b72a897116ceee0de923302092e4a038c22e2863f8553801b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.2.1` - linux; amd64

```console
$ docker pull emqx@sha256:4b4f1170ccfd1f165ccdfda91c397d9eded306027882658f5e5325502e4508c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.8 MB (100774714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8ccbc15b91e8356489482489737c88e5d9b6184118271ae17a3b147f870049`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 25 Sep 2023 09:53:58 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
CMD ["bash"]
# Mon, 25 Sep 2023 09:53:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx; # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
ENV EMQX_VERSION=5.2.1
# Mon, 25 Sep 2023 09:53:58 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Mon, 25 Sep 2023 09:53:58 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Mon, 25 Sep 2023 09:53:58 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 25 Sep 2023 09:53:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
WORKDIR /opt/emqx
# Mon, 25 Sep 2023 09:53:58 GMT
USER emqx
# Mon, 25 Sep 2023 09:53:58 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 25 Sep 2023 09:53:58 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 25 Sep 2023 09:53:58 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 25 Sep 2023 09:53:58 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428b970105e944635a3cd4c16ac06795925563715826d3120d5e62f24dd8b1cf`  
		Last Modified: Tue, 12 Nov 2024 02:12:41 GMT  
		Size: 1.4 MB (1424446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975a1341c7b7788042c2c9e4bc30f6a34ef5afeeb0665a8bcb07dac736d6ea2e`  
		Last Modified: Tue, 12 Nov 2024 02:12:41 GMT  
		Size: 4.0 KB (3991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070c82d7ed36127e9d0ff6ecb92e1b595a87f105e00e50f4b178b09ac5fc6612`  
		Last Modified: Tue, 12 Nov 2024 02:12:42 GMT  
		Size: 67.9 MB (67893785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ddbc1cc95a97f00b27e944a314f6ba99fdd731354aea36fdba36c2dffe6f1d`  
		Last Modified: Tue, 12 Nov 2024 02:12:41 GMT  
		Size: 899.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.2.1` - unknown; unknown

```console
$ docker pull emqx@sha256:91e590a45d791bace507ca47b9f8ceecc5ccd595bea5b6f1943487b4d783d65e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2847150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8c078df80017f0f78023fd6d7200193f25785f2fa7ce3d03645d2894f35f296`

```dockerfile
```

-	Layers:
	-	`sha256:ed75388ccc9ed575e0c2d8354443c1c70046f4d61c39d0a671667bc51cf29665`  
		Last Modified: Tue, 12 Nov 2024 02:12:41 GMT  
		Size: 2.8 MB (2831308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59b1f18d01dc1c0c8d2f933b4a63e6a038c4f8014bfd2b47c8b9ee3b79ebb8c9`  
		Last Modified: Tue, 12 Nov 2024 02:12:41 GMT  
		Size: 15.8 KB (15842 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.2.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:011af9a242ba200cb2ab38ed44f566415965271a2b1fb261c39397db0566a345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.1 MB (91072372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dbd9e915b37b17f1bd515f44b7ed6f29854f55a80c06d7bc5e2b9400674333e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 25 Sep 2023 09:53:58 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
CMD ["bash"]
# Mon, 25 Sep 2023 09:53:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx; # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
ENV EMQX_VERSION=5.2.1
# Mon, 25 Sep 2023 09:53:58 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Mon, 25 Sep 2023 09:53:58 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Mon, 25 Sep 2023 09:53:58 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 25 Sep 2023 09:53:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
WORKDIR /opt/emqx
# Mon, 25 Sep 2023 09:53:58 GMT
USER emqx
# Mon, 25 Sep 2023 09:53:58 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 25 Sep 2023 09:53:58 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 25 Sep 2023 09:53:58 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 25 Sep 2023 09:53:58 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 25 Sep 2023 09:53:58 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970e68f674111ab1ca1300ba730483f6f02491bc0edc6c8e31151ac9b1598a3d`  
		Last Modified: Tue, 12 Nov 2024 02:37:20 GMT  
		Size: 1.4 MB (1438714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ffa0abe444a277eaca04b53ee843c4dff12bc55dd16a25c14d1a5ec1bc8a773`  
		Last Modified: Tue, 12 Nov 2024 02:37:20 GMT  
		Size: 4.0 KB (3989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f096c7cbed8175f39218fd73fca431ccc072da9b79e894025af8d241d0c10ef3`  
		Last Modified: Tue, 12 Nov 2024 02:37:22 GMT  
		Size: 59.5 MB (59537139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fdf0dd19c16dfcddcb9ee85af9bd34c537c4cb6e82bc84553e3da6712c6899`  
		Last Modified: Tue, 12 Nov 2024 02:37:20 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.2.1` - unknown; unknown

```console
$ docker pull emqx@sha256:20319f9ccc39ed7ee2b5062e24c3f5073e96cbf26ab579d101010d02ce3d1bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2847494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ba2c2f6fd7b823db373be4ad4febb2aec020966c263fcf58299f3051dd3f6b`

```dockerfile
```

-	Layers:
	-	`sha256:8f859ca08ccd2e046f088b7ba36e26e7b65945a462f211f91ad1fe2b11a1943a`  
		Last Modified: Tue, 12 Nov 2024 02:37:20 GMT  
		Size: 2.8 MB (2831543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d2bc12f806421c63852aaab525a4dd11d8a421e9dcf8c7931c4b54b997b954c`  
		Last Modified: Tue, 12 Nov 2024 02:37:20 GMT  
		Size: 16.0 KB (15951 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.3`

```console
$ docker pull emqx@sha256:a161880a9b9260f16bd5d22a1341c00fc3494a2abfe0cd5e6c433f6641be3664
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.3` - linux; amd64

```console
$ docker pull emqx@sha256:708c43f17368ef960beaa76f7fbff9e97e82f6e9a6897066ce4b90ebfd860c8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 MB (101608143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ccecd97dae8467cca0ee7ba3d118be7b194c04c799cf5562f4399112147817`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 01 Dec 2023 10:27:11 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
CMD ["bash"]
# Fri, 01 Dec 2023 10:27:11 GMT
ENV EMQX_VERSION=5.3.2
# Fri, 01 Dec 2023 10:27:11 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Fri, 01 Dec 2023 10:27:11 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Fri, 01 Dec 2023 10:27:11 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 01 Dec 2023 10:27:11 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
WORKDIR /opt/emqx
# Fri, 01 Dec 2023 10:27:11 GMT
USER emqx
# Fri, 01 Dec 2023 10:27:11 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 01 Dec 2023 10:27:11 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 01 Dec 2023 10:27:11 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 01 Dec 2023 10:27:11 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33adcb2ec591b6dfd0bd044ff184431e4a900ed6ab9b6b20b52e19106530ce34`  
		Last Modified: Tue, 12 Nov 2024 02:12:44 GMT  
		Size: 70.2 MB (70155650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6aa3324dc0a28807a6074567caa3e84e39c712553c645111ead39daaef22b29`  
		Last Modified: Tue, 12 Nov 2024 02:12:43 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.3` - unknown; unknown

```console
$ docker pull emqx@sha256:f1eb7b7fc96b4e83dae5bc2eedd16902ed8147b8f404d82d1560d6d3ae1bddb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2856493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64dc6f0f7e4381323e989917849905a04eb290434e2bedca952514658d4bf26e`

```dockerfile
```

-	Layers:
	-	`sha256:e6339c0b357d150f6bf5d7260537130c98f7444683102ed633d851ff54cd2c86`  
		Last Modified: Tue, 12 Nov 2024 02:12:43 GMT  
		Size: 2.8 MB (2843711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b59d674a2f890a4436393425947e1ae545d5f0e6248965d0131c70fe5cef71d`  
		Last Modified: Tue, 12 Nov 2024 02:12:43 GMT  
		Size: 12.8 KB (12782 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.3` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:3dad2ec727aefe47468bd7b24e107753ad2c741908e75a24dcb4f6e0f02269f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91897678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c55cc86bfc51ffa0d279b94f9dc3513cca45895fed7f1a8cae66d36f471b284b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 01 Dec 2023 10:27:11 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
CMD ["bash"]
# Fri, 01 Dec 2023 10:27:11 GMT
ENV EMQX_VERSION=5.3.2
# Fri, 01 Dec 2023 10:27:11 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Fri, 01 Dec 2023 10:27:11 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Fri, 01 Dec 2023 10:27:11 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 01 Dec 2023 10:27:11 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
WORKDIR /opt/emqx
# Fri, 01 Dec 2023 10:27:11 GMT
USER emqx
# Fri, 01 Dec 2023 10:27:11 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 01 Dec 2023 10:27:11 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 01 Dec 2023 10:27:11 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 01 Dec 2023 10:27:11 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fa904ff48b0b26f2aa4dca1c2da2247fc37da4f41ad94b96770bfd60772901`  
		Last Modified: Tue, 12 Nov 2024 02:37:58 GMT  
		Size: 61.8 MB (61805147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e806a0f4dd4aa9839c86db7368977cdeca8232eb79452b8ffe55bcb5f37e321c`  
		Last Modified: Tue, 12 Nov 2024 02:37:56 GMT  
		Size: 899.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.3` - unknown; unknown

```console
$ docker pull emqx@sha256:599a4a0d5707684eb1cbf2cdd13f5c8718e4296dcded4e09abefb03615e1afa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2856809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1358574f8ae2cad3e1dc61f6987f6f001d70970836c004ce1d35ff188312ace8`

```dockerfile
```

-	Layers:
	-	`sha256:93aa3744c6a0cdc54ccc627cc596f8f51bdf503f98d77710d580961f030d1a83`  
		Last Modified: Tue, 12 Nov 2024 02:37:56 GMT  
		Size: 2.8 MB (2843946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb70271779b0bca3a6358b65651d47d1182d8862f578b8fd46a5a68e511ca2df`  
		Last Modified: Tue, 12 Nov 2024 02:37:55 GMT  
		Size: 12.9 KB (12863 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.3.2`

```console
$ docker pull emqx@sha256:a161880a9b9260f16bd5d22a1341c00fc3494a2abfe0cd5e6c433f6641be3664
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.3.2` - linux; amd64

```console
$ docker pull emqx@sha256:708c43f17368ef960beaa76f7fbff9e97e82f6e9a6897066ce4b90ebfd860c8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 MB (101608143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62ccecd97dae8467cca0ee7ba3d118be7b194c04c799cf5562f4399112147817`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 01 Dec 2023 10:27:11 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
CMD ["bash"]
# Fri, 01 Dec 2023 10:27:11 GMT
ENV EMQX_VERSION=5.3.2
# Fri, 01 Dec 2023 10:27:11 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Fri, 01 Dec 2023 10:27:11 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Fri, 01 Dec 2023 10:27:11 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 01 Dec 2023 10:27:11 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
WORKDIR /opt/emqx
# Fri, 01 Dec 2023 10:27:11 GMT
USER emqx
# Fri, 01 Dec 2023 10:27:11 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 01 Dec 2023 10:27:11 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 01 Dec 2023 10:27:11 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 01 Dec 2023 10:27:11 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33adcb2ec591b6dfd0bd044ff184431e4a900ed6ab9b6b20b52e19106530ce34`  
		Last Modified: Tue, 12 Nov 2024 02:12:44 GMT  
		Size: 70.2 MB (70155650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6aa3324dc0a28807a6074567caa3e84e39c712553c645111ead39daaef22b29`  
		Last Modified: Tue, 12 Nov 2024 02:12:43 GMT  
		Size: 900.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.3.2` - unknown; unknown

```console
$ docker pull emqx@sha256:f1eb7b7fc96b4e83dae5bc2eedd16902ed8147b8f404d82d1560d6d3ae1bddb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2856493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64dc6f0f7e4381323e989917849905a04eb290434e2bedca952514658d4bf26e`

```dockerfile
```

-	Layers:
	-	`sha256:e6339c0b357d150f6bf5d7260537130c98f7444683102ed633d851ff54cd2c86`  
		Last Modified: Tue, 12 Nov 2024 02:12:43 GMT  
		Size: 2.8 MB (2843711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b59d674a2f890a4436393425947e1ae545d5f0e6248965d0131c70fe5cef71d`  
		Last Modified: Tue, 12 Nov 2024 02:12:43 GMT  
		Size: 12.8 KB (12782 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.3.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:3dad2ec727aefe47468bd7b24e107753ad2c741908e75a24dcb4f6e0f02269f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.9 MB (91897678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c55cc86bfc51ffa0d279b94f9dc3513cca45895fed7f1a8cae66d36f471b284b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 01 Dec 2023 10:27:11 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
CMD ["bash"]
# Fri, 01 Dec 2023 10:27:11 GMT
ENV EMQX_VERSION=5.3.2
# Fri, 01 Dec 2023 10:27:11 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Fri, 01 Dec 2023 10:27:11 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Fri, 01 Dec 2023 10:27:11 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 01 Dec 2023 10:27:11 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
WORKDIR /opt/emqx
# Fri, 01 Dec 2023 10:27:11 GMT
USER emqx
# Fri, 01 Dec 2023 10:27:11 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 01 Dec 2023 10:27:11 GMT
EXPOSE map[11883/tcp:{} 18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 01 Dec 2023 10:27:11 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 01 Dec 2023 10:27:11 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 01 Dec 2023 10:27:11 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fa904ff48b0b26f2aa4dca1c2da2247fc37da4f41ad94b96770bfd60772901`  
		Last Modified: Tue, 12 Nov 2024 02:37:58 GMT  
		Size: 61.8 MB (61805147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e806a0f4dd4aa9839c86db7368977cdeca8232eb79452b8ffe55bcb5f37e321c`  
		Last Modified: Tue, 12 Nov 2024 02:37:56 GMT  
		Size: 899.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.3.2` - unknown; unknown

```console
$ docker pull emqx@sha256:599a4a0d5707684eb1cbf2cdd13f5c8718e4296dcded4e09abefb03615e1afa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2856809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1358574f8ae2cad3e1dc61f6987f6f001d70970836c004ce1d35ff188312ace8`

```dockerfile
```

-	Layers:
	-	`sha256:93aa3744c6a0cdc54ccc627cc596f8f51bdf503f98d77710d580961f030d1a83`  
		Last Modified: Tue, 12 Nov 2024 02:37:56 GMT  
		Size: 2.8 MB (2843946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb70271779b0bca3a6358b65651d47d1182d8862f578b8fd46a5a68e511ca2df`  
		Last Modified: Tue, 12 Nov 2024 02:37:55 GMT  
		Size: 12.9 KB (12863 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.4`

```console
$ docker pull emqx@sha256:4df2381df8d36e414be9e398f1f23a27a6e5a50a2ea4c84e61e7576c741d79ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.4` - linux; amd64

```console
$ docker pull emqx@sha256:88ad93fd8fb9e8700aed30741ba12255c92960254681ab8b5f6bfeb2ea40d4f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118521397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c78169d46ceb38af785f38ca4fc1f099461019305af05d80f2b18ae3c7e9ef`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 12 Jan 2024 14:13:45 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 14:13:45 GMT
ENV EMQX_VERSION=5.4.1
# Fri, 12 Jan 2024 14:13:45 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Fri, 12 Jan 2024 14:13:45 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Fri, 12 Jan 2024 14:13:45 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 12 Jan 2024 14:13:45 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
WORKDIR /opt/emqx
# Fri, 12 Jan 2024 14:13:45 GMT
USER emqx
# Fri, 12 Jan 2024 14:13:45 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 12 Jan 2024 14:13:45 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 12 Jan 2024 14:13:45 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 12 Jan 2024 14:13:45 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86030722d78d880b7bb09bd34f18dd071fd3e9ffc81c08d398b4c6100f29ff3`  
		Last Modified: Tue, 12 Nov 2024 02:12:47 GMT  
		Size: 87.1 MB (87068906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd546ae3d9463757401d01eab4cd199cf1ee6b9b06e1e8a2a03b5d576f61301`  
		Last Modified: Tue, 12 Nov 2024 02:12:45 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.4` - unknown; unknown

```console
$ docker pull emqx@sha256:df288192346dcbab203c22e5060e5249ba33014c400fdf8ece6aebb6e3314096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2849127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b613ffd41402c57189bd283e0fe567b4ed226d14567d687b5a9b56e60fc29dbb`

```dockerfile
```

-	Layers:
	-	`sha256:a76af073583a9d30c3a88e3790763ef486426282cb452518f0b04cf151f04543`  
		Last Modified: Tue, 12 Nov 2024 02:12:46 GMT  
		Size: 2.8 MB (2836400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b9203a9e971c502bbba16b56f7fe8f48a875dfa7ebe255b6ba143517aeeefd8`  
		Last Modified: Tue, 12 Nov 2024 02:12:46 GMT  
		Size: 12.7 KB (12727 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:e51213eff75476eb9b18e264fad8c7bd126083a644e6f8e0066468334a50aeb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108297086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6792e7931173947c60141de82106cd7c17d210868a44eae20886b32dfd140eb5`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 12 Jan 2024 14:13:45 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 14:13:45 GMT
ENV EMQX_VERSION=5.4.1
# Fri, 12 Jan 2024 14:13:45 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Fri, 12 Jan 2024 14:13:45 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Fri, 12 Jan 2024 14:13:45 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 12 Jan 2024 14:13:45 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
WORKDIR /opt/emqx
# Fri, 12 Jan 2024 14:13:45 GMT
USER emqx
# Fri, 12 Jan 2024 14:13:45 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 12 Jan 2024 14:13:45 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 12 Jan 2024 14:13:45 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 12 Jan 2024 14:13:45 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e642083b3de87c9921a49629e9aaf8bdab470c093564d20646e5514b9685eed`  
		Last Modified: Tue, 12 Nov 2024 02:38:38 GMT  
		Size: 78.2 MB (78204555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728c4903ccc130f186605a0742c63145943a4ebe1e42f37ed1117b6becb6fe0b`  
		Last Modified: Tue, 12 Nov 2024 02:38:36 GMT  
		Size: 899.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.4` - unknown; unknown

```console
$ docker pull emqx@sha256:626c634bf6d26603550d534174fdef1381ddba924dc5e832ab52264ed3ab4efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2849442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b65d8aa253ccadd2ceaf2ed809ee00cb6790662e7b43f78870cf39072f525ac`

```dockerfile
```

-	Layers:
	-	`sha256:c96c48b2d5aef0a47ecf11c563e8a97239206df540ca3ff8f0f8cc3db3dedb06`  
		Last Modified: Tue, 12 Nov 2024 02:38:36 GMT  
		Size: 2.8 MB (2836635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fee380fc0c39c34d4a675c4b0175596aa0a8522cf7b85b922aff4b1f1ae8ce90`  
		Last Modified: Tue, 12 Nov 2024 02:38:36 GMT  
		Size: 12.8 KB (12807 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.4.1`

```console
$ docker pull emqx@sha256:4df2381df8d36e414be9e398f1f23a27a6e5a50a2ea4c84e61e7576c741d79ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.4.1` - linux; amd64

```console
$ docker pull emqx@sha256:88ad93fd8fb9e8700aed30741ba12255c92960254681ab8b5f6bfeb2ea40d4f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.5 MB (118521397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c78169d46ceb38af785f38ca4fc1f099461019305af05d80f2b18ae3c7e9ef`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 12 Jan 2024 14:13:45 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 14:13:45 GMT
ENV EMQX_VERSION=5.4.1
# Fri, 12 Jan 2024 14:13:45 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Fri, 12 Jan 2024 14:13:45 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Fri, 12 Jan 2024 14:13:45 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 12 Jan 2024 14:13:45 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
WORKDIR /opt/emqx
# Fri, 12 Jan 2024 14:13:45 GMT
USER emqx
# Fri, 12 Jan 2024 14:13:45 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 12 Jan 2024 14:13:45 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 12 Jan 2024 14:13:45 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 12 Jan 2024 14:13:45 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86030722d78d880b7bb09bd34f18dd071fd3e9ffc81c08d398b4c6100f29ff3`  
		Last Modified: Tue, 12 Nov 2024 02:12:47 GMT  
		Size: 87.1 MB (87068906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd546ae3d9463757401d01eab4cd199cf1ee6b9b06e1e8a2a03b5d576f61301`  
		Last Modified: Tue, 12 Nov 2024 02:12:45 GMT  
		Size: 898.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.4.1` - unknown; unknown

```console
$ docker pull emqx@sha256:df288192346dcbab203c22e5060e5249ba33014c400fdf8ece6aebb6e3314096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2849127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b613ffd41402c57189bd283e0fe567b4ed226d14567d687b5a9b56e60fc29dbb`

```dockerfile
```

-	Layers:
	-	`sha256:a76af073583a9d30c3a88e3790763ef486426282cb452518f0b04cf151f04543`  
		Last Modified: Tue, 12 Nov 2024 02:12:46 GMT  
		Size: 2.8 MB (2836400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b9203a9e971c502bbba16b56f7fe8f48a875dfa7ebe255b6ba143517aeeefd8`  
		Last Modified: Tue, 12 Nov 2024 02:12:46 GMT  
		Size: 12.7 KB (12727 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.4.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:e51213eff75476eb9b18e264fad8c7bd126083a644e6f8e0066468334a50aeb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.3 MB (108297086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6792e7931173947c60141de82106cd7c17d210868a44eae20886b32dfd140eb5`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Fri, 12 Jan 2024 14:13:45 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 14:13:45 GMT
ENV EMQX_VERSION=5.4.1
# Fri, 12 Jan 2024 14:13:45 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Fri, 12 Jan 2024 14:13:45 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Fri, 12 Jan 2024 14:13:45 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Fri, 12 Jan 2024 14:13:45 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
WORKDIR /opt/emqx
# Fri, 12 Jan 2024 14:13:45 GMT
USER emqx
# Fri, 12 Jan 2024 14:13:45 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Fri, 12 Jan 2024 14:13:45 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Fri, 12 Jan 2024 14:13:45 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Fri, 12 Jan 2024 14:13:45 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Fri, 12 Jan 2024 14:13:45 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e642083b3de87c9921a49629e9aaf8bdab470c093564d20646e5514b9685eed`  
		Last Modified: Tue, 12 Nov 2024 02:38:38 GMT  
		Size: 78.2 MB (78204555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728c4903ccc130f186605a0742c63145943a4ebe1e42f37ed1117b6becb6fe0b`  
		Last Modified: Tue, 12 Nov 2024 02:38:36 GMT  
		Size: 899.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.4.1` - unknown; unknown

```console
$ docker pull emqx@sha256:626c634bf6d26603550d534174fdef1381ddba924dc5e832ab52264ed3ab4efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2849442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b65d8aa253ccadd2ceaf2ed809ee00cb6790662e7b43f78870cf39072f525ac`

```dockerfile
```

-	Layers:
	-	`sha256:c96c48b2d5aef0a47ecf11c563e8a97239206df540ca3ff8f0f8cc3db3dedb06`  
		Last Modified: Tue, 12 Nov 2024 02:38:36 GMT  
		Size: 2.8 MB (2836635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fee380fc0c39c34d4a675c4b0175596aa0a8522cf7b85b922aff4b1f1ae8ce90`  
		Last Modified: Tue, 12 Nov 2024 02:38:36 GMT  
		Size: 12.8 KB (12807 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.5`

```console
$ docker pull emqx@sha256:8f88a3e43ebf54d024c972d8b706c1803128769669e1a4406b98d80d7a13e2b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.5` - linux; amd64

```console
$ docker pull emqx@sha256:5f653aed5e6a7406bb3ce68e999da15ffd968273a61b0247ba3daecc72980e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121087557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc693fbcc00ece3aeb7b64f03a4964052fc3e7bcbac048c4b8c8e1aa98d58f0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 03 Apr 2024 12:49:39 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
CMD ["bash"]
# Wed, 03 Apr 2024 12:49:39 GMT
ENV EMQX_VERSION=5.5.1
# Wed, 03 Apr 2024 12:49:39 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Wed, 03 Apr 2024 12:49:39 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Wed, 03 Apr 2024 12:49:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 Apr 2024 12:49:39 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
WORKDIR /opt/emqx
# Wed, 03 Apr 2024 12:49:39 GMT
USER emqx
# Wed, 03 Apr 2024 12:49:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 Apr 2024 12:49:39 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 03 Apr 2024 12:49:39 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 Apr 2024 12:49:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9e03176dbb215eb362377443deb0bb6af76fd40c2c1943024f3e16f6b283ef`  
		Last Modified: Tue, 12 Nov 2024 02:12:57 GMT  
		Size: 89.6 MB (89634934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db1e2b5c34c29f763f5981372f533b2c6c687e45912f7d7a6e6ba9d7a0a674e`  
		Last Modified: Tue, 12 Nov 2024 02:12:55 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.5` - unknown; unknown

```console
$ docker pull emqx@sha256:1c11c97f5378b76179fab5a48c78e9ebe030e9de154f3bfa2ee8305f1e7cf50c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2849190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9907dcad2571565fe2166dde27814c60331ec23f7d2a822fffbd7dc8c1b3b235`

```dockerfile
```

-	Layers:
	-	`sha256:9e2d2f0c44ed23a7224a10cad29fcfbe08f111280be083c2533569af5df7f4cf`  
		Last Modified: Tue, 12 Nov 2024 02:12:56 GMT  
		Size: 2.8 MB (2836361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08d1411b48588b51090e354c5bd6e09457ef42e7644ea61ed86218642a727e81`  
		Last Modified: Tue, 12 Nov 2024 02:12:55 GMT  
		Size: 12.8 KB (12829 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:2ec29148aee28543cb44333868336cd24c0d6e62a6ba49cf6017fab173d9429c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 MB (116595880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12fec08e945fa59c3a4d7dfa50031436d8545b0ad37157926d61e7abe750490c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 03 Apr 2024 12:49:39 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
CMD ["bash"]
# Wed, 03 Apr 2024 12:49:39 GMT
ENV EMQX_VERSION=5.5.1
# Wed, 03 Apr 2024 12:49:39 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Wed, 03 Apr 2024 12:49:39 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Wed, 03 Apr 2024 12:49:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 Apr 2024 12:49:39 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
WORKDIR /opt/emqx
# Wed, 03 Apr 2024 12:49:39 GMT
USER emqx
# Wed, 03 Apr 2024 12:49:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 Apr 2024 12:49:39 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 03 Apr 2024 12:49:39 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 Apr 2024 12:49:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823aa289d8d9cad57eb445bf3b1ac7f0350b900d24a1c01aecb8f5929212a7ca`  
		Last Modified: Tue, 12 Nov 2024 02:39:24 GMT  
		Size: 86.5 MB (86503217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff436e9451433abc61b4c4c0989b0a88b25bdb79c3074da13d558686cf531d8`  
		Last Modified: Tue, 12 Nov 2024 02:39:21 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.5` - unknown; unknown

```console
$ docker pull emqx@sha256:b614e18165be7d98a6ce8e547f53a7ccc6d037b16fa17933eab33e4f3fc524b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2849505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2f4afc57518e5369706b2aaea27e9b4f50bcf0785bb974c22675a13db3469b`

```dockerfile
```

-	Layers:
	-	`sha256:8275dfb4346afd5a41aa32a8b7d5090bf2ded7aa55ea902f950fe06232bffa2b`  
		Last Modified: Tue, 12 Nov 2024 02:39:22 GMT  
		Size: 2.8 MB (2836596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8c768a5d0594dc9514e6f5877e94007eb45edb9ace3555d15fc703c30180e96`  
		Last Modified: Tue, 12 Nov 2024 02:39:22 GMT  
		Size: 12.9 KB (12909 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.5.1`

```console
$ docker pull emqx@sha256:8f88a3e43ebf54d024c972d8b706c1803128769669e1a4406b98d80d7a13e2b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.5.1` - linux; amd64

```console
$ docker pull emqx@sha256:5f653aed5e6a7406bb3ce68e999da15ffd968273a61b0247ba3daecc72980e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.1 MB (121087557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc693fbcc00ece3aeb7b64f03a4964052fc3e7bcbac048c4b8c8e1aa98d58f0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 03 Apr 2024 12:49:39 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
CMD ["bash"]
# Wed, 03 Apr 2024 12:49:39 GMT
ENV EMQX_VERSION=5.5.1
# Wed, 03 Apr 2024 12:49:39 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Wed, 03 Apr 2024 12:49:39 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Wed, 03 Apr 2024 12:49:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 Apr 2024 12:49:39 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
WORKDIR /opt/emqx
# Wed, 03 Apr 2024 12:49:39 GMT
USER emqx
# Wed, 03 Apr 2024 12:49:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 Apr 2024 12:49:39 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 03 Apr 2024 12:49:39 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 Apr 2024 12:49:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9e03176dbb215eb362377443deb0bb6af76fd40c2c1943024f3e16f6b283ef`  
		Last Modified: Tue, 12 Nov 2024 02:12:57 GMT  
		Size: 89.6 MB (89634934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db1e2b5c34c29f763f5981372f533b2c6c687e45912f7d7a6e6ba9d7a0a674e`  
		Last Modified: Tue, 12 Nov 2024 02:12:55 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.5.1` - unknown; unknown

```console
$ docker pull emqx@sha256:1c11c97f5378b76179fab5a48c78e9ebe030e9de154f3bfa2ee8305f1e7cf50c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2849190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9907dcad2571565fe2166dde27814c60331ec23f7d2a822fffbd7dc8c1b3b235`

```dockerfile
```

-	Layers:
	-	`sha256:9e2d2f0c44ed23a7224a10cad29fcfbe08f111280be083c2533569af5df7f4cf`  
		Last Modified: Tue, 12 Nov 2024 02:12:56 GMT  
		Size: 2.8 MB (2836361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08d1411b48588b51090e354c5bd6e09457ef42e7644ea61ed86218642a727e81`  
		Last Modified: Tue, 12 Nov 2024 02:12:55 GMT  
		Size: 12.8 KB (12829 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.5.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:2ec29148aee28543cb44333868336cd24c0d6e62a6ba49cf6017fab173d9429c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.6 MB (116595880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12fec08e945fa59c3a4d7dfa50031436d8545b0ad37157926d61e7abe750490c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 03 Apr 2024 12:49:39 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
CMD ["bash"]
# Wed, 03 Apr 2024 12:49:39 GMT
ENV EMQX_VERSION=5.5.1
# Wed, 03 Apr 2024 12:49:39 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Wed, 03 Apr 2024 12:49:39 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Wed, 03 Apr 2024 12:49:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 Apr 2024 12:49:39 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     mkdir -p /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     chown -R emqx:emqx /opt/emqx/log /opt/emqx/data /opt/emqx/plugins;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
WORKDIR /opt/emqx
# Wed, 03 Apr 2024 12:49:39 GMT
USER emqx
# Wed, 03 Apr 2024 12:49:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 Apr 2024 12:49:39 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Wed, 03 Apr 2024 12:49:39 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Wed, 03 Apr 2024 12:49:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 Apr 2024 12:49:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823aa289d8d9cad57eb445bf3b1ac7f0350b900d24a1c01aecb8f5929212a7ca`  
		Last Modified: Tue, 12 Nov 2024 02:39:24 GMT  
		Size: 86.5 MB (86503217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff436e9451433abc61b4c4c0989b0a88b25bdb79c3074da13d558686cf531d8`  
		Last Modified: Tue, 12 Nov 2024 02:39:21 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.5.1` - unknown; unknown

```console
$ docker pull emqx@sha256:b614e18165be7d98a6ce8e547f53a7ccc6d037b16fa17933eab33e4f3fc524b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2849505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2f4afc57518e5369706b2aaea27e9b4f50bcf0785bb974c22675a13db3469b`

```dockerfile
```

-	Layers:
	-	`sha256:8275dfb4346afd5a41aa32a8b7d5090bf2ded7aa55ea902f950fe06232bffa2b`  
		Last Modified: Tue, 12 Nov 2024 02:39:22 GMT  
		Size: 2.8 MB (2836596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8c768a5d0594dc9514e6f5877e94007eb45edb9ace3555d15fc703c30180e96`  
		Last Modified: Tue, 12 Nov 2024 02:39:22 GMT  
		Size: 12.9 KB (12909 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.6`

```console
$ docker pull emqx@sha256:4e8615238a7e9feb3a6cfaa1d36d15174b984587c12e343273eafb9a8e6fee07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.6` - linux; amd64

```console
$ docker pull emqx@sha256:e37f49ee3c742e76c50c77b85423ecf322e1fb44208e5881ce6bf2b0881be356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124184785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29351f4c416538452dd51c3629e13a2ed3123dc1ec1f2a61c96e60f1cb70787d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 22 Apr 2024 06:31:42 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 06:31:42 GMT
ENV EMQX_VERSION=5.6.1
# Mon, 22 Apr 2024 06:31:42 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Mon, 22 Apr 2024 06:31:42 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Mon, 22 Apr 2024 06:31:42 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 22 Apr 2024 06:31:42 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
WORKDIR /opt/emqx
# Mon, 22 Apr 2024 06:31:42 GMT
USER emqx
# Mon, 22 Apr 2024 06:31:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 22 Apr 2024 06:31:42 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 22 Apr 2024 06:31:42 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 22 Apr 2024 06:31:42 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8c5daed23e495b00531f87295807356f2d94d546d9d6706fc6ab53efb25a37`  
		Last Modified: Tue, 12 Nov 2024 02:13:16 GMT  
		Size: 95.1 MB (95055726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0e9f298813314105c01e19c0dd89ba107f84a92ab2904f0294ea93e07bf76c`  
		Last Modified: Tue, 12 Nov 2024 02:13:13 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.6` - unknown; unknown

```console
$ docker pull emqx@sha256:5f15450038463093c58e7c0f44ba360ac7861064321e0bd4f104c7eb97d129f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2629876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd49abbad25aa6e5db92805c799b054acf8c233868b0178e42bf86198914782`

```dockerfile
```

-	Layers:
	-	`sha256:b9a733a8b135e74e4bf6a543fc5616527a8b9c3ac57c584e4763ff7cf72b2052`  
		Last Modified: Tue, 12 Nov 2024 02:13:14 GMT  
		Size: 2.6 MB (2617925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85e52ebd1d03f824afcce965d6474cdfb4f6ac2d025e190dd34b9931556fe9f8`  
		Last Modified: Tue, 12 Nov 2024 02:13:14 GMT  
		Size: 12.0 KB (11951 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.6` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:14d8a18592f7bb4abd920b8a944e81034396a6c213edf9ddec143a6dc03cf1b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120778413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05aae234d763a36bef27d0b3d150e3b0659ebb329964fd34af488af2cb38033f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 22 Apr 2024 06:31:42 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 06:31:42 GMT
ENV EMQX_VERSION=5.6.1
# Mon, 22 Apr 2024 06:31:42 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Mon, 22 Apr 2024 06:31:42 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Mon, 22 Apr 2024 06:31:42 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 22 Apr 2024 06:31:42 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
WORKDIR /opt/emqx
# Mon, 22 Apr 2024 06:31:42 GMT
USER emqx
# Mon, 22 Apr 2024 06:31:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 22 Apr 2024 06:31:42 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 22 Apr 2024 06:31:42 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 22 Apr 2024 06:31:42 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243458e30951ebe711f4756535a594ee8b9725bad792b51917c4aa4e2f3afe9e`  
		Last Modified: Tue, 12 Nov 2024 02:40:04 GMT  
		Size: 91.6 MB (91619994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367882c8c809f7e1b07a82bbd70be4344224e54eb1be2f25ca4407d9c17fbc11`  
		Last Modified: Tue, 12 Nov 2024 02:40:01 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.6` - unknown; unknown

```console
$ docker pull emqx@sha256:f11ebde5ee8ee02a560f546b3aff5f0f5fd926aba666142cd389935f451d9a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2630211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a146680a6c9a23b0da71d2b1aca28fcd2962db8da705eb2d332946abc3cd3864`

```dockerfile
```

-	Layers:
	-	`sha256:3ea336835b993568185db3d33ad9e04800523b40eac25ddfd38156bdbc6f3ae0`  
		Last Modified: Tue, 12 Nov 2024 02:40:02 GMT  
		Size: 2.6 MB (2618180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870df897d95ac201b8ebec8c040b342aa7cf622a21cc3a558dea3abd4725f58b`  
		Last Modified: Tue, 12 Nov 2024 02:40:01 GMT  
		Size: 12.0 KB (12031 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.6.1`

```console
$ docker pull emqx@sha256:4e8615238a7e9feb3a6cfaa1d36d15174b984587c12e343273eafb9a8e6fee07
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.6.1` - linux; amd64

```console
$ docker pull emqx@sha256:e37f49ee3c742e76c50c77b85423ecf322e1fb44208e5881ce6bf2b0881be356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124184785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29351f4c416538452dd51c3629e13a2ed3123dc1ec1f2a61c96e60f1cb70787d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 22 Apr 2024 06:31:42 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 06:31:42 GMT
ENV EMQX_VERSION=5.6.1
# Mon, 22 Apr 2024 06:31:42 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Mon, 22 Apr 2024 06:31:42 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Mon, 22 Apr 2024 06:31:42 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 22 Apr 2024 06:31:42 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
WORKDIR /opt/emqx
# Mon, 22 Apr 2024 06:31:42 GMT
USER emqx
# Mon, 22 Apr 2024 06:31:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 22 Apr 2024 06:31:42 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 22 Apr 2024 06:31:42 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 22 Apr 2024 06:31:42 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8c5daed23e495b00531f87295807356f2d94d546d9d6706fc6ab53efb25a37`  
		Last Modified: Tue, 12 Nov 2024 02:13:16 GMT  
		Size: 95.1 MB (95055726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0e9f298813314105c01e19c0dd89ba107f84a92ab2904f0294ea93e07bf76c`  
		Last Modified: Tue, 12 Nov 2024 02:13:13 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.6.1` - unknown; unknown

```console
$ docker pull emqx@sha256:5f15450038463093c58e7c0f44ba360ac7861064321e0bd4f104c7eb97d129f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2629876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd49abbad25aa6e5db92805c799b054acf8c233868b0178e42bf86198914782`

```dockerfile
```

-	Layers:
	-	`sha256:b9a733a8b135e74e4bf6a543fc5616527a8b9c3ac57c584e4763ff7cf72b2052`  
		Last Modified: Tue, 12 Nov 2024 02:13:14 GMT  
		Size: 2.6 MB (2617925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85e52ebd1d03f824afcce965d6474cdfb4f6ac2d025e190dd34b9931556fe9f8`  
		Last Modified: Tue, 12 Nov 2024 02:13:14 GMT  
		Size: 12.0 KB (11951 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.6.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:14d8a18592f7bb4abd920b8a944e81034396a6c213edf9ddec143a6dc03cf1b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120778413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05aae234d763a36bef27d0b3d150e3b0659ebb329964fd34af488af2cb38033f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 22 Apr 2024 06:31:42 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
CMD ["bash"]
# Mon, 22 Apr 2024 06:31:42 GMT
ENV EMQX_VERSION=5.6.1
# Mon, 22 Apr 2024 06:31:42 GMT
ENV AMD64_SHA256=a5be37660bfe6130bc159b934ed98ffcb9bef5519765491b4ed38d08ba304538
# Mon, 22 Apr 2024 06:31:42 GMT
ENV ARM64_SHA256=3f7f9b10d313f760af43e0a54cba2af4eb23ad3864b439196cb8b2903baf5651
# Mon, 22 Apr 2024 06:31:42 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 22 Apr 2024 06:31:42 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
WORKDIR /opt/emqx
# Mon, 22 Apr 2024 06:31:42 GMT
USER emqx
# Mon, 22 Apr 2024 06:31:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 22 Apr 2024 06:31:42 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 22 Apr 2024 06:31:42 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 22 Apr 2024 06:31:42 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 22 Apr 2024 06:31:42 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243458e30951ebe711f4756535a594ee8b9725bad792b51917c4aa4e2f3afe9e`  
		Last Modified: Tue, 12 Nov 2024 02:40:04 GMT  
		Size: 91.6 MB (91619994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367882c8c809f7e1b07a82bbd70be4344224e54eb1be2f25ca4407d9c17fbc11`  
		Last Modified: Tue, 12 Nov 2024 02:40:01 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.6.1` - unknown; unknown

```console
$ docker pull emqx@sha256:f11ebde5ee8ee02a560f546b3aff5f0f5fd926aba666142cd389935f451d9a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2630211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a146680a6c9a23b0da71d2b1aca28fcd2962db8da705eb2d332946abc3cd3864`

```dockerfile
```

-	Layers:
	-	`sha256:3ea336835b993568185db3d33ad9e04800523b40eac25ddfd38156bdbc6f3ae0`  
		Last Modified: Tue, 12 Nov 2024 02:40:02 GMT  
		Size: 2.6 MB (2618180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870df897d95ac201b8ebec8c040b342aa7cf622a21cc3a558dea3abd4725f58b`  
		Last Modified: Tue, 12 Nov 2024 02:40:01 GMT  
		Size: 12.0 KB (12031 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7`

```console
$ docker pull emqx@sha256:f6f3000487692994753b02188cd23b96f2a95f197484a558e6b5144142a8e6e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7` - linux; amd64

```console
$ docker pull emqx@sha256:2b6d872f4ff96b97a2de7ba9b0b19f1484e0c69dfb611e8a7780da2ed0228f96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126276931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56770ebc14f8b281617a6f339a5947c87de6232987bb7193fda36a63f336d2a`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 12 Aug 2024 08:39:51 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 08:39:51 GMT
ENV EMQX_VERSION=5.7.2
# Mon, 12 Aug 2024 08:39:51 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Mon, 12 Aug 2024 08:39:51 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Mon, 12 Aug 2024 08:39:51 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 12 Aug 2024 08:39:51 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 12 Aug 2024 08:39:51 GMT
WORKDIR /opt/emqx
# Mon, 12 Aug 2024 08:39:51 GMT
USER emqx
# Mon, 12 Aug 2024 08:39:51 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 12 Aug 2024 08:39:51 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 12 Aug 2024 08:39:51 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 12 Aug 2024 08:39:51 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 12 Aug 2024 08:39:51 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac80b899fe4235b0d056970844430af4fe7c9000e0bc7e4be7f4038ba11936a`  
		Last Modified: Tue, 12 Nov 2024 02:15:01 GMT  
		Size: 97.1 MB (97147873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b53433d8f3176cc284e319898195176834e87843dd5a977d46a44fc70dbff5`  
		Last Modified: Tue, 12 Nov 2024 02:14:59 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:4261e965889e2989d9709a480dc69f20eeefffe31445cc59fd01e2753c8b8953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2638372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094f574438166c65420d7a1aef42b20de36461b3127900e19d8ab3a44410c5e6`

```dockerfile
```

-	Layers:
	-	`sha256:059f24c7f0dd0f9c89546a4c0e3a8a6b558ec907406ef7a923f8e1f47f4712aa`  
		Last Modified: Tue, 12 Nov 2024 02:14:59 GMT  
		Size: 2.6 MB (2626421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e865313a785a64d5f094a3ad8b0885f21d208bb423eb904aa31a074be42f45dd`  
		Last Modified: Tue, 12 Nov 2024 02:14:59 GMT  
		Size: 12.0 KB (11951 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:00459319260b3484bce730f286aea2c24ec2e9062da05a6562008d6c863cc1c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122853953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81bb4cc5e8b2a4d55bf09ab610bd269a1b58628e49ac730a724b7ea7ddb47457`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 12 Aug 2024 08:39:51 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 08:39:51 GMT
ENV EMQX_VERSION=5.7.2
# Mon, 12 Aug 2024 08:39:51 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Mon, 12 Aug 2024 08:39:51 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Mon, 12 Aug 2024 08:39:51 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 12 Aug 2024 08:39:51 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 12 Aug 2024 08:39:51 GMT
WORKDIR /opt/emqx
# Mon, 12 Aug 2024 08:39:51 GMT
USER emqx
# Mon, 12 Aug 2024 08:39:51 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 12 Aug 2024 08:39:51 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 12 Aug 2024 08:39:51 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 12 Aug 2024 08:39:51 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 12 Aug 2024 08:39:51 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3639ce46453cf32c3c5e881d475637e54710c76a4377b820cab1c86aaf4d8b`  
		Last Modified: Tue, 12 Nov 2024 02:40:42 GMT  
		Size: 93.7 MB (93695538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7ecd7c98e8c4e3d054255b8dfa1b821a76c623966696d28abfe874472ef13a`  
		Last Modified: Tue, 12 Nov 2024 02:40:40 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:5de9a4b7154e7cd3370b31d365fce0cf8fc8349fbb05d3010371cd4b0662d0f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2638707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc55d7cc7c55ffa39f0fb10cb87292b88f6a0b633295cfb4e3173a79aee9e82a`

```dockerfile
```

-	Layers:
	-	`sha256:6a99192d69240ec6d7e82c6f91393a1acc298c74ee3e3b028fe9b17a28397654`  
		Last Modified: Tue, 12 Nov 2024 02:40:40 GMT  
		Size: 2.6 MB (2626676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbb22026cff88a6f206d0b34308c7fdbbe96f5965e46c06467daad1142cada1b`  
		Last Modified: Tue, 12 Nov 2024 02:40:40 GMT  
		Size: 12.0 KB (12031 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7.2`

```console
$ docker pull emqx@sha256:f6f3000487692994753b02188cd23b96f2a95f197484a558e6b5144142a8e6e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7.2` - linux; amd64

```console
$ docker pull emqx@sha256:2b6d872f4ff96b97a2de7ba9b0b19f1484e0c69dfb611e8a7780da2ed0228f96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126276931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56770ebc14f8b281617a6f339a5947c87de6232987bb7193fda36a63f336d2a`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 12 Aug 2024 08:39:51 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 08:39:51 GMT
ENV EMQX_VERSION=5.7.2
# Mon, 12 Aug 2024 08:39:51 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Mon, 12 Aug 2024 08:39:51 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Mon, 12 Aug 2024 08:39:51 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 12 Aug 2024 08:39:51 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 12 Aug 2024 08:39:51 GMT
WORKDIR /opt/emqx
# Mon, 12 Aug 2024 08:39:51 GMT
USER emqx
# Mon, 12 Aug 2024 08:39:51 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 12 Aug 2024 08:39:51 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 12 Aug 2024 08:39:51 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 12 Aug 2024 08:39:51 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 12 Aug 2024 08:39:51 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac80b899fe4235b0d056970844430af4fe7c9000e0bc7e4be7f4038ba11936a`  
		Last Modified: Tue, 12 Nov 2024 02:15:01 GMT  
		Size: 97.1 MB (97147873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b53433d8f3176cc284e319898195176834e87843dd5a977d46a44fc70dbff5`  
		Last Modified: Tue, 12 Nov 2024 02:14:59 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:4261e965889e2989d9709a480dc69f20eeefffe31445cc59fd01e2753c8b8953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2638372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094f574438166c65420d7a1aef42b20de36461b3127900e19d8ab3a44410c5e6`

```dockerfile
```

-	Layers:
	-	`sha256:059f24c7f0dd0f9c89546a4c0e3a8a6b558ec907406ef7a923f8e1f47f4712aa`  
		Last Modified: Tue, 12 Nov 2024 02:14:59 GMT  
		Size: 2.6 MB (2626421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e865313a785a64d5f094a3ad8b0885f21d208bb423eb904aa31a074be42f45dd`  
		Last Modified: Tue, 12 Nov 2024 02:14:59 GMT  
		Size: 12.0 KB (11951 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:00459319260b3484bce730f286aea2c24ec2e9062da05a6562008d6c863cc1c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122853953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81bb4cc5e8b2a4d55bf09ab610bd269a1b58628e49ac730a724b7ea7ddb47457`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 12 Aug 2024 08:39:51 GMT
CMD ["bash"]
# Mon, 12 Aug 2024 08:39:51 GMT
ENV EMQX_VERSION=5.7.2
# Mon, 12 Aug 2024 08:39:51 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Mon, 12 Aug 2024 08:39:51 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Mon, 12 Aug 2024 08:39:51 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 12 Aug 2024 08:39:51 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 12 Aug 2024 08:39:51 GMT
WORKDIR /opt/emqx
# Mon, 12 Aug 2024 08:39:51 GMT
USER emqx
# Mon, 12 Aug 2024 08:39:51 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 12 Aug 2024 08:39:51 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 12 Aug 2024 08:39:51 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 12 Aug 2024 08:39:51 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 12 Aug 2024 08:39:51 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3639ce46453cf32c3c5e881d475637e54710c76a4377b820cab1c86aaf4d8b`  
		Last Modified: Tue, 12 Nov 2024 02:40:42 GMT  
		Size: 93.7 MB (93695538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7ecd7c98e8c4e3d054255b8dfa1b821a76c623966696d28abfe874472ef13a`  
		Last Modified: Tue, 12 Nov 2024 02:40:40 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:5de9a4b7154e7cd3370b31d365fce0cf8fc8349fbb05d3010371cd4b0662d0f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2638707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc55d7cc7c55ffa39f0fb10cb87292b88f6a0b633295cfb4e3173a79aee9e82a`

```dockerfile
```

-	Layers:
	-	`sha256:6a99192d69240ec6d7e82c6f91393a1acc298c74ee3e3b028fe9b17a28397654`  
		Last Modified: Tue, 12 Nov 2024 02:40:40 GMT  
		Size: 2.6 MB (2626676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbb22026cff88a6f206d0b34308c7fdbbe96f5965e46c06467daad1142cada1b`  
		Last Modified: Tue, 12 Nov 2024 02:40:40 GMT  
		Size: 12.0 KB (12031 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8`

```console
$ docker pull emqx@sha256:decc1d0f5d41d2f1c4eb6f627404ed20ba42fde086cb028edaf8974ee65cee21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8` - linux; amd64

```console
$ docker pull emqx@sha256:60384f7e0afce136ad3fc5e57a4616720d5e5cf1083570301955c6bf8b943ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109911598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1b4c407ac1e4415796e5e02b662f753d7d482a03262e58d2a141012d533f4d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Sat, 19 Oct 2024 08:18:43 GMT
ADD rootfs.tar.xz / # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
CMD ["bash"]
# Sat, 19 Oct 2024 08:18:43 GMT
ENV EMQX_VERSION=5.8.1
# Sat, 19 Oct 2024 08:18:43 GMT
ENV AMD64_SHA256=5d7173169216f0af0cb6058387d8132dfa2cca901d684957f7b5ff75ae9ed6d8
# Sat, 19 Oct 2024 08:18:43 GMT
ENV ARM64_SHA256=fa404a444baeb8f67a4fdf1edbc3a16ea7f1249df8a43107fd54b8c02afcb167
# Sat, 19 Oct 2024 08:18:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Sat, 19 Oct 2024 08:18:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
WORKDIR /opt/emqx
# Sat, 19 Oct 2024 08:18:43 GMT
USER emqx
# Sat, 19 Oct 2024 08:18:43 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 19 Oct 2024 08:18:43 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Sat, 19 Oct 2024 08:18:43 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 19 Oct 2024 08:18:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3411c98fdf0a87bfa9c602bd68d8f3c97b43171b38b76d1359aa50a1b9a6fddb`  
		Last Modified: Tue, 12 Nov 2024 02:14:55 GMT  
		Size: 80.8 MB (80782541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6c3a751b4cd2ffbd05ad84e4817a59b00c30eeaf5af43352bcc747ebb5afda`  
		Last Modified: Tue, 12 Nov 2024 02:14:54 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:576eb49ecbf8a0a0649fed6d551d21144a90a68fc8f80182a2180ac476a027dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f74d1ca98d1e8c51cef06a64cf3621e8dc460279988a76c7feb8217f654e398`

```dockerfile
```

-	Layers:
	-	`sha256:aa34fea48a2d1a4629118d5daa681d0bd0ed894ffc2929b8d729590ad05b4aa2`  
		Last Modified: Tue, 12 Nov 2024 02:14:54 GMT  
		Size: 2.6 MB (2624750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8219044b35c6840dfdbc37b4d0c04b2c88df30be8e0722561941244969d466c`  
		Last Modified: Tue, 12 Nov 2024 02:14:54 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:26d0a2a274b6544735682c5c6b0fa79228aa7116107a8e641b10078352226e96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107099280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bffb3299ca78f97d0e7b8af7ae0f4263b23336165bc264ef2245fe9532ce1e60`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Sat, 19 Oct 2024 08:18:43 GMT
ADD rootfs.tar.xz / # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
CMD ["bash"]
# Sat, 19 Oct 2024 08:18:43 GMT
ENV EMQX_VERSION=5.8.1
# Sat, 19 Oct 2024 08:18:43 GMT
ENV AMD64_SHA256=5d7173169216f0af0cb6058387d8132dfa2cca901d684957f7b5ff75ae9ed6d8
# Sat, 19 Oct 2024 08:18:43 GMT
ENV ARM64_SHA256=fa404a444baeb8f67a4fdf1edbc3a16ea7f1249df8a43107fd54b8c02afcb167
# Sat, 19 Oct 2024 08:18:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Sat, 19 Oct 2024 08:18:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
WORKDIR /opt/emqx
# Sat, 19 Oct 2024 08:18:43 GMT
USER emqx
# Sat, 19 Oct 2024 08:18:43 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 19 Oct 2024 08:18:43 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Sat, 19 Oct 2024 08:18:43 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 19 Oct 2024 08:18:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1213e8941a1d725c8135186c642ce11321dfbce484861d16bbac4c0257f72936`  
		Last Modified: Tue, 12 Nov 2024 02:41:28 GMT  
		Size: 77.9 MB (77940861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0613112341eb4a876b533274a0c30bc7aea14ebe44ed4dde3609e0fe85835bde`  
		Last Modified: Tue, 12 Nov 2024 02:41:25 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:3c653c150236b3bd8bdbd1eab140b272178aaca27e7cef076786f1cdb5b45b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da20b0757e0d879de0d9a518eef254e2f20383f6c8c9996c1dcbabb72e735aa5`

```dockerfile
```

-	Layers:
	-	`sha256:3d67ea5997e278c74f766db587db9fee37836cb35dc2ab1344068a7a2e5987cb`  
		Last Modified: Tue, 12 Nov 2024 02:41:26 GMT  
		Size: 2.6 MB (2625029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b11bbf5e707341528c4fb7bcb32af45cfe08ceb39a2059720e2541d31e490f5a`  
		Last Modified: Tue, 12 Nov 2024 02:41:25 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8.1`

```console
$ docker pull emqx@sha256:decc1d0f5d41d2f1c4eb6f627404ed20ba42fde086cb028edaf8974ee65cee21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8.1` - linux; amd64

```console
$ docker pull emqx@sha256:60384f7e0afce136ad3fc5e57a4616720d5e5cf1083570301955c6bf8b943ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109911598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1b4c407ac1e4415796e5e02b662f753d7d482a03262e58d2a141012d533f4d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Sat, 19 Oct 2024 08:18:43 GMT
ADD rootfs.tar.xz / # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
CMD ["bash"]
# Sat, 19 Oct 2024 08:18:43 GMT
ENV EMQX_VERSION=5.8.1
# Sat, 19 Oct 2024 08:18:43 GMT
ENV AMD64_SHA256=5d7173169216f0af0cb6058387d8132dfa2cca901d684957f7b5ff75ae9ed6d8
# Sat, 19 Oct 2024 08:18:43 GMT
ENV ARM64_SHA256=fa404a444baeb8f67a4fdf1edbc3a16ea7f1249df8a43107fd54b8c02afcb167
# Sat, 19 Oct 2024 08:18:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Sat, 19 Oct 2024 08:18:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
WORKDIR /opt/emqx
# Sat, 19 Oct 2024 08:18:43 GMT
USER emqx
# Sat, 19 Oct 2024 08:18:43 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 19 Oct 2024 08:18:43 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Sat, 19 Oct 2024 08:18:43 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 19 Oct 2024 08:18:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3411c98fdf0a87bfa9c602bd68d8f3c97b43171b38b76d1359aa50a1b9a6fddb`  
		Last Modified: Tue, 12 Nov 2024 02:14:55 GMT  
		Size: 80.8 MB (80782541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6c3a751b4cd2ffbd05ad84e4817a59b00c30eeaf5af43352bcc747ebb5afda`  
		Last Modified: Tue, 12 Nov 2024 02:14:54 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.1` - unknown; unknown

```console
$ docker pull emqx@sha256:576eb49ecbf8a0a0649fed6d551d21144a90a68fc8f80182a2180ac476a027dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f74d1ca98d1e8c51cef06a64cf3621e8dc460279988a76c7feb8217f654e398`

```dockerfile
```

-	Layers:
	-	`sha256:aa34fea48a2d1a4629118d5daa681d0bd0ed894ffc2929b8d729590ad05b4aa2`  
		Last Modified: Tue, 12 Nov 2024 02:14:54 GMT  
		Size: 2.6 MB (2624750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8219044b35c6840dfdbc37b4d0c04b2c88df30be8e0722561941244969d466c`  
		Last Modified: Tue, 12 Nov 2024 02:14:54 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:26d0a2a274b6544735682c5c6b0fa79228aa7116107a8e641b10078352226e96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107099280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bffb3299ca78f97d0e7b8af7ae0f4263b23336165bc264ef2245fe9532ce1e60`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Sat, 19 Oct 2024 08:18:43 GMT
ADD rootfs.tar.xz / # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
CMD ["bash"]
# Sat, 19 Oct 2024 08:18:43 GMT
ENV EMQX_VERSION=5.8.1
# Sat, 19 Oct 2024 08:18:43 GMT
ENV AMD64_SHA256=5d7173169216f0af0cb6058387d8132dfa2cca901d684957f7b5ff75ae9ed6d8
# Sat, 19 Oct 2024 08:18:43 GMT
ENV ARM64_SHA256=fa404a444baeb8f67a4fdf1edbc3a16ea7f1249df8a43107fd54b8c02afcb167
# Sat, 19 Oct 2024 08:18:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Sat, 19 Oct 2024 08:18:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
WORKDIR /opt/emqx
# Sat, 19 Oct 2024 08:18:43 GMT
USER emqx
# Sat, 19 Oct 2024 08:18:43 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 19 Oct 2024 08:18:43 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Sat, 19 Oct 2024 08:18:43 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 19 Oct 2024 08:18:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1213e8941a1d725c8135186c642ce11321dfbce484861d16bbac4c0257f72936`  
		Last Modified: Tue, 12 Nov 2024 02:41:28 GMT  
		Size: 77.9 MB (77940861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0613112341eb4a876b533274a0c30bc7aea14ebe44ed4dde3609e0fe85835bde`  
		Last Modified: Tue, 12 Nov 2024 02:41:25 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.1` - unknown; unknown

```console
$ docker pull emqx@sha256:3c653c150236b3bd8bdbd1eab140b272178aaca27e7cef076786f1cdb5b45b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da20b0757e0d879de0d9a518eef254e2f20383f6c8c9996c1dcbabb72e735aa5`

```dockerfile
```

-	Layers:
	-	`sha256:3d67ea5997e278c74f766db587db9fee37836cb35dc2ab1344068a7a2e5987cb`  
		Last Modified: Tue, 12 Nov 2024 02:41:26 GMT  
		Size: 2.6 MB (2625029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b11bbf5e707341528c4fb7bcb32af45cfe08ceb39a2059720e2541d31e490f5a`  
		Last Modified: Tue, 12 Nov 2024 02:41:25 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:latest`

```console
$ docker pull emqx@sha256:decc1d0f5d41d2f1c4eb6f627404ed20ba42fde086cb028edaf8974ee65cee21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:60384f7e0afce136ad3fc5e57a4616720d5e5cf1083570301955c6bf8b943ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.9 MB (109911598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1b4c407ac1e4415796e5e02b662f753d7d482a03262e58d2a141012d533f4d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Sat, 19 Oct 2024 08:18:43 GMT
ADD rootfs.tar.xz / # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
CMD ["bash"]
# Sat, 19 Oct 2024 08:18:43 GMT
ENV EMQX_VERSION=5.8.1
# Sat, 19 Oct 2024 08:18:43 GMT
ENV AMD64_SHA256=5d7173169216f0af0cb6058387d8132dfa2cca901d684957f7b5ff75ae9ed6d8
# Sat, 19 Oct 2024 08:18:43 GMT
ENV ARM64_SHA256=fa404a444baeb8f67a4fdf1edbc3a16ea7f1249df8a43107fd54b8c02afcb167
# Sat, 19 Oct 2024 08:18:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Sat, 19 Oct 2024 08:18:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
WORKDIR /opt/emqx
# Sat, 19 Oct 2024 08:18:43 GMT
USER emqx
# Sat, 19 Oct 2024 08:18:43 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 19 Oct 2024 08:18:43 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Sat, 19 Oct 2024 08:18:43 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 19 Oct 2024 08:18:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3411c98fdf0a87bfa9c602bd68d8f3c97b43171b38b76d1359aa50a1b9a6fddb`  
		Last Modified: Tue, 12 Nov 2024 02:14:55 GMT  
		Size: 80.8 MB (80782541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6c3a751b4cd2ffbd05ad84e4817a59b00c30eeaf5af43352bcc747ebb5afda`  
		Last Modified: Tue, 12 Nov 2024 02:14:54 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:576eb49ecbf8a0a0649fed6d551d21144a90a68fc8f80182a2180ac476a027dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f74d1ca98d1e8c51cef06a64cf3621e8dc460279988a76c7feb8217f654e398`

```dockerfile
```

-	Layers:
	-	`sha256:aa34fea48a2d1a4629118d5daa681d0bd0ed894ffc2929b8d729590ad05b4aa2`  
		Last Modified: Tue, 12 Nov 2024 02:14:54 GMT  
		Size: 2.6 MB (2624750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8219044b35c6840dfdbc37b4d0c04b2c88df30be8e0722561941244969d466c`  
		Last Modified: Tue, 12 Nov 2024 02:14:54 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:26d0a2a274b6544735682c5c6b0fa79228aa7116107a8e641b10078352226e96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107099280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bffb3299ca78f97d0e7b8af7ae0f4263b23336165bc264ef2245fe9532ce1e60`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Sat, 19 Oct 2024 08:18:43 GMT
ADD rootfs.tar.xz / # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
CMD ["bash"]
# Sat, 19 Oct 2024 08:18:43 GMT
ENV EMQX_VERSION=5.8.1
# Sat, 19 Oct 2024 08:18:43 GMT
ENV AMD64_SHA256=5d7173169216f0af0cb6058387d8132dfa2cca901d684957f7b5ff75ae9ed6d8
# Sat, 19 Oct 2024 08:18:43 GMT
ENV ARM64_SHA256=fa404a444baeb8f67a4fdf1edbc3a16ea7f1249df8a43107fd54b8c02afcb167
# Sat, 19 Oct 2024 08:18:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Sat, 19 Oct 2024 08:18:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
WORKDIR /opt/emqx
# Sat, 19 Oct 2024 08:18:43 GMT
USER emqx
# Sat, 19 Oct 2024 08:18:43 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 19 Oct 2024 08:18:43 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Sat, 19 Oct 2024 08:18:43 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Sat, 19 Oct 2024 08:18:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 19 Oct 2024 08:18:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1213e8941a1d725c8135186c642ce11321dfbce484861d16bbac4c0257f72936`  
		Last Modified: Tue, 12 Nov 2024 02:41:28 GMT  
		Size: 77.9 MB (77940861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0613112341eb4a876b533274a0c30bc7aea14ebe44ed4dde3609e0fe85835bde`  
		Last Modified: Tue, 12 Nov 2024 02:41:25 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:3c653c150236b3bd8bdbd1eab140b272178aaca27e7cef076786f1cdb5b45b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2637662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da20b0757e0d879de0d9a518eef254e2f20383f6c8c9996c1dcbabb72e735aa5`

```dockerfile
```

-	Layers:
	-	`sha256:3d67ea5997e278c74f766db587db9fee37836cb35dc2ab1344068a7a2e5987cb`  
		Last Modified: Tue, 12 Nov 2024 02:41:26 GMT  
		Size: 2.6 MB (2625029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b11bbf5e707341528c4fb7bcb32af45cfe08ceb39a2059720e2541d31e490f5a`  
		Last Modified: Tue, 12 Nov 2024 02:41:25 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json
