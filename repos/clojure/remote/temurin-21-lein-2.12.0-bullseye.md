## `clojure:temurin-21-lein-2.12.0-bullseye`

```console
$ docker pull clojure@sha256:144a48b95ee83af7e7b9baa22acec68335ce2b6405935abfa14a6d14dafe3251
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-2.12.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:5c1d6c2ab2452c04030a9f40a37b7ba7f060ab20d4e59fba4e2c1ddff0fc0d93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233077875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e137fb8d78a5ff50a8e355268f24e7ee0d264b9ff0cffc17352f511f2f4518d4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:17:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:17:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:17:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:17:59 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:17:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:17:59 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:18:15 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:18:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:18:15 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:18:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:18:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:18:16 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:18:16 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f846496bb8de82d45036689f323745541ec6bef545aa0582164c2254e8a2188`  
		Last Modified: Fri, 08 May 2026 20:18:38 GMT  
		Size: 158.2 MB (158166903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df7704f15324daf8f97507308c5d56b46a3880b69991278935cd29fb78c7add`  
		Last Modified: Fri, 08 May 2026 20:18:35 GMT  
		Size: 16.6 MB (16629503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aba66fe5c55aeb692b7c627daee8639e2f00fe4f92886d90f96b62185686511`  
		Last Modified: Fri, 08 May 2026 20:18:35 GMT  
		Size: 4.5 MB (4517696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b67d86d7a08f5fe85c1493036c21a75a3c89494222cd5538ef4e0e2c1b6897`  
		Last Modified: Fri, 08 May 2026 20:18:34 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c16507a743043599d0a2add1c97636847c5b482e377508470a373148a2f96d26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4506863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfa2633e3af3f3862825bf2ca68137698d1d4cf3bea8476fbc7753e319585a7`

```dockerfile
```

-	Layers:
	-	`sha256:73f259a64435aa99f04db8d9686b1dfce55f173f8f070f9a72a9826c21f3bf66`  
		Last Modified: Fri, 08 May 2026 20:18:34 GMT  
		Size: 4.5 MB (4488341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3937fce7cdc92302aa08a1ec82c160098d104abd85fd07891e9451525273b1a5`  
		Last Modified: Fri, 08 May 2026 20:18:34 GMT  
		Size: 18.5 KB (18522 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b4944678fc0d436b46de66339e68675899498d71d542670a965130698e0fb325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229849015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c66f78ff8bc828e2df93b98484714f03cfc72984a03ebdbd44a36170c36fb10`
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
# Fri, 08 May 2026 20:22:23 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:22:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:22:23 GMT
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
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84451bc36798ee1282d9987d1d686e77b64cfa6ff266bebbee37de634761ecd2`  
		Last Modified: Fri, 08 May 2026 20:22:44 GMT  
		Size: 156.5 MB (156461154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adb701b2b88fd667728f227233b10a7e89569bf3c42791b4f6e22d8f3a41d290`  
		Last Modified: Fri, 08 May 2026 20:22:43 GMT  
		Size: 16.6 MB (16616521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6282f0d2452468b472af11ec875889370bc2dc4ec32dac731589365a1fda30`  
		Last Modified: Fri, 08 May 2026 20:22:43 GMT  
		Size: 4.5 MB (4517700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288f951146c2fd4bb00f2f0f53409708fefd450c7639d58af8724dad73c9826a`  
		Last Modified: Fri, 08 May 2026 20:22:40 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:44b81d4dde145c32ac59bafaba512c11f5837d59ed7ad9223ad4eee8f8e35455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4505958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa45010adaf44107b64076c3732b54b777741e9caac7c5727090a56ce96ce040`

```dockerfile
```

-	Layers:
	-	`sha256:64896b458d37ff169a6b50236856fb21fd58f45298ad3f13a8e19289d97c9822`  
		Last Modified: Fri, 08 May 2026 20:22:42 GMT  
		Size: 4.5 MB (4487315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9284a2bbda5b3690f2fb8b6d1d0e8721d5c61aac31e65e384c5029f74f075483`  
		Last Modified: Fri, 08 May 2026 20:22:42 GMT  
		Size: 18.6 KB (18643 bytes)  
		MIME: application/vnd.in-toto+json
