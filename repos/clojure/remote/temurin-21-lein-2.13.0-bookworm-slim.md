## `clojure:temurin-21-lein-2.13.0-bookworm-slim`

```console
$ docker pull clojure@sha256:df0c1a5f8d09f5988a417e720331594338f42caaee01cd7ed3094222978e22f5
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

### `clojure:temurin-21-lein-2.13.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d2a22ba57ff7a9c893cb9fb55a4e757125d5c5a792e8b88939081868cdcd26cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.0 MB (208979909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c8fd8fb615d0e4cad79aac359e3727a41bbfd02f710272201619f147ee2127c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:18:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:18:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:18:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:18:16 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:18:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:18:16 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:19:21 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:19:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:19:21 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:19:23 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:19:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:19:23 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:19:23 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575dd9a7abf5c9b4a1ae5dc22d4cb33ddaf5630b0b98b4ae6b4378553627a15e`  
		Last Modified: Fri, 19 Jun 2026 02:19:44 GMT  
		Size: 158.2 MB (158166941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39226eb3d9658fc85e933661783f983361d6e6056ad7278d6cd4cf7982e2c8ea`  
		Last Modified: Fri, 19 Jun 2026 02:19:41 GMT  
		Size: 18.1 MB (18059690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbe05e58f6e9313a58a55812057ccecdfea3ccdc1baca6d77001503962ea976`  
		Last Modified: Fri, 19 Jun 2026 02:19:40 GMT  
		Size: 4.5 MB (4515224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8953a55577d6d4f8a24284208a7e3fef4a7e19334095c921ac9e7b98fa9ac4fc`  
		Last Modified: Fri, 19 Jun 2026 02:19:40 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6ae36eb40e052908fc308fe13e4c85cc5cc68dbcdac60bc1cc1fc29053b3f9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2751962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c123191f4ef70517d23d317fbc624e7e6ea67472a5745ebf6f8475c04868a8a4`

```dockerfile
```

-	Layers:
	-	`sha256:e1970f86d24738bfb4c8cdfcb40a0e12bc9f46a9a352f8b5f3f2753728eee029`  
		Last Modified: Fri, 19 Jun 2026 02:19:40 GMT  
		Size: 2.7 MB (2734189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:678db619e696765fd238ddccfb3eeadaa3237bdc9d62540bec747491dcadd7ab`  
		Last Modified: Fri, 19 Jun 2026 02:19:40 GMT  
		Size: 17.8 KB (17773 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.13.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c402a4feaa76586cde6dc8c0446586ae9fb49ee2a6dc6de4902248af26bf6cf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.0 MB (206993425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acd4ca01d2f92e1b3410dd4096f96bc1af7779e9edf4cd8ca698aa9a9949adaf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:18:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:18:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:18:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:18:24 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:18:24 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:18:24 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:19:32 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:19:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:19:32 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:19:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:19:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:19:33 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:19:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26517a5e3ab121dde40422cbc7f082d8ec3a8b837d3f62fdbb6ff39ca40aa409`  
		Last Modified: Fri, 19 Jun 2026 02:19:55 GMT  
		Size: 156.5 MB (156461275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910fcfdd1d260c6db22dffd6f53bd931032cc3c2eb9e1b2a3d5e008976161ba4`  
		Last Modified: Fri, 19 Jun 2026 02:19:51 GMT  
		Size: 17.9 MB (17894247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a3749ff7986eafe8852a96df988be24b0b748168ff32d041e981e2cc002c7c`  
		Last Modified: Fri, 19 Jun 2026 02:19:51 GMT  
		Size: 4.5 MB (4515167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74649bc6ba19e8e79655b80a57d6ad94caf89363245285887fd442c9a1df1143`  
		Last Modified: Fri, 19 Jun 2026 02:19:51 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e53e5181a3cf5103bb22b83645574697d193cb80e80695c4648ac40a1a71b131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2751697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:977d8701fe517bc8332fbe7656c90035cdfcfe294586ef93845682746c26ef62`

```dockerfile
```

-	Layers:
	-	`sha256:4be20bb37d2466efb2adb9d372256f66784c4be02689d231ecd6eead25d29cf6`  
		Last Modified: Fri, 19 Jun 2026 02:19:51 GMT  
		Size: 2.7 MB (2733804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1f6713c155c1b898815c23b84d61381ea4fbf975f6780b4d645e71ccd84a9ab`  
		Last Modified: Fri, 19 Jun 2026 02:19:51 GMT  
		Size: 17.9 KB (17893 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.13.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:cc40384948213e5add04f7c8814fccc529ef85e33a9af945d3932103657d5bf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.2 MB (213204365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d914bdb4526f5f00456c941a3c9981a52aa4bf7eeae19254e32b7e2d3e17a2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:54:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:54:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:54:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:54:22 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:54:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:54:22 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:56:39 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:56:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:56:39 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:56:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:56:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:56:42 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:56:42 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e41ba91bd198088eadb03a3c25545d904cf2490691f50cad346a585a8741f3`  
		Last Modified: Tue, 16 Jun 2026 23:57:21 GMT  
		Size: 158.3 MB (158343240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22cda46999dab13e1a86484f55ebe6af329cb34c9d7b8669ecf478b6c76d5c6`  
		Last Modified: Tue, 16 Jun 2026 23:57:18 GMT  
		Size: 18.3 MB (18263539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aadb112f8f8bbceda17d6125b9f026b97eaf83ad53233c90c09661e640ddb2db`  
		Last Modified: Tue, 16 Jun 2026 23:57:17 GMT  
		Size: 4.5 MB (4515215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb7f388087fef03a3df8f2a52d1ed5ead2ac342aa1350e11bd0ec4a9cac182a`  
		Last Modified: Tue, 16 Jun 2026 23:57:17 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c7a2744f9559426a65c2364db1b0fd99b3b315071392b0a8faca92200ae6238c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2753839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb31b88820f36d4758439049987b10516e2609cc59a8917b8c0b5f168be96106`

```dockerfile
```

-	Layers:
	-	`sha256:d4c74d7bfe145ee33a6b3e6f38b00c02a3ba4bf5720b02aab39db23462c39993`  
		Last Modified: Fri, 19 Jun 2026 02:49:16 GMT  
		Size: 2.7 MB (2736022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:757a99733dc215ae7a80f9eeb236bd31c576c9ab2ef37e54051923472412b3b0`  
		Last Modified: Fri, 19 Jun 2026 02:49:15 GMT  
		Size: 17.8 KB (17817 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.13.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:05e4335be6ad5852ab89ebe281ed814b3a2ab76637e0b317e91638ce91cf63b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.5 MB (196522035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b130de8fcd9ab28d48057e37d423455c39e4d225b5820ec0746c3b1f56fed15c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:36:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:36:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:36:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:36:47 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:36:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:36:47 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:37:55 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:37:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:37:55 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:37:57 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:37:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:37:57 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:37:57 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7c23db7ea29bb7aa16742bb5f7f37601f5b9a0301d0417f6608ab147d6a0ad`  
		Last Modified: Tue, 16 Jun 2026 23:38:27 GMT  
		Size: 147.4 MB (147388339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb3db630d839f97775a716f31889bc52272e066e0537211457e72a89edf153a`  
		Last Modified: Tue, 16 Jun 2026 23:38:24 GMT  
		Size: 17.7 MB (17724540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7b1a0614b96c2a7d8752d82b8bed305df18e67ee10dea10d2fae7dbc954540`  
		Last Modified: Tue, 16 Jun 2026 23:38:24 GMT  
		Size: 4.5 MB (4515218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734e16d53a32ce404484f7beb1b3c50698c3de50a3442890bf03e9e0b815fbdc`  
		Last Modified: Tue, 16 Jun 2026 23:38:24 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:074af611094d02bc67535cbd2d1633ddcc4eadf104336b6a731b181d52b13664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2743776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86318025acb96382d7bdf192d49fcd73a596dbbdd6b67156624e9f6187bd4556`

```dockerfile
```

-	Layers:
	-	`sha256:c58f5311b89ce536b6dec2bdf86ea41f325fead388bacd4665cb3b64e846da29`  
		Last Modified: Fri, 19 Jun 2026 02:19:34 GMT  
		Size: 2.7 MB (2726003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58d0796e6a2270b1eb2f12700ef9fa92e4678b5d042e8382c98ab0b8de596ff1`  
		Last Modified: Fri, 19 Jun 2026 02:19:34 GMT  
		Size: 17.8 KB (17773 bytes)  
		MIME: application/vnd.in-toto+json
