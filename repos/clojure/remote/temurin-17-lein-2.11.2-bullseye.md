## `clojure:temurin-17-lein-2.11.2-bullseye`

```console
$ docker pull clojure@sha256:42d293fbff0f435e02cb2d7e84d93451c294347ddcaa44d9fa39786afa72c6a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-2.11.2-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:57d33af35ed41ccd9fcc16000039037b583e35109993f17ce57c46b3e7a1cd0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.6 MB (255621261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28132b5752db7860cbdc54fbf73f70137a82e6ed903ecea45783e0e0d652b2b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
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
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721a26d53e8e6c4d6f87be96b36d0bd406241b59dcbba4d382c34ba3b3f56c8a`  
		Last Modified: Wed, 09 Apr 2025 02:19:39 GMT  
		Size: 144.6 MB (144566536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2263b35ff4519b469d50e371d7e1a90fdc1241d71290b2bb7e4f0a436ce70a3`  
		Last Modified: Wed, 09 Apr 2025 02:19:38 GMT  
		Size: 52.8 MB (52791585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035851edfca461be881ffb9ca0ad88ddc93bbe1670eba5a0b29881385e9bb1cc`  
		Last Modified: Wed, 09 Apr 2025 02:19:37 GMT  
		Size: 4.5 MB (4514182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2de6c0d12b34306ccd4cdc3d59111b730ded8041994b2495a42a187e71a3d0`  
		Last Modified: Wed, 09 Apr 2025 02:19:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.11.2-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:644c179dedbe2edfbdf753c20418203c324be957689797969b17f99cbe187345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6640125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69cb3ce4168dcd4458e47821f207799c4efae71a61d65c0b29573144b103e48`

```dockerfile
```

-	Layers:
	-	`sha256:e8d0e92a498719cd4492ef8e0ef379abbc59edbb6ca6d7fd9d211c824ec571a8`  
		Last Modified: Wed, 09 Apr 2025 02:19:37 GMT  
		Size: 6.6 MB (6621702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:836934534f4452616625c8ade9d2edaec65111228264894f9bc035516e05238d`  
		Last Modified: Wed, 09 Apr 2025 02:19:37 GMT  
		Size: 18.4 KB (18423 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.11.2-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c4721f92767cb9cffb6afec96a02913b1270caf97c40ae6d88686b1ae52e6fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.1 MB (253054378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79bdd8323be5d876177bed4e2c974ea414ece8969ec3625962386636cdcdd887`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
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
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c583047e73666cdc94eb0df609aa7d53eb0babfc52611f6c4d087a9ffda6db84`  
		Last Modified: Wed, 09 Apr 2025 17:31:24 GMT  
		Size: 143.5 MB (143454679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1461694be650e28757303234553c9ddd65546a72ce29e1101922721921d04d78`  
		Last Modified: Wed, 09 Apr 2025 17:31:21 GMT  
		Size: 52.8 MB (52830888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6cc8730b52699a15fabc0a8997ec29ead4e1f8dc1d25d7e32214fdc16b29bc`  
		Last Modified: Wed, 09 Apr 2025 17:31:19 GMT  
		Size: 4.5 MB (4514158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f1f89befadb7863f72ef9c6eeba010cd8119e0652c7006e7e3e06cc2174d58`  
		Last Modified: Wed, 09 Apr 2025 17:31:19 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.11.2-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:50a423f4b9a1b423850a7d1be4eb75d30703ac6a7145036ea94b34be26d7024e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6645276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8812d579bc48fe44975461da7e0d3b972ce680dbf6f86c89dfaae2642b44482d`

```dockerfile
```

-	Layers:
	-	`sha256:6d26f8027adc2663aa87f8722c784c785cf6da942cf92c3d45ef9e0d203df6a3`  
		Last Modified: Wed, 09 Apr 2025 17:31:19 GMT  
		Size: 6.6 MB (6626733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78c5fa216bc1735f8cb41078c0694f8e5dfc0fc3caa4734626945d13c46c7f06`  
		Last Modified: Wed, 09 Apr 2025 17:31:19 GMT  
		Size: 18.5 KB (18543 bytes)  
		MIME: application/vnd.in-toto+json
