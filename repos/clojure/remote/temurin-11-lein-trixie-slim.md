## `clojure:temurin-11-lein-trixie-slim`

```console
$ docker pull clojure@sha256:c95d2a7cbd061042e8ee216dba08633ef96cc50a76aa9705c267abadeb6a48c5
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
$ docker pull clojure@sha256:718b0523e5132f17ba0a3e4d4dcfc754ce6cd1c8e711e6bcd855693558afa298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (188014631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e8730897d30b23571888850d43c62586706fde5d3833fedd8e29ac24029b4b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:29:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:29:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:29:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:29:08 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:29:08 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:29:09 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:32:19 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:32:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:32:19 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:32:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:32:25 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2428a8f97ac98f0d71ffd28681ba4ff4587bb2650c297ffc24f3785b183cee`  
		Last Modified: Fri, 19 Jun 2026 02:33:02 GMT  
		Size: 133.1 MB (133110616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b701981a681035eec125512938022e01eddc1096b136df5a1e9711433f27f273`  
		Last Modified: Fri, 19 Jun 2026 02:32:59 GMT  
		Size: 16.8 MB (16782401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932f1347799285c7578fa00132a0ad95accb5956d494eda85732e7a96ba8fb80`  
		Last Modified: Fri, 19 Jun 2026 02:32:58 GMT  
		Size: 4.5 MB (4515242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:06e63accac352fdd7a9c71bff49b19611a3bfe6425fd8de1e2b68cb02ad56706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2402770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eda31f804d33089dbb186f79bdb6ee0552b7a9a47fac39fb8e403b85b1aaa35`

```dockerfile
```

-	Layers:
	-	`sha256:bf56c35304e329cc5ffc1fb5be3a5715a2badeda2b6b78bcfe4f36d8a3562fb6`  
		Last Modified: Fri, 19 Jun 2026 02:32:58 GMT  
		Size: 2.4 MB (2386962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecfa3a6c3b4db577d2f6b2691005606c03900fd920f497546a8d5057732be0e6`  
		Last Modified: Fri, 19 Jun 2026 02:32:58 GMT  
		Size: 15.8 KB (15808 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:9f2655a33f6bc40ebb399581cef8e4620b14b7a661d7b571fd251c52797affa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.8 MB (177799000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:241ad181d2696e2b667b8a9dc32207ba76bd00ab2687148ffa9b283b775f2e1b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:14:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:14:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:14:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:14:00 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:14:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:14:00 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:15:22 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:15:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:15:22 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:15:24 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:15:24 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd9a5cf310e63c0615d380a52eb1e280e0631226aa90f1347143cb06bd067939`  
		Last Modified: Fri, 19 Jun 2026 02:15:47 GMT  
		Size: 126.7 MB (126652584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e08b81908522a87be55e97fa3ec7df87e884f0d23479b659c787363df196af`  
		Last Modified: Fri, 19 Jun 2026 02:15:45 GMT  
		Size: 16.8 MB (16779809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6703fb1bd7956ac8d6647f5824386d7c87d8bf6ae9c1651827bcc23a429b134a`  
		Last Modified: Fri, 19 Jun 2026 02:15:44 GMT  
		Size: 4.5 MB (4515221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:79213ad6b9f4d101ba0edd99addd2b5a9e6adf15179e176dda684cc18ea51072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ab97011f3151a7524c6fe9df5e3476bf1999185a3c4ea129c4dba438d8110b`

```dockerfile
```

-	Layers:
	-	`sha256:21f322f28c4b3f32d7bac9637bd0a66b563c93bd9cb53415be3a36c3530463dd`  
		Last Modified: Fri, 19 Jun 2026 02:15:44 GMT  
		Size: 2.4 MB (2383028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:536a20cbcdf59ad23400991ee4d0b17f185edc9db1957a4ff27ceaf2aed3eb0f`  
		Last Modified: Fri, 19 Jun 2026 02:15:44 GMT  
		Size: 15.8 KB (15762 bytes)  
		MIME: application/vnd.in-toto+json
