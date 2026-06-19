## `clojure:temurin-17-lein-2.13.0-trixie-slim`

```console
$ docker pull clojure@sha256:9b8bd6e4a6776c25add51b26c44d997f1c3134762c1de9e4fefec1d3438151e0
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

### `clojure:temurin-17-lein-2.13.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8eb6e437eb0ead2b2d2988e0ad6114e002d55303921998e8a2132a66cfdb4dd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.9 MB (196949411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde096ab829744ca26bbb7c2d20770b9e48c35730d7d09c7f802d719cd584b97`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:17:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:17:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:17:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:17:05 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:17:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:17:05 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:18:20 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:18:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:18:20 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:18:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:18:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:18:22 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:18:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e4a01d6ba161d4e52c06d88d8c65e974381fa61e9bc011a3e945d085edc8f1`  
		Last Modified: Fri, 19 Jun 2026 02:18:44 GMT  
		Size: 145.9 MB (145905425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8bb094162d071a46ac2e8303c816cca01c5fe772403c65d3dadee11ed1fd63`  
		Last Modified: Fri, 19 Jun 2026 02:18:39 GMT  
		Size: 16.7 MB (16742915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6676c54fd84a54db4083caf726f247bdb303adb95464fb6b3896394eabdf2aba`  
		Last Modified: Fri, 19 Jun 2026 02:18:38 GMT  
		Size: 4.5 MB (4515226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3f91a9abaa8581d18083cfbc46c23507971d4116a80c338246c34c82633ec9`  
		Last Modified: Fri, 19 Jun 2026 02:18:38 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:240339b68695c07415fe2a81353beaa966860792a6f9611b918515ba0e492d32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6537b9d9cb8e88d839a5b591a06f73aba585c876dfbc99c54767d185a8b949b3`

```dockerfile
```

-	Layers:
	-	`sha256:54c12d8e2a662921cabd2eac29265ee7f2810ce1642a607de8d15d7adc82d087`  
		Last Modified: Fri, 19 Jun 2026 02:18:38 GMT  
		Size: 2.4 MB (2367081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:414530ba85c0e8beaf03ab3caab5c38dbe23c322ec8e90f1dcd87b2684cea56c`  
		Last Modified: Fri, 19 Jun 2026 02:18:38 GMT  
		Size: 17.8 KB (17753 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.13.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c60f16f3537d32d64d0e95bebaeafb93cd68b9a0aab7601a83b4576e65dbdc0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.1 MB (196099552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dfb1c9c5b81af137abeb1a4bbcba098e8625353d25be0830cbdac21628f9f86`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:17:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:17:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:17:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:17:25 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:17:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:17:25 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:18:40 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:18:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:18:40 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:18:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:18:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:18:42 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:18:42 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45be6e49d0401dd197c27ec3f1da0398dad998dbef009df0a176bdc5842200d`  
		Last Modified: Fri, 19 Jun 2026 02:19:02 GMT  
		Size: 144.7 MB (144724310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0426d3613a8cf6a35b5e939a7a10681f879f6631ef779cc942c04410a11e81`  
		Last Modified: Fri, 19 Jun 2026 02:18:59 GMT  
		Size: 16.7 MB (16711072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c80ad7ca0fd7408a247566379497de4385e39dcdc881fbe8423655748be722`  
		Last Modified: Fri, 19 Jun 2026 02:18:58 GMT  
		Size: 4.5 MB (4515210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161502afc4224d68872b49c3bb5d8e09531a67cc3fcde31508cf647bd6768ace`  
		Last Modified: Fri, 19 Jun 2026 02:18:58 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:855bff4d1347192e5e8670ae0a852b22eb4ae10ab127028a0a6d61762cc49c68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ee62324eab1c7446060b112c2cff2f930858c5484faddb382d6bfa9506bb1f`

```dockerfile
```

-	Layers:
	-	`sha256:46bd451d2571fcc9c115035920f93994eb7e2ae3afedb7ff15f167f93b43276f`  
		Last Modified: Fri, 19 Jun 2026 02:18:58 GMT  
		Size: 2.4 MB (2366691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92534132509fd391b0ad6b3e55445615c0116a09f86e6c8697204fd3a4cd1ba2`  
		Last Modified: Fri, 19 Jun 2026 02:18:58 GMT  
		Size: 17.9 KB (17873 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.13.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:9ae3c799207af18bdea1dc8e01e788c2bdb364ba0789002d59fecaef5c34b91f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.7 MB (200670668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20610d18d882bb41e2dc59ff5a23a6704184dc5af2319f131a6b93effcd9294a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:40:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:40:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:40:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:40:59 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:40:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:40:59 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:44:13 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:44:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:44:13 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:44:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:44:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:44:17 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:44:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c12061528e7da232c3a05c00802e8fb865782cca2399322852ad4b4c6566c13`  
		Last Modified: Fri, 19 Jun 2026 02:44:54 GMT  
		Size: 145.8 MB (145766192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc71102235546c0e1f845ce2a55876b4f5f506d0a02be97145170a4f45b5fb0`  
		Last Modified: Fri, 19 Jun 2026 02:44:51 GMT  
		Size: 16.8 MB (16782475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4100a58f7d02e211bf388edcbf54e2d89b1cd0b154c1ac6c735da5bfd749c5f3`  
		Last Modified: Fri, 19 Jun 2026 02:44:50 GMT  
		Size: 4.5 MB (4515233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898d1a4005773ece28acd56d574050f2e2090559d03033fe4f2415c766475f1a`  
		Last Modified: Fri, 19 Jun 2026 02:44:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:565dd85d5f66bfdc7bb1be4975b5501a3714dfc912c8d39cacb26b126b5f1cab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac243f3f771abadefe134ba259d427a1cb4f9d67e8c25e8a708dd77a19dbaf0`

```dockerfile
```

-	Layers:
	-	`sha256:69b962d860e49e979c29b7d4ba8a0af9b6e0741b2574dd5d50687444afba3dac`  
		Last Modified: Fri, 19 Jun 2026 02:44:50 GMT  
		Size: 2.4 MB (2368061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:303c6aeeaf64556f180bc1783023d13d72ceb3083b9a0dfa70643b2b74730c7e`  
		Last Modified: Fri, 19 Jun 2026 02:44:50 GMT  
		Size: 17.8 KB (17797 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.13.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:489435e7a4d6e04b28831e52bafd6fb890f8ffcdb90493e8751b74de5419fbec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187057233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b1f5c2852698043154decd8750d574c6a4f86732f6079ce132cfb123895ee7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:17:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:17:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:17:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:17:15 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:17:15 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:17:15 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:18:30 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:18:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:18:30 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:18:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:18:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:18:32 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:18:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd16adea10fbf1d54ca2e5edb1f4b081332ccd028cf6b0964ac17b7ace1cf74`  
		Last Modified: Fri, 19 Jun 2026 02:18:57 GMT  
		Size: 135.9 MB (135910426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bc5db70cad8c0e6d707a01e3b50dc55cc52a13f933d6c5c47d77c86602c7a3`  
		Last Modified: Fri, 19 Jun 2026 02:18:54 GMT  
		Size: 16.8 MB (16779799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c670dbb487320826dcacb893af0b699e8c772e9bede8f8a0c11bf25ca6c1cd2e`  
		Last Modified: Fri, 19 Jun 2026 02:18:54 GMT  
		Size: 4.5 MB (4515225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af059e947a6d3e2704409b8f5d7b0997a5c859f779b9ac0f48d1745def2478c6`  
		Last Modified: Fri, 19 Jun 2026 02:18:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.13.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:27b951dbdfacbb08fa7cce60c01f3e9b37a38d90dbf3cc0bb798cf8674eb52cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d1ab1e4b020ca16f4be380fb89154c853233f7824dc03fb53b642b01d3fe98`

```dockerfile
```

-	Layers:
	-	`sha256:6cc927f416089cbebd7e86a74d804ca6c6005b326f0424fffbcaa88faa10a959`  
		Last Modified: Fri, 19 Jun 2026 02:18:54 GMT  
		Size: 2.4 MB (2363508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3223277262d56a86597d46f031c94a0074c54a6d2e922a7b3ada43c35c81d4db`  
		Last Modified: Fri, 19 Jun 2026 02:18:54 GMT  
		Size: 17.8 KB (17752 bytes)  
		MIME: application/vnd.in-toto+json
