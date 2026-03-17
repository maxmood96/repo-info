## `clojure:temurin-21-lein-2.12.0-bullseye`

```console
$ docker pull clojure@sha256:f74a83e9d7f24508dd47e67f0cd14fbb9c906f88597393c2b202a43f40578564
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-2.12.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:7a1d7c879981faa407bdb5595488ec58a6ab05e402ece5dc8e7a9f7d81cc8232
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232767202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4d0e0e6daefa00f9057ddbc437ace2b2818de17c855ef3128f233e659182c93`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 02:59:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:59:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:59:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:00 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 02:59:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 02:59:00 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:59:13 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 02:59:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 02:59:13 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 02:59:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 02:59:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 02:59:15 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 02:59:15 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e759575b5b0029fea51256b7ad3afa90c8ff1a6a9457787359c2b05b4a964edd`  
		Last Modified: Mon, 16 Mar 2026 21:52:53 GMT  
		Size: 53.8 MB (53762481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088e979cb2fb1d2494e2eadca33d30761342621b61f8f00c4d40673685b8ccb7`  
		Last Modified: Tue, 17 Mar 2026 02:59:36 GMT  
		Size: 157.9 MB (157857117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f224c93fbe31abf243bd8947e319b3db888ecd6b7ddeaf800b438fc647d041`  
		Last Modified: Tue, 17 Mar 2026 02:59:33 GMT  
		Size: 16.6 MB (16629437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35ddd38f180da8ac617e3cb974f840588106509ac63458435ae01fdda32d07c`  
		Last Modified: Tue, 17 Mar 2026 02:59:33 GMT  
		Size: 4.5 MB (4517738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f74ae426b2781d2a75d4a010432dccd737c9f62489682afbf845adf4d10ce8`  
		Last Modified: Tue, 17 Mar 2026 02:59:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:225f4eaacec2e812ab73fe97161a5f7ee2187926ba8ac11940856d2d36c63171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4506082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb6a0828eb1e06ed3f1bcec284d46b5b52f69dcc62a36f8eaf50ed867941c8a7`

```dockerfile
```

-	Layers:
	-	`sha256:82eb62ade5b66136a36828215267d5cc3214beffe44b1afc9d60523a7a6fea68`  
		Last Modified: Tue, 17 Mar 2026 02:59:33 GMT  
		Size: 4.5 MB (4487714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74adc4cbc7c1c65ef8f06ae4b2d9eb5215a88f92762f6b9478ab8dcbe6107b1c`  
		Last Modified: Tue, 17 Mar 2026 02:59:32 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d2e555bfa3dca76ecd5ed997416e3e9f4dfab2566ec5f6547f5de3f0b2bba25a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229514898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe50fbf338a7054b6c5dac81ae701418a6ca98c0982871efa5eebf4f2cf13e7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 03:04:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:04:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:04:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:04:07 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 03:04:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 03:04:07 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:04:22 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 03:04:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 03:04:22 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 03:04:23 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 03:04:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:04:23 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:04:23 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:da8e260297fdb91b3f012b26dd982feb43d0bf977ff8adeb7a850ef9c5829770`  
		Last Modified: Mon, 16 Mar 2026 21:52:51 GMT  
		Size: 52.2 MB (52247254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152ddccac770f128c404ba512d77114e9abdb176b7523fbe1b172309c42f77ca`  
		Last Modified: Tue, 17 Mar 2026 03:04:50 GMT  
		Size: 156.1 MB (156133026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1683816f6a0b6d5d69f46982b4da4f2a64cfbd5320a8b663386363dd1e9716`  
		Last Modified: Tue, 17 Mar 2026 03:04:46 GMT  
		Size: 16.6 MB (16616480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650fd49431f615b65d763e6d655cb89de582910b3c632d99f35a9e87f0f472ec`  
		Last Modified: Tue, 17 Mar 2026 03:04:46 GMT  
		Size: 4.5 MB (4517710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a370d94c013aeb9a1fce8105ba53aec38221eecc799d120fbcf076a08ce72a`  
		Last Modified: Tue, 17 Mar 2026 03:04:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:add8885d415b2d53cbf25c3213b18a116259a1fd2b25dc95ed51a5c6acf76e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4505177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16fd0265351aa674f40226de500c01021c67ac16ce8a01bffccfae27ef4e9cb7`

```dockerfile
```

-	Layers:
	-	`sha256:48ecc2c746e5c0d0d86cbec9f7e850ecf8fc7263ce03125013c5c015de3dddae`  
		Last Modified: Tue, 17 Mar 2026 03:04:46 GMT  
		Size: 4.5 MB (4486688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dce523a8ecb54c17c90d51dfde622d6eab978a261075283f116a4fba8b568e56`  
		Last Modified: Tue, 17 Mar 2026 03:04:46 GMT  
		Size: 18.5 KB (18489 bytes)  
		MIME: application/vnd.in-toto+json
