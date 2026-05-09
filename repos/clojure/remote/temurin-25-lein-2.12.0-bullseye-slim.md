## `clojure:temurin-25-lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:73062dc151a46867847e296b32e259ad5bee2d36c1a63cdeb27b2d68e9de3ca5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-lein-2.12.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ce4c6d328174759ced44fbb5d1585a59dbbf8bed298a7bc494428129ff898f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142689562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c5d4bd982a66f4d3a3b12465f42dd28f128ad2c32840a23bfe12e413e62ebf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:19:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:19:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:19:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:19:00 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:19:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:19:00 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:19:13 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:19:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:19:13 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:19:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:19:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:19:15 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:19:15 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:77e30ef52aeb52d8466baf0f50b54ed2fc0b421f44c49e5bf93682b27110f4d3`  
		Last Modified: Fri, 08 May 2026 18:22:59 GMT  
		Size: 30.3 MB (30257958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bdf6695366c1bb144d4a724b94fd1e5b96f33ac91fdba58877d8954f67e0fe3`  
		Last Modified: Fri, 08 May 2026 20:19:33 GMT  
		Size: 92.6 MB (92574586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3198d45a424d2c2dcd49b47b563b3d2c4fe13ce91712f97e5f09079574709931`  
		Last Modified: Fri, 08 May 2026 20:19:32 GMT  
		Size: 15.3 MB (15338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e9a173a21db335bdc94afc2107a083f3b6d75648847b082798041d82003f9a`  
		Last Modified: Fri, 08 May 2026 20:19:31 GMT  
		Size: 4.5 MB (4517738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03243f6cf5d1d5427d13621f149289b972c1b51c1d2f3ff892dc311600b6250e`  
		Last Modified: Fri, 08 May 2026 20:19:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:70e357a5748135222ed3d10173a67c1350993cdb8efb2b80fb8f11224471b1ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe1edffeabb83d655f03559a39c1b4eac1620eb996d9e828cc348c3fc9c0f7e`

```dockerfile
```

-	Layers:
	-	`sha256:39b0595484eb3be53d32fa397884dffc610123ef4d9622be96fb6ec592370e23`  
		Last Modified: Fri, 08 May 2026 20:19:31 GMT  
		Size: 3.0 MB (2996265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4985e0697b1d6de9fbe1a5f20e4fa0394e696b2913d3c8d7b516e58fad709440`  
		Last Modified: Fri, 08 May 2026 20:19:31 GMT  
		Size: 19.2 KB (19212 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:217459f79911d8e0100c5aaeb0d6db60ad545e4d247b8bbfff3883ff4b628362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140130209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d12f098de9bda5673d3897ef9da8a0d03f7535125168143d7a2f65db585971a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:23:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:23:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:23:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:23:19 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:23:19 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:23:19 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:23:33 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:23:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:23:33 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:23:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:23:35 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:23:35 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:23:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ab0f13d792ff9100407906fb422a0b62a8b437abde4c245e03f0366814be9aae`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 28.7 MB (28742591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18782c5e12e03285d05285badc9e083c63ebc1aca95f23bfcd8390158c300b6`  
		Last Modified: Fri, 08 May 2026 20:23:53 GMT  
		Size: 91.5 MB (91542268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8090fa3a3aab61e4defc6747723ad667512c470062edbd2c635bcfe1d8f9989`  
		Last Modified: Fri, 08 May 2026 20:23:51 GMT  
		Size: 15.3 MB (15327177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10237ac8e5db58f6161060df01937c0427476c0be5947d51f511148b00fee089`  
		Last Modified: Fri, 08 May 2026 20:23:51 GMT  
		Size: 4.5 MB (4517743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2699688dcc24b3620b84f377837a1cad3de49d8ddeee42887ae73df865c64e0a`  
		Last Modified: Fri, 08 May 2026 20:23:50 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:33927f4ab13bc34d315b5dd66ae6d4702f445e53108d4b2a5d40ec5390b9ed0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3015252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12565d4b864d7570996303d7da2eb3ad6c3def2bc9162470d525a571681d3b8`

```dockerfile
```

-	Layers:
	-	`sha256:8aa72c93724f13d16ebfbc7d4a06f35634ed670f9f42fa4b02bbf49e3af6d5d0`  
		Last Modified: Fri, 08 May 2026 20:23:50 GMT  
		Size: 3.0 MB (2995895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6acddc3d12d24215f4c21565933fd548f898dc8dfaae6a4c5614365f98ad1f24`  
		Last Modified: Fri, 08 May 2026 20:23:50 GMT  
		Size: 19.4 KB (19357 bytes)  
		MIME: application/vnd.in-toto+json
