## `clojure:lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:cfd89c6c79021f0b44fd9db74e16d22c3d874f37ad6e3a1bc642270d67bee823
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:lein-2.12.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a556b1218c7ba8fe619f34a3b6a801fe3eba8b1bad49bd74f8e621d379257995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142371260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b1199fb94436cf971d8eadc5041f5082f796aca2298d3c0c99be64e09ec6d2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:06:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:06:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:06:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:06:16 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:06:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:06:16 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:06:31 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:06:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:06:31 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:06:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:06:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:06:32 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:06:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30a4bd162b1146e9afdcd2ff28c821f0f3e82bec4199a386d433a1f436d35a1`  
		Last Modified: Wed, 15 Apr 2026 22:06:51 GMT  
		Size: 92.3 MB (92256316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841c3b227dcdbccee83e558a949705614981652cbd70dd06d939f6823210b74f`  
		Last Modified: Wed, 15 Apr 2026 22:06:49 GMT  
		Size: 15.3 MB (15338782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47acdb682be6d803a9383aeb8b8e4e02505b8cde8d32e365d8b5d28c7a959661`  
		Last Modified: Wed, 15 Apr 2026 22:06:49 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed408a68361a0d14068338ae35354fb87567e991abd893ac7817b16b8611ff1c`  
		Last Modified: Wed, 15 Apr 2026 22:06:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8ceff25744d861d5c50acddbc65108a5db8a22e5520956cdac44ef6784629400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f897986a0355943197f347dd31c5e668f371ae49f178c568ed998397fd4b03ca`

```dockerfile
```

-	Layers:
	-	`sha256:a7c7baf857404260529854258b93020121f6c23c8874d05d9a406ec19a56307d`  
		Last Modified: Wed, 15 Apr 2026 22:06:48 GMT  
		Size: 3.0 MB (2995642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fd91595402f024c074df827dcc16244f6c87e1ec4d223966eb25cce28c424eb`  
		Last Modified: Wed, 15 Apr 2026 22:06:48 GMT  
		Size: 19.1 KB (19058 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:832d76e6d804d2494907abe26ae8eca06b7cf1be45b680b779f7d30e00f11cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139876193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99e114aae4d96d4adb9c200bb95220ec22608fea96e9a61673ef20f689db873`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:23:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:23:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:23:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:23:37 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:23:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:23:37 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:23:50 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:23:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:23:50 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:23:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:23:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:23:51 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:23:51 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1fe91dec7493aebdce03e00a6f571330100660fc56a6fc6d4018b941584cbbd`  
		Last Modified: Wed, 22 Apr 2026 02:24:10 GMT  
		Size: 91.3 MB (91288276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0ccd3317a261505e6d785099bf6e17287fd0d69c1a5f6323f2a0ad95f888ce`  
		Last Modified: Wed, 22 Apr 2026 02:24:08 GMT  
		Size: 15.3 MB (15327272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7d8014af229065cdef2da513610cfcd4c8da83365963c480806d88eae44f6e`  
		Last Modified: Wed, 22 Apr 2026 02:24:08 GMT  
		Size: 4.5 MB (4517704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e097599aa8293f0077b8de9624f9ae29cf52b0f62c1603897f1bc81a036a74c`  
		Last Modified: Wed, 22 Apr 2026 02:24:08 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cc8bec79edd50c5133c75b6b655efd1caa3a8c143e5c3f20c007d66a28587c68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2f4cd9de3364253ff0b530ddd020fbd41276ff5d6e0f19bebf4b4f816c34536`

```dockerfile
```

-	Layers:
	-	`sha256:3b903084f74ed2f9ebc48b935109c7e406df5da33a8b519d4ad756dfbc4dd3ed`  
		Last Modified: Wed, 22 Apr 2026 02:24:08 GMT  
		Size: 3.0 MB (2995272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4ff8606435b7059d71d29edab02928c77066b34e5e496b3206e142a33126f4a`  
		Last Modified: Wed, 22 Apr 2026 02:24:07 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.in-toto+json
