## `clojure:temurin-11-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:c72d011460e93b47df12f7556d951e2cb2c6a295a7d4257593d8eff93d17e7ac
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

### `clojure:temurin-11-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:127af0198d7404ca404cdc31a1b6615c844a77bf760af0c150175c4254b15a3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.4 MB (196399779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a379b775d9932439a782d1d63e5ec26a65a790ad30a4ba5bbd3d3bd007f586dc`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:06:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:06:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:06:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:06:09 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:06:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:06:09 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:06:22 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:06:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:06:22 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:06:23 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:06:23 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9a53ee883582cf467c7182d9c18ba38853f4878490341cb42290a7be74dced`  
		Last Modified: Fri, 08 May 2026 00:07:08 GMT  
		Size: 145.9 MB (145886193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d5dc4cd252c5edded51b19c83317a6eb10daf046d366cab1ec7b66c64a5d74`  
		Last Modified: Fri, 08 May 2026 00:06:39 GMT  
		Size: 17.8 MB (17759582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1095ae253e97ee33ae7b5c4f948b39b7a073fd281ba0e9c7e27089b04f377f5d`  
		Last Modified: Fri, 08 May 2026 00:06:38 GMT  
		Size: 4.5 MB (4517720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:617b2b391db5e3146e28fcdbaf29adaa5d08cd5a05a138b62623f3f6505f7c46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2766759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4905c9f83f0ca70a8322d1e008aceec427e27fbe0ed5c96ff1a15e57229132`

```dockerfile
```

-	Layers:
	-	`sha256:103386f19eb0bf58edb1b6523bbcf8f37edc9903f87b6d72a6b86ccc5f79bcb8`  
		Last Modified: Fri, 08 May 2026 00:06:38 GMT  
		Size: 2.8 MB (2750193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68a8c1e81b2674dce9376b48e1c26f7d0f323322cf5d03d9b7266e4284e29c15`  
		Last Modified: Fri, 08 May 2026 00:06:38 GMT  
		Size: 16.6 KB (16566 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c023daa562d1ad168139ae24aea46c246fa70ae9d5db0824e732ecc2c1e78c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192809200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:245ca9ad9ccd259ca236d95e4d415eed6fde7fa9b0480f6288dd6b2fb0f39250`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:07:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:07:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:07:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:07:41 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:07:41 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:07:41 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:07:56 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:07:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:07:56 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:07:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:07:58 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664e60b116dcd5312df842254784f869b87cff3aba2dd3582dd24ddce22bf9c2`  
		Last Modified: Fri, 08 May 2026 00:08:20 GMT  
		Size: 142.6 MB (142582244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc1b45fc426274fad7d62eca4f0a798784085c43603482d836329e50c532053`  
		Last Modified: Fri, 08 May 2026 00:08:16 GMT  
		Size: 17.6 MB (17593063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8661d7c3977cd0ec1711a70cfb5c5a81e670e2517601841a306ece7ae94b351`  
		Last Modified: Fri, 08 May 2026 00:08:14 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8c9e4bb2c0d3cf0b88cc1d20e54c4badb532b0e752d78c44657accb5df357ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2767113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc28b3af680bbe0d0855364c27807a78c49b6d7885e3f6ee1f7ce6e72f9e0180`

```dockerfile
```

-	Layers:
	-	`sha256:ca102aef9b4425d7aecb11ce523881b2d1c86af47bdceace4d6f466fa0edd162`  
		Last Modified: Fri, 08 May 2026 00:08:14 GMT  
		Size: 2.8 MB (2750426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3caf1138a2d87d9930af1472b4e7924f4e44650785319a879539708a246e9d1`  
		Last Modified: Fri, 08 May 2026 00:08:14 GMT  
		Size: 16.7 KB (16687 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:3120e04bcff76f6924df91d20b527dc604ea80f156d1e27b9b770dbe73505d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187667649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06add360ba3df834759b49dfa950ce3bd0c7ad2e19517d83b33b1890fb25a48e`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:32:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:32:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:32:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:32:03 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:32:03 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:32:03 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:37:50 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:37:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:37:50 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:37:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:37:54 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:0bcb46f6315f7a2c8ddde875fca21de96c94e451046e6692f77a99aca489f3be`  
		Last Modified: Wed, 22 Apr 2026 00:15:02 GMT  
		Size: 32.1 MB (32078402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76ccb486cd38d4bc6e81d6a758dc0756e8388df36970ae898570b04b2565a95`  
		Last Modified: Fri, 08 May 2026 00:38:30 GMT  
		Size: 133.1 MB (133110145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c791f3c3459d541f7acd5246b21fe3d03cd54e2754cad81bbebbd87de910bb92`  
		Last Modified: Fri, 08 May 2026 00:38:28 GMT  
		Size: 18.0 MB (17961314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b841541b2a77d7a35b8cace7b8bf76f5051fd9e4e207791b1d6fed8d81a6704`  
		Last Modified: Fri, 08 May 2026 00:38:27 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b3ca5df562840c9419cfe0a06acffc71823f1266257976755e5d79816b695ac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2768021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c90b4c73991b853320babe073c8972f6c379476427b061d8afcd341b5663beaf`

```dockerfile
```

-	Layers:
	-	`sha256:bdcd46f44bf199bfd6b16f1698186a4795d46bccb2d5c04bbecd246d4792ab19`  
		Last Modified: Fri, 08 May 2026 00:38:27 GMT  
		Size: 2.8 MB (2751411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7293a5b5d3d888a94d55feefa21e3fdd0170d8aa4003e47f3ec82138fe06d85`  
		Last Modified: Fri, 08 May 2026 00:38:27 GMT  
		Size: 16.6 KB (16610 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:1073845fea06a914178d205933a302355b77a0e501eb7435d46f4bc97ba41892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175483998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ce9ab316be692f4ca9c384f099a0ebc0d1e5c987fb4395af2fd4af6cdb4bd7`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 29 Apr 2026 23:13:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:13:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:13:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:13:31 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 29 Apr 2026 23:13:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 29 Apr 2026 23:13:31 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:13:41 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 29 Apr 2026 23:13:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 29 Apr 2026 23:13:41 GMT
ENV LEIN_ROOT=1
# Wed, 29 Apr 2026 23:13:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 29 Apr 2026 23:13:42 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb51d1f6103c562773e5ad9b244bea0d905640ceeb1f8ac3e09c56a4396e5429`  
		Last Modified: Wed, 29 Apr 2026 23:14:06 GMT  
		Size: 126.7 MB (126652697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df2947cfb44a9c7361d06d2241f7704e2078535e5c5cfeb47b5ba2c5807b7c7`  
		Last Modified: Wed, 29 Apr 2026 23:14:05 GMT  
		Size: 17.4 MB (17421991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dff3bb9322504cb736b0b42224da7c4081ef898a7e0c4c4f446e60c669e34b1`  
		Last Modified: Wed, 29 Apr 2026 23:14:04 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1ca6425fd91ff74a7d89db603437bbba9c3c350efdb4e6441ee1ba8dc873e1f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2758423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7a801c79180886b18e2a1b747f8001485c2d127b62780f175fb16a44fafcd5`

```dockerfile
```

-	Layers:
	-	`sha256:e521abc0f61871380fe08eb46b886ced977fde445840294273d48970b3f931be`  
		Last Modified: Wed, 29 Apr 2026 23:14:04 GMT  
		Size: 2.7 MB (2742011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a7ce1d0705911edb6d8515907ef0c102c3dcc588259030928d0feaffdfda49`  
		Last Modified: Wed, 29 Apr 2026 23:14:04 GMT  
		Size: 16.4 KB (16412 bytes)  
		MIME: application/vnd.in-toto+json
