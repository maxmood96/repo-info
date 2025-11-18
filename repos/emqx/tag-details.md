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
$ docker pull emqx@sha256:d45b4cdccd6f0381461b57de2d83e7c45920b4829827443cfc599e581d9d4f3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:de575cc9c3f2297495e7c20a6df5f8ad56f38671e67119e533f81a2d26b0bfde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108401110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8d091c7c9e4b039f92a2f4ffaccc2d52f7e51db5807e9da98ce07fb9fd8819c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 07:56:49 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 04 Nov 2025 07:56:49 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 04 Nov 2025 07:56:49 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 04 Nov 2025 07:56:49 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 04 Nov 2025 07:56:49 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 07:56:49 GMT
WORKDIR /opt/emqx
# Tue, 04 Nov 2025 07:56:49 GMT
USER emqx
# Tue, 04 Nov 2025 07:56:49 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 04 Nov 2025 07:56:49 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 04 Nov 2025 07:56:49 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 04 Nov 2025 07:56:49 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 07:56:49 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1cf32effd94989dd74a148d877a700d4243f11e8ad8569f6eca908e7487af8`  
		Last Modified: Tue, 04 Nov 2025 07:57:19 GMT  
		Size: 78.6 MB (78621941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712c14e66fdf14adc2b18bbdbbd97fce5f48a058da7391ad30b29661736a0eb0`  
		Last Modified: Tue, 04 Nov 2025 07:57:09 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:6a1194f7197fd809825ed747ca84f1c67a1d6720c616e5c4a0d37571d957d0a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7179793449735effc426b818d5b79351953eef79b9f358fcf9c8ad2ca21c48f9`

```dockerfile
```

-	Layers:
	-	`sha256:d72c18cf09dbec93333b00842a4b4c574e709129d3f8a193c8deb1d3e2696236`  
		Last Modified: Tue, 04 Nov 2025 09:27:16 GMT  
		Size: 2.4 MB (2403335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4312173f4d9534c705996a043146519da9ac5973889faa4ca2a9de23bdffe01`  
		Last Modified: Tue, 04 Nov 2025 09:27:16 GMT  
		Size: 12.5 KB (12486 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:2914f34446a28e83672a4ebad6a6f09c0e78d3f4da354b48d9d42a75941dd5a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106670092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d37d9b08cd65f9d60e490f0326ade1f02f60189074ffc39c719827133cf850f1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:48 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 18 Nov 2025 02:16:48 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 18 Nov 2025 02:16:48 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 18 Nov 2025 02:16:48 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 18 Nov 2025 02:16:48 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 02:16:48 GMT
WORKDIR /opt/emqx
# Tue, 18 Nov 2025 02:16:48 GMT
USER emqx
# Tue, 18 Nov 2025 02:16:48 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 18 Nov 2025 02:16:48 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 18 Nov 2025 02:16:48 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 18 Nov 2025 02:16:48 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:16:48 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e541109d4a769feb4626dcb0f4d07dedc5e2f5a9d2a97935eb0db4bc60a5d668`  
		Last Modified: Tue, 18 Nov 2025 02:17:18 GMT  
		Size: 76.5 MB (76530421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836f769a8ad0aa01680cea4551d1e8e49c50f2305aaa73034cb63d92ba0d46c4`  
		Last Modified: Tue, 18 Nov 2025 02:17:09 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:377863c25ed05f4cf152843af2493ab4a2752e1dbc6b34c382bcbf6ad07dba1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bbeb07447af4f21036c5a68de8233d61e77c6eb1520fa237dd644404f879d4`

```dockerfile
```

-	Layers:
	-	`sha256:5aebafb940c0c778fedd2bd4fdf2379fb796a24dd8cb14a1e732b2517c8f23c3`  
		Last Modified: Tue, 18 Nov 2025 03:30:35 GMT  
		Size: 2.4 MB (2403654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29d6ce50e68a41360a096f23126a443a9875f2019cdae545b78f1199822f0a76`  
		Last Modified: Tue, 18 Nov 2025 03:30:36 GMT  
		Size: 12.6 KB (12589 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7`

```console
$ docker pull emqx@sha256:405c49c5a95c2978d05bf772bb32eaa544aeccfe6fec60b4815c38c8f48b62ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7` - linux; amd64

```console
$ docker pull emqx@sha256:a7a408c46e788d87530d7ad2fcb602649ff0ab01725f6355422a8efefe34348a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125384853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8804f098c46410f15fe69998ec7ce4f27af4fb373c1904f8e300fe666a7b63b7`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:16:43 GMT
ENV EMQX_VERSION=5.7.2
# Tue, 04 Nov 2025 00:16:43 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Tue, 04 Nov 2025 00:16:43 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Tue, 04 Nov 2025 00:16:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 04 Nov 2025 00:16:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 00:16:43 GMT
WORKDIR /opt/emqx
# Tue, 04 Nov 2025 00:16:43 GMT
USER emqx
# Tue, 04 Nov 2025 00:16:43 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 04 Nov 2025 00:16:43 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 04 Nov 2025 00:16:43 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 04 Nov 2025 00:16:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:16:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f4e8ffa5a7061027b4d7ee0e147118262589236b269198333433622e115019`  
		Last Modified: Tue, 04 Nov 2025 00:17:14 GMT  
		Size: 97.2 MB (97155222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273aa7800906947b0a95214435bf7eb1dedf20b0fcfc5f859020a5bfa166d2d9`  
		Last Modified: Tue, 04 Nov 2025 00:17:04 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:862181fc56e4605d596e98e9a2b7671ea1e5e2f9475f346cdacd3c9e8fad66e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee1de4698254b683f4365743b79957213e708999dfad5c1e5de47126190c153`

```dockerfile
```

-	Layers:
	-	`sha256:a57bd8ff5d4907cf5d1cf0db461e56d13312ae147bf3139ca30937cf0c1137ac`  
		Last Modified: Tue, 04 Nov 2025 09:27:22 GMT  
		Size: 2.8 MB (2751388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:856ee25e02eabe5d7816ea8969cb615ba9b9f1026891d6b5b1cd3136c01e8d68`  
		Last Modified: Tue, 04 Nov 2025 09:27:24 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8dd176f815a25b03e1e890aa0f8d69440a2b2dc3c3b8b1e20ceca36492a2699a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121818439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1059914f9f4a03cb7d34ff2b8b63b4e32ac71537cb8a7e5512e31fa35c6fa1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:14:11 GMT
ENV EMQX_VERSION=5.7.2
# Tue, 18 Nov 2025 02:14:11 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Tue, 18 Nov 2025 02:14:11 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Tue, 18 Nov 2025 02:14:11 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 18 Nov 2025 02:14:11 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 02:14:11 GMT
WORKDIR /opt/emqx
# Tue, 18 Nov 2025 02:14:11 GMT
USER emqx
# Tue, 18 Nov 2025 02:14:11 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 18 Nov 2025 02:14:11 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 18 Nov 2025 02:14:12 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 18 Nov 2025 02:14:12 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:14:12 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d526c0043df2310fc7956a7d5b8fee30f7b1baa9ed990bd2eb9ed4079f7db674`  
		Last Modified: Tue, 18 Nov 2025 02:14:59 GMT  
		Size: 93.7 MB (93715171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514a376a62d1f5c69acc4ca0a77576694629ba819d8f43651e13082aff9a2220`  
		Last Modified: Tue, 18 Nov 2025 02:14:48 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:3b1705652cd4eb5650e74614edaa5d5ff915433ac5c7c6a009862448ebe5b1b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172e0218f632dbd46ebd950dfe4380b601012fc68cbd45d26e47c4066908a501`

```dockerfile
```

-	Layers:
	-	`sha256:b6fc605599f1d5602815447fae8b4dbb80e49a9bf516fd63adcb44bf74f532b2`  
		Last Modified: Tue, 18 Nov 2025 03:30:41 GMT  
		Size: 2.8 MB (2751644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ae369c3d4bd51fa2545bec90a1106320df4829ec88330c726aae0f779781f93`  
		Last Modified: Tue, 18 Nov 2025 03:30:42 GMT  
		Size: 12.0 KB (11988 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7.2`

```console
$ docker pull emqx@sha256:405c49c5a95c2978d05bf772bb32eaa544aeccfe6fec60b4815c38c8f48b62ca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7.2` - linux; amd64

```console
$ docker pull emqx@sha256:a7a408c46e788d87530d7ad2fcb602649ff0ab01725f6355422a8efefe34348a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125384853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8804f098c46410f15fe69998ec7ce4f27af4fb373c1904f8e300fe666a7b63b7`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:16:43 GMT
ENV EMQX_VERSION=5.7.2
# Tue, 04 Nov 2025 00:16:43 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Tue, 04 Nov 2025 00:16:43 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Tue, 04 Nov 2025 00:16:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 04 Nov 2025 00:16:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 00:16:43 GMT
WORKDIR /opt/emqx
# Tue, 04 Nov 2025 00:16:43 GMT
USER emqx
# Tue, 04 Nov 2025 00:16:43 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 04 Nov 2025 00:16:43 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 04 Nov 2025 00:16:43 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 04 Nov 2025 00:16:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:16:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f4e8ffa5a7061027b4d7ee0e147118262589236b269198333433622e115019`  
		Last Modified: Tue, 04 Nov 2025 00:17:14 GMT  
		Size: 97.2 MB (97155222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273aa7800906947b0a95214435bf7eb1dedf20b0fcfc5f859020a5bfa166d2d9`  
		Last Modified: Tue, 04 Nov 2025 00:17:04 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:862181fc56e4605d596e98e9a2b7671ea1e5e2f9475f346cdacd3c9e8fad66e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee1de4698254b683f4365743b79957213e708999dfad5c1e5de47126190c153`

```dockerfile
```

-	Layers:
	-	`sha256:a57bd8ff5d4907cf5d1cf0db461e56d13312ae147bf3139ca30937cf0c1137ac`  
		Last Modified: Tue, 04 Nov 2025 09:27:22 GMT  
		Size: 2.8 MB (2751388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:856ee25e02eabe5d7816ea8969cb615ba9b9f1026891d6b5b1cd3136c01e8d68`  
		Last Modified: Tue, 04 Nov 2025 09:27:24 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8dd176f815a25b03e1e890aa0f8d69440a2b2dc3c3b8b1e20ceca36492a2699a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121818439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1059914f9f4a03cb7d34ff2b8b63b4e32ac71537cb8a7e5512e31fa35c6fa1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:14:11 GMT
ENV EMQX_VERSION=5.7.2
# Tue, 18 Nov 2025 02:14:11 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Tue, 18 Nov 2025 02:14:11 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Tue, 18 Nov 2025 02:14:11 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 18 Nov 2025 02:14:11 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 02:14:11 GMT
WORKDIR /opt/emqx
# Tue, 18 Nov 2025 02:14:11 GMT
USER emqx
# Tue, 18 Nov 2025 02:14:11 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 18 Nov 2025 02:14:11 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 18 Nov 2025 02:14:12 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 18 Nov 2025 02:14:12 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:14:12 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d526c0043df2310fc7956a7d5b8fee30f7b1baa9ed990bd2eb9ed4079f7db674`  
		Last Modified: Tue, 18 Nov 2025 02:14:59 GMT  
		Size: 93.7 MB (93715171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514a376a62d1f5c69acc4ca0a77576694629ba819d8f43651e13082aff9a2220`  
		Last Modified: Tue, 18 Nov 2025 02:14:48 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:3b1705652cd4eb5650e74614edaa5d5ff915433ac5c7c6a009862448ebe5b1b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172e0218f632dbd46ebd950dfe4380b601012fc68cbd45d26e47c4066908a501`

```dockerfile
```

-	Layers:
	-	`sha256:b6fc605599f1d5602815447fae8b4dbb80e49a9bf516fd63adcb44bf74f532b2`  
		Last Modified: Tue, 18 Nov 2025 03:30:41 GMT  
		Size: 2.8 MB (2751644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ae369c3d4bd51fa2545bec90a1106320df4829ec88330c726aae0f779781f93`  
		Last Modified: Tue, 18 Nov 2025 03:30:42 GMT  
		Size: 12.0 KB (11988 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8`

```console
$ docker pull emqx@sha256:d45b4cdccd6f0381461b57de2d83e7c45920b4829827443cfc599e581d9d4f3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8` - linux; amd64

```console
$ docker pull emqx@sha256:de575cc9c3f2297495e7c20a6df5f8ad56f38671e67119e533f81a2d26b0bfde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108401110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8d091c7c9e4b039f92a2f4ffaccc2d52f7e51db5807e9da98ce07fb9fd8819c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 07:56:49 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 04 Nov 2025 07:56:49 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 04 Nov 2025 07:56:49 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 04 Nov 2025 07:56:49 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 04 Nov 2025 07:56:49 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 07:56:49 GMT
WORKDIR /opt/emqx
# Tue, 04 Nov 2025 07:56:49 GMT
USER emqx
# Tue, 04 Nov 2025 07:56:49 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 04 Nov 2025 07:56:49 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 04 Nov 2025 07:56:49 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 04 Nov 2025 07:56:49 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 07:56:49 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1cf32effd94989dd74a148d877a700d4243f11e8ad8569f6eca908e7487af8`  
		Last Modified: Tue, 04 Nov 2025 07:57:19 GMT  
		Size: 78.6 MB (78621941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712c14e66fdf14adc2b18bbdbbd97fce5f48a058da7391ad30b29661736a0eb0`  
		Last Modified: Tue, 04 Nov 2025 07:57:09 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:6a1194f7197fd809825ed747ca84f1c67a1d6720c616e5c4a0d37571d957d0a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7179793449735effc426b818d5b79351953eef79b9f358fcf9c8ad2ca21c48f9`

```dockerfile
```

-	Layers:
	-	`sha256:d72c18cf09dbec93333b00842a4b4c574e709129d3f8a193c8deb1d3e2696236`  
		Last Modified: Tue, 04 Nov 2025 09:27:16 GMT  
		Size: 2.4 MB (2403335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4312173f4d9534c705996a043146519da9ac5973889faa4ca2a9de23bdffe01`  
		Last Modified: Tue, 04 Nov 2025 09:27:16 GMT  
		Size: 12.5 KB (12486 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:2914f34446a28e83672a4ebad6a6f09c0e78d3f4da354b48d9d42a75941dd5a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106670092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d37d9b08cd65f9d60e490f0326ade1f02f60189074ffc39c719827133cf850f1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:48 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 18 Nov 2025 02:16:48 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 18 Nov 2025 02:16:48 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 18 Nov 2025 02:16:48 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 18 Nov 2025 02:16:48 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 02:16:48 GMT
WORKDIR /opt/emqx
# Tue, 18 Nov 2025 02:16:48 GMT
USER emqx
# Tue, 18 Nov 2025 02:16:48 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 18 Nov 2025 02:16:48 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 18 Nov 2025 02:16:48 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 18 Nov 2025 02:16:48 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:16:48 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e541109d4a769feb4626dcb0f4d07dedc5e2f5a9d2a97935eb0db4bc60a5d668`  
		Last Modified: Tue, 18 Nov 2025 02:17:18 GMT  
		Size: 76.5 MB (76530421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836f769a8ad0aa01680cea4551d1e8e49c50f2305aaa73034cb63d92ba0d46c4`  
		Last Modified: Tue, 18 Nov 2025 02:17:09 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:377863c25ed05f4cf152843af2493ab4a2752e1dbc6b34c382bcbf6ad07dba1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bbeb07447af4f21036c5a68de8233d61e77c6eb1520fa237dd644404f879d4`

```dockerfile
```

-	Layers:
	-	`sha256:5aebafb940c0c778fedd2bd4fdf2379fb796a24dd8cb14a1e732b2517c8f23c3`  
		Last Modified: Tue, 18 Nov 2025 03:30:35 GMT  
		Size: 2.4 MB (2403654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29d6ce50e68a41360a096f23126a443a9875f2019cdae545b78f1199822f0a76`  
		Last Modified: Tue, 18 Nov 2025 03:30:36 GMT  
		Size: 12.6 KB (12589 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8.8`

```console
$ docker pull emqx@sha256:d45b4cdccd6f0381461b57de2d83e7c45920b4829827443cfc599e581d9d4f3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8.8` - linux; amd64

```console
$ docker pull emqx@sha256:de575cc9c3f2297495e7c20a6df5f8ad56f38671e67119e533f81a2d26b0bfde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108401110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8d091c7c9e4b039f92a2f4ffaccc2d52f7e51db5807e9da98ce07fb9fd8819c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 07:56:49 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 04 Nov 2025 07:56:49 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 04 Nov 2025 07:56:49 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 04 Nov 2025 07:56:49 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 04 Nov 2025 07:56:49 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 07:56:49 GMT
WORKDIR /opt/emqx
# Tue, 04 Nov 2025 07:56:49 GMT
USER emqx
# Tue, 04 Nov 2025 07:56:49 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 04 Nov 2025 07:56:49 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 04 Nov 2025 07:56:49 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 04 Nov 2025 07:56:49 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 07:56:49 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1cf32effd94989dd74a148d877a700d4243f11e8ad8569f6eca908e7487af8`  
		Last Modified: Tue, 04 Nov 2025 07:57:19 GMT  
		Size: 78.6 MB (78621941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712c14e66fdf14adc2b18bbdbbd97fce5f48a058da7391ad30b29661736a0eb0`  
		Last Modified: Tue, 04 Nov 2025 07:57:09 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.8` - unknown; unknown

```console
$ docker pull emqx@sha256:6a1194f7197fd809825ed747ca84f1c67a1d6720c616e5c4a0d37571d957d0a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7179793449735effc426b818d5b79351953eef79b9f358fcf9c8ad2ca21c48f9`

```dockerfile
```

-	Layers:
	-	`sha256:d72c18cf09dbec93333b00842a4b4c574e709129d3f8a193c8deb1d3e2696236`  
		Last Modified: Tue, 04 Nov 2025 09:27:16 GMT  
		Size: 2.4 MB (2403335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4312173f4d9534c705996a043146519da9ac5973889faa4ca2a9de23bdffe01`  
		Last Modified: Tue, 04 Nov 2025 09:27:16 GMT  
		Size: 12.5 KB (12486 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8.8` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:2914f34446a28e83672a4ebad6a6f09c0e78d3f4da354b48d9d42a75941dd5a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106670092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d37d9b08cd65f9d60e490f0326ade1f02f60189074ffc39c719827133cf850f1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:48 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 18 Nov 2025 02:16:48 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 18 Nov 2025 02:16:48 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 18 Nov 2025 02:16:48 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 18 Nov 2025 02:16:48 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 02:16:48 GMT
WORKDIR /opt/emqx
# Tue, 18 Nov 2025 02:16:48 GMT
USER emqx
# Tue, 18 Nov 2025 02:16:48 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 18 Nov 2025 02:16:48 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 18 Nov 2025 02:16:48 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 18 Nov 2025 02:16:48 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:16:48 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e541109d4a769feb4626dcb0f4d07dedc5e2f5a9d2a97935eb0db4bc60a5d668`  
		Last Modified: Tue, 18 Nov 2025 02:17:18 GMT  
		Size: 76.5 MB (76530421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836f769a8ad0aa01680cea4551d1e8e49c50f2305aaa73034cb63d92ba0d46c4`  
		Last Modified: Tue, 18 Nov 2025 02:17:09 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.8` - unknown; unknown

```console
$ docker pull emqx@sha256:377863c25ed05f4cf152843af2493ab4a2752e1dbc6b34c382bcbf6ad07dba1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bbeb07447af4f21036c5a68de8233d61e77c6eb1520fa237dd644404f879d4`

```dockerfile
```

-	Layers:
	-	`sha256:5aebafb940c0c778fedd2bd4fdf2379fb796a24dd8cb14a1e732b2517c8f23c3`  
		Last Modified: Tue, 18 Nov 2025 03:30:35 GMT  
		Size: 2.4 MB (2403654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29d6ce50e68a41360a096f23126a443a9875f2019cdae545b78f1199822f0a76`  
		Last Modified: Tue, 18 Nov 2025 03:30:36 GMT  
		Size: 12.6 KB (12589 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:latest`

```console
$ docker pull emqx@sha256:d45b4cdccd6f0381461b57de2d83e7c45920b4829827443cfc599e581d9d4f3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:de575cc9c3f2297495e7c20a6df5f8ad56f38671e67119e533f81a2d26b0bfde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108401110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8d091c7c9e4b039f92a2f4ffaccc2d52f7e51db5807e9da98ce07fb9fd8819c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 07:56:49 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 04 Nov 2025 07:56:49 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 04 Nov 2025 07:56:49 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 04 Nov 2025 07:56:49 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 04 Nov 2025 07:56:49 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 07:56:49 GMT
WORKDIR /opt/emqx
# Tue, 04 Nov 2025 07:56:49 GMT
USER emqx
# Tue, 04 Nov 2025 07:56:49 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 04 Nov 2025 07:56:49 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 04 Nov 2025 07:56:49 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 04 Nov 2025 07:56:49 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 07:56:49 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1cf32effd94989dd74a148d877a700d4243f11e8ad8569f6eca908e7487af8`  
		Last Modified: Tue, 04 Nov 2025 07:57:19 GMT  
		Size: 78.6 MB (78621941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712c14e66fdf14adc2b18bbdbbd97fce5f48a058da7391ad30b29661736a0eb0`  
		Last Modified: Tue, 04 Nov 2025 07:57:09 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:6a1194f7197fd809825ed747ca84f1c67a1d6720c616e5c4a0d37571d957d0a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7179793449735effc426b818d5b79351953eef79b9f358fcf9c8ad2ca21c48f9`

```dockerfile
```

-	Layers:
	-	`sha256:d72c18cf09dbec93333b00842a4b4c574e709129d3f8a193c8deb1d3e2696236`  
		Last Modified: Tue, 04 Nov 2025 09:27:16 GMT  
		Size: 2.4 MB (2403335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4312173f4d9534c705996a043146519da9ac5973889faa4ca2a9de23bdffe01`  
		Last Modified: Tue, 04 Nov 2025 09:27:16 GMT  
		Size: 12.5 KB (12486 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:2914f34446a28e83672a4ebad6a6f09c0e78d3f4da354b48d9d42a75941dd5a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106670092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d37d9b08cd65f9d60e490f0326ade1f02f60189074ffc39c719827133cf850f1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 02:16:48 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 18 Nov 2025 02:16:48 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 18 Nov 2025 02:16:48 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 18 Nov 2025 02:16:48 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 18 Nov 2025 02:16:48 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 18 Nov 2025 02:16:48 GMT
WORKDIR /opt/emqx
# Tue, 18 Nov 2025 02:16:48 GMT
USER emqx
# Tue, 18 Nov 2025 02:16:48 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 18 Nov 2025 02:16:48 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 18 Nov 2025 02:16:48 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 18 Nov 2025 02:16:48 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 18 Nov 2025 02:16:48 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e541109d4a769feb4626dcb0f4d07dedc5e2f5a9d2a97935eb0db4bc60a5d668`  
		Last Modified: Tue, 18 Nov 2025 02:17:18 GMT  
		Size: 76.5 MB (76530421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836f769a8ad0aa01680cea4551d1e8e49c50f2305aaa73034cb63d92ba0d46c4`  
		Last Modified: Tue, 18 Nov 2025 02:17:09 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:377863c25ed05f4cf152843af2493ab4a2752e1dbc6b34c382bcbf6ad07dba1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74bbeb07447af4f21036c5a68de8233d61e77c6eb1520fa237dd644404f879d4`

```dockerfile
```

-	Layers:
	-	`sha256:5aebafb940c0c778fedd2bd4fdf2379fb796a24dd8cb14a1e732b2517c8f23c3`  
		Last Modified: Tue, 18 Nov 2025 03:30:35 GMT  
		Size: 2.4 MB (2403654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29d6ce50e68a41360a096f23126a443a9875f2019cdae545b78f1199822f0a76`  
		Last Modified: Tue, 18 Nov 2025 03:30:36 GMT  
		Size: 12.6 KB (12589 bytes)  
		MIME: application/vnd.in-toto+json
