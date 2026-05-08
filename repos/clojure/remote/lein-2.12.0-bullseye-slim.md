## `clojure:lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:3c769db05d452b4726d40f5916e45d63b48ffa87e697bf40ac60ccbc40499fb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:lein-2.12.0-bullseye-slim` - linux; amd64

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

### `clojure:lein-2.12.0-bullseye-slim` - unknown; unknown

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

### `clojure:lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:694d38ddff7df5b06ceb33ce4018a00ef15c8d4fd9160b05aa399e0bf9ed458e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140130184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:417e9c898635acfccbd1acd498d0db2b2bb1eacc03d8b1172ee1b10bf4fcb775`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:27:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:27:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:27:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:27:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:27:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:27:18 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:27:32 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:27:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:27:32 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:27:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:27:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:27:33 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:27:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75f0dedbdc6f5f34c39efbc1e92b564944c4405fc1842ea5afbd67d0f635bb4`  
		Last Modified: Fri, 08 May 2026 00:27:51 GMT  
		Size: 91.5 MB (91542278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8237de51e4cb8dde7d3ec9ae61bdbbdce62c7535117a3e1b2c39b3f1dbeb19`  
		Last Modified: Fri, 08 May 2026 00:27:50 GMT  
		Size: 15.3 MB (15327250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d1821b49e5b13362e218f474fe5ac30b98dc0ee28c7a60dd96bd1cbb35d72a`  
		Last Modified: Fri, 08 May 2026 00:27:49 GMT  
		Size: 4.5 MB (4517716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062c4538066e28f2f347f0cebb6a1836d07d38750ffe51cdf5173938f12e605c`  
		Last Modified: Fri, 08 May 2026 00:27:49 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f02970b07006b898f2db903e25a61c01904bc6c119bb26204884b2a7bd0d32c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253761d1cc7e35b71860eb0c51333811e850af6ffe8d25ff35aca8084810667b`

```dockerfile
```

-	Layers:
	-	`sha256:edf4e04b81fc98d9dab0b0323811d5963338952c8c086fad1ee4726cc8d08446`  
		Last Modified: Fri, 08 May 2026 00:27:49 GMT  
		Size: 3.0 MB (2995895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e4d04083f1ffdc31e783d65e6bbdfcda82de55ea03f5545ce06c05881a8458c`  
		Last Modified: Fri, 08 May 2026 00:27:49 GMT  
		Size: 19.4 KB (19355 bytes)  
		MIME: application/vnd.in-toto+json
