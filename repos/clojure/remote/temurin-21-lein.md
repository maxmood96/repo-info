## `clojure:temurin-21-lein`

```console
$ docker pull clojure@sha256:eccf3ae7890d650bb4f6edbc0bf7df1c9ed5b190862d0b6209a2a6eab6da0f02
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

### `clojure:temurin-21-lein` - linux; amd64

```console
$ docker pull clojure@sha256:a48f9c96fbed00fd53764e9a3b707ee547cf3952e1a6d6f4f11f76fc095959c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (230992157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e05b8bd8e0ba770bc12662cee8047fd42d5bb94b276616f581ead58db9365634`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:59:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:59:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:59:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:59:16 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 19 May 2026 23:59:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 19 May 2026 23:59:16 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:59:29 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 19 May 2026 23:59:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 May 2026 23:59:29 GMT
ENV LEIN_ROOT=1
# Tue, 19 May 2026 23:59:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 19 May 2026 23:59:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 19 May 2026 23:59:30 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 May 2026 23:59:30 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29dd3908a0cd9dd820bf12d26cbcd1907987d0cbbaceedb1d20671d9d8851e9f`  
		Last Modified: Tue, 19 May 2026 23:59:49 GMT  
		Size: 158.2 MB (158166925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3561af59809982b7021f245e4592852d5ebc598b06984f5b719fed851720845c`  
		Last Modified: Tue, 19 May 2026 23:59:46 GMT  
		Size: 19.8 MB (19811671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9faa91bcc841a9e2b5bfa38dd4aaeeb07430a4f988914f479d588a9160100c`  
		Last Modified: Tue, 19 May 2026 23:59:46 GMT  
		Size: 4.5 MB (4517701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8134c0b28c2106fca0611ca6ec52af97d10673697f653d5136c6517424b1b7b3`  
		Last Modified: Tue, 19 May 2026 23:59:45 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:7f746621b312419f1e7ebd81bd5e1ab22d2931d3266077fae13a3ac540d2dfb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4304050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc8aa8eb01d5ef699e882e9168945fb95a1e99560d478057442e6f7bfee7059`

```dockerfile
```

-	Layers:
	-	`sha256:721a137623ba2bd4495b3494bc233f9dee41dd0f13d93af4882b26c50cfffab0`  
		Last Modified: Tue, 19 May 2026 23:59:46 GMT  
		Size: 4.3 MB (4284878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ed4a9102630b5293a36e5db28579fcc5381a4b1c2d66c6085f17f90fe087b7d`  
		Last Modified: Tue, 19 May 2026 23:59:45 GMT  
		Size: 19.2 KB (19172 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e7f928360d6fbf51f349e82fcddcd62b8a265ecce797e758614c6ad8c7438871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (229000809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4a3bf7673b108f6d3afe5c16dbccc3e5f65ce82083a8f71f22277cbf55443ee`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:06:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:06:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:06:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:06:18 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:06:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:06:18 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:06:33 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:06:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:06:33 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:06:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:06:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:06:35 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:06:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb8876c7ff02ce1bf18d6dbdaf5e50cdd4122984dcb8dc716b8c065401d1c9f`  
		Last Modified: Wed, 20 May 2026 00:06:57 GMT  
		Size: 156.5 MB (156461324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba69d4c081851129c464820ab87371020292368db5ebef409e05860101b8eac6`  
		Last Modified: Wed, 20 May 2026 00:06:54 GMT  
		Size: 19.6 MB (19641909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa7da5e5f02c24f5c9eb5f1581c4e4f8b783a847baf83dc84c91df3b325eae5`  
		Last Modified: Wed, 20 May 2026 00:06:53 GMT  
		Size: 4.5 MB (4517716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1245e6d6da0bb33f0e96f214952aa3d3320d3a59220a9cfe95687d1aab72a6af`  
		Last Modified: Wed, 20 May 2026 00:06:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:af37945402c695f2d453d34624f2f8452b4db0245fc4516b975c65c8a4871e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4303834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c966188ae344a3e2912c620bebaf8e50db7f288d4aa63ae6ba4b62301dde826d`

```dockerfile
```

-	Layers:
	-	`sha256:82b984f08cf247b042927ed7bc3323d6c9741fb16b73d7d66db015af05d820b5`  
		Last Modified: Wed, 20 May 2026 00:06:53 GMT  
		Size: 4.3 MB (4284517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b1f8359a877383e67aa15a47448b16bf5af528e9768ce6d5ebe203ce4a28881`  
		Last Modified: Wed, 20 May 2026 00:06:53 GMT  
		Size: 19.3 KB (19317 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein` - linux; ppc64le

```console
$ docker pull clojure@sha256:319995a13ecb7812b9b1557cd2dd7f326a5ac2c91d6ab4f3a18e3ab737997cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235234819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fae28423af0ed3ad724ce2e9148d05d3c35aa1176b21fd8b0219a514348cd1c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 06:00:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 06:00:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 06:00:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 06:00:37 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 06:00:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 06:00:38 GMT
WORKDIR /tmp
# Wed, 20 May 2026 06:01:08 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 06:01:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 06:01:08 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 06:01:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 06:01:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 06:01:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 06:01:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e7fbe50b4d52434b8ad854b561dba737b35bc2557a57acfb7c49c4490a4b2a`  
		Last Modified: Wed, 20 May 2026 06:02:05 GMT  
		Size: 158.3 MB (158343223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbb01814499907b59bdc239dfde265f0fe71cad24b1d057d8176611155e8045`  
		Last Modified: Wed, 20 May 2026 06:02:02 GMT  
		Size: 20.0 MB (20033227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f430f66719c3a4d89736f371d2b6ea92f4da58b946b5b2334b2fb97d3a2da87`  
		Last Modified: Wed, 20 May 2026 06:02:01 GMT  
		Size: 4.5 MB (4517743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ceee381ba7b860e4b26abb2863715c2d89dbedc33826f3ae71e4c8dbd1ac713`  
		Last Modified: Wed, 20 May 2026 06:02:00 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:66192d6162b66848f88701f1d65a2fcaecf70939d222c4c0ecbf4965afd02121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4305979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9b42194a08bb08ff8c885fcc95db75119722e8196a73e4f693345173302802`

```dockerfile
```

-	Layers:
	-	`sha256:88624b51eef4252e2692d08374311402ad11dbf32f9d5e4540d183182623a284`  
		Last Modified: Wed, 20 May 2026 06:02:01 GMT  
		Size: 4.3 MB (4286751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6346fda29f518feec25687e8ebd2402a581ad7f8354bcab01a7ec78775b78fa8`  
		Last Modified: Wed, 20 May 2026 06:02:00 GMT  
		Size: 19.2 KB (19228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein` - linux; s390x

```console
$ docker pull clojure@sha256:8f4c66ed59bb030e3751a2adac9b267339cc107f9102c917a96f631e6572cda8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.5 MB (218535822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a79f81153a5ab190c9804164c125b8e849679d209d32ee28639a3970fd6c4e56`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 01:45:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:45:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:45:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:45:24 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 01:45:24 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 01:45:24 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:45:36 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 01:45:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 01:45:36 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 01:45:38 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 01:45:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 01:45:38 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 01:45:38 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e0fc2c7a6bb12f7a9b333cc117b6ea5fa5cf251c5fa4dd298303beee01028f59`  
		Last Modified: Tue, 19 May 2026 22:35:39 GMT  
		Size: 47.2 MB (47155589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73860fe658c65ad4a5f7d2de80e6569e6b7acde5efb74aebd17e9384fee084d9`  
		Last Modified: Wed, 20 May 2026 01:46:05 GMT  
		Size: 147.4 MB (147388338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d6512aa0524b44c909eda9c4d73b69e6a89f72c5cef014b63c172946873cf8`  
		Last Modified: Wed, 20 May 2026 01:46:02 GMT  
		Size: 19.5 MB (19473754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7473128da6ec2edddb1e80db5178950e862bb2cd397c10449d0336ab278011`  
		Last Modified: Wed, 20 May 2026 01:46:01 GMT  
		Size: 4.5 MB (4517713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b218458aa7f4d779467329bb455f6050c6bdb07781d00d29bc9f5de7d90ce1`  
		Last Modified: Wed, 20 May 2026 01:46:01 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein` - unknown; unknown

```console
$ docker pull clojure@sha256:485acc4bcb14aebf9b7473608283d660ef2cf51a6c46438ac976ead296506805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4295864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e6606d781111cc2a3b702cdd580750147cf88d89d7aad75268f552c183aa11`

```dockerfile
```

-	Layers:
	-	`sha256:fe291671e83834ec173e8c18807c0bcf4604c7e34563bc199c8bac5f88568c27`  
		Last Modified: Wed, 20 May 2026 01:46:02 GMT  
		Size: 4.3 MB (4276692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5be98fac075e51fba468056a38203fc7d83a46d7532c61406b50c28cd99b9eb8`  
		Last Modified: Wed, 20 May 2026 01:46:02 GMT  
		Size: 19.2 KB (19172 bytes)  
		MIME: application/vnd.in-toto+json
