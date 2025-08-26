## `clojure:tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:470a7a0e116087c45c964d6101d6660c978942dbb85a6f53948d712bd7dfc3d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:efc8b485c51857acf9c5a02daf795e15753abe245ee340b2e04b81c42ea0da23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255712310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b36736d3fb57412fae377620f1f58045964bc5348778b255b27012a7886034f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0976a2b85d9680202b5efd21763d991db4f57a6a31baa3d2dea1f16bc33017`  
		Last Modified: Tue, 26 Aug 2025 19:12:35 GMT  
		Size: 157.8 MB (157804752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30aaf088ddf17d6501eec0ad4769c9676fe7e446d751a51e7fbc52809530b02`  
		Last Modified: Tue, 26 Aug 2025 19:12:34 GMT  
		Size: 69.7 MB (69676259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f719ecddafc2592f96b5dc33b1cf07a6838b62e451039f039d30b43df371cb20`  
		Last Modified: Tue, 26 Aug 2025 19:12:27 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281534d0f7a2e520bf96e10e77bbd34e11e770ec1fc13fc27917dbb7f21c3053`  
		Last Modified: Tue, 26 Aug 2025 19:12:27 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e5d9b91d153c68014c0c1b90c52284ea07d12cc3aed06979587ea76a01908013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5131646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441c3057d0a9d35eafe59cf47a1074c1d1484ce89c7d19a6d7b64bb8ae2aa18a`

```dockerfile
```

-	Layers:
	-	`sha256:26b5e5bc27e0b8b33b47306d1626a2ec499c8accdd1adf5e41e43b1dd6407ceb`  
		Last Modified: Tue, 26 Aug 2025 18:39:53 GMT  
		Size: 5.1 MB (5115071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:496bcdc67a197a6c2f5d4a41bb9b0c90464cf5fc8a9932f2539cec9449cab14d`  
		Last Modified: Tue, 26 Aug 2025 18:39:54 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b1ddff4da9f14136b35e43f633f4ce67c0cfd1cf7738bec21a0e6c5fa737131b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253713757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54b3dd1001816565ce3b1bd8359e765dbf2c868dc6a367920985ca2ac64d1dae`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7991a92c7ee87da171852566b076064998d9091210c9e1f68f8874a4a0f1ef`  
		Last Modified: Mon, 18 Aug 2025 20:51:19 GMT  
		Size: 156.1 MB (156081253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c4c2836ef9b52981af34c11d65eccc77018a2c40dad9c8bc696ee34faf28da`  
		Last Modified: Tue, 26 Aug 2025 17:48:34 GMT  
		Size: 69.5 MB (69549460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf06219a6f05ae84a8a8a7f7840eeed8cceb5ada0bc6e16dd01ad1016d386aa`  
		Last Modified: Tue, 26 Aug 2025 17:48:28 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1509569a08fd6fa13b26d5bb128d1de6ea7a482ed7b966773136816cd2b1ee1d`  
		Last Modified: Tue, 26 Aug 2025 17:48:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:541430df0486c295ce1e8e8a2f135a067095af52f0235e7707a7b1cb5478a244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2c6b277f3f98866e145f82a268e1e7682c793964114c055766b23deddd6872`

```dockerfile
```

-	Layers:
	-	`sha256:74307c93ed0102f47d33dfcc74bfd1adc55499acb3001de23fd041f3e6017662`  
		Last Modified: Tue, 26 Aug 2025 18:40:01 GMT  
		Size: 5.1 MB (5120856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:410ee0024ab2796f34b3b38687b5a7ce55e6374fa17d061273d6f71e1e873f2f`  
		Last Modified: Tue, 26 Aug 2025 18:40:02 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:c9c9aef3fb59ca549448101067f4a3ff3da53794bfb5de1a04a0043a2af4b842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.4 MB (265444668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfaa9c39a56fcb853845d29a09b5bf038912e917acd896843661ad2db733e16f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f159f526f8a9c3649fee57d0df8248d04aeb1f957c2fcd7d35d584b2f74bdf`  
		Last Modified: Tue, 19 Aug 2025 18:06:25 GMT  
		Size: 158.0 MB (157963439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e8a316ff386438bea7db2703240e600588816fc10e30591d522bf8ab520aa2`  
		Last Modified: Mon, 18 Aug 2025 17:27:58 GMT  
		Size: 75.4 MB (75406766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e2d3c02bcc1f65699ce97030616bc4a16bb2a2ca9baee40c9ecec1a54576b7`  
		Last Modified: Mon, 18 Aug 2025 17:27:49 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca79fe52215be3d2995e531dc6b9c148d335ee94b1260f650ada4253cc129a5`  
		Last Modified: Mon, 18 Aug 2025 17:27:49 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:40a5e970b0efd3cd852200c8c4e02f95e6d6eb2372b45c2717467a0db94a74c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5136876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936dfc8728e055203414e23be8f09a42bd5f4b2c3887a8e835823a92fbac8dcc`

```dockerfile
```

-	Layers:
	-	`sha256:f5024f52b78db729e1b36ddb54524415ab0c173099825067b5f586ce8274d1cf`  
		Last Modified: Mon, 18 Aug 2025 18:40:17 GMT  
		Size: 5.1 MB (5120241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10e501bd5c3ca25dd9bfb6501e68210822c532fd8715b045ba66dcd9cc290a8e`  
		Last Modified: Mon, 18 Aug 2025 18:40:18 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:125f3f26c216ad19f8bc0f45ba030ab1f6f28c57d042208ac66c1a37e67ea5c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242303959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93673982fa6d52bc9aa17a16e8a606d7b148f0fdc1a3627476c26dd82138ffbc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f1cd2e643b85f38b855ab774d4606497ec4c96716612b07695839e1f191597`  
		Last Modified: Tue, 19 Aug 2025 18:06:08 GMT  
		Size: 147.0 MB (147026954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b68b6c5d3ca276eb037bf2837b8aadc76425b02d267f15248a559a539bd5dd`  
		Last Modified: Mon, 18 Aug 2025 17:51:59 GMT  
		Size: 68.4 MB (68388126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff56a384e39296cd36ec6e33a5b063320366d7b98be8abeba2407d6af881765`  
		Last Modified: Mon, 18 Aug 2025 17:51:42 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35607ae545ba54cba461c96dd15383b7a5d95703528bd296ac551f17edb34f72`  
		Last Modified: Mon, 18 Aug 2025 17:51:42 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:539d4276a1cdcf2cc5b7679513959b77b32277418b2880ff673bad8fa72e2acb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5122966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10b881abdc03b18131243b7b5173f008b386a55e13967b836988e966f4c2cc5d`

```dockerfile
```

-	Layers:
	-	`sha256:f5f9323ac6ef19939d7d818ee94b520373802ba1dbb2f74229c9a751a9ce0a5b`  
		Last Modified: Mon, 18 Aug 2025 18:40:23 GMT  
		Size: 5.1 MB (5106392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c57f51533344c26f4d4505ca5eb5aaa979ed26df268b990f595e9ef6ee9d6d22`  
		Last Modified: Mon, 18 Aug 2025 18:40:24 GMT  
		Size: 16.6 KB (16574 bytes)  
		MIME: application/vnd.in-toto+json
