## `clojure:temurin-17-lein-bullseye`

```console
$ docker pull clojure@sha256:6a119f889c1e41e9b726045cab9ea7431500d485ceae501cd02b160772366a58
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:c4c6b9612f0575e6ddddfd0411cc53c3ce0126450ddbe6c615fd81e8cbb46ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255688810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d698ad64e71f0d42667fea41360086036ff7c286ea2d6a1b67d63b7660a02d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_VERSION=2.11.2
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_ROOT=1
# Mon, 28 Apr 2025 17:24:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db61d149868a0c5de645ba08cb77f29a5f7a4e438e9c44dd8b90400f9bce5d2`  
		Last Modified: Mon, 28 Apr 2025 22:07:16 GMT  
		Size: 144.6 MB (144634964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ca46dff8cefd0e3f37be2a7bd9e20c2c3de722d91f7d5cf09e6e8a66adc329`  
		Last Modified: Mon, 28 Apr 2025 22:07:13 GMT  
		Size: 52.8 MB (52791519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b60f95f753d08ebd2d7b77ea55349572bbd259556c05671421cbe0d3598e46`  
		Last Modified: Mon, 28 Apr 2025 22:07:09 GMT  
		Size: 4.5 MB (4514159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885aecbfcbbdc4c0c54510ed9f2b2e5c1c29668d3e091a3e12b2c4c28d88ff21`  
		Last Modified: Mon, 28 Apr 2025 22:07:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2e6f1bcbc1b9c8e22dc340a8d0f1559b561837b3989ec70ca0a77436152e58ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6640178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf63ad43867a7748e168297ecf54f8de5d461f8e6fe36ac7e80ab66c730857f2`

```dockerfile
```

-	Layers:
	-	`sha256:f71cdc0c57ddeb48012480b5a72b0f50a857aadd96fcc3e2221ae0f9d9041801`  
		Last Modified: Mon, 28 Apr 2025 22:07:12 GMT  
		Size: 6.6 MB (6621756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38430c9db36d386dbd6d63a1d02152c24b9b4a3acf5c3abf75a5411c93840a78`  
		Last Modified: Mon, 28 Apr 2025 22:07:11 GMT  
		Size: 18.4 KB (18422 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:27b96fb8e24b4040ae910c05805aaf4d89aa6e4d179f4797ae901066590f54a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.1 MB (253104867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1bee01be567174c2acc8f64cb6726aebbf5c6f3f7f0822136e083677780047`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_VERSION=2.11.2
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_ROOT=1
# Mon, 28 Apr 2025 17:24:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Mon, 28 Apr 2025 21:20:53 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c441d9b4a0e858b97a1d7c29b1a927fdf6f835e7f9d6713307867ec981319cb`  
		Last Modified: Wed, 30 Apr 2025 01:35:05 GMT  
		Size: 143.5 MB (143512607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4ac5abaefef64b21be3b047cd9a9e6c6bda76a4f821ccbc72d98c9fd94600d`  
		Last Modified: Wed, 30 Apr 2025 04:46:07 GMT  
		Size: 52.8 MB (52831635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7b02cd99b0fd36a31d2dd11c133516b6ec38e00075fd178345b783e45f4206`  
		Last Modified: Wed, 30 Apr 2025 04:46:06 GMT  
		Size: 4.5 MB (4514217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cada64f26e86fa06725fb09900ffc553fe8da87ebf7109588046148598c5c64c`  
		Last Modified: Wed, 30 Apr 2025 04:46:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1902734449d6be59c3352d98383ee3234187792198fa311d3397bb209cce06a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6645330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:347ec4c60f3f271ae284d0f2119f4769895adbcdf1b29eaa4f5d4ea4e6ae0210`

```dockerfile
```

-	Layers:
	-	`sha256:db220c3ff5426a460030acf654882e3bb5c79054767377ade58675423f09e904`  
		Last Modified: Wed, 30 Apr 2025 04:46:06 GMT  
		Size: 6.6 MB (6626787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da6dfbb0c75dc14b1096d67aff07633c75c5244f4812e4ad41bd157ae2fbfcf7`  
		Last Modified: Wed, 30 Apr 2025 04:46:05 GMT  
		Size: 18.5 KB (18543 bytes)  
		MIME: application/vnd.in-toto+json
