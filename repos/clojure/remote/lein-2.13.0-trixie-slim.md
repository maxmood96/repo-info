## `clojure:lein-2.13.0-trixie-slim`

```console
$ docker pull clojure@sha256:8b9513b77050e816fba1108b33cbd5ad06b47b694777f91b1736a7df977c2ebf
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

### `clojure:lein-2.13.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ee475416548725627f0895914c3ac2d3ba96bab49128b8543cc2b281d065f82e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.6 MB (143618329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c6734ee908859eda90a1fe351983705bdda156c401a47a9c96245f7a10ee01`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:37:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:37:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:37:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:37:49 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:37:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:37:49 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:39:05 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:39:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:39:05 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:39:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:39:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:39:06 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:39:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044c01fbca7d1f74e96c66392e3cc2d0c577b615dc2b61fc5603e4dbd4526b5c`  
		Last Modified: Tue, 16 Jun 2026 23:39:25 GMT  
		Size: 92.6 MB (92574564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6705aa463024571ce50a64b0b3b320366cd988f75b55f83253aa61234858338a`  
		Last Modified: Tue, 16 Jun 2026 23:39:23 GMT  
		Size: 16.7 MB (16742753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae76a5bf29000015f0e999b520c2486938a73e9f56c59fa3a142436567e802be`  
		Last Modified: Tue, 16 Jun 2026 23:39:23 GMT  
		Size: 4.5 MB (4515167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3292e3d23ddd72a084fd9cd2f226f514241adfd6cdf27ebd7b74b8ce3befdb2`  
		Last Modified: Tue, 16 Jun 2026 23:39:22 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.13.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7a57faf7ac3c26597d9f97313d58e2cf2f7e39e8aaaa969c9f2788b59a26a4b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2353529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed386923544b32104ac1d3476c9fc77324a3e84fab357596ba5b00884fb6297f`

```dockerfile
```

-	Layers:
	-	`sha256:633c0dd60fd7c38e1766226723ca2c8b60041b857db5936eb6778b806ab297a0`  
		Last Modified: Tue, 16 Jun 2026 23:39:22 GMT  
		Size: 2.3 MB (2335129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5688ba9371d91949287a1746d26b4ab92ad4dec4c2a6c15ebe8276b46e95f851`  
		Last Modified: Tue, 16 Jun 2026 23:39:22 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.13.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7df5277a9ff5bdc812b7a9bd6be6e43a0d6c3e765df9ae3d5025983ac7eb9fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.9 MB (142917995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a2eb7d24322be54b72bb9b03264311c8e89540b72f6fc44d39e5885896791c7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:37:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:37:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:37:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:37:40 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:37:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:37:40 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:38:56 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:38:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:38:56 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:38:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:38:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:38:58 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:38:58 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d21978ab524a4c7038f0ebc427c03d83e392948a3340ea30cfd394812fee92f`  
		Last Modified: Tue, 16 Jun 2026 23:39:16 GMT  
		Size: 91.5 MB (91542260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b68156eb781b1b11a713cb4964f14f5260700cf9955a96a2ec68b822001095`  
		Last Modified: Tue, 16 Jun 2026 23:39:15 GMT  
		Size: 16.7 MB (16711555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc746fdc3290a717ae8b0e8d2614d686b83fa9b6e093f0da5536bbde21574e08`  
		Last Modified: Tue, 16 Jun 2026 23:39:14 GMT  
		Size: 4.5 MB (4515220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685bb7baf5e751130fa4bd57e66ff3a20460bfa650444c0c4f6a1dcbaf75728e`  
		Last Modified: Tue, 16 Jun 2026 23:39:14 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.13.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:722e8ec1f3ad8d0754768ba6010ff03e11cb5e66c9debe10ae3c5ed4279394e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2353305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3c3c6d7ae918af2082e4981a0b8d2f90abd2ef009dba2f774ba3c59ba22676`

```dockerfile
```

-	Layers:
	-	`sha256:2d868932b1d21ab9ac7a85dec7c30b1bd45f56e91c8ac5b2f2848521ca2c22a4`  
		Last Modified: Tue, 16 Jun 2026 23:39:14 GMT  
		Size: 2.3 MB (2334760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d48cccbb8d532a7cf63b3318c169653524cbb8ceb06137069fbd21ba5c450823`  
		Last Modified: Tue, 16 Jun 2026 23:39:14 GMT  
		Size: 18.5 KB (18545 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.13.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d07931c28608effdef6bb06f627deda5010e9c1318f399938890b5e5b030ad51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146818032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f1d4751e895eb6794b08dff4ce5c5061b054206f82ada29e49c11e754d738de`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Wed, 17 Jun 2026 00:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jun 2026 00:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 17 Jun 2026 00:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jun 2026 00:06:39 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 17 Jun 2026 00:06:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 17 Jun 2026 00:06:40 GMT
WORKDIR /tmp
# Wed, 17 Jun 2026 00:09:21 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 17 Jun 2026 00:09:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 17 Jun 2026 00:09:21 GMT
ENV LEIN_ROOT=1
# Wed, 17 Jun 2026 00:09:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 17 Jun 2026 00:09:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 17 Jun 2026 00:09:26 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 17 Jun 2026 00:09:26 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d2e9d705b633c31ee18ff0b56f7ec3ad425fb9e720182ee7a6e0f18d85842b`  
		Last Modified: Wed, 17 Jun 2026 00:10:02 GMT  
		Size: 91.9 MB (91914009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3988b62f6dd5c16c60ee94f04dcead13d040bed1810bbf54c9907675c924824`  
		Last Modified: Wed, 17 Jun 2026 00:10:00 GMT  
		Size: 16.8 MB (16782071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f8d12b51dd2c6f9a710a18a1f0946a97b2523fb8e369a2f5b33d0235d12650`  
		Last Modified: Wed, 17 Jun 2026 00:10:00 GMT  
		Size: 4.5 MB (4515183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf5612caefc5410b0abbaa5d6ae3595e18033ca3bad791686e4baaf114524f7`  
		Last Modified: Wed, 17 Jun 2026 00:09:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.13.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7eaf2bb94634567e649c0890954cea6f294ef394c51cfea259667357af6cb565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2337889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f2b5a0c05987001e342d6e560b90fffb0e2e5c5cd81295f26dfd0c0f119562`

```dockerfile
```

-	Layers:
	-	`sha256:8f4351695c5707b5e2047633f3d1dc4c87d438ea627489343b9488aa5a4fa1c8`  
		Last Modified: Wed, 17 Jun 2026 00:09:59 GMT  
		Size: 2.3 MB (2319433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c12e3cee552f04ce61b3f9a598b18ef7a0d34e16df18df9a5718a14e84be4c45`  
		Last Modified: Wed, 17 Jun 2026 00:09:59 GMT  
		Size: 18.5 KB (18456 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.13.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:9c90358d7ea7d5777346a5fbb1a2fde80cee11ec886ad3fe8930d0c6cf207ad1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.6 MB (139567601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6cc15e7be28f848ccac9944e2171e5f473b0f978de9cf6bacec556ba23ca058`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Tue, 16 Jun 2026 23:41:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:41:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:41:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:41:05 GMT
ENV LEIN_VERSION=2.13.0
# Tue, 16 Jun 2026 23:41:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 16 Jun 2026 23:41:05 GMT
WORKDIR /tmp
# Tue, 16 Jun 2026 23:42:20 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Tue, 16 Jun 2026 23:42:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 16 Jun 2026 23:42:20 GMT
ENV LEIN_ROOT=1
# Tue, 16 Jun 2026 23:42:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 16 Jun 2026 23:42:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 16 Jun 2026 23:42:22 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Jun 2026 23:42:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e141af4c3ca44d66006c21b5229d05180427e764c0a36b8e43c72eabd028a0d`  
		Last Modified: Tue, 16 Jun 2026 23:42:49 GMT  
		Size: 88.4 MB (88420336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9482dc5ca9b3004f09343d4ce9ae3958ee894228c4da1f267f4fa53ae4abfa99`  
		Last Modified: Tue, 16 Jun 2026 23:42:48 GMT  
		Size: 16.8 MB (16780293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9caa99a45afcafb0138e9d3acc27e1bfe26dbd1ad2e3e852c0a7d799975b000f`  
		Last Modified: Tue, 16 Jun 2026 23:42:48 GMT  
		Size: 4.5 MB (4515188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb688b5872adfb62fd1e33e9c76623052ce9fba6e98aa98107e73969a471bde`  
		Last Modified: Tue, 16 Jun 2026 23:42:48 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.13.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:453dbc97f0e7c1fa510ec67f542885f913017fb576e50d08d2e9b0def4f68e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4060a4193bc799cf4a12d4b79520e31467211b4920f59536fc7760d2d32eed19`

```dockerfile
```

-	Layers:
	-	`sha256:e47e460a18b3e54943aaf1ca8eb90ca3d7263e6b4b328fa8f1c9c901b99ac3d9`  
		Last Modified: Tue, 16 Jun 2026 23:42:48 GMT  
		Size: 2.3 MB (2316118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e317b1e7317cf04ac4441eb67ff29272c08391f4691babaed147881ff278e883`  
		Last Modified: Tue, 16 Jun 2026 23:42:48 GMT  
		Size: 18.4 KB (18399 bytes)  
		MIME: application/vnd.in-toto+json
