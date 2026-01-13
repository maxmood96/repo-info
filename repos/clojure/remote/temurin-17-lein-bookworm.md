## `clojure:temurin-17-lein-bookworm`

```console
$ docker pull clojure@sha256:b870123da2c8d64d949c97acb2a7727f9af48a26ed13725fb86517c75fa91829
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

### `clojure:temurin-17-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:4da98cc7c95dafaaf0f4094845f3361c0f5164a55c1876ef10cd0e2c0b1a1343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217649883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b397f17243c6b480cec0cf9889fd491eba261678140daa8c6ebc575fbdd29879`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:57:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:57:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:57:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:57:43 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 00:57:43 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 00:57:43 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:57:57 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 00:57:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 00:57:57 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 00:57:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 00:57:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 00:57:59 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 00:57:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b646c925f63f627dc99a80f05c6e0dac0bfae2a4777f9319eed952d4efd04492`  
		Last Modified: Tue, 30 Dec 2025 00:58:42 GMT  
		Size: 144.8 MB (144847922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3673f93f0e04703cddaac97ff410b75b8c519b18c4823e10df29c85eb3ccb165`  
		Last Modified: Tue, 30 Dec 2025 00:58:29 GMT  
		Size: 19.8 MB (19802979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01513f3b084208e1c2c3cbcd21dee088a8f1c4db83a255c78fd2dac2b5d5f4e4`  
		Last Modified: Tue, 30 Dec 2025 00:58:37 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e508fa022e70a15862c121dfc845d6d904f0fdfc91364263d904885b5e52d1b`  
		Last Modified: Tue, 30 Dec 2025 00:58:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:6199afbb1404bb29bafb102d223da5bc6fe736fb969ef9bf954c11ca24b4150c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4298204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c792301d8da6fed62673460d172ac4c7cda54e3397a391a8299b7ca52419c9`

```dockerfile
```

-	Layers:
	-	`sha256:0ad355fd9432cff13ac2fff0b981aede9536f7b1243cf0a7cad8e9592d84ceb4`  
		Last Modified: Tue, 30 Dec 2025 04:40:08 GMT  
		Size: 4.3 MB (4279836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99ca635c31bed949a842eae7455c86e3e1d386d453c58c4e934a002c09ba4852`  
		Last Modified: Tue, 30 Dec 2025 04:40:09 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:53dcf94550b3a107ea9c06c2a84236233840140c95c270746267ce51882b0990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.2 MB (216189298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6508321bb70b100958e60523687e9289b9a9f37ea96a5184da000407cece2c3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:58:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:58:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:58:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:58:38 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 00:58:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 00:58:38 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:58:52 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 00:58:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 00:58:52 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 00:58:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 00:58:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 00:58:53 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 00:58:53 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a5238db66472033247a1c0252c4398b29acfac523730e3aacbc613881526cd`  
		Last Modified: Tue, 30 Dec 2025 00:59:48 GMT  
		Size: 143.7 MB (143679914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a026aa3b80a314ef3a6cc9b8ad05ab26ebdb781664773b579e18da1a66dba33`  
		Last Modified: Tue, 30 Dec 2025 00:59:23 GMT  
		Size: 19.6 MB (19632084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7082d210758d012e7536b0db395442d0e813f34471aee46e9cfc5284f26f073`  
		Last Modified: Tue, 30 Dec 2025 00:59:21 GMT  
		Size: 4.5 MB (4517724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfea1bc545768b6eb1a857f3cffa683913a3a16877eb3c3d2d0a39f22f7ccc8a`  
		Last Modified: Tue, 30 Dec 2025 00:59:21 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:be8452932b437ebe979944f461ead31a64b3533ed8986109b1b59f24cf0ef8a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4297940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc889a083cb0cfe02a0e07d071f306bd9e43e1e90a08c1e8c3e478c0e9108c55`

```dockerfile
```

-	Layers:
	-	`sha256:8da63473399d0272da9c42212dcb2702cd1fcc18bd8173b65c4a58316bc6d1c8`  
		Last Modified: Tue, 30 Dec 2025 04:40:13 GMT  
		Size: 4.3 MB (4279451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9710259ad531e52e1a172eb19e7bbf83cddc164e7411e50417ff984223dc38d3`  
		Last Modified: Tue, 30 Dec 2025 04:40:14 GMT  
		Size: 18.5 KB (18489 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:95f24da5fedb56449bce89fee2b2448d631baadf34c79ce93a24782b1aee0453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.4 MB (221392073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02e0966d4d6b406ac897a6693318f111fdd7e54aad829b7dc3d1fe489bdb30cc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 01:41:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:41:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:41:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:41:39 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 01:41:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 01:41:39 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:42:21 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 01:42:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 01:42:21 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 01:42:23 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 01:42:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:42:24 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:42:24 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:48e256c4119c0ad256492d6a930e99d2b2d7f8d7920d619aa2de4f616c37076e`  
		Last Modified: Mon, 29 Dec 2025 22:25:39 GMT  
		Size: 52.3 MB (52326998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7a8066a3d82608858f32fca639475eb98fdc4539bc7abe179d1e9964bf731f`  
		Last Modified: Tue, 30 Dec 2025 01:43:10 GMT  
		Size: 144.5 MB (144525257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b47bd4769080259762c4bd1889866d13af3663c7963ee43dc2764daab69eac0`  
		Last Modified: Tue, 30 Dec 2025 01:43:23 GMT  
		Size: 20.0 MB (20021657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fc13860bc60173d46bbaaade93885b1498a439a53caf938b01ec4c5bd82858`  
		Last Modified: Tue, 30 Dec 2025 01:43:21 GMT  
		Size: 4.5 MB (4517732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33ce9148c778549dc2d3512c5ded1b542cbace87d9db6e490fc740e1f2aa489`  
		Last Modified: Tue, 30 Dec 2025 01:43:20 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:68b28b88c0c69c527e3459c8192a5548b43828b38be995d25ceb16d00f01c507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b9beac1eb6fccc3a70c8c50d66759050ece1809e5af3feffecd2277b928b5e`

```dockerfile
```

-	Layers:
	-	`sha256:6a546091332e3ce8ffd0c140fe68f70f7383835c204fe53cec85e585a8dbfec5`  
		Last Modified: Tue, 30 Dec 2025 04:40:18 GMT  
		Size: 4.3 MB (4281695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30693824e40b3eea44dda264231c3ff0deacdd1f22c0d6935c0f189c905ec88f`  
		Last Modified: Tue, 30 Dec 2025 04:40:19 GMT  
		Size: 18.4 KB (18412 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:df645424094ade0db46c3d50984c5f31349287fc63bbd52a170e097298a3d7d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205977724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ba305631f1287ce6621bf3747de817849cac92eb5e04a8713009ed195c516c1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 03:02:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:02:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:02:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:02:05 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:02:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:02:05 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:02:15 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:02:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:02:15 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:02:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:02:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:02:17 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:02:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:533e1723f6efd3a2dac5ef2d710062f1e6292bf061b83d41b908fe862b8922dc`  
		Last Modified: Tue, 13 Jan 2026 00:40:26 GMT  
		Size: 47.1 MB (47138430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377e101c17ebdce9c73b4b044ea0633ed12041cc83ca9e8b72b3585c8ea37029`  
		Last Modified: Tue, 13 Jan 2026 03:03:00 GMT  
		Size: 134.9 MB (134859065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6594db14b4b01ac7a8c5a078e3be785d8d6b4037827cb1828cd8eb4e4e5092e`  
		Last Modified: Tue, 13 Jan 2026 03:02:52 GMT  
		Size: 19.5 MB (19462050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7620172d68ede34d41aa010f6c2d53adbf9c9814a3e63b0d2de417c462f55b1`  
		Last Modified: Tue, 13 Jan 2026 03:02:48 GMT  
		Size: 4.5 MB (4517751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa91d9872c316752736059ae891f73d8a3af66934b8fc72fc37f436051b46aaf`  
		Last Modified: Tue, 13 Jan 2026 03:02:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:68a5cfc0a3502f48164ddc047858f7ced229c3e7c4d72ee036395829edb8156b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4290661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59818b3e52dc0594031fd5f0da458ea62c427ab84fdc5863fd8765e4e55dd002`

```dockerfile
```

-	Layers:
	-	`sha256:2b5dab3e03531ab0b35d487eabc58efa89ee8cc3d45a8dc88768a082dbb31bdb`  
		Last Modified: Tue, 13 Jan 2026 04:37:31 GMT  
		Size: 4.3 MB (4272293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c63cc414a23d9d97b443dc269fcd8360cf2457d2f195fa9e960c739f803a59e0`  
		Last Modified: Tue, 13 Jan 2026 04:37:32 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json
