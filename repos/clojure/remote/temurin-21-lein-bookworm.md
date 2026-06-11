## `clojure:temurin-21-lein-bookworm`

```console
$ docker pull clojure@sha256:2cb5a9d79c0333a912c493b962cb18e6e43abaec3ab64dc7ad5c36650a0458cf
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

### `clojure:temurin-21-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:7d7f410bc0e1163b7e60d61359de4b9de979b5b31b0d0a2e0e224b683f28b0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231000290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89763b3913f21b4b8fbc453c6eec58465d750064ba70176db6baf4c995538a0e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:19:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:19:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:19:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:19:17 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:19:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:19:17 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:19:31 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:19:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:19:31 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:19:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:19:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:19:32 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:19:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71664a22df42e180e74169e06f93138c4f3b52a0b9a16dfbfe356ab4035ca69f`  
		Last Modified: Thu, 11 Jun 2026 01:19:54 GMT  
		Size: 158.2 MB (158166940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891c2969f5fada326e892c4a847e7f6350d75911eb58dfb3149d6c725d765b80`  
		Last Modified: Thu, 11 Jun 2026 01:19:51 GMT  
		Size: 19.8 MB (19813166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b2d9f962d23c7c26730f457577aa1733d941f0fb37b3c55083354e738ae85`  
		Last Modified: Thu, 11 Jun 2026 01:19:51 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70dad837455c71292c9a5d66f224f68b8a2592e5b44dbf2caad378a3030cbf59`  
		Last Modified: Thu, 11 Jun 2026 01:19:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ef24b26a90ef370c5e980273e05c20a89655adadf977ab00f7bee6e701214603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4304067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd28845cbb72f6d249deb2f8b8cac81bb109d1c910937d13b6357e8375d0bfa0`

```dockerfile
```

-	Layers:
	-	`sha256:6d704f629da5badb28703e5fcb26828732622a53845ed9d3b90cd57dbc490d6b`  
		Last Modified: Thu, 11 Jun 2026 01:19:50 GMT  
		Size: 4.3 MB (4284896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97c21373d9aa3278c5103d0a843b4b7251a9e0b38d9115a0bd049ac26bffa91e`  
		Last Modified: Thu, 11 Jun 2026 01:19:50 GMT  
		Size: 19.2 KB (19171 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a3b4c78dd0ece93e55bc0748c251b5a2330722e55fe6994ff9a4549ac4c99c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (229011498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef058327064549fd6a65354591e47b8d0aa37afceadfa7582e90fe7acaceb98`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:23:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:23:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:23:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:23:14 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:23:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:23:14 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:23:33 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:23:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:23:33 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:23:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:23:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:23:35 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:23:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77e9303ae3f92577d5cda4facc925daeb36f9b1202afe3cbe55c847a00e2e89`  
		Last Modified: Thu, 11 Jun 2026 01:23:56 GMT  
		Size: 156.5 MB (156461281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb7f9a7adaec4af5f97d6f25df1797262f9c3bcc612bb0098a1f63cf6312e93`  
		Last Modified: Thu, 11 Jun 2026 01:23:53 GMT  
		Size: 19.6 MB (19643019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339d7f29b55e7be8bdd434bf7549be6b5097bbd7a7be713386aa82c4a74b2741`  
		Last Modified: Thu, 11 Jun 2026 01:23:52 GMT  
		Size: 4.5 MB (4517752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4168948a9b3d8ad023213361273c11b9a6041cf8bf0f51378f6fbddb62c6b3`  
		Last Modified: Thu, 11 Jun 2026 01:23:52 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8c7b64055cc1259a43208d952b093ac75291c7001e477efe7617e8eedf646280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4303852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac6621448f539af04cf2b897ffaec0c8c5db583c938dc5007f29bd9656c8b51c`

```dockerfile
```

-	Layers:
	-	`sha256:774ab9e24acae407304968e5472b09599d687c347e0eb5b80a86d774355a51ef`  
		Last Modified: Thu, 11 Jun 2026 01:23:52 GMT  
		Size: 4.3 MB (4284535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2244605fd462e43471231673bf7e1eae3239c32f44ea3a79faf31ae31a110b40`  
		Last Modified: Thu, 11 Jun 2026 01:23:52 GMT  
		Size: 19.3 KB (19317 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm` - linux; ppc64le

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

### `clojure:temurin-21-lein-bookworm` - unknown; unknown

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

### `clojure:temurin-21-lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:55a0d8e5cde92564a67b544abd47203e6c7990721e95fd81cd6226448378c2c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.5 MB (218543019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dad2824e3fc75915347a98641a8e35b05ebc4e717596b3c981aeae921a3dca6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 03:11:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:11:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:11:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:11:05 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 03:11:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 03:11:05 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:11:16 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 03:11:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 03:11:16 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 03:11:19 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 03:11:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 03:11:19 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 03:11:19 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b041a55a85cc0e47dd570746852cc1b0fee042f3a03eb250b9f896ac4aa74a3d`  
		Last Modified: Wed, 10 Jun 2026 23:41:01 GMT  
		Size: 47.2 MB (47161500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315e35399e5d4547db2084583fbe80262cce5f385bc84081f625e7edec4d8b6b`  
		Last Modified: Thu, 11 Jun 2026 03:11:50 GMT  
		Size: 147.4 MB (147388354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8178b5f9c48eecd51b5a77801956ab93ea86df6786b647618a74d9df8a8cca6`  
		Last Modified: Thu, 11 Jun 2026 03:11:46 GMT  
		Size: 19.5 MB (19475023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce407c8000121534c7f1e4dd18789bb0058e581cc3b3a70cad3d574618470ab`  
		Last Modified: Thu, 11 Jun 2026 03:11:45 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c76522e97c94b6737567f0d9e79e958dd93ac67bcc52b8bb0da1fa4b605623a`  
		Last Modified: Thu, 11 Jun 2026 03:11:45 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1889e188ac8cb47bc01eed54771f04c374159c3c41d4b758ce3a1fdbb5096305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4295882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14d67155f9e7304929cd79c8a9fed2a30c60eb19b1b2c91d8fad7a5f15f13542`

```dockerfile
```

-	Layers:
	-	`sha256:daf74b1f7de0d5b36847e4cf0a09f6c0351da396bfc10c09bec5271e556ec7f6`  
		Last Modified: Thu, 11 Jun 2026 03:11:45 GMT  
		Size: 4.3 MB (4276710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c344cf2226eb49bc4773e656854c82559f1534aa30bacab07dbc93ac9cabbc01`  
		Last Modified: Thu, 11 Jun 2026 03:11:45 GMT  
		Size: 19.2 KB (19172 bytes)  
		MIME: application/vnd.in-toto+json
