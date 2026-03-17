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
$ docker pull emqx@sha256:ef071632cd7933e551b074d834b2674096f0490ac242e99756d7a1b14fbcbf0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:6d5ae6bd9ef2b80fcc28df79c37017e7726e4cf139f756849eeecac5bf2ca178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108400970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0da0abaa9f1bcee18bf9c440005800b72e49c391b2097de712041e1629f35f1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:16:13 GMT
ENV EMQX_VERSION=5.8.8
# Mon, 16 Mar 2026 22:16:13 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Mon, 16 Mar 2026 22:16:13 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Mon, 16 Mar 2026 22:16:13 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 16 Mar 2026 22:16:13 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 16 Mar 2026 22:16:13 GMT
WORKDIR /opt/emqx
# Mon, 16 Mar 2026 22:16:13 GMT
USER emqx
# Mon, 16 Mar 2026 22:16:13 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 16 Mar 2026 22:16:13 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 16 Mar 2026 22:16:13 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 16 Mar 2026 22:16:13 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:16:13 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904f97fd81e702b2ceee48558a02977070b0bf97e36f34039fa5a86734eacc3f`  
		Last Modified: Mon, 16 Mar 2026 22:16:27 GMT  
		Size: 78.6 MB (78624408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0cad49748de04acd939080e30a3b2a887971ccf4f392aea03ccac0873b564b`  
		Last Modified: Mon, 16 Mar 2026 22:16:25 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:655a1b87c1e38dd1d1bba5ea39f0d8a84dc1987d7c81fc11b83357e2a4f273f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d84ac141b17d1b991366b927531eb8463dd68817080b2e1df779bd29c537ce63`

```dockerfile
```

-	Layers:
	-	`sha256:6911da73eb750fe99b4739e9b640127f7b6af44a872f4ec088c1df10974a044f`  
		Last Modified: Mon, 16 Mar 2026 22:16:25 GMT  
		Size: 2.4 MB (2403501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11142c734c3da0fb1dc6d1da7967cd13dec9747671764eab62f9d00cb7954b20`  
		Last Modified: Mon, 16 Mar 2026 22:16:25 GMT  
		Size: 12.5 KB (12486 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:040d4aa42301e353ac651f52adb6a75450bff0381c7aa9b103f7b832ad25b8b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106671055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607d1f826cd8c5dbdd5e00d0699578f4f64fed11b7c5d22bc340d41dc44af7fa`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:15:29 GMT
ENV EMQX_VERSION=5.8.8
# Mon, 16 Mar 2026 22:15:29 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Mon, 16 Mar 2026 22:15:29 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Mon, 16 Mar 2026 22:15:29 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 16 Mar 2026 22:15:29 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 16 Mar 2026 22:15:29 GMT
WORKDIR /opt/emqx
# Mon, 16 Mar 2026 22:15:29 GMT
USER emqx
# Mon, 16 Mar 2026 22:15:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 16 Mar 2026 22:15:29 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 16 Mar 2026 22:15:29 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 16 Mar 2026 22:15:29 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:15:29 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0d34e72ceb0b7ab53d6c16e2ca318826abac86182fa008375a7bbce8b63c87`  
		Last Modified: Mon, 16 Mar 2026 22:15:44 GMT  
		Size: 76.5 MB (76531577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9d9386780f37c816b9f75c4fa04cc5b475c7af0fe1032d44244a71313c9a50`  
		Last Modified: Mon, 16 Mar 2026 22:15:42 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:5cd2d78a1e35893eb56365ce044dc883865829c997fdfd81a9f70275aca20482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97dad188baac0f204140fac0fe3f18792f26db5051a6d3be9f823d00cd274c0`

```dockerfile
```

-	Layers:
	-	`sha256:8edb65027663c927b9e5e6ad3082a0d4b0e8aa0e4a34044b4077f7537c37b54a`  
		Last Modified: Mon, 16 Mar 2026 22:15:42 GMT  
		Size: 2.4 MB (2403790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8839089d3ec10e5f82e0c9fd0f7d2a128217235a91cca99122b61f4b25066a6`  
		Last Modified: Mon, 16 Mar 2026 22:15:42 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7`

```console
$ docker pull emqx@sha256:bd29c6e656c00f5ba8009344709f6c5947d545af2b58808c8ae4acae168a132a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7` - linux; amd64

```console
$ docker pull emqx@sha256:be7003dfcf8ca22df1535840802215eb1a92fed1f9c89d18e049be55506e86db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125392542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d6e3a1351f2718080046c11ff1b5ae4fa554984afbc0e6ec91cb8117ddff424`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:16:18 GMT
ENV EMQX_VERSION=5.7.2
# Mon, 16 Mar 2026 22:16:18 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Mon, 16 Mar 2026 22:16:18 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Mon, 16 Mar 2026 22:16:18 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 16 Mar 2026 22:16:18 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 16 Mar 2026 22:16:18 GMT
WORKDIR /opt/emqx
# Mon, 16 Mar 2026 22:16:18 GMT
USER emqx
# Mon, 16 Mar 2026 22:16:18 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 16 Mar 2026 22:16:18 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 16 Mar 2026 22:16:18 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 16 Mar 2026 22:16:18 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:16:18 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eddceb1d4aebb1230e217dbbd4d64b57485e1dfe02db4215230db621ddc07fd0`  
		Last Modified: Mon, 16 Mar 2026 22:16:34 GMT  
		Size: 97.2 MB (97155257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a497ef78ce5960bb150e0b21bc280590138268c20e0f2a95105520a335914f6`  
		Last Modified: Mon, 16 Mar 2026 22:16:32 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:76fcf5dd55b8de706ce0fab98e8b8d1aec2388ce2a876750e58c539b8ff185da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b77899bb19a48269a2ff1bc4a72f37b3802bf998af1f21f0aac447804616be2`

```dockerfile
```

-	Layers:
	-	`sha256:057d901a50bff2672bb405e9888d62d4e5d6e3a86e10bd883d1fd33a4453e8cd`  
		Last Modified: Mon, 16 Mar 2026 22:16:32 GMT  
		Size: 2.8 MB (2751398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e50ec359a2098630a193862a05db8fd58b84e7bbe987eb3364f9d65784472f2`  
		Last Modified: Mon, 16 Mar 2026 22:16:31 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:6f636c2c233d7e18859a25a065b202ff623551d3f24568e50084c403de0ced4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121833068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac778eaa353aa0fe5ee37557de2bedf94579524edb73f8c4d394f240c9128b7a`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:15:50 GMT
ENV EMQX_VERSION=5.7.2
# Mon, 16 Mar 2026 22:15:50 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Mon, 16 Mar 2026 22:15:50 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Mon, 16 Mar 2026 22:15:50 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 16 Mar 2026 22:15:50 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 16 Mar 2026 22:15:50 GMT
WORKDIR /opt/emqx
# Mon, 16 Mar 2026 22:15:50 GMT
USER emqx
# Mon, 16 Mar 2026 22:15:50 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 16 Mar 2026 22:15:50 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 16 Mar 2026 22:15:51 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 16 Mar 2026 22:15:51 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:15:51 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3080710e54d4abe06f15c241d6893959bd4ef88871214ca11d707e295daa8e8c`  
		Last Modified: Mon, 16 Mar 2026 22:16:08 GMT  
		Size: 93.7 MB (93715940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1e3a1d4a6715373afba57c642a878957ac34e48b7b8fe6de47648583e8c492`  
		Last Modified: Mon, 16 Mar 2026 22:16:05 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:191fc84fa5a48e73b7fa597bb7aa185300eb120bee512d05cdf94cf837182724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e06ec9f2410617df9e167c931d0801cbf613ff57bb2e8cbd32329a730b7d9c`

```dockerfile
```

-	Layers:
	-	`sha256:2dc01cdad654a42de7fa1c08f6ccf079980c426030f1a2c8069fb6717e06285c`  
		Last Modified: Mon, 16 Mar 2026 22:16:05 GMT  
		Size: 2.8 MB (2751654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0b067e9d6602324170cad5c4a4dfd43005b616fd891b3969d73610402300e1d`  
		Last Modified: Mon, 16 Mar 2026 22:16:05 GMT  
		Size: 12.0 KB (11988 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7.2`

```console
$ docker pull emqx@sha256:bd29c6e656c00f5ba8009344709f6c5947d545af2b58808c8ae4acae168a132a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7.2` - linux; amd64

```console
$ docker pull emqx@sha256:be7003dfcf8ca22df1535840802215eb1a92fed1f9c89d18e049be55506e86db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125392542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d6e3a1351f2718080046c11ff1b5ae4fa554984afbc0e6ec91cb8117ddff424`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:16:18 GMT
ENV EMQX_VERSION=5.7.2
# Mon, 16 Mar 2026 22:16:18 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Mon, 16 Mar 2026 22:16:18 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Mon, 16 Mar 2026 22:16:18 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 16 Mar 2026 22:16:18 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 16 Mar 2026 22:16:18 GMT
WORKDIR /opt/emqx
# Mon, 16 Mar 2026 22:16:18 GMT
USER emqx
# Mon, 16 Mar 2026 22:16:18 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 16 Mar 2026 22:16:18 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 16 Mar 2026 22:16:18 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 16 Mar 2026 22:16:18 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:16:18 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eddceb1d4aebb1230e217dbbd4d64b57485e1dfe02db4215230db621ddc07fd0`  
		Last Modified: Mon, 16 Mar 2026 22:16:34 GMT  
		Size: 97.2 MB (97155257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a497ef78ce5960bb150e0b21bc280590138268c20e0f2a95105520a335914f6`  
		Last Modified: Mon, 16 Mar 2026 22:16:32 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:76fcf5dd55b8de706ce0fab98e8b8d1aec2388ce2a876750e58c539b8ff185da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b77899bb19a48269a2ff1bc4a72f37b3802bf998af1f21f0aac447804616be2`

```dockerfile
```

-	Layers:
	-	`sha256:057d901a50bff2672bb405e9888d62d4e5d6e3a86e10bd883d1fd33a4453e8cd`  
		Last Modified: Mon, 16 Mar 2026 22:16:32 GMT  
		Size: 2.8 MB (2751398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e50ec359a2098630a193862a05db8fd58b84e7bbe987eb3364f9d65784472f2`  
		Last Modified: Mon, 16 Mar 2026 22:16:31 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:6f636c2c233d7e18859a25a065b202ff623551d3f24568e50084c403de0ced4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.8 MB (121833068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac778eaa353aa0fe5ee37557de2bedf94579524edb73f8c4d394f240c9128b7a`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:15:50 GMT
ENV EMQX_VERSION=5.7.2
# Mon, 16 Mar 2026 22:15:50 GMT
ENV AMD64_SHA256=1f32fb90ca5e7b3d2a447a82d4e3d22397e25bc97800bdcb1deb6d2a685c1c35
# Mon, 16 Mar 2026 22:15:50 GMT
ENV ARM64_SHA256=6bfa8c774a9f7b2957a6519e428c96d58ac4f748ddd0b40dd2b429d270fcf9c0
# Mon, 16 Mar 2026 22:15:50 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 16 Mar 2026 22:15:50 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 16 Mar 2026 22:15:50 GMT
WORKDIR /opt/emqx
# Mon, 16 Mar 2026 22:15:50 GMT
USER emqx
# Mon, 16 Mar 2026 22:15:50 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 16 Mar 2026 22:15:50 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 16 Mar 2026 22:15:51 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 16 Mar 2026 22:15:51 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:15:51 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3080710e54d4abe06f15c241d6893959bd4ef88871214ca11d707e295daa8e8c`  
		Last Modified: Mon, 16 Mar 2026 22:16:08 GMT  
		Size: 93.7 MB (93715940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1e3a1d4a6715373afba57c642a878957ac34e48b7b8fe6de47648583e8c492`  
		Last Modified: Mon, 16 Mar 2026 22:16:05 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:191fc84fa5a48e73b7fa597bb7aa185300eb120bee512d05cdf94cf837182724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2763642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e06ec9f2410617df9e167c931d0801cbf613ff57bb2e8cbd32329a730b7d9c`

```dockerfile
```

-	Layers:
	-	`sha256:2dc01cdad654a42de7fa1c08f6ccf079980c426030f1a2c8069fb6717e06285c`  
		Last Modified: Mon, 16 Mar 2026 22:16:05 GMT  
		Size: 2.8 MB (2751654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0b067e9d6602324170cad5c4a4dfd43005b616fd891b3969d73610402300e1d`  
		Last Modified: Mon, 16 Mar 2026 22:16:05 GMT  
		Size: 12.0 KB (11988 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8`

```console
$ docker pull emqx@sha256:ef071632cd7933e551b074d834b2674096f0490ac242e99756d7a1b14fbcbf0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8` - linux; amd64

```console
$ docker pull emqx@sha256:6d5ae6bd9ef2b80fcc28df79c37017e7726e4cf139f756849eeecac5bf2ca178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108400970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0da0abaa9f1bcee18bf9c440005800b72e49c391b2097de712041e1629f35f1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:16:13 GMT
ENV EMQX_VERSION=5.8.8
# Mon, 16 Mar 2026 22:16:13 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Mon, 16 Mar 2026 22:16:13 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Mon, 16 Mar 2026 22:16:13 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 16 Mar 2026 22:16:13 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 16 Mar 2026 22:16:13 GMT
WORKDIR /opt/emqx
# Mon, 16 Mar 2026 22:16:13 GMT
USER emqx
# Mon, 16 Mar 2026 22:16:13 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 16 Mar 2026 22:16:13 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 16 Mar 2026 22:16:13 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 16 Mar 2026 22:16:13 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:16:13 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904f97fd81e702b2ceee48558a02977070b0bf97e36f34039fa5a86734eacc3f`  
		Last Modified: Mon, 16 Mar 2026 22:16:27 GMT  
		Size: 78.6 MB (78624408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0cad49748de04acd939080e30a3b2a887971ccf4f392aea03ccac0873b564b`  
		Last Modified: Mon, 16 Mar 2026 22:16:25 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:655a1b87c1e38dd1d1bba5ea39f0d8a84dc1987d7c81fc11b83357e2a4f273f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d84ac141b17d1b991366b927531eb8463dd68817080b2e1df779bd29c537ce63`

```dockerfile
```

-	Layers:
	-	`sha256:6911da73eb750fe99b4739e9b640127f7b6af44a872f4ec088c1df10974a044f`  
		Last Modified: Mon, 16 Mar 2026 22:16:25 GMT  
		Size: 2.4 MB (2403501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11142c734c3da0fb1dc6d1da7967cd13dec9747671764eab62f9d00cb7954b20`  
		Last Modified: Mon, 16 Mar 2026 22:16:25 GMT  
		Size: 12.5 KB (12486 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:040d4aa42301e353ac651f52adb6a75450bff0381c7aa9b103f7b832ad25b8b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106671055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607d1f826cd8c5dbdd5e00d0699578f4f64fed11b7c5d22bc340d41dc44af7fa`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:15:29 GMT
ENV EMQX_VERSION=5.8.8
# Mon, 16 Mar 2026 22:15:29 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Mon, 16 Mar 2026 22:15:29 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Mon, 16 Mar 2026 22:15:29 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 16 Mar 2026 22:15:29 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 16 Mar 2026 22:15:29 GMT
WORKDIR /opt/emqx
# Mon, 16 Mar 2026 22:15:29 GMT
USER emqx
# Mon, 16 Mar 2026 22:15:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 16 Mar 2026 22:15:29 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 16 Mar 2026 22:15:29 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 16 Mar 2026 22:15:29 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:15:29 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0d34e72ceb0b7ab53d6c16e2ca318826abac86182fa008375a7bbce8b63c87`  
		Last Modified: Mon, 16 Mar 2026 22:15:44 GMT  
		Size: 76.5 MB (76531577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9d9386780f37c816b9f75c4fa04cc5b475c7af0fe1032d44244a71313c9a50`  
		Last Modified: Mon, 16 Mar 2026 22:15:42 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:5cd2d78a1e35893eb56365ce044dc883865829c997fdfd81a9f70275aca20482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97dad188baac0f204140fac0fe3f18792f26db5051a6d3be9f823d00cd274c0`

```dockerfile
```

-	Layers:
	-	`sha256:8edb65027663c927b9e5e6ad3082a0d4b0e8aa0e4a34044b4077f7537c37b54a`  
		Last Modified: Mon, 16 Mar 2026 22:15:42 GMT  
		Size: 2.4 MB (2403790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8839089d3ec10e5f82e0c9fd0f7d2a128217235a91cca99122b61f4b25066a6`  
		Last Modified: Mon, 16 Mar 2026 22:15:42 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8.8`

```console
$ docker pull emqx@sha256:ef071632cd7933e551b074d834b2674096f0490ac242e99756d7a1b14fbcbf0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8.8` - linux; amd64

```console
$ docker pull emqx@sha256:6d5ae6bd9ef2b80fcc28df79c37017e7726e4cf139f756849eeecac5bf2ca178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108400970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0da0abaa9f1bcee18bf9c440005800b72e49c391b2097de712041e1629f35f1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:16:13 GMT
ENV EMQX_VERSION=5.8.8
# Mon, 16 Mar 2026 22:16:13 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Mon, 16 Mar 2026 22:16:13 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Mon, 16 Mar 2026 22:16:13 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 16 Mar 2026 22:16:13 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 16 Mar 2026 22:16:13 GMT
WORKDIR /opt/emqx
# Mon, 16 Mar 2026 22:16:13 GMT
USER emqx
# Mon, 16 Mar 2026 22:16:13 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 16 Mar 2026 22:16:13 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 16 Mar 2026 22:16:13 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 16 Mar 2026 22:16:13 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:16:13 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904f97fd81e702b2ceee48558a02977070b0bf97e36f34039fa5a86734eacc3f`  
		Last Modified: Mon, 16 Mar 2026 22:16:27 GMT  
		Size: 78.6 MB (78624408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0cad49748de04acd939080e30a3b2a887971ccf4f392aea03ccac0873b564b`  
		Last Modified: Mon, 16 Mar 2026 22:16:25 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.8` - unknown; unknown

```console
$ docker pull emqx@sha256:655a1b87c1e38dd1d1bba5ea39f0d8a84dc1987d7c81fc11b83357e2a4f273f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d84ac141b17d1b991366b927531eb8463dd68817080b2e1df779bd29c537ce63`

```dockerfile
```

-	Layers:
	-	`sha256:6911da73eb750fe99b4739e9b640127f7b6af44a872f4ec088c1df10974a044f`  
		Last Modified: Mon, 16 Mar 2026 22:16:25 GMT  
		Size: 2.4 MB (2403501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11142c734c3da0fb1dc6d1da7967cd13dec9747671764eab62f9d00cb7954b20`  
		Last Modified: Mon, 16 Mar 2026 22:16:25 GMT  
		Size: 12.5 KB (12486 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8.8` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:040d4aa42301e353ac651f52adb6a75450bff0381c7aa9b103f7b832ad25b8b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106671055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607d1f826cd8c5dbdd5e00d0699578f4f64fed11b7c5d22bc340d41dc44af7fa`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:15:29 GMT
ENV EMQX_VERSION=5.8.8
# Mon, 16 Mar 2026 22:15:29 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Mon, 16 Mar 2026 22:15:29 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Mon, 16 Mar 2026 22:15:29 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 16 Mar 2026 22:15:29 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 16 Mar 2026 22:15:29 GMT
WORKDIR /opt/emqx
# Mon, 16 Mar 2026 22:15:29 GMT
USER emqx
# Mon, 16 Mar 2026 22:15:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 16 Mar 2026 22:15:29 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 16 Mar 2026 22:15:29 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 16 Mar 2026 22:15:29 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:15:29 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0d34e72ceb0b7ab53d6c16e2ca318826abac86182fa008375a7bbce8b63c87`  
		Last Modified: Mon, 16 Mar 2026 22:15:44 GMT  
		Size: 76.5 MB (76531577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9d9386780f37c816b9f75c4fa04cc5b475c7af0fe1032d44244a71313c9a50`  
		Last Modified: Mon, 16 Mar 2026 22:15:42 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8.8` - unknown; unknown

```console
$ docker pull emqx@sha256:5cd2d78a1e35893eb56365ce044dc883865829c997fdfd81a9f70275aca20482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97dad188baac0f204140fac0fe3f18792f26db5051a6d3be9f823d00cd274c0`

```dockerfile
```

-	Layers:
	-	`sha256:8edb65027663c927b9e5e6ad3082a0d4b0e8aa0e4a34044b4077f7537c37b54a`  
		Last Modified: Mon, 16 Mar 2026 22:15:42 GMT  
		Size: 2.4 MB (2403790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8839089d3ec10e5f82e0c9fd0f7d2a128217235a91cca99122b61f4b25066a6`  
		Last Modified: Mon, 16 Mar 2026 22:15:42 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:latest`

```console
$ docker pull emqx@sha256:ef071632cd7933e551b074d834b2674096f0490ac242e99756d7a1b14fbcbf0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:6d5ae6bd9ef2b80fcc28df79c37017e7726e4cf139f756849eeecac5bf2ca178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108400970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0da0abaa9f1bcee18bf9c440005800b72e49c391b2097de712041e1629f35f1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:16:13 GMT
ENV EMQX_VERSION=5.8.8
# Mon, 16 Mar 2026 22:16:13 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Mon, 16 Mar 2026 22:16:13 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Mon, 16 Mar 2026 22:16:13 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 16 Mar 2026 22:16:13 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 16 Mar 2026 22:16:13 GMT
WORKDIR /opt/emqx
# Mon, 16 Mar 2026 22:16:13 GMT
USER emqx
# Mon, 16 Mar 2026 22:16:13 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 16 Mar 2026 22:16:13 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 16 Mar 2026 22:16:13 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 16 Mar 2026 22:16:13 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:16:13 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904f97fd81e702b2ceee48558a02977070b0bf97e36f34039fa5a86734eacc3f`  
		Last Modified: Mon, 16 Mar 2026 22:16:27 GMT  
		Size: 78.6 MB (78624408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0cad49748de04acd939080e30a3b2a887971ccf4f392aea03ccac0873b564b`  
		Last Modified: Mon, 16 Mar 2026 22:16:25 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:655a1b87c1e38dd1d1bba5ea39f0d8a84dc1987d7c81fc11b83357e2a4f273f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d84ac141b17d1b991366b927531eb8463dd68817080b2e1df779bd29c537ce63`

```dockerfile
```

-	Layers:
	-	`sha256:6911da73eb750fe99b4739e9b640127f7b6af44a872f4ec088c1df10974a044f`  
		Last Modified: Mon, 16 Mar 2026 22:16:25 GMT  
		Size: 2.4 MB (2403501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11142c734c3da0fb1dc6d1da7967cd13dec9747671764eab62f9d00cb7954b20`  
		Last Modified: Mon, 16 Mar 2026 22:16:25 GMT  
		Size: 12.5 KB (12486 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:040d4aa42301e353ac651f52adb6a75450bff0381c7aa9b103f7b832ad25b8b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106671055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607d1f826cd8c5dbdd5e00d0699578f4f64fed11b7c5d22bc340d41dc44af7fa`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:15:29 GMT
ENV EMQX_VERSION=5.8.8
# Mon, 16 Mar 2026 22:15:29 GMT
ENV AMD64_SHA256=cf48d49f80db3d447a8015c222ef7d4686289f799695c7740c153ae6b0185523
# Mon, 16 Mar 2026 22:15:29 GMT
ENV ARM64_SHA256=7ff020a2b9acc488bb26578e966ef212b75b8418fd8d0b7ec193f9af411e1e68
# Mon, 16 Mar 2026 22:15:29 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 16 Mar 2026 22:15:29 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Mon, 16 Mar 2026 22:15:29 GMT
WORKDIR /opt/emqx
# Mon, 16 Mar 2026 22:15:29 GMT
USER emqx
# Mon, 16 Mar 2026 22:15:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 16 Mar 2026 22:15:29 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Mon, 16 Mar 2026 22:15:29 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Mon, 16 Mar 2026 22:15:29 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:15:29 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0d34e72ceb0b7ab53d6c16e2ca318826abac86182fa008375a7bbce8b63c87`  
		Last Modified: Mon, 16 Mar 2026 22:15:44 GMT  
		Size: 76.5 MB (76531577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9d9386780f37c816b9f75c4fa04cc5b475c7af0fe1032d44244a71313c9a50`  
		Last Modified: Mon, 16 Mar 2026 22:15:42 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:5cd2d78a1e35893eb56365ce044dc883865829c997fdfd81a9f70275aca20482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97dad188baac0f204140fac0fe3f18792f26db5051a6d3be9f823d00cd274c0`

```dockerfile
```

-	Layers:
	-	`sha256:8edb65027663c927b9e5e6ad3082a0d4b0e8aa0e4a34044b4077f7537c37b54a`  
		Last Modified: Mon, 16 Mar 2026 22:15:42 GMT  
		Size: 2.4 MB (2403790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8839089d3ec10e5f82e0c9fd0f7d2a128217235a91cca99122b61f4b25066a6`  
		Last Modified: Mon, 16 Mar 2026 22:15:42 GMT  
		Size: 12.6 KB (12590 bytes)  
		MIME: application/vnd.in-toto+json
