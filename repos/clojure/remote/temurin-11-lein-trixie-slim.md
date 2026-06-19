## `clojure:temurin-11-lein-trixie-slim`

```console
$ docker pull clojure@sha256:e1cdda43eeddd4e6da6d07776bd5aa67481248d016c9c7ef4f728aa7201cf169
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
$ docker pull clojure@sha256:73dc8b483ec40bf81341768c5eb8d81bfd84d423c82274db3bf9f594ff5b8bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.9 MB (196930153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82553537ce3ed05acf52e85085d81060ef3ce74bd97e503bfd1c25b7df4d6f70`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:15:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:15:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:15:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:15:37 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:15:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:15:37 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:16:52 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:16:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:16:52 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:16:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:16:54 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a4870b74893324c27ff071ac509c8b67bd3bd350a0cac69b32edeccf1883660`  
		Last Modified: Fri, 19 Jun 2026 02:17:12 GMT  
		Size: 145.9 MB (145886162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00edcddda20b0329a4c1a87bd28b9661f2518f2557d76e922e240dbd8109e398`  
		Last Modified: Fri, 19 Jun 2026 02:17:10 GMT  
		Size: 16.7 MB (16743328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61abdcf763e027761e54c86d10be27d905334ddd8cf2ba028c5103664ee5086`  
		Last Modified: Fri, 19 Jun 2026 02:17:09 GMT  
		Size: 4.5 MB (4515216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:83d3ed786bf1ec48d405c45aed1b31f9d6ddd2cbe688f509e68279652c2b4bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2402361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66edb533904d40354a1d1b931bf3673c5df33c04a2dbb8ab832889ef3d7ad122`

```dockerfile
```

-	Layers:
	-	`sha256:88e92fadaea910c2ecefc69026fafe45e1a29e1b226154d1b4b8abfb3a6a0dcb`  
		Last Modified: Fri, 19 Jun 2026 02:17:09 GMT  
		Size: 2.4 MB (2386597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b9488dab1bb03ec2d8aabb8a243540e93f86160d2d9e983314f5e8648d6d25a`  
		Last Modified: Fri, 19 Jun 2026 02:17:09 GMT  
		Size: 15.8 KB (15764 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8dee97b89cabf4bb6ea65f7fe4e1fc48294b5b51462f00a24a82d6992709ff0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 MB (193957431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf06c333029a8d2a52d8c87163c2d32c294461d11d77bf28914fbf391f77054`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:15:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:15:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:15:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:15:45 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:15:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:15:45 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:17:02 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:17:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:17:02 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:17:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:17:04 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b53ebc623387df5bedd5228ffb66ed6067acfd21825518f8b8b07b946b998be`  
		Last Modified: Fri, 19 Jun 2026 02:17:23 GMT  
		Size: 142.6 MB (142582140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4689829aed3e22af6be1d5d5d850b335bd6903d0d06e3cbce15de7dfe4ac309`  
		Last Modified: Fri, 19 Jun 2026 02:17:20 GMT  
		Size: 16.7 MB (16711500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e1aabee8930fd415b1f8d2cb03824713aa1a822fb72cc078311b20d13eb6bc9`  
		Last Modified: Fri, 19 Jun 2026 02:17:20 GMT  
		Size: 4.5 MB (4515229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6481f92f0d871789f7f03c8acaa53c9f1aa70d7310e0c9fbb08b06a2bc384b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2402710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c4e8d3e1edbc091d89f387d603490aebc650509ced9c3a2b6ba3b37ab5ecce`

```dockerfile
```

-	Layers:
	-	`sha256:23b690f1a523a0bd94091bf53521b9e77bdc3a68d3160de12639f7dcea6c9c97`  
		Last Modified: Fri, 19 Jun 2026 02:17:19 GMT  
		Size: 2.4 MB (2386825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84663e6416e80bf1edc592e20f3a5a1ae8c4fffdcb781d1fed9f7f1e440063fd`  
		Last Modified: Fri, 19 Jun 2026 02:17:19 GMT  
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
