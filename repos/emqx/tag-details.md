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
$ docker pull emqx@sha256:b043b8d361dc34c831ce5e72eba1b24a99856c04916d547cdc980183cc606318
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
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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
$ docker pull emqx@sha256:6cc8e56f1eb2abad01e866a5571a7155e2237bfb5265853fa28eeece4f6cd7b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106672200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b5c2966ef6edeada2f153e33e1b394f9e59706a56c7bd57809c25980bc3bf3`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 04 Sep 2025 09:09:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
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
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50be6a559560e623244034288cdce7f9bd13b00572055694a63ac19d22efd223`  
		Last Modified: Mon, 29 Sep 2025 23:50:26 GMT  
		Size: 76.5 MB (76530300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317426f3d32e76e8396368a1cac6ba1ebc95895aaed3b51fbe41d13e41088fbf`  
		Last Modified: Mon, 29 Sep 2025 23:50:19 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:d7557cedf7e2eef8eddaa3dccaa84ffb05f0fd021116521bc7ddc9972937b01f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7e8a6a1e8fc38221ffe6c1486f0df153358295795f0ce7c6fc44f9fb3a82f8`

```dockerfile
```

-	Layers:
	-	`sha256:987e891359279bf419bd44d95994b9d11d43c009c10045bf387b145ee24f963b`  
		Last Modified: Tue, 30 Sep 2025 02:27:25 GMT  
		Size: 2.4 MB (2403570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c796a6b3d30ab5c276f977ab5703f548c7b8bec9b79e132c4331acadcc7cb8dd`  
		Last Modified: Tue, 30 Sep 2025 02:27:25 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7`

```console
$ docker pull emqx@sha256:3bcb10af97d72a2896854692d3face278945654202cadadb82294f81fa3c1a92
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
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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
$ docker pull emqx@sha256:0fd297d23792d058c8c71d3c65c38d6f50ba2ec502b0434f990c848d4e4805d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121818451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5ab94e4be140d9b9e67aa826cb55f796edd030b43dff1516a4cbc49e62c614`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99399773f0ce15d2800cce6fbe21fc4484d20631e293a208b09a68e1ecc8d68b`  
		Last Modified: Mon, 29 Sep 2025 23:50:20 GMT  
		Size: 93.7 MB (93715246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4607858aff03679fdc35127da5f48b362739e8b9123637ac1ec6fa63dea7035f`  
		Last Modified: Mon, 29 Sep 2025 23:50:15 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:2e7bd7fbd29a8a231e887a44b1cf93902f13d1d22a27cc9305743b4e7983f361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc0bfb8554aba3b808e7edf1a21d928c2330a6c6948d9b4d1150320bd27f13b`

```dockerfile
```

-	Layers:
	-	`sha256:feca5e74202a896b124f5805cf1a5da08f09b679f9e5573c4fa351346395eb84`  
		Last Modified: Tue, 30 Sep 2025 02:27:35 GMT  
		Size: 2.8 MB (2751644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf970c603843288a71c6e8c3c5d02c91a661dc714e8c3135560cd3d381b70084`  
		Last Modified: Tue, 30 Sep 2025 02:27:36 GMT  
		Size: 12.0 KB (12031 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7.2`

```console
$ docker pull emqx@sha256:3bcb10af97d72a2896854692d3face278945654202cadadb82294f81fa3c1a92
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
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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
$ docker pull emqx@sha256:0fd297d23792d058c8c71d3c65c38d6f50ba2ec502b0434f990c848d4e4805d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121818451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5ab94e4be140d9b9e67aa826cb55f796edd030b43dff1516a4cbc49e62c614`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
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
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99399773f0ce15d2800cce6fbe21fc4484d20631e293a208b09a68e1ecc8d68b`  
		Last Modified: Mon, 29 Sep 2025 23:50:20 GMT  
		Size: 93.7 MB (93715246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4607858aff03679fdc35127da5f48b362739e8b9123637ac1ec6fa63dea7035f`  
		Last Modified: Mon, 29 Sep 2025 23:50:15 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:2e7bd7fbd29a8a231e887a44b1cf93902f13d1d22a27cc9305743b4e7983f361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc0bfb8554aba3b808e7edf1a21d928c2330a6c6948d9b4d1150320bd27f13b`

```dockerfile
```

-	Layers:
	-	`sha256:feca5e74202a896b124f5805cf1a5da08f09b679f9e5573c4fa351346395eb84`  
		Last Modified: Tue, 30 Sep 2025 02:27:35 GMT  
		Size: 2.8 MB (2751644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf970c603843288a71c6e8c3c5d02c91a661dc714e8c3135560cd3d381b70084`  
		Last Modified: Tue, 30 Sep 2025 02:27:36 GMT  
		Size: 12.0 KB (12031 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8`

```console
$ docker pull emqx@sha256:b043b8d361dc34c831ce5e72eba1b24a99856c04916d547cdc980183cc606318
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
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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
$ docker pull emqx@sha256:6cc8e56f1eb2abad01e866a5571a7155e2237bfb5265853fa28eeece4f6cd7b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106672200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b5c2966ef6edeada2f153e33e1b394f9e59706a56c7bd57809c25980bc3bf3`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 04 Sep 2025 09:09:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
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
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50be6a559560e623244034288cdce7f9bd13b00572055694a63ac19d22efd223`  
		Last Modified: Mon, 29 Sep 2025 23:50:26 GMT  
		Size: 76.5 MB (76530300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317426f3d32e76e8396368a1cac6ba1ebc95895aaed3b51fbe41d13e41088fbf`  
		Last Modified: Mon, 29 Sep 2025 23:50:19 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:d7557cedf7e2eef8eddaa3dccaa84ffb05f0fd021116521bc7ddc9972937b01f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7e8a6a1e8fc38221ffe6c1486f0df153358295795f0ce7c6fc44f9fb3a82f8`

```dockerfile
```

-	Layers:
	-	`sha256:987e891359279bf419bd44d95994b9d11d43c009c10045bf387b145ee24f963b`  
		Last Modified: Tue, 30 Sep 2025 02:27:25 GMT  
		Size: 2.4 MB (2403570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c796a6b3d30ab5c276f977ab5703f548c7b8bec9b79e132c4331acadcc7cb8dd`  
		Last Modified: Tue, 30 Sep 2025 02:27:25 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8.8`

```console
$ docker pull emqx@sha256:b043b8d361dc34c831ce5e72eba1b24a99856c04916d547cdc980183cc606318
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
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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
$ docker pull emqx@sha256:6cc8e56f1eb2abad01e866a5571a7155e2237bfb5265853fa28eeece4f6cd7b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106672200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b5c2966ef6edeada2f153e33e1b394f9e59706a56c7bd57809c25980bc3bf3`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 04 Sep 2025 09:09:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
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
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50be6a559560e623244034288cdce7f9bd13b00572055694a63ac19d22efd223`  
		Last Modified: Mon, 29 Sep 2025 23:50:26 GMT  
		Size: 76.5 MB (76530300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317426f3d32e76e8396368a1cac6ba1ebc95895aaed3b51fbe41d13e41088fbf`  
		Last Modified: Mon, 29 Sep 2025 23:50:19 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.8` - unknown; unknown

```console
$ docker pull emqx@sha256:d7557cedf7e2eef8eddaa3dccaa84ffb05f0fd021116521bc7ddc9972937b01f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7e8a6a1e8fc38221ffe6c1486f0df153358295795f0ce7c6fc44f9fb3a82f8`

```dockerfile
```

-	Layers:
	-	`sha256:987e891359279bf419bd44d95994b9d11d43c009c10045bf387b145ee24f963b`  
		Last Modified: Tue, 30 Sep 2025 02:27:25 GMT  
		Size: 2.4 MB (2403570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c796a6b3d30ab5c276f977ab5703f548c7b8bec9b79e132c4331acadcc7cb8dd`  
		Last Modified: Tue, 30 Sep 2025 02:27:25 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:latest`

```console
$ docker pull emqx@sha256:b043b8d361dc34c831ce5e72eba1b24a99856c04916d547cdc980183cc606318
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
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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
$ docker pull emqx@sha256:6cc8e56f1eb2abad01e866a5571a7155e2237bfb5265853fa28eeece4f6cd7b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106672200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b5c2966ef6edeada2f153e33e1b394f9e59706a56c7bd57809c25980bc3bf3`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 04 Sep 2025 09:09:19 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
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
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50be6a559560e623244034288cdce7f9bd13b00572055694a63ac19d22efd223`  
		Last Modified: Mon, 29 Sep 2025 23:50:26 GMT  
		Size: 76.5 MB (76530300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317426f3d32e76e8396368a1cac6ba1ebc95895aaed3b51fbe41d13e41088fbf`  
		Last Modified: Mon, 29 Sep 2025 23:50:19 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:d7557cedf7e2eef8eddaa3dccaa84ffb05f0fd021116521bc7ddc9972937b01f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7e8a6a1e8fc38221ffe6c1486f0df153358295795f0ce7c6fc44f9fb3a82f8`

```dockerfile
```

-	Layers:
	-	`sha256:987e891359279bf419bd44d95994b9d11d43c009c10045bf387b145ee24f963b`  
		Last Modified: Tue, 30 Sep 2025 02:27:25 GMT  
		Size: 2.4 MB (2403570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c796a6b3d30ab5c276f977ab5703f548c7b8bec9b79e132c4331acadcc7cb8dd`  
		Last Modified: Tue, 30 Sep 2025 02:27:25 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json
