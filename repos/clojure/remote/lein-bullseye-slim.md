## `clojure:lein-bullseye-slim`

```console
$ docker pull clojure@sha256:4968289cbb31ef3e2f6931ed0ab442e90c7c2d5130f1bcfb7b2ac61ce3e9b99b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:52ccdd60f7a449bed38877da3fb3ced3cb5bd688addb1ee7cb9157d61d3a72ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142689604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d9bc45ca16a8289b5e49e19fb8c8e99a886da94a3a34e43a29dfe1ce03ceda`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Thu, 30 Apr 2026 23:52:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:52:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:52:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:52:57 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 30 Apr 2026 23:52:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 30 Apr 2026 23:52:57 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:53:11 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 30 Apr 2026 23:53:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 30 Apr 2026 23:53:11 GMT
ENV LEIN_ROOT=1
# Thu, 30 Apr 2026 23:53:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 30 Apr 2026 23:53:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:53:13 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:53:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7263c37a27b96bd5e0c0de77a44122fc986156c49e3c82b0ba12448611753e10`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 30.3 MB (30257934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81cf83b65b5023bccc08f3b82b8102eb618027de9ffa39cc4bd77fee12992ec`  
		Last Modified: Thu, 30 Apr 2026 23:53:31 GMT  
		Size: 92.6 MB (92574598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:484f4a25e51579df98c657a0f999fff6357b6243191c98db76487de9c58ee87e`  
		Last Modified: Thu, 30 Apr 2026 23:53:29 GMT  
		Size: 15.3 MB (15338891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40dd95fb8fb80ba39810ffc49659b9c160eaefdf33d6bea6cb872c90f945217d`  
		Last Modified: Thu, 30 Apr 2026 23:53:29 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eca79f633ed1292dab868d9fc72501e45c454a7e9fbb9935dd6e95e49d8fa49`  
		Last Modified: Thu, 30 Apr 2026 23:53:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:305ea79bb273b8547bab1335cd99663f9d378ae14cb70a298cc15755abf5ca38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f18b006e3b997c116ce41286ebb2218c8c3e5e813f52474e3694a88b02493eea`

```dockerfile
```

-	Layers:
	-	`sha256:f978e50408978b32313b2d5a160079f7a46948dc1dedee5f4b8f47ac84b47ec6`  
		Last Modified: Thu, 30 Apr 2026 23:53:29 GMT  
		Size: 3.0 MB (2996265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:675d91a5791c0908dca22b79b6c699ff5709126e919da2d03cae5fe53ce4bb5b`  
		Last Modified: Thu, 30 Apr 2026 23:53:28 GMT  
		Size: 19.1 KB (19058 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:76cce452798c9d9a7e2daacf920ce1303f8c8c0c95defe42bbd946b5b4b8bd4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140130176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a055ed60149a15efc61092863aeed10426e877ab1cf7cf6674914a5ece37eafa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Thu, 30 Apr 2026 23:52:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:52:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:52:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:52:39 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 30 Apr 2026 23:52:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 30 Apr 2026 23:52:39 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:52:52 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 30 Apr 2026 23:52:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 30 Apr 2026 23:52:52 GMT
ENV LEIN_ROOT=1
# Thu, 30 Apr 2026 23:52:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 30 Apr 2026 23:52:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:52:54 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:52:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2edb4294bb762cf72c918abd64eb2a96f327c2be3d13eb5cd9897ce992fe0362`  
		Last Modified: Thu, 30 Apr 2026 23:53:15 GMT  
		Size: 91.5 MB (91542246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720c3390b64b3fcb5f1f2ee14c8ad54dd28a3908ddc9e5491552dfc7d0496bd6`  
		Last Modified: Thu, 30 Apr 2026 23:53:11 GMT  
		Size: 15.3 MB (15327228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1689281f3e255bf6e545f563d4542524c068231b0bd257a4a13d865dc33eb6b4`  
		Last Modified: Thu, 30 Apr 2026 23:53:11 GMT  
		Size: 4.5 MB (4517762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200967c4965389eca6d48ff7c7eb37e5e57f8d3d2dcf6472ad3c492df8c54873`  
		Last Modified: Thu, 30 Apr 2026 23:53:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ec630069252b9157706fd133788e38e879ed3f613dcd099e03723f83c6a81382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8efd49d49f91912873a730cce4159fb2dcd6469111c19dd5ecf325c88fa94fe1`

```dockerfile
```

-	Layers:
	-	`sha256:68f9ecec4d528040d6cda7cc4675eb0fcefdaf15afd557958738e4cfb8814b19`  
		Last Modified: Thu, 30 Apr 2026 23:53:11 GMT  
		Size: 3.0 MB (2995895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e7d8c654bfda6e886e31c57ae405af5f0ad15da0385aa848b031ae0b5530344`  
		Last Modified: Thu, 30 Apr 2026 23:53:11 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.in-toto+json
