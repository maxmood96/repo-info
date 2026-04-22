## `clojure:temurin-8-lein-trixie-slim`

```console
$ docker pull clojure@sha256:7e2fd81ca0282ff73f959f997d467f62c2ced31ba8ab53a2b0f53d1133b979f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ed8df04b30f3bfaaee5cc2ed777be92b1fa940fb77dc60f62153e004153885c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.9 MB (105916123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad03fdf47be46af0467ba921ffcf746a0ecb7f8cd920a0ab6734e235bd9c50c3`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:15:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:15:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:15:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:15:44 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:15:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:15:44 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:15:59 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:15:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:15:59 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:16:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:16:01 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d538f1686a5609028a8ad4b470e0f5ce44f124b6b5d607c43b960e1552b18f`  
		Last Modified: Wed, 22 Apr 2026 02:16:14 GMT  
		Size: 55.2 MB (55170118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8eb3ece359f86f2e5a4a8cfcb69d71645417c92fa720b553cbccd761d88e35`  
		Last Modified: Wed, 22 Apr 2026 02:16:13 GMT  
		Size: 16.4 MB (16448070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6031b9a57b91eafe33997aaf524d24da884edcef4090887de65ffc604ec167`  
		Last Modified: Wed, 22 Apr 2026 02:16:12 GMT  
		Size: 4.5 MB (4517729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:23b9a5011799449037a1c834a1284a866882ee78ffe5451ae6d488d4471aa6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2502159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e29118942c49be82dd6eb9e2695f0ba7499f61a40eaae896cf0259844a851fc`

```dockerfile
```

-	Layers:
	-	`sha256:0972655f5ac1dcc3575329bcf48cd37b2dc69b86450130a5fe01687ddb506b3a`  
		Last Modified: Wed, 22 Apr 2026 02:16:12 GMT  
		Size: 2.5 MB (2485777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec3a3379746034ef78c2c443d4429fabeea4bd18538b61bff0bc3737876dcdea`  
		Last Modified: Wed, 22 Apr 2026 02:16:12 GMT  
		Size: 16.4 KB (16382 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:523214243a1810c90fe056d17b61d0e35cd59b25f179a0f1718d7d35fbb56de9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105326915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff4bd264dc10ef4d868f919c69c54afc37f850dabd1edc121b0bfb08ac941368`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:19:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:19:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:19:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:19:14 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:19:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:19:14 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:19:29 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:19:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:19:29 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:19:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:19:31 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99c7e1673659c62daf0e22168054dc6afa147b69aea6eb8104103d09bf4eb8c`  
		Last Modified: Wed, 22 Apr 2026 02:19:45 GMT  
		Size: 54.3 MB (54251614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ec0414744c779d9acf5de1cca44bcc9951880bf8969315d10d2ec96c01c4c0`  
		Last Modified: Wed, 22 Apr 2026 02:19:44 GMT  
		Size: 16.4 MB (16413956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d4bbfc4aea447faa7c831aeafaaf8c152e326264b041c61e41aae86f059d42`  
		Last Modified: Wed, 22 Apr 2026 02:19:43 GMT  
		Size: 4.5 MB (4517707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3a7925f374f8a136f09ae8ab3845b52c2fdc297a0e4ed99b16bf47d8005d7251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2502597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c80a89d3242ad062c5f00ed7c295671bc86fb6acbe32823420c4b4244e2ae091`

```dockerfile
```

-	Layers:
	-	`sha256:3be73b8c106ec50b90fe14906fceefc770f33727629bb90de746c910d2aef9a3`  
		Last Modified: Wed, 22 Apr 2026 02:19:43 GMT  
		Size: 2.5 MB (2486095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a01cbda7abfdcd8564af12153f90cd50dfd1fed8a2428d68a4f8fbff740bdc4`  
		Last Modified: Wed, 22 Apr 2026 02:19:43 GMT  
		Size: 16.5 KB (16502 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:f41b9107b434b99a15691b38596626d965b748a703e0b091e7013b667cb28415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110447622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e81e2a1e764ce9bc11909a8029c90d104b4cb12060ac675f14f8d3cafa7ff0`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 02:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:33:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:33:49 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 02:33:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 02:33:49 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 02:34:32 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 02:34:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 02:34:32 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 02:34:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 02:34:37 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e63a89287f0e4231d910962450035b1c85dad03ac1f8a55f7f7733aa2a3a02`  
		Last Modified: Thu, 16 Apr 2026 02:35:04 GMT  
		Size: 52.7 MB (52650393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72f829bcee7a87453fc38eebf0cb4ca5207f19a1f98f65113beae2cef05016ac`  
		Last Modified: Thu, 16 Apr 2026 02:35:02 GMT  
		Size: 19.7 MB (19686449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff80f9b6a19637731dbc126372881daa458c36d54f1554df94983e608666127`  
		Last Modified: Thu, 16 Apr 2026 02:35:02 GMT  
		Size: 4.5 MB (4517732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1e95a9c91b327702988cdf8616accef59f4083a65b51aff36d508023cd8f34d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2503778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1beaf6ea67650f0e2a68b924a96651feab9d9266341e1195a70f4e08ab556f2`

```dockerfile
```

-	Layers:
	-	`sha256:b93d6eed351b1f9f242b5fe8d40073b8ed985f665b76890d06f1c9149054d60e`  
		Last Modified: Thu, 16 Apr 2026 02:35:02 GMT  
		Size: 2.5 MB (2487352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:007a04765b6aa7120936523799845870297cc907a67425ff387f3dce71de2659`  
		Last Modified: Thu, 16 Apr 2026 02:35:01 GMT  
		Size: 16.4 KB (16426 bytes)  
		MIME: application/vnd.in-toto+json
