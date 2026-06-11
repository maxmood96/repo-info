## `clojure:temurin-11-trixie-slim`

```console
$ docker pull clojure@sha256:418956bd8e237b1da2a2558d5346dec825e3e1f73a8009dc5ef8af180b0f959d
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

### `clojure:temurin-11-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:934b4f01dc3ae398c820fb4f56a851d1acb5b17951fb6c384f4a75df3b81ebb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244623929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:123261516bc9349f1d2fcdfb3d75a0f0fc6a01740ec85c8255449047a98349a5`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:17:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:17:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:17:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:17:52 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:17:52 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:18:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:18:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:18:08 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2939ac8ab476ff537b17050b25e2fafea7bf4f86046fa7193130889dac01e4`  
		Last Modified: Thu, 11 Jun 2026 01:18:30 GMT  
		Size: 145.9 MB (145886263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c01e709ee894e080699ab2f10ee67ff10cd6b7d1364514a27be04fbf3b86fe`  
		Last Modified: Thu, 11 Jun 2026 01:18:29 GMT  
		Size: 69.0 MB (68951607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9657d3e0c2e66860f0decc335efceb7198102ce399a68d96367277ead43dc6`  
		Last Modified: Thu, 11 Jun 2026 01:18:25 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2e5619bc7a7dd24bbb22e8683293cbab083f6a6dc317f7c1ea49e00716df5727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5291155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe8bc4e7e6b26e894c767724c323ad189aa767566372a59d7f71728e59a2c77`

```dockerfile
```

-	Layers:
	-	`sha256:2045bb188b49f6691673f5ce15a3dd7fe34f1f24c9615faf91c6f5156f9f15d1`  
		Last Modified: Thu, 11 Jun 2026 01:18:26 GMT  
		Size: 5.3 MB (5276758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:652fcd4f392d805ed91d4a202e9c1a878f2d7e95bd302f2d270fff29d9a2bdfd`  
		Last Modified: Thu, 11 Jun 2026 01:18:25 GMT  
		Size: 14.4 KB (14397 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:21f1501eb7802e9711b73673ca1b76464b5652c404cb38885a3a91c8ae331f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.5 MB (241508726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:805b92db95a3d0067d9b0087cc3b3c0e0f53ec6445283f5171f935b4e17dcbb9`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:22:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:22:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:22:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:22:06 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:22:06 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:22:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:22:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:22:23 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab3321c3b1ead911d01bc404260fcd2b1ca0b986e766f50cc1ab43a6795cfaf`  
		Last Modified: Thu, 11 Jun 2026 01:22:47 GMT  
		Size: 142.6 MB (142582230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92546c10de2a367201eb6680c8505dd3dbc4bdae1c6f1e6dadcb93f82d70f2b`  
		Last Modified: Thu, 11 Jun 2026 01:22:44 GMT  
		Size: 68.8 MB (68777322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e02375fe09ce95e2ed9b31169fd412b9a15871ec79e2807785cece885022ee0c`  
		Last Modified: Thu, 11 Jun 2026 01:22:40 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2ed0ff758fbc8864b3f38d32e69e0c6d41d2f9c464babe39ce656c5acff162c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29f48c37fa12885dc859965d4ca405131e473c4bcde6a84f48f6ffa770cc899d`

```dockerfile
```

-	Layers:
	-	`sha256:33e3ffb17299cdd904f06e096e6224f1e5be0b4556a7257da8206c1ac18e85b5`  
		Last Modified: Thu, 11 Jun 2026 01:22:41 GMT  
		Size: 5.3 MB (5283137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:098650593aec2430611e6582c046ebf5f3666c8e8a71ec88550693b46e2e7ff8`  
		Last Modified: Thu, 11 Jun 2026 01:22:40 GMT  
		Size: 14.5 KB (14515 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:0596ea11a693cf60e70f303fccfc4618df6a4a5788edfb213ed09e4c8b530d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241086324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9fc974faa51e6feb9a40b93b8727f68f629d71073409e3e9233bbdc0ca3fd88`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 09:24:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 09:24:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 09:24:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 09:24:10 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 09:24:11 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 09:28:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 09:28:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 09:28:13 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9054a5ac768834a10d14169acc177113311408987ed6c5625592f8ed37e45e6d`  
		Last Modified: Thu, 11 Jun 2026 09:25:29 GMT  
		Size: 133.1 MB (133110170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498e8bbfd20a42c2f2ab957a1bc9dcdd1e0fe577488643d1fdb4c5d2bdae142d`  
		Last Modified: Thu, 11 Jun 2026 09:28:49 GMT  
		Size: 74.4 MB (74369170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feac09fd9ee3d468b16e7228c9dd2b6cbe62a3187588a02c57f858c6582be7fc`  
		Last Modified: Thu, 11 Jun 2026 09:28:47 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ddef48ccfa2a2c878f27899f11fca2b514af7513cbba335d9368a6b7322a29fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5294004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aada5da33306b7bcdbeef856869e16a084373b4a144c2d15c5166893ca98533`

```dockerfile
```

-	Layers:
	-	`sha256:cf15e9eebcb24fc849c268f13fd4080b9481d051c00ce5087380a90e5ab51d91`  
		Last Modified: Thu, 11 Jun 2026 09:28:47 GMT  
		Size: 5.3 MB (5280514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1595f03c73e7bc6f48727e54b692faab049c3ff1e710d9b8f23f8361391b58f`  
		Last Modified: Thu, 11 Jun 2026 09:28:47 GMT  
		Size: 13.5 KB (13490 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:244163f1c4c553d68c456f2d57268bc7c2c6a1915e2c5da53ee240a75d3f1b4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226436265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78a6f0d1d8c240a63088e3be37930284650d51c450951675e4ccbdfd6565c2cf`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 03:07:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:07:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:07:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:07:28 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 03:07:28 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:08:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 03:08:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 03:08:58 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5802eb9f5d41feedb6c258a1f1f2df21baf827b10fc2b57c1794f8c975245ec2`  
		Last Modified: Thu, 11 Jun 2026 03:08:13 GMT  
		Size: 126.7 MB (126651744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bddae99a41b2a91fd261ca6862a705d2f7a7fe3f17d9bad14864f1f7fbb7e094`  
		Last Modified: Thu, 11 Jun 2026 03:09:23 GMT  
		Size: 69.9 MB (69932522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c84831520d7f6d06a80100f1f2a87693aa89414f694ced15b22d7235fa5f44`  
		Last Modified: Thu, 11 Jun 2026 03:09:21 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dc1118c3ba70bc5c3af66969fa6a2d6be76778b82e0c33e6cf637170969a846c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5286128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da4c0c43eeef18f7fadff309b1fea1b46a6b005478400a3e05709cc177cb5691`

```dockerfile
```

-	Layers:
	-	`sha256:5a5c48bfb7862ee7d1efffdd698a554894dd6f23978ff4c1dc436d288d0c313a`  
		Last Modified: Thu, 11 Jun 2026 03:09:22 GMT  
		Size: 5.3 MB (5272686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87575554b20b0eb05afa72d05dadfd0dcbb2b3ce514dced9d7e2ef45301ff3a4`  
		Last Modified: Thu, 11 Jun 2026 03:09:21 GMT  
		Size: 13.4 KB (13442 bytes)  
		MIME: application/vnd.in-toto+json
