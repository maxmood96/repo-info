## `clojure:temurin-21-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:0e1cfde18cde8a52beb69150f7d5af257597c271bea3c0251f1ac237c02fd1ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:88778e48e21e9bf2186a7de4b85446883ec611cb34d12c067cd507df56313eab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.6 MB (208573839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96928279f02aed95a8f981806ff59f1fcc0d2371dfdae434f23f30cd01e94897`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Tue, 16 Jun 2026 23:36:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:36:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:36:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:36:12 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:36:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:36:12 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:37:21 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:37:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:37:21 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:37:23 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:37:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:37:23 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:37:23 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:55534d9909ecd18467599b415fa2553c3106849154ae8a361a75f1a24f2a4364`  
		Last Modified: Wed, 10 Jun 2026 23:40:12 GMT  
		Size: 30.3 MB (30260255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe928327b9bdebaaaa617d1638463f189670ce6c8b974ed3f9f330be72d1ee0`  
		Last Modified: Tue, 16 Jun 2026 23:37:44 GMT  
		Size: 158.2 MB (158166957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec667b3b6d32ca35e1ba5c08bcdf4ef87e5e3941f03d6ddc815ca2366e2e9e8`  
		Last Modified: Tue, 16 Jun 2026 23:37:41 GMT  
		Size: 15.6 MB (15631016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8c3c420f9684d0d69dff8aa97f3be0767acff26319b771bc9d81ce2c82d153`  
		Last Modified: Tue, 16 Jun 2026 23:37:41 GMT  
		Size: 4.5 MB (4515180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bca2d5fe375f1284c69dc9fdd94bb47927784d7fa8187882bba66429dc6a118`  
		Last Modified: Tue, 16 Jun 2026 23:37:40 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:362ede7fa6be6cac316232cb0eaf579608dce48dbe7a103ec6a062de5c19077a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3058361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b1d262d8bcf0b9180c8a1dfb729490fc9279628c12ba25993d6d976c2adee3e`

```dockerfile
```

-	Layers:
	-	`sha256:fd3e5683eaa3ecf7ab1b4de104ba8b9f6ebd6a4d718bd2ee83254edfadc935c2`  
		Last Modified: Tue, 16 Jun 2026 23:37:40 GMT  
		Size: 3.0 MB (3040588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac87a9eb2e8849a2087dffe1ab07e8883a9f9a60136da38f2f727e4a47fb01ce`  
		Last Modified: Tue, 16 Jun 2026 23:37:40 GMT  
		Size: 17.8 KB (17773 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ad53f380eba74800084aedf7e810c79b06fe836e7432fd252053e030105c9793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.3 MB (205342718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127ca45d07c77ea57f2229ccb41dfeee562b0187aa00435f521a0cf6d01c6a7f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Tue, 16 Jun 2026 23:35:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:35:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:35:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:35:57 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:35:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:35:57 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:37:04 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:37:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:37:04 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:37:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:37:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:37:06 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:37:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ca483a18241c226a06a4a4afd22dc5496062254c671fa595136458fb8fcd0107`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 28.7 MB (28746154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed860c84f19ac38d5140912d3aff9f0d870d865e2e9e881b39c94b7daeeab040`  
		Last Modified: Tue, 16 Jun 2026 23:37:28 GMT  
		Size: 156.5 MB (156461282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8fd0bfc4805b221d646001c50c667082344f2c79a37b1c2a3de6c87c7c76b35`  
		Last Modified: Tue, 16 Jun 2026 23:37:24 GMT  
		Size: 15.6 MB (15619643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2c4889b566c135d437ccbfa666a6101c627ec8fad6056755bb78fc937cc26d`  
		Last Modified: Tue, 16 Jun 2026 23:37:24 GMT  
		Size: 4.5 MB (4515208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ebd8616b8e38061c21ffe3b917ad3cc0f4c64266f3e51ec770f23fc955f05b`  
		Last Modified: Tue, 16 Jun 2026 23:37:23 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f75fb6c8f22984803cb43946440071fb2bef799cbea90ad6b706c37632c301a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3058090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b09af92a8d8e5da2c0e346d470ebb71e8a96b1202fddb94ad0b7d0d7937d890`

```dockerfile
```

-	Layers:
	-	`sha256:6e73639868bc2bff380ca70d14513886c086659caf273e68e78962ddf39feefb`  
		Last Modified: Tue, 16 Jun 2026 23:37:23 GMT  
		Size: 3.0 MB (3040197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e3a4451cd729b31fa75ae0475e779f2e5eee946d5ae4650bd515476828c815a`  
		Last Modified: Tue, 16 Jun 2026 23:37:23 GMT  
		Size: 17.9 KB (17893 bytes)  
		MIME: application/vnd.in-toto+json
