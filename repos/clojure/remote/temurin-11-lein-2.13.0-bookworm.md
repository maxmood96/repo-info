## `clojure:temurin-11-lein-2.13.0-bookworm`

```console
$ docker pull clojure@sha256:78ebc360c92cdfd1bcb961e2faa343dfbffcd0c5e60ee7ea11cda618d4bfcf41
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

### `clojure:temurin-11-lein-2.13.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:b079fc717d76d42788796bf01d8184d5e2509641e4e84bd95ab2394907aafc0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.0 MB (219011292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85be1f46dc2b2586fc52a02542b09e1966afd1ca29977c6f4febf93f9f9b1031`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:32:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:32:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:32:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:32:55 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:32:55 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:32:55 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:34:05 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:34:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:34:05 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:34:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:34:06 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1128a14d8bac411acb06d4549e5e9319c4ce895a030d3875d2ccb346a1f8a9ea`  
		Last Modified: Tue, 16 Jun 2026 23:34:27 GMT  
		Size: 145.9 MB (145886244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163270cfb3dcb80d5522938e820f214e5e9524bb7db93fddec2a03883ecaef62`  
		Last Modified: Tue, 16 Jun 2026 23:34:24 GMT  
		Size: 20.1 MB (20107795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd83a8011c754e61f9d35431b8045cf1d045bffadef4a1974a614c2a97ba2c0`  
		Last Modified: Tue, 16 Jun 2026 23:34:23 GMT  
		Size: 4.5 MB (4515179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.13.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d1212052e1d93d3530e267066189d19e3ad5474fd024ab6204ee8e56ce35f5e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4319282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb4cecc8cdf3e20d7a7ae14df72b02fe53e698791af1bd829c9a3a65660f87e0`

```dockerfile
```

-	Layers:
	-	`sha256:4b9bafc5eac3465df83235cd873368324931b5a0472762152443fc1ad9cc454c`  
		Last Modified: Tue, 16 Jun 2026 23:34:23 GMT  
		Size: 4.3 MB (4303534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f245741ed283f4485ceeee699f03f450f358e6716bd697b781f7589fdbdfb930`  
		Last Modified: Tue, 16 Jun 2026 23:34:23 GMT  
		Size: 15.7 KB (15748 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.13.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d8041778af3eeaf0b876a33bd68afcf73ae68904e8dd0eda16179837a1191450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215426626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda02ba4145a89515b3401727458701f501498d5d238711f2a9d9602be87f068`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:32:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:32:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:32:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:32:38 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:32:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:32:38 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:33:53 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:33:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:33:53 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:33:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:33:55 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc5f63b8a72ba79866102d5463eaa71fea652c33fe87e3fb158536d6bb745c9`  
		Last Modified: Tue, 16 Jun 2026 23:34:16 GMT  
		Size: 142.6 MB (142582230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c7c88df9f449a8c27991bb83207b838e06efd1893b12beac4872910801cb30`  
		Last Modified: Tue, 16 Jun 2026 23:34:13 GMT  
		Size: 19.9 MB (19940150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eddf2246771c1ad3b639e3fed7fd78ffe63967dd72965fc29ebbca2bf5a7e0c9`  
		Last Modified: Tue, 16 Jun 2026 23:34:13 GMT  
		Size: 4.5 MB (4515198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.13.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f823d89222b605b4967e906718d33cd320afccdb0b7f9a9d91b89192206e589c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4319636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3425ac9d8e9d41cb7563c40399139bced27be59d7b35b27609f85e35f7447ed`

```dockerfile
```

-	Layers:
	-	`sha256:1b7504254475082b9798674178a84a42bf46e6df18635bdaa007db9b3a31c5f9`  
		Last Modified: Tue, 16 Jun 2026 23:34:13 GMT  
		Size: 4.3 MB (4303767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bda320381200eebfc61a156ee503f3ff5b446cded38c96ec281523b413b4e37`  
		Last Modified: Tue, 16 Jun 2026 23:34:12 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.13.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:7a9afbe14696d6ee54c2596c917f8a3e327b52183fc15f2640ade0604ed4f142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.3 MB (210304140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73fbcdb2c8232c355bd00a09b892749b97ae9283e079d4a31a1d64752d881b65`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:30:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:30:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:30:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:30:21 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:30:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:30:22 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:33:50 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:33:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:33:50 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:33:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:33:53 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:88b94a58fac236a778527a3293ccd0ff4d309bff0bf314017ea5af603908fa2e`  
		Last Modified: Thu, 11 Jun 2026 00:21:34 GMT  
		Size: 52.3 MB (52346670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c827bc71dfc3d68de295bd88b4657cbd537998b965359abd8f7b294129d180`  
		Last Modified: Tue, 16 Jun 2026 23:34:33 GMT  
		Size: 133.1 MB (133110215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ade1c5b394a15c6471f98094398d3fcb508880620a44f76b1dd531dd0e6afb`  
		Last Modified: Tue, 16 Jun 2026 23:34:31 GMT  
		Size: 20.3 MB (20332006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531927db1465973f66892c05f8e86e6c077b539fb16aea545761f91c1161043c`  
		Last Modified: Tue, 16 Jun 2026 23:34:30 GMT  
		Size: 4.5 MB (4515217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.13.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c549082e2b256cb14a2137a4b37f9b89f9a4b65fefd467d7c934e82f36016f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4320572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7ed15831187e4728a9cd22aa7ea1827edecbe650929da828cda0b1e5efc1b6`

```dockerfile
```

-	Layers:
	-	`sha256:4eeb776e10d793e66f86dc139bee3a310792c8bd5d77b6daea63cbfe6228eab3`  
		Last Modified: Tue, 16 Jun 2026 23:34:30 GMT  
		Size: 4.3 MB (4304780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ddd1307b2ed6f9bd7fe9a61bf4ca5fb7ddd4f5cec3f123601fc8933841f6e3d`  
		Last Modified: Tue, 16 Jun 2026 23:34:30 GMT  
		Size: 15.8 KB (15792 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.13.0-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:6cceec102f4858f82804abb352e5be9025057b7942db51b5aada68b48fd01f36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.1 MB (198098649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f1a7ed96bf5f263fadb978b92b798fb3f31091d8cea5d2af84d1f5b4736692`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:30:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:30:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:30:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:30:17 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:30:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:30:17 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:31:42 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:31:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:31:42 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:31:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:31:44 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b041a55a85cc0e47dd570746852cc1b0fee042f3a03eb250b9f896ac4aa74a3d`  
		Last Modified: Wed, 10 Jun 2026 23:41:01 GMT  
		Size: 47.2 MB (47161500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faac26a16c3512d100392fa084d87083a807fb6ccdcbaeac23013af9a52a1d55`  
		Last Modified: Tue, 16 Jun 2026 23:32:10 GMT  
		Size: 126.7 MB (126651720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebb8082cbd77ec3ee8a6a7e6e8bd4599ddd859f14dc77e3ce52e0a081066a9f`  
		Last Modified: Tue, 16 Jun 2026 23:32:07 GMT  
		Size: 19.8 MB (19770179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dae906a63c7ba901a61bc74977bb79d1f432dfc26bacea4e19e378c1bbc2b35`  
		Last Modified: Tue, 16 Jun 2026 23:32:07 GMT  
		Size: 4.5 MB (4515218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.13.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e900aea1f4205568767d91bfbe0c7921c3a3c9364daa7e2fac67ee9740ad8dd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4311099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18f965db1f60aed1f666b4906a60caf5ba45e9b3eeb436db7329e135532dbcdc`

```dockerfile
```

-	Layers:
	-	`sha256:d3d06dad42e67d7f9b3551727a76c19bed710245ee0fbe5e9c066e2ce9f93d1f`  
		Last Modified: Tue, 16 Jun 2026 23:32:06 GMT  
		Size: 4.3 MB (4295352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0e8ce8adfaf233cea6b9a9c335a48bf61c19ff3c0cc85c7a79bd0e2d85d2f88`  
		Last Modified: Tue, 16 Jun 2026 23:32:06 GMT  
		Size: 15.7 KB (15747 bytes)  
		MIME: application/vnd.in-toto+json
