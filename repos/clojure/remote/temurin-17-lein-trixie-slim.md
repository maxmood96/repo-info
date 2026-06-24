## `clojure:temurin-17-lein-trixie-slim`

```console
$ docker pull clojure@sha256:e559c6102e5ad601b09e11683e744434bb324ecc29dba36d8525d64a982f3605
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

### `clojure:temurin-17-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b9383f5e8ea7f1533723f6c44ace5fa723695869cb0246787c85495262b061c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.9 MB (196949038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23da9083d6af28eb7fc252c8c838798064bbffd1cda7c7baf860f0f731be85bb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:17:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:17:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:17:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:17:44 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:17:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:17:44 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:18:59 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:18:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:18:59 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:19:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:19:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:19:01 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:19:01 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fefbb45f8a05acbea95ed420822365aa7549e295edc2962382554ec22127af83`  
		Last Modified: Wed, 24 Jun 2026 02:19:21 GMT  
		Size: 145.9 MB (145905407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f5aba8d6a30dacc410d5077527adad3015d7fc4449fb0d84db744fdc486ece`  
		Last Modified: Wed, 24 Jun 2026 02:19:18 GMT  
		Size: 16.7 MB (16742566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7b5e9f433b98807f5d3c5f99bdda42f4af1436e101e6d2d1d76774d270dfd5`  
		Last Modified: Wed, 24 Jun 2026 02:19:17 GMT  
		Size: 4.5 MB (4515217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9281cbee40e984401d3bce6dfca27943326760f41de37ab9153d425b1d0ea9d`  
		Last Modified: Wed, 24 Jun 2026 02:19:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c8da5c0bed25c524fa95e44bf72635408c2ac27922dddbe925bf3f0825f89678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25f7be661eda78accd6a11e0dd5a28263c0d80026c1a2cbae7e4a308e1a8a2a9`

```dockerfile
```

-	Layers:
	-	`sha256:b030616d89d73e2d72c305f6259fe532b5408e566a1dfda84bf1ebf11e63d33e`  
		Last Modified: Wed, 24 Jun 2026 02:19:17 GMT  
		Size: 2.4 MB (2367081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e58f4a31ccf6b0a8d671bf2938e8ca291ef579e87bbe8ebf1faf6e131161b0c`  
		Last Modified: Wed, 24 Jun 2026 02:19:17 GMT  
		Size: 17.8 KB (17753 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:51ae1d8c1dc188341810fa59b514a246398a1d6c24f3cced7791270de9206aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.1 MB (196100005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62b1c894781820ccdfd59d5e228c95ebfc017825f8e384b808cf97f356567474`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:24:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:24:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:24:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:24:13 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:24:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:24:13 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:25:29 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:25:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:25:29 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:25:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:25:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:25:31 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:25:31 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a672f27034f2d96295f80af7b7d571b77b1f6a98957be61414a228b26b1d6ea8`  
		Last Modified: Wed, 24 Jun 2026 02:25:51 GMT  
		Size: 144.7 MB (144724322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9d968247cf41c7baa84819e8967a702c6588c52d71fdc540f68741997e0cc5`  
		Last Modified: Wed, 24 Jun 2026 02:25:48 GMT  
		Size: 16.7 MB (16711490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70cd9eb4293e2daf23fc78163c3e6813c6787c791d1d0742da2ef171fcff217e`  
		Last Modified: Wed, 24 Jun 2026 02:25:47 GMT  
		Size: 4.5 MB (4515212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e3c4b9c4347d4a634705ebd738431b0cae15794e2a9d2c35c3df494a0fb6e5`  
		Last Modified: Wed, 24 Jun 2026 02:25:47 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:654bb10ceedb2977fbb6b72feee4573bfcb34a647710822c797caa6c0d1f3565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af2c41c674870d8ce26988de5d3d90e6c1e857d418dfcb7a36339e51badcbb2`

```dockerfile
```

-	Layers:
	-	`sha256:f4e64db05e5abfc34b3bcd909373dc3ebcf3812ad94a46109acdaf352b92933f`  
		Last Modified: Wed, 24 Jun 2026 02:25:47 GMT  
		Size: 2.4 MB (2366691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2134dc02e00ab05f6b1fad28187a5669289ae86f3738550b35e7ae594c26c3b2`  
		Last Modified: Wed, 24 Jun 2026 02:25:47 GMT  
		Size: 17.9 KB (17874 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; ppc64le

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

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

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

### `clojure:temurin-17-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:f964b68c390036168d6b1b1116fb59995178d6127a769e727ee4cd9935f011e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187057268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569022b9cbea908e008d3b6aa07af3dfa951c71fabd3403ad51308bdf0629a7e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 04:12:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:12:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:12:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:12:03 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 04:12:03 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 04:12:03 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:13:14 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 04:13:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 04:13:14 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 04:13:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 04:13:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 04:13:16 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 04:13:16 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b6a0af2ceb4b698210b8776157288a3fb06e46aaf75d641139449fcc50ce430d`  
		Last Modified: Wed, 24 Jun 2026 00:28:43 GMT  
		Size: 29.9 MB (29851381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05c36f551f9fd6de79c47abc786138e29e52e3c8358678884024c1b48e8687d`  
		Last Modified: Wed, 24 Jun 2026 04:13:41 GMT  
		Size: 135.9 MB (135910422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4b1bd9243318d345c9ea4ecc11a6b54a4202f3666c4952fc8ddbabc4448da8`  
		Last Modified: Wed, 24 Jun 2026 04:13:38 GMT  
		Size: 16.8 MB (16779835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4354770efb732aaa14f04bb9c115809b7668816eeac371734c124c2af28919`  
		Last Modified: Wed, 24 Jun 2026 04:13:38 GMT  
		Size: 4.5 MB (4515200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2b34bf4fb557e4584afc44bb3cb342e56f750e62ba6bcb005abea0dc40bf85`  
		Last Modified: Wed, 24 Jun 2026 04:13:38 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1bfba3be5fb3a556221b3a23915f7b7d34af6222ef867c832eace7b6d271c511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b29bc0645d09f2e97de3df6392f6dbb39c7be4218aef65f92188aaa10fdbf36c`

```dockerfile
```

-	Layers:
	-	`sha256:93650db64303a4021ac802fa1741788ee6d17f6a9044e5aeacd74570db3bf561`  
		Last Modified: Wed, 24 Jun 2026 04:13:38 GMT  
		Size: 2.4 MB (2363508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fe8cfaa47fd4bf08297c5270aacbe55b2988c7d83ce577ca07dd8f3da91d997`  
		Last Modified: Wed, 24 Jun 2026 04:13:38 GMT  
		Size: 17.8 KB (17752 bytes)  
		MIME: application/vnd.in-toto+json
