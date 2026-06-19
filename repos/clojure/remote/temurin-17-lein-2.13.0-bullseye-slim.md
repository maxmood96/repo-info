## `clojure:temurin-17-lein-2.13.0-bullseye-slim`

```console
$ docker pull clojure@sha256:bd324282dc8bbd30c34a411d9f1c586842f02ab7bcb809712aca0c9dee965b79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-2.13.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6b33841a05576b12f346846c01474a4d5ec5f39f9c22fd08cd38fef23f313aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196312648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ec1f0f403f4b42f67e5bd77a13d973cd0f7e082381cdfc7b1662ecb81cee33`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:16:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:16:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:16:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:16:58 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:16:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:16:58 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:18:04 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:18:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:18:04 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:18:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:18:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:18:05 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:18:05 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:55534d9909ecd18467599b415fa2553c3106849154ae8a361a75f1a24f2a4364`  
		Last Modified: Wed, 10 Jun 2026 23:40:12 GMT  
		Size: 30.3 MB (30260255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a59815f07d195238fbc5411c5f60523304f0417ce5c51ede29a900843da00b6`  
		Last Modified: Fri, 19 Jun 2026 02:18:22 GMT  
		Size: 145.9 MB (145905454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d229dddc60eb36f64486fe228a352cef76d59014e652447a190d70aa496fba4f`  
		Last Modified: Fri, 19 Jun 2026 02:18:21 GMT  
		Size: 15.6 MB (15631325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526afbcf566457130c1fb373a2a0dbb72ee003584241c3c8791ff8c3320f33e9`  
		Last Modified: Fri, 19 Jun 2026 02:18:21 GMT  
		Size: 4.5 MB (4515184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f116b93b4457440df00c7a2c4b6a933a8f447a8bc3ad3f5bd2ddb3af4a4b3242`  
		Last Modified: Fri, 19 Jun 2026 02:18:20 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:76e911d04e714a800bf4245d61a7c9523f0fccb7d826c63bece17b24c4cff715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3056509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b03a9198a0e65d8425f17d48db61c6621fb6678a8de61b05017e661e4ee437`

```dockerfile
```

-	Layers:
	-	`sha256:23a05b584cc071d9c42b92e1a8952371711922961cfbd11fd606f66cefa532c1`  
		Last Modified: Fri, 19 Jun 2026 02:18:20 GMT  
		Size: 3.0 MB (3038736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc1eea5e617523f7866ee7a128824745cf0037f99386950543de13b511deea66`  
		Last Modified: Fri, 19 Jun 2026 02:18:20 GMT  
		Size: 17.8 KB (17773 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.13.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b3e9d9ec05ff3b43dd44864cfc2eb5d5cc7db3d5f1318c4ea0b707b93ca9b88d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193605669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:057adb0e2799157777dafaf6c381e69bac43d36a3c064704bf5bae5dd6638047`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Fri, 19 Jun 2026 02:17:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:17:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:17:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:17:13 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:17:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:17:13 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:18:19 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:18:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:18:19 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:18:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:18:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:18:21 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:18:21 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ca483a18241c226a06a4a4afd22dc5496062254c671fa595136458fb8fcd0107`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 28.7 MB (28746154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8515476967c6b932b5a0a84e83a442bd286dc34e9917832f981285cc11f748f8`  
		Last Modified: Fri, 19 Jun 2026 02:18:40 GMT  
		Size: 144.7 MB (144724310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3d53500e41ad695072d2c8a6fa1c745d6eb68d8d1a52fedf7d93b56ee6c725`  
		Last Modified: Fri, 19 Jun 2026 02:18:37 GMT  
		Size: 15.6 MB (15619553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85acb20cd9574ca2e3d52e4d7cec57274f0af6ada37e979811cc4bfea743401`  
		Last Modified: Fri, 19 Jun 2026 02:18:37 GMT  
		Size: 4.5 MB (4515223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf0c93ded684185b39efd1ec6ff21d4c2b61dfe798dfbb15ea26d1eab4022b5`  
		Last Modified: Fri, 19 Jun 2026 02:18:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fbb23255dc94543210041c9112cda57681aca5b73de6a2cfa2843d92e2ab9536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3056239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c75df53892e8d9456714cc535a032ad4cd9b08b2fa0aa45498a04fbc0bcb7a0`

```dockerfile
```

-	Layers:
	-	`sha256:68acbe3e6f2c17ef8492ffbe3abf891725f61008426d909ce41e2df2a258fca7`  
		Last Modified: Fri, 19 Jun 2026 02:18:37 GMT  
		Size: 3.0 MB (3038345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8665cd533d1a1820e9eaeeeb82e110a45b831acf9dd79a2830d9613fd83b7dda`  
		Last Modified: Fri, 19 Jun 2026 02:18:36 GMT  
		Size: 17.9 KB (17894 bytes)  
		MIME: application/vnd.in-toto+json
