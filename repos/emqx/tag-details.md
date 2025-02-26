<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:5`](#emqx5)
-	[`emqx:5.7`](#emqx57)
-	[`emqx:5.7.2`](#emqx572)
-	[`emqx:5.8`](#emqx58)
-	[`emqx:5.8.5`](#emqx585)
-	[`emqx:latest`](#emqxlatest)

## `emqx:5`

```console
$ docker pull emqx@sha256:7589d8c001c0f81b40525f881bf2b744348e40b864510a607906597bfa53b3a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:59d47b398e0f526bb95d4bb1a6325d89714b138fd50099bfdf6890e431b18121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105357366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7c825a495d939c2878b65b7331cf527aa64eb27e3abf2acc0d7b67f6b2d5bc`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 07 Jan 2025 05:32:24 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Tue, 07 Jan 2025 05:32:24 GMT
ENV EMQX_VERSION=5.8.4
# Tue, 07 Jan 2025 05:32:24 GMT
ENV AMD64_SHA256=48776760e500e0e38b810c9c2e4156ec5022565f700bbea121695e76463ed042
# Tue, 07 Jan 2025 05:32:24 GMT
ENV ARM64_SHA256=dd45d06ee2f7f5ace05ec9ce53b2739b54dad2105cdfcadb6f7bb514724caf91
# Tue, 07 Jan 2025 05:32:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 07 Jan 2025 05:32:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
WORKDIR /opt/emqx
# Tue, 07 Jan 2025 05:32:24 GMT
USER emqx
# Tue, 07 Jan 2025 05:32:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 07 Jan 2025 05:32:24 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 07 Jan 2025 05:32:24 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 07 Jan 2025 05:32:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9263fe54900f156534cb9a1964bfc66dc8f31de5c54739bb44ce1204c901cc`  
		Last Modified: Tue, 25 Feb 2025 02:11:58 GMT  
		Size: 77.1 MB (77137001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26af8a37ffeff4fa44fc228b4fcbac7c3b3bfb8875d1c5e7ab4c40719d067c75`  
		Last Modified: Tue, 25 Feb 2025 02:11:57 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:4b983fe2456a8ddf74dfcb394fc84e964722e1e2fdf0650a0eb676fb925f9b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2483093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92fd031fdbecc71d7836b7a1ff03397f6b0f18dc4c60a29251941453cf50d193`

```dockerfile
```

-	Layers:
	-	`sha256:d6e3d161547765763c0b252493f1762d6c61e7b9faaf31025a0ed6e8bae3a97a`  
		Last Modified: Tue, 25 Feb 2025 02:11:57 GMT  
		Size: 2.5 MB (2470564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:771463518a0be09906a92ba6f60ca5c2bed9a673416e8443c73dcdbcb99c7440`  
		Last Modified: Tue, 25 Feb 2025 02:11:57 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:bb4f87d7d3a6116acabab76f27d35cba214b11baa6d2e31f9aed5e76116e43e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102457966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f93c89683094d71279385fd2d6dc21d36570f45298bf66605ed86f6670200756`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 07 Jan 2025 05:32:24 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Tue, 07 Jan 2025 05:32:24 GMT
ENV EMQX_VERSION=5.8.4
# Tue, 07 Jan 2025 05:32:24 GMT
ENV AMD64_SHA256=48776760e500e0e38b810c9c2e4156ec5022565f700bbea121695e76463ed042
# Tue, 07 Jan 2025 05:32:24 GMT
ENV ARM64_SHA256=dd45d06ee2f7f5ace05ec9ce53b2739b54dad2105cdfcadb6f7bb514724caf91
# Tue, 07 Jan 2025 05:32:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 07 Jan 2025 05:32:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
WORKDIR /opt/emqx
# Tue, 07 Jan 2025 05:32:24 GMT
USER emqx
# Tue, 07 Jan 2025 05:32:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 07 Jan 2025 05:32:24 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 07 Jan 2025 05:32:24 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 07 Jan 2025 05:32:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27c5b469ad917972405d37e069f91a116dd976b97cf678e0690d0622c01bf2a`  
		Last Modified: Tue, 25 Feb 2025 02:19:07 GMT  
		Size: 74.4 MB (74408477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39f64e39954115c3c2337a4140f13ceef8da269cf842eeedbf4a548fd8ec08a`  
		Last Modified: Tue, 25 Feb 2025 02:19:05 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5` - unknown; unknown

```console
$ docker pull emqx@sha256:e6053c2d522e4981890e166ba0e036044f59383d92ac7a3d2b5af33efed83565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a6a595128f2a02f8d5b6a605c188c0413bc21a1d3a5fe6a428dc9a0800c0a76`

```dockerfile
```

-	Layers:
	-	`sha256:f7b05da203bf1d9874b7d2966dee910af35010ccb8f578aaa61af08141c648b2`  
		Last Modified: Tue, 25 Feb 2025 02:19:05 GMT  
		Size: 2.6 MB (2614780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa9bd5667c99e9a4035c31bf4b1e4c3c9f6112814fc03dc0874b33945077322d`  
		Last Modified: Tue, 25 Feb 2025 02:19:05 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7`

```console
$ docker pull emqx@sha256:f1db05edcec99e0c811c79257582d103844d2668cfeddafe2aeee1bb64dc4747
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7` - linux; amd64

```console
$ docker pull emqx@sha256:19bef65c58a9d80e7b16532682048499386b2a97443f32e338ba4f593904f45b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125368143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acfa6e4d932249862f18693d6c17e5d44f9266c019fd0189fb33a43af4df8c5e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06295ae8c5f311aab004684137a401206e103b1223d50549de5f51e490d63a91`  
		Last Modified: Tue, 25 Feb 2025 02:11:55 GMT  
		Size: 97.1 MB (97147780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1623c54f375602bb851b2a56ee34806ffa1adc91313f7db32597491d62718b8`  
		Last Modified: Tue, 25 Feb 2025 02:11:54 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:4a223a603e47ea2970b3f59a55a22985ef320f5fda9ce3428a00b65a3d7ecdd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2481936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b8b1f5b8be3bf3db841d6559d69549fdaa3c34ae5baf30942af16cc8c263ad`

```dockerfile
```

-	Layers:
	-	`sha256:e7d29a56f2a5dce372bd688ebfcc912c47457df63f8002a5e74e20270dbec5ab`  
		Last Modified: Tue, 25 Feb 2025 02:11:54 GMT  
		Size: 2.5 MB (2469986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:361431caf86526d1b02a2a1132ff3efc67a3b5bc697709731838ca1eaf8465b5`  
		Last Modified: Tue, 25 Feb 2025 02:11:54 GMT  
		Size: 11.9 KB (11950 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:fc1f0bc72480373cb6026e537271120d66f5427ac865d2da3ffcff7f73a5d5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121745136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b464c6dcfc92f136330077d779362fb41087d4c6c4fc26fa9f59708f25960c3`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b75f0ae6ae2f3d7a07935e2e953a9049f63039114decfe8ccf4ff4ce987b69`  
		Last Modified: Tue, 25 Feb 2025 02:18:37 GMT  
		Size: 93.7 MB (93695648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a672a2c5d502e4285088b479ad1934c813f4ca20c43001bbce878b5280609cf`  
		Last Modified: Tue, 25 Feb 2025 02:18:34 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7` - unknown; unknown

```console
$ docker pull emqx@sha256:95ee8343bc0b25fd940a40884b66c2bc621e8bf24aa36e413f9bf92e1cdd1e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2636186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e166d78a7d069dc27968deff9034284ccf029123ce40b9d3c1d7327c89d140c`

```dockerfile
```

-	Layers:
	-	`sha256:3600e2fee9d3ba1ffbe41bc43ebb773cf8787a74c9a03b19eba34b807b12c693`  
		Last Modified: Tue, 25 Feb 2025 02:18:34 GMT  
		Size: 2.6 MB (2624155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:598f302a8cb26e3042885c9f04bc95a726d89ee978c4b495d7c546f524e08942`  
		Last Modified: Tue, 25 Feb 2025 02:18:34 GMT  
		Size: 12.0 KB (12031 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.7.2`

```console
$ docker pull emqx@sha256:f1db05edcec99e0c811c79257582d103844d2668cfeddafe2aeee1bb64dc4747
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.7.2` - linux; amd64

```console
$ docker pull emqx@sha256:19bef65c58a9d80e7b16532682048499386b2a97443f32e338ba4f593904f45b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125368143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acfa6e4d932249862f18693d6c17e5d44f9266c019fd0189fb33a43af4df8c5e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06295ae8c5f311aab004684137a401206e103b1223d50549de5f51e490d63a91`  
		Last Modified: Tue, 25 Feb 2025 02:11:55 GMT  
		Size: 97.1 MB (97147780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1623c54f375602bb851b2a56ee34806ffa1adc91313f7db32597491d62718b8`  
		Last Modified: Tue, 25 Feb 2025 02:11:54 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:4a223a603e47ea2970b3f59a55a22985ef320f5fda9ce3428a00b65a3d7ecdd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2481936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b8b1f5b8be3bf3db841d6559d69549fdaa3c34ae5baf30942af16cc8c263ad`

```dockerfile
```

-	Layers:
	-	`sha256:e7d29a56f2a5dce372bd688ebfcc912c47457df63f8002a5e74e20270dbec5ab`  
		Last Modified: Tue, 25 Feb 2025 02:11:54 GMT  
		Size: 2.5 MB (2469986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:361431caf86526d1b02a2a1132ff3efc67a3b5bc697709731838ca1eaf8465b5`  
		Last Modified: Tue, 25 Feb 2025 02:11:54 GMT  
		Size: 11.9 KB (11950 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.7.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:fc1f0bc72480373cb6026e537271120d66f5427ac865d2da3ffcff7f73a5d5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.7 MB (121745136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b464c6dcfc92f136330077d779362fb41087d4c6c4fc26fa9f59708f25960c3`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Mon, 12 Aug 2024 08:39:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b75f0ae6ae2f3d7a07935e2e953a9049f63039114decfe8ccf4ff4ce987b69`  
		Last Modified: Tue, 25 Feb 2025 02:18:37 GMT  
		Size: 93.7 MB (93695648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a672a2c5d502e4285088b479ad1934c813f4ca20c43001bbce878b5280609cf`  
		Last Modified: Tue, 25 Feb 2025 02:18:34 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.7.2` - unknown; unknown

```console
$ docker pull emqx@sha256:95ee8343bc0b25fd940a40884b66c2bc621e8bf24aa36e413f9bf92e1cdd1e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2636186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e166d78a7d069dc27968deff9034284ccf029123ce40b9d3c1d7327c89d140c`

```dockerfile
```

-	Layers:
	-	`sha256:3600e2fee9d3ba1ffbe41bc43ebb773cf8787a74c9a03b19eba34b807b12c693`  
		Last Modified: Tue, 25 Feb 2025 02:18:34 GMT  
		Size: 2.6 MB (2624155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:598f302a8cb26e3042885c9f04bc95a726d89ee978c4b495d7c546f524e08942`  
		Last Modified: Tue, 25 Feb 2025 02:18:34 GMT  
		Size: 12.0 KB (12031 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8`

```console
$ docker pull emqx@sha256:7589d8c001c0f81b40525f881bf2b744348e40b864510a607906597bfa53b3a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:5.8` - linux; amd64

```console
$ docker pull emqx@sha256:59d47b398e0f526bb95d4bb1a6325d89714b138fd50099bfdf6890e431b18121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105357366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7c825a495d939c2878b65b7331cf527aa64eb27e3abf2acc0d7b67f6b2d5bc`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 07 Jan 2025 05:32:24 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Tue, 07 Jan 2025 05:32:24 GMT
ENV EMQX_VERSION=5.8.4
# Tue, 07 Jan 2025 05:32:24 GMT
ENV AMD64_SHA256=48776760e500e0e38b810c9c2e4156ec5022565f700bbea121695e76463ed042
# Tue, 07 Jan 2025 05:32:24 GMT
ENV ARM64_SHA256=dd45d06ee2f7f5ace05ec9ce53b2739b54dad2105cdfcadb6f7bb514724caf91
# Tue, 07 Jan 2025 05:32:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 07 Jan 2025 05:32:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
WORKDIR /opt/emqx
# Tue, 07 Jan 2025 05:32:24 GMT
USER emqx
# Tue, 07 Jan 2025 05:32:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 07 Jan 2025 05:32:24 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 07 Jan 2025 05:32:24 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 07 Jan 2025 05:32:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9263fe54900f156534cb9a1964bfc66dc8f31de5c54739bb44ce1204c901cc`  
		Last Modified: Tue, 25 Feb 2025 02:11:58 GMT  
		Size: 77.1 MB (77137001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26af8a37ffeff4fa44fc228b4fcbac7c3b3bfb8875d1c5e7ab4c40719d067c75`  
		Last Modified: Tue, 25 Feb 2025 02:11:57 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:4b983fe2456a8ddf74dfcb394fc84e964722e1e2fdf0650a0eb676fb925f9b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2483093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92fd031fdbecc71d7836b7a1ff03397f6b0f18dc4c60a29251941453cf50d193`

```dockerfile
```

-	Layers:
	-	`sha256:d6e3d161547765763c0b252493f1762d6c61e7b9faaf31025a0ed6e8bae3a97a`  
		Last Modified: Tue, 25 Feb 2025 02:11:57 GMT  
		Size: 2.5 MB (2470564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:771463518a0be09906a92ba6f60ca5c2bed9a673416e8443c73dcdbcb99c7440`  
		Last Modified: Tue, 25 Feb 2025 02:11:57 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:5.8` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:bb4f87d7d3a6116acabab76f27d35cba214b11baa6d2e31f9aed5e76116e43e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102457966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f93c89683094d71279385fd2d6dc21d36570f45298bf66605ed86f6670200756`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 07 Jan 2025 05:32:24 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Tue, 07 Jan 2025 05:32:24 GMT
ENV EMQX_VERSION=5.8.4
# Tue, 07 Jan 2025 05:32:24 GMT
ENV AMD64_SHA256=48776760e500e0e38b810c9c2e4156ec5022565f700bbea121695e76463ed042
# Tue, 07 Jan 2025 05:32:24 GMT
ENV ARM64_SHA256=dd45d06ee2f7f5ace05ec9ce53b2739b54dad2105cdfcadb6f7bb514724caf91
# Tue, 07 Jan 2025 05:32:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 07 Jan 2025 05:32:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
WORKDIR /opt/emqx
# Tue, 07 Jan 2025 05:32:24 GMT
USER emqx
# Tue, 07 Jan 2025 05:32:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 07 Jan 2025 05:32:24 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 07 Jan 2025 05:32:24 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 07 Jan 2025 05:32:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27c5b469ad917972405d37e069f91a116dd976b97cf678e0690d0622c01bf2a`  
		Last Modified: Tue, 25 Feb 2025 02:19:07 GMT  
		Size: 74.4 MB (74408477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39f64e39954115c3c2337a4140f13ceef8da269cf842eeedbf4a548fd8ec08a`  
		Last Modified: Tue, 25 Feb 2025 02:19:05 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:5.8` - unknown; unknown

```console
$ docker pull emqx@sha256:e6053c2d522e4981890e166ba0e036044f59383d92ac7a3d2b5af33efed83565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a6a595128f2a02f8d5b6a605c188c0413bc21a1d3a5fe6a428dc9a0800c0a76`

```dockerfile
```

-	Layers:
	-	`sha256:f7b05da203bf1d9874b7d2966dee910af35010ccb8f578aaa61af08141c648b2`  
		Last Modified: Tue, 25 Feb 2025 02:19:05 GMT  
		Size: 2.6 MB (2614780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa9bd5667c99e9a4035c31bf4b1e4c3c9f6112814fc03dc0874b33945077322d`  
		Last Modified: Tue, 25 Feb 2025 02:19:05 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json

## `emqx:5.8.5`

```console
$ docker pull emqx@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `emqx:latest`

```console
$ docker pull emqx@sha256:7589d8c001c0f81b40525f881bf2b744348e40b864510a607906597bfa53b3a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:59d47b398e0f526bb95d4bb1a6325d89714b138fd50099bfdf6890e431b18121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.4 MB (105357366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7c825a495d939c2878b65b7331cf527aa64eb27e3abf2acc0d7b67f6b2d5bc`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 07 Jan 2025 05:32:24 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Tue, 07 Jan 2025 05:32:24 GMT
ENV EMQX_VERSION=5.8.4
# Tue, 07 Jan 2025 05:32:24 GMT
ENV AMD64_SHA256=48776760e500e0e38b810c9c2e4156ec5022565f700bbea121695e76463ed042
# Tue, 07 Jan 2025 05:32:24 GMT
ENV ARM64_SHA256=dd45d06ee2f7f5ace05ec9ce53b2739b54dad2105cdfcadb6f7bb514724caf91
# Tue, 07 Jan 2025 05:32:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 07 Jan 2025 05:32:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
WORKDIR /opt/emqx
# Tue, 07 Jan 2025 05:32:24 GMT
USER emqx
# Tue, 07 Jan 2025 05:32:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 07 Jan 2025 05:32:24 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 07 Jan 2025 05:32:24 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 07 Jan 2025 05:32:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef9263fe54900f156534cb9a1964bfc66dc8f31de5c54739bb44ce1204c901cc`  
		Last Modified: Tue, 25 Feb 2025 02:11:58 GMT  
		Size: 77.1 MB (77137001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26af8a37ffeff4fa44fc228b4fcbac7c3b3bfb8875d1c5e7ab4c40719d067c75`  
		Last Modified: Tue, 25 Feb 2025 02:11:57 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:4b983fe2456a8ddf74dfcb394fc84e964722e1e2fdf0650a0eb676fb925f9b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2483093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92fd031fdbecc71d7836b7a1ff03397f6b0f18dc4c60a29251941453cf50d193`

```dockerfile
```

-	Layers:
	-	`sha256:d6e3d161547765763c0b252493f1762d6c61e7b9faaf31025a0ed6e8bae3a97a`  
		Last Modified: Tue, 25 Feb 2025 02:11:57 GMT  
		Size: 2.5 MB (2470564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:771463518a0be09906a92ba6f60ca5c2bed9a673416e8443c73dcdbcb99c7440`  
		Last Modified: Tue, 25 Feb 2025 02:11:57 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:bb4f87d7d3a6116acabab76f27d35cba214b11baa6d2e31f9aed5e76116e43e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102457966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f93c89683094d71279385fd2d6dc21d36570f45298bf66605ed86f6670200756`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 07 Jan 2025 05:32:24 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Tue, 07 Jan 2025 05:32:24 GMT
ENV EMQX_VERSION=5.8.4
# Tue, 07 Jan 2025 05:32:24 GMT
ENV AMD64_SHA256=48776760e500e0e38b810c9c2e4156ec5022565f700bbea121695e76463ed042
# Tue, 07 Jan 2025 05:32:24 GMT
ENV ARM64_SHA256=dd45d06ee2f7f5ace05ec9ce53b2739b54dad2105cdfcadb6f7bb514724caf91
# Tue, 07 Jan 2025 05:32:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 07 Jan 2025 05:32:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     . /etc/os-release;     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     ln -s /opt/emqx/bin/* /usr/local/bin/;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chown -R emqx:emqx /opt/emqx;     rm -f $pkg;     rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
WORKDIR /opt/emqx
# Tue, 07 Jan 2025 05:32:24 GMT
USER emqx
# Tue, 07 Jan 2025 05:32:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 07 Jan 2025 05:32:24 GMT
EXPOSE map[18083/tcp:{} 1883/tcp:{} 4370/tcp:{} 5369/tcp:{} 8083/tcp:{} 8084/tcp:{} 8883/tcp:{}]
# Tue, 07 Jan 2025 05:32:24 GMT
COPY docker-entrypoint.sh /usr/bin/ # buildkit
# Tue, 07 Jan 2025 05:32:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 07 Jan 2025 05:32:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27c5b469ad917972405d37e069f91a116dd976b97cf678e0690d0622c01bf2a`  
		Last Modified: Tue, 25 Feb 2025 02:19:07 GMT  
		Size: 74.4 MB (74408477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39f64e39954115c3c2337a4140f13ceef8da269cf842eeedbf4a548fd8ec08a`  
		Last Modified: Tue, 25 Feb 2025 02:19:05 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `emqx:latest` - unknown; unknown

```console
$ docker pull emqx@sha256:e6053c2d522e4981890e166ba0e036044f59383d92ac7a3d2b5af33efed83565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a6a595128f2a02f8d5b6a605c188c0413bc21a1d3a5fe6a428dc9a0800c0a76`

```dockerfile
```

-	Layers:
	-	`sha256:f7b05da203bf1d9874b7d2966dee910af35010ccb8f578aaa61af08141c648b2`  
		Last Modified: Tue, 25 Feb 2025 02:19:05 GMT  
		Size: 2.6 MB (2614780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa9bd5667c99e9a4035c31bf4b1e4c3c9f6112814fc03dc0874b33945077322d`  
		Last Modified: Tue, 25 Feb 2025 02:19:05 GMT  
		Size: 12.6 KB (12633 bytes)  
		MIME: application/vnd.in-toto+json
