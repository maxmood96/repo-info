## `clojure:lein-bookworm-slim`

```console
$ docker pull clojure@sha256:40b9f63d0d07d2aa66de26d76eb19196987dad5e180eff04b69c135701375b41
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

### `clojure:lein-bookworm-slim` - linux; amd64

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

### `clojure:lein-bookworm-slim` - unknown; unknown

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

### `clojure:lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:56632f664b2c129149e209835aadfe9b834fb0732a2352111841ef58cac76ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141769628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15cf4972166e2c90a054adfa58a1cdd10ccfcd9e44a12cf1ff55f824409fdb21`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Thu, 30 Apr 2026 23:52:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:52:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:52:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:52:33 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 30 Apr 2026 23:52:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 30 Apr 2026 23:52:33 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:52:46 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 30 Apr 2026 23:52:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 30 Apr 2026 23:52:46 GMT
ENV LEIN_ROOT=1
# Thu, 30 Apr 2026 23:52:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 30 Apr 2026 23:52:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:52:48 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:52:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41125abbaae815b8fe9cd697a1d0399c3cf22d9fb311601a1bbbeeca0820963b`  
		Last Modified: Thu, 30 Apr 2026 23:53:06 GMT  
		Size: 91.5 MB (91542288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea25aa937fa58dceecf64a3128c852b2617c03ebf73ac5244d5a5fde441868f`  
		Last Modified: Thu, 30 Apr 2026 23:53:05 GMT  
		Size: 17.6 MB (17593075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae2259f603b5386936703599d76b4c2286e400f7688e67e5495463740ddad0a`  
		Last Modified: Thu, 30 Apr 2026 23:53:04 GMT  
		Size: 4.5 MB (4517723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f7855affc373e7653fffdfd60d5ffc9e0fbfd15a38a1bc72d96be0023e4f1c`  
		Last Modified: Thu, 30 Apr 2026 23:53:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:df4bc8cb023998715e35cebf4f4b4c150e970b81171c74e0fbc8145a6ca6d8cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2717572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b117cf702f2a6db26e94a70de8f0984eab9a4e7987554788305b8d4373b29a`

```dockerfile
```

-	Layers:
	-	`sha256:6096e9817cd0e52e5aa119bd0c28efab9d46b2b7fcd0a49f4683e616708b9c0d`  
		Last Modified: Thu, 30 Apr 2026 23:53:04 GMT  
		Size: 2.7 MB (2698369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2693dc248d9b839b24ec06eaf1ee3b60f01090c5dd21e779738d75daad293acb`  
		Last Modified: Thu, 30 Apr 2026 23:53:03 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:41b4afb69e3bff07d1dd9c8d56fe2b2e07f05ad06dd902098e13c53d3bfcb538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146471906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69b9215d06b40d3479e2fc21f85f5e7102b432d99bf008e5c06a42d6ac75e0e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Fri, 01 May 2026 00:08:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 May 2026 00:08:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 01 May 2026 00:08:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:08:52 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 01 May 2026 00:08:52 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 01 May 2026 00:08:53 GMT
WORKDIR /tmp
# Fri, 01 May 2026 00:09:27 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 01 May 2026 00:09:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 01 May 2026 00:09:27 GMT
ENV LEIN_ROOT=1
# Fri, 01 May 2026 00:09:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 01 May 2026 00:09:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 01 May 2026 00:09:31 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 01 May 2026 00:09:31 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0bcb46f6315f7a2c8ddde875fca21de96c94e451046e6692f77a99aca489f3be`  
		Last Modified: Wed, 22 Apr 2026 00:15:02 GMT  
		Size: 32.1 MB (32078402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b864cb58d14d804b69aef93f888801a5a40998b4ed809b787a8c67eb93313014`  
		Last Modified: Fri, 01 May 2026 00:10:07 GMT  
		Size: 91.9 MB (91914022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82df78b489ab0bf0ba9455b34c61ac72e361d85599126358ae45dc638023b36c`  
		Last Modified: Fri, 01 May 2026 00:10:06 GMT  
		Size: 18.0 MB (17961337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36313569cc5f4bf59c4bafe3955af53127c74b2ec47818cb8d668881a7f9e817`  
		Last Modified: Fri, 01 May 2026 00:10:05 GMT  
		Size: 4.5 MB (4517717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1924964612a8cf09ccf4e1d5120aba363e19d67c0ad278cc2c3fec8842802e`  
		Last Modified: Fri, 01 May 2026 00:10:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0f6b15085182aecd7ff6b70fd0b960b75da7479a3893108322869e8b747a4964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2703004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4ea6cfcd9ef809743b81384ce93d0ec1966832d5523a32a7301924f0b961ad`

```dockerfile
```

-	Layers:
	-	`sha256:ba5c340b18850b8d41687c0fca8c8dc654d20153ed898c13fb8ae48ffaac9ba9`  
		Last Modified: Fri, 01 May 2026 00:10:05 GMT  
		Size: 2.7 MB (2683890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d22ec7f9436154ee2266e83e227abf2774b0b9dd80da1428761c8a6052dcd09b`  
		Last Modified: Fri, 01 May 2026 00:10:05 GMT  
		Size: 19.1 KB (19114 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-bookworm-slim` - linux; s390x

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

### `clojure:lein-bookworm-slim` - unknown; unknown

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
