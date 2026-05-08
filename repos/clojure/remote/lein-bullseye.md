## `clojure:lein-bullseye`

```console
$ docker pull clojure@sha256:0c3c1d78c5a495a992bb52ab565cffb4d0e065b442a607d0926b20a988ae5ff5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:72daf2ae6c0012c689da6a7cc48fb109322a73d3312de1c6d8bc15f00b562d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167485464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5992558d5f2e5d1574036c9da6e1e6873029eb5d8c3306c4e786dbbbec96d83c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Thu, 30 Apr 2026 23:52:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:52:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:52:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:52:55 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 30 Apr 2026 23:52:55 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 30 Apr 2026 23:52:55 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:53:09 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 30 Apr 2026 23:53:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 30 Apr 2026 23:53:09 GMT
ENV LEIN_ROOT=1
# Thu, 30 Apr 2026 23:53:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 30 Apr 2026 23:53:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:53:10 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:53:10 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:54a03544060169d4b3f081ec8b02433016510da63c54baa3c2da97d8d0f1e9cc`  
		Last Modified: Wed, 22 Apr 2026 00:16:31 GMT  
		Size: 53.8 MB (53763152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1779936b18f2ba80705eaba06523b8b6c3131cc07b2c7b7d4ac4ecb62adc51e`  
		Last Modified: Thu, 30 Apr 2026 23:53:27 GMT  
		Size: 92.6 MB (92574598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0cd744eb5734362e59d96c51e7459ca094c4e33b1c0d72a92ff58f8a266a4e`  
		Last Modified: Thu, 30 Apr 2026 23:53:26 GMT  
		Size: 16.6 MB (16629541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eda4beeb1186fa9dd03230aacc19a5d01a8138c4b9d838119bf3b7d5f7e8219`  
		Last Modified: Thu, 30 Apr 2026 23:53:25 GMT  
		Size: 4.5 MB (4517745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980c903c8b12c395bc3a410de07664fad187eebaac8ea18ab0b01b616c10daf0`  
		Last Modified: Thu, 30 Apr 2026 23:53:25 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1fd214cb4d163047de27e18e46a1ad0d2a47a2dbed9fca4e40f7211049b9bb0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4473528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a867b14bdef0605fbfc064b20931ae68db625ac06ce879669bac5a5cc26e9e9`

```dockerfile
```

-	Layers:
	-	`sha256:966bab8ee944f822843433533d57e1c8af856afa9c2c5604f21f45f47cf09417`  
		Last Modified: Thu, 30 Apr 2026 23:53:25 GMT  
		Size: 4.5 MB (4454525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6011129fb7dac1a684285378e5eca2931074d099c0f009742e2c7139b5f111ed`  
		Last Modified: Thu, 30 Apr 2026 23:53:25 GMT  
		Size: 19.0 KB (19003 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d55300324e43a9273f9dae47e3a25d1c08c0034f9f2beefccbc0596328af448c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.9 MB (164929907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf4dfae64b6d2c0af3f4711aee52cd3cf716b95cc7dce4f7c9558492bfd7e45`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Fri, 08 May 2026 00:27:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:27:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:27:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:27:09 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:27:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:27:09 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:27:23 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:27:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:27:23 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:27:24 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:27:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:27:24 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:27:24 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2ba2d04412a926ea9f6ebac8d3d6d5738f9d008c45d94fd00311d3be4637e4`  
		Last Modified: Fri, 08 May 2026 00:27:44 GMT  
		Size: 91.5 MB (91542275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44074d7151de6fef0b171e25bca37e32ea9abbed5eccd2c5fb6d015789945e8b`  
		Last Modified: Fri, 08 May 2026 00:27:42 GMT  
		Size: 16.6 MB (16616499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ffe9e29b4c44537b17b187bf18990e1e7c069e5891931d19c4005dcfb0386dd`  
		Last Modified: Fri, 08 May 2026 00:27:42 GMT  
		Size: 4.5 MB (4517703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9096672a7ae4df68de87be7c14747bed4b4f8954843f3cc513c1e5afedadb52b`  
		Last Modified: Fri, 08 May 2026 00:27:41 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b5b7c8c73c04ee2df09c60919d52643b3081e909ee06a1cc689ab0f857d73654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4472821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be6d02703e3311604df38b9274a90bb233dbc3f8ad446a96392e29942a4eb04`

```dockerfile
```

-	Layers:
	-	`sha256:2f78f46f7a2d98867d658d5cb19abe8fc10e5b03e34cdf8be9022d23e5fb1f8d`  
		Last Modified: Fri, 08 May 2026 00:27:42 GMT  
		Size: 4.5 MB (4453520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56f29ba386ed26c5240710a63b3e455148afe119ae8356d8041115d765add0dc`  
		Last Modified: Fri, 08 May 2026 00:27:41 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.in-toto+json
