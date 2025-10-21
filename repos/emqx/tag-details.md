<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:5`](#emqx5)
-	[`emqx:5.7`](#emqx57)
-	[`emqx:5.7.2`](#emqx572)
-	[`emqx:5.8`](#emqx58)
-	[`emqx:5.8.8`](#emqx588)
-	[`emqx:latest`](#emqxlatest)

## `emqx:5`

```console
$ docker pull emqx@sha256:5414bf315fb1bbf7d0fb0dbe971cc62c5ae99befd73345e313771ab282b3ba3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:0804a3947b981ddf74f0846d4e20d25dedac31bb688e1701d7329243d22b8889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108400206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c25b925c1b5729b143bc5050139d52c163079051bf841c0354decc0882c97d31`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 04 Sep 2025 09:09:19 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Thu, 04 Sep 2025 09:09:19 GMT
ENV EMQX_VERSION=5.8.8
# Thu, 04 Sep 2025 09:09:19 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Thu, 04 Sep 2025 09:09:19 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Thu, 04 Sep 2025 09:09:19 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 04 Sep 2025 09:09:19 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 04 Sep 2025 09:09:19 GMT
WORKDIR /opt/emqx
# Thu, 04 Sep 2025 09:09:19 GMT
USER emqx
# Thu, 04 Sep 2025 09:09:19 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 04 Sep 2025 09:09:19 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 04 Sep 2025 09:09:19 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 04 Sep 2025 09:09:19 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 04 Sep 2025 09:09:19 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e44c22435bd21daa2ff794907a94909566dcd1afb2fcbddbe1b0da6a2737d`  
		Last Modified: Mon, 29 Sep 2025 23:50:08 GMT  
		Size: 78.6 MB (78621379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553af2f16f58b51f0446a58a8d963ef85f3d3b08e5b8668179ecd8b4b0807513`  
		Last Modified: Mon, 29 Sep 2025 23:50:00 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:9c444abd178a893d0aa3bac0d074a84427a057f9d5eae603b8d906b85dd47ac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f6b089289a00e7c08e60bef5cbdef68d7cb9e5d73139c247765dca06aec1b7`

```dockerfile
```

-	Layers:
	-	`sha256:be87a94c77de160916e7918008d8a6ca70245fdc419ec5abe911bd482763b15c`  
		Last Modified: Tue, 30 Sep 2025 02:27:20 GMT  
		Size: 2.4 MB (2403281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e64734c5a713e83738166ba985acb3bcfcdcba9f64146a9856140c954dfb3b9`  
		Last Modified: Tue, 30 Sep 2025 02:27:21 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:6f192eb65b219b92ccb54ebb86bb287246ba5dbc65e77ead97d6205036ebf186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106673462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b364b82e944ba5ef5cc8d10559cf239f5f02af5fbf0de573394da737351ee73c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 04 Sep 2025 09:09:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Thu, 04 Sep 2025 09:09:19 GMT
ENV EMQX_VERSION=5.8.8
# Thu, 04 Sep 2025 09:09:19 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Thu, 04 Sep 2025 09:09:19 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Thu, 04 Sep 2025 09:09:19 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 04 Sep 2025 09:09:19 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 04 Sep 2025 09:09:19 GMT
WORKDIR /opt/emqx
# Thu, 04 Sep 2025 09:09:19 GMT
USER emqx
# Thu, 04 Sep 2025 09:09:19 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 04 Sep 2025 09:09:19 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 04 Sep 2025 09:09:19 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 04 Sep 2025 09:09:19 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 04 Sep 2025 09:09:19 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13ddf0ee5532d35175437c90898d40055da1300a6555a0db4742545f7563933`  
		Last Modified: Tue, 21 Oct 2025 01:16:58 GMT  
		Size: 76.5 MB (76530272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff8b66d54b881659f5c9f77dec25ae05e4218d016f32f57bef15de19709b51d`  
		Last Modified: Tue, 21 Oct 2025 01:16:52 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:39002a88ec037650c0a6a1ed52a5ce7bb446e19dabde8e07589682753b3d54b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf3be2f3d329a71640a643571fa66e232303cc2cd5dddca941350f155b94b9c`

```dockerfile
```

-	Layers:
	-	`sha256:8b42980123438161a3909064137eb866a1c420bfca5778582c8495a944e47168`  
		Last Modified: Tue, 21 Oct 2025 08:27:21 GMT  
		Size: 2.4 MB (2403624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25a5bb2dae5298fa0cff01cb24a233fe38dec22b38a04104d654ead5eb2d17e8`  
		Last Modified: Tue, 21 Oct 2025 08:27:21 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7`

```console
$ docker pull emqx@sha256:4451c30045d1c82a0b73f5e11de66ace35c90858ef310d2d5e1c7fe1641f803b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7` - linux; amd64

```console
$ docker pull emqx@sha256:d4d2be694c456b4f211c9037ba2aaf699de51f5ded889c9952d182947319fdd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125384504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45cc8d16a1f34c15a380f8b8f145cd4f87e6fe82447fd5b9d8a8c61d39e7591`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0628f7890c381e952543eb173d22fef7f1df65236214c854cf6991c0aedac806`  
		Last Modified: Mon, 29 Sep 2025 23:49:12 GMT  
		Size: 97.2 MB (97155108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbcf27f27834abeff4eaf9b39c5dacdfab526197f64b176f6ee19d3f78b92f6`  
		Last Modified: Mon, 29 Sep 2025 23:49:04 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:ff8d1c37033f85164b73b2c40b25a042273170bedc5ad63a059b2fe79a028955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567bc27ab07608c1f810e6be1c4655bb0c82cd69670e4208f51822a1858fa62a`

```dockerfile
```

-	Layers:
	-	`sha256:c6db834e3474da93e3aecce627e8e5c24c8fdf2ec0c56e84f08c46a7e2d2574c`  
		Last Modified: Tue, 30 Sep 2025 02:27:29 GMT  
		Size: 2.8 MB (2751388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:802124f137901f75eaad2cdccea550817e88251a0d703c1f39affcda2447e7a9`  
		Last Modified: Tue, 30 Sep 2025 02:27:30 GMT  
		Size: 12.0 KB (11951 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:b48505ebdd664e93d00b38808cb1f2e74a303986f06354a95d6bd8ef6d943ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121818409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba1c02f56e5e412c9bde7031d9ea42844914d170189b607ab844a87c09e5ea41`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc548190a21913c35ba4dbe17c3c4b37ed06678ea847074804b1e1c4e9c1969`  
		Last Modified: Tue, 21 Oct 2025 01:16:55 GMT  
		Size: 93.7 MB (93715157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53eba7ef9def7713ed3d9b50a068132e7cff40a762c97c8f68e16bbc0ca9d70a`  
		Last Modified: Tue, 21 Oct 2025 01:16:49 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:ea1ecfdce388a8b969852217bd43b61b44954ac6e90b81aef62fc0052f25afcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c32633282838ea24adf5b7836bd51f9445f374e2d5718eafb8affb5b92bdc29`

```dockerfile
```

-	Layers:
	-	`sha256:0f976322463dad34963b79cf85a393a3921a45132ca6093fae7d6e62fd7d515f`  
		Last Modified: Tue, 21 Oct 2025 08:27:26 GMT  
		Size: 2.8 MB (2751644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d47f6a22166992368c2422d44f5e42b35e17288d93fe07cc4736e2de96e54e4`  
		Last Modified: Tue, 21 Oct 2025 08:27:26 GMT  
		Size: 12.0 KB (12031 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7.2`

```console
$ docker pull emqx@sha256:4451c30045d1c82a0b73f5e11de66ace35c90858ef310d2d5e1c7fe1641f803b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7.2` - linux; amd64

```console
$ docker pull emqx@sha256:d4d2be694c456b4f211c9037ba2aaf699de51f5ded889c9952d182947319fdd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125384504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45cc8d16a1f34c15a380f8b8f145cd4f87e6fe82447fd5b9d8a8c61d39e7591`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0628f7890c381e952543eb173d22fef7f1df65236214c854cf6991c0aedac806`  
		Last Modified: Mon, 29 Sep 2025 23:49:12 GMT  
		Size: 97.2 MB (97155108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbcf27f27834abeff4eaf9b39c5dacdfab526197f64b176f6ee19d3f78b92f6`  
		Last Modified: Mon, 29 Sep 2025 23:49:04 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:ff8d1c37033f85164b73b2c40b25a042273170bedc5ad63a059b2fe79a028955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567bc27ab07608c1f810e6be1c4655bb0c82cd69670e4208f51822a1858fa62a`

```dockerfile
```

-	Layers:
	-	`sha256:c6db834e3474da93e3aecce627e8e5c24c8fdf2ec0c56e84f08c46a7e2d2574c`  
		Last Modified: Tue, 30 Sep 2025 02:27:29 GMT  
		Size: 2.8 MB (2751388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:802124f137901f75eaad2cdccea550817e88251a0d703c1f39affcda2447e7a9`  
		Last Modified: Tue, 30 Sep 2025 02:27:30 GMT  
		Size: 12.0 KB (11951 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:b48505ebdd664e93d00b38808cb1f2e74a303986f06354a95d6bd8ef6d943ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121818409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba1c02f56e5e412c9bde7031d9ea42844914d170189b607ab844a87c09e5ea41`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
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
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc548190a21913c35ba4dbe17c3c4b37ed06678ea847074804b1e1c4e9c1969`  
		Last Modified: Tue, 21 Oct 2025 01:16:55 GMT  
		Size: 93.7 MB (93715157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53eba7ef9def7713ed3d9b50a068132e7cff40a762c97c8f68e16bbc0ca9d70a`  
		Last Modified: Tue, 21 Oct 2025 01:16:49 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:ea1ecfdce388a8b969852217bd43b61b44954ac6e90b81aef62fc0052f25afcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c32633282838ea24adf5b7836bd51f9445f374e2d5718eafb8affb5b92bdc29`

```dockerfile
```

-	Layers:
	-	`sha256:0f976322463dad34963b79cf85a393a3921a45132ca6093fae7d6e62fd7d515f`  
		Last Modified: Tue, 21 Oct 2025 08:27:26 GMT  
		Size: 2.8 MB (2751644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d47f6a22166992368c2422d44f5e42b35e17288d93fe07cc4736e2de96e54e4`  
		Last Modified: Tue, 21 Oct 2025 08:27:26 GMT  
		Size: 12.0 KB (12031 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8`

```console
$ docker pull emqx@sha256:5414bf315fb1bbf7d0fb0dbe971cc62c5ae99befd73345e313771ab282b3ba3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8` - linux; amd64

```console
$ docker pull emqx@sha256:0804a3947b981ddf74f0846d4e20d25dedac31bb688e1701d7329243d22b8889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108400206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c25b925c1b5729b143bc5050139d52c163079051bf841c0354decc0882c97d31`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 04 Sep 2025 09:09:19 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Thu, 04 Sep 2025 09:09:19 GMT
ENV EMQX_VERSION=5.8.8
# Thu, 04 Sep 2025 09:09:19 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Thu, 04 Sep 2025 09:09:19 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Thu, 04 Sep 2025 09:09:19 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 04 Sep 2025 09:09:19 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 04 Sep 2025 09:09:19 GMT
WORKDIR /opt/emqx
# Thu, 04 Sep 2025 09:09:19 GMT
USER emqx
# Thu, 04 Sep 2025 09:09:19 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 04 Sep 2025 09:09:19 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 04 Sep 2025 09:09:19 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 04 Sep 2025 09:09:19 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 04 Sep 2025 09:09:19 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e44c22435bd21daa2ff794907a94909566dcd1afb2fcbddbe1b0da6a2737d`  
		Last Modified: Mon, 29 Sep 2025 23:50:08 GMT  
		Size: 78.6 MB (78621379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553af2f16f58b51f0446a58a8d963ef85f3d3b08e5b8668179ecd8b4b0807513`  
		Last Modified: Mon, 29 Sep 2025 23:50:00 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:9c444abd178a893d0aa3bac0d074a84427a057f9d5eae603b8d906b85dd47ac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f6b089289a00e7c08e60bef5cbdef68d7cb9e5d73139c247765dca06aec1b7`

```dockerfile
```

-	Layers:
	-	`sha256:be87a94c77de160916e7918008d8a6ca70245fdc419ec5abe911bd482763b15c`  
		Last Modified: Tue, 30 Sep 2025 02:27:20 GMT  
		Size: 2.4 MB (2403281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e64734c5a713e83738166ba985acb3bcfcdcba9f64146a9856140c954dfb3b9`  
		Last Modified: Tue, 30 Sep 2025 02:27:21 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:6f192eb65b219b92ccb54ebb86bb287246ba5dbc65e77ead97d6205036ebf186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106673462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b364b82e944ba5ef5cc8d10559cf239f5f02af5fbf0de573394da737351ee73c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 04 Sep 2025 09:09:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Thu, 04 Sep 2025 09:09:19 GMT
ENV EMQX_VERSION=5.8.8
# Thu, 04 Sep 2025 09:09:19 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Thu, 04 Sep 2025 09:09:19 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Thu, 04 Sep 2025 09:09:19 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 04 Sep 2025 09:09:19 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 04 Sep 2025 09:09:19 GMT
WORKDIR /opt/emqx
# Thu, 04 Sep 2025 09:09:19 GMT
USER emqx
# Thu, 04 Sep 2025 09:09:19 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 04 Sep 2025 09:09:19 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 04 Sep 2025 09:09:19 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 04 Sep 2025 09:09:19 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 04 Sep 2025 09:09:19 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13ddf0ee5532d35175437c90898d40055da1300a6555a0db4742545f7563933`  
		Last Modified: Tue, 21 Oct 2025 01:16:58 GMT  
		Size: 76.5 MB (76530272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff8b66d54b881659f5c9f77dec25ae05e4218d016f32f57bef15de19709b51d`  
		Last Modified: Tue, 21 Oct 2025 01:16:52 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:39002a88ec037650c0a6a1ed52a5ce7bb446e19dabde8e07589682753b3d54b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf3be2f3d329a71640a643571fa66e232303cc2cd5dddca941350f155b94b9c`

```dockerfile
```

-	Layers:
	-	`sha256:8b42980123438161a3909064137eb866a1c420bfca5778582c8495a944e47168`  
		Last Modified: Tue, 21 Oct 2025 08:27:21 GMT  
		Size: 2.4 MB (2403624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25a5bb2dae5298fa0cff01cb24a233fe38dec22b38a04104d654ead5eb2d17e8`  
		Last Modified: Tue, 21 Oct 2025 08:27:21 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8.8`

```console
$ docker pull emqx@sha256:5414bf315fb1bbf7d0fb0dbe971cc62c5ae99befd73345e313771ab282b3ba3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8.8` - linux; amd64

```console
$ docker pull emqx@sha256:0804a3947b981ddf74f0846d4e20d25dedac31bb688e1701d7329243d22b8889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108400206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c25b925c1b5729b143bc5050139d52c163079051bf841c0354decc0882c97d31`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 04 Sep 2025 09:09:19 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Thu, 04 Sep 2025 09:09:19 GMT
ENV EMQX_VERSION=5.8.8
# Thu, 04 Sep 2025 09:09:19 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Thu, 04 Sep 2025 09:09:19 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Thu, 04 Sep 2025 09:09:19 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 04 Sep 2025 09:09:19 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 04 Sep 2025 09:09:19 GMT
WORKDIR /opt/emqx
# Thu, 04 Sep 2025 09:09:19 GMT
USER emqx
# Thu, 04 Sep 2025 09:09:19 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 04 Sep 2025 09:09:19 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 04 Sep 2025 09:09:19 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 04 Sep 2025 09:09:19 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 04 Sep 2025 09:09:19 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e44c22435bd21daa2ff794907a94909566dcd1afb2fcbddbe1b0da6a2737d`  
		Last Modified: Mon, 29 Sep 2025 23:50:08 GMT  
		Size: 78.6 MB (78621379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553af2f16f58b51f0446a58a8d963ef85f3d3b08e5b8668179ecd8b4b0807513`  
		Last Modified: Mon, 29 Sep 2025 23:50:00 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.8` - unknown; unknown

```console
$ docker pull emqx@sha256:9c444abd178a893d0aa3bac0d074a84427a057f9d5eae603b8d906b85dd47ac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f6b089289a00e7c08e60bef5cbdef68d7cb9e5d73139c247765dca06aec1b7`

```dockerfile
```

-	Layers:
	-	`sha256:be87a94c77de160916e7918008d8a6ca70245fdc419ec5abe911bd482763b15c`  
		Last Modified: Tue, 30 Sep 2025 02:27:20 GMT  
		Size: 2.4 MB (2403281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e64734c5a713e83738166ba985acb3bcfcdcba9f64146a9856140c954dfb3b9`  
		Last Modified: Tue, 30 Sep 2025 02:27:21 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8.8` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:6f192eb65b219b92ccb54ebb86bb287246ba5dbc65e77ead97d6205036ebf186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106673462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b364b82e944ba5ef5cc8d10559cf239f5f02af5fbf0de573394da737351ee73c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 04 Sep 2025 09:09:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Thu, 04 Sep 2025 09:09:19 GMT
ENV EMQX_VERSION=5.8.8
# Thu, 04 Sep 2025 09:09:19 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Thu, 04 Sep 2025 09:09:19 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Thu, 04 Sep 2025 09:09:19 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 04 Sep 2025 09:09:19 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 04 Sep 2025 09:09:19 GMT
WORKDIR /opt/emqx
# Thu, 04 Sep 2025 09:09:19 GMT
USER emqx
# Thu, 04 Sep 2025 09:09:19 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 04 Sep 2025 09:09:19 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 04 Sep 2025 09:09:19 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 04 Sep 2025 09:09:19 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 04 Sep 2025 09:09:19 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13ddf0ee5532d35175437c90898d40055da1300a6555a0db4742545f7563933`  
		Last Modified: Tue, 21 Oct 2025 01:16:58 GMT  
		Size: 76.5 MB (76530272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff8b66d54b881659f5c9f77dec25ae05e4218d016f32f57bef15de19709b51d`  
		Last Modified: Tue, 21 Oct 2025 01:16:52 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.8` - unknown; unknown

```console
$ docker pull emqx@sha256:39002a88ec037650c0a6a1ed52a5ce7bb446e19dabde8e07589682753b3d54b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf3be2f3d329a71640a643571fa66e232303cc2cd5dddca941350f155b94b9c`

```dockerfile
```

-	Layers:
	-	`sha256:8b42980123438161a3909064137eb866a1c420bfca5778582c8495a944e47168`  
		Last Modified: Tue, 21 Oct 2025 08:27:21 GMT  
		Size: 2.4 MB (2403624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25a5bb2dae5298fa0cff01cb24a233fe38dec22b38a04104d654ead5eb2d17e8`  
		Last Modified: Tue, 21 Oct 2025 08:27:21 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:latest`

```console
$ docker pull emqx@sha256:5414bf315fb1bbf7d0fb0dbe971cc62c5ae99befd73345e313771ab282b3ba3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:0804a3947b981ddf74f0846d4e20d25dedac31bb688e1701d7329243d22b8889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108400206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c25b925c1b5729b143bc5050139d52c163079051bf841c0354decc0882c97d31`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 04 Sep 2025 09:09:19 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Thu, 04 Sep 2025 09:09:19 GMT
ENV EMQX_VERSION=5.8.8
# Thu, 04 Sep 2025 09:09:19 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Thu, 04 Sep 2025 09:09:19 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Thu, 04 Sep 2025 09:09:19 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 04 Sep 2025 09:09:19 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 04 Sep 2025 09:09:19 GMT
WORKDIR /opt/emqx
# Thu, 04 Sep 2025 09:09:19 GMT
USER emqx
# Thu, 04 Sep 2025 09:09:19 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 04 Sep 2025 09:09:19 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 04 Sep 2025 09:09:19 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 04 Sep 2025 09:09:19 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 04 Sep 2025 09:09:19 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e44c22435bd21daa2ff794907a94909566dcd1afb2fcbddbe1b0da6a2737d`  
		Last Modified: Mon, 29 Sep 2025 23:50:08 GMT  
		Size: 78.6 MB (78621379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553af2f16f58b51f0446a58a8d963ef85f3d3b08e5b8668179ecd8b4b0807513`  
		Last Modified: Mon, 29 Sep 2025 23:50:00 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:9c444abd178a893d0aa3bac0d074a84427a057f9d5eae603b8d906b85dd47ac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f6b089289a00e7c08e60bef5cbdef68d7cb9e5d73139c247765dca06aec1b7`

```dockerfile
```

-	Layers:
	-	`sha256:be87a94c77de160916e7918008d8a6ca70245fdc419ec5abe911bd482763b15c`  
		Last Modified: Tue, 30 Sep 2025 02:27:20 GMT  
		Size: 2.4 MB (2403281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e64734c5a713e83738166ba985acb3bcfcdcba9f64146a9856140c954dfb3b9`  
		Last Modified: Tue, 30 Sep 2025 02:27:21 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:6f192eb65b219b92ccb54ebb86bb287246ba5dbc65e77ead97d6205036ebf186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106673462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b364b82e944ba5ef5cc8d10559cf239f5f02af5fbf0de573394da737351ee73c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 04 Sep 2025 09:09:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Thu, 04 Sep 2025 09:09:19 GMT
ENV EMQX_VERSION=5.8.8
# Thu, 04 Sep 2025 09:09:19 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Thu, 04 Sep 2025 09:09:19 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Thu, 04 Sep 2025 09:09:19 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 04 Sep 2025 09:09:19 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Thu, 04 Sep 2025 09:09:19 GMT
WORKDIR /opt/emqx
# Thu, 04 Sep 2025 09:09:19 GMT
USER emqx
# Thu, 04 Sep 2025 09:09:19 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 04 Sep 2025 09:09:19 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Thu, 04 Sep 2025 09:09:19 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Thu, 04 Sep 2025 09:09:19 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 04 Sep 2025 09:09:19 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e13ddf0ee5532d35175437c90898d40055da1300a6555a0db4742545f7563933`  
		Last Modified: Tue, 21 Oct 2025 01:16:58 GMT  
		Size: 76.5 MB (76530272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff8b66d54b881659f5c9f77dec25ae05e4218d016f32f57bef15de19709b51d`  
		Last Modified: Tue, 21 Oct 2025 01:16:52 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:39002a88ec037650c0a6a1ed52a5ce7bb446e19dabde8e07589682753b3d54b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf3be2f3d329a71640a643571fa66e232303cc2cd5dddca941350f155b94b9c`

```dockerfile
```

-	Layers:
	-	`sha256:8b42980123438161a3909064137eb866a1c420bfca5778582c8495a944e47168`  
		Last Modified: Tue, 21 Oct 2025 08:27:21 GMT  
		Size: 2.4 MB (2403624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25a5bb2dae5298fa0cff01cb24a233fe38dec22b38a04104d654ead5eb2d17e8`  
		Last Modified: Tue, 21 Oct 2025 08:27:21 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json
