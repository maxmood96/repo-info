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
$ docker pull emqx@sha256:516df7073402cadd42995460e69600d0416a4a9329338cd8f5fa6831649192db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:cacf91d9eb4b8ec3a2aca265ce5f17e4dcaacaa6c03d1551e24cc6aab78fe218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108399110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49f29a0e9115ef92a20e8ab16cc9eab40c7dd7280c49c2fe640e6825c55635dd`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:56 GMT
ENV EMQX_VERSION=5.8.8
# Mon, 08 Dec 2025 22:33:56 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Mon, 08 Dec 2025 22:33:56 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Mon, 08 Dec 2025 22:33:56 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 08 Dec 2025 22:33:56 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 08 Dec 2025 22:33:56 GMT
WORKDIR /opt/emqx
# Mon, 08 Dec 2025 22:33:56 GMT
USER emqx
# Mon, 08 Dec 2025 22:33:56 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 08 Dec 2025 22:33:56 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 08 Dec 2025 22:33:56 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 08 Dec 2025 22:33:56 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:33:56 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee851dbc9e6748a1a8e982e716b5427e46535cc7b781a813dfd98be52bc7eb6`  
		Last Modified: Mon, 08 Dec 2025 22:34:23 GMT  
		Size: 78.6 MB (78621554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a2f7fb8635a90190ce542685acfd0492631545f2206d8a7fbc539d7455d47c`  
		Last Modified: Mon, 08 Dec 2025 22:34:15 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:0d6422799dd4d94f6d14486ed31c51581e6e2b32958e1d7a623a8a3a5fb3c41b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea3e0d80229d4fe945daed273a70f7abdffc4dfe50154689382b3e2060cc6ac`

```dockerfile
```

-	Layers:
	-	`sha256:fda30db641eded936294f53aa8bb16fa01ceeee415001ef56fb36b4070fa0174`  
		Last Modified: Tue, 09 Dec 2025 00:28:05 GMT  
		Size: 2.4 MB (2403365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff6781a413fe2cd76eda946d9ac14ef8471e55f55bcf856ec25f27e1844d6377`  
		Last Modified: Tue, 09 Dec 2025 00:28:06 GMT  
		Size: 12.5 KB (12486 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:b13d61a6485f03c14b32349a6a085d6c2ee9867809a51a8a869afe896503ced8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106670113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80f70b1de050571ebe9de15615ff81a043f4694b916e7711944425b2986b8c4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:23 GMT
ENV EMQX_VERSION=5.8.8
# Mon, 08 Dec 2025 22:33:23 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Mon, 08 Dec 2025 22:33:23 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Mon, 08 Dec 2025 22:33:23 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 08 Dec 2025 22:33:23 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 08 Dec 2025 22:33:23 GMT
WORKDIR /opt/emqx
# Mon, 08 Dec 2025 22:33:23 GMT
USER emqx
# Mon, 08 Dec 2025 22:33:23 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 08 Dec 2025 22:33:23 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 08 Dec 2025 22:33:23 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 08 Dec 2025 22:33:23 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:33:23 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbf02f9d00f7977907ce76e8384e00eb205c8f38171a3f9f825a001d30561fb`  
		Last Modified: Mon, 08 Dec 2025 22:33:49 GMT  
		Size: 76.5 MB (76530423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e607df1ff2410131172ae217d2ad23f9d60a7ff61e888cd5614d979ed6c85030`  
		Last Modified: Mon, 08 Dec 2025 22:33:43 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:bf61c23366b642c4d67eca5726ac549ef02df46d316d7f868e0eba4da94a6aa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf947df68c57dab06a035a3498393d31c9385a6f2dd33abb91f0b3ea76baa45a`

```dockerfile
```

-	Layers:
	-	`sha256:a51290bac0811b652c5ffe7d3a61c8383398a29c84a1fd776c0cefe9206c57bf`  
		Last Modified: Tue, 09 Dec 2025 00:28:11 GMT  
		Size: 2.4 MB (2403654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf464f98e7e2f52f0cbcf3bff6d218f5123b4caf8c6c67f26ab2757972628a55`  
		Last Modified: Tue, 09 Dec 2025 00:28:12 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7`

```console
$ docker pull emqx@sha256:fa3c530bd2f7972a6f3daadd5e51fa6b9757d26c60519d05e3c3240d5d554d76
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7` - linux; amd64

```console
$ docker pull emqx@sha256:85a1d39e8d345904c4589c6d59bbbb6dbfefdb297fead0122a3332055ffbe23e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125384529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9dde4426c138c1e3f81fd4b1b94ffe768e75480ca0765660a6d49f56fb1384`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:33:54 GMT
ENV EMQX_VERSION=5.7.2
# Mon, 08 Dec 2025 22:33:54 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Mon, 08 Dec 2025 22:33:54 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Mon, 08 Dec 2025 22:33:54 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 08 Dec 2025 22:33:54 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 08 Dec 2025 22:33:54 GMT
WORKDIR /opt/emqx
# Mon, 08 Dec 2025 22:33:54 GMT
USER emqx
# Mon, 08 Dec 2025 22:33:54 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 08 Dec 2025 22:33:54 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 08 Dec 2025 22:33:54 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 08 Dec 2025 22:33:54 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:33:54 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8f9bb75a455f2561c5f3de90adf4613976a8fad0fcb179a731cc43263cbb85`  
		Last Modified: Mon, 08 Dec 2025 22:34:28 GMT  
		Size: 97.2 MB (97155050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b929cc3ced5ee1317a25609d542656c82631a4ac9453672d726a1523fe303715`  
		Last Modified: Mon, 08 Dec 2025 22:34:16 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:64fd0f402f59f8688e2f7ba3a32e0cc1359d6e9c25980eca68844c95cb31061b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8056e7a087f6839fc88f703b964d34fa28673cd8a0f4ee09784ce6409838635`

```dockerfile
```

-	Layers:
	-	`sha256:1d802fb5d5a218d4b809804cb5a628dbec9516dd292560c5dddecc3a9bf9ccc0`  
		Last Modified: Tue, 09 Dec 2025 00:28:14 GMT  
		Size: 2.8 MB (2751388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a09258bbeadee6de30b06bf2a30891d9f540e6c5b3f6e27db09b8152b104369b`  
		Last Modified: Tue, 09 Dec 2025 00:28:16 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:ef8c9125530b25111bef86f101b73915793ba20d81579a430ca3e48651aacac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121818442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5651cead3faba3ae8c8b5c704e4d98bd2ec4ef8a0a006cd36a2fba43c7b2e2`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:32:59 GMT
ENV EMQX_VERSION=5.7.2
# Mon, 08 Dec 2025 22:32:59 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Mon, 08 Dec 2025 22:32:59 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Mon, 08 Dec 2025 22:32:59 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 08 Dec 2025 22:32:59 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 08 Dec 2025 22:32:59 GMT
WORKDIR /opt/emqx
# Mon, 08 Dec 2025 22:32:59 GMT
USER emqx
# Mon, 08 Dec 2025 22:32:59 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 08 Dec 2025 22:32:59 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 08 Dec 2025 22:32:59 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 08 Dec 2025 22:32:59 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:32:59 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7de8f4b379a6ea926905ac780260939ba591ef591b22d9a56bb2787fd2fbf4a`  
		Last Modified: Mon, 08 Dec 2025 22:33:28 GMT  
		Size: 93.7 MB (93715151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a07fbfed7876eee433bfd3bb43a0da7922043c4e476971981b53cd0bbe7b9eb`  
		Last Modified: Mon, 08 Dec 2025 22:33:22 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:64c7ea3f3c28698d01d714fca4558241adb83b842ab122669c3be304457218ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e25b4bb75dc6652921abffc2d37f44e814fca0e8507f36dde0fcc5030c896c`

```dockerfile
```

-	Layers:
	-	`sha256:8f9159488be417bc9f658c42e902def3b21468c15e518b2e2e7ffcdada2492b6`  
		Last Modified: Tue, 09 Dec 2025 00:28:20 GMT  
		Size: 2.8 MB (2751644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8bf01e6c4d4141ccdf0e404cc5808e5601869c51aab4cadf003a02fa5425b09`  
		Last Modified: Tue, 09 Dec 2025 00:28:20 GMT  
		Size: 12.0 KB (11985 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7.2`

```console
$ docker pull emqx@sha256:fa3c530bd2f7972a6f3daadd5e51fa6b9757d26c60519d05e3c3240d5d554d76
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7.2` - linux; amd64

```console
$ docker pull emqx@sha256:85a1d39e8d345904c4589c6d59bbbb6dbfefdb297fead0122a3332055ffbe23e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125384529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf9dde4426c138c1e3f81fd4b1b94ffe768e75480ca0765660a6d49f56fb1384`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:33:54 GMT
ENV EMQX_VERSION=5.7.2
# Mon, 08 Dec 2025 22:33:54 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Mon, 08 Dec 2025 22:33:54 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Mon, 08 Dec 2025 22:33:54 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 08 Dec 2025 22:33:54 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 08 Dec 2025 22:33:54 GMT
WORKDIR /opt/emqx
# Mon, 08 Dec 2025 22:33:54 GMT
USER emqx
# Mon, 08 Dec 2025 22:33:54 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 08 Dec 2025 22:33:54 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 08 Dec 2025 22:33:54 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 08 Dec 2025 22:33:54 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:33:54 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8f9bb75a455f2561c5f3de90adf4613976a8fad0fcb179a731cc43263cbb85`  
		Last Modified: Mon, 08 Dec 2025 22:34:28 GMT  
		Size: 97.2 MB (97155050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b929cc3ced5ee1317a25609d542656c82631a4ac9453672d726a1523fe303715`  
		Last Modified: Mon, 08 Dec 2025 22:34:16 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:64fd0f402f59f8688e2f7ba3a32e0cc1359d6e9c25980eca68844c95cb31061b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8056e7a087f6839fc88f703b964d34fa28673cd8a0f4ee09784ce6409838635`

```dockerfile
```

-	Layers:
	-	`sha256:1d802fb5d5a218d4b809804cb5a628dbec9516dd292560c5dddecc3a9bf9ccc0`  
		Last Modified: Tue, 09 Dec 2025 00:28:14 GMT  
		Size: 2.8 MB (2751388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a09258bbeadee6de30b06bf2a30891d9f540e6c5b3f6e27db09b8152b104369b`  
		Last Modified: Tue, 09 Dec 2025 00:28:16 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:ef8c9125530b25111bef86f101b73915793ba20d81579a430ca3e48651aacac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121818442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5651cead3faba3ae8c8b5c704e4d98bd2ec4ef8a0a006cd36a2fba43c7b2e2`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:32:59 GMT
ENV EMQX_VERSION=5.7.2
# Mon, 08 Dec 2025 22:32:59 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Mon, 08 Dec 2025 22:32:59 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Mon, 08 Dec 2025 22:32:59 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 08 Dec 2025 22:32:59 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 08 Dec 2025 22:32:59 GMT
WORKDIR /opt/emqx
# Mon, 08 Dec 2025 22:32:59 GMT
USER emqx
# Mon, 08 Dec 2025 22:32:59 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 08 Dec 2025 22:32:59 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 08 Dec 2025 22:32:59 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 08 Dec 2025 22:32:59 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:32:59 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7de8f4b379a6ea926905ac780260939ba591ef591b22d9a56bb2787fd2fbf4a`  
		Last Modified: Mon, 08 Dec 2025 22:33:28 GMT  
		Size: 93.7 MB (93715151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a07fbfed7876eee433bfd3bb43a0da7922043c4e476971981b53cd0bbe7b9eb`  
		Last Modified: Mon, 08 Dec 2025 22:33:22 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:64c7ea3f3c28698d01d714fca4558241adb83b842ab122669c3be304457218ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e25b4bb75dc6652921abffc2d37f44e814fca0e8507f36dde0fcc5030c896c`

```dockerfile
```

-	Layers:
	-	`sha256:8f9159488be417bc9f658c42e902def3b21468c15e518b2e2e7ffcdada2492b6`  
		Last Modified: Tue, 09 Dec 2025 00:28:20 GMT  
		Size: 2.8 MB (2751644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8bf01e6c4d4141ccdf0e404cc5808e5601869c51aab4cadf003a02fa5425b09`  
		Last Modified: Tue, 09 Dec 2025 00:28:20 GMT  
		Size: 12.0 KB (11985 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8`

```console
$ docker pull emqx@sha256:516df7073402cadd42995460e69600d0416a4a9329338cd8f5fa6831649192db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8` - linux; amd64

```console
$ docker pull emqx@sha256:cacf91d9eb4b8ec3a2aca265ce5f17e4dcaacaa6c03d1551e24cc6aab78fe218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108399110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49f29a0e9115ef92a20e8ab16cc9eab40c7dd7280c49c2fe640e6825c55635dd`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:56 GMT
ENV EMQX_VERSION=5.8.8
# Mon, 08 Dec 2025 22:33:56 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Mon, 08 Dec 2025 22:33:56 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Mon, 08 Dec 2025 22:33:56 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 08 Dec 2025 22:33:56 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 08 Dec 2025 22:33:56 GMT
WORKDIR /opt/emqx
# Mon, 08 Dec 2025 22:33:56 GMT
USER emqx
# Mon, 08 Dec 2025 22:33:56 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 08 Dec 2025 22:33:56 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 08 Dec 2025 22:33:56 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 08 Dec 2025 22:33:56 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:33:56 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee851dbc9e6748a1a8e982e716b5427e46535cc7b781a813dfd98be52bc7eb6`  
		Last Modified: Mon, 08 Dec 2025 22:34:23 GMT  
		Size: 78.6 MB (78621554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a2f7fb8635a90190ce542685acfd0492631545f2206d8a7fbc539d7455d47c`  
		Last Modified: Mon, 08 Dec 2025 22:34:15 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:0d6422799dd4d94f6d14486ed31c51581e6e2b32958e1d7a623a8a3a5fb3c41b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea3e0d80229d4fe945daed273a70f7abdffc4dfe50154689382b3e2060cc6ac`

```dockerfile
```

-	Layers:
	-	`sha256:fda30db641eded936294f53aa8bb16fa01ceeee415001ef56fb36b4070fa0174`  
		Last Modified: Tue, 09 Dec 2025 00:28:05 GMT  
		Size: 2.4 MB (2403365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff6781a413fe2cd76eda946d9ac14ef8471e55f55bcf856ec25f27e1844d6377`  
		Last Modified: Tue, 09 Dec 2025 00:28:06 GMT  
		Size: 12.5 KB (12486 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:b13d61a6485f03c14b32349a6a085d6c2ee9867809a51a8a869afe896503ced8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106670113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80f70b1de050571ebe9de15615ff81a043f4694b916e7711944425b2986b8c4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:23 GMT
ENV EMQX_VERSION=5.8.8
# Mon, 08 Dec 2025 22:33:23 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Mon, 08 Dec 2025 22:33:23 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Mon, 08 Dec 2025 22:33:23 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 08 Dec 2025 22:33:23 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 08 Dec 2025 22:33:23 GMT
WORKDIR /opt/emqx
# Mon, 08 Dec 2025 22:33:23 GMT
USER emqx
# Mon, 08 Dec 2025 22:33:23 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 08 Dec 2025 22:33:23 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 08 Dec 2025 22:33:23 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 08 Dec 2025 22:33:23 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:33:23 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbf02f9d00f7977907ce76e8384e00eb205c8f38171a3f9f825a001d30561fb`  
		Last Modified: Mon, 08 Dec 2025 22:33:49 GMT  
		Size: 76.5 MB (76530423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e607df1ff2410131172ae217d2ad23f9d60a7ff61e888cd5614d979ed6c85030`  
		Last Modified: Mon, 08 Dec 2025 22:33:43 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:bf61c23366b642c4d67eca5726ac549ef02df46d316d7f868e0eba4da94a6aa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf947df68c57dab06a035a3498393d31c9385a6f2dd33abb91f0b3ea76baa45a`

```dockerfile
```

-	Layers:
	-	`sha256:a51290bac0811b652c5ffe7d3a61c8383398a29c84a1fd776c0cefe9206c57bf`  
		Last Modified: Tue, 09 Dec 2025 00:28:11 GMT  
		Size: 2.4 MB (2403654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf464f98e7e2f52f0cbcf3bff6d218f5123b4caf8c6c67f26ab2757972628a55`  
		Last Modified: Tue, 09 Dec 2025 00:28:12 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8.8`

```console
$ docker pull emqx@sha256:516df7073402cadd42995460e69600d0416a4a9329338cd8f5fa6831649192db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8.8` - linux; amd64

```console
$ docker pull emqx@sha256:cacf91d9eb4b8ec3a2aca265ce5f17e4dcaacaa6c03d1551e24cc6aab78fe218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108399110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49f29a0e9115ef92a20e8ab16cc9eab40c7dd7280c49c2fe640e6825c55635dd`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:56 GMT
ENV EMQX_VERSION=5.8.8
# Mon, 08 Dec 2025 22:33:56 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Mon, 08 Dec 2025 22:33:56 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Mon, 08 Dec 2025 22:33:56 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 08 Dec 2025 22:33:56 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 08 Dec 2025 22:33:56 GMT
WORKDIR /opt/emqx
# Mon, 08 Dec 2025 22:33:56 GMT
USER emqx
# Mon, 08 Dec 2025 22:33:56 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 08 Dec 2025 22:33:56 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 08 Dec 2025 22:33:56 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 08 Dec 2025 22:33:56 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:33:56 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee851dbc9e6748a1a8e982e716b5427e46535cc7b781a813dfd98be52bc7eb6`  
		Last Modified: Mon, 08 Dec 2025 22:34:23 GMT  
		Size: 78.6 MB (78621554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a2f7fb8635a90190ce542685acfd0492631545f2206d8a7fbc539d7455d47c`  
		Last Modified: Mon, 08 Dec 2025 22:34:15 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.8` - unknown; unknown

```console
$ docker pull emqx@sha256:0d6422799dd4d94f6d14486ed31c51581e6e2b32958e1d7a623a8a3a5fb3c41b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea3e0d80229d4fe945daed273a70f7abdffc4dfe50154689382b3e2060cc6ac`

```dockerfile
```

-	Layers:
	-	`sha256:fda30db641eded936294f53aa8bb16fa01ceeee415001ef56fb36b4070fa0174`  
		Last Modified: Tue, 09 Dec 2025 00:28:05 GMT  
		Size: 2.4 MB (2403365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff6781a413fe2cd76eda946d9ac14ef8471e55f55bcf856ec25f27e1844d6377`  
		Last Modified: Tue, 09 Dec 2025 00:28:06 GMT  
		Size: 12.5 KB (12486 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8.8` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:b13d61a6485f03c14b32349a6a085d6c2ee9867809a51a8a869afe896503ced8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106670113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80f70b1de050571ebe9de15615ff81a043f4694b916e7711944425b2986b8c4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:23 GMT
ENV EMQX_VERSION=5.8.8
# Mon, 08 Dec 2025 22:33:23 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Mon, 08 Dec 2025 22:33:23 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Mon, 08 Dec 2025 22:33:23 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 08 Dec 2025 22:33:23 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 08 Dec 2025 22:33:23 GMT
WORKDIR /opt/emqx
# Mon, 08 Dec 2025 22:33:23 GMT
USER emqx
# Mon, 08 Dec 2025 22:33:23 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 08 Dec 2025 22:33:23 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 08 Dec 2025 22:33:23 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 08 Dec 2025 22:33:23 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:33:23 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbf02f9d00f7977907ce76e8384e00eb205c8f38171a3f9f825a001d30561fb`  
		Last Modified: Mon, 08 Dec 2025 22:33:49 GMT  
		Size: 76.5 MB (76530423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e607df1ff2410131172ae217d2ad23f9d60a7ff61e888cd5614d979ed6c85030`  
		Last Modified: Mon, 08 Dec 2025 22:33:43 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.8` - unknown; unknown

```console
$ docker pull emqx@sha256:bf61c23366b642c4d67eca5726ac549ef02df46d316d7f868e0eba4da94a6aa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf947df68c57dab06a035a3498393d31c9385a6f2dd33abb91f0b3ea76baa45a`

```dockerfile
```

-	Layers:
	-	`sha256:a51290bac0811b652c5ffe7d3a61c8383398a29c84a1fd776c0cefe9206c57bf`  
		Last Modified: Tue, 09 Dec 2025 00:28:11 GMT  
		Size: 2.4 MB (2403654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf464f98e7e2f52f0cbcf3bff6d218f5123b4caf8c6c67f26ab2757972628a55`  
		Last Modified: Tue, 09 Dec 2025 00:28:12 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:latest`

```console
$ docker pull emqx@sha256:516df7073402cadd42995460e69600d0416a4a9329338cd8f5fa6831649192db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:cacf91d9eb4b8ec3a2aca265ce5f17e4dcaacaa6c03d1551e24cc6aab78fe218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108399110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49f29a0e9115ef92a20e8ab16cc9eab40c7dd7280c49c2fe640e6825c55635dd`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:56 GMT
ENV EMQX_VERSION=5.8.8
# Mon, 08 Dec 2025 22:33:56 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Mon, 08 Dec 2025 22:33:56 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Mon, 08 Dec 2025 22:33:56 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 08 Dec 2025 22:33:56 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 08 Dec 2025 22:33:56 GMT
WORKDIR /opt/emqx
# Mon, 08 Dec 2025 22:33:56 GMT
USER emqx
# Mon, 08 Dec 2025 22:33:56 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 08 Dec 2025 22:33:56 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 08 Dec 2025 22:33:56 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 08 Dec 2025 22:33:56 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:33:56 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee851dbc9e6748a1a8e982e716b5427e46535cc7b781a813dfd98be52bc7eb6`  
		Last Modified: Mon, 08 Dec 2025 22:34:23 GMT  
		Size: 78.6 MB (78621554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a2f7fb8635a90190ce542685acfd0492631545f2206d8a7fbc539d7455d47c`  
		Last Modified: Mon, 08 Dec 2025 22:34:15 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:0d6422799dd4d94f6d14486ed31c51581e6e2b32958e1d7a623a8a3a5fb3c41b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea3e0d80229d4fe945daed273a70f7abdffc4dfe50154689382b3e2060cc6ac`

```dockerfile
```

-	Layers:
	-	`sha256:fda30db641eded936294f53aa8bb16fa01ceeee415001ef56fb36b4070fa0174`  
		Last Modified: Tue, 09 Dec 2025 00:28:05 GMT  
		Size: 2.4 MB (2403365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff6781a413fe2cd76eda946d9ac14ef8471e55f55bcf856ec25f27e1844d6377`  
		Last Modified: Tue, 09 Dec 2025 00:28:06 GMT  
		Size: 12.5 KB (12486 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:b13d61a6485f03c14b32349a6a085d6c2ee9867809a51a8a869afe896503ced8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106670113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80f70b1de050571ebe9de15615ff81a043f4694b916e7711944425b2986b8c4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:33:23 GMT
ENV EMQX_VERSION=5.8.8
# Mon, 08 Dec 2025 22:33:23 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Mon, 08 Dec 2025 22:33:23 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Mon, 08 Dec 2025 22:33:23 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 08 Dec 2025 22:33:23 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 08 Dec 2025 22:33:23 GMT
WORKDIR /opt/emqx
# Mon, 08 Dec 2025 22:33:23 GMT
USER emqx
# Mon, 08 Dec 2025 22:33:23 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 08 Dec 2025 22:33:23 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 08 Dec 2025 22:33:23 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 08 Dec 2025 22:33:23 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 08 Dec 2025 22:33:23 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbf02f9d00f7977907ce76e8384e00eb205c8f38171a3f9f825a001d30561fb`  
		Last Modified: Mon, 08 Dec 2025 22:33:49 GMT  
		Size: 76.5 MB (76530423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e607df1ff2410131172ae217d2ad23f9d60a7ff61e888cd5614d979ed6c85030`  
		Last Modified: Mon, 08 Dec 2025 22:33:43 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:bf61c23366b642c4d67eca5726ac549ef02df46d316d7f868e0eba4da94a6aa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf947df68c57dab06a035a3498393d31c9385a6f2dd33abb91f0b3ea76baa45a`

```dockerfile
```

-	Layers:
	-	`sha256:a51290bac0811b652c5ffe7d3a61c8383398a29c84a1fd776c0cefe9206c57bf`  
		Last Modified: Tue, 09 Dec 2025 00:28:11 GMT  
		Size: 2.4 MB (2403654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf464f98e7e2f52f0cbcf3bff6d218f5123b4caf8c6c67f26ab2757972628a55`  
		Last Modified: Tue, 09 Dec 2025 00:28:12 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json
