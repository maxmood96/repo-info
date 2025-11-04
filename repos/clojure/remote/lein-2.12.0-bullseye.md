## `clojure:lein-2.12.0-bullseye`

```console
$ docker pull clojure@sha256:6a3b9c92ab46a8a4dc4c0637f2aa28354b2e1f431bbc8c82b3f0e496bbae7f64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:lein-2.12.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:fd5988e53fe563102e6ea6566c64b30bf90badbdf56d78f1eacbc6004dda993f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166918467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:929b236b36af61f6d65b49fd3f23fcbc3f1acb7d81594665fdff1f48977d8c7e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:56:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:56:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:56:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:56:31 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 00:56:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 00:56:31 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:56:46 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 00:56:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 00:56:46 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 00:56:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 00:56:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:56:48 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:56:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81652aae210cbbdc5bfc8f2db28e1f9da00af16ddcb642229bfadf8d1f6aad8d`  
		Last Modified: Tue, 04 Nov 2025 00:57:39 GMT  
		Size: 92.0 MB (92036035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea64a553b5fbdb51c184f40df23724697e3b57ac0789acdf10ff4893c377ed37`  
		Last Modified: Tue, 04 Nov 2025 00:57:28 GMT  
		Size: 16.6 MB (16607564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b15746bf3d595984c6be70f7c9aef7e79cc1ae7a82e62908c77c4b17ba7c87`  
		Last Modified: Tue, 04 Nov 2025 00:57:27 GMT  
		Size: 4.5 MB (4517745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71849c860c735000f237bfbf1e4a5e215d01776444240b84f4f2a1396fe48e50`  
		Last Modified: Tue, 04 Nov 2025 00:57:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:0cd9b42909f022891153415e143a0ef743d48b6c952537ecefabf5ca3dcdc479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4446483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba25b94617432898c8d589e7dbe7b39b043c776b2779143ca511a49b0adfe4b`

```dockerfile
```

-	Layers:
	-	`sha256:f4efeab533744112095dae4d94cead1634e8a04360de71b5b5479860a3533a25`  
		Last Modified: Tue, 04 Nov 2025 10:35:09 GMT  
		Size: 4.4 MB (4427480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3674875b31eb6fe391d277021bd2c5a1a2a74326c15b6c2400c7c88d556cdcc5`  
		Last Modified: Tue, 04 Nov 2025 10:35:10 GMT  
		Size: 19.0 KB (19003 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:35d1ab0786d7882e3d8db265785868c5bb117e68cad0b1c8d25c727f4fc14227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.4 MB (164416362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e08b2c0c05da283c0089f2d3f2302ddf6d98c5063be65aa26781c01f8968cc6f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:57:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:57:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:57:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:57:04 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 04 Nov 2025 00:57:04 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 04 Nov 2025 00:57:04 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:57:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 04 Nov 2025 00:57:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 04 Nov 2025 00:57:18 GMT
ENV LEIN_ROOT=1
# Tue, 04 Nov 2025 00:57:19 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 04 Nov 2025 00:57:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:57:20 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:57:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd9ece75df292c8f7586a75a70e5f9644d5bd242a3054c6d8729f2b729c31f4d`  
		Last Modified: Tue, 04 Nov 2025 00:57:56 GMT  
		Size: 91.0 MB (91045257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce8cb6c4a0d99a845b8052bfe6a876058f270d9112f14cdf0710455d8f49b24e`  
		Last Modified: Tue, 04 Nov 2025 00:57:47 GMT  
		Size: 16.6 MB (16594996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c2437625988222e796e04fba5d7188a6a0d331556a023a54585af35c880217`  
		Last Modified: Tue, 04 Nov 2025 00:57:46 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f363dc2fb24ce1c85f36e9bb7d97bc3e6af11f407282745c7888f52c5e7829`  
		Last Modified: Tue, 04 Nov 2025 00:57:45 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f41da600923ce91544989191ff4e06e3e7d8a262b40318cbae9447e4a3160048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4445623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9feb9f8ce563bc15f817de5fbb0c5b909435041deb0391cf09c17e4a1677d10c`

```dockerfile
```

-	Layers:
	-	`sha256:c994974bc18fe30615e9237eb051e49ae998866ee78aea459f67ad88b10a161a`  
		Last Modified: Tue, 04 Nov 2025 10:35:14 GMT  
		Size: 4.4 MB (4426475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:babcb8eab570456a9bf2dfe82d3e1b241e54247f7990a97ecb1f77501b3825d9`  
		Last Modified: Tue, 04 Nov 2025 10:35:15 GMT  
		Size: 19.1 KB (19148 bytes)  
		MIME: application/vnd.in-toto+json
