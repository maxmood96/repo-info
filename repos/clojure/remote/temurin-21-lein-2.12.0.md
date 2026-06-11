## `clojure:temurin-21-lein-2.12.0`

```console
$ docker pull clojure@sha256:3435cb8a0b61432b0a4aab79efd668aee9fadc9bf0bb47afc9e5e7367fdaf66a
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

### `clojure:temurin-21-lein-2.12.0` - linux; amd64

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

### `clojure:temurin-21-lein-2.12.0` - unknown; unknown

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

### `clojure:temurin-21-lein-2.12.0` - linux; arm64 variant v8

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

### `clojure:temurin-21-lein-2.12.0` - unknown; unknown

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

### `clojure:temurin-21-lein-2.12.0` - linux; ppc64le

```console
$ docker pull clojure@sha256:6829f4f4b2d0e6ccc6359c78526fc6d7780e47617968c11f3186a1dbb020c50d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235241828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a063caa02fb8c600a384fd2ee90933481b853fc5286be90738ca6db63ebe078`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 09:36:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 09:36:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 09:36:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 09:36:58 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 09:36:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 09:36:59 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 09:37:28 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 09:37:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 09:37:28 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 09:37:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 09:37:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 09:37:32 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 09:37:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:88b94a58fac236a778527a3293ccd0ff4d309bff0bf314017ea5af603908fa2e`  
		Last Modified: Thu, 11 Jun 2026 00:21:34 GMT  
		Size: 52.3 MB (52346670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce7fc17844961c443ec6ff9fc6852d7315d0c5de57330a5cd0dd3369a5a4e22`  
		Last Modified: Thu, 11 Jun 2026 09:38:13 GMT  
		Size: 158.3 MB (158343198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8204be212cc166bd859738df61c152376706e2624d3ab3bbb3de85346b2ce3`  
		Last Modified: Thu, 11 Jun 2026 09:38:10 GMT  
		Size: 20.0 MB (20033816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ca09662a628fab044bfc824e7c9cf2139f70d2c9ecfc1ddf855025127ca4a8`  
		Last Modified: Thu, 11 Jun 2026 09:38:09 GMT  
		Size: 4.5 MB (4517716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490f007df31ea351f4c0f14836479e113d7811d6493f0e14ac364964c7f86982`  
		Last Modified: Thu, 11 Jun 2026 09:38:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:be5d4eba1f69d044194fff4b5030ef1740d0691c6ec1aee23a6126118ce33c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4305996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ece4db9bf1b6ed2622bb420322c43f77ebe1a5c6bd8b680a8513de773e6bed85`

```dockerfile
```

-	Layers:
	-	`sha256:02999f4b4ddb8b62169e4fa405f3ebeb70b74bcf65e05554bd2629264001b39d`  
		Last Modified: Thu, 11 Jun 2026 09:38:09 GMT  
		Size: 4.3 MB (4286769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbff1d752bb55743f4b9b35399167ce0766eb4cfb9df4dea62a11a2b6d20a748`  
		Last Modified: Thu, 11 Jun 2026 09:38:09 GMT  
		Size: 19.2 KB (19227 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0` - linux; s390x

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

### `clojure:temurin-21-lein-2.12.0` - unknown; unknown

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
