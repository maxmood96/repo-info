## `clojure:temurin-21-lein-2.13.0-bookworm-slim`

```console
$ docker pull clojure@sha256:8ed6617b0c46a6f71cdc02859a85f3b0bd4b58a734f31a1b0f1ddf0479ad5942
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
$ docker pull clojure@sha256:46825afbde90ff27c0c89c2052a3b497d6f6ccbd3959d80b5958d6357e7f0cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.0 MB (208979542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c0d436b43de4722cf8a829e963a5519cbed470b48fb800ee9fb44f304a9bb74`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:36:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:36:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:36:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:36:07 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:36:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:36:07 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:37:13 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:37:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:37:13 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:37:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:37:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:37:15 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:37:15 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679a4e47c456238aae1b0b3d56f7c04ba54f6c664d3b9594ad88b20ecd27b215`  
		Last Modified: Tue, 16 Jun 2026 23:37:34 GMT  
		Size: 158.2 MB (158166904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3556b3a2aa651213e38e4fb2bbcf857cfd38aab7036656858a6117f494af17d`  
		Last Modified: Tue, 16 Jun 2026 23:37:32 GMT  
		Size: 18.1 MB (18059421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60091155f92f4c960e71ce54feb72dd4763be9440d7e573e2e9a306e4c54f681`  
		Last Modified: Tue, 16 Jun 2026 23:37:31 GMT  
		Size: 4.5 MB (4515162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bbe85684a978835b3f206e30def61f4761ef856a81eea112310ecb7031388d`  
		Last Modified: Tue, 16 Jun 2026 23:37:31 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a7dfc0621f6ba6b2a3b7d7678d11aee97a5759c4b6acac3452fdb8f428056b4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2751962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eccda645495b03ebdaa6769fbee65a119e38dd26dc37fe25a01208eed22888f7`

```dockerfile
```

-	Layers:
	-	`sha256:d7f319bafa4a8c52870202cdf574327b0b3b4a997ffb8b396dd4194f97935022`  
		Last Modified: Tue, 16 Jun 2026 23:37:31 GMT  
		Size: 2.7 MB (2734189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac4c336148f64bac15e22c4716781a19c2c81f0a6551736bca31f26e721aaaf4`  
		Last Modified: Tue, 16 Jun 2026 23:37:31 GMT  
		Size: 17.8 KB (17773 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.13.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:67ef4b5e7cff7897dffe65d0c2b6b3ef3a55ddcdebaa3de1af52f919917925f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.0 MB (206993150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e5275a6167782e6e01bb75d139fedb191b33c75a89556ee93a830d00b86f32`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:35:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:35:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:35:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:35:09 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:35:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:35:09 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:36:16 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:36:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:36:16 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:36:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:36:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:36:18 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:36:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28aaeb27c0871f36d6516414467216803cca9c1a8d1d61e7b07d395b7857a5d`  
		Last Modified: Tue, 16 Jun 2026 23:36:39 GMT  
		Size: 156.5 MB (156461324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a061e8cc02209b7986bb84a02320c6b7e9880add8b2f1ecdbb14cf28d789471`  
		Last Modified: Tue, 16 Jun 2026 23:36:35 GMT  
		Size: 17.9 MB (17893884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7793f8ffa48612b800c0171f9c7c91d2571dd491d11cf06311da84d46d0a1689`  
		Last Modified: Tue, 16 Jun 2026 23:36:35 GMT  
		Size: 4.5 MB (4515205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9376b5687678604542b8d7a02ca9794c77b7410fe994252af6a3ba8ecf19b02f`  
		Last Modified: Tue, 16 Jun 2026 23:36:34 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.13.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4349592ac083c2db4e466c298b9283753a99c8ed93f632878f9accd518f9f95e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2751698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83faf765afbce2212b2f2e9cb898a8ba2b6b35fb2298cd6ef8ae72cacf357fdb`

```dockerfile
```

-	Layers:
	-	`sha256:f608f5de581d2464421e12d33496e19decf163cef1680b060192481a0b99e65d`  
		Last Modified: Tue, 16 Jun 2026 23:36:34 GMT  
		Size: 2.7 MB (2733804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75c45d853fbd3d4b54d6c8270c90d4cc4afa47f04736dc62b4a61c3d3f6b99e1`  
		Last Modified: Tue, 16 Jun 2026 23:36:34 GMT  
		Size: 17.9 KB (17894 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.13.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:61f0883b2a8a082904ed440d31a4ff83fa634c86002ee9e0a394c1f3aff5df77
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
$ docker pull clojure@sha256:689a62ebebddf222e22eb532301e681d8fcabb25eeb2cd702e214538f66d13cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2753839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a1481fc4d5c55c3aa2c0294bd7b8ba821d1ff2449fc4aa48ed36c12ced2509`

```dockerfile
```

-	Layers:
	-	`sha256:d934b03fdfa76f0833cb7336c9574663d5f3adae97454843d697f707a8a8a0e3`  
		Last Modified: Tue, 16 Jun 2026 23:57:17 GMT  
		Size: 2.7 MB (2736022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa4db88748370129b9e27125566b9aae8c96f1183814bd9aadfdb3a9784f4e22`  
		Last Modified: Tue, 16 Jun 2026 23:57:17 GMT  
		Size: 17.8 KB (17817 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.13.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:cfeb8dff4fc67485bbe257c21abb7a32b1dd2753bbf375ae139c2ed6fb1de0ea
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
$ docker pull clojure@sha256:6dda0e38b6b65def6e01d40ec9c358adace60e1b6ef329ab6d0bf954885fdb5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2743776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a79e4f01f9bb0d6a8ec548f1540c39bb39f94324a75eced121e941a30db220e2`

```dockerfile
```

-	Layers:
	-	`sha256:1bd7a048a91fa07561256954bc8ee2109b5f79170bc0fb7f9c937d84cfdc7010`  
		Last Modified: Tue, 16 Jun 2026 23:38:24 GMT  
		Size: 2.7 MB (2726003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:521c5a9e8ebd672e7acb724648301955c19dcd2a39ac537ad73fc57348fa0137`  
		Last Modified: Tue, 16 Jun 2026 23:38:24 GMT  
		Size: 17.8 KB (17773 bytes)  
		MIME: application/vnd.in-toto+json
