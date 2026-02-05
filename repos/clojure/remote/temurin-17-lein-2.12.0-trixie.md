## `clojure:temurin-17-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:505a93fa4e699fe12fe270ca9b1323a5f5adcc108b6e6e4f9d81791599407734
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:707bf7626839916915edd0a89e382cf660dfad5fc1c8afe940288fa816246cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 MB (217239180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2814602ac233f59b4ba1870b8efa75c359d193e1d5a0933f0dc999cc1158fbc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:20:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:20:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:20:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:20:21 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:20:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:20:21 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:20:39 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:20:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:20:39 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:20:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:20:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:20:41 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:20:41 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fcf6d6cb3555cf374b8a09a171ce43706e83f88bfa269672bee4b898004ac22`  
		Last Modified: Tue, 03 Feb 2026 03:20:54 GMT  
		Size: 144.8 MB (144847906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7396b5b81ace1a3c4f0643ae3a6eb0f3d35451b5999fd1848e41f61a26df76a7`  
		Last Modified: Tue, 03 Feb 2026 03:20:58 GMT  
		Size: 18.6 MB (18580140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e88577f5605bbb9e109ae290f966f1952a81221c0546484607ad481a74feaaa`  
		Last Modified: Tue, 03 Feb 2026 03:20:58 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a468deb34991af8de42777235ed632e9931d10b2ee14200287a9d36698cf05`  
		Last Modified: Tue, 03 Feb 2026 03:20:57 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3ece8c586ca5bd617b347003e53ef0a5b6ca7c61d9a18ab7f29ab51d20bef649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3832591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e7fb1804ec970b16a7638b97f8a22c086b1b6d1f70192d5ffed6b4875c4c52`

```dockerfile
```

-	Layers:
	-	`sha256:d7359c0dfcedbe918f4dcfec0e39e86265de0c07acff6adba2f6010fb2b33e1d`  
		Last Modified: Tue, 03 Feb 2026 03:20:58 GMT  
		Size: 3.8 MB (3814239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9111324f88e42c2913240039f43300aeca5288d258c847f598eba651e0d1523`  
		Last Modified: Tue, 03 Feb 2026 03:20:58 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:44ea478b2f4a0374402d01b6830508328837738bbaeb2aab4d3a3796347b411d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.4 MB (216391599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9043e16efea340ab94e689a2e7c65c9d7379be6e1750cd9a06a122b5d1c0fce3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:23:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:23:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:23:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:23:00 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 03:23:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 03:23:00 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:23:17 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 03:23:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 03:23:17 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 03:23:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 03:23:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:23:19 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:23:19 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1e7eb8766a332e5fd2f1c0233c2799b48bd6207af24e668730b484bc6b152e`  
		Last Modified: Tue, 03 Feb 2026 03:23:39 GMT  
		Size: 143.7 MB (143679932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a74a1fbda2eb08bf92d1317069111195b8a6eae3939634c239f6f8d35d990db9`  
		Last Modified: Tue, 03 Feb 2026 03:23:37 GMT  
		Size: 18.5 MB (18541509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964349f8322f0027a1e93657b84bbad3cdc59e029cd163a7d69efd75f4b9b4c5`  
		Last Modified: Tue, 03 Feb 2026 03:23:36 GMT  
		Size: 4.5 MB (4517711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b1e00d1b483832b27ab970af6edc0e81bdb309c0e5a3392e4f3198f526b0e2`  
		Last Modified: Tue, 03 Feb 2026 03:23:36 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:88b53bf44deda0ff97e37e0c4a48e3b788bcbeab24dd505afe3357dd6ac2878a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3833589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2879345bec8048d90128056a1a98093b983f04b4f5a3120fe84679f6eaca25a6`

```dockerfile
```

-	Layers:
	-	`sha256:fe0366d284c749f29373196a3100d5f1eed309f3fe0516762da3fffa21e2b507`  
		Last Modified: Tue, 03 Feb 2026 03:23:36 GMT  
		Size: 3.8 MB (3815116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:badfa43f0f87b86648cd8d44566a149c98cd885e3d584c84085ab67f3d3c951f`  
		Last Modified: Tue, 03 Feb 2026 03:23:36 GMT  
		Size: 18.5 KB (18473 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:7c363de1fd630ba5d3919819d982e226ab9454a5750b91fd54e103107bee9c36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220792490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a0e582933cc10346c0c665175d4dd577341445dee058b21b8dec5e18c058fe`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 09:41:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 09:41:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 09:41:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 09:41:44 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 09:41:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 09:41:44 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 09:42:20 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 09:42:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 09:42:20 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 09:42:23 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 09:42:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 09:42:24 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 09:42:24 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba372745a3f66503d172e659feebce952b517e572b656ca7ad4427c81440823`  
		Last Modified: Tue, 03 Feb 2026 09:43:13 GMT  
		Size: 144.5 MB (144524726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c44424bace0498307b563b2946a4af6d4f7f1ff50390c9c8bf98780c7e8fe1`  
		Last Modified: Tue, 03 Feb 2026 09:43:10 GMT  
		Size: 18.6 MB (18637468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec713bd749f8e61fddb30140d7a33380c8a564ce19a600e9b1c99fd5bd29bdd`  
		Last Modified: Tue, 03 Feb 2026 09:43:09 GMT  
		Size: 4.5 MB (4517752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceaee02239fef7d4d51b0ba7c03be5dbad5e1d54b22249a7081f482715affc28`  
		Last Modified: Tue, 03 Feb 2026 09:43:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:65fc7ce5f13ca408bc4cbc88330d50d9ea50c79228222f476f0e53394168cd45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3833635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dace21038f8bb237a6b759dea4001d4c77b0db09b2e6b48787ad0580a50fcfdc`

```dockerfile
```

-	Layers:
	-	`sha256:ba3f7b93f27aaaa8b4ddca29ba1eddfc4d803baa6baa482085798639252a3fc5`  
		Last Modified: Tue, 03 Feb 2026 09:43:09 GMT  
		Size: 3.8 MB (3815239 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35fbf8e59c627a2877d6e51037efc0c74897b21c111384cc1b1500315fd75c7f`  
		Last Modified: Tue, 03 Feb 2026 09:43:09 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:401e3ce48270dd4bbf160daabe320e7e794b87b0ea64f0cb2a84f8e92294d9ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.7 MB (212716454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280bee791cf7be4c31124e5e18ef9068808a7038d4325acc1bee40ce17232fee`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 20:13:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 20:13:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 20:13:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 20:13:51 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 05 Feb 2026 20:13:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 05 Feb 2026 20:13:51 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 20:16:15 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 05 Feb 2026 20:16:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 05 Feb 2026 20:16:15 GMT
ENV LEIN_ROOT=1
# Thu, 05 Feb 2026 20:16:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 05 Feb 2026 20:16:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 20:16:33 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 20:16:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:618efd37f74728f7dcba60c231fad7f2d777dc65e4da32d0adae5e032e1fd125`  
		Last Modified: Tue, 03 Feb 2026 07:13:10 GMT  
		Size: 47.8 MB (47776763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8715f0f462c27c39b67aba65879f61c571d7691a6bbfdcec6aed27eeb28ae68`  
		Last Modified: Thu, 05 Feb 2026 20:20:41 GMT  
		Size: 141.9 MB (141889578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39f4bda650cfdcfae48ee2e1ff7d18298a1d3bbb859a11cf4bca3d174e926fe`  
		Last Modified: Thu, 05 Feb 2026 20:20:24 GMT  
		Size: 18.5 MB (18531887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185666daa5d6540a047c9ce44bc731d33aa468da2e5aae3854a6b78042552413`  
		Last Modified: Thu, 05 Feb 2026 20:20:20 GMT  
		Size: 4.5 MB (4517795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28481884be0a4f341ec9b041b03cc78e4e2180bed88e86bd78edf33d89bfc10f`  
		Last Modified: Thu, 05 Feb 2026 20:20:17 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a685245080defba5fb10a558aa8f0739061735dc6b5545d6453f9009a333024a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3821193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a15fed9ae6a458efd330526c6d6f8495c8bf004655e4cffbb40441a7b80f3af`

```dockerfile
```

-	Layers:
	-	`sha256:a60676cac8a59e35f063575ffe855f2eac5c3d6e5b3c5a369f798f94493cc09b`  
		Last Modified: Thu, 05 Feb 2026 20:20:19 GMT  
		Size: 3.8 MB (3802797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a6e29abffd531221836d3d9419cbeb4995a16b9da4af94df103631f41ce672`  
		Last Modified: Thu, 05 Feb 2026 20:20:17 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:163ce8d369c57a91846c64ffb8f4b26aee369ec6becec44d2124d769174ed7c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.4 MB (207353364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c39c11c647a48da919172ed8a992431caa61d022149c1a6be3ba7df3bf10471`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 05:02:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 05:02:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 05:02:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:02:00 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 03 Feb 2026 05:02:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 03 Feb 2026 05:02:00 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:02:12 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 03 Feb 2026 05:02:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 03 Feb 2026 05:02:12 GMT
ENV LEIN_ROOT=1
# Tue, 03 Feb 2026 05:02:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 03 Feb 2026 05:02:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 05:02:14 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 05:02:14 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0521af9429b24592bd981b694df00f2d02ab05a0bbb63192b66fd3a113c887f`  
		Last Modified: Tue, 03 Feb 2026 05:02:39 GMT  
		Size: 134.9 MB (134859772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb775aaffc3678941b32619acc50369476f95f6b1b2b3e689e5e2e10b968e2e`  
		Last Modified: Tue, 03 Feb 2026 05:02:37 GMT  
		Size: 18.6 MB (18621037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9297b5a18be3013f48e22bcf11cbe69aa90b881191f748353be6170f772f10f`  
		Last Modified: Tue, 03 Feb 2026 05:02:37 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ccdca359c7a5225df526c919d49bfdf6f043f91ec126af28b6eba43fd12d286`  
		Last Modified: Tue, 03 Feb 2026 05:02:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d6e646d5fa499f93f2c8abd80554f11443fb22baaaa97e4917cba03187826deb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3829018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f1ef5caa90d7c97df85a182b8772fdcde771909ac8e9fc72793356e32fe19d`

```dockerfile
```

-	Layers:
	-	`sha256:96458bafce479238e9867b3f0af22d5e150a037ec12b7f8f3cc7dbc4841c857f`  
		Last Modified: Tue, 03 Feb 2026 05:02:37 GMT  
		Size: 3.8 MB (3810666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ebe1b07d83a7a1c732e4343edc333adfabf834aca1e4a9ef2515df98ce4087a`  
		Last Modified: Tue, 03 Feb 2026 05:02:37 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json
