## `clojure:temurin-11-bookworm-slim`

```console
$ docker pull clojure@sha256:99452606ec9a6bd94b991257f01562120ef006f9a4afeabda4746b521209ce4b
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

### `clojure:temurin-11-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:87658c2332544938aa70de7a8433e213cd3c59b43c4a30f2d4c0548799da0290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242872516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d257b52741a3feb9f98425ea173282672e089a56edb67fcec6321405812438`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:23:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:23:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:23:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:23:38 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:23:38 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:27:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:27:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:27:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b03ac94e93ce5604e190a298621555423cbb379a3190cf61a7755de240cc03`  
		Last Modified: Tue, 13 Jan 2026 03:24:12 GMT  
		Size: 145.0 MB (144966652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12a3efd305d58a3f920e882656e4dfda17e9b9dfc8ca6af5ec68681213520be`  
		Last Modified: Tue, 13 Jan 2026 03:27:34 GMT  
		Size: 69.7 MB (69676648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb39a253a3ba9bad67923bc45633a29d0bc25e74bbcc5e073688983104421d51`  
		Last Modified: Tue, 13 Jan 2026 03:27:30 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e68efd36b07ff200597cbf7be2e57cb3d73fc621f65d5f402f28a152f78f53d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5147005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6c3b1cf4675d8028858e743f2ddeecb66e717535dec7f0cccd3e39cd9c0c299`

```dockerfile
```

-	Layers:
	-	`sha256:46e2677197bfa54c2a568b3c6f147795e28a82bf24208fe9aa5d410557817023`  
		Last Modified: Tue, 13 Jan 2026 07:36:42 GMT  
		Size: 5.1 MB (5133539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e19de54eb066b120f88231404da77616157c22fcddf6adf79a578284ab394f8`  
		Last Modified: Tue, 13 Jan 2026 07:36:42 GMT  
		Size: 13.5 KB (13466 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:58e11ce9d25ec952f2a7528b57fbd8deb5940fff367460d06fa0d0429cef22ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.5 MB (239512769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370b2b8dd594a0a8f4d922ff89e34ab2f6243dcf2483944d70eb848fa99d61a6`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:31:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:31:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:31:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:31:17 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:31:17 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:31:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:31:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:31:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d7147aee72b66e37fd7d0a6827010278d17065623f4148866fca3e62d59206`  
		Last Modified: Tue, 13 Jan 2026 03:31:55 GMT  
		Size: 141.7 MB (141731577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3f28524b0e70f7dec26d9baa0c69eae61b5a387a77bd3888667ff3c8381bd3e`  
		Last Modified: Tue, 13 Jan 2026 03:32:06 GMT  
		Size: 69.7 MB (69672660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d9bdbe9e502ac116367c5f0c68e5c9269f3f85570d3caff7e5dd9a44db7a0e`  
		Last Modified: Tue, 13 Jan 2026 03:32:00 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3b32f3f649db6d423b6bee6384fcdf6994679ab66071d3426f8aae313c81980c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5154303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:832d8561acedbe8bea6f7c02fdf2a28e3cec355b6d454cec42a3175a17cf4598`

```dockerfile
```

-	Layers:
	-	`sha256:0e730301936d5434548eb9a23738cf64de6966ce29d0bf84fd2300145da3c271`  
		Last Modified: Tue, 13 Jan 2026 07:36:47 GMT  
		Size: 5.1 MB (5139918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d559f869d5988efdad4049d766642cbfe088d51d901da5f694994cd9d62ed30d`  
		Last Modified: Tue, 13 Jan 2026 07:36:48 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:69e0465009257719eb5f490352e7ab29849ff560cf983da2e1d5525d60f135b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.7 MB (239661120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ccccd4d88145d1fd99d1c9a78b0be166ba76520b3e530dd321c2517415d19b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 05:14:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 05:14:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 05:14:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 05:14:14 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 05:14:15 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 05:16:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 05:16:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 05:16:47 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b7648f01f6858fc79caf032b4b9ed2f7e43e57f4621dc8cb36e84eb86399065b`  
		Last Modified: Tue, 30 Dec 2025 01:48:36 GMT  
		Size: 32.1 MB (32068844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28d8ccc35fc31711a7931dd555a5784bc61992d973063264ed06d23cca9c64f7`  
		Last Modified: Tue, 30 Dec 2025 05:18:24 GMT  
		Size: 132.1 MB (132081964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260af39645f62526779a9353bab91c1f1a99c27a4803e39e57ba7727e13288b8`  
		Last Modified: Tue, 30 Dec 2025 05:17:40 GMT  
		Size: 75.5 MB (75509669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dcc2426080ccba654a2ec1e33817d8ae747a2e0d05e67c366969bddb9615597`  
		Last Modified: Tue, 30 Dec 2025 05:17:33 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3d522b27e2a4ff6a7db9648ce9c52243673617e92fb14199d56102d298ec22f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5152387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bae5c05c0136f49bf5df0e5f0942d3d65462f7dae85a873b79135ed26c2c773`

```dockerfile
```

-	Layers:
	-	`sha256:0d910917a81d4e5d214f83aac30bb102fa4c92fde03891ff0a54f7cd4fc3c9d9`  
		Last Modified: Tue, 30 Dec 2025 07:34:59 GMT  
		Size: 5.1 MB (5138072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35c292c8733303bccfb82795ba8dab85b870e86d42d6964ca70745dcf7d845c4`  
		Last Modified: Tue, 30 Dec 2025 07:35:00 GMT  
		Size: 14.3 KB (14315 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:811ea844dbd4f517dae7dc90fcc10d2a0bc3359a0bd84524fea86e851ca9c56f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221068229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c5a70d8b1c711c5e0bca19d43613483c2f92e561fe912562e24edf40b1aa0d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:01:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:01:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:01:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:01:29 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:01:29 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:01:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:01:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:01:43 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecafc31a8cbbadb7cb515bdf13e00436d9fd6739120638d8356a4a42e35d125f`  
		Last Modified: Tue, 13 Jan 2026 03:02:27 GMT  
		Size: 125.7 MB (125694449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8db0412ed356785d2f7acb0b7fcb005d1e5e9bef8fe2bae413e2d7bbe7504e`  
		Last Modified: Tue, 13 Jan 2026 03:02:08 GMT  
		Size: 68.5 MB (68488721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d2542f4fec3d527759247338f313166106bf8a11487029c662829d9bfa44bb`  
		Last Modified: Tue, 13 Jan 2026 03:02:15 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f95e3424885d2eaf39d41ff5a63cbce261e21d07ad5aa09ca5d6190a0a6897b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195d6da755275b8484376e9159c3130b85b58edcec8672d41a77d02f43b763d8`

```dockerfile
```

-	Layers:
	-	`sha256:718b326b109c55aca4aa87decd0d7d20e48987fb20b93cdac99bf3cc2c24ed2d`  
		Last Modified: Tue, 13 Jan 2026 04:36:05 GMT  
		Size: 5.1 MB (5124864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b81d97084fdd539ca337747e459eecebbdabc5347e74577b87be6d44f77b9c41`  
		Last Modified: Tue, 13 Jan 2026 04:36:05 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json
