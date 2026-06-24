## `clojure:temurin-25-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:823c5aadddc6d8bbb0f531a86e0aeb77c85ba6debbbfaa1c3ef206f01402a468
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-25-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:86c598550a1776aa5e5d8022f54d0dd34f584d03ce966eec39b139b00e4d2bab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143386986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b639a43e416021d444e89ad64625088111205ec82a7ad71d86ec516180dbc6ef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:20:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:20:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:20:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:20:38 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:20:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:20:38 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:21:47 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:21:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:21:47 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:21:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:21:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:21:48 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:21:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1aa161488d1cd5cc78227d51e88232cfa58a9e86da2f585dcd44d2586e0a0cd`  
		Last Modified: Wed, 24 Jun 2026 02:22:08 GMT  
		Size: 92.6 MB (92574577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56003547b9696f24ce5a12c06f4d1434861a95019199f22bb36a616cafee1308`  
		Last Modified: Wed, 24 Jun 2026 02:22:06 GMT  
		Size: 18.1 MB (18059151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326cc7aedda6200385e172a024fe1f38be82804f01d5d2dd2a4d82cf86806cfa`  
		Last Modified: Wed, 24 Jun 2026 02:22:05 GMT  
		Size: 4.5 MB (4515190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e4e396d0bd9195579e5079a5d41d37403bb6671173db1cfed95ca8d7cc504a`  
		Last Modified: Wed, 24 Jun 2026 02:22:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4db27269a2d5f04dd3b8c45e187d78e92688cf027cb96b8358e507dfffd25e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2718821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f5f97dc06b78554e47b9db0de112786d3bb9013a0c68b87947cf807d9f8ff4`

```dockerfile
```

-	Layers:
	-	`sha256:2d7128de8241d0a17e54ccfb6f5c5a7d9fce33fa787c9a7653afab0086978889`  
		Last Modified: Wed, 24 Jun 2026 02:22:05 GMT  
		Size: 2.7 MB (2700393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b65088a3ccce70b6920d5a25ba36ad6201ef23b093b4e5e3e63272220c3076e6`  
		Last Modified: Wed, 24 Jun 2026 02:22:04 GMT  
		Size: 18.4 KB (18428 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5a2e0e1ecc930b96b75d0e65680d4960ceb8c56cd3b4fa9df616b8201c2def19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142074535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a8cd02eef33575489364c6c4ba808eea628ccea1c1a391322f0ca809776db5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:27:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:27:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:27:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:27:08 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:27:08 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:27:08 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:28:17 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:28:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:28:17 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:28:19 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:28:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:28:19 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:28:19 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db5afc03736b31104e588033cea3438f59c73d2780c15c98314a6028d9fada7`  
		Last Modified: Wed, 24 Jun 2026 02:28:39 GMT  
		Size: 91.5 MB (91542269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625c85cd59cedcff28c0ceead7375180d83797d3a2c5ca0539ad7070707cf72e`  
		Last Modified: Wed, 24 Jun 2026 02:28:37 GMT  
		Size: 17.9 MB (17894225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc19e8b98b7e9eb81acdf6aabfaf30e5922612d0317e463d0570a56aaec54bdd`  
		Last Modified: Wed, 24 Jun 2026 02:28:36 GMT  
		Size: 4.5 MB (4515194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7cc0c6b70fcb7108ad40bd79cc037d53e9963674bbc239cf6d0fe29dc449dc`  
		Last Modified: Wed, 24 Jun 2026 02:28:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:49593fb5d10248cedb5031627e021c14ffe2b4a47f1b128bf4b20dfeb2e1ed2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2718602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e664e1b04c008cf9f1348cad32777a30c56b07ff756fd36baab88ecc0d3c0e`

```dockerfile
```

-	Layers:
	-	`sha256:ad4a5e35669e43c0f03033ef2a331397083883fc71766fd9058b4aa1ebc6db1d`  
		Last Modified: Wed, 24 Jun 2026 02:28:36 GMT  
		Size: 2.7 MB (2700029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18c5fea4e57f1f9f053094f8e7189410a0e884464c86e216fe95b428eaeac18d`  
		Last Modified: Wed, 24 Jun 2026 02:28:36 GMT  
		Size: 18.6 KB (18573 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:7c2f394f25b28b0839d25ba97f1c97011486d197f070fd1036f990683f8505c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146775616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c5150f7938eb18bb743ed0044513960e4ab0f3e4416fa724f55698a16e13aa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Wed, 17 Jun 2026 00:03:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jun 2026 00:03:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 17 Jun 2026 00:03:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jun 2026 00:03:19 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 17 Jun 2026 00:03:19 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 17 Jun 2026 00:03:20 GMT
WORKDIR /tmp
# Wed, 17 Jun 2026 00:05:41 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 17 Jun 2026 00:05:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 17 Jun 2026 00:05:41 GMT
ENV LEIN_ROOT=1
# Wed, 17 Jun 2026 00:05:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 17 Jun 2026 00:05:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 17 Jun 2026 00:05:48 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 17 Jun 2026 00:05:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ceb0eb5280b5d711b09e7b6fc60f0539124c87d3b78261261a7696dc0d1b48`  
		Last Modified: Wed, 17 Jun 2026 00:06:20 GMT  
		Size: 91.9 MB (91914038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288824b737e140672c5359ac26cdf40f7402af84806ca2f2ca85693c1a65540d`  
		Last Modified: Wed, 17 Jun 2026 00:06:18 GMT  
		Size: 18.3 MB (18263976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d8b18ccb620978340ca0e9523359cdcd9b22288db9e8520225def4084cfb72`  
		Last Modified: Wed, 17 Jun 2026 00:06:18 GMT  
		Size: 4.5 MB (4515231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c1d33dd77c9c8b63e94da87f5cf3fad3f10c885655fc1a1dbfa1a05ae9eda7`  
		Last Modified: Wed, 17 Jun 2026 00:06:17 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cbfbd0287618b458e90dd696449ecfc4e4a4330b82d70c4f857775f6cd935f1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2704034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf522356267d39fd39985057e5606e8dcb88e17cbfde0d5a121b1c3ba4ab3e66`

```dockerfile
```

-	Layers:
	-	`sha256:94f8bb7adc95d26a6fa9752c99f2e96aff6207ffb4f4afcea94a9672ac4c630c`  
		Last Modified: Fri, 19 Jun 2026 02:54:16 GMT  
		Size: 2.7 MB (2685550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17643a4b33e0724cf6dfefcd10105e645f57e15c13b55b9eba6ae1e707687a46`  
		Last Modified: Fri, 19 Jun 2026 02:54:15 GMT  
		Size: 18.5 KB (18484 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:c9b3b6fa96eb94ed7d1e0364bf90323d025124c25cbf8892c26b19892164d502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137554583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fb450c0f4fee8a611b837ea59e1f30a87b1c91a6b65c6e46bf10531660025d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:17:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:17:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:17:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:17:28 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 04:17:28 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 04:17:28 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:18:34 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 04:18:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 04:18:34 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 04:18:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 04:18:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 04:18:36 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 04:18:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e9aeeda7513dde59469463716e9e14f36210d6570c3cad5e5440b32d941733cd`  
		Last Modified: Wed, 24 Jun 2026 00:27:21 GMT  
		Size: 26.9 MB (26893585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64512e22f1cf746a8cfa05946899c57c3e320cd67aa253aab1b07c92bdf674a2`  
		Last Modified: Wed, 24 Jun 2026 04:19:00 GMT  
		Size: 88.4 MB (88420330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f36d994ca01f7264c56fd3376d4433d7b9851cbb291fc1de2b98b6bd4c30305`  
		Last Modified: Wed, 24 Jun 2026 04:18:59 GMT  
		Size: 17.7 MB (17725044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817e9d857db004392b07bd19973a7decf2a1bac709f7719e8a2973b4a36d3c0c`  
		Last Modified: Wed, 24 Jun 2026 04:18:58 GMT  
		Size: 4.5 MB (4515195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f6135c69daac357e68d18fa1d89eba4872e9b12b6968bd57ae3b842a3e30d5`  
		Last Modified: Wed, 24 Jun 2026 04:18:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:aecb211b7dd687b37376767af7a828b5dd7cd150fe0aae33f32448ecf3cc9c55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2695197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1aeab9e2eba07a9679bb33f818a6335addc48f0d36e537152a1efbcd7a62e09`

```dockerfile
```

-	Layers:
	-	`sha256:b90290ee9cc125cc3899feab092093d425160aa101267f2a33756d1362bd27b1`  
		Last Modified: Wed, 24 Jun 2026 04:18:58 GMT  
		Size: 2.7 MB (2676769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d61efeb1053fcc6b258bb81e221bbf765abfc338093c5d227ee4f06773844199`  
		Last Modified: Wed, 24 Jun 2026 04:18:58 GMT  
		Size: 18.4 KB (18428 bytes)  
		MIME: application/vnd.in-toto+json
