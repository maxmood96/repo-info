## `clojure:temurin-8-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:832bace519ce54167f5ac48852b396b9482789d248d2c06f851bc071bd8cc95b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-2.12.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:6aaabf0a634aeaf74b24e8617ac5ae1884cdc36a91fd161eff7f7c64bf8c0ab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127561034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3830a69903c8093de6ca5b73f9012f08c2b629c87020669faf8bbfb751a5dfb`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:52:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:52:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:52:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:52:23 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 19:52:23 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 19:52:23 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:52:41 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 19:52:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 19:52:41 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 19:52:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 19:52:42 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b748e78e7b88335045a7938572d023d71fe0f01480d555a0534a19c0f0ba5b`  
		Last Modified: Tue, 24 Feb 2026 19:52:53 GMT  
		Size: 55.2 MB (55170068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9018757790c99c9d105bb52ce2849aae5ad975d9a5c4453529bf97153b2569e`  
		Last Modified: Tue, 24 Feb 2026 19:52:56 GMT  
		Size: 18.6 MB (18580092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39c8010e8108c26f01d0108fe21da4ffdb3d61c885729e00cf189f5eb2fe451`  
		Last Modified: Tue, 24 Feb 2026 19:52:55 GMT  
		Size: 4.5 MB (4517718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a738ac91c94c1b20627c1c815cccc59b4707663e6b2bdf3e94aa2c19ca52654d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6473acf467cc691904e9d11b785c7d6117ad69f95cbd435d7af879a76df98fae`

```dockerfile
```

-	Layers:
	-	`sha256:291cabc12e4163564ef7137d39af3649d63abd206c8caf773c4d67005ed5ab7c`  
		Last Modified: Tue, 24 Feb 2026 19:52:55 GMT  
		Size: 3.9 MB (3936480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f8439520be088bca72155c64c0fc3a8e58caac3a52f5e2391423c5ad738f303`  
		Last Modified: Tue, 24 Feb 2026 19:52:55 GMT  
		Size: 16.4 KB (16351 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4aa3db19f98532070aa84b7ba6de738b418471a621157cb97c72fe2c1305659c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (126962986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5d9af37fb30d5c21268606bf47296babc4fceb4ab25ecc23ff4754598609114`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:03:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:03:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:03:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:03:06 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 20:03:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 20:03:06 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:03:23 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 20:03:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 20:03:23 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 20:03:24 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 20:03:24 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e05858b6b1aec7ed77d8f21639463813a17bf44d0d527ea78f4145515644f22`  
		Last Modified: Tue, 24 Feb 2026 20:03:53 GMT  
		Size: 54.3 MB (54251612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cf31175ef07b1ac4bc1c5108faac0b829880be902adfd7cc359d8774294b7f`  
		Last Modified: Tue, 24 Feb 2026 20:03:50 GMT  
		Size: 18.5 MB (18541460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49a47e5507db333d2ace2da1e579cb84b713bb19aa0e59c1c56c1edf4d26a46`  
		Last Modified: Tue, 24 Feb 2026 20:03:46 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:af6611298ae1f3c20ef3d60010f41c89c804a96b900d07dd24ed87881ace0218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b898417bc9d7b38f326b82cf896d1ee7d84a1269db5290dc7be64c4911e268`

```dockerfile
```

-	Layers:
	-	`sha256:5f2d7fcd92c516d1d0f5e8aa0f4b05d7408210456f212ff352a409fc42bdf5d3`  
		Last Modified: Tue, 24 Feb 2026 20:03:45 GMT  
		Size: 3.9 MB (3938057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e895b1356110fc53e754bb9a396f6c2e485f07c8508d8f0561dd923b880d7f8`  
		Last Modified: Tue, 24 Feb 2026 20:03:39 GMT  
		Size: 16.5 KB (16471 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:b828b5a4b62059c922dd7d66c1cdca1e4cae8810012c0f142c9d0c3ff4559b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.9 MB (128917959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a82d0c7d0b7bb58c12524dec2f291eb604f11a0cb68ad7562b4c847d41fb01`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 01:43:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 01:43:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 01:43:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:43:24 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 25 Feb 2026 01:43:24 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 25 Feb 2026 01:43:24 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 01:44:09 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 25 Feb 2026 01:44:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 25 Feb 2026 01:44:09 GMT
ENV LEIN_ROOT=1
# Wed, 25 Feb 2026 01:44:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 25 Feb 2026 01:44:16 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fdef948f7a075c7ba090915db8bdf444c4fd6f03737e0d659d8563f21b69755`  
		Last Modified: Wed, 25 Feb 2026 01:44:45 GMT  
		Size: 52.7 MB (52650395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27675fddd81bcc6928cb0f24d8c463677bb122c90ae6bb5390128588c3953283`  
		Last Modified: Wed, 25 Feb 2026 01:44:44 GMT  
		Size: 18.6 MB (18637516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3210e59924e879f181f590f4fb5d7324b881cb48837b9d54b7a95ef9a24d32fd`  
		Last Modified: Wed, 25 Feb 2026 01:44:44 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c485aa5b6f873a6c1264e1083de023e639a1aca942ffb619a94ed0db1d63f599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921e74b0d3eb703fbbe91b70159e7557d3b3939e9235598426d9862da60440ee`

```dockerfile
```

-	Layers:
	-	`sha256:ad6f42f56dd5d22f7dfc9525e2ede96a20e778a2abb67b9bf12dc012ecace298`  
		Last Modified: Wed, 25 Feb 2026 01:44:44 GMT  
		Size: 3.9 MB (3938075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fad4bda816a6f93edb0652a33fc51c5f60c7e87773d43f884cd86f1139da3936`  
		Last Modified: Wed, 25 Feb 2026 01:44:43 GMT  
		Size: 16.4 KB (16396 bytes)  
		MIME: application/vnd.in-toto+json
