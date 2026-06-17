## `clojure:temurin-26-lein-2.13.0-trixie`

```console
$ docker pull clojure@sha256:313d8bfa93736a444d4ccfba5ccc3a12e44e8ffab64e1e078acf8364f1d22791
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

### `clojure:temurin-26-lein-2.13.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:6d0f874133157d27da5be18a777865ec33def01dc201cbd1481f07c6cb67a42d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.2 MB (167237331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca37ad12a6a680a6dfe4d7d4c44ffff2c2f547fe065dcd238940db531941c0a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:38:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:38:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:38:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:38:59 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:38:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:38:59 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:40:12 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:40:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:40:12 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:40:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:40:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:40:14 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:40:14 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d049c5d087028c9806e548b0d46b310c802bf74e8fc530d41d72ef0d489f41b`  
		Last Modified: Tue, 16 Jun 2026 23:40:33 GMT  
		Size: 94.5 MB (94524332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a5221c1ebff83a9ebc39bdbeac21f72a927ad30c74b23a0631fb396b375e76`  
		Last Modified: Tue, 16 Jun 2026 23:40:31 GMT  
		Size: 18.9 MB (18880269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df3e49696a4666084818921be76ae67f9e8edbd0049e12fcc84940afce842f7`  
		Last Modified: Tue, 16 Jun 2026 23:40:31 GMT  
		Size: 4.5 MB (4515179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13234e72c29ca30d40ca79056d3c87796c952bae36420b3c295cfec729685587`  
		Last Modified: Tue, 16 Jun 2026 23:40:30 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.13.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:88e9a54d4e375e9af595479de50a5a1e7a17c0e32548bd7b26e136f0f0275321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a057c924a50635573aa39afac00815abf5552b0261d834bcdf79763ded2476`

```dockerfile
```

-	Layers:
	-	`sha256:516c34548f24bfa2c42b7bb92623742cdf849d5ed3388ad4a0d7e008ec7ed646`  
		Last Modified: Tue, 16 Jun 2026 23:40:30 GMT  
		Size: 3.8 MB (3782711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c72d2b5aeeed036f2b7ff377a6b01ee7f4aa1cb2b1977412acfd0e3ebb41b73`  
		Last Modified: Tue, 16 Jun 2026 23:40:30 GMT  
		Size: 17.7 KB (17710 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.13.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:25789c3d3600405b05cd262de248c80c750d50564e510fbea3e748b3613b4607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.5 MB (166537784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffdbc024aedee16f3840b5ec9e602353622df85c5ecbbc5860d4b3b761639d8c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:38:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:38:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:38:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:38:38 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:38:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:38:38 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:39:54 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:39:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:39:54 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:39:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:39:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:39:55 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:39:55 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02723b48d3de066cb3ed8d3969fb86dca1aa96b54b5ebaaf25b2145a8520c5a6`  
		Last Modified: Tue, 16 Jun 2026 23:40:14 GMT  
		Size: 93.5 MB (93504350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a91e06905aaca876c9c5948dd738f6bb800ffc9041ac1b5f1c89629596db05`  
		Last Modified: Tue, 16 Jun 2026 23:40:12 GMT  
		Size: 18.8 MB (18839674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b397f729e828e2c1e0f6201fd0669142497910a6da9fac22ca3397f2df1d5c03`  
		Last Modified: Tue, 16 Jun 2026 23:40:12 GMT  
		Size: 4.5 MB (4515161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743edd666f8ceac8e42258f3ff32069dab131eade7a5203942ade71e2490bc0e`  
		Last Modified: Tue, 16 Jun 2026 23:40:12 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.13.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:099dc3ee264a5f87df097627038440df2eba8aa5bfd723a51716b49cfacf4da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3800780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a73c5093ff242534c90731c5a3506a18d4c089a3fd5e76f4a85d7c3166d0b8`

```dockerfile
```

-	Layers:
	-	`sha256:25209609254e14ac714cb32d6c1cc38d0f4b07b3f666634d9377b18111786b22`  
		Last Modified: Tue, 16 Jun 2026 23:40:12 GMT  
		Size: 3.8 MB (3782948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79ad75552cc074bf04eb41fe23bf3cb867a71d30b5fac9b826548465b11040f5`  
		Last Modified: Tue, 16 Jun 2026 23:40:11 GMT  
		Size: 17.8 KB (17832 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.13.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:f6d264359044c354ba9313ec06b2b3a7f00c7c1d521fe9a1307094a8fb02036a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.5 MB (170492207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e234cdc7623c1bd4ae74205325c115fbdaed8085d21f4205ec5bb3d0260a93fc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Wed, 17 Jun 2026 00:14:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jun 2026 00:14:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 17 Jun 2026 00:14:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jun 2026 00:14:41 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 17 Jun 2026 00:14:41 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 17 Jun 2026 00:14:42 GMT
WORKDIR /tmp
# Wed, 17 Jun 2026 00:17:40 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 17 Jun 2026 00:17:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 17 Jun 2026 00:17:40 GMT
ENV LEIN_ROOT=1
# Wed, 17 Jun 2026 00:17:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 17 Jun 2026 00:17:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 17 Jun 2026 00:17:44 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 17 Jun 2026 00:17:44 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328775c3b052bb498a48836eab308724b02180a01e1a5397b2235df60a8765bf`  
		Last Modified: Wed, 17 Jun 2026 00:18:19 GMT  
		Size: 93.9 MB (93902081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c0856248fb467b82985129297c21544fb2328e6f1fb68d6913e6e87ca96b7c`  
		Last Modified: Wed, 17 Jun 2026 00:18:17 GMT  
		Size: 18.9 MB (18936572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064532ee2c899459b97ebc1eb2b2b07fc800dcc2b2ce9e37a19f17ef71edc802`  
		Last Modified: Wed, 17 Jun 2026 00:18:16 GMT  
		Size: 4.5 MB (4515185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c2f5619a2374ba7c1d16953d8042d97597f1b93902129f3555e8ebb80ad576`  
		Last Modified: Wed, 17 Jun 2026 00:18:16 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.13.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d19f43691b6a4402b8131f77d3946ca0cf1edc3477c0d2b561319466cc54de23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3785401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f02d5a87e1c88da0bad0d14265f8a4131dc17dc05458fab71f9b33938dd87c8f`

```dockerfile
```

-	Layers:
	-	`sha256:8b7aaaf62e11d2612b819c31c71535c193a43b37aee681586196bb2a28896423`  
		Last Modified: Wed, 17 Jun 2026 00:18:16 GMT  
		Size: 3.8 MB (3767647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5ec9ce420ff7b809c19358c28969621e5ed9d561a98d246433487a1a37d9d0a`  
		Last Modified: Wed, 17 Jun 2026 00:18:16 GMT  
		Size: 17.8 KB (17754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.13.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:4f52f295f962ca27d5b066dd3edfba7c3cb2c4b44eaa63985c18b0e7866ebc11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163360902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bee66968b82731d5260302c999d004dc566a7a261a12e1d52bc01a19d92134c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:43:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:43:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:43:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:43:17 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:43:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:43:17 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:49:37 GMT
RUN set -eux; apt-get update && apt-get install -y make maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:49:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:49:37 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:49:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:49:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:49:39 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:49:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de4fe075b6dd2f22b2b5ed10e7aa905d6a156ebcea02659f73eed01d90f3f8b4`  
		Last Modified: Tue, 16 Jun 2026 23:50:05 GMT  
		Size: 90.5 MB (90537002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4273ecc671ff91c7968fca3bdabcada23a6ca3a62f6b5a0137e67a887af44dc4`  
		Last Modified: Tue, 16 Jun 2026 23:50:04 GMT  
		Size: 18.9 MB (18922386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45de982be076580f46c3e427fa3699eb35d1b2f631f094e8cebc35689c52f7be`  
		Last Modified: Tue, 16 Jun 2026 23:50:03 GMT  
		Size: 4.5 MB (4515187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e8e4325c39722e2ba329e4ea43a714b97b4ad56bb215a3159ca07150be768a`  
		Last Modified: Tue, 16 Jun 2026 23:50:03 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.13.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a2d61fd0bd38259bdec95c2a7bb6b31c9de39a2fc1016bcc8ef53bc0e946d6f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3782035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8e10ce468b1f1da880a2e792b08733c613b4b075217686e2561c0b3fca22670`

```dockerfile
```

-	Layers:
	-	`sha256:c2bd7953513fe531885307c01ab3a79ff45d003aef626b5b5c94264735d035c5`  
		Last Modified: Tue, 16 Jun 2026 23:50:03 GMT  
		Size: 3.8 MB (3764324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:252d688ff90734fceea9a6bfcdb704ab1f10c905720b1b58c2f342dff9a139ee`  
		Last Modified: Tue, 16 Jun 2026 23:50:03 GMT  
		Size: 17.7 KB (17711 bytes)  
		MIME: application/vnd.in-toto+json
