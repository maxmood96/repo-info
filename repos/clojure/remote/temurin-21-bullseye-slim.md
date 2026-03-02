## `clojure:temurin-21-bullseye-slim`

```console
$ docker pull clojure@sha256:67254c2d01e93eb2f37f96def5a194cc2f7426cc86c84715f1aa0c7b9c1dc4de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:600fa7f5dc50d682c83a3b30f4b610faff53482a54e41a0d44c4f16a7ab41349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.3 MB (247293121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b5d0ba10d82965c05c1ed03c3eca206e3501319df198cf83c57ca52327c5dce`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1771804800'
# Mon, 02 Mar 2026 19:47:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:47:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:47:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:47:36 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:47:36 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:47:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:47:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:47:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:47:49 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:47:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:34f0642d22440b5813561cd4375937013bfb556bec8ff3b0e208699b786282a7`  
		Last Modified: Tue, 24 Feb 2026 18:43:06 GMT  
		Size: 30.3 MB (30258379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02dea5ad8a31d019b8d1e212d2470466294a050a6ece2eaa5440083f3d84670`  
		Last Modified: Mon, 02 Mar 2026 19:48:14 GMT  
		Size: 157.9 MB (157857102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22836b92c13878e6877527f15301d099923877ea8d943d4eabe17d434cb793f`  
		Last Modified: Mon, 02 Mar 2026 19:48:10 GMT  
		Size: 59.2 MB (59176599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b0544fa18f5e04e4fb5621b9c4be1b166a57c46370d168d7f197f5e01fc181`  
		Last Modified: Mon, 02 Mar 2026 19:48:07 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26058608bd945b79ec30c44ec165c05a2b584d99874912a68725af441ccdb7b2`  
		Last Modified: Mon, 02 Mar 2026 19:48:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c21b8b007f02a6887d729a8c6656b9331de35714828585c92e61f347c1b6b611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5339364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a75d02d2f1c97ff7be00baa68ece1f230c304d0e895f403bb82bf35c750c5f3d`

```dockerfile
```

-	Layers:
	-	`sha256:ee17235ed42dfd2a5a091887d70d865f8f7923e436c21b5b5f7059c52c4942ac`  
		Last Modified: Mon, 02 Mar 2026 19:48:08 GMT  
		Size: 5.3 MB (5323529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2574572080e02cc564cb2e7704930c3e2ffcc88b850f927c22c948ad63ed5beb`  
		Last Modified: Mon, 02 Mar 2026 19:48:07 GMT  
		Size: 15.8 KB (15835 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d3d7a9d6aab700431b5dbb6416669087cbca422e2cb9be9164b6285794043027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244195990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f70304ad2c293c44fea17a5e32fa9a6c39b55b3fea323fe6ba7d5d2a1f2f8ee2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1771804800'
# Mon, 02 Mar 2026 19:47:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:47:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:47:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:47:31 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:47:31 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:47:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:47:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:47:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:47:44 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:47:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:018c0693c4a2532e5636d6115333db6d882da8f33f1f40cb3e88dbe62da21aac`  
		Last Modified: Tue, 24 Feb 2026 18:42:36 GMT  
		Size: 28.7 MB (28744470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6bb01c9ca0b6f9b43cc91f6d74b824755c0758fc45d3958a89fa3a47f3c3b7`  
		Last Modified: Mon, 02 Mar 2026 19:48:07 GMT  
		Size: 156.1 MB (156133072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dadadb336ba9540a26a7a326c79aa30f7c6882b4cf55b1869d25fcc177ffe6f5`  
		Last Modified: Mon, 02 Mar 2026 19:48:06 GMT  
		Size: 59.3 MB (59317406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f50ac170d477c3fd2a4812276dceb68ca71b9221c2662881e6f1580f7679614`  
		Last Modified: Mon, 02 Mar 2026 19:48:03 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b94e97f7ea8dc4a06950329ef27b52b59077efaa5618e3d3abe9f0cfb031d05`  
		Last Modified: Mon, 02 Mar 2026 19:48:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:60033a7ae2128e10a12a989f009f79feb8c5243bd117e6f143a511c9ae48c3b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5345215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b406437f5530799dd3d63b74e19f3d65f6e8e4be9d9231e5d7b40de40ce533b`

```dockerfile
```

-	Layers:
	-	`sha256:79612079ec00a37584b2dc6ca6b6dce2a105ec8e991034031899fd28f54910b2`  
		Last Modified: Mon, 02 Mar 2026 19:48:03 GMT  
		Size: 5.3 MB (5329261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1187717b358fddcf42b823ca5a2e6ff41e10f40a856cc60a16b1cea8f8bd4e79`  
		Last Modified: Mon, 02 Mar 2026 19:48:03 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json
