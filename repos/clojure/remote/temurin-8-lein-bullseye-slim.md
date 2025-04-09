## `clojure:temurin-8-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:4c239423f752a8db88379f5323c05c587b17e2190175a8e2c7ea43c602401f59
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:71e797fbe57e3ba10f8151ff2e233b1b7f40da9dde55da83131843398ed79b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132771552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d0a6d6478e540785b94a3962bac3b840e04055ac64f8f51d690f3aed6eb8bd8`
-	Default Command: `["lein","repl"]`

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
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_ROOT=1
# Wed, 26 Mar 2025 16:17:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b64c58628a1ded9c8c5ebf32c5b521217d15aab9fc181962d5f76613d68485`  
		Last Modified: Wed, 09 Apr 2025 02:18:09 GMT  
		Size: 54.7 MB (54721225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b20daccff68298d3e8c3d548ea6bf085d9a50ecebe8b4c77adb7fee8999102`  
		Last Modified: Wed, 09 Apr 2025 02:18:08 GMT  
		Size: 43.3 MB (43278737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082a242a3845391d80b1a8ec681080192e29579c649f43ce4421659c3403ef65`  
		Last Modified: Wed, 09 Apr 2025 02:18:07 GMT  
		Size: 4.5 MB (4514139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3c1defcf31c22291a971e4e58c559653caf6729321dbf5bafe05d0177b9f6f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4708178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a78f4dbfbbcf6b0915da1ab90179c99869049bcd4622480f01ca8c81e6030952`

```dockerfile
```

-	Layers:
	-	`sha256:9ed22ef22e2f3c0c6397784196cd0042c51693848dffadc47514eacf00a40647`  
		Last Modified: Wed, 09 Apr 2025 02:18:07 GMT  
		Size: 4.7 MB (4691727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b493b2722be3e2f31e1222a9ccb54e0a5904c5f5dfb1c44ad9bb0f7dfa22ab3e`  
		Last Modified: Wed, 09 Apr 2025 02:18:07 GMT  
		Size: 16.5 KB (16451 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c34d252b890f62e50af328325dd97afed552a3fbba5c191752a1865e387199f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.4 MB (130400708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41cc9e45531dff5d206acab28b23741b39c6d82bae664ec24f56c377f15e03f8`
-	Default Command: `["lein","repl"]`

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
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_ROOT=1
# Wed, 26 Mar 2025 16:17:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0861fe7ff88c49bb4627c613a692e3a36a03b94a53527929464db92b49b9e55`  
		Last Modified: Wed, 09 Apr 2025 17:14:06 GMT  
		Size: 53.8 MB (53822769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca96fe791cd310d99782db69730e6d1fabbab75dcac617d8f5fc3c31393c889`  
		Last Modified: Wed, 09 Apr 2025 17:14:06 GMT  
		Size: 43.3 MB (43314257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ed5aa5eb810be55721f8b83e8f7e2edf808340e1647d17b5a68f50d4136455`  
		Last Modified: Wed, 09 Apr 2025 17:14:05 GMT  
		Size: 4.5 MB (4514152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dc823db4d5be91f0949a67637b4740785c4cbab8903ba2761a7fcb875d0923a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4714661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f3231469bd1abcb3560ec4151680e94da038b69d81c44101e0dc3e5583829db`

```dockerfile
```

-	Layers:
	-	`sha256:657fb8b27cf8b7f93d1050843c3968293a072eecd1de4600d79b71d79081ba89`  
		Last Modified: Wed, 09 Apr 2025 17:14:05 GMT  
		Size: 4.7 MB (4698089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df71ea7044646bde3a9c6390b2fef2fff3843632cc2120e24854ad45553de399`  
		Last Modified: Wed, 09 Apr 2025 17:14:04 GMT  
		Size: 16.6 KB (16572 bytes)  
		MIME: application/vnd.in-toto+json
