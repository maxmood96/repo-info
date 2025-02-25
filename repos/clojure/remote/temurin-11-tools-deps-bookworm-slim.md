## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:3c7dc2ed31bcef14a4329a752372f9252baf6a60920dde238215920dce2d3ca9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5f8d6c6fe77774fd1642b0c272fc4f465dab16089a1da60f4fa72f6a2e3abd9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243349301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7380c424ef6ba5ebb58eca0f3ba8fcf711dad943c7546a10d17a9f2d9c3ed56a`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60142f10a5604d4d6c4532056fe5f1ec19b6f118972b98028c0ebfba9f7c3c9f`  
		Last Modified: Tue, 25 Feb 2025 02:16:05 GMT  
		Size: 145.6 MB (145598925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffbf6c8d59020c0ab1a3bad975aca975b918f90bc1be1399b4d2890b9223edd`  
		Last Modified: Tue, 25 Feb 2025 02:16:04 GMT  
		Size: 69.5 MB (69530427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6d6d223edbafb45a9fc0aada54e6afa0388d5dff60368bb80d953125d307e3c`  
		Last Modified: Tue, 25 Feb 2025 02:16:03 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:692654187bd2aaea6cd9c710716ebf071ab43a00b320164874c746e6a911b5c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4947036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73bb7e731971bfab68cc9119c0f7e71a4500388d6680d255ce9764ba8260ac47`

```dockerfile
```

-	Layers:
	-	`sha256:9f3dadb327192bec0815595a57d3bce93d9623a1c5625b5424672b5c328b25e3`  
		Last Modified: Tue, 25 Feb 2025 02:16:03 GMT  
		Size: 4.9 MB (4932726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd1e47b07bbe4a87a72029c2261140feb966f457a9e4ec4018d906b2a4a67d32`  
		Last Modified: Tue, 25 Feb 2025 02:16:03 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8cda252d6b1e3e7927d05e2814efa4421a9155e9786040b48e0b6960f188912d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.8 MB (239813831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71db8bc5833817ca46231b7e1f60adcb265d6b717c9e02600274e4a594f7515f`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b2c27e4a83f192332670ed834f644604dddd9bcf00e2d36dc7bab0c39be3ee`  
		Last Modified: Tue, 25 Feb 2025 10:57:01 GMT  
		Size: 142.4 MB (142385384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e142b831706009ffb397535c50c1305b5a9f54eef19a4e8f186c6a66bba6b363`  
		Last Modified: Tue, 25 Feb 2025 11:00:17 GMT  
		Size: 69.4 MB (69379378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f15c166abbff8e2b7fcc8998ed5fcd48ce2324bdab50307e6bfccc490b32e7c4`  
		Last Modified: Tue, 25 Feb 2025 11:00:15 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:13bddde754bff980077d69618a1ea49da76eb8d6d589ec142693cf9119b6bf58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4953532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4db2ba4834dc5b7a6ddb45ab2190bfbf23da381abbd2038d79760bbf854f4d0`

```dockerfile
```

-	Layers:
	-	`sha256:985c413ad48cacb85ff3580f8d2c4be25323bafbfdf55eba18639be33cbd9020`  
		Last Modified: Tue, 25 Feb 2025 11:00:15 GMT  
		Size: 4.9 MB (4939105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eb76f19768bc74b9567717cac4a2e1d23c77ae2783d7e7637bd243f8447edcc`  
		Last Modified: Tue, 25 Feb 2025 11:00:15 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json
