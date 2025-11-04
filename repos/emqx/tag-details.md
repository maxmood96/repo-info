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
$ docker pull emqx@sha256:dd5c59d344e608b03cbb6aa39ed699d24a2bc9866e074d2f7ffc22d3ba9dc638
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
$ docker pull emqx@sha256:8daa96ee3e5b157aaaa6e05649620c3bbf7c4cfb668adf5c1bda3fc2c7d05872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106673648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc9ff7f1029b574cf65c9d2da6ff2cff4b9553dee9df9fe4d1ecacbc0dc65f9`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:18:28 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 04 Nov 2025 01:18:28 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 04 Nov 2025 01:18:28 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 04 Nov 2025 01:18:28 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 04 Nov 2025 01:18:28 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 01:18:28 GMT
WORKDIR /opt/emqx
# Tue, 04 Nov 2025 01:18:28 GMT
USER emqx
# Tue, 04 Nov 2025 01:18:28 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 04 Nov 2025 01:18:28 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 04 Nov 2025 01:18:28 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 04 Nov 2025 01:18:28 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:18:28 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391720a3556ed31cee8f9be412ebcf8e5c5d332f062f5325ad401ed1a9d20029`  
		Last Modified: Tue, 04 Nov 2025 01:18:59 GMT  
		Size: 76.5 MB (76530287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5beb909533634e0e2f79c928ee74a4b9497bc56fb9414a8a72bfcb3335a02069`  
		Last Modified: Tue, 04 Nov 2025 01:18:56 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:53ee5dd7af46a6600d72e4d64cc751254a03b165567e0bba38d7135821fcdc22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4743917d3bf200ffd44c630e7077fee06ea66c99e37817c6399005dfc3dc72a2`

```dockerfile
```

-	Layers:
	-	`sha256:888263e2e222dbb8a55cbc7361d01efe78289a547fd4a018a4eefe8ddd9eb3c3`  
		Last Modified: Tue, 04 Nov 2025 12:27:19 GMT  
		Size: 2.4 MB (2403624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af6186b1967ca4983cf1fe83da4836dacc3a0378766717b3131516522abe1dc4`  
		Last Modified: Tue, 04 Nov 2025 12:27:20 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7`

```console
$ docker pull emqx@sha256:a29e40e5ebf0940db3f89377df72817460b8fc7c262cd392da5c5e40d48c440f
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
$ docker pull emqx@sha256:682ccb7738bb61a836a7c936142cddb476a73f85c438ba5bb61602721a182b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121818691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ffb8cd08170bb941e35afda98fb36ea4624ae50e37f923343a8f49b9f811725`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:16:48 GMT
ENV EMQX_VERSION=5.7.2
# Tue, 04 Nov 2025 00:16:48 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Tue, 04 Nov 2025 00:16:48 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Tue, 04 Nov 2025 00:16:48 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 04 Nov 2025 00:16:48 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 00:16:48 GMT
WORKDIR /opt/emqx
# Tue, 04 Nov 2025 00:16:48 GMT
USER emqx
# Tue, 04 Nov 2025 00:16:48 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 04 Nov 2025 00:16:48 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 04 Nov 2025 00:16:48 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 04 Nov 2025 00:16:48 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:16:48 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c7a39705fadb239ba3422ec663e2e2f1b80a14475fc15f80e05f5949227bca`  
		Last Modified: Tue, 04 Nov 2025 00:17:20 GMT  
		Size: 93.7 MB (93715254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ec3d441dbdb02746057b1be1e8fa9170c3fc00fb6d99be52aaf7fcdafa0c2f`  
		Last Modified: Tue, 04 Nov 2025 00:17:11 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:a1a0bfbaffc5ec2eece73185c5a6c75a722b4c88e1d58edd2e0d57975e222768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2062450b87af1f37494c29ddadb70c4b8fce05976ee9b534a07e0f12ecfbc03e`

```dockerfile
```

-	Layers:
	-	`sha256:a645a216f9ee67d5f8d1d2796809f20921fbf130422fcbc9efdd4595c41bc73b`  
		Last Modified: Tue, 04 Nov 2025 12:27:25 GMT  
		Size: 2.8 MB (2751644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:555f21f16eaaaed8713bc4a9f6585f7da2e61390a9a0c879c657c6831bf47f89`  
		Last Modified: Tue, 04 Nov 2025 12:27:25 GMT  
		Size: 12.0 KB (11988 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7.2`

```console
$ docker pull emqx@sha256:a29e40e5ebf0940db3f89377df72817460b8fc7c262cd392da5c5e40d48c440f
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
$ docker pull emqx@sha256:682ccb7738bb61a836a7c936142cddb476a73f85c438ba5bb61602721a182b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121818691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ffb8cd08170bb941e35afda98fb36ea4624ae50e37f923343a8f49b9f811725`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:16:48 GMT
ENV EMQX_VERSION=5.7.2
# Tue, 04 Nov 2025 00:16:48 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Tue, 04 Nov 2025 00:16:48 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Tue, 04 Nov 2025 00:16:48 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 04 Nov 2025 00:16:48 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 00:16:48 GMT
WORKDIR /opt/emqx
# Tue, 04 Nov 2025 00:16:48 GMT
USER emqx
# Tue, 04 Nov 2025 00:16:48 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 04 Nov 2025 00:16:48 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 04 Nov 2025 00:16:48 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 04 Nov 2025 00:16:48 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 00:16:48 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c7a39705fadb239ba3422ec663e2e2f1b80a14475fc15f80e05f5949227bca`  
		Last Modified: Tue, 04 Nov 2025 00:17:20 GMT  
		Size: 93.7 MB (93715254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ec3d441dbdb02746057b1be1e8fa9170c3fc00fb6d99be52aaf7fcdafa0c2f`  
		Last Modified: Tue, 04 Nov 2025 00:17:11 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:a1a0bfbaffc5ec2eece73185c5a6c75a722b4c88e1d58edd2e0d57975e222768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2062450b87af1f37494c29ddadb70c4b8fce05976ee9b534a07e0f12ecfbc03e`

```dockerfile
```

-	Layers:
	-	`sha256:a645a216f9ee67d5f8d1d2796809f20921fbf130422fcbc9efdd4595c41bc73b`  
		Last Modified: Tue, 04 Nov 2025 12:27:25 GMT  
		Size: 2.8 MB (2751644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:555f21f16eaaaed8713bc4a9f6585f7da2e61390a9a0c879c657c6831bf47f89`  
		Last Modified: Tue, 04 Nov 2025 12:27:25 GMT  
		Size: 12.0 KB (11988 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8`

```console
$ docker pull emqx@sha256:dd5c59d344e608b03cbb6aa39ed699d24a2bc9866e074d2f7ffc22d3ba9dc638
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
$ docker pull emqx@sha256:8daa96ee3e5b157aaaa6e05649620c3bbf7c4cfb668adf5c1bda3fc2c7d05872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106673648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc9ff7f1029b574cf65c9d2da6ff2cff4b9553dee9df9fe4d1ecacbc0dc65f9`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:18:28 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 04 Nov 2025 01:18:28 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 04 Nov 2025 01:18:28 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 04 Nov 2025 01:18:28 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 04 Nov 2025 01:18:28 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 01:18:28 GMT
WORKDIR /opt/emqx
# Tue, 04 Nov 2025 01:18:28 GMT
USER emqx
# Tue, 04 Nov 2025 01:18:28 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 04 Nov 2025 01:18:28 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 04 Nov 2025 01:18:28 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 04 Nov 2025 01:18:28 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:18:28 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391720a3556ed31cee8f9be412ebcf8e5c5d332f062f5325ad401ed1a9d20029`  
		Last Modified: Tue, 04 Nov 2025 01:18:59 GMT  
		Size: 76.5 MB (76530287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5beb909533634e0e2f79c928ee74a4b9497bc56fb9414a8a72bfcb3335a02069`  
		Last Modified: Tue, 04 Nov 2025 01:18:56 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:53ee5dd7af46a6600d72e4d64cc751254a03b165567e0bba38d7135821fcdc22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4743917d3bf200ffd44c630e7077fee06ea66c99e37817c6399005dfc3dc72a2`

```dockerfile
```

-	Layers:
	-	`sha256:888263e2e222dbb8a55cbc7361d01efe78289a547fd4a018a4eefe8ddd9eb3c3`  
		Last Modified: Tue, 04 Nov 2025 12:27:19 GMT  
		Size: 2.4 MB (2403624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af6186b1967ca4983cf1fe83da4836dacc3a0378766717b3131516522abe1dc4`  
		Last Modified: Tue, 04 Nov 2025 12:27:20 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8.8`

```console
$ docker pull emqx@sha256:dd5c59d344e608b03cbb6aa39ed699d24a2bc9866e074d2f7ffc22d3ba9dc638
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
$ docker pull emqx@sha256:8daa96ee3e5b157aaaa6e05649620c3bbf7c4cfb668adf5c1bda3fc2c7d05872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106673648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc9ff7f1029b574cf65c9d2da6ff2cff4b9553dee9df9fe4d1ecacbc0dc65f9`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:18:28 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 04 Nov 2025 01:18:28 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 04 Nov 2025 01:18:28 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 04 Nov 2025 01:18:28 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 04 Nov 2025 01:18:28 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 01:18:28 GMT
WORKDIR /opt/emqx
# Tue, 04 Nov 2025 01:18:28 GMT
USER emqx
# Tue, 04 Nov 2025 01:18:28 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 04 Nov 2025 01:18:28 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 04 Nov 2025 01:18:28 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 04 Nov 2025 01:18:28 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:18:28 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391720a3556ed31cee8f9be412ebcf8e5c5d332f062f5325ad401ed1a9d20029`  
		Last Modified: Tue, 04 Nov 2025 01:18:59 GMT  
		Size: 76.5 MB (76530287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5beb909533634e0e2f79c928ee74a4b9497bc56fb9414a8a72bfcb3335a02069`  
		Last Modified: Tue, 04 Nov 2025 01:18:56 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.8` - unknown; unknown

```console
$ docker pull emqx@sha256:53ee5dd7af46a6600d72e4d64cc751254a03b165567e0bba38d7135821fcdc22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4743917d3bf200ffd44c630e7077fee06ea66c99e37817c6399005dfc3dc72a2`

```dockerfile
```

-	Layers:
	-	`sha256:888263e2e222dbb8a55cbc7361d01efe78289a547fd4a018a4eefe8ddd9eb3c3`  
		Last Modified: Tue, 04 Nov 2025 12:27:19 GMT  
		Size: 2.4 MB (2403624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af6186b1967ca4983cf1fe83da4836dacc3a0378766717b3131516522abe1dc4`  
		Last Modified: Tue, 04 Nov 2025 12:27:20 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:latest`

```console
$ docker pull emqx@sha256:dd5c59d344e608b03cbb6aa39ed699d24a2bc9866e074d2f7ffc22d3ba9dc638
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
$ docker pull emqx@sha256:8daa96ee3e5b157aaaa6e05649620c3bbf7c4cfb668adf5c1bda3fc2c7d05872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106673648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc9ff7f1029b574cf65c9d2da6ff2cff4b9553dee9df9fe4d1ecacbc0dc65f9`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:18:28 GMT
ENV EMQX_VERSION=5.8.8
# Tue, 04 Nov 2025 01:18:28 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Tue, 04 Nov 2025 01:18:28 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Tue, 04 Nov 2025 01:18:28 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 04 Nov 2025 01:18:28 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 04 Nov 2025 01:18:28 GMT
WORKDIR /opt/emqx
# Tue, 04 Nov 2025 01:18:28 GMT
USER emqx
# Tue, 04 Nov 2025 01:18:28 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 04 Nov 2025 01:18:28 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 04 Nov 2025 01:18:28 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 04 Nov 2025 01:18:28 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 04 Nov 2025 01:18:28 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391720a3556ed31cee8f9be412ebcf8e5c5d332f062f5325ad401ed1a9d20029`  
		Last Modified: Tue, 04 Nov 2025 01:18:59 GMT  
		Size: 76.5 MB (76530287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5beb909533634e0e2f79c928ee74a4b9497bc56fb9414a8a72bfcb3335a02069`  
		Last Modified: Tue, 04 Nov 2025 01:18:56 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:53ee5dd7af46a6600d72e4d64cc751254a03b165567e0bba38d7135821fcdc22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4743917d3bf200ffd44c630e7077fee06ea66c99e37817c6399005dfc3dc72a2`

```dockerfile
```

-	Layers:
	-	`sha256:888263e2e222dbb8a55cbc7361d01efe78289a547fd4a018a4eefe8ddd9eb3c3`  
		Last Modified: Tue, 04 Nov 2025 12:27:19 GMT  
		Size: 2.4 MB (2403624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af6186b1967ca4983cf1fe83da4836dacc3a0378766717b3131516522abe1dc4`  
		Last Modified: Tue, 04 Nov 2025 12:27:20 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json
