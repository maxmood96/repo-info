## `clojure:temurin-17-lein-trixie-slim`

```console
$ docker pull clojure@sha256:6a435efd635f8257da5accaaee41963a082cb2341532e66e98e67c82a9e6fdbb
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

### `clojure:temurin-17-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e6c9131c159b204bff0e47d31984abdffd1d1ba4dc977555600bc32dbcafb654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.7 MB (232715389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa06663a9ef238dcfc2d99149581fdcf46a3bbf5241fed676d297bb1fffe34b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3ae34fc80ed56f2b3a9a0b682b58e28e57fe981f5e514c3f687044f4b967608f`  
		Last Modified: Thu, 08 May 2025 17:06:40 GMT  
		Size: 29.8 MB (29753912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d246d5f0b3c94c3da70595d0f566fc2d95bc3c62283a685b4b741038ff43d3`  
		Last Modified: Tue, 13 May 2025 17:53:50 GMT  
		Size: 144.6 MB (144634958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58bd3cefe5f4a714f16e6f5966da58f0a11b07a0c2768505f548c1f5509f807`  
		Last Modified: Sat, 17 May 2025 13:44:37 GMT  
		Size: 53.8 MB (53811899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:052d2ecbd035dd3c32fa313b0d4e1673f9703c78e5c42cf9b825497a9a13050a`  
		Last Modified: Sat, 17 May 2025 13:44:33 GMT  
		Size: 4.5 MB (4514190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c926a0c9e0c35a238d7e0e1b36af7cfaf56066dab0d4df65d01ed63d827a38a`  
		Last Modified: Sat, 17 May 2025 13:44:35 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dfd540be5626e8dcaba705edd404d30250920e5f31e4d359edcd4845d015f1d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4138216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087335893684b5489e1b370fa690d5be6da26416dddaab4baa418df3347f8b2a`

```dockerfile
```

-	Layers:
	-	`sha256:f01b48a86b213aa559c2cecf225b326e94f34a60fb47d9acc24ea6c9df4ddb27`  
		Last Modified: Tue, 13 May 2025 17:53:48 GMT  
		Size: 4.1 MB (4119778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abab748d0b9631d7df44635390f76d66729cd239aa05c2c24857b7d392dd157d`  
		Last Modified: Tue, 13 May 2025 17:53:47 GMT  
		Size: 18.4 KB (18438 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5338a4ef971199cd23e05890ccc11c74e112d36a5ce479c86ff1e0d222f1d2f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (232015186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b02c566e1bfa3b18f554445fa04aaea89d4b1718e63189bfbf49a89ab4b5d2e3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d0342bfffaba1a8be0950e44b5334c6cf9a05d9eedd81a042ec7813ac91850a4`  
		Last Modified: Thu, 08 May 2025 17:31:22 GMT  
		Size: 30.1 MB (30130233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1862c5660d0d55c936747bbb44d2f2a5a6c318c406ceb110d2aac1c4519264`  
		Last Modified: Tue, 13 May 2025 18:01:43 GMT  
		Size: 143.5 MB (143512634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd017f6be823c4e9c360506de222dc4efad1542eba3fab9966df2816abb74759`  
		Last Modified: Tue, 13 May 2025 18:01:41 GMT  
		Size: 53.9 MB (53857690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50d21999b8ac902cdc68150b2c2b1f893af9b9989c3b4cf900ebb6495feab71a`  
		Last Modified: Tue, 13 May 2025 18:01:40 GMT  
		Size: 4.5 MB (4514201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8d2618cc553894dfeab36cf1cf7262685f147fca787b907182c9e5cf106e66`  
		Last Modified: Tue, 13 May 2025 18:01:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:018f04e9c371db48a1a2f1b735f8094785e06d01da9ce5165824a15e55038e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4144039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb421cace5d82aab8f0e10c80b5cbec8780c4d09e716cfe5ac3da1e0e59d6181`

```dockerfile
```

-	Layers:
	-	`sha256:33050b97bfd99c09953866f3f6056c0478107612d8fe87ce5268ccb953c88d4c`  
		Last Modified: Tue, 13 May 2025 18:01:39 GMT  
		Size: 4.1 MB (4125480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:459efaf8cd9c60ac87a80de43849f854877b188b201fd7866590642d0bbd0154`  
		Last Modified: Tue, 13 May 2025 18:01:39 GMT  
		Size: 18.6 KB (18559 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:a53e31ccf863c1104f4ee0d49390d7ab23a873dd7638d58ff3fabbd79481e1df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241248151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e4f478768e4e9eb00864f8b533cf52935b4340498826017a31bd22165c4d4c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a739447e8599431e1e4996b4b6d4022822d37eddea9a3737acbea74b8a860d49`  
		Last Modified: Fri, 09 May 2025 00:17:30 GMT  
		Size: 33.6 MB (33577694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c71ca239809271676c3c02eaf9b6189c986087dbccce9fa3aca9bf1852aa9f`  
		Last Modified: Tue, 13 May 2025 18:59:38 GMT  
		Size: 144.3 MB (144280488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd78421881380ce0ccb53f0a2fd7ffb4d409be2e87f4e9a250366273c954d188`  
		Last Modified: Tue, 13 May 2025 18:59:36 GMT  
		Size: 58.9 MB (58875365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4698931c09759134cf0171dbe93b8ed7c3a02387bf3f04d023e0149d12987e`  
		Last Modified: Tue, 13 May 2025 18:59:34 GMT  
		Size: 4.5 MB (4514175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15a58a63693127695d19f9858e1d21f7a25e8c5c403c7efe33b7ef374fcd1ec`  
		Last Modified: Tue, 13 May 2025 18:59:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:aea8721352764db4bb9a1d01f2a6c4db375b2bc19d788f0f6413601ca0c75423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4142174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f8fb482759582b5b1a029860fe700662d345a9d49cb936d60396d8ef818b05`

```dockerfile
```

-	Layers:
	-	`sha256:a855108490ea06b186edce7187506c9fc8fca3b91b1659185bfe01672f442baf`  
		Last Modified: Tue, 13 May 2025 18:59:34 GMT  
		Size: 4.1 MB (4123692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da46b6945aea9d2bdec93cf407aa8773de3a249ea19a6dae32cea77587d93175`  
		Last Modified: Tue, 13 May 2025 18:59:33 GMT  
		Size: 18.5 KB (18482 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:5168a3bd35b8a494ca2895f0148d1ce0e595d3b48625bfd68c6214a1a64da6ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.3 MB (224271883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3758f09fe2cb028fd8a540aa6ded40eb1403c1dd25b59031c50b372110b4d41`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:facf81ceeaa2f81a0f9ef1ab66d52f94aba08977754588b2609aaf3106342525`  
		Last Modified: Fri, 09 May 2025 06:41:03 GMT  
		Size: 28.3 MB (28251718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aabe73eb42cc2635ac942e3dbc64942a805995a7c9330e4728fcf9f9491a2d8f`  
		Last Modified: Tue, 13 May 2025 18:14:54 GMT  
		Size: 138.5 MB (138492628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11f6be6c937060fc5b38eb26c5dc65da91f4ba16d2ce08f1df82922cd192fda`  
		Last Modified: Tue, 13 May 2025 18:14:43 GMT  
		Size: 53.0 MB (53012881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbae60cd6666ce51ab52e299f3b28de4964a1fd1dd0139e9005f7d0cadf3c92`  
		Last Modified: Tue, 13 May 2025 18:14:35 GMT  
		Size: 4.5 MB (4514227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c133be1af074b94dbdb5ecdd4e5d079a37f726eea4f286db82740e8ec8fe8e3`  
		Last Modified: Tue, 13 May 2025 18:14:35 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ecacd00b9d5842e032dd2e3f8b0d5f13922b7ff69a3115d06c798c3bb2b50f83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4125847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2f4b731995e6a23af2894f566190f38f93bb8e489c1ac6e71351932ce48f6e`

```dockerfile
```

-	Layers:
	-	`sha256:23216c4285ffac30cd1988a66187509252f407e4ba89b99f1aaca3fe1ad9c74a`  
		Last Modified: Tue, 13 May 2025 18:14:35 GMT  
		Size: 4.1 MB (4107366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e28803adf42e74f657331889dbb81c5161beb089ea449df1727784806cf4249`  
		Last Modified: Tue, 13 May 2025 18:14:34 GMT  
		Size: 18.5 KB (18481 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:d8f5a8a323b22bb62ac2af40b9d79171b839cdbab7fb9f038ec57dda20d51ec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 MB (223890328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a9bfa62cbbeb614f7959a8f5cdab545e7d0628126b22c24e4a7e6f82ecb1426`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2efa8ce97d282fc76ea2985fc31102becef655447ddbf9bdd3209771347a0182`  
		Last Modified: Thu, 08 May 2025 17:32:36 GMT  
		Size: 29.8 MB (29825462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b674b6d2790c8572b4f337294d5779bf8394dac4c40b0e834eaff345e3fc45`  
		Last Modified: Tue, 13 May 2025 18:14:24 GMT  
		Size: 134.7 MB (134673562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f63cd8caea23cab5cf0b6f25555444395c8e4a5af2f929142c7201bca69352`  
		Last Modified: Tue, 13 May 2025 18:14:22 GMT  
		Size: 54.9 MB (54876663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:028d0725bb01189f5f32c24ffa2f167680000aac646a1bcd110d97dc530a511d`  
		Last Modified: Tue, 13 May 2025 18:14:22 GMT  
		Size: 4.5 MB (4514213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bce957888af8ede865e1211823b230363a5a3f62c42bb30551e1748e241613`  
		Last Modified: Tue, 13 May 2025 18:14:21 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:092d529603a55304d4edd3ee5f48dd113fd2fff3296babb41cc6e9f383cd53d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4134194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c863bace1213c56570ba2e4802555afddae2d611bc6be18afbbc99533ef298de`

```dockerfile
```

-	Layers:
	-	`sha256:27c57a7a021a4d6946fe1d25714e382ed2ad329f440c031031f9cca0bcdd34c0`  
		Last Modified: Tue, 13 May 2025 18:14:21 GMT  
		Size: 4.1 MB (4115757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:005ac6d7f75a83530ce9648bd73324995d1932958024c3a0dabf17b3ea32b8cf`  
		Last Modified: Tue, 13 May 2025 18:14:21 GMT  
		Size: 18.4 KB (18437 bytes)  
		MIME: application/vnd.in-toto+json
