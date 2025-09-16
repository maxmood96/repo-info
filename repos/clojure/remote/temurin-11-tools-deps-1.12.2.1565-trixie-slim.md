## `clojure:temurin-11-tools-deps-1.12.2.1565-trixie-slim`

```console
$ docker pull clojure@sha256:25bdb4bfd5c97f19b82a5e009dc0116c186225976b54092bb3fabaf444cce839
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

### `clojure:temurin-11-tools-deps-1.12.2.1565-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0c1e720c3ebc0bf7d9470f2eb3c9430de777ad8ea72a68154fc6041efd9cc20e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 MB (247414766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91702313f589fe9bc596555a476db86838e100f055a6432d8fc69005fd6c3e40`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6df00df25340df1a15dc87cd89b1688d13d27bf9bd662aa1082f8ceb9a3bd36`  
		Last Modified: Mon, 15 Sep 2025 23:25:43 GMT  
		Size: 145.7 MB (145658216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3baae3b44796c85adccc95086b54d495b4ea0d67abee8758dc8f99fb9da16cd`  
		Last Modified: Mon, 15 Sep 2025 23:26:06 GMT  
		Size: 72.0 MB (71982411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c33ebda74420d6dc8e78a2fd665d491f6259725e68933684133c0389737326`  
		Last Modified: Mon, 15 Sep 2025 23:26:02 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8f6c894a97a2331b42a0e03f7f8e11e4813122f58f31465c494487ff2b63d03e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5290540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69319af85794180123b8868c4821ca01397a39a17c20037c9f3505b382aa0256`

```dockerfile
```

-	Layers:
	-	`sha256:1f5c919289f1fc23e3729f499c598e87b1ae69070b647b3136daaff0be23dec9`  
		Last Modified: Tue, 16 Sep 2025 00:38:02 GMT  
		Size: 5.3 MB (5276254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a130fa9ce875d636891d16aa74500dc4c429438f5af1f8437996f951a537e496`  
		Last Modified: Tue, 16 Sep 2025 00:38:03 GMT  
		Size: 14.3 KB (14286 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.2.1565-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:725b5e5bd69126a61b946ebaace6d09fa8dc3a3ef3701b519e6fc191dce77103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.4 MB (244399977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09055ec6fc6a43179a464cb6b218a018dce4c1f38e7fc448fd1821c2708a378f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b9b55f535f6899654d31bb475506ba3fee76f20729a2fabb9a2f6ab1c5c282`  
		Last Modified: Mon, 15 Sep 2025 23:25:56 GMT  
		Size: 142.5 MB (142458787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097564e63766dec7f257e90f2006e9561cb025f09f7265db0a15c40614f4227d`  
		Last Modified: Mon, 15 Sep 2025 23:25:55 GMT  
		Size: 71.8 MB (71803915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0dd685fcdb624e1ec592f52578a87f8aa94616099fff234b1014a8f8aef56d`  
		Last Modified: Tue, 16 Sep 2025 01:56:36 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2dd1e0ced5ffbcdc1e50460e0108691f3460ed1487dd74538f4c34a3763110b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a522834063f2c235cbaec0c0048599f9b70aad194e12a46f87ca8f4058f102d`

```dockerfile
```

-	Layers:
	-	`sha256:fb8c3e16426fa416c59c39ccf2c7fa1fcba510863fb329879d6ddf7b11a8b791`  
		Last Modified: Tue, 16 Sep 2025 00:38:08 GMT  
		Size: 5.3 MB (5282641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a548fc743e19e34d2f3e02cdcbefecb04c4c13bf5afa91c0c94bc21d6c2bcf11`  
		Last Modified: Tue, 16 Sep 2025 00:38:09 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.2.1565-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:f6813b51399caa2b7cfaaf5f35c8a6f2b761371302667952cc3dff39b4b0cb74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243846055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dea577b4f3c82026a91cf83edc6d3dc27ca85fabeea9b9439fb044005af83804`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c94cac26ef981e81b6f0cab59e76bd11b6b65af6f8e3256c3ad1866621521fb`  
		Last Modified: Tue, 09 Sep 2025 09:10:54 GMT  
		Size: 132.9 MB (132853147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67112c9f4061c98789aaa69fd19ec06199f6464f1470c19a07d13e4a83383ab`  
		Last Modified: Tue, 09 Sep 2025 12:16:26 GMT  
		Size: 77.4 MB (77397915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbfe1f754e71592be2fca9277defd27fc0cccc1888827fd1fb063c9ca18db16d`  
		Last Modified: Tue, 09 Sep 2025 13:04:43 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7da50cb228381c22ef4cb18145a0297a0544526fa3d7ad85c7e399db81245225
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5294344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a4a453dcda946c29bed3b2c4ba243edadce54b5e3b2d7a0bd4882ffb0dccd6`

```dockerfile
```

-	Layers:
	-	`sha256:4698a0f098419b2d453283882d48d27182063d3d38a284d60cccd5cf81d9fdd7`  
		Last Modified: Tue, 09 Sep 2025 15:35:49 GMT  
		Size: 5.3 MB (5280010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05373f332c0ffdbf23d4fafd1a6a122c0cc31dbd2968c46519475589dd19b187`  
		Last Modified: Tue, 09 Sep 2025 15:35:49 GMT  
		Size: 14.3 KB (14334 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.2.1565-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:4dede646615e74d67af1b332c097de9962bc41f8bedcd68c6f5ea94203c6b045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228407243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f2cbb0a65c9fd5d4fa354b8ff3cf9502971e84dcf54bac14c1456b519fa5e60`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 26 Aug 2025 17:11:52 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5b3dd12a4d4a204979dd98c6bdd5fd4e2ce8094fed17860ab58a98a1e9df72`  
		Last Modified: Tue, 09 Sep 2025 12:35:09 GMT  
		Size: 125.6 MB (125622199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1940a7376671ce603601a9074088049734f412cc4eed9803f68ccfa30da03f`  
		Last Modified: Tue, 09 Sep 2025 15:36:08 GMT  
		Size: 73.0 MB (72951495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724c4912cfa36798193bc83a00e41fd5aa9bc47d0ce4481d12af2dad43bd9afb`  
		Last Modified: Tue, 09 Sep 2025 06:11:46 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1565-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cc7d7b392b388df64c6b6883070f87a4c72f7878939c1b41206353d1655e6ae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5286467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e773b284fb27fd2b3819b61462cbde9b13961de9632f169ba19250f3e4054fa`

```dockerfile
```

-	Layers:
	-	`sha256:05efe475753eabf85e275a2795a3580c3bdd41b31575bfaff423a675552af845`  
		Last Modified: Tue, 09 Sep 2025 06:36:15 GMT  
		Size: 5.3 MB (5272182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:844e48e43f043ee942d195816ce8dc93107c3e0ca8f7b1929051462731bc119c`  
		Last Modified: Tue, 09 Sep 2025 06:36:16 GMT  
		Size: 14.3 KB (14285 bytes)  
		MIME: application/vnd.in-toto+json
