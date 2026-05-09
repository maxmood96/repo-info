## `clojure:temurin-21-lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:f488e8564263f57a7e9200dc86d384b677c790d14014729406a83085e99add9f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-2.12.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2d91f512ca5fbf4ae4bc25f1d0a46b5036cb7e26ad5bf4ee520e9f9fb37ed847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208281886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e61585d5fcc94b134393509ebc5113ec9e8ef872b1e984dad5fd59f4a40a1029`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:18:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:18:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:18:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:18:02 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:18:02 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:18:03 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:18:17 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:18:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:18:17 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:18:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:18:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:18:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:18:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:77e30ef52aeb52d8466baf0f50b54ed2fc0b421f44c49e5bf93682b27110f4d3`  
		Last Modified: Fri, 08 May 2026 18:22:59 GMT  
		Size: 30.3 MB (30257958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6711bb39824c6b11d8931bc81a611b09e270928c5deddf5a5f391376ef81f09a`  
		Last Modified: Fri, 08 May 2026 20:18:40 GMT  
		Size: 158.2 MB (158166936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969676f95ffaf41f85856bdb5384c37a0ab993969382255930b8a1f47cdda36f`  
		Last Modified: Fri, 08 May 2026 20:18:36 GMT  
		Size: 15.3 MB (15338844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55943ff9a8ee6b9016825e0890dc340c1380616f4746529c1ce5237cb6eafd8`  
		Last Modified: Fri, 08 May 2026 20:18:35 GMT  
		Size: 4.5 MB (4517720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041d29035fab69cbd84691c135bf8d05fbd48d50e6eb35329d9e211f2a62f401`  
		Last Modified: Fri, 08 May 2026 20:18:34 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0aeb0c476078149a52d0ea0a83ac311b69c753dcf62f04eb52d24032f94c29f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3048618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7d48fa54c653a6bce1b5c3561c86dd55956dea231ec2480d05298fe148a4379`

```dockerfile
```

-	Layers:
	-	`sha256:3eb67a570c187a4a9466f27630a8e0d5859862e48d35d64c009cf58b3a513293`  
		Last Modified: Fri, 08 May 2026 20:18:35 GMT  
		Size: 3.0 MB (3030061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b36b6194495b853c4cb1d13e2227642a3ef3dde04211cb053415b912e6eb7d5`  
		Last Modified: Fri, 08 May 2026 20:18:34 GMT  
		Size: 18.6 KB (18557 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:19502a3f562dca66e674e703f3ca4f9f06c558ed1e4dad8365fc9399be4f5370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (205049102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657bd2f4624d11c961c1a35b7888ea78234092f8a9485c4feb6c083a3a86e48b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:22:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:22:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:22:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:22:09 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:22:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:22:09 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:22:22 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:22:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:22:22 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:22:24 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:22:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:22:24 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:22:24 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ab0f13d792ff9100407906fb422a0b62a8b437abde4c245e03f0366814be9aae`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 28.7 MB (28742591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84451bc36798ee1282d9987d1d686e77b64cfa6ff266bebbee37de634761ecd2`  
		Last Modified: Fri, 08 May 2026 20:22:44 GMT  
		Size: 156.5 MB (156461154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931f2abac9f083283d75d1aff091dcb7917879f204d1984b3dc168fd013a6455`  
		Last Modified: Fri, 08 May 2026 20:22:41 GMT  
		Size: 15.3 MB (15327205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c975deb844af68104d13e8e3c6c95db464f9daab282f894594291d20546abac8`  
		Last Modified: Fri, 08 May 2026 20:22:41 GMT  
		Size: 4.5 MB (4517722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288f951146c2fd4bb00f2f0f53409708fefd450c7639d58af8724dad73c9826a`  
		Last Modified: Fri, 08 May 2026 20:22:40 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f7498805d5332b87158f577af3991df3b8592ed36f43dea1578fe4e92e34b860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3048348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9048923393f360e82b8e4f534b63d196cb7ed94f524987447c781f59932149`

```dockerfile
```

-	Layers:
	-	`sha256:3741a77a5935ae0d59243863db614dc908a73e2ca9c3a7c5e0b5fe4c6068f1e9`  
		Last Modified: Fri, 08 May 2026 20:22:41 GMT  
		Size: 3.0 MB (3029670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f2af74cef3e078ad490689ff73c2d78ee6737588d945de85d6eb76672ab501f`  
		Last Modified: Fri, 08 May 2026 20:22:40 GMT  
		Size: 18.7 KB (18678 bytes)  
		MIME: application/vnd.in-toto+json
