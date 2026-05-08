## `clojure:temurin-25-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:7ccc691c2bb239fb8f7a03f3803c7bbbdfada74b748edb1736d335eaa738216c
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

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6e9b9ca89dbe771aa5b614d7544126d9fcfca5c237dc3157256edfa3482becc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143088585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c9432818e85c3258120fa7a603aa2f89aecf735579e92b82c53adcf6625301`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Thu, 30 Apr 2026 23:52:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:52:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:52:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:52:54 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 30 Apr 2026 23:52:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 30 Apr 2026 23:52:54 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:53:08 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 30 Apr 2026 23:53:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 30 Apr 2026 23:53:08 GMT
ENV LEIN_ROOT=1
# Thu, 30 Apr 2026 23:53:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 30 Apr 2026 23:53:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:53:09 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:53:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1779936b18f2ba80705eaba06523b8b6c3131cc07b2c7b7d4ac4ecb62adc51e`  
		Last Modified: Thu, 30 Apr 2026 23:53:27 GMT  
		Size: 92.6 MB (92574598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aefb646d5088d67c173c954fe357f732a489351ddb17a17431b6c4565391abe`  
		Last Modified: Thu, 30 Apr 2026 23:53:25 GMT  
		Size: 17.8 MB (17759593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224a545ad35e09a96156c5794684b3a31d69819db254fbd2cebec7765ec9c077`  
		Last Modified: Thu, 30 Apr 2026 23:53:24 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0cde348af56716aa93ad83bcf923ed098785cd6b6af17c79788b55d011ab3e`  
		Last Modified: Thu, 30 Apr 2026 23:53:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:db9591a5cc6965c62697dcc71492602a73d811ed0db99094f993263da2a6ea04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2717791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d962149c348a9cf3fe88c8dfcba280a5916406b7da8ad87ea040b3ec07873a03`

```dockerfile
```

-	Layers:
	-	`sha256:b0d1b48206d53ef11adbdd55d9b19936c91ac5e11bd4e6a51c162409e7a993ca`  
		Last Modified: Thu, 30 Apr 2026 23:53:24 GMT  
		Size: 2.7 MB (2698733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56b57b134e144abac1b13239bb678af56be4136906a44e652c70b1c490eb69f9`  
		Last Modified: Thu, 30 Apr 2026 23:53:24 GMT  
		Size: 19.1 KB (19058 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9b7338da0df5b4fc9afe7091a3355cac7ab7953d7f0b28fd368e3078fff55ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141769603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:448201db953207f4c459f588dcbd6424e9b9c29e27108e551c5590f614dce3c3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:26:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:26:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:26:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:26:58 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:26:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:26:58 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:27:12 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:27:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:27:12 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:27:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:27:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:27:14 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:27:14 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a495a1617ef5a0c526f4d1765362fe4528bff997346f7c910b40cb875e318bcd`  
		Last Modified: Fri, 08 May 2026 00:27:32 GMT  
		Size: 91.5 MB (91542267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fe2cd2da57de8dfe3a876b5270d11ee94b455603f5fc1a76b040c225822abb`  
		Last Modified: Fri, 08 May 2026 00:27:31 GMT  
		Size: 17.6 MB (17593065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdcce9e4ec5e5fb5f073b48c94328c1f83629a54d513faea2aed0e3e2be9ec5`  
		Last Modified: Fri, 08 May 2026 00:27:30 GMT  
		Size: 4.5 MB (4517729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23caff61650d0fa85bce60d493ff834c99c30b317486601edd9e4820d09a20fd`  
		Last Modified: Fri, 08 May 2026 00:27:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ca63dd15071cf5f738af9debfe115011e70ba1d872e8f1290e5d179772a612ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2717726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fe3099d7794cd7a90c375b51b46dd706d3d4343c7fc49fc0a04c60a4a64b541`

```dockerfile
```

-	Layers:
	-	`sha256:737a4597334f4967ecbf111c94e7afb1cfbf88ebbe49359d358eebaf403fbb8d`  
		Last Modified: Fri, 08 May 2026 00:27:30 GMT  
		Size: 2.7 MB (2698369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98ce3a4c37b6e38cc23dae95a13bf745f7690ef0688d3f3afdb912981770292a`  
		Last Modified: Fri, 08 May 2026 00:27:30 GMT  
		Size: 19.4 KB (19357 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:8d1c89e086c336a061c2579000318c690e78f9678648dce6fd82080ea372f2f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146471939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ab3646525799a834c431495de1c69a3fa5d2ced545af1314eb024fbb7c1364`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 01:43:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 01:43:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 01:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 01:43:56 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 01:43:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 01:43:56 GMT
WORKDIR /tmp
# Fri, 08 May 2026 01:44:37 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 01:44:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 01:44:37 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 01:44:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 01:44:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 01:44:42 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 01:44:42 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0bcb46f6315f7a2c8ddde875fca21de96c94e451046e6692f77a99aca489f3be`  
		Last Modified: Wed, 22 Apr 2026 00:15:02 GMT  
		Size: 32.1 MB (32078402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de1619367effbb8009b986da2ea9fbc4fb9ea6adb3d628cb1ec99649f247618`  
		Last Modified: Fri, 08 May 2026 01:45:16 GMT  
		Size: 91.9 MB (91914008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04147a14efd079f09579035ff8f47b7906c74945cb73748252e38be066c66c8b`  
		Last Modified: Fri, 08 May 2026 01:45:14 GMT  
		Size: 18.0 MB (17961353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce1379bdf4712c3b38dec097678550de8cf3bee45421aca03ec9a8906f28f18`  
		Last Modified: Fri, 08 May 2026 01:45:14 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365882b7054523ae69b0caa8ce305241d2d2c4434508fee016af4c628a65af12`  
		Last Modified: Fri, 08 May 2026 01:45:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e399b2a32aadaf755dd107b8b8d80b35e0893012b68a5cfa2c3f0ab528a7f488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2703158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a87ae73a4fcc9d3c85a8aad20f32d4d41d2e2d7a51e6ef735d1c752b53dc7151`

```dockerfile
```

-	Layers:
	-	`sha256:6169cf8137d3db1215755298d9e684432631f0bfb19fac7781aeb63336960266`  
		Last Modified: Fri, 08 May 2026 01:45:14 GMT  
		Size: 2.7 MB (2683890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:363654b67ee91f893f36d75d08c90826054f8179ae7247e018970084b9ba5e4e`  
		Last Modified: Fri, 08 May 2026 01:45:13 GMT  
		Size: 19.3 KB (19268 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:e2d2f986e92e9293ff424a50ed38fdd273b1d7dc3efa1e956d69ff0be42aa522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137252057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dc059208ab916b946bfe2ade0c7e98d8c64d37448741266df121a8ba9f8a949`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Thu, 30 Apr 2026 23:50:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:50:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:50:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:50:05 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 30 Apr 2026 23:50:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 30 Apr 2026 23:50:05 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:50:16 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 30 Apr 2026 23:50:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 30 Apr 2026 23:50:16 GMT
ENV LEIN_ROOT=1
# Thu, 30 Apr 2026 23:50:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 30 Apr 2026 23:50:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:50:18 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:50:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704d003fe83fa56fc5a01331019c043d445770deca81dbbb54efeaa0262d16e4`  
		Last Modified: Thu, 30 Apr 2026 23:50:44 GMT  
		Size: 88.4 MB (88420323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098a3c88cc507c3632c767e4c4cc737c022e59c8f8f7dca691fa253049459d8f`  
		Last Modified: Thu, 30 Apr 2026 23:50:43 GMT  
		Size: 17.4 MB (17421986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:399e2535b9f96661c8eea490648eb6d636be0bcb6ed29c3ee2fccb96fabeada3`  
		Last Modified: Thu, 30 Apr 2026 23:50:42 GMT  
		Size: 4.5 MB (4517757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c72954149a55469c29a816d5fe99e89a25be2277a40030ec841a93eff578e3`  
		Last Modified: Thu, 30 Apr 2026 23:50:42 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e019ccc1195e8e397e46a17d3e88ec576cf77b5a0312fa5b4e21a66108926e4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6988d576f384ad09f076c65ea3fadfb91587fccf9078f9f5cf01e1d26bd261dd`

```dockerfile
```

-	Layers:
	-	`sha256:c1e3fcdf17491739d4a75e2a6726190f76d88b487b5ff2ddb5171debccc99001`  
		Last Modified: Thu, 30 Apr 2026 23:50:42 GMT  
		Size: 2.7 MB (2675109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4016f7e403b54b22d93900871f7848855cc28d7e3f2fbe20dcc55ea16e1537e3`  
		Last Modified: Thu, 30 Apr 2026 23:50:42 GMT  
		Size: 19.1 KB (19058 bytes)  
		MIME: application/vnd.in-toto+json
