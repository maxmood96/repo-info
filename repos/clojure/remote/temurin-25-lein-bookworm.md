## `clojure:temurin-25-lein-bookworm`

```console
$ docker pull clojure@sha256:5a212616965eb0a292251ca9437caa11714ea91aebdf2c3c10b35f4db033b1ed
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

### `clojure:temurin-25-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:242996f5db9d1a3ddd530459aaf6325729d8cece7aeb3ddfe68e83d8d4584859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.1 MB (165069823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f58b02a520b54c186bbd106ab467e284e95afd152d6e7b89b51c2209327bcfd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:06:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:06:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:06:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:06:00 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:06:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:06:00 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:06:14 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:06:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:06:14 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:06:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:06:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:06:16 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:06:16 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc34deaa582fcba22b40df8c8f4a60503cb7e0251579f70bc87e97173833b79`  
		Last Modified: Wed, 15 Apr 2026 22:06:35 GMT  
		Size: 92.3 MB (92256332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff03364cc8471dd8256b5df70b44ee5b9d851ad07fa751e178036d88d5e30b1c`  
		Last Modified: Wed, 15 Apr 2026 22:06:33 GMT  
		Size: 19.8 MB (19806499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603e35eb8845d8afff5920e4fd879a393bf99c02f2db335e225f31a37430266e`  
		Last Modified: Wed, 15 Apr 2026 22:06:32 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979e58a3af91e8d8e3a9bb40e30ab6755da24a322e4349475676ff62d269afbe`  
		Last Modified: Wed, 15 Apr 2026 22:06:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d8db754f77813d7c211d283f1ca7a99898919f282a424445b8103200e3007ed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4271286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dec49f192a4ad4faff1c478368ae23144e8bc535c9aee9c25f3e0b502280987`

```dockerfile
```

-	Layers:
	-	`sha256:6b50f4ff7eb22157f00d297f9819890f60e5e90f338daff607c032ea651b954c`  
		Last Modified: Wed, 15 Apr 2026 22:06:33 GMT  
		Size: 4.3 MB (4251027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a17428985d09651dc667d6e24c17df77c69dd707f874014408b3d4249f63553`  
		Last Modified: Wed, 15 Apr 2026 22:06:32 GMT  
		Size: 20.3 KB (20259 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:66ced419d4c6f6647d19be2d3cb1f42e795cde692d708cfca536b6001bb74c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.8 MB (163816651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da0a31565c99cb381357c4a5ac772a25ac212df7dcb8178d03409a8977e6d3e0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:17:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:17:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:17:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:17:34 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:17:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:17:34 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:17:48 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:17:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:17:48 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:17:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:17:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:17:49 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:17:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b6d0db9dd7bf526a236916418ed4fc1d1063f4d5b1ff5524e6a988deb3c4c4a`  
		Last Modified: Wed, 15 Apr 2026 22:18:08 GMT  
		Size: 91.3 MB (91288275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9aa6f813fbabd45f779784df40667dfcad9a717a7bd8c8188f4062aa1655c95`  
		Last Modified: Wed, 15 Apr 2026 22:18:07 GMT  
		Size: 19.6 MB (19636973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bff5cebafb096a55030ccc8d82d4100311e10c6bd41ec9b656867feb7f2d45c`  
		Last Modified: Wed, 15 Apr 2026 22:18:06 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7067443c8bbbec035d5bd38fe15755e6f4919d3fe60cf13708986f84e437dadf`  
		Last Modified: Wed, 15 Apr 2026 22:18:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:cf83ab22b77fcf6c1378862236bcff3b38d9f607350235dd45eafb966ac22938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4271163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9264531a69af3ef9e9d2e234d22565c191f2e78328320df9857570e222918f3`

```dockerfile
```

-	Layers:
	-	`sha256:65224c30940a6c15c72b2cbbdd812d64e1c8adc02238df80c738290796a35c4c`  
		Last Modified: Wed, 15 Apr 2026 22:18:06 GMT  
		Size: 4.3 MB (4250711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93b5a729d9779cff9062cd559f12f97c41aa00f0d88f6eff8e215d345d8e844a`  
		Last Modified: Wed, 15 Apr 2026 22:18:05 GMT  
		Size: 20.5 KB (20452 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:c58692c5fc493124ab3a9dd290c1cc42d5cfdf565b548eade041722a4d4c353e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168511912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d79b9623517abbd30918de57917f027c8861cc1832ba666ef357ac773fd91422`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 14:18:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:18:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:18:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:18:46 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 14:18:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 14:18:46 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:19:19 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 14:19:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 14:19:19 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 14:19:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 14:53:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 14:53:08 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 14:53:08 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d37828c75dd85ae1dfea53ab4854b6b0d30152c9a1fa77b22f23ecfe7b3ca4a`  
		Last Modified: Tue, 07 Apr 2026 14:21:10 GMT  
		Size: 91.6 MB (91633006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4bc93c9840ce4b21d184ead1de55d042e190180a69ae68a6d42f7252bba52af`  
		Last Modified: Tue, 07 Apr 2026 14:21:06 GMT  
		Size: 20.0 MB (20023784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5917b0bed8dc348fbecd021570abc3cde637ad10b82be291fae70f1e32b8dad2`  
		Last Modified: Tue, 07 Apr 2026 14:21:06 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b5c0486059204c6833b4404ee0182eee07999ecb57fb200327630e726b15b2`  
		Last Modified: Tue, 07 Apr 2026 14:53:24 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4421fac82d84546fab4a38da62bb3ea668016792cda63cd7fae15db8ad1886b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4256575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1349563721a9016e5b0a5db2b99509e3e4d10a01b7357b33af8167267ceb664`

```dockerfile
```

-	Layers:
	-	`sha256:2bbb2c2cd59054e9664b905f5293a9b03c4cf010572adccd1f69ca7b23ae42e1`  
		Last Modified: Tue, 07 Apr 2026 14:53:25 GMT  
		Size: 4.2 MB (4236236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2e229cef3b587670ae4fc6c7fc6faaecf2bfc3738360cd751eba61b3a8d5fd8`  
		Last Modified: Tue, 07 Apr 2026 14:53:24 GMT  
		Size: 20.3 KB (20339 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:66c18bef94d84e9d704594989cc4862eecc68a80fcef8ea630853b5d3a956b32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.4 MB (159363271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2434e4437dae3cc3cfa77eeafd6f925c0f1aaa19fcf91cf6af511461a1b98a92`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 05:38:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:38:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:38:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:38:40 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 05:38:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 05:38:40 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:38:53 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 05:38:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 05:38:53 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 05:38:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 05:46:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 05:46:25 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 05:46:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:40ecbf1d4e17f6b072e6cef463823baec601d9f21c9dc33d98bd258448a986f6`  
		Last Modified: Tue, 07 Apr 2026 00:10:32 GMT  
		Size: 47.1 MB (47148084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6336049cfea2fb1bf6fe937dfa06a3231de1bcd109cc0d07cc3ba41fd378402`  
		Last Modified: Tue, 07 Apr 2026 05:39:45 GMT  
		Size: 88.2 MB (88233804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94d5138627d9e4edb404122d05597758714dcab9e5b88c41aa2fe814dd04b85`  
		Last Modified: Tue, 07 Apr 2026 05:39:43 GMT  
		Size: 19.5 MB (19463188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c53efa365a3be02bd634a88ae7bd02b5fa2c28b559bb0375684b4319d37eee`  
		Last Modified: Tue, 07 Apr 2026 05:39:42 GMT  
		Size: 4.5 MB (4517767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0f7d62fd23c30452c16a29ff17b1dc20dfb8f6ca89a10360d33b68e96bc47a`  
		Last Modified: Tue, 07 Apr 2026 05:46:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:eaf792a2933e69826856e055815187a06c2945c67c87e4f1a884a6ac0aa6482e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4247662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94fb3ad3bd67f68136a5552d0928289357f5211ca58a927f64d07e6abf51ba49`

```dockerfile
```

-	Layers:
	-	`sha256:f4840977f44d427da0e3c3de5a7a72b6487c6404dd3c3a203d406b4dffb9a2a6`  
		Last Modified: Tue, 07 Apr 2026 05:46:39 GMT  
		Size: 4.2 MB (4227403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bed1c66d1f655fc2792fa7d2bc17515b9f65202cac83e3815df1d61c4d61b36`  
		Last Modified: Tue, 07 Apr 2026 05:46:38 GMT  
		Size: 20.3 KB (20259 bytes)  
		MIME: application/vnd.in-toto+json
