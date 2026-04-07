## `clojure:temurin-8-lein-2.12.0-bullseye`

```console
$ docker pull clojure@sha256:59f8c19cf902efde2e8e2cd8c8f07594d402a968a8b4f8f1843012ed9d9d06a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-lein-2.12.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:82fb2359a629f117fd3d62a03909cbdaa2a549d88f623f67788f2b78946f8c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130080164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636f97c803b3bf7b9341490b48dc89396cea133881fa88923fc3407e5e3a51ed`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 03:12:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:12:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:12:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:12:12 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:12:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:12:12 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:12:25 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:12:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:12:25 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:12:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:12:26 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1398ff8bbce5d60fb09f8f7de303465fc385ef7fdcc5cf3cc79d8ed03becdf16`  
		Last Modified: Tue, 07 Apr 2026 03:12:40 GMT  
		Size: 55.2 MB (55170110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2691f145c4197ed0b30f56f06a0cf3df80fbd7b9a1da9cc989c72e83ea3b467f`  
		Last Modified: Tue, 07 Apr 2026 03:12:39 GMT  
		Size: 16.6 MB (16629516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29940c5b7f86f4191d5e5201c92b7e16a98175d3ffac1a030764bd83132f096`  
		Last Modified: Tue, 07 Apr 2026 03:12:39 GMT  
		Size: 4.5 MB (4517713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c1ccd861721332100233a4099db6ea551bf85fb0fd3d306c924d4b39835f8707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4623221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead031f843142acae86992f630c589232e75e578c22256056e3824fef6b48ef8`

```dockerfile
```

-	Layers:
	-	`sha256:b930ee2e211cccfb5e447228dabc8f4741ba194396632692c4b1480a5fd89fdd`  
		Last Modified: Tue, 07 Apr 2026 03:12:38 GMT  
		Size: 4.6 MB (4606851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7baeb7c38f2adb6ba25f4f3538c2bda17a82e0d0f5cdad92830a4a761950b118`  
		Last Modified: Tue, 07 Apr 2026 03:12:38 GMT  
		Size: 16.4 KB (16370 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:61bd44b48784e664d28502e87f7da8652fd2faaf55c9ad42a2d6ce6bb16ce0ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127633552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d8eba2a948a443e14b3e1388485e8eb724b2890a75526c9b795083b0528fe5`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 03:22:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:22:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:22:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:22:54 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:22:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:22:54 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:23:08 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:23:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:23:08 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:23:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:23:10 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d07348fd56265119cabe0caa2d4f84f1b04544c12ba5553af3975a2a82e88aa`  
		Last Modified: Tue, 07 Apr 2026 03:23:25 GMT  
		Size: 54.3 MB (54251622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c52c5ce42db598e3c028304dc5f281746edea78023f45d6e48e2202a3e1bbcd`  
		Last Modified: Tue, 07 Apr 2026 03:23:24 GMT  
		Size: 16.6 MB (16616552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361827a96d22a9bb52ec65a59dbe91abd8099cd33399745e8d42397004572789`  
		Last Modified: Tue, 07 Apr 2026 03:23:24 GMT  
		Size: 4.5 MB (4517731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:ce6842e35eda2b0a1fd9c4face2be5dea631ba959147be4267a7fab70ace93bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4623016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3241d5562b625af9e946e296561b5e49ee7ff8b8460a1eff1c7dbe75c4937e85`

```dockerfile
```

-	Layers:
	-	`sha256:5810e0915db3336b454d7f53c438daf5e3bc3b1aaf4e441d3bfd3211056d2758`  
		Last Modified: Tue, 07 Apr 2026 03:23:24 GMT  
		Size: 4.6 MB (4606525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b34f90a60c8c34c1616f076b3871b3a18da14d0e92cc39533443cb16eab24fee`  
		Last Modified: Tue, 07 Apr 2026 03:23:23 GMT  
		Size: 16.5 KB (16491 bytes)  
		MIME: application/vnd.in-toto+json
