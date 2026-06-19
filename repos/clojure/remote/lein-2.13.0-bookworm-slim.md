## `clojure:lein-2.13.0-bookworm-slim`

```console
$ docker pull clojure@sha256:a2471d02d1febb653c2ddd1b41f34c87ae22db04a4944a47f42d574396a98a0e
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

### `clojure:lein-2.13.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:29bcb052d7c5f62f313933fa13945441ea3cef62f7c1957fe1c8a6c4e96db901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143387066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8363e8217236ae7c26fc89d5773350e4668ead6feedf4bae9889bfbbc1c57ad9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:19:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:19:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:19:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:19:43 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:19:43 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:19:43 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:20:53 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:20:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:20:53 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:20:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:20:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:20:54 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:20:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0375fc655d98fa4fcdfe6965de036a6695082079c00d4f0a1529325be138984`  
		Last Modified: Fri, 19 Jun 2026 02:21:14 GMT  
		Size: 92.6 MB (92574566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2da111fc47b1f97cb9e8c05e099d76beb0a8ef1713047fe847abcb1f129dd20`  
		Last Modified: Fri, 19 Jun 2026 02:21:12 GMT  
		Size: 18.1 MB (18059255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d5cf4a4eef1816b9df1fd98ec07aeffc854abb117091d00606e2335b5edc49`  
		Last Modified: Fri, 19 Jun 2026 02:21:11 GMT  
		Size: 4.5 MB (4515191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1782ee8dbcf2028b1750f184a799824693de0ea24bcba2baa95949d14e51a114`  
		Last Modified: Fri, 19 Jun 2026 02:21:11 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fa312dea4f372ac32197ddf0ab6f774db9c2ed4770b3bfefa146c835b6046132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2718821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3205aa12c7d788ed0c8f9fd2a37213ff6dea9eaafe44afc96d5914eda8c7c51`

```dockerfile
```

-	Layers:
	-	`sha256:20fdc20350e3133c219336e8d7fdb0aafa6a849412c17077e411f72d788c4c7e`  
		Last Modified: Fri, 19 Jun 2026 02:21:11 GMT  
		Size: 2.7 MB (2700393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ff061127dcc0daea6e845ea40afa767eb6015327920e8be9f3d0d18f2394367`  
		Last Modified: Fri, 19 Jun 2026 02:21:11 GMT  
		Size: 18.4 KB (18428 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.13.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:84e3cf13421e13e2f444b600850b824b0237f7979d0fa1de13cb53503428c359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142074424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32f992be45ed3695b6b2a59a5e5c9ebc7194d84e0ce0dd56d6e8f9bedfd759a9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:20:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:20:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:20:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:20:06 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:20:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:20:06 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:21:13 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:21:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:21:13 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:21:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:21:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:21:15 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:21:15 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee3ff71742d4a68256bda0c72af24d4d7262496bacc2e018492e09598a3a054`  
		Last Modified: Fri, 19 Jun 2026 02:21:33 GMT  
		Size: 91.5 MB (91542237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d492de91b25f42c94b9d379317c10962aa4753f7d4e525b1a997b7cd00c57768`  
		Last Modified: Fri, 19 Jun 2026 02:21:32 GMT  
		Size: 17.9 MB (17894249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c1273e5ad3b12335cbe7ef5b0074bd4ee20d5a834df2990ae7a5ed92509249`  
		Last Modified: Fri, 19 Jun 2026 02:21:31 GMT  
		Size: 4.5 MB (4515201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cab1ad816f638ffb010c481e14da24909a40d0cc98ca8fabeb55a81eb8a49ed`  
		Last Modified: Fri, 19 Jun 2026 02:21:31 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e503e7562337ea477cca50d2edc6b31bdf529f3ab17be4ad337d8c184a36c7e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2718602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2a541f3ac9f7af8faeffcb983e44ef7899ebd2bf925194101d7a0caf1bf6398`

```dockerfile
```

-	Layers:
	-	`sha256:dfe1475c155fc6125b64277f77260813a4a9fefad3df18f696d9e222cf7ccf7f`  
		Last Modified: Fri, 19 Jun 2026 02:21:31 GMT  
		Size: 2.7 MB (2700029 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81eed4dea56fc398b47e3cf549c0c4258429a87278bac445ff56d8e0028a491a`  
		Last Modified: Fri, 19 Jun 2026 02:21:31 GMT  
		Size: 18.6 KB (18573 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.13.0-bookworm-slim` - linux; ppc64le

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

### `clojure:lein-2.13.0-bookworm-slim` - unknown; unknown

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

### `clojure:lein-2.13.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:1a064873de64d684d28bb1cb783f5b437fcc1bd23208fc7392fdbb360908edc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137554393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e9758472aee5ad2887a1fadeff9020a57b03e0111e8aed3e2ed8e4eb0ce33f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:21:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:21:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:21:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:21:00 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:21:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:21:00 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:22:04 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:22:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:22:04 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:22:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:22:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:22:06 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:22:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f24253f44b61e08a6eea6c9ac2c141af3fb831e29f77c9f2a38981b7fd8a04`  
		Last Modified: Fri, 19 Jun 2026 02:22:31 GMT  
		Size: 88.4 MB (88420366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5808db170a4ee8558a297389f748e353778c431f4ad8979d5b455ccc3ea01a84`  
		Last Modified: Fri, 19 Jun 2026 02:22:29 GMT  
		Size: 17.7 MB (17724879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea8e20097fadadf3e514382e6f55aaa6c14c37a278db382464ffb4e332a26ea`  
		Last Modified: Fri, 19 Jun 2026 02:22:28 GMT  
		Size: 4.5 MB (4515210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814c76f19988660f80831e88e128f3fee53a3821f8e1680e61570ae91dc3a56b`  
		Last Modified: Fri, 19 Jun 2026 02:22:28 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:47b138f1e1add193dfecd4ad51bf425d1302182038d8b2f90ad7ff94c9920f60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2695197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785920a3b8dcb8ca106bf0d8c22fe21fb37b40ebef5b18220f5cf2c74d15198a`

```dockerfile
```

-	Layers:
	-	`sha256:d4215094c8b1e5bbbb6dc42e6f3eda965749cc8e2db48186b31c193d347846c8`  
		Last Modified: Fri, 19 Jun 2026 02:22:28 GMT  
		Size: 2.7 MB (2676769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f703d8c32b8c2c4fbf4ff70f4ec8a62ef08fa185c541d90d4f4154a4d7394e4`  
		Last Modified: Fri, 19 Jun 2026 02:22:28 GMT  
		Size: 18.4 KB (18428 bytes)  
		MIME: application/vnd.in-toto+json
