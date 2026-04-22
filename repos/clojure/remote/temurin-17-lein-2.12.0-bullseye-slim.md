## `clojure:temurin-17-lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:b27fd64183d836f8298e22994f64ba727971a31ec73841b3b412af8cca30b213
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-2.12.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7bb16be02bc23868d7505952cd11f80e663ef417127376d8e947ae36ed674d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195743705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd02a03ae3ffd49cf8edaace0a7c2dd45e0a97c016830376ade112a570b11b5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:18:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:18:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:18:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:18:23 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:18:23 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:18:23 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:18:36 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:18:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:18:36 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:18:38 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:18:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:18:38 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:18:38 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7263c37a27b96bd5e0c0de77a44122fc986156c49e3c82b0ba12448611753e10`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 30.3 MB (30257934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1350dcde4f96737226196533d72ca1adf05f9a64ad0119cbdccc71cac9bf3c00`  
		Last Modified: Wed, 22 Apr 2026 02:18:57 GMT  
		Size: 145.6 MB (145628777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00939380cccdbe6d6a8914da489dcf29902dd4f8f7195706b092b0eb934af16`  
		Last Modified: Wed, 22 Apr 2026 02:18:54 GMT  
		Size: 15.3 MB (15338835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de383a6001b35740ee7d4784e865e653649e1344341b25a4a6709ac623359cbb`  
		Last Modified: Wed, 22 Apr 2026 02:18:54 GMT  
		Size: 4.5 MB (4517731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7744c0b3ff7bfef99b9fa6e625ca050c1b5a8502334841c539f668eab2810f`  
		Last Modified: Wed, 22 Apr 2026 02:18:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dd5fd6c8e4c817a6dd3d43a19dbea22ab5597371bd9a94b57121c0e33f8f9a13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3045985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65bb3526c7cd7c49ab1d5846ae84a5b1907a5420d90a8d0d23f1adbeb5ffea42`

```dockerfile
```

-	Layers:
	-	`sha256:6a3c6fcd2df098b7cadd7f26182e23b916c6f641f71bda51c3a4cf5315ec3339`  
		Last Modified: Wed, 22 Apr 2026 02:18:54 GMT  
		Size: 3.0 MB (3027582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2839d6d7070be12c3ed757bea691b90d9e3c07a6394595b0d9730506bd1f4381`  
		Last Modified: Wed, 22 Apr 2026 02:18:53 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:821e49737bea2622382ab26b0028c0e9779e807b56f2e27dde26236cacbccec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (193024129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e01358494b6eb27e07285a4577d17049bd7672a25ff03b08e8a046d1568d3cc6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:21:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:21:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:21:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:21:35 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:21:35 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:21:35 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:21:48 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:21:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:21:48 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:21:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:21:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:21:50 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:21:50 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ab304f220d8a8ccbd47569f385750aa3f87cafd221f915b82f8e566f1abe130b`  
		Last Modified: Wed, 22 Apr 2026 00:16:28 GMT  
		Size: 28.7 MB (28742512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e7d277dd066ce341aff4605bf8782e015afa7ea5e709710fbaeb24ab0d5112`  
		Last Modified: Wed, 22 Apr 2026 02:22:11 GMT  
		Size: 144.4 MB (144436230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454167e423a91df45398ca8062765f0528875b0aebb9c524dd70d101d99b5407`  
		Last Modified: Wed, 22 Apr 2026 02:22:07 GMT  
		Size: 15.3 MB (15327213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d54c06e6055f61d99d381847c158e24ca8b76cc05ca4123fd62634983cc6f3`  
		Last Modified: Wed, 22 Apr 2026 02:22:06 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ef2167011feb7f2232634ae6a40a4384bf13dfcef3aac7e9122b88d4b225c4`  
		Last Modified: Wed, 22 Apr 2026 02:22:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eb1187749fd81dea302aa80f7003f632308683a47b64bc8339c07a7a1b314c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3045715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adab719fca5aff4b9ec8a9b034c6ce3b35c9fefb50d3ee8b02b4652925ff359e`

```dockerfile
```

-	Layers:
	-	`sha256:9ba255007252748e76c2348c8f963c6dbd54add93b221aebc75cac4b35ac32be`  
		Last Modified: Wed, 22 Apr 2026 02:22:06 GMT  
		Size: 3.0 MB (3027191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4fb147ccf7dbbf0e9fa452936ff24b444a3c226ff79782c6b153ddd6a88cff0`  
		Last Modified: Wed, 22 Apr 2026 02:22:06 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json
