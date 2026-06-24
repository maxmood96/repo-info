## `clojure:temurin-21-lein-trixie-slim`

```console
$ docker pull clojure@sha256:1f9b4a1ad24e342c5ccbc23754c3024d34257d5b26f198a7825f35072898289f
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

### `clojure:temurin-21-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ff452c60f42ebe2954c43c2c068868215ee555fc81bfcc7de87ba21dd34f8d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.2 MB (209211120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d2a0f77a2a267d05dc7459451103c156ff9493bb7498b18faef816e579a8af`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 01:43:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 01:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:43:42 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 01:43:42 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:19:24 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:20:42 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:20:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:20:42 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:20:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:20:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:20:44 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:20:44 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7473c91b88d5eb633f18a6a19dc16a1174c9959796e98bd7a022ab10b75c41`  
		Last Modified: Wed, 24 Jun 2026 01:45:17 GMT  
		Size: 158.2 MB (158166926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db25e66c8f1c91c15e8fd71acb9bf9669655d97c8c17362147d66f5d2f60f948`  
		Last Modified: Wed, 24 Jun 2026 02:20:53 GMT  
		Size: 16.7 MB (16743127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e5c2537acf932dbc6cab1101303512ae13e0104bdeaf2ec3455fec4657284c`  
		Last Modified: Wed, 24 Jun 2026 02:20:53 GMT  
		Size: 4.5 MB (4515219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151e8bc201f3d5a20c3657dd29f4ed6d3cba38c50ab29570d9d55a666bfeffc9`  
		Last Modified: Wed, 24 Jun 2026 02:20:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:69c235c0dceadd9d29857a81d0a9e8a3573a6bbc0955a40519d814affe1af786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e3199a5b266a257866ac8b016cf852c00d038be4e7a55e7b82ab122629f175`

```dockerfile
```

-	Layers:
	-	`sha256:0b5a996d1036aed647862b1e0acac8872c4b88e648a6c2579aa188d44ddb8b58`  
		Last Modified: Wed, 24 Jun 2026 02:20:53 GMT  
		Size: 2.4 MB (2368933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:816d44f121fdcc5dc15b87d55b93ad1916e835e7a09f33cf66fd65fb36105aef`  
		Last Modified: Wed, 24 Jun 2026 02:20:53 GMT  
		Size: 16.8 KB (16798 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:73460206934bdd8868115b7e7c010b60264c7015e6e170ba4ef295b6f24ecd75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207837062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b002010c1f8bd5001d8507f5a3ccaff0d95fb6dcbc4d8280c3ed92b4439734f8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:26:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:26:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:26:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:26:01 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:26:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:26:01 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:27:17 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:27:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:27:17 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:27:19 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:27:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:27:19 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:27:19 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1738deb2880d5c7ada0d6868777c9e272a1887c111d1656d8e23281e2c278a`  
		Last Modified: Wed, 24 Jun 2026 02:27:40 GMT  
		Size: 156.5 MB (156461287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad2b7d99aade0dfc7966e2f723324013bde75061cbe42ea08991de1814ac3e8f`  
		Last Modified: Wed, 24 Jun 2026 02:27:37 GMT  
		Size: 16.7 MB (16711603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f3baee3b94b2feafb3268ba831885fffbd281e5c2d476d87f175f9977a42f7`  
		Last Modified: Wed, 24 Jun 2026 02:27:37 GMT  
		Size: 4.5 MB (4515192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200c9369ec377924d4ffb986e9688e1fb3a5ad26f7e857ed0eeb3c727868755e`  
		Last Modified: Wed, 24 Jun 2026 02:27:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7a3e1eed46f717a8542070752ef647cff8cbce11526659131b241a7d24a74aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc526de6cd12475fa03e128706835e7f6f001294b3100838f46093f4e4315b13`

```dockerfile
```

-	Layers:
	-	`sha256:f1a6d4babe90a309e4c4e479c642501bba916dd07f926d6efbe2b7b51f4203f7`  
		Last Modified: Wed, 24 Jun 2026 02:27:37 GMT  
		Size: 2.4 MB (2368543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d9d86f9a0673d76e9804eac97f9073b910bc300f4bf580939f1402c3bec7a14`  
		Last Modified: Wed, 24 Jun 2026 02:27:36 GMT  
		Size: 17.9 KB (17874 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:47c448af4f9b03796b047e88902126ca3989494143b24faae8ad68a0fd56d3ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.2 MB (213247199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79c5acf50cf557380dbff71aa4d2008d4c185d26aa4f0b1d44f17ecdd7dcda7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 08:15:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 08:15:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 08:15:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 08:15:22 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 08:15:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 08:15:23 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 08:18:14 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 08:18:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 08:18:14 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 08:18:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 08:18:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 08:18:18 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 08:18:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:639e1c13483ea279c94219be2736856262d8dd2efeff3e6d309f11a66aba21fb`  
		Last Modified: Wed, 24 Jun 2026 00:30:29 GMT  
		Size: 33.6 MB (33606388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8411e185f9b4e8882a4fcb58a6e9dae45b9847e5c95ef274b2a91a371cdf3a7d`  
		Last Modified: Wed, 24 Jun 2026 08:18:58 GMT  
		Size: 158.3 MB (158343230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75de90274adf5def47c1b3550b3acc8941ab81e0aabd25a26b4a1f1d1af61f9a`  
		Last Modified: Wed, 24 Jun 2026 08:18:55 GMT  
		Size: 16.8 MB (16781949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf0303e148016823bbb534bd61512f5fbcaaa19badedddc6c5cf0648979e59e`  
		Last Modified: Wed, 24 Jun 2026 08:18:54 GMT  
		Size: 4.5 MB (4515204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708d7929acf8f5f0e90100be702fa28e4b15b6c39b478211a399f53d7c955c14`  
		Last Modified: Wed, 24 Jun 2026 08:18:54 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:52695c1d79cd0c425a073d0818c38d01cf7c4611180e75530423c53f866db857
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2387709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b08d3c88911b598819ebf20c88ea8cc9427fa9120317eabce311a602e48c551`

```dockerfile
```

-	Layers:
	-	`sha256:64347349e1d0bb0cf85522e583faaaf233004125948e2d4469c75b0b3e1c40d1`  
		Last Modified: Wed, 24 Jun 2026 08:18:54 GMT  
		Size: 2.4 MB (2369913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eff0b685bc1519aad179113880f06bcb9f7ba026f22e0bb132891d4025668f49`  
		Last Modified: Wed, 24 Jun 2026 08:18:53 GMT  
		Size: 17.8 KB (17796 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:918016d63be36befdcf93df505ca18936c3eb8d70bbf0d7ba9706945a93a9caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.5 MB (198535268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cba4f03ad09c37ac4089bc8dd40ba7813ffe6ca74b64f93c5ca24563102a0547`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 04:14:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:14:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:14:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:14:49 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 04:14:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 04:14:49 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:15:58 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 04:15:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 04:15:58 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 04:16:00 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 04:16:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 04:16:00 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 04:16:00 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b6a0af2ceb4b698210b8776157288a3fb06e46aaf75d641139449fcc50ce430d`  
		Last Modified: Wed, 24 Jun 2026 00:28:43 GMT  
		Size: 29.9 MB (29851381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e9b13550a9711d1138542940547872fdc415743f8fb5a489f85f7b77c03a57`  
		Last Modified: Wed, 24 Jun 2026 04:16:27 GMT  
		Size: 147.4 MB (147388430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9806f38c3eda771195aa2d2c0a90f28ac6edd94b452d9eab50061e0019a67b`  
		Last Modified: Wed, 24 Jun 2026 04:16:24 GMT  
		Size: 16.8 MB (16779801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bdefdebacd5155b990b419c1e6c044cec1f7651f283b1f7b2ceb0f5e6d73916`  
		Last Modified: Wed, 24 Jun 2026 04:16:24 GMT  
		Size: 4.5 MB (4515228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9003263fb569db8444d566208ebcc08865e5273764487a7dae0b0b75addf94`  
		Last Modified: Wed, 24 Jun 2026 04:16:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fe6028f1aa8d04e518c87dea2655ed3cb8cca67ad7c9a5c36be92149f79244b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2383113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89fae8c73a636a5fabf6ca269ddd3bc32f7b61e3d509563ea5c6a7b0ceaf9851`

```dockerfile
```

-	Layers:
	-	`sha256:30daffb1150b9d0dfc26fc1cd2465c405c9f68e2c8cfcf12bb83d84eb2752025`  
		Last Modified: Wed, 24 Jun 2026 04:16:24 GMT  
		Size: 2.4 MB (2365360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cf32f052ea3a5a9ee3ae8b10b8fd1c3e085a9b5b7252f22564e13c6c87b5a8d`  
		Last Modified: Wed, 24 Jun 2026 04:16:24 GMT  
		Size: 17.8 KB (17753 bytes)  
		MIME: application/vnd.in-toto+json
