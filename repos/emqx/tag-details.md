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
$ docker pull emqx@sha256:2829687a7e7d14df0ad2a2d17d83c2002e9aacae5e663b8bda586fdaaa01e949
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:632b8250c5c1f3a4bfef7854a1b551b0c5112e7e49c776ffc9e244c78562afb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108404241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9154df55f910221401b1b3771a5136923d3c6115cc9e9682a36b9088053ccc25`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:52:39 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 24 Feb 2026 18:52:39 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 24 Feb 2026 18:52:39 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 24 Feb 2026 18:52:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 24 Feb 2026 18:52:39 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 18:52:39 GMT
WORKDIR /opt/emqx
# Tue, 24 Feb 2026 18:52:39 GMT
USER emqx
# Tue, 24 Feb 2026 18:52:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 24 Feb 2026 18:52:39 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 24 Feb 2026 18:52:39 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 24 Feb 2026 18:52:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 18:52:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a56cc393affa2cbe7c8277cd9b749f3121d5281ddfdfdd3fc8cd0d5ca81bf14`  
		Last Modified: Tue, 24 Feb 2026 18:52:54 GMT  
		Size: 78.6 MB (78624546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a504ce29c56ffc47e51bf9597d04ca558c968b91f51a8c9e26ed6edc89688039`  
		Last Modified: Tue, 24 Feb 2026 18:52:52 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:7545a82e901d7a10fc8761e9d03b7dc73ca157b3af4bf676cd0ee55d2b4045b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e08ecdf33aecce1e52292c3740ed6e92050e1b888aa8bb2380d47957f4adef4`

```dockerfile
```

-	Layers:
	-	`sha256:23b73ab6fcbdb172f7d1407dde8bc42754c7cc20d9f893de1d9bdff4e095a2c6`  
		Last Modified: Tue, 24 Feb 2026 18:52:52 GMT  
		Size: 2.4 MB (2403463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e070728fc870e46c950c41aa4807d5a48f2384bedbb0f94e19368ee692bc39c1`  
		Last Modified: Tue, 24 Feb 2026 18:52:52 GMT  
		Size: 12.5 KB (12486 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:10af0712de4ae8b88bf07dd8266dee7f09857d48ffb349f2ff2baf170cd5d533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106672562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55dac24477c09674d0469032829783e0d39c0a862acfe0dd258b2fa7d63038b0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:58:59 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 24 Feb 2026 18:58:59 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 24 Feb 2026 18:58:59 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 24 Feb 2026 18:58:59 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 24 Feb 2026 18:58:59 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 18:58:59 GMT
WORKDIR /opt/emqx
# Tue, 24 Feb 2026 18:58:59 GMT
USER emqx
# Tue, 24 Feb 2026 18:58:59 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 24 Feb 2026 18:58:59 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 24 Feb 2026 18:58:59 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 24 Feb 2026 18:58:59 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 18:58:59 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00a1849c07c16e665c58b12aa62c89718fd84beec9fa1438c36923a797b8d83`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 76.5 MB (76531400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d83c8715f4a968cc8b0d47c8f4f8ebf93b60a41c7f5508ecfb04f98a52ce67e`  
		Last Modified: Tue, 24 Feb 2026 18:59:12 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:db4d2f7cdfc55c2ed654d228ef20f0c356742fe5095d1df8a882971f3e600fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc62f1776a4586af477312ec6e48141ff035e4707b2390f3b490f804d6c49ea`

```dockerfile
```

-	Layers:
	-	`sha256:1074a1e98da480a04d8502c065225855055485aa6d1fb25aad824d22543a03d6`  
		Last Modified: Tue, 24 Feb 2026 18:59:12 GMT  
		Size: 2.4 MB (2403752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ff77e088bb8c553b66b92183f270c68bc33d7961ee8e3b77b6109534528f1f8`  
		Last Modified: Tue, 24 Feb 2026 18:59:12 GMT  
		Size: 12.6 KB (12589 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7`

```console
$ docker pull emqx@sha256:5e2f43a713eb82900f758f96bf66d49f862a456709b12b0fb3089659d3b9e13f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7` - linux; amd64

```console
$ docker pull emqx@sha256:d4319528a60ffbf0f7129350231b589c0d68054ee7d3855069077079745cdc39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125392820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a7639795cdc474da1d859019b6a1289f45b1b059d3618745d0bcbc0b3e97c8`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 18:52:28 GMT
ENV EMQX_VERSION=5.7.2
# Tue, 24 Feb 2026 18:52:28 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Tue, 24 Feb 2026 18:52:28 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Tue, 24 Feb 2026 18:52:28 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 24 Feb 2026 18:52:28 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 18:52:28 GMT
WORKDIR /opt/emqx
# Tue, 24 Feb 2026 18:52:28 GMT
USER emqx
# Tue, 24 Feb 2026 18:52:28 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 24 Feb 2026 18:52:28 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 24 Feb 2026 18:52:28 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 24 Feb 2026 18:52:28 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 18:52:28 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4822f9b05b8eae90cd96cd404ab4d5e6745ec6f8ed4caf2acb77f5a22d761071`  
		Last Modified: Tue, 24 Feb 2026 18:52:45 GMT  
		Size: 97.2 MB (97155476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f59caeb7aa689fc72bdd4ac9aa1d20f7b1aa1f73b56232db6e49e0c7f8a8194f`  
		Last Modified: Tue, 24 Feb 2026 18:52:42 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:a683aa68e1bb5f70ffc0d93c29b3c2aa778bcb1e76efee0553a9389cd41c9bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8208306ded3f3cdb3024795f410a026fed95fb6cd4893b0f2f1c437a078c7207`

```dockerfile
```

-	Layers:
	-	`sha256:cd075d7d73c45b2b657a80db4bc945905663e72432858e3016af551fd26b8ab2`  
		Last Modified: Tue, 24 Feb 2026 18:52:43 GMT  
		Size: 2.8 MB (2751398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2f4efbd732dc9e57c5e8e22d3e775e7b98b947ef63732a20ed75ee502cb779c`  
		Last Modified: Tue, 24 Feb 2026 18:52:42 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:ba644816cf88b07385b6a1917af141897277148e8a47d92ac8c64bce0e917f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121833103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5395bd91eec936e576c52c8a018cc04598fca5979e63b4573fc1c9f97b6a9b6a`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 18:58:22 GMT
ENV EMQX_VERSION=5.7.2
# Tue, 24 Feb 2026 18:58:22 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Tue, 24 Feb 2026 18:58:22 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Tue, 24 Feb 2026 18:58:22 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 24 Feb 2026 18:58:22 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 18:58:22 GMT
WORKDIR /opt/emqx
# Tue, 24 Feb 2026 18:58:22 GMT
USER emqx
# Tue, 24 Feb 2026 18:58:22 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 24 Feb 2026 18:58:22 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 24 Feb 2026 18:58:22 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 24 Feb 2026 18:58:22 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 18:58:22 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f937a62abfc4c640f7eb886d87c735b50a0b7bd828bfa0eda01111e4a1b3967f`  
		Last Modified: Tue, 24 Feb 2026 18:58:39 GMT  
		Size: 93.7 MB (93715957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c96ab2f1aff8282d087a816e5e0cd90019835f206ea10eec4db506a7d9f935`  
		Last Modified: Tue, 24 Feb 2026 18:58:36 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:1e9df040b8aa2c489b22be5195376dd57cca0439a4fdedbe884626cd40c39dae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a17b9051853ff5b9aa53509c562fa14c2b17452e0e6dcbe7706ed9fc66eadd9`

```dockerfile
```

-	Layers:
	-	`sha256:5d0ef5b1fd35397a328fafb58de8bcef64f438706759e0371dec9be4debcbb76`  
		Last Modified: Tue, 24 Feb 2026 18:58:37 GMT  
		Size: 2.8 MB (2751654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed357b9be333e21e3966b32ff3e79d9820fea397e53ce7e147dea9e0a43a5fde`  
		Last Modified: Tue, 24 Feb 2026 18:58:36 GMT  
		Size: 12.0 KB (11988 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7.2`

```console
$ docker pull emqx@sha256:5e2f43a713eb82900f758f96bf66d49f862a456709b12b0fb3089659d3b9e13f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7.2` - linux; amd64

```console
$ docker pull emqx@sha256:d4319528a60ffbf0f7129350231b589c0d68054ee7d3855069077079745cdc39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125392820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a7639795cdc474da1d859019b6a1289f45b1b059d3618745d0bcbc0b3e97c8`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 18:52:28 GMT
ENV EMQX_VERSION=5.7.2
# Tue, 24 Feb 2026 18:52:28 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Tue, 24 Feb 2026 18:52:28 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Tue, 24 Feb 2026 18:52:28 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 24 Feb 2026 18:52:28 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 18:52:28 GMT
WORKDIR /opt/emqx
# Tue, 24 Feb 2026 18:52:28 GMT
USER emqx
# Tue, 24 Feb 2026 18:52:28 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 24 Feb 2026 18:52:28 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 24 Feb 2026 18:52:28 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 24 Feb 2026 18:52:28 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 18:52:28 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4822f9b05b8eae90cd96cd404ab4d5e6745ec6f8ed4caf2acb77f5a22d761071`  
		Last Modified: Tue, 24 Feb 2026 18:52:45 GMT  
		Size: 97.2 MB (97155476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f59caeb7aa689fc72bdd4ac9aa1d20f7b1aa1f73b56232db6e49e0c7f8a8194f`  
		Last Modified: Tue, 24 Feb 2026 18:52:42 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:a683aa68e1bb5f70ffc0d93c29b3c2aa778bcb1e76efee0553a9389cd41c9bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8208306ded3f3cdb3024795f410a026fed95fb6cd4893b0f2f1c437a078c7207`

```dockerfile
```

-	Layers:
	-	`sha256:cd075d7d73c45b2b657a80db4bc945905663e72432858e3016af551fd26b8ab2`  
		Last Modified: Tue, 24 Feb 2026 18:52:43 GMT  
		Size: 2.8 MB (2751398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2f4efbd732dc9e57c5e8e22d3e775e7b98b947ef63732a20ed75ee502cb779c`  
		Last Modified: Tue, 24 Feb 2026 18:52:42 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:ba644816cf88b07385b6a1917af141897277148e8a47d92ac8c64bce0e917f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121833103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5395bd91eec936e576c52c8a018cc04598fca5979e63b4573fc1c9f97b6a9b6a`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 18:58:22 GMT
ENV EMQX_VERSION=5.7.2
# Tue, 24 Feb 2026 18:58:22 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Tue, 24 Feb 2026 18:58:22 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Tue, 24 Feb 2026 18:58:22 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 24 Feb 2026 18:58:22 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 18:58:22 GMT
WORKDIR /opt/emqx
# Tue, 24 Feb 2026 18:58:22 GMT
USER emqx
# Tue, 24 Feb 2026 18:58:22 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 24 Feb 2026 18:58:22 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 24 Feb 2026 18:58:22 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 24 Feb 2026 18:58:22 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 18:58:22 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f937a62abfc4c640f7eb886d87c735b50a0b7bd828bfa0eda01111e4a1b3967f`  
		Last Modified: Tue, 24 Feb 2026 18:58:39 GMT  
		Size: 93.7 MB (93715957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c96ab2f1aff8282d087a816e5e0cd90019835f206ea10eec4db506a7d9f935`  
		Last Modified: Tue, 24 Feb 2026 18:58:36 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:1e9df040b8aa2c489b22be5195376dd57cca0439a4fdedbe884626cd40c39dae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a17b9051853ff5b9aa53509c562fa14c2b17452e0e6dcbe7706ed9fc66eadd9`

```dockerfile
```

-	Layers:
	-	`sha256:5d0ef5b1fd35397a328fafb58de8bcef64f438706759e0371dec9be4debcbb76`  
		Last Modified: Tue, 24 Feb 2026 18:58:37 GMT  
		Size: 2.8 MB (2751654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed357b9be333e21e3966b32ff3e79d9820fea397e53ce7e147dea9e0a43a5fde`  
		Last Modified: Tue, 24 Feb 2026 18:58:36 GMT  
		Size: 12.0 KB (11988 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8`

```console
$ docker pull emqx@sha256:2829687a7e7d14df0ad2a2d17d83c2002e9aacae5e663b8bda586fdaaa01e949
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8` - linux; amd64

```console
$ docker pull emqx@sha256:632b8250c5c1f3a4bfef7854a1b551b0c5112e7e49c776ffc9e244c78562afb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108404241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9154df55f910221401b1b3771a5136923d3c6115cc9e9682a36b9088053ccc25`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:52:39 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 24 Feb 2026 18:52:39 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 24 Feb 2026 18:52:39 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 24 Feb 2026 18:52:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 24 Feb 2026 18:52:39 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 18:52:39 GMT
WORKDIR /opt/emqx
# Tue, 24 Feb 2026 18:52:39 GMT
USER emqx
# Tue, 24 Feb 2026 18:52:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 24 Feb 2026 18:52:39 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 24 Feb 2026 18:52:39 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 24 Feb 2026 18:52:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 18:52:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a56cc393affa2cbe7c8277cd9b749f3121d5281ddfdfdd3fc8cd0d5ca81bf14`  
		Last Modified: Tue, 24 Feb 2026 18:52:54 GMT  
		Size: 78.6 MB (78624546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a504ce29c56ffc47e51bf9597d04ca558c968b91f51a8c9e26ed6edc89688039`  
		Last Modified: Tue, 24 Feb 2026 18:52:52 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:7545a82e901d7a10fc8761e9d03b7dc73ca157b3af4bf676cd0ee55d2b4045b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e08ecdf33aecce1e52292c3740ed6e92050e1b888aa8bb2380d47957f4adef4`

```dockerfile
```

-	Layers:
	-	`sha256:23b73ab6fcbdb172f7d1407dde8bc42754c7cc20d9f893de1d9bdff4e095a2c6`  
		Last Modified: Tue, 24 Feb 2026 18:52:52 GMT  
		Size: 2.4 MB (2403463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e070728fc870e46c950c41aa4807d5a48f2384bedbb0f94e19368ee692bc39c1`  
		Last Modified: Tue, 24 Feb 2026 18:52:52 GMT  
		Size: 12.5 KB (12486 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:10af0712de4ae8b88bf07dd8266dee7f09857d48ffb349f2ff2baf170cd5d533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106672562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55dac24477c09674d0469032829783e0d39c0a862acfe0dd258b2fa7d63038b0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:58:59 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 24 Feb 2026 18:58:59 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 24 Feb 2026 18:58:59 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 24 Feb 2026 18:58:59 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 24 Feb 2026 18:58:59 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 18:58:59 GMT
WORKDIR /opt/emqx
# Tue, 24 Feb 2026 18:58:59 GMT
USER emqx
# Tue, 24 Feb 2026 18:58:59 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 24 Feb 2026 18:58:59 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 24 Feb 2026 18:58:59 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 24 Feb 2026 18:58:59 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 18:58:59 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00a1849c07c16e665c58b12aa62c89718fd84beec9fa1438c36923a797b8d83`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 76.5 MB (76531400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d83c8715f4a968cc8b0d47c8f4f8ebf93b60a41c7f5508ecfb04f98a52ce67e`  
		Last Modified: Tue, 24 Feb 2026 18:59:12 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:db4d2f7cdfc55c2ed654d228ef20f0c356742fe5095d1df8a882971f3e600fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc62f1776a4586af477312ec6e48141ff035e4707b2390f3b490f804d6c49ea`

```dockerfile
```

-	Layers:
	-	`sha256:1074a1e98da480a04d8502c065225855055485aa6d1fb25aad824d22543a03d6`  
		Last Modified: Tue, 24 Feb 2026 18:59:12 GMT  
		Size: 2.4 MB (2403752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ff77e088bb8c553b66b92183f270c68bc33d7961ee8e3b77b6109534528f1f8`  
		Last Modified: Tue, 24 Feb 2026 18:59:12 GMT  
		Size: 12.6 KB (12589 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8.8`

```console
$ docker pull emqx@sha256:2829687a7e7d14df0ad2a2d17d83c2002e9aacae5e663b8bda586fdaaa01e949
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8.8` - linux; amd64

```console
$ docker pull emqx@sha256:632b8250c5c1f3a4bfef7854a1b551b0c5112e7e49c776ffc9e244c78562afb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108404241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9154df55f910221401b1b3771a5136923d3c6115cc9e9682a36b9088053ccc25`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:52:39 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 24 Feb 2026 18:52:39 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 24 Feb 2026 18:52:39 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 24 Feb 2026 18:52:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 24 Feb 2026 18:52:39 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 18:52:39 GMT
WORKDIR /opt/emqx
# Tue, 24 Feb 2026 18:52:39 GMT
USER emqx
# Tue, 24 Feb 2026 18:52:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 24 Feb 2026 18:52:39 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 24 Feb 2026 18:52:39 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 24 Feb 2026 18:52:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 18:52:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a56cc393affa2cbe7c8277cd9b749f3121d5281ddfdfdd3fc8cd0d5ca81bf14`  
		Last Modified: Tue, 24 Feb 2026 18:52:54 GMT  
		Size: 78.6 MB (78624546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a504ce29c56ffc47e51bf9597d04ca558c968b91f51a8c9e26ed6edc89688039`  
		Last Modified: Tue, 24 Feb 2026 18:52:52 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.8` - unknown; unknown

```console
$ docker pull emqx@sha256:7545a82e901d7a10fc8761e9d03b7dc73ca157b3af4bf676cd0ee55d2b4045b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e08ecdf33aecce1e52292c3740ed6e92050e1b888aa8bb2380d47957f4adef4`

```dockerfile
```

-	Layers:
	-	`sha256:23b73ab6fcbdb172f7d1407dde8bc42754c7cc20d9f893de1d9bdff4e095a2c6`  
		Last Modified: Tue, 24 Feb 2026 18:52:52 GMT  
		Size: 2.4 MB (2403463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e070728fc870e46c950c41aa4807d5a48f2384bedbb0f94e19368ee692bc39c1`  
		Last Modified: Tue, 24 Feb 2026 18:52:52 GMT  
		Size: 12.5 KB (12486 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8.8` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:10af0712de4ae8b88bf07dd8266dee7f09857d48ffb349f2ff2baf170cd5d533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106672562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55dac24477c09674d0469032829783e0d39c0a862acfe0dd258b2fa7d63038b0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:58:59 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 24 Feb 2026 18:58:59 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 24 Feb 2026 18:58:59 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 24 Feb 2026 18:58:59 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 24 Feb 2026 18:58:59 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 18:58:59 GMT
WORKDIR /opt/emqx
# Tue, 24 Feb 2026 18:58:59 GMT
USER emqx
# Tue, 24 Feb 2026 18:58:59 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 24 Feb 2026 18:58:59 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 24 Feb 2026 18:58:59 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 24 Feb 2026 18:58:59 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 18:58:59 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00a1849c07c16e665c58b12aa62c89718fd84beec9fa1438c36923a797b8d83`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 76.5 MB (76531400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d83c8715f4a968cc8b0d47c8f4f8ebf93b60a41c7f5508ecfb04f98a52ce67e`  
		Last Modified: Tue, 24 Feb 2026 18:59:12 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.8` - unknown; unknown

```console
$ docker pull emqx@sha256:db4d2f7cdfc55c2ed654d228ef20f0c356742fe5095d1df8a882971f3e600fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc62f1776a4586af477312ec6e48141ff035e4707b2390f3b490f804d6c49ea`

```dockerfile
```

-	Layers:
	-	`sha256:1074a1e98da480a04d8502c065225855055485aa6d1fb25aad824d22543a03d6`  
		Last Modified: Tue, 24 Feb 2026 18:59:12 GMT  
		Size: 2.4 MB (2403752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ff77e088bb8c553b66b92183f270c68bc33d7961ee8e3b77b6109534528f1f8`  
		Last Modified: Tue, 24 Feb 2026 18:59:12 GMT  
		Size: 12.6 KB (12589 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:latest`

```console
$ docker pull emqx@sha256:2829687a7e7d14df0ad2a2d17d83c2002e9aacae5e663b8bda586fdaaa01e949
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:632b8250c5c1f3a4bfef7854a1b551b0c5112e7e49c776ffc9e244c78562afb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108404241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9154df55f910221401b1b3771a5136923d3c6115cc9e9682a36b9088053ccc25`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:52:39 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 24 Feb 2026 18:52:39 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 24 Feb 2026 18:52:39 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 24 Feb 2026 18:52:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 24 Feb 2026 18:52:39 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 18:52:39 GMT
WORKDIR /opt/emqx
# Tue, 24 Feb 2026 18:52:39 GMT
USER emqx
# Tue, 24 Feb 2026 18:52:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 24 Feb 2026 18:52:39 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 24 Feb 2026 18:52:39 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 24 Feb 2026 18:52:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 18:52:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a56cc393affa2cbe7c8277cd9b749f3121d5281ddfdfdd3fc8cd0d5ca81bf14`  
		Last Modified: Tue, 24 Feb 2026 18:52:54 GMT  
		Size: 78.6 MB (78624546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a504ce29c56ffc47e51bf9597d04ca558c968b91f51a8c9e26ed6edc89688039`  
		Last Modified: Tue, 24 Feb 2026 18:52:52 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:7545a82e901d7a10fc8761e9d03b7dc73ca157b3af4bf676cd0ee55d2b4045b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e08ecdf33aecce1e52292c3740ed6e92050e1b888aa8bb2380d47957f4adef4`

```dockerfile
```

-	Layers:
	-	`sha256:23b73ab6fcbdb172f7d1407dde8bc42754c7cc20d9f893de1d9bdff4e095a2c6`  
		Last Modified: Tue, 24 Feb 2026 18:52:52 GMT  
		Size: 2.4 MB (2403463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e070728fc870e46c950c41aa4807d5a48f2384bedbb0f94e19368ee692bc39c1`  
		Last Modified: Tue, 24 Feb 2026 18:52:52 GMT  
		Size: 12.5 KB (12486 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:10af0712de4ae8b88bf07dd8266dee7f09857d48ffb349f2ff2baf170cd5d533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106672562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55dac24477c09674d0469032829783e0d39c0a862acfe0dd258b2fa7d63038b0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 18:58:59 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 24 Feb 2026 18:58:59 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 24 Feb 2026 18:58:59 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 24 Feb 2026 18:58:59 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 24 Feb 2026 18:58:59 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 24 Feb 2026 18:58:59 GMT
WORKDIR /opt/emqx
# Tue, 24 Feb 2026 18:58:59 GMT
USER emqx
# Tue, 24 Feb 2026 18:58:59 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 24 Feb 2026 18:58:59 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 24 Feb 2026 18:58:59 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 24 Feb 2026 18:58:59 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 18:58:59 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00a1849c07c16e665c58b12aa62c89718fd84beec9fa1438c36923a797b8d83`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 76.5 MB (76531400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d83c8715f4a968cc8b0d47c8f4f8ebf93b60a41c7f5508ecfb04f98a52ce67e`  
		Last Modified: Tue, 24 Feb 2026 18:59:12 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:db4d2f7cdfc55c2ed654d228ef20f0c356742fe5095d1df8a882971f3e600fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc62f1776a4586af477312ec6e48141ff035e4707b2390f3b490f804d6c49ea`

```dockerfile
```

-	Layers:
	-	`sha256:1074a1e98da480a04d8502c065225855055485aa6d1fb25aad824d22543a03d6`  
		Last Modified: Tue, 24 Feb 2026 18:59:12 GMT  
		Size: 2.4 MB (2403752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ff77e088bb8c553b66b92183f270c68bc33d7961ee8e3b77b6109534528f1f8`  
		Last Modified: Tue, 24 Feb 2026 18:59:12 GMT  
		Size: 12.6 KB (12589 bytes)  
		MIME: application/vnd.in-toto+json
