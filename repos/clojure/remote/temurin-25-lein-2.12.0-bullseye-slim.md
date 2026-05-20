## `clojure:temurin-25-lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:3a0c2293c1823cfb63760fb6fbd8441e8c706b24720de6f2116b6c97848394d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-lein-2.12.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6227011664bde777d74ed7f8c2998494d0d20456ac19ed35ec38c91d2f91b8ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142689211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8552574a5446d1ccd3a9ca8f2a4a721c5a829ea1b9b47b82691ff4f232e4d24`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:00:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:00:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:00:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:00:51 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:00:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:00:51 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:01:05 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:01:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:01:05 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:01:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:01:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:01:06 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:01:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8419f4a27c97b0c111ab0dc77e0159bd3abfadcb948d4a49cf6dd6670703b84e`  
		Last Modified: Tue, 19 May 2026 22:36:35 GMT  
		Size: 30.3 MB (30257598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bdcfce1d5ccaf450f9985d2be0226e4a69725efe46e7112b9fcd56ea4dbc1b`  
		Last Modified: Wed, 20 May 2026 00:01:26 GMT  
		Size: 92.6 MB (92574588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d630fe001187db5040973af59a4bb4e2cc6ab7d0fd576c8bccc2daca97c82d`  
		Last Modified: Wed, 20 May 2026 00:01:24 GMT  
		Size: 15.3 MB (15338896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc579499232d880dd969e8899a344d820a24542e35a92f56fb7ed291191a986`  
		Last Modified: Wed, 20 May 2026 00:01:23 GMT  
		Size: 4.5 MB (4517701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b741198e8d38cb16515c286d1d9862508c1c1aeeddca0268b86e79aed4e98a49`  
		Last Modified: Wed, 20 May 2026 00:01:23 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f8e636e9c097ca67ed2cb7966b6f232b8e265af1a93d7c747bf19738acf8e18d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef19de84e053a7e29e7245eef7e2b140c904e4e3ed06327b1943a33cd11f087`

```dockerfile
```

-	Layers:
	-	`sha256:ca78ad6805f2f89a37de622d90f8cda9a32d642e2f9b6e9f6913273f039bac21`  
		Last Modified: Wed, 20 May 2026 00:01:23 GMT  
		Size: 3.0 MB (2996265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81fd67c21ec21894849fcd33bf6849e83b20813e4c43907e5b5377d30eb8ad7f`  
		Last Modified: Wed, 20 May 2026 00:01:23 GMT  
		Size: 19.2 KB (19212 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6e9a9b897a26686b69033f4c09cc65e3492592003aa1e1395f9ebdf0bca0b25c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140130576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7b6d47d98a5ccb4fc9d21014d3a52899de5ab647aee8ec34e4d1a170413ee8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:07:46 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:07:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:07:46 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:08:00 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:08:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:08:00 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:08:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:08:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:08:01 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:08:01 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2b99ba6638377be8e7e1e9a328ebb001513ab9f700c8168d404eed03437c7ce5`  
		Last Modified: Tue, 19 May 2026 22:36:47 GMT  
		Size: 28.7 MB (28742972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a88c856343e796d21136e0045b8b8b7dfaded3855fe3dd529124993d2242083`  
		Last Modified: Wed, 20 May 2026 00:08:22 GMT  
		Size: 91.5 MB (91542245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e32e46746a904bfee583d9f267378af1eb407cc8419b5a6cc0f46144cf8d750`  
		Last Modified: Wed, 20 May 2026 00:08:20 GMT  
		Size: 15.3 MB (15327231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce5b0278e1a85c973e425b63f998b46b5ec090eea1bc0c41750f8e64c50dc6e`  
		Last Modified: Wed, 20 May 2026 00:08:20 GMT  
		Size: 4.5 MB (4517700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7004c1f724179b44f2d03b141a9cedf0cf6c8b77c92546484672a5fe53f22e`  
		Last Modified: Wed, 20 May 2026 00:08:19 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f4402b55c1f87a6dd5be607d8c5a9ae1f3641087de05f74583b6f8e28034b9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a4a979fac0c8581e2a975c09b5e5eaf540304b1337631e5386f708a9e4f71d`

```dockerfile
```

-	Layers:
	-	`sha256:2b9a5605bf74410a029b4ad31d687f76594340f4ac974c05279c6c6e3ed3ffda`  
		Last Modified: Wed, 20 May 2026 00:08:19 GMT  
		Size: 3.0 MB (2995895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af4875f08a11e32399d8ca013b52a4948395cf14c298a0a4cdf0cbdf37d5db9e`  
		Last Modified: Wed, 20 May 2026 00:08:19 GMT  
		Size: 19.4 KB (19357 bytes)  
		MIME: application/vnd.in-toto+json
