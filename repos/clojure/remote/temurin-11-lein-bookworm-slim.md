## `clojure:temurin-11-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:8f3f338a27c21cc502ec1f40ea550b59354049afca15235cb323d4518c01743d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d9e50b0e75e7974a1e4ce156aad36ff18db6767f107fbbe7f6d1bc8e1cd1d703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196346326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8822facce9d214113789eda7fa363a0938fe5f165a58bbede1adc66504750ec0`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_ROOT=1
# Tue, 28 May 2024 15:17:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ea103f594324940ac5057160cacfc731bde3680386133cbe568d91dfbf9c2b`  
		Last Modified: Wed, 29 May 2024 19:57:05 GMT  
		Size: 145.5 MB (145504828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bac9ca72ab12fc5e7a28753763679e6002c4028ff5864afc01658610eae4b0`  
		Last Modified: Wed, 29 May 2024 19:57:01 GMT  
		Size: 17.3 MB (17292976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2744503f24e1e7686bfb310b1f3bfff3f83b024fbddf3c6ba8735a961bc779`  
		Last Modified: Wed, 29 May 2024 19:57:01 GMT  
		Size: 4.4 MB (4398079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6e8b99e245bb3afb6a46c38ce03b39d25b23451b8a1b36f66ddc7d149f50e61a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2414446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0d5acfd98fe4a02a75657903fb0db141512f2b70cac6dc5b52fbefd9c02dfe`

```dockerfile
```

-	Layers:
	-	`sha256:4ab6bf46d02d6516395267ae5ba205a729e5055b9f3472e8127cf6f186f4d130`  
		Last Modified: Wed, 29 May 2024 19:57:01 GMT  
		Size: 2.4 MB (2398414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e74416ab58c77663d79cb309f82c69f11e53e15f3a63b4e39dfcc137d3f03b7`  
		Last Modified: Wed, 29 May 2024 19:57:00 GMT  
		Size: 16.0 KB (16032 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0395073329ac18c2b68bde1566918d64a3a905517bc25519db29dfa659eba7d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (192997938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd02b9e0d334f2bc8fe178d408dc32ace739df17e094015b052d3a16616a400a`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_ROOT=1
# Tue, 28 May 2024 15:17:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5868317bcd6d62ca7d7340a6f775b564ac57ead186dab5864fe6ec9755e29f7d`  
		Last Modified: Wed, 29 May 2024 20:36:38 GMT  
		Size: 142.3 MB (142304178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f722748184df7be92623f94c4ca3b87fcbdd71b9fa5342d1ef9e40ce02bce1`  
		Last Modified: Wed, 29 May 2024 20:36:35 GMT  
		Size: 17.1 MB (17116189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8a46d115357b7b0ff0d7cad51eaafbbe85be73022e2f8f76dac8252bcfa53e`  
		Last Modified: Wed, 29 May 2024 20:36:35 GMT  
		Size: 4.4 MB (4398036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b11eb8c6ffa0360e2bf7e42d97c919fcaad7c7f4b490cc71b8afa1ae1c0b81dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6810177cd6f98ce3ae9425124847de833475cdf43b7505dbb5afcc641ae9797a`

```dockerfile
```

-	Layers:
	-	`sha256:cc67886050036a7e1746890149ab45d3fa80326a2562c79077526018c8b00601`  
		Last Modified: Wed, 29 May 2024 20:36:35 GMT  
		Size: 2.4 MB (2398646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67e0bce14a2523a42541ca8bd4dffadf79a838cac56d8b2b310bba665666ba89`  
		Last Modified: Wed, 29 May 2024 20:36:34 GMT  
		Size: 16.6 KB (16561 bytes)  
		MIME: application/vnd.in-toto+json
