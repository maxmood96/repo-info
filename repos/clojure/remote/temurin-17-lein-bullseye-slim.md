## `clojure:temurin-17-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:383aa7c8365da368fd3781d2d98d970699935886c33a64ac8f94708d39bf8e94
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1626be015768787e43bc0b89652120d24b8b42712662d800ab04d83fe1d696b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 MB (196022752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7bdecedb0fb34141f02f226c52933f8ea8b7b667f70be0af0043014fc8fc2c0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:18:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:18:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:18:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:18:37 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:18:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:18:37 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:18:52 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:18:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:18:52 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:18:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:18:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:18:53 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:18:53 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:55534d9909ecd18467599b415fa2553c3106849154ae8a361a75f1a24f2a4364`  
		Last Modified: Wed, 10 Jun 2026 23:40:12 GMT  
		Size: 30.3 MB (30260255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9396e8b7026e608c399a9659700596795ec0c8aca9d9d983655bf3d931573029`  
		Last Modified: Thu, 11 Jun 2026 01:19:14 GMT  
		Size: 145.9 MB (145905490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43907f1764bded88d87b7712a9304bffbb93e37f1a5ebfa2521120117a640f03`  
		Last Modified: Thu, 11 Jun 2026 01:19:11 GMT  
		Size: 15.3 MB (15338867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990abb0ec0ab691518cce9a835c9fb41d539cc1812d7fd37fda3c2f7fcc8bf00`  
		Last Modified: Thu, 11 Jun 2026 01:19:10 GMT  
		Size: 4.5 MB (4517713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7224194cfb9132da5a7c9501a3b4a7dfb70e51c6a104a39bc87e6ba1ed851f1b`  
		Last Modified: Thu, 11 Jun 2026 01:19:10 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5444e48c7ff581c071c8306304733d7782abb7f0a215cfb7e59e93fc25d0b05a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3046770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6a948480793a4696046d4b8e8456c7896ff4f425d2154f7531378962c862fb6`

```dockerfile
```

-	Layers:
	-	`sha256:d70c32e087728115c75a56b1616da958545459e9321c79781bdee9703cd9349d`  
		Last Modified: Thu, 11 Jun 2026 01:19:10 GMT  
		Size: 3.0 MB (3028213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4123dc1eb90db7dfc666722e3f987a09b509486f27c71eb04e8185eb9288862`  
		Last Modified: Thu, 11 Jun 2026 01:19:09 GMT  
		Size: 18.6 KB (18557 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:508893652a26b8dda9a18aae189cd31a6a9fd52ad72acb83f818e3ef26832b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193315931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13691a1185685ea31d78e8e4f3056081402017b0aa1624e6b28beca0f33ffd3e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:22:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:22:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:22:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:22:24 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:22:24 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:22:24 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:22:37 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:22:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:22:37 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:22:38 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:22:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:22:38 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:22:38 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ca483a18241c226a06a4a4afd22dc5496062254c671fa595136458fb8fcd0107`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 28.7 MB (28746154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7347e99cd3f44ba332247072e63d776f0032e33aab010ddaac45bc123843d0eb`  
		Last Modified: Thu, 11 Jun 2026 01:22:59 GMT  
		Size: 144.7 MB (144724360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67131d81d6226eb94210658f932943d6a590c3d52445d736aec002b00994ec2e`  
		Last Modified: Thu, 11 Jun 2026 01:22:55 GMT  
		Size: 15.3 MB (15327284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f8e98942b3edabddf06503cf80f7db1d2aa5cdbfc330a3d46ea93f0ae4fdc2`  
		Last Modified: Thu, 11 Jun 2026 01:22:55 GMT  
		Size: 4.5 MB (4517705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a059eab83bd547f3c683df5663dd292a64cde05ffa3f9582aab722a1e570c967`  
		Last Modified: Thu, 11 Jun 2026 01:22:54 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:73343410f41100b63c5f1f188c54acf8aa305da1392fba6f59c5f9e8d8564c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3046500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ff7e93d4678866ce5a89d09aad520adbc15ea69ef5f3284314588d576fb18f`

```dockerfile
```

-	Layers:
	-	`sha256:4ae3d5f0668d24be9879564bfb8e41319b9c1524f84a461e35e92a15ddb6d449`  
		Last Modified: Thu, 11 Jun 2026 01:22:54 GMT  
		Size: 3.0 MB (3027822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5be50d0fd14a392f1996d3cb215fa63ab918a37c958717f0b2035e28552dfb37`  
		Last Modified: Thu, 11 Jun 2026 01:22:54 GMT  
		Size: 18.7 KB (18678 bytes)  
		MIME: application/vnd.in-toto+json
