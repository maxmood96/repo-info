## `clojure:lein-trixie-slim`

```console
$ docker pull clojure@sha256:e185df01719ae56eb1a7546aaab489bc50c206346cc0f68721584b1991c2aa9c
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

### `clojure:lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7ccdc84ea8fd854e9a6247d5eb603bf6a6981648bd2e70cc735b91c9f36f78c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.6 MB (143618202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c647ca14af274f53f5a24cc7e80eb23185ee7d727c0ddde2dbfb4758fa0aa9e4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:20:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:20:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:20:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:20:08 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:20:08 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:20:08 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:21:18 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:21:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:21:18 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:21:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:21:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:21:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:21:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762dda30aa9cf76546a178edf37e9aba848ac509a22fd4f31639f63f01b50df4`  
		Last Modified: Fri, 19 Jun 2026 02:21:38 GMT  
		Size: 92.6 MB (92574569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d6a85109fe4899fa1adef774b57fbf55142fba3597dca64918450b11b45493`  
		Last Modified: Fri, 19 Jun 2026 02:21:36 GMT  
		Size: 16.7 MB (16742561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9751d0f388718ec72435255c7040d6deed9aef9506a66effcf294c47336002f0`  
		Last Modified: Fri, 19 Jun 2026 02:21:36 GMT  
		Size: 4.5 MB (4515228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b3f4f11c156fe024614b3097188c0d61872207006a752b7da2944bc1de41a6`  
		Last Modified: Fri, 19 Jun 2026 02:21:35 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1ad2ef43c3891052c43abaa6a0387488ad1e44056ca3041876dc8978d9c6851b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2353529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50faa24ac4b50e7d10ccdbb5195f54b5be6e51ac284ebc3c50f3e12de717b09f`

```dockerfile
```

-	Layers:
	-	`sha256:a0c2439fa5902be46c8f45fe66da078ef1f32da74e81cf9844fdd323e0d5d156`  
		Last Modified: Fri, 19 Jun 2026 02:21:36 GMT  
		Size: 2.3 MB (2335129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a90693baedb5e8be2234e9e16d96b094f51563dd6fdc7b5e6fa8a9f280f4e21`  
		Last Modified: Fri, 19 Jun 2026 02:21:35 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:da3607bef036c93b1651889748899054c3d5821f1925d0a5609dd4b4b7a56473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.9 MB (142917884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd924b4ef639a78c71c826730b81c3b3e66821006bb265ceeab05536aa17fbbe`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Fri, 19 Jun 2026 02:20:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:20:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:20:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:20:15 GMT
ENV LEIN_VERSION=2.13.0
# Fri, 19 Jun 2026 02:20:15 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 19 Jun 2026 02:20:15 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:21:30 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Fri, 19 Jun 2026 02:21:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 19 Jun 2026 02:21:30 GMT
ENV LEIN_ROOT=1
# Fri, 19 Jun 2026 02:21:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 19 Jun 2026 02:21:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:21:32 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:21:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609a5c7736b53d2684282ca36cbbd47d5bb82a8a067e4be15c11555959dec150`  
		Last Modified: Fri, 19 Jun 2026 02:21:51 GMT  
		Size: 91.5 MB (91542254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f74fc7dee578d2d55356e5dfe6820fecfdf6634a4462c6fda41384f8ffd99e`  
		Last Modified: Fri, 19 Jun 2026 02:21:49 GMT  
		Size: 16.7 MB (16711465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9086c78a4dc5634ff1e4b874912b8cfe7fd24390acca3c06ea160081b9d5a4c7`  
		Last Modified: Fri, 19 Jun 2026 02:21:48 GMT  
		Size: 4.5 MB (4515205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e71c8270a49360ad0a60a2a5ab55ae38cf96f05e36d3eb04ae3d1d2511916a`  
		Last Modified: Fri, 19 Jun 2026 02:21:48 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e4fb44589518093d208fb0912832df769c77905c5df3657b671bfac8ff5275d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2353305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a4c3718a9f64f61e03bdd848adca0c046eb1339434503a5e2528860fbb4da1`

```dockerfile
```

-	Layers:
	-	`sha256:0300982b1c79df233ac7431d73b06c67f8c7a8b602bd20e03e819513197db324`  
		Last Modified: Fri, 19 Jun 2026 02:21:48 GMT  
		Size: 2.3 MB (2334760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c7f1c1e2f7d6d6e5dee41e96737cb7ba6c603ff0048f2a396b5610566807dd5`  
		Last Modified: Fri, 19 Jun 2026 02:21:48 GMT  
		Size: 18.5 KB (18545 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:5d8d6dfeff1c60ac64ad31e756318e3af0ebcba694101a08f669c29797759474
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

### `clojure:lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9610db639ab710362803c8652183232d53e30e533a5ef9b3b2a9d383e2fcad0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2337889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58bfd436dee6daf89b6de1938f0f1830c2fd4b56063e18bbb964d6bf726cc2ae`

```dockerfile
```

-	Layers:
	-	`sha256:02e403082a3367f1fa414425dbc67156c393600c3db9a1920bab119dc3ce43bb`  
		Last Modified: Fri, 19 Jun 2026 02:54:48 GMT  
		Size: 2.3 MB (2319433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:662fa6604b9b4b1e8362855b68ed993bcf2e1e8ac4e845c9f4a409c54cadbc3b`  
		Last Modified: Fri, 19 Jun 2026 02:54:48 GMT  
		Size: 18.5 KB (18456 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:9fd517535c950259cee7f17959b60f1db687c789d0777c5b82052fec6acdbff9
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

### `clojure:lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dabdcad02945efa80e6a17d320493e67ee016abbb66cdfd1121786485dca9025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207625bd68e348d9a9521eeb4854111384439bd87ff55d45c00d1ef021711f0d`

```dockerfile
```

-	Layers:
	-	`sha256:8a7963e074e4de31f786e63a1aa8f3f11debc72ff7ded49964ad6abb518e0558`  
		Last Modified: Fri, 19 Jun 2026 02:21:34 GMT  
		Size: 2.3 MB (2316118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b37f8445c407549cda68db25e4bc8180b41c19d3a66036e37556141793b99d8`  
		Last Modified: Fri, 19 Jun 2026 02:21:33 GMT  
		Size: 18.4 KB (18400 bytes)  
		MIME: application/vnd.in-toto+json
