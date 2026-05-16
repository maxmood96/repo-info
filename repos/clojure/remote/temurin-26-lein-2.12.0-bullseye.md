## `clojure:temurin-26-lein-2.12.0-bullseye`

```console
$ docker pull clojure@sha256:730c6286b81b0bb3cbc028a02b27e211c9e77268bd04a4209969a0be4ec1a1d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-lein-2.12.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:8bd11fa82fb54baee290e40cab0165efcd03d676cd94b303df0148bc4c72cb3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169435407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50a07e3a97d7918eabba708f5d01985e5774067e11c66e51eff4e0c80f03523`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 15 May 2026 20:36:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:36:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:36:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:36:30 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 15 May 2026 20:36:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 15 May 2026 20:36:30 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:36:44 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 15 May 2026 20:36:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 15 May 2026 20:36:44 GMT
ENV LEIN_ROOT=1
# Fri, 15 May 2026 20:36:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 15 May 2026 20:36:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:36:45 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:36:45 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc625ab0122b565511ec9df67eb35a283228c6302fdb5fe92c8bc65aad7fa3d`  
		Last Modified: Fri, 15 May 2026 20:36:56 GMT  
		Size: 94.5 MB (94524372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f7d099aec3bd14cf4a41328b56412ae1b508cc919410c84ad633a7471efbbf`  
		Last Modified: Fri, 15 May 2026 20:37:03 GMT  
		Size: 16.6 MB (16629508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65299ba5c91dd9bd2fb11b16a357ac921bc5a1e4e3ca9347ac22b1f0b24e68b`  
		Last Modified: Fri, 15 May 2026 20:37:02 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78262310598009f73b644b02dd1e20e4bc0feeb67c0a8fe0fbca838891755708`  
		Last Modified: Fri, 15 May 2026 20:37:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:0f6aea242788e2bfc552e3131e49b1537a6c7383289573746dbd3026681b786e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4469895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8920d7e42d9f4fd04a12ac4ee848177ec684a1fb6557179260915da1f9f782f5`

```dockerfile
```

-	Layers:
	-	`sha256:fed87d4190d02168d07ae38c969ecc7e707dcf4f9fd77d26221eb5fa852890b5`  
		Last Modified: Fri, 15 May 2026 20:37:02 GMT  
		Size: 4.5 MB (4451380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c6e0e9ca6696c21c933d6553e2c36e42dfbcf76225c28383b9df8f356f64719`  
		Last Modified: Fri, 15 May 2026 20:37:02 GMT  
		Size: 18.5 KB (18515 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:22bc0dbe70a957fa49c50a9b7d256e59bacea98c2d2c9e85927c9e816e49a0c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166892352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aa44c94b1d044738592de50759bb62e0e15946c17e36ad1faaed0c448743b83`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 15 May 2026 20:35:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:35:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:35:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:35:58 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 15 May 2026 20:35:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 15 May 2026 20:35:58 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:36:11 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 15 May 2026 20:36:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 15 May 2026 20:36:11 GMT
ENV LEIN_ROOT=1
# Fri, 15 May 2026 20:36:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 15 May 2026 20:36:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:36:12 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:36:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0711e4c3ba63b66d51d59d6a3c1724c26d046a86e82e8bcfd8798d86c1c8e599`  
		Last Modified: Fri, 15 May 2026 20:36:32 GMT  
		Size: 93.5 MB (93504386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ecb60787f2ea593a2f204d63b34053814b69be81f12c5eed05d9f444da2647`  
		Last Modified: Fri, 15 May 2026 20:36:30 GMT  
		Size: 16.6 MB (16616612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f75024492684d0aca374a40f61f022097a721fddd04706419814f98e007a68`  
		Last Modified: Fri, 15 May 2026 20:36:29 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2bd974cda46163b81cc76156e3bf27cbdeb296cd82b3b221ea1b677ab4dc5d`  
		Last Modified: Fri, 15 May 2026 20:36:29 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2539b36fe95f78dcb4d53533c50ae0bcb88e75916fd89ea9e909dce53c7207e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4468987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e15680cfa27175048f978efb47901ecde428bb9128580f65fc08a4fa20a9921`

```dockerfile
```

-	Layers:
	-	`sha256:89e933f8a2192c7900094f99c10013ffae4e00f09f61fe40fe0c5263b6f1e4be`  
		Last Modified: Fri, 15 May 2026 20:36:30 GMT  
		Size: 4.5 MB (4450351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5da2011a77cc7cbdb568a92446c11df8fecee16c9f2a264ef4fe0ebae3ce619`  
		Last Modified: Fri, 15 May 2026 20:36:29 GMT  
		Size: 18.6 KB (18636 bytes)  
		MIME: application/vnd.in-toto+json
