## `clojure:temurin-21-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:a8c9b9798d7e8ba9ba82d1b7dfe0d790aef725f9e2b1812411cc6cb1d5908438
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5a61670f71746398cd114be54895ea738d50a9c9b6f50a2ace31dca859c43d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244528521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5822bd70f96910c17520906f580d552a6467ec353ddb6369336eca017bcff93`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:19:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:19:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:19:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:19:59 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:19:59 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:20:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:20:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:20:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:20:13 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:20:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:55534d9909ecd18467599b415fa2553c3106849154ae8a361a75f1a24f2a4364`  
		Last Modified: Wed, 10 Jun 2026 23:40:12 GMT  
		Size: 30.3 MB (30260255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d9d3f8415db9cefd6920d25ac4841b76ccbdde939a8113eaaf86d5b75e93f9`  
		Last Modified: Thu, 11 Jun 2026 01:20:37 GMT  
		Size: 158.2 MB (158166906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b89c08cc04c5e128ddef3d8afe4f3578f9cb69a7c883e8f9e3705ad8e1790cb`  
		Last Modified: Thu, 11 Jun 2026 01:20:35 GMT  
		Size: 56.1 MB (56100317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d12247268463ddbfc6bf65ecf573a0ca414cf3530db23d89e68237c4b2c064`  
		Last Modified: Thu, 11 Jun 2026 01:20:33 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab262daf2fb27b6a548eb942a76df76b0a8b02f259dc38de177ab0fdc3ac7bc`  
		Last Modified: Thu, 11 Jun 2026 01:20:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5a973b5726f038bbe6e7fc92865bbb3f44748c972f20fdd92040c3ba834c5cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5335691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c1ee1cadf714b145df74af3edef13f30a9347982f6823c265c1b075ee4caa8`

```dockerfile
```

-	Layers:
	-	`sha256:e3e75e014c01c17188f8329ad1532835d7f399a07e70d72cc089a0b85a07858a`  
		Last Modified: Thu, 11 Jun 2026 01:20:33 GMT  
		Size: 5.3 MB (5319701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ab9aedaf80f96690771be88d516e6c56891f591bba7d36dc5bb575ed86920bf`  
		Last Modified: Thu, 11 Jun 2026 01:20:32 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f7c7b6c1c43c63c088517a7215758cb98270d97a8912827af6d1db2bd9313f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.5 MB (241476030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a421f017d1cefb17a3c5bcf442252c60f8735281585e66a2d498cde8a14b6c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:24:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:24:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:24:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:24:20 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:24:20 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:24:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:24:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:24:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:24:32 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:24:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ca483a18241c226a06a4a4afd22dc5496062254c671fa595136458fb8fcd0107`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 28.7 MB (28746154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ceaee37505e5ec00bae1d397aef8f1db69939c20295665111767733c477286`  
		Last Modified: Thu, 11 Jun 2026 01:25:01 GMT  
		Size: 156.5 MB (156461324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10325eed431f676190d61016fb672dc1d19caf644523b3acb24b701f735d9675`  
		Last Modified: Thu, 11 Jun 2026 01:24:56 GMT  
		Size: 56.3 MB (56267513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c069ab923fb0af38f1e8019960e8a9095f0448163a2036f15a10e3593b209a8`  
		Last Modified: Thu, 11 Jun 2026 01:24:52 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdff3ec35a8a7c086b2d1563c1cd3b0beea45f59a5d2f863bcb45641ae37ef0`  
		Last Modified: Thu, 11 Jun 2026 01:24:52 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f60d4188e01b59d4ea7360314b51816380605308a194189a5766ee9b3a06e104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5341541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:178113699ce9fda20b5ee3a53486c0ff9ef3e0fb9c43eea5f7396e1d480eda62`

```dockerfile
```

-	Layers:
	-	`sha256:9a19714e232008e7a682ed6cde44a97cfbe8d1375ce46c0333dcf7736892a7dc`  
		Last Modified: Thu, 11 Jun 2026 01:24:52 GMT  
		Size: 5.3 MB (5325433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93910aeb025eb1d5bfcd507095a955d6d1a113ad9a48c3b710f7c8f0eddf6d80`  
		Last Modified: Thu, 11 Jun 2026 01:24:52 GMT  
		Size: 16.1 KB (16108 bytes)  
		MIME: application/vnd.in-toto+json
