## `clojure:temurin-21-lein-bookworm`

```console
$ docker pull clojure@sha256:ee29c5dedc5ca3f4992505c542733126bc453051d9363bdca92f638ce2d76a34
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
$ docker pull clojure@sha256:5f1051c97d69035861bcd40e30a2b82fc5936415f3b24f9422ba58e40cff9fff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230659556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f46241687992e20a4e74b9c60917a9f4c6d266d1e8db51af7c0ad78e7a2ad8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:43:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:43:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:43:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:43:53 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 21:43:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 21:43:54 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:44:11 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 21:44:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 21:44:11 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 21:44:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 21:44:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:44:12 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:44:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32900048d4bc4528bcfadba2eeb686e2b2927d1faf5317286f82d4d46386882c`  
		Last Modified: Tue, 17 Feb 2026 21:44:32 GMT  
		Size: 157.9 MB (157857066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0085d16ad0b653847927dd0b8d853e4448326a29378322c9d7284583d92b6a03`  
		Last Modified: Tue, 17 Feb 2026 21:44:29 GMT  
		Size: 19.8 MB (19802876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1542384e572d77792817d4524ac08a131d4b8fd7cda084bfaa77826a8dfa6e`  
		Last Modified: Tue, 17 Feb 2026 21:44:28 GMT  
		Size: 4.5 MB (4517702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f72b0a7a5383abf3f8d0ae1f262756ab05ed26f0fea21b10b361585fea95663`  
		Last Modified: Tue, 17 Feb 2026 21:44:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:bbb5bf86c025c9160dff5a50c6c60cf467359256d999e7fccfc16a8f0bdd4f1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4303251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:705b01d6d4d13044921526be31cfa88d12f566154f8f0a2a645eab0855154d8d`

```dockerfile
```

-	Layers:
	-	`sha256:fe6341a11d4840d6a610043593e5b140c86f8edd0b3c1df7e0efd0aefb8c2e9d`  
		Last Modified: Tue, 17 Feb 2026 21:44:28 GMT  
		Size: 4.3 MB (4284233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:554f5d14363f936b0a4660e7eedff258a6731e03bddc8318e67121ad50c66738`  
		Last Modified: Tue, 17 Feb 2026 21:44:28 GMT  
		Size: 19.0 KB (19018 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a599fa71435d60ec5b8af59f0ef8a638c2713841ba916bc1e04b6c9b477d86c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228650084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa2ac850eca3fa6bb0ae8fce90ee41b92056af204a0d94a26a09af247f4a2e5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:43:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:43:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:43:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:43:50 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 21:43:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 21:43:50 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:44:05 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 21:44:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 21:44:05 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 21:44:07 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 21:44:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:44:07 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:44:07 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:64e8f4c09e7ac936ecc3deb0e61613f653224c28b2e35fa9d8e6e11cbdb5f911`  
		Last Modified: Tue, 03 Feb 2026 01:13:22 GMT  
		Size: 48.4 MB (48365956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8ebf352dba19ed0f51ab1944eed76e54a79d2e3f7ced71af26730106918453`  
		Last Modified: Tue, 17 Feb 2026 21:44:29 GMT  
		Size: 156.1 MB (156133079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8882e3f4d6d1518645aa58997caf30b6e5675158bcab3cd32002c2a189c716d8`  
		Last Modified: Tue, 17 Feb 2026 21:44:26 GMT  
		Size: 19.6 MB (19632863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0cdb5f1ecf201e779830d2b077ce8ba647413c3d89dc34d38aac6e2c928a8bd`  
		Last Modified: Tue, 17 Feb 2026 21:44:25 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3362787c87777c151636bf245935f94bdc2cdbdcd632bc956b39e7230c50df94`  
		Last Modified: Tue, 17 Feb 2026 21:44:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b3d9f91b331d4a38b22faca00436a2b77ce20816bc11e34ca730475cfc048540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4303035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb2e473e38a5618903286efae4d6b48d99c520c68f1bf2c74bb0ed31d9df20a`

```dockerfile
```

-	Layers:
	-	`sha256:883a75c141443a63c64ca5d402a1fed2d41b9e37b41d90b5caa02e0018d27c33`  
		Last Modified: Tue, 17 Feb 2026 21:44:26 GMT  
		Size: 4.3 MB (4283872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22fa62f02670552cd55354230fa136a7552261c0928b6d7af23aa16e509618c4`  
		Last Modified: Tue, 17 Feb 2026 21:44:25 GMT  
		Size: 19.2 KB (19163 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:f8a146a098de9a96d6347c88b376cb97605c569a3cfc6c2a6949a7107a7314af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 MB (234846844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e417552c6345b139a4444f2a0de4e70bab9d67a14dcb0eedaa9ddbaa72fbd80`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Fri, 06 Feb 2026 00:34:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:34:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:34:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:34:00 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 06 Feb 2026 00:34:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 06 Feb 2026 00:34:00 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:34:58 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 06 Feb 2026 00:34:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 06 Feb 2026 00:34:58 GMT
ENV LEIN_ROOT=1
# Fri, 06 Feb 2026 00:35:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 06 Feb 2026 00:35:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:35:03 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:35:03 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5e189aacb842725e8d1d9877c9ab9af09e14901412b6665e179393112b5bca51`  
		Last Modified: Tue, 03 Feb 2026 01:12:57 GMT  
		Size: 52.3 MB (52327289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04686be48d2a894920edac0c0c6434c05a7128013df9522a975b048c103c93d`  
		Last Modified: Fri, 06 Feb 2026 00:36:06 GMT  
		Size: 158.0 MB (157977491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5308edaf3d998d611f0bca7d4706dfec48d76180df263136cbfa669fc5324293`  
		Last Modified: Fri, 06 Feb 2026 00:36:03 GMT  
		Size: 20.0 MB (20023887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ce01306bf353e6f4ec6bf8bb2fb8dad1881ad78f6607d1563fb7e93998458b`  
		Last Modified: Fri, 06 Feb 2026 00:36:02 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d15dae6899e01e3c1c8eefdd497e80b311749c6573f898b47a1fbff0f0ff5f`  
		Last Modified: Fri, 06 Feb 2026 00:36:02 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c5d3af9ed8e1d88ce552f9d03be04cae013a258c2e0c29374deabfce68d9b278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4305180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be8b9b3bc96ff07fca68093c2b44e79cacf442d63188ee5d1b78244bd237ea4d`

```dockerfile
```

-	Layers:
	-	`sha256:1a0fee53ffaea170b36391ccc4c04d8ba862dfd96ee24b3b780038009312628d`  
		Last Modified: Tue, 17 Feb 2026 23:57:12 GMT  
		Size: 4.3 MB (4286106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6199e7b0c8c69c3e96df8162b405061bb0b76654f37bb7114d60809da9bee5dd`  
		Last Modified: Tue, 17 Feb 2026 23:57:12 GMT  
		Size: 19.1 KB (19074 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:bea9c80ec56d2cedcb767bc33bf4d6c73b04d5d9e2c1849a8f88e799271f05f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 MB (218225143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f4d064172319a2ba43a1894770ee6e021af887c72efeaaa5c316d08335f757`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 22:10:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 22:10:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 22:10:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 22:10:51 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 22:10:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 22:10:51 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 22:11:15 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 22:11:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 22:11:15 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 22:11:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 22:11:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 22:11:18 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 22:11:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a0c87f6cc5f4110bd67035cd7755f19f9aafb832b1457fef813c0b6c748325`  
		Last Modified: Tue, 17 Feb 2026 22:12:02 GMT  
		Size: 147.1 MB (147105303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f49def24b66b5d9b9dd03b1c1d6041652623ac280de33c18c3659212d77b083`  
		Last Modified: Tue, 17 Feb 2026 22:12:01 GMT  
		Size: 19.5 MB (19463302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9464059b9443180b19202586edd885da202d8ac416237d5c07a1498e41ae756`  
		Last Modified: Tue, 17 Feb 2026 22:12:01 GMT  
		Size: 4.5 MB (4517765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0b5137a9a223bf9879c0d62e2b8099c557363f645997e460d2efc3d6aaf8c4`  
		Last Modified: Tue, 17 Feb 2026 22:12:00 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1b91d138e20e9a58960e6f86b2ac17284a36c6e6044bdaeccb409358eb950809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4295065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dc9958c75dec8b8981c3c070a72afbf723be415086551397203515c5e85b1df`

```dockerfile
```

-	Layers:
	-	`sha256:5862bf6b75037d9f2e7cefa2a4f9af3499767f457850b8ac575a10da89d4ca7e`  
		Last Modified: Tue, 17 Feb 2026 22:12:01 GMT  
		Size: 4.3 MB (4276047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d068eca7265ca33f29a8afb956f9db82268095ec752e6b68cfb20e191f739821`  
		Last Modified: Tue, 17 Feb 2026 22:12:00 GMT  
		Size: 19.0 KB (19018 bytes)  
		MIME: application/vnd.in-toto+json
