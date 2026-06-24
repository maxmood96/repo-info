## `clojure:temurin-11-lein-trixie-slim`

```console
$ docker pull clojure@sha256:7840d66e6d61316c5203489201398949c0435c6f51c980be267940a1f5154984
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

### `clojure:temurin-11-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:22e496dd6bfccb2cbaf2944b241a3caf4d6e49bf9f6b5f293b662a61c143f375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.9 MB (196929633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ce2c3549dc4ab5f0ebfb79d1fb1633d715788b0b24712ace7507b010d9fda9`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:15:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:15:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:15:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:15:51 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:15:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:15:51 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:17:08 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:17:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:17:08 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:17:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:17:09 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cecc09d0db743b703f56e5bb40f9bf269a33e3c2b5817147c9eef5505ac6a1e`  
		Last Modified: Wed, 24 Jun 2026 02:17:30 GMT  
		Size: 145.9 MB (145886165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c44053d3a2a11db1bc85df7c700d0b4e3798f4adadff4a2684bb90f2e2e97c`  
		Last Modified: Wed, 24 Jun 2026 02:17:27 GMT  
		Size: 16.7 MB (16742824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314d393b1a8a971346de3ee0d623581521517c5647a3acd77861197a2812eb78`  
		Last Modified: Wed, 24 Jun 2026 02:17:26 GMT  
		Size: 4.5 MB (4515193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1ef91733d445e90e303562d041aaa01d18be989d007caf372919005262afeb83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2402361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:291b6a2c722195be3a8646f1845219274e2c9220b2a14d447d82590d293d220d`

```dockerfile
```

-	Layers:
	-	`sha256:156029319291c0133984ab8ca38da44d6345d12ebb489358dd102c34244631af`  
		Last Modified: Wed, 24 Jun 2026 02:17:26 GMT  
		Size: 2.4 MB (2386597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b25c87873b6294b2f92412f3f91d83f3f3db0fb5744cd6a01cc7d2c0cb865214`  
		Last Modified: Wed, 24 Jun 2026 02:17:26 GMT  
		Size: 15.8 KB (15764 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1377f5ec9d5247cb471e9970738675e5a0bd66ad335620f2a974fcdf593dc1bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 MB (193957597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:448978b177632b41eb7c7a652867362fc9ebf481391a050d80f7e8c718a3e67c`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:22:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:22:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:22:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:22:49 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:22:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:22:49 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:24:04 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:24:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:24:04 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:24:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:24:06 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789bd356a8e8e958b71a7325e958e5befc1a9dd56eb4d96d95d07c5efab6a522`  
		Last Modified: Wed, 24 Jun 2026 02:24:25 GMT  
		Size: 142.6 MB (142582159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7c776b426d14a0e3089ed49864d1e535c18fd4d9d701a20a74cbed30b39798`  
		Last Modified: Wed, 24 Jun 2026 02:24:23 GMT  
		Size: 16.7 MB (16711639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d761723eebb18835f41d28b9b19b575168bdd738f8d3af17c029e1d3173e10ba`  
		Last Modified: Wed, 24 Jun 2026 02:24:22 GMT  
		Size: 4.5 MB (4515216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6275b6a2d57c88294bce3aaa7ea5626972ae1fa9fe82bbe9ce7ac79f796d633d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2402710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:373237cf0ebb8575a6898e47e449e86dbf8d6910b127ac072b7404e9adcafde5`

```dockerfile
```

-	Layers:
	-	`sha256:594b03103dac4f9a078e15b714394dd70efc7abe66f83034686dcc50f2f79172`  
		Last Modified: Wed, 24 Jun 2026 02:24:22 GMT  
		Size: 2.4 MB (2386825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43913f11a34d8ead2ec89cd87ec578fb05e44d32b12e8cc2be58b0062a716fb2`  
		Last Modified: Wed, 24 Jun 2026 02:24:22 GMT  
		Size: 15.9 KB (15885 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:770da58d5a132509d200d91e9697c1ca000f2b5ec75bf61526335861fc228d2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (188014175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3afa563861de2b4d61d9b4424441918b8bae74cecbe1d2df58982bd98081d474`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 07:55:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 07:55:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 07:55:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 07:55:31 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 07:55:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 07:55:31 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 07:58:10 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 07:58:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 07:58:10 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 07:58:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 07:58:13 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:639e1c13483ea279c94219be2736856262d8dd2efeff3e6d309f11a66aba21fb`  
		Last Modified: Wed, 24 Jun 2026 00:30:29 GMT  
		Size: 33.6 MB (33606388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db522026de845aea7c62013762889066999c7eaf835c33375388fea3c6f40605`  
		Last Modified: Wed, 24 Jun 2026 07:58:47 GMT  
		Size: 133.1 MB (133110641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e28903e70ffcf1bccbab6136c6fa3880b62f6185169ec53974bded54e42496`  
		Last Modified: Wed, 24 Jun 2026 07:58:44 GMT  
		Size: 16.8 MB (16781926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466a3d1b6bcd072088b5b9270735c10d677c6cb496ba294600751b09b594ba15`  
		Last Modified: Wed, 24 Jun 2026 07:58:44 GMT  
		Size: 4.5 MB (4515188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:88c48f8c16c5de1061044f207aea9ad5601888928899699076ee7882d408d36c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2402770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a638684e6c495bac872ed2c46206fef6a0250fd173baa3e973c32b8ab03c5fa`

```dockerfile
```

-	Layers:
	-	`sha256:06efc5e5ca9e40b7258511a6922f943b116f154cfcf81ebe4d7273aaa919f04a`  
		Last Modified: Wed, 24 Jun 2026 07:58:44 GMT  
		Size: 2.4 MB (2386962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3daa45c3d6f0328228a4a8f762aefeb941f885a2bf90b448b6dddfb148733be2`  
		Last Modified: Wed, 24 Jun 2026 07:58:43 GMT  
		Size: 15.8 KB (15808 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:b94202b4f001fe00b6c6fc2bc5ddcf551985ea9d8025181ec38cb029112e2590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177798779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbde78ba235f0488cbaa49c53d2ab538a74506457fed4eb5eb080338a66230c7`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 04:09:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:09:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:09:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:09:53 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 04:09:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 04:09:54 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:11:03 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 04:11:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 04:11:03 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 04:11:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 04:11:04 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b6a0af2ceb4b698210b8776157288a3fb06e46aaf75d641139449fcc50ce430d`  
		Last Modified: Wed, 24 Jun 2026 00:28:43 GMT  
		Size: 29.9 MB (29851381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b87600735711a900456e3bd25c4cf517f88c2e7b03e995721c676276dba2d8d`  
		Last Modified: Wed, 24 Jun 2026 04:11:29 GMT  
		Size: 126.7 MB (126652567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1800ec9df242f49f81f71e04a1f439ccb2a7de6fd5522202c90744a1e55d385c`  
		Last Modified: Wed, 24 Jun 2026 04:11:26 GMT  
		Size: 16.8 MB (16779611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e011fd0c8cc14ab22cbac064fab5a9b50bf76cc730680e85da2af6a87d1514a`  
		Last Modified: Wed, 24 Jun 2026 04:11:26 GMT  
		Size: 4.5 MB (4515188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3c9ea94377db43f7279ca436f5f1b5bc8c7c807a911d9f650293f92463c62ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b7b91a0e10378b1665d0f2bbaca3e8f1282741c36083c72c857f699207323ca`

```dockerfile
```

-	Layers:
	-	`sha256:28c83d79bd77ecb1939aa4545f0edede9b7bc09d1a12dcfbcf7f4cd5dd5c0e12`  
		Last Modified: Wed, 24 Jun 2026 04:11:26 GMT  
		Size: 2.4 MB (2383028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fed7e8fbf6edecc6e8d5b1b1d4223a24a078d576ede8605fec43dfb05a889265`  
		Last Modified: Wed, 24 Jun 2026 04:11:26 GMT  
		Size: 15.8 KB (15763 bytes)  
		MIME: application/vnd.in-toto+json
