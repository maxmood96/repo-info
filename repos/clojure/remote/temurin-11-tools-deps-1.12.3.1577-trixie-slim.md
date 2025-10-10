## `clojure:temurin-11-tools-deps-1.12.3.1577-trixie-slim`

```console
$ docker pull clojure@sha256:32bc540d01fba1ed8334dcaec45d6c456a02af06fd50e2384be20e5ba765de4a
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

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:99fcd00ae715644745066d832700e976ec2f219b676f3c8dcd94f7feae09e7ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 MB (250374889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76293da450965584a7d8b80f78f7fe02878fec6ef294f8c7b8a6862f3a540acd`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52ebca87d00ad513511f98a44d8a7b243ca05daf15aa37aa83d2bd3b7fd2104`  
		Last Modified: Thu, 02 Oct 2025 09:29:11 GMT  
		Size: 145.7 MB (145658171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b12b09585ee927b1e975f5f988b80c586d91786cbb8eb73c39c919f1df9fdc`  
		Last Modified: Thu, 02 Oct 2025 08:58:11 GMT  
		Size: 74.9 MB (74938308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b2f18c647d07b6c0bc823429989d25aec05680b298f0ec61a1f4515f9feab5`  
		Last Modified: Thu, 02 Oct 2025 08:58:05 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b0dbb30c2abe76ce6559d612bc0db51c0e63d1c69fe45af403d560ec47740bde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5290594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f8cf62ffb88fb869248a52d10e6fe6a0daca782ac22e06b478412542418a14`

```dockerfile
```

-	Layers:
	-	`sha256:5d9072f6bd14b3ac478ed518a94c3d98f4f9b7aad6008470721d3a37f97f8a75`  
		Last Modified: Thu, 02 Oct 2025 12:37:29 GMT  
		Size: 5.3 MB (5276308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f55185b2492603f83dd3d2b891706c74ca39082e8532ba9376b80370971fda6`  
		Last Modified: Thu, 02 Oct 2025 12:37:30 GMT  
		Size: 14.3 KB (14286 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9582153fa792f1a98e0cea75d58975c8fd5d8038968d08a6d14ac573bf4ec1b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 MB (247726706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709f4c73a2911eef824830910845a80ae7b58c5ae39754522823b990ae74102c`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618d75423bce1f565f31b6086da2409fed7b62cc1272cc1c7ca82825345236df`  
		Last Modified: Thu, 09 Oct 2025 22:27:49 GMT  
		Size: 142.5 MB (142460559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7db1bcff211b4716c1b731b1c304c846d70e49aa945c7c49067f4c6147b3e0`  
		Last Modified: Thu, 09 Oct 2025 22:28:13 GMT  
		Size: 75.1 MB (75124659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee4136eea81a71f3e2625c7f55ae63608419035d699b1ecf54b2fb0c1f40da8`  
		Last Modified: Thu, 09 Oct 2025 22:28:04 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a11dff6b154040e7e18f57c2bbf5561f0127fcfdf28b422b1656b6c8fc6c37f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8b6bebcf3c6b4ef4c8da7b00c0e51b46b4c9ba2a4dafc73cc25a7b138b78243`

```dockerfile
```

-	Layers:
	-	`sha256:b2d1d340b818b3b7a22b4d6d8728bf219d29f4683b6ac12f621ab37f3b8fe3a2`  
		Last Modified: Fri, 10 Oct 2025 03:35:08 GMT  
		Size: 5.3 MB (5282695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5275abda392de28baa84e0bce02aaf7abc7e46599c6825e988cb570330635ea2`  
		Last Modified: Fri, 10 Oct 2025 03:35:09 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:92abd4fbff326dac24b41de23f179f0a777eb62a07d66a2efc5488f07558eae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.0 MB (247040634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f573950dfe4e88b001d53ab152cbf7cc5276202beac06646bc5b4c4577793cf8`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f38963c60f58211f48adb1985b3e1972224f5ee978afbbc88f9d6a9e57994f84`  
		Last Modified: Sun, 05 Oct 2025 11:51:11 GMT  
		Size: 132.9 MB (132853300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e765a73acbb3348daf7f3804a154d52328ad786f05929d8f55c540a6fb08fc9`  
		Last Modified: Thu, 02 Oct 2025 08:41:29 GMT  
		Size: 80.6 MB (80588236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7558696ef75f20f9ea1b4ac59a442c2338c229c9c10925b23bf50fbd09981f77`  
		Last Modified: Thu, 02 Oct 2025 08:41:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bed4d4debece011e8435a37ebcd55cbb00e6703ba438db98d7548f29d8230077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5294398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ef350bf3616c3d51b1054f4576b8a4ad8afe56f34723a7effb9be59c74f528`

```dockerfile
```

-	Layers:
	-	`sha256:2ecefce08227f64136687347adde87abfcdb5084b5a6a88cc49e02838ca2199f`  
		Last Modified: Thu, 02 Oct 2025 09:36:38 GMT  
		Size: 5.3 MB (5280064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:313990a48bf9cb23d4c3928ea02d92dbbeb1075101aa442eaeab7a8f8069b381`  
		Last Modified: Thu, 02 Oct 2025 09:36:39 GMT  
		Size: 14.3 KB (14334 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:4dcce88ed2952a5c50f91b0ff0d4e2897d27f6a44114a48df17da82da9ce1cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231022562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:388886c630afb8aca49ce0c1059f4a6cc9b7041696191c42b1f55af8b24baecb`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e79b5900b5effeda4776d69d4a251c63021d33a0ee35fa09174f72fb2c2348d`  
		Last Modified: Thu, 09 Oct 2025 23:01:47 GMT  
		Size: 125.6 MB (125622160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e28ad475e5850d31559ad5a4a4fd8a122056358bbbcbb146901f63fc424b46`  
		Last Modified: Thu, 09 Oct 2025 23:07:31 GMT  
		Size: 75.6 MB (75562527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:341fb9185caaf29f861e138acceb05af227fe4253b0af3fa7442eb60493a3132`  
		Last Modified: Thu, 09 Oct 2025 23:07:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ec7c30648c2b7946cfbdd52b9fabd7f67f873da8995c3d970b7daf693b5a2454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5286521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad25d428ba507bacee76b7cbef4221054c7f2eb97a3fec9a7f712eaa7a7d8ec4`

```dockerfile
```

-	Layers:
	-	`sha256:42e553ca624159931c3989469da2f188896ec5318d323b25eb4b32ea28f7fd8b`  
		Last Modified: Fri, 10 Oct 2025 00:36:45 GMT  
		Size: 5.3 MB (5272236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b500d9ed0593c91fdc203b5ab1f6e68d564230fde0674c83800ee3c73814cf9`  
		Last Modified: Fri, 10 Oct 2025 00:36:46 GMT  
		Size: 14.3 KB (14285 bytes)  
		MIME: application/vnd.in-toto+json
