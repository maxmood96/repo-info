## `clojure:temurin-17-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:f775f3a35f41c34daca22bc36495ef5255674386dd2577de955dcb9e40c61900
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

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f90a3d8505df53db9b5a90b61355232a354ad40e0db01e03c6df764e3c6e2725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.1 MB (196142028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff67704030d2f2c70ed1dd23147a67ee7186b2b469ae78565435c6a095cbf5d2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:14:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:14:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:14:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:14:27 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:14:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:14:27 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:14:41 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:14:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:14:41 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:14:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:14:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:14:42 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:14:42 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91aaec9343fcbe65bfeecd5e1a675b0c9301edd514adfe2317a5d76d20931e26`  
		Last Modified: Tue, 07 Apr 2026 03:15:01 GMT  
		Size: 145.6 MB (145628782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643e17420496741ca8583673557ca672b3b30ad394608810b3ece1fcc3d86b31`  
		Last Modified: Tue, 07 Apr 2026 03:14:58 GMT  
		Size: 17.8 MB (17758737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d5b0b6b66d82ee321318fbb044c67525bff99b8de83072a0432d843f5af7ff`  
		Last Modified: Tue, 07 Apr 2026 03:14:57 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00806c71441dd4ee48ebf0a0604abb38b7653bc37380ab08a13254d9d9bcd73`  
		Last Modified: Tue, 07 Apr 2026 03:14:57 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:af4132b47d03929e574925648fb5f89021a24acd10b131d82e67c3a0bb4c6938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2748453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a399873abb52d5f2965a5f444ec07e14a27fb9527a19af3f6f18bbb853bf9104`

```dockerfile
```

-	Layers:
	-	`sha256:565c33a6f2f2c80907048de915b665a68a7dedc93cf46317c0a222438e0ea2bf`  
		Last Modified: Tue, 07 Apr 2026 03:14:57 GMT  
		Size: 2.7 MB (2730050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:026cf9ab48c2628f11f43bf3d9630ec9325bcb42f770bffc459506e534ddedf8`  
		Last Modified: Tue, 07 Apr 2026 03:14:57 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:65bb1c06417351e5b02c3eec33a2949e23b9b5d2d787a0dd0ac696504b2a8f49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194662242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:974d2c1f32d10c5b00c91b17afda8a4ef465acb30d38c9924c9b2dfe53b724a0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:25:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:25:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:25:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:25:06 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:25:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:25:06 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:25:20 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:25:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:25:20 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:25:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:25:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:25:21 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:25:21 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355ca048bebab1889bfb4c93ba32d1eca2f181a3350b08e8d77663450ab61cb3`  
		Last Modified: Tue, 07 Apr 2026 03:25:51 GMT  
		Size: 144.4 MB (144436222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014a9b1f9d55ec53097ad7dfb5763ccc57e540d43034852109ec428556d6adf4`  
		Last Modified: Tue, 07 Apr 2026 03:25:42 GMT  
		Size: 17.6 MB (17591721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4dc3046509d662124e6edf91e69709ce0ccb285d1d6f5c1527905ce9d38bef`  
		Last Modified: Tue, 07 Apr 2026 03:25:40 GMT  
		Size: 4.5 MB (4517705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9310ae3a7b8cdfd793b5ddab3e8a0d5dbccdffe0a27b2c85710a6171d5869ee0`  
		Last Modified: Tue, 07 Apr 2026 03:25:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fd4910a5247480a42396d5973bb791d717b6d59453d4ec7987d6c91e340aeab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2748189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81686f32a792904d88f0c9ce4e57bea08abdce70998c30c5d08f8b52b0b97261`

```dockerfile
```

-	Layers:
	-	`sha256:44e92b4107e44455d519188141782f8332cfac8566c89383c1eb5bfe4cc8b383`  
		Last Modified: Tue, 07 Apr 2026 03:25:39 GMT  
		Size: 2.7 MB (2729665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dc077b8c94cbcd98efd872797636c4be62196d5a72babd103d75a1cae730296`  
		Last Modified: Tue, 07 Apr 2026 03:25:38 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:65b33b406d6b925d6a9bd5907520e3c5c772d6e3683f9046622c22cef36c35b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.0 MB (199995849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d22d7eb85cfebeb8df85da93dc0d812d51ace8eccae419627d4d7a60cd424b98`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:24:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:24:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:24:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:24:41 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 18:24:41 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 18:24:42 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:25:14 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 18:25:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 18:25:14 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 18:25:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 18:25:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 18:25:19 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 18:25:19 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7a0392d98c02d4219c67a8e3d3837c1ac5d4af6836b9264bdd6c427cc7a24f76`  
		Last Modified: Mon, 16 Mar 2026 21:51:26 GMT  
		Size: 32.1 MB (32078368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7705c24a18f6ee8e217698c94ce8917cf545ab215e1af2f67054b8aadf8bc4a9`  
		Last Modified: Tue, 17 Mar 2026 18:25:57 GMT  
		Size: 145.4 MB (145438266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e3395bc70d914613b67a90bbaeb271931c0cc91249e7591b60d32465d23bed`  
		Last Modified: Tue, 17 Mar 2026 18:25:54 GMT  
		Size: 18.0 MB (17961026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbe0ec3ef42cf989bd7286131fd877f83a5720ffabed690d0e8fa5f542c06893`  
		Last Modified: Tue, 17 Mar 2026 18:25:53 GMT  
		Size: 4.5 MB (4517760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903d3ebd10b9b06a8b70d206f0e9cfcd5764f1eeeb6e38d077adc6b72f92702b`  
		Last Modified: Tue, 17 Mar 2026 18:25:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:75b224a25fc81a2065c30d09446a278e405ef12e299a647d0a3661667db186f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40778313ec6597afa67f7750fb8f3fdca18e2eb045b6c83afa6a4a13c9804340`

```dockerfile
```

-	Layers:
	-	`sha256:53308d9bb344f5da78d69a06c4c32e0ee64c80e1803e99099bce59c179c7b3d1`  
		Last Modified: Tue, 17 Mar 2026 18:25:53 GMT  
		Size: 2.7 MB (2731883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49b5cc350b1ecec378d00bab4c99687c88c5639c2a6ff8463d0282cdeea50145`  
		Last Modified: Tue, 17 Mar 2026 18:25:53 GMT  
		Size: 18.4 KB (18447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:c98fb44f2bcd2863eee27a30bffdf5af5e69755dbb685a71b9144b7741cf0908
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.5 MB (184457730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8025916ba325a19c1c1d7644183773889488b6f39b5ea8a21c8bbd565a1daef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 05:41:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:41:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:41:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:41:51 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 05:41:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 05:41:51 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:42:01 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 05:42:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 05:42:01 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 05:42:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 05:42:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 05:42:03 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 05:42:03 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5bb5c429c7fc69853b04b7b379880a199d321686ac73dcbc03c18f0876fec8`  
		Last Modified: Tue, 07 Apr 2026 05:42:27 GMT  
		Size: 135.6 MB (135626852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325808f73e8f388e4951eb7b96e4e92075e92da606e6cf93652a52e765810dd1`  
		Last Modified: Tue, 07 Apr 2026 05:42:25 GMT  
		Size: 17.4 MB (17421087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41067c022b1888529dc9e4360508cc4f4e7c2e3ae04893e485e230ac3eb5bf68`  
		Last Modified: Tue, 07 Apr 2026 05:42:25 GMT  
		Size: 4.5 MB (4517728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29bb477ed9d3d1e77bd0e1689d25e71421a1cbf64aec7310b5468d8fee97736`  
		Last Modified: Tue, 07 Apr 2026 05:42:24 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fc82e1eaf7fe1fb7fb85c24253efba0f576e7f078d87282c6b2be940f6ee1528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2740267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ebb9d0aca78c7418d138ca13a5c602968a65661ef719816a130e49ebb015139`

```dockerfile
```

-	Layers:
	-	`sha256:4e56f7b2b0aa5850d6bd9eab7f03dfef23df9078d9eb5e0d676a13fa3afcc0d9`  
		Last Modified: Tue, 07 Apr 2026 05:42:25 GMT  
		Size: 2.7 MB (2721864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8a9907ef179f113ec65a5f4597fb6bcfb624c31855fb9cc8c5b7809fae5f6c3`  
		Last Modified: Tue, 07 Apr 2026 05:42:24 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json
