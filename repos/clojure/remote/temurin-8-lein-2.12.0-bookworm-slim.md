## `clojure:temurin-8-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:695654c8077182cd2b7ca0ff5f31021f0265770904bba239a723c8c21aed6070
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:cfe3d21fa63e2069ba971bfa057cdcbb4dd5e7d2020137a26377b9bca16d3fce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 MB (105683684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6a99d121418119126dd1883bd9c9dc08f21f0a86c55350ead34064050f8485`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:15:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:15:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:15:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:15:14 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:15:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:15:15 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:15:28 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:15:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:15:28 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:15:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:15:29 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1eff77e6a51c17b6e3a08fcd3a36c13d776376f3c2df207e788ca742c27b41`  
		Last Modified: Wed, 22 Apr 2026 02:15:42 GMT  
		Size: 55.2 MB (55170060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58ed7b1c6573d5d5c2535b577b489a9f86eeed453334c7609626f4c95fbf2f2`  
		Last Modified: Wed, 22 Apr 2026 02:15:41 GMT  
		Size: 17.8 MB (17759599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6484a75b4c2b32e6dc9e89a405af02b05a5cef046978c80f5c0f17b12c3359cd`  
		Last Modified: Wed, 22 Apr 2026 02:15:40 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:168a5ca686564a1a0d4c9406d9a9a07c97c33ba7cc43f331d35eaa8eb48db3f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2867438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68abec6f94da46d6de6f3d4e0afb09f9fa598f84c3c800d4e8ea7ee630db958a`

```dockerfile
```

-	Layers:
	-	`sha256:b7247480e0c8daa35ac0e2c9dbc91c6c237a8c1a9ca5db61902e9f866d4e1e68`  
		Last Modified: Wed, 22 Apr 2026 02:15:40 GMT  
		Size: 2.9 MB (2851039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:211a3f4711266b82e58e8d835e167c91eacd30e26756fff4e9ea4bd42ad55f11`  
		Last Modified: Wed, 22 Apr 2026 02:15:40 GMT  
		Size: 16.4 KB (16399 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bb69a107cbb47c4265434b84b8db9931459b93c0254108e4323ecbb67e9b7b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104478497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d40da91b1564587b69bf6821bdc2bc48a5fb89c6e44c733d46ba7d2f51fadab1`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:18:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:18:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:18:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:18:38 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:18:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:18:39 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:18:52 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:18:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:18:52 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:18:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:18:54 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c0e9cb5eaaf9b1c1f8161f162fa080aa1ba1ca703cc45e61311c0c4bd2e500`  
		Last Modified: Wed, 22 Apr 2026 02:19:08 GMT  
		Size: 54.3 MB (54251616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780ec3c54fce69c5a0efffe6719341bce2a1e7b728ddce4b2e6545046ee40b98`  
		Last Modified: Wed, 22 Apr 2026 02:19:07 GMT  
		Size: 17.6 MB (17593014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67790deb152eac6be418e92e592a03b5d1b255d2b1d60548d528943e13efebf9`  
		Last Modified: Wed, 22 Apr 2026 02:19:06 GMT  
		Size: 4.5 MB (4517721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ae9ae1284a43a738f6212ff49228e08712d9f85f5d01cb309fd7db851a51cefd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2867874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85b55ba332b5d613ad9abadc70bedf07cc17d88ac7edb48a60cc81a8f37f466b`

```dockerfile
```

-	Layers:
	-	`sha256:c3278ae88569407632b4eaeb8236943f998545a999d49f5a856dd42550bffa0f`  
		Last Modified: Wed, 22 Apr 2026 02:19:06 GMT  
		Size: 2.9 MB (2851354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74f0eadcbc41c3da11a5e627c60b096c2674720676ff2c08093fcc9bc04ea589`  
		Last Modified: Wed, 22 Apr 2026 02:19:06 GMT  
		Size: 16.5 KB (16520 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:0b3523d923be20336a055bb58d731c7ba953d2be6fa1d3004443a9684b4747de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107208072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ec59f7186804a374c2f6faedc462f8212b5b91f01e10130ffc751bf61a1cb8`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 02:31:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:31:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:31:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:31:40 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 02:31:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 02:31:40 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 02:32:17 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 02:32:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 02:32:17 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 02:32:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 02:32:21 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b1c56220ca211bc9d02f1ed5c589465809676b6ab2cef705f1e2fb8e9726de76`  
		Last Modified: Tue, 07 Apr 2026 00:09:42 GMT  
		Size: 32.1 MB (32078464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca09ab2f7ae5f0a2c569e6862baef7188079f93d19533ec83941e939b63131e`  
		Last Modified: Thu, 16 Apr 2026 02:32:47 GMT  
		Size: 52.7 MB (52650382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:976cd1cd282054d201387788849dc9adb5806bfd8a9bc8bfe1da7a67ec79a2fc`  
		Last Modified: Thu, 16 Apr 2026 02:32:46 GMT  
		Size: 18.0 MB (17961436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5032c50cb8d5b5eb61b61ae9d443186bfb7b2db0d142322ec9a48157fbff8c94`  
		Last Modified: Thu, 16 Apr 2026 02:32:45 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:aba9bcca6bdfde824e01178809596760117cdbf431d8c0835b29728dbacafac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2869910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2777fc0ae2ddfb74e480b3803c9d80b2b2756579c61e97f3e3c18bb801fbcb0`

```dockerfile
```

-	Layers:
	-	`sha256:3df5967a51f80246c0a46f14a7e95470702a4d86b68f3bb16fbc99a9cb4850dc`  
		Last Modified: Thu, 16 Apr 2026 02:32:45 GMT  
		Size: 2.9 MB (2853467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22119def43e88613bf1af1ec58dedd5bd467a25c7add3f9857a5fc725dbe57f0`  
		Last Modified: Thu, 16 Apr 2026 02:32:44 GMT  
		Size: 16.4 KB (16443 bytes)  
		MIME: application/vnd.in-toto+json
