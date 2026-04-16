## `clojure:lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:05ce6395f040440abc5cd65ea616cb964ae0a25a35b8fe80212da76126f9a29d
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
$ docker pull clojure@sha256:31ab3669ee3db0456082ba9de9a52b5102428a9fa6e6fb7e840ef1557629c191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139878381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e673e9a1b70e496c8a578b7ff58135af8a1a3d12a2bd1639f6adfc6038a6cc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 03:27:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:27:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:27:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:27:37 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:27:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:27:37 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:27:51 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:27:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:27:51 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:27:52 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:27:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:27:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:27:52 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce54fafbf6a17c00335a514c8435c4a53149c0426bad635de54eed2756ed43d`  
		Last Modified: Tue, 07 Apr 2026 03:28:12 GMT  
		Size: 91.3 MB (91288274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b1412228a78dd9380c6f4311313709617360304b421b8d53dc519461501d69`  
		Last Modified: Tue, 07 Apr 2026 03:28:10 GMT  
		Size: 15.3 MB (15327277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16cb17f9ce0ba13d7ca13268e21e4584837839e9dd5062ecefa52ef9a7ac6281`  
		Last Modified: Tue, 07 Apr 2026 03:28:09 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809680aec859cc3af64e42eb5fdcd2d9907de0dcb6af6021273774a94764b3a7`  
		Last Modified: Tue, 07 Apr 2026 03:28:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e1180c4090f62b9db8530d3341806a0cb9cdff04975c7140e09897f067e5453b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94d338c2a167a947a94753c91f5dd7410447f0c34031ea7845c59fb5af20d738`

```dockerfile
```

-	Layers:
	-	`sha256:4a2bb6102db40f4eb481b6fb74006e9e6b0f61ae2d1c0237400316bce71a5951`  
		Last Modified: Tue, 07 Apr 2026 03:28:09 GMT  
		Size: 3.0 MB (2995272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92e72278b31e89905ee74de1fe0bb80e6ac103720c2d1d841e42e7ba3d8fc9ef`  
		Last Modified: Tue, 07 Apr 2026 03:28:09 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.in-toto+json
