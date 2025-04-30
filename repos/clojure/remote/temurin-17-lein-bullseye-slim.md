## `clojure:temurin-17-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:3672e922ce9dc30c470fa56862c48d0b903e6bfb0cb0312f435fcda2775ab0d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6b6667271d66a1503924acda66105536e2049456f03a1c1f75910af59148547c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.7 MB (222682446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23f613eef353fc48220ddeafc41e6670cc4bf9d5e5d1e2f72ddbb1389bdb173`
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
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
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
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0efa4e4a0857e4b7f8534562bfee33c489ba085e46d2e1d613cf6f6710f09f`  
		Last Modified: Mon, 28 Apr 2025 22:07:11 GMT  
		Size: 144.6 MB (144634964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ef6d08edb626b858abde422f78066432e462385a4ee311efce7e2fabfd7636`  
		Last Modified: Mon, 28 Apr 2025 22:07:10 GMT  
		Size: 43.3 MB (43278291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b60f95f753d08ebd2d7b77ea55349572bbd259556c05671421cbe0d3598e46`  
		Last Modified: Mon, 28 Apr 2025 22:07:09 GMT  
		Size: 4.5 MB (4514159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6219ef61bada68fccfd08c9082a4ba744dac2b245dbb03c77a9ca80322002de`  
		Last Modified: Mon, 28 Apr 2025 22:07:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:aef1e5638a891619b8de35c2ccd32415edb861e933045723cba24069ee96c2a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4588627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe99bc5135de6f2c190c0b7e9ea53d78f2bf0aac991a97bcedad7cf7b859b5e`

```dockerfile
```

-	Layers:
	-	`sha256:f120324e781b542a9492df9682681c0387b899663a57af25b595c022857be100`  
		Last Modified: Mon, 28 Apr 2025 22:07:09 GMT  
		Size: 4.6 MB (4570169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ecbf9b01fda44ab18512ed876828733f58e6cf381d9842e2fa2c2e1c060ffb6`  
		Last Modified: Mon, 28 Apr 2025 22:07:09 GMT  
		Size: 18.5 KB (18458 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ff259a234ef304c06077e426ed362a09291386d28e0ed7cb2626d2cf8b630ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.1 MB (220086001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5032dca13257afb19fe4dd52006e014c24ebdae45d6b6978033f17cb3f83fab6`
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
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
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
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72262fe32b026e7f23e9a38bfb2a66973be30355ac7b2a0fe73a91bfb575d0f`  
		Last Modified: Tue, 29 Apr 2025 20:15:14 GMT  
		Size: 143.5 MB (143512633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fc4ee01fa84136eae9f32b90fa3364a8ab02e89ede1037689815626fc7730b`  
		Last Modified: Wed, 30 Apr 2025 04:46:48 GMT  
		Size: 43.3 MB (43314136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf15c67f86d0d513fc6148ddc580aa5e8097e5bec6429b2387af98c0c3eb991`  
		Last Modified: Wed, 30 Apr 2025 04:46:47 GMT  
		Size: 4.5 MB (4514159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259735291119d3848b0e765bb72d6a0bfeb9076148fbffad635a0a68c2d29026`  
		Last Modified: Wed, 30 Apr 2025 04:46:47 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:38cfe38eeb348d5e533a548ee06e6b252af324a07fe8c02ab9014eae792b20ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4594412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab22137240488c2d1195a6eb5402df84a10da8aab613fd3ef26a6e88c6236d5`

```dockerfile
```

-	Layers:
	-	`sha256:6954c4ca14ebcaf189879feb42e3fdc6f6a45e7a8541a17b234bf71806aab5b1`  
		Last Modified: Wed, 30 Apr 2025 04:46:47 GMT  
		Size: 4.6 MB (4575833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0675cba27f14be6df301a2085a382491acb258e33ff3ea26d8b675459e168c2c`  
		Last Modified: Wed, 30 Apr 2025 04:46:47 GMT  
		Size: 18.6 KB (18579 bytes)  
		MIME: application/vnd.in-toto+json
