## `clojure:temurin-21-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:d6e67f5bb585d3619213713da48baa001b622981740f882180b57174f24e5cd2
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

### `clojure:temurin-21-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:12a30c8b19378f0a4b17fe30ba15c64c1752f64e7095e4e63c529740741dc099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.4 MB (208370264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25a36c12421e78e59ebddf05c6f0045a2f15dd184b4d543cec15f558a0aab8ba`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:59:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:59:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:59:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:05 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 02:59:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 02:59:05 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:59:19 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 02:59:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 02:59:19 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 02:59:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 02:59:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 02:59:21 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 02:59:21 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b8a097080f69241fab9e5f7e7ac30e44bf1f2f6290cdef803ca691091b8103`  
		Last Modified: Tue, 17 Mar 2026 02:59:41 GMT  
		Size: 157.9 MB (157857094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ff18db9d76dd212156d2febc715829fb1c6c296fedc5ed52949967ea6a82d0`  
		Last Modified: Tue, 17 Mar 2026 02:59:38 GMT  
		Size: 17.8 MB (17758767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e58212c04a4f6ea914e8cb8bdaed91444be4360c7e975bc490f085c52415ee5`  
		Last Modified: Tue, 17 Mar 2026 02:59:37 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab659af8427e8e32660e81d2aa7b6654e03c4cc184f2353ca899490a17e38ecb`  
		Last Modified: Tue, 17 Mar 2026 02:59:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:687acb80b596b31845f0e854cae7065a2caf51bbed121a9a87c9ab7a68f2decd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b872ab04310aeb1b7f8c96b813e3420501d8de46c6efb5164674e1070250b73b`

```dockerfile
```

-	Layers:
	-	`sha256:00611565a320a1fd95c2ab5f5951bbd451ea425cb058e96a9fe7c15f1a1da386`  
		Last Modified: Tue, 17 Mar 2026 02:59:37 GMT  
		Size: 2.7 MB (2731902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:019fda3b19ccbf06789efa6580240c88def9f49221538b636c91bbbaec6b71f3`  
		Last Modified: Tue, 17 Mar 2026 02:59:37 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:59b5f0589e7c3599364e526da119358c29a1210a0f819ecc6c05a7197ad783f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.4 MB (206358969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd4d5396b34f2ba50b7c1312681394c026eb180d412e2cf9501c431f5d5f47a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 03:03:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:03:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:03:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:03:44 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 03:03:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 03:03:44 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:03:59 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 03:03:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 03:03:59 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 03:04:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 03:04:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:04:01 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:04:01 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304620f29e8b183c88765b7ff2bbe3947fdd1be256759a9709865c4d9783dc58`  
		Last Modified: Tue, 17 Mar 2026 03:04:23 GMT  
		Size: 156.1 MB (156133067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de666aaefd2ee85c07f61808d7b8114c335b748a34e22659d279926277ed1c9`  
		Last Modified: Tue, 17 Mar 2026 03:04:20 GMT  
		Size: 17.6 MB (17591654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2aa3034100b010df785ba3bce4cf8cd34932e83a61e2713536e29ca754f5ff`  
		Last Modified: Tue, 17 Mar 2026 03:04:19 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4dfad67606a908f61f17f296316439b260fbb2180879f80ee5b55b26a086f52`  
		Last Modified: Tue, 17 Mar 2026 03:04:20 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:33ad46cb0c904a61b5bd87477285b4a39cca1b4cbef1b0e660851fe61acb9254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b45e5aed1c1b267f3526b2180f26e5ceb49365313e1d40969ac53f7a7b4271`

```dockerfile
```

-	Layers:
	-	`sha256:f524244292fc88a6001c8462c9246db1d476c2978fb6bba6ceb35914b8ad4258`  
		Last Modified: Tue, 17 Mar 2026 03:04:19 GMT  
		Size: 2.7 MB (2731517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b207b8375ae834d9720629f5d364edf79caf1c4c08c83fd770bf44c2de6a963a`  
		Last Modified: Tue, 17 Mar 2026 03:04:19 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:547010ecb3a36cf37b2e444fe774155873bc2a387dcd1c66b89b75df3b2fe9b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212535178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2750ae5bb389ceda1b2f1a9d1ebf2c045cdfe6a5a7ee0726b7c1a56ac1e56c11`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Wed, 25 Feb 2026 02:05:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 02:05:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 02:05:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 02:05:55 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 25 Feb 2026 02:05:55 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 25 Feb 2026 02:05:56 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 02:06:39 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 25 Feb 2026 02:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 25 Feb 2026 02:06:39 GMT
ENV LEIN_ROOT=1
# Wed, 25 Feb 2026 02:06:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 25 Feb 2026 02:06:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 25 Feb 2026 02:06:43 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 25 Feb 2026 02:06:43 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3def25e912c223ee8b3899e5ca048b2439f856f438ac690293817fbc0291fb36`  
		Last Modified: Tue, 24 Feb 2026 18:41:49 GMT  
		Size: 32.1 MB (32078334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5554cc30d2ece3b83d1f3ef7a2c6ac48097d705e7c60313c2c3e4c68fe1a70`  
		Last Modified: Wed, 25 Feb 2026 02:07:30 GMT  
		Size: 158.0 MB (157977535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aef61f6b66df0da77ec669d30996943f9c1c58a078cacf74f4d4c5639a2b7d0`  
		Last Modified: Wed, 25 Feb 2026 02:07:27 GMT  
		Size: 18.0 MB (17961128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7539bb9611efa3ce3cecbfb9bce7bfb0f67fab620817335c5aab86d391228cbe`  
		Last Modified: Wed, 25 Feb 2026 02:07:26 GMT  
		Size: 4.5 MB (4517751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af35ddd479dce75360ab8dc8b60b1eb9a0f87bf0fc7bc47f0122065b40eed1b1`  
		Last Modified: Wed, 25 Feb 2026 02:07:26 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:97aa7369d5f8d36c1fd8b40698eef566edebcf10523d80312e28b2beb27456e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2752182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806b4b87bfcde4f52dd7888570322610f67ba42300c2a3eb743cf5e71887cbd5`

```dockerfile
```

-	Layers:
	-	`sha256:5b4c8cadaac783f5f6e7916afd346848028bac9df085174ba90d9d52949702d3`  
		Last Modified: Wed, 25 Feb 2026 02:07:26 GMT  
		Size: 2.7 MB (2733735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:106f0ce88a083411fd1f4e04e8caf12233ed986db43c0721c768f39ecebdeb3c`  
		Last Modified: Wed, 25 Feb 2026 02:07:25 GMT  
		Size: 18.4 KB (18447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:af8a0bdd3ff42ae7e68a9cdb12967a6129d4a9b1206c1d91c4e975c34e66b53f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 MB (195936230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43337067e711769f8589dcfbdc62def7678bca1b569194e45d2fefe953c4fcd5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 23:19:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:19:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:19:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:19:01 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 23:19:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 23:19:02 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:19:32 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 23:19:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 23:19:32 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 23:19:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 23:19:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 23:19:38 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 23:19:38 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49354e9f0679f3ff8b88e9d693551817e9930dd3f79f0b6470d4ff396a09d7f9`  
		Last Modified: Tue, 24 Feb 2026 23:20:16 GMT  
		Size: 147.1 MB (147105304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fa045514c6d6d4f9575cbc3bc87ca37f3f4c017f92eabc714dd0d7e97b743c`  
		Last Modified: Tue, 24 Feb 2026 23:20:16 GMT  
		Size: 17.4 MB (17421214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da680f9827b4af59cab020cac1044a4b991fdb289897429a12c2028a1259911a`  
		Last Modified: Tue, 24 Feb 2026 23:20:15 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f1f874c4f84f0cde05eca6c02a47e4d112383963df8372ec1ccb5964df2e67`  
		Last Modified: Tue, 24 Feb 2026 23:20:15 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9cc0fe128548475db199bbef5066eb9c86c2c3527b96419033bb3e152bf13d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2742119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103be78e64973d8725bcaf70a67a199b9ed5ecb7d2dea3530c7438db32bb702b`

```dockerfile
```

-	Layers:
	-	`sha256:94ce26bd89950f87425d914fa63471932a908bb56debe42cc54b4c1558468542`  
		Last Modified: Tue, 24 Feb 2026 23:20:15 GMT  
		Size: 2.7 MB (2723716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aaccf6814bdd0a86d8a4220f4cb3caabfb929cf01a5d15837ab6808db7f3a019`  
		Last Modified: Tue, 24 Feb 2026 23:20:15 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json
