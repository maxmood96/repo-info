## `clojure:temurin-26-lein-trixie-slim`

```console
$ docker pull clojure@sha256:9a5f825d826ef34aa066e815f6b91553583582aae2e5d97cf0b87e627fecf67b
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

### `clojure:temurin-26-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f58c679db6708d2ba7137dd8aed777b83cea7d0614fbb6474305f5c8b3ce815a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.6 MB (145568730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eab373ff9d1f3d91d59ae12a18363e0a5067f58cdf3048ecbabd78652cee1073`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:22:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:22:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:22:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:22:37 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:22:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:22:37 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:23:49 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:23:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:23:49 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:23:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:23:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:23:51 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:23:51 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f5b6cc0fcfc79c342d1936b630c95d9a3b50c050f5c74ed4fb06fd667189b2`  
		Last Modified: Wed, 24 Jun 2026 02:24:10 GMT  
		Size: 94.5 MB (94524331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c551387aa0b06f7a118dac0568731d4c83132d1c21aacd3341737a93da2b04cc`  
		Last Modified: Wed, 24 Jun 2026 02:24:08 GMT  
		Size: 16.7 MB (16743348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1036308514c59733e7f1bb01c9c2d5ad2ef4709dae7721c6eb33ae6b5807086`  
		Last Modified: Wed, 24 Jun 2026 02:24:08 GMT  
		Size: 4.5 MB (4515202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07293f2fe21e4be5e0b12c82c97c326a8ecc57d19ac86b4da9070f97b5fdc8f6`  
		Last Modified: Wed, 24 Jun 2026 02:24:08 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a4a7bf0cbc4dde2d55cc57dc5caede2094f1b04053b948910cdb72ef2264be45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2349718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:608bed0d9ed2fb74f947ced19be002a5338662f963526f85420f85446e48a7ce`

```dockerfile
```

-	Layers:
	-	`sha256:b3be1d069e91cafd91097fb892e0b80d87235395c86e119c9dbc5bae5ac5c6ca`  
		Last Modified: Wed, 24 Jun 2026 02:24:08 GMT  
		Size: 2.3 MB (2331972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28a717e18e029002425c16c9dafb9b316515cc0500aa7d0475fbefcf17172fb8`  
		Last Modified: Wed, 24 Jun 2026 02:24:07 GMT  
		Size: 17.7 KB (17746 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4b702b082a438fdcd677a4a5da9c53cf1715d756edcddc65338a822ccc2a625c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.9 MB (144880192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09a3bae3ae786a5ea2d3e0f1514614030e02f35fd5cb1a47ef59cccfae0cf5c6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:29:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:29:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:29:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:29:27 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 02:29:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 02:29:27 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:30:45 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 02:30:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 02:30:45 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 02:30:47 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 02:30:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:30:47 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:30:47 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c84670bb579c5eb438cc79693e1bcde0d6222ef28699357b17a2857a057ff28`  
		Last Modified: Wed, 24 Jun 2026 02:31:07 GMT  
		Size: 93.5 MB (93504334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14174148a2a8da1dc9e43e44b61142760add7e8faadea4c55c4737502973584a`  
		Last Modified: Wed, 24 Jun 2026 02:31:05 GMT  
		Size: 16.7 MB (16711670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c616b514279747fd5b6c089b11a88ee5ccf17331d50f7e856875d76a505173f`  
		Last Modified: Wed, 24 Jun 2026 02:31:04 GMT  
		Size: 4.5 MB (4515208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e11a0dca487abf69ea985e9a3d40b875b427692a7da901243f0b15c2892b27`  
		Last Modified: Wed, 24 Jun 2026 02:31:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:117cb4ec7015513fc98e16245c98915377ab094adff09c571037f911a681af8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2349446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce089fd19bf5d666b6903e13547d749b4bb7715f17a31a86da0c09f9083140f`

```dockerfile
```

-	Layers:
	-	`sha256:4c7310ad59c5a500aaead57d42e33c0af7a88c5f4ba77f37f9345e05e1803780`  
		Last Modified: Wed, 24 Jun 2026 02:31:04 GMT  
		Size: 2.3 MB (2331579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79e7df9480391639d4c139f7a210cd4e7fcd8e51cd5f48224c6e34380b68c2d9`  
		Last Modified: Wed, 24 Jun 2026 02:31:04 GMT  
		Size: 17.9 KB (17867 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:ed0130bff3a2f94836085042a497c08bb63f4ec18962059403d99584b6cc4a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.8 MB (148806357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f70afe16d66284ccda0ae0022aee99d7b416efc422694127b643eae7b223bb0c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 08:34:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 08:34:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 08:34:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 08:34:39 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 08:34:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 08:34:41 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 08:37:24 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 08:37:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 08:37:24 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 08:37:27 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 08:37:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 08:37:27 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 08:37:27 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:639e1c13483ea279c94219be2736856262d8dd2efeff3e6d309f11a66aba21fb`  
		Last Modified: Wed, 24 Jun 2026 00:30:29 GMT  
		Size: 33.6 MB (33606388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb8abfa12b6427363309b1547420d955191530c07a3fd257bfff14f6647ed36`  
		Last Modified: Wed, 24 Jun 2026 08:38:02 GMT  
		Size: 93.9 MB (93902053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121e9cb76324b6e363cbd6334c47fbce725d35f9595edb23da6336ea24e432e1`  
		Last Modified: Wed, 24 Jun 2026 08:38:00 GMT  
		Size: 16.8 MB (16782269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dd2bc1677fb2101841f53d788e9757882286a8c037d6d6d7f8fbcd0f67553a`  
		Last Modified: Wed, 24 Jun 2026 08:37:59 GMT  
		Size: 4.5 MB (4515218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dfea94b37663b7bd2ce53fee57b4f7b76a4388dc691e6ed2c8bba6adaea88ff`  
		Last Modified: Wed, 24 Jun 2026 08:37:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7b33533ae12bcc7e7215931bc1492abecb13b8e017ed4687ebc395c571d5dc30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:503d5a9356f23a24e2e4da33ef9cfbb476445a1ac5e0847ad919759944d4a4fb`

```dockerfile
```

-	Layers:
	-	`sha256:4c5f3525719fe2359f00e3208fb604eb5cbbd09e71121b2ad9dd5ff8690acaf7`  
		Last Modified: Wed, 24 Jun 2026 08:37:59 GMT  
		Size: 2.3 MB (2316888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77d11647ae62385cc6672e12549d6f6150d8a171be6f782154c6c59bd9c9f5bc`  
		Last Modified: Wed, 24 Jun 2026 08:37:59 GMT  
		Size: 17.8 KB (17790 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:d07742b289425e7763d9edc4b2d24eab3e2628bdbfc3cba20b9430be4bfe2746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141683709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d147e1e31241a3ae4bd89dcd9d48578a818d5ffb857dfe7dfffc190bd312b7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 04:20:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:20:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:20:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:20:27 GMT
ENV LEIN_VERSION=2.13.0
# Wed, 24 Jun 2026 04:20:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Jun 2026 04:20:27 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:21:34 GMT
RUN set -eux; apt-get update && apt-get install -y maven git gnupg && rm -rf /var/lib/apt/lists/* && export GNUPGHOME="$(mktemp -d)" && export LEIN_ROOT=1 && mkdir -p $LEIN_INSTALL /usr/share/java /root/.lein && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && git clone --depth 1 --branch $LEIN_VERSION https://codeberg.org/leiningen/leiningen.git && cd leiningen && git verify-tag $LEIN_VERSION && [ "$(git rev-parse HEAD)" = "d703e4802feb3e5c3fa9ae9f1874fb7a3a3e3030" ] && ( cd leiningen-core && mvn -B -q -DskipTests install && mvn -B -q dependency:build-classpath -Dmdep.outputFile=.lein-bootstrap ) && bin/lein uberjar && install -m 0644 target/leiningen-$LEIN_VERSION-standalone.jar /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && install -m 0755 bin/lein-pkg $LEIN_INSTALL/lein && gpgconf --kill all && cd /tmp && rm -rf /tmp/leiningen /root/.m2 "$GNUPGHOME" && apt-get purge -y --auto-remove maven git gnupg # buildkit
# Wed, 24 Jun 2026 04:21:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jun 2026 04:21:34 GMT
ENV LEIN_ROOT=1
# Wed, 24 Jun 2026 04:21:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.5"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 24 Jun 2026 04:21:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 04:21:36 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 04:21:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b6a0af2ceb4b698210b8776157288a3fb06e46aaf75d641139449fcc50ce430d`  
		Last Modified: Wed, 24 Jun 2026 00:28:43 GMT  
		Size: 29.9 MB (29851381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb4490279375ef221a99da6a4e5907fc8759368ec38edca67792d9dd2d7925f`  
		Last Modified: Wed, 24 Jun 2026 04:22:03 GMT  
		Size: 90.5 MB (90536937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d1672c580035fdfa11e93af3a301e13713348879e8ef8fa2bf2c0930ac33fb1`  
		Last Modified: Wed, 24 Jun 2026 04:22:01 GMT  
		Size: 16.8 MB (16779738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42a73c77e144bd6ab311a48a6c570e5286c5cb7fa4af2c14d2945329c8982d7`  
		Last Modified: Wed, 24 Jun 2026 04:22:00 GMT  
		Size: 4.5 MB (4515225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e663c9818b03ee5a8dabb60316dc2c398c1866cf21c0a7b67d4c57e7fce8e3c5`  
		Last Modified: Wed, 24 Jun 2026 04:22:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8b88c8b6dabf1b36d255e5932414883b92f34db6e2081f88f03ca86072f965b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2331330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ccca1041313440b3c6ca7c3a9420052d748dc9ccbfdc70e92f456708bd114cc`

```dockerfile
```

-	Layers:
	-	`sha256:9e66eaea2a5af906c03809f3a02da4ae9d16fd654eca2c78f2eb58dd19a7f6a9`  
		Last Modified: Wed, 24 Jun 2026 04:22:00 GMT  
		Size: 2.3 MB (2313585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c8e3d651dca9a2faf62ac81ae8da21038ed7dc0d1290e887521376b23f39346`  
		Last Modified: Wed, 24 Jun 2026 04:22:00 GMT  
		Size: 17.7 KB (17745 bytes)  
		MIME: application/vnd.in-toto+json
