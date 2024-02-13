## `clojure:temurin-21-lein-2.11.1-bullseye-slim`

```console
$ docker pull clojure@sha256:7a0e36cc75a5bacf56a54ba9374795ece2ee20267d9392410c1902aec881d231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-21-lein-2.11.1-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6ef4347d14778fc78321e8844bd4a552e16739056cf6096c5cb1e82ca6766405
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.5 MB (210466725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932357f7489181bbc196e82d4d1e1380ce32601319f4a02e7703e6a9a71dbd6d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:48:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 02:05:07 GMT
COPY dir:64a8841762a9afbd2fb8b4cf497b2dee87765737d44ff0387ce1cfc51371c9a2 in /opt/java/openjdk 
# Tue, 13 Feb 2024 02:05:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 02:05:09 GMT
ENV LEIN_VERSION=2.11.1
# Tue, 13 Feb 2024 02:05:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Feb 2024 02:05:09 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 02:05:24 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "03b3fbf7e6fac262f88f843a87b712a2b37f39cffc4f4f384436a30d8b01d6e4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 13 Feb 2024 02:05:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Feb 2024 02:05:24 GMT
ENV LEIN_ROOT=1
# Tue, 13 Feb 2024 02:05:27 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Tue, 13 Feb 2024 02:05:27 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Tue, 13 Feb 2024 02:05:27 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Feb 2024 02:05:27 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9603b74f1aa7577b6b561eb7c59ceb9e578802067629395b2ea6eb7acf0942`  
		Last Modified: Tue, 13 Feb 2024 02:21:21 GMT  
		Size: 159.6 MB (159582956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77b4adf5809948ce7825eb4a8e2f6f7771f33773c4dd66484e2dd6f3349ff90`  
		Last Modified: Tue, 13 Feb 2024 02:21:09 GMT  
		Size: 15.1 MB (15061780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02310197b109f0adeaab67f30f75a0e91a2a29689ded92f269b018e29594eff2`  
		Last Modified: Tue, 13 Feb 2024 02:21:09 GMT  
		Size: 4.4 MB (4399166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93429ba0153cb5ab347467d40254691710e57ad25a856e9a8815e4e2ab031ff6`  
		Last Modified: Tue, 13 Feb 2024 02:21:08 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-21-lein-2.11.1-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a7c5f940fb4be1846cd5551eed20f75ee87d16543415418eadb089ae7f4b154b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.3 MB (207304764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed4838d9da3bda727ee47b258875c21c2d1bc590c896ce35ba147dd615c04e81`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:56:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 02:10:08 GMT
COPY dir:ab40534e435f9942975c0e8b5454d6b7a8d69c445f8e0758c1bd9c500e157fca in /opt/java/openjdk 
# Tue, 13 Feb 2024 02:10:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 02:10:12 GMT
ENV LEIN_VERSION=2.11.1
# Tue, 13 Feb 2024 02:10:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Feb 2024 02:10:12 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 02:10:25 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "03b3fbf7e6fac262f88f843a87b712a2b37f39cffc4f4f384436a30d8b01d6e4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 13 Feb 2024 02:10:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Feb 2024 02:10:25 GMT
ENV LEIN_ROOT=1
# Tue, 13 Feb 2024 02:10:27 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Tue, 13 Feb 2024 02:10:27 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Tue, 13 Feb 2024 02:10:27 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Feb 2024 02:10:28 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedb0672bb53fbc4271f32edf7d667943222010451c4ce1826996cc183a4ad4e`  
		Last Modified: Tue, 13 Feb 2024 02:25:10 GMT  
		Size: 157.8 MB (157784647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08343ebf4666a6ae290ced0ec6156fcf9df2344b3e1028cc1cae2a91eef2dbc8`  
		Last Modified: Tue, 13 Feb 2024 02:25:00 GMT  
		Size: 15.0 MB (15049469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb059871f5081fbf1c97988752c817a8e8a62eb64530c28dde7ca2e5f6dd429`  
		Last Modified: Tue, 13 Feb 2024 02:24:59 GMT  
		Size: 4.4 MB (4399171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d3b1215c621bf7cd127fe14bcfc34d211779bace83cd82d4d9a6634948dd1d`  
		Last Modified: Tue, 13 Feb 2024 02:24:59 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
