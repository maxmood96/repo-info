## `clojure:temurin-26-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:4ca991c98c641d9a193044de692a32c6a1183ab22df52122c2f5a5f99af5b20b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6e618d1f18832dbce7918b1774e1dae0f6babf362bd0e33ce273fdf94e3a4eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.9 MB (144931446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ab06e40c6572229031f5d3adfaac5c28a89027e1a353d9059b469d9dcff89d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:21:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:21:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:21:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:21:26 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:21:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:21:26 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:22:35 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:22:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:22:35 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:22:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:22:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:22:37 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:22:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:55534d9909ecd18467599b415fa2553c3106849154ae8a361a75f1a24f2a4364`  
		Last Modified: Wed, 10 Jun 2026 23:40:12 GMT  
		Size: 30.3 MB (30260255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ed819ccc936ea5749ddc2c27285c02b64770db441e71c96de822fa91027854`  
		Last Modified: Fri, 19 Jun 2026 02:22:55 GMT  
		Size: 94.5 MB (94524360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de41a1aa97c95c977b3f89f2c692ce3636b5eb53397d4c4a149d8af7afea9891`  
		Last Modified: Fri, 19 Jun 2026 02:22:53 GMT  
		Size: 15.6 MB (15631191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f188af97f22013644e8e6ebbe05034a8b5eea50498bfce0cfb64712ce4b7cf31`  
		Last Modified: Fri, 19 Jun 2026 02:22:53 GMT  
		Size: 4.5 MB (4515211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa099661a40f416ffb8a6bb2f07e93864185037b92af827f272fff4e98ebb4fe`  
		Last Modified: Fri, 19 Jun 2026 02:22:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b311ca8a31cdb7699f4650b490eaccb8d7ebd24d60e7ac7c41041c38ed4c97f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3021393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69af3e3693ce227b1ae9e6d47b45011219cffefa7d4844fcac6bca643d829040`

```dockerfile
```

-	Layers:
	-	`sha256:0be3e75ad5362285175debfb6867ab669f99bcf3be215e169ab25904c4bf0d8c`  
		Last Modified: Fri, 19 Jun 2026 02:22:52 GMT  
		Size: 3.0 MB (3003627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91dbafd47c0c5982d1118a0549309b95439982928802af1a443fc93bdbb460b7`  
		Last Modified: Fri, 19 Jun 2026 02:22:52 GMT  
		Size: 17.8 KB (17766 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e3970b8154ef179721c1ca7190385ade6842be8fcfafcad8b3a82d40010cedfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142386024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0dad283adeb3d5f5507676f4b8acf03466e4ff7febc30cab634a68e9b1689c6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:21:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:21:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:21:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:21:42 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:21:42 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:21:42 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:22:51 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:22:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:22:51 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:22:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:22:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:22:53 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:22:53 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ca483a18241c226a06a4a4afd22dc5496062254c671fa595136458fb8fcd0107`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 28.7 MB (28746154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5caecff9440be95453d9c8edfd58d26bd418b17ebb1ce5465a3eb19128de0f46`  
		Last Modified: Fri, 19 Jun 2026 02:23:12 GMT  
		Size: 93.5 MB (93504337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13019ce82b1ea5a26c848c66a8738580fbc28404d1be1eb5b819eea7e83a7c59`  
		Last Modified: Fri, 19 Jun 2026 02:23:10 GMT  
		Size: 15.6 MB (15619882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06529c6097e5a1a11b30b4f720c56cefaece9e1fa66450b4ba6365e0749b0f71`  
		Last Modified: Fri, 19 Jun 2026 02:23:10 GMT  
		Size: 4.5 MB (4515221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6dca5c3b615e1be46e01ff3dd2256057cdaa5e5e49c57388ec4fb727901b7be`  
		Last Modified: Fri, 19 Jun 2026 02:23:10 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7d351a670b52ec12df26c397712653e53a0a6a0a05bc174b7dea140c27914536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3021120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84024a4dd178d6f8fb586d368ecb87e8b5aa395a55b844b1655613c6b838feda`

```dockerfile
```

-	Layers:
	-	`sha256:2fff0e5c07a279c29d7d3649046420df58ae3ac8444d5783f93f4576225a0ec1`  
		Last Modified: Fri, 19 Jun 2026 02:23:10 GMT  
		Size: 3.0 MB (3003233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b0d4aa1eaf13ac6905bcf806f7afffdb8fd73a555c24ca85dee272ad9411274`  
		Last Modified: Fri, 19 Jun 2026 02:23:09 GMT  
		Size: 17.9 KB (17887 bytes)  
		MIME: application/vnd.in-toto+json
