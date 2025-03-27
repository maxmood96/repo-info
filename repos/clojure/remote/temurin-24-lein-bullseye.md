## `clojure:temurin-24-lein-bullseye`

```console
$ docker pull clojure@sha256:980ac18ec4696d325dbb67d29482e1c3b4dcc59e58de0fbbf19ebafc499c566c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1df73750177cf5cb30196b375502c90f1db79dbcbeb4d13d1fd7303775da8243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.8 MB (200791688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7caf9f8fee89987b1b6289a8fb84330cf4a3ca725bbe73a62c1f6e63ffa4ccda`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_ROOT=1
# Wed, 26 Mar 2025 16:17:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8d1bfb80edb9306e3de72f4095daeae4c281712482255562f2e236ae85233e7d`  
		Last Modified: Mon, 17 Mar 2025 22:17:19 GMT  
		Size: 53.7 MB (53741275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49caf4e2bfd91869805b20444447863dc5abc3bc95d7cedb9b9c05bb54e3e6e4`  
		Last Modified: Thu, 27 Mar 2025 17:53:48 GMT  
		Size: 89.9 MB (89949053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d293c5a0a16281a47cbbdb1f9cdf0b22168dd4029f983e26f862aa5dbd7b155`  
		Last Modified: Thu, 27 Mar 2025 17:53:47 GMT  
		Size: 52.6 MB (52586771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073c9d97db9539e20ff36636af5f01f9b2db03f940c196ac00358d30bd225ed1`  
		Last Modified: Thu, 27 Mar 2025 17:53:46 GMT  
		Size: 4.5 MB (4514159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92802d52bc33a70211b967d81b2eae5831c486a880b548de1f8e0a92ee050498`  
		Last Modified: Thu, 27 Mar 2025 17:53:45 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:23e8cdea3406d7c2c5e0225bb0a5e220db5aa69495018692b62758bb593d8900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6588804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc9ed40aaee55fa32145ffa549caa083c2563d1bc901afdce3b9a64b1fd3463`

```dockerfile
```

-	Layers:
	-	`sha256:e0aeae876d3a76e92a2ae570d99fefe3165bcbd1381c48e3a01e44e14ea4ce5e`  
		Last Modified: Thu, 27 Mar 2025 17:53:46 GMT  
		Size: 6.6 MB (6570388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44802c247dc732915d70b470b103bf722dac3d0ba89f549a4e4e2097e9fc0495`  
		Last Modified: Thu, 27 Mar 2025 17:53:45 GMT  
		Size: 18.4 KB (18416 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6683ae3963af3da001b0c30e38eb8ffac25f1fffdc8c1a0c078e75bdb964d599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.5 MB (198481099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb127ba6fae46b3a22d301fef97062dba7ff0435c75e856054c754edb4edd2e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_ROOT=1
# Wed, 26 Mar 2025 16:17:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7d61d9dafd0c900d9eaa97f9411b10213d45699b9afb91aee676649c07fc4a51`  
		Last Modified: Mon, 17 Mar 2025 22:18:23 GMT  
		Size: 52.2 MB (52248394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7cff61800d77fea8ceca86197d0088a545723471fc54b8d8f0c4585f35410dd`  
		Last Modified: Thu, 27 Mar 2025 17:55:17 GMT  
		Size: 89.1 MB (89092706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83840d9b951af15ec0e16f70689708b23384aa95e81207ffeb144009a819b55f`  
		Last Modified: Thu, 27 Mar 2025 17:55:16 GMT  
		Size: 52.6 MB (52625394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811a8186339bf1d7a717613d3bd240b8e3867498fd3332f4c13594492911f7bb`  
		Last Modified: Thu, 27 Mar 2025 17:55:15 GMT  
		Size: 4.5 MB (4514176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd502627192a2a39937774518caa1e27366c0bc82f6c1e9e8227645920dae7ce`  
		Last Modified: Thu, 27 Mar 2025 17:55:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3e465594bb285fa1e701f200b1b5a05323020f00990209e0874f5d21cfb3ad56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6593953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e81a9ccbeb2506a5b9d1a31f94b20f7f9cf9ea813aba80397b6d8dbe184ba71`

```dockerfile
```

-	Layers:
	-	`sha256:8066b3f1419dff16691e8f2f3383201b8150e3aecf2eca72567bbf45786eac1c`  
		Last Modified: Thu, 27 Mar 2025 17:55:15 GMT  
		Size: 6.6 MB (6575416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ff43aa1acf8b1a30b26178d3e5797849e8159691ca7600e8274314403b09599`  
		Last Modified: Thu, 27 Mar 2025 17:55:14 GMT  
		Size: 18.5 KB (18537 bytes)  
		MIME: application/vnd.in-toto+json
