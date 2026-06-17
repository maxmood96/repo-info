## `clojure:temurin-26-lein-2.13.0-bullseye-slim`

```console
$ docker pull clojure@sha256:ee0ece924ab32317eed83f1cbfc893efae0b1091dc9baf19f81016d95d904577
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-lein-2.13.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4870c99d2700094d0d9c6206325a1310c897c27cf8140805d06e23510add96ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.9 MB (144931349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf05efa49ac292256cdb589385597cb5f74b940960d4241a54e859450fdd2c3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Tue, 16 Jun 2026 23:38:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:38:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:38:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:38:39 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:38:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:38:39 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:39:50 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:39:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:39:50 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:39:52 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:39:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:39:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:39:52 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:55534d9909ecd18467599b415fa2553c3106849154ae8a361a75f1a24f2a4364`  
		Last Modified: Wed, 10 Jun 2026 23:40:12 GMT  
		Size: 30.3 MB (30260255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8d4dc16ba4bf58eddfcd386a22d9c667432617694159ee4b8b867d99f880de`  
		Last Modified: Tue, 16 Jun 2026 23:40:10 GMT  
		Size: 94.5 MB (94524344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec844a4db343a68067517b523663f6eee010ab4481b559ee60e13adb0af4f61`  
		Last Modified: Tue, 16 Jun 2026 23:40:08 GMT  
		Size: 15.6 MB (15631135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a603d68d280a0317ea3ded9818cd13823f498914cb1bb6ea067b536f9e30b1`  
		Last Modified: Tue, 16 Jun 2026 23:40:08 GMT  
		Size: 4.5 MB (4515187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de111b90b1d6d4fe36ed03cb1c8ebf48912fb55c91b21108cd620979d576a3a`  
		Last Modified: Tue, 16 Jun 2026 23:40:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.13.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:46a729cb5b78f44c7d4f965cc39d91170cce14662be01d76dae9821ab8212786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3021392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507e6f2240fd04bb7d9b34ab354d1d5fbd3fcb03bf6e80769677a87608b63a10`

```dockerfile
```

-	Layers:
	-	`sha256:af552ea00879a11e2bf41a5d6b9108050e41ca7d2379226de3975d91b48c7923`  
		Last Modified: Tue, 16 Jun 2026 23:40:08 GMT  
		Size: 3.0 MB (3003627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b664d996038cdd03378706bc5db0b55c710d4ae8a4a2fd7998db79df55ffc94d`  
		Last Modified: Tue, 16 Jun 2026 23:40:08 GMT  
		Size: 17.8 KB (17765 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.13.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b68bc75ce2b9da8a73f1faf4dc725feb3331b175e34807251a2cfe657977d28e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142385954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de9ac25c0f3d937d9fa5475e95613cdbd27fbcf4b778dd092d8083eb3e8f632`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Tue, 16 Jun 2026 23:38:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:38:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:38:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:38:32 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:38:32 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:38:32 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:39:39 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:39:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:39:39 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:39:40 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:39:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:39:41 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:39:41 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ca483a18241c226a06a4a4afd22dc5496062254c671fa595136458fb8fcd0107`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 28.7 MB (28746154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ab77bc564cbad0b9b085a742ab7269371745d150c7c2026b7f387b0abff1ac`  
		Last Modified: Tue, 16 Jun 2026 23:40:00 GMT  
		Size: 93.5 MB (93504327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400d50830701533276160f7414cdd33f2899337902ab796809444ff53f494ae9`  
		Last Modified: Tue, 16 Jun 2026 23:39:58 GMT  
		Size: 15.6 MB (15619873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a8dee120c5b2a6f1e28ebb4e4aa70791a31bcd93c096016527f268dc8217f2`  
		Last Modified: Tue, 16 Jun 2026 23:39:57 GMT  
		Size: 4.5 MB (4515170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a13bda2bf04c226bb32cba85ed53992d015a7e6b179b6eec47360afacba8001`  
		Last Modified: Tue, 16 Jun 2026 23:39:57 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.13.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:949ec51b7a049915913f53a3af98a8b8edcb66e44b584cc881afcc4a93fc293f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3021120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3022fb6b62c315ca25756830d7fdaeeb676161e4db5a58c4f5767f800bffbfec`

```dockerfile
```

-	Layers:
	-	`sha256:bb3a961fb15ebf97908ea6440b27953e775ba01812997f4ff0f94472b8b6b2b2`  
		Last Modified: Tue, 16 Jun 2026 23:39:57 GMT  
		Size: 3.0 MB (3003233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c9928e115d07df11498ddaed99d822332934fd75edefcc63bdd91b9f770b39b`  
		Last Modified: Tue, 16 Jun 2026 23:39:57 GMT  
		Size: 17.9 KB (17887 bytes)  
		MIME: application/vnd.in-toto+json
