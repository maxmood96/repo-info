## `clojure:tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:958d27f116e5f362624cb0cb37a84dd622c3a650adfeacee019f0e9f1f60e90c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:152f076a830ea4ce11fa98ed6a842fb9533cfc27712c1583e5368bb6eec9df40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178936193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d54a8d3ad5485a8fc0de5bc90f34c4ac53c542721e7a683f7183713d99f256bd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:20:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:20:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:20:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:20:19 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:20:19 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:20:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:20:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:20:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:20:31 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:20:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:55534d9909ecd18467599b415fa2553c3106849154ae8a361a75f1a24f2a4364`  
		Last Modified: Wed, 10 Jun 2026 23:40:12 GMT  
		Size: 30.3 MB (30260255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7fba96a6915ccb871e13d10f486666e06266279c3c4ee8ef11571a51f70ff0`  
		Last Modified: Fri, 19 Jun 2026 02:20:51 GMT  
		Size: 92.6 MB (92574566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecbfe0698993cc43d9da215342f6b49494296b7511b82d090ac3ad1eecb091e`  
		Last Modified: Fri, 19 Jun 2026 02:20:51 GMT  
		Size: 56.1 MB (56100331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af63105a5a3d6333491ea90f6d9c14439ace8eca8c2203741598db28b9e1854d`  
		Last Modified: Fri, 19 Jun 2026 02:20:47 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053114e752ee109e02afdf21515e35a7f1485b2234b6375d71b890d3cb591733`  
		Last Modified: Fri, 19 Jun 2026 02:20:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2d3c6db33780b506cd726e599b8730c34723a5d9db80cdc5a1d43572076d78b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5304242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97e226e2dbca15509eb1f71100583ad3e6a110cf744ab5272558c02595af885`

```dockerfile
```

-	Layers:
	-	`sha256:83a46bac3d75b238d60f02b19a9fa567546e0aa409ff31eb038c3a113c66e73a`  
		Last Modified: Fri, 19 Jun 2026 02:20:48 GMT  
		Size: 5.3 MB (5287563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50bc0ca995b81876c8c973d015009ceb86854d4451f3ed7f1d4a27c09eaeea03`  
		Last Modified: Fri, 19 Jun 2026 02:20:47 GMT  
		Size: 16.7 KB (16679 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b6e2070cf9964d39d65711759479f35efdf487578a633f9206d98ff5aee7d492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.6 MB (176556607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76913b5b46af02474563378631265e545a67c9efd598b683d5b611d5e093ba70`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:20:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:20:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:20:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:20:51 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:20:51 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:21:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:21:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:21:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:21:04 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:21:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ca483a18241c226a06a4a4afd22dc5496062254c671fa595136458fb8fcd0107`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 28.7 MB (28746154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd6831257ebca43ed98b0bc5312b3224ffc537289690c095bc6bfa31ab52d14`  
		Last Modified: Fri, 19 Jun 2026 02:21:24 GMT  
		Size: 91.5 MB (91542251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4803e8e15a18595f28a8915981ef225d97dedcae49655a2cf32e26aa876dc54a`  
		Last Modified: Fri, 19 Jun 2026 02:21:23 GMT  
		Size: 56.3 MB (56267162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1f18065518ad3c82a987adcec26061fa42efff44784375e1c818f023c7805d`  
		Last Modified: Fri, 19 Jun 2026 02:21:21 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8dc4efabb9e042c2c99e2b6a55232c7bf8a21ec847d8cc9a4ed4896f53546fc`  
		Last Modified: Fri, 19 Jun 2026 02:21:21 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8ed75ec1df995d5e3ca171242395161f315ffea777c72314939053b631547e27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5310136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9941d519815dcd8518006dc9cf51a372e4f197f548a3a6eb46e7834a1c23c1`

```dockerfile
```

-	Layers:
	-	`sha256:e8e0efb3ee60a7f91fd727acfbfd44aafcc8bcbe14f716831772226d757accb0`  
		Last Modified: Fri, 19 Jun 2026 02:21:21 GMT  
		Size: 5.3 MB (5293316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46fcbe7487496950b7858086a7d44a28bf3bf41eb4876a60572ef2556562d672`  
		Last Modified: Fri, 19 Jun 2026 02:21:21 GMT  
		Size: 16.8 KB (16820 bytes)  
		MIME: application/vnd.in-toto+json
