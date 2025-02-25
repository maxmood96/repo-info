## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:ea9e3ead16e52e35d1e3cbe2b30c79b1befbbf9cf113b0ecc595a1b06970e3ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e4fd1566e0728117ed2e862d693f41578e447675337089a98b2668c6c9701d16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.7 MB (177650798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68759ec3ec48908e51dacb35524e8330588851b49f12a4a1d1372b0adc8f061f`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4ff5a3a54264ee833e4a09583363bbe779e881f15449fe4f4a6a662885dd37fb`  
		Last Modified: Tue, 25 Feb 2025 01:29:47 GMT  
		Size: 53.7 MB (53741401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6442588b0a71939b2f330c324569a215c5c58a1421aeaa1aa06132ce3f5710f9`  
		Last Modified: Tue, 25 Feb 2025 02:15:11 GMT  
		Size: 54.7 MB (54721234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968441723d588c6285f75117aeb0d665bd95dde45f0f232ed04229c177ec9818`  
		Last Modified: Tue, 25 Feb 2025 02:15:11 GMT  
		Size: 69.2 MB (69187518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80191ddab46fbed061a61de8dfa9b665ba4ee29b1b14cf1f04bd2a45c222c118`  
		Last Modified: Tue, 25 Feb 2025 02:15:10 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e66b70561497548a673091d4f3afe53070985568e22582824d23b4d53751927b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7340402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394df6665dc5202e90266175539ce064df8b7fad512cb109f8c4159e62837c61`

```dockerfile
```

-	Layers:
	-	`sha256:61c27094e1f572d657f943b5c15cedf7b0f6468ad31e0c244f1eaeac44253c1b`  
		Last Modified: Tue, 25 Feb 2025 02:15:10 GMT  
		Size: 7.3 MB (7326165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00e799e8aaf171c9b12dfa1e242783208e590973d7ba8714b2565ef4e3999459`  
		Last Modified: Tue, 25 Feb 2025 02:15:10 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b93d61ec7b12e77ff02525e63274f2f6f650cfa561993b9c0e4b53f4cb49fe3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175381466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7bacda93679c9475c815fa23459d8270dc1875211f0691041908c36ce1b587`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7e1cabb756c27ddad3e1de86c2aaf2bca04f012bff531cd99d37f98896026ca4`  
		Last Modified: Tue, 25 Feb 2025 01:31:16 GMT  
		Size: 52.2 MB (52248644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7d1dd57497a7dd0bcaca93f8e2580e1b8bf8bc345c23617c590ac204111a74`  
		Last Modified: Tue, 25 Feb 2025 10:51:30 GMT  
		Size: 53.8 MB (53822770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5a9191106baa618fffbf36abf0732e3ab1999448be91bb151116a6578b8d60`  
		Last Modified: Tue, 25 Feb 2025 10:54:30 GMT  
		Size: 69.3 MB (69309408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109655a87614ccd3630228a17f4ea40ed9e35bf1509b635e3a71fd60afbdf1f1`  
		Last Modified: Tue, 25 Feb 2025 10:54:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:8446f7a03eea6f5f6d1d89a98b1c6717c153ed12e765f5bbba815edfe7f1c892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7346317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31be530b659beea6d30497d0e800f5c29f7a2a0e7d6cd800f118afa69447b8e7`

```dockerfile
```

-	Layers:
	-	`sha256:88ce3a5856ce2b046b275bc00cf0ff599f5f39be6f756dbfcb2fe3d48edb4929`  
		Last Modified: Tue, 25 Feb 2025 10:54:28 GMT  
		Size: 7.3 MB (7331962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6351459093db6c214fe4a73a917a0deca0525027cdb3e15f7f2082a10f73111c`  
		Last Modified: Tue, 25 Feb 2025 10:54:27 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json
