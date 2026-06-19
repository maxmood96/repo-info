## `clojure:temurin-8-tools-deps-1.12.5.1654-bullseye-slim`

```console
$ docker pull clojure@sha256:e464643c060c094da19def62634afa3b463f8fb5529b11d2e5498ad80875d76f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.5.1654-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:18a46a8aa1879892e4aff54b4493a0d2c0a8215152ec35df79b2c19c1c598483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141559991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1378180932a528a2ec7045901db8e29ba1d15313eb7a74cfadb9bfd46c4762b`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:14:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:14:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:14:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:14:57 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:14:58 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:15:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:15:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:15:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:55534d9909ecd18467599b415fa2553c3106849154ae8a361a75f1a24f2a4364`  
		Last Modified: Wed, 10 Jun 2026 23:40:12 GMT  
		Size: 30.3 MB (30260255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0e1eae80c753dc49b1d509f044d218e47f0e3ccdf5c03c52d7a2158983bccb`  
		Last Modified: Fri, 19 Jun 2026 02:15:28 GMT  
		Size: 55.2 MB (55198724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89ddd0d0ca47e3938329502d1afb5e97cd81b42e8fa6fc01649ca42c24fb08a`  
		Last Modified: Fri, 19 Jun 2026 02:15:28 GMT  
		Size: 56.1 MB (56100368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7833cf834a0fb868b7bd2798620d913ef678f68665efccac4e37e89b7518619d`  
		Last Modified: Fri, 19 Jun 2026 02:15:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.5.1654-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5c8f25b26881ab8aefbe27b8ebbc6cb3b221a1db5aec5ff353fc2e43bf11b136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5454233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e73d6e58ebac484b958c1e86e8070c53b7c44a48aff36c06789f3a6b01f2f65`

```dockerfile
```

-	Layers:
	-	`sha256:10a4bc62a0538fdfb46e158c022ce19c78dbb4aee4a5d21bf0672e66e90f6053`  
		Last Modified: Fri, 19 Jun 2026 02:15:26 GMT  
		Size: 5.4 MB (5439833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3346915fdd1a693b5539f4f2372a932b972bdd9139ebaf1605a6d656547225c4`  
		Last Modified: Fri, 19 Jun 2026 02:15:26 GMT  
		Size: 14.4 KB (14400 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.5.1654-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3f1e6762a1047ea2e0e68499513b06d755879864e3631eb0c9e165ac34034661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.3 MB (139287141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec43d568b6ae57b8b2f38485c7a126da649017e5b53f7979102bb06eda27ccb`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:15:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:15:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:15:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:15:09 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:15:09 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:15:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:15:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:15:21 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ca483a18241c226a06a4a4afd22dc5496062254c671fa595136458fb8fcd0107`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 28.7 MB (28746154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbbaee480d35c8fe9896a3ff45be697448c01f12396994a8794ef9dfe4883b2`  
		Last Modified: Fri, 19 Jun 2026 02:15:38 GMT  
		Size: 54.3 MB (54272924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff61c225926433f57aee8e1b57e1ccb9279738516e205d3097de8820bdcaeec2`  
		Last Modified: Fri, 19 Jun 2026 02:15:37 GMT  
		Size: 56.3 MB (56267419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e6be4c8ac3c7a7534dbaca8c7f4b45ee06e53dd389cd8de297f4a4d7e54372`  
		Last Modified: Fri, 19 Jun 2026 02:15:35 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.5.1654-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:12961305ad61a0bae45c875a32ce1d633144a7512315a92e4506ff0c7b762a59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5460785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83f4f6cd6448e9d5f06155e1e9017e6157d71a0b9439e83219134d63723ab6ae`

```dockerfile
```

-	Layers:
	-	`sha256:37c5b0ec05fb259dc69f7fb2227a4623fbd28dcfb5c8b3ecaf4a7d0198d58407`  
		Last Modified: Fri, 19 Jun 2026 02:15:35 GMT  
		Size: 5.4 MB (5446265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a144cd90e4cc399fad50ece7f257eeb8077cedcddb954a5fc4b7a9ecc5b7842c`  
		Last Modified: Fri, 19 Jun 2026 02:15:35 GMT  
		Size: 14.5 KB (14520 bytes)  
		MIME: application/vnd.in-toto+json
