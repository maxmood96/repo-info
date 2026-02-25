## `clojure:temurin-25-lein-trixie`

```console
$ docker pull clojure@sha256:789ac56bdd91673d9fcc2533c9edf85ff57d22df1d3a8fba4919e225614c0959
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

### `clojure:temurin-25-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:baacd64c5e152d28fc3582a8914f23aacf8c7cfebae9b08930006ee18427c6ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.6 MB (164647599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b22375a520632574cc569567abdbc9b5c8492bf5ea247127beaa7cc217aa9994`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:57:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:57:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:57:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:57:07 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 19:57:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 19:57:07 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:57:24 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 19:57:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 19:57:24 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 19:57:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 19:57:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:57:25 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:57:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bdaa5ae7f8607c3b0f2f20a05eb7deeb64caa1874f569103af7825749c2e4a`  
		Last Modified: Tue, 24 Feb 2026 19:57:44 GMT  
		Size: 92.3 MB (92256297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20a3ac59aeb52f777933f7442efdf773c4b3d5972065566e760c128d86f7bbf`  
		Last Modified: Tue, 24 Feb 2026 19:57:42 GMT  
		Size: 18.6 MB (18580041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02898894494a2e641a9f61046d17c7573460d1def07371538c496f9757df3e3`  
		Last Modified: Tue, 24 Feb 2026 19:57:42 GMT  
		Size: 4.5 MB (4517710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32d5bb3f31a565e9baba53f659530cd5a0811c0df3dd8b16f16e5cc5f1abd24`  
		Last Modified: Tue, 24 Feb 2026 19:57:41 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:61b00e72c3fd022abc9f9f0bb6480da004c5172f863b2902b297a0b0e5c90649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3802502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6095de46af9b2d34e23029624cde3238c4cb3e21f58cbca59327e65f23586435`

```dockerfile
```

-	Layers:
	-	`sha256:84b528fe85fd264e076fc99b35a0a4ac7ea5ff51e5314b02a2134a6e1eeb98fb`  
		Last Modified: Tue, 24 Feb 2026 19:57:42 GMT  
		Size: 3.8 MB (3783523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb3ad4cc7d04a700354beb586cdc5e72dce9703e3cb78005f01cfcac5d143201`  
		Last Modified: Tue, 24 Feb 2026 19:57:41 GMT  
		Size: 19.0 KB (18979 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a6162ece27c1cbdec71e4d15979748ddc31e8407046cdeefd505a5d4d21b36cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (164000066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547cd2cfdc42d24ae0f7a1379bf40107d32577f25b32d0b5a4f2020a7d7a4767`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:07:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:07:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:07:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:07:36 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 20:07:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 20:07:36 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:07:53 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 20:07:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 20:07:53 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 20:07:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 20:07:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:07:55 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:07:55 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6d0193859402b46e871b8e097f8c9cd87d98e701d50734e47de49502b6e828`  
		Last Modified: Tue, 24 Feb 2026 20:08:13 GMT  
		Size: 91.3 MB (91288263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652fc95e87473cdeb7fc6dc2818c197f03b146e699f9f21672ffc9b48973ea37`  
		Last Modified: Tue, 24 Feb 2026 20:08:11 GMT  
		Size: 18.5 MB (18541462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6231906259dbaa6120ab704bbf9e36c3f8c41d8528c18e023a77dc0c20dc8dd9`  
		Last Modified: Tue, 24 Feb 2026 20:08:11 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b5bc2163fd53455af236d089700d9d7f74a9aa81b57edda5384f6f218ffbf5`  
		Last Modified: Tue, 24 Feb 2026 20:08:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b835058b5c2114132cc9bdcab52499f6af11fc8b7b49e9b5d595e53728f5f205
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3803545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5150305f75ef6c99006a59b8cb8ad5c075dc3d3feb31b0c38505cda2cf728cb4`

```dockerfile
```

-	Layers:
	-	`sha256:a3f288c7ca7c2a00d9f7b923e766c8014cc3df18185bb6be62ed9c7d5f249fa1`  
		Last Modified: Tue, 24 Feb 2026 20:08:11 GMT  
		Size: 3.8 MB (3784421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4c9136a44a604d9e27cc26de29c69f891297e4969bda23b7e2fdda32c0dfd87`  
		Last Modified: Tue, 24 Feb 2026 20:08:11 GMT  
		Size: 19.1 KB (19124 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:e1f4c2abe183bfd38e2e68c99df00fc0c03f5b86dd7f395f638d22e2fe10ca6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.9 MB (167900787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc304254a82c553b039ac9fbaf05e743203a0b051b6f6af518d752b34b99e349`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 02:14:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 02:14:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 02:14:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 02:14:50 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 25 Feb 2026 02:14:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 25 Feb 2026 02:14:50 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 02:15:31 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 25 Feb 2026 02:15:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 25 Feb 2026 02:15:31 GMT
ENV LEIN_ROOT=1
# Wed, 25 Feb 2026 02:15:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 25 Feb 2026 02:15:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 25 Feb 2026 02:15:35 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 25 Feb 2026 02:15:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898bd9db475a819ec030b333968ed33ad54a305029d5289784462edd831f227f`  
		Last Modified: Wed, 25 Feb 2026 02:16:20 GMT  
		Size: 91.6 MB (91632903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe49b28e243877fd9506758852f14f53e8c766dec765cadb8c0a8407c14cd7b`  
		Last Modified: Wed, 25 Feb 2026 02:16:19 GMT  
		Size: 18.6 MB (18637443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729b5abc8709dc1d1217ef637b73b8092397b5e1e43dcb443f913247bbe20b68`  
		Last Modified: Wed, 25 Feb 2026 02:16:18 GMT  
		Size: 4.5 MB (4517751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9182811bdb0bf6412ad694524bc3f4c34fe2e412da9c3b74feeef5d05975ce92`  
		Last Modified: Wed, 25 Feb 2026 02:16:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:86cb8228c421d501c8c23bb450d32c0b76fc4597ce259506f752043f03ddd4b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48152d4aaf870cbd08dfb8f6298416721c7d20defe62e80b4fef6e571a95e767`

```dockerfile
```

-	Layers:
	-	`sha256:83192634636cbf0e497144027e60d58c9548ad7fea32d7074b54f7204c9a8b4c`  
		Last Modified: Wed, 25 Feb 2026 02:16:18 GMT  
		Size: 3.8 MB (3767847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:773746993e81c99af48e12a94229f35daa0376c933078e4d6dffa2c303e86765`  
		Last Modified: Wed, 25 Feb 2026 02:16:17 GMT  
		Size: 19.0 KB (19035 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:6936cdcf8c4843c1f70d8bcd100bc8f7ffd015b4f30bfeaa136a23c818bccc6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.6 MB (161600266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:482a82f70071da5da9a76115ea6cfca465a52576b121e785e7d6c475cd309a83`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Wed, 18 Feb 2026 11:49:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 18 Feb 2026 11:49:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 18 Feb 2026 11:49:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Feb 2026 11:49:18 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 18 Feb 2026 11:49:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 18 Feb 2026 11:49:18 GMT
WORKDIR /tmp
# Wed, 18 Feb 2026 13:12:16 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 18 Feb 2026 13:12:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 18 Feb 2026 13:12:16 GMT
ENV LEIN_ROOT=1
# Wed, 18 Feb 2026 13:12:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 18 Feb 2026 13:12:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 18 Feb 2026 13:12:33 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 18 Feb 2026 13:12:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:618efd37f74728f7dcba60c231fad7f2d777dc65e4da32d0adae5e032e1fd125`  
		Last Modified: Tue, 03 Feb 2026 07:13:10 GMT  
		Size: 47.8 MB (47776763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0c08292c273f6fa94290477f212196176e148c5443e72d590aa78d4b504c5d`  
		Last Modified: Wed, 18 Feb 2026 11:56:49 GMT  
		Size: 90.8 MB (90773425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a4fa34c44266bcdaa95e9c003ce6ac0f425d8ea75ef6bd3f09ef4ebe3d9fdf`  
		Last Modified: Wed, 18 Feb 2026 13:14:40 GMT  
		Size: 18.5 MB (18531846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75f81327f9103dbf75d53c2ad906b5f23c7c7a10107ce723b7c30710de3dc37`  
		Last Modified: Wed, 18 Feb 2026 13:14:38 GMT  
		Size: 4.5 MB (4517802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9be28f227f700a214e6fe2974d5854a553ddc1eaa32609a87490a8a181931345`  
		Last Modified: Wed, 18 Feb 2026 13:14:36 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:65aeaff25c6b4a3ecdfa0b88bc653e4a9073d333e5bb7538b72044bdbed26c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e7974411bce539459c68db9afec592eb7524dc7308db3d8b7fb28bedb15f1f`

```dockerfile
```

-	Layers:
	-	`sha256:ea81b455fe7f324d5b676e9939a09c4a0dd5c536eb253b15f8bb7996c5d8c147`  
		Last Modified: Wed, 18 Feb 2026 13:14:38 GMT  
		Size: 3.8 MB (3756023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38761fda52b42e86c41b119ad66b816a6eef4a240017307c7ec30199683d9533`  
		Last Modified: Wed, 18 Feb 2026 13:14:36 GMT  
		Size: 19.0 KB (19035 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:c8be8a4be721928d325989834758387fe124ba32af647437d074bb02679d21d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160727724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19043f8290467573878ffc1718685e450685417320464ee6e57459512c2158cd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 23:24:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:24:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:24:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:24:44 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 23:24:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 23:24:45 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:25:23 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 23:25:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 23:25:23 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 23:25:27 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 23:25:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 23:25:30 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 23:25:30 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:aba9aa950add2749194487d5c63a3069af6daf9dfe54d80cfbe32bfa7a5faa07`  
		Last Modified: Tue, 24 Feb 2026 18:43:53 GMT  
		Size: 49.4 MB (49354534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17752fdef1f284b40fe320bd54d7f9eefb1972a0ccd86993bc2287b508f560f7`  
		Last Modified: Tue, 24 Feb 2026 23:25:51 GMT  
		Size: 88.2 MB (88233869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416ff14df2418c67019f78a6065974f59167588791b663e1b60ac7ddd8336346`  
		Last Modified: Tue, 24 Feb 2026 23:26:01 GMT  
		Size: 18.6 MB (18621168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd0470f13c36090d6b19a2be41f7d76133e9d24e93b5ca2a7ed7d6fbcdf81ed`  
		Last Modified: Tue, 24 Feb 2026 23:26:00 GMT  
		Size: 4.5 MB (4517724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0074f8cc737ff967b181856c175defe55ea6cc3c60efe7716abf5ac74478de64`  
		Last Modified: Tue, 24 Feb 2026 23:26:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c5b49e5d410b9ddf026f832a74a3466303c7e81709ec5d79e8e3d5ace80482a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3783491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6043172e49664f88e5891ce424dc0ebea02852952a3910ed3ef5c2cd92a15fb`

```dockerfile
```

-	Layers:
	-	`sha256:d7ac437f3ead469e8bdee12903afcc8a026662090f5497083c3ef496461a22c2`  
		Last Modified: Tue, 24 Feb 2026 23:26:00 GMT  
		Size: 3.8 MB (3764512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b0fdbc916e48e3b3b9bca8cd1eaaac1c4360ce81267b8366b88e6377d3c0c8e`  
		Last Modified: Tue, 24 Feb 2026 23:25:59 GMT  
		Size: 19.0 KB (18979 bytes)  
		MIME: application/vnd.in-toto+json
