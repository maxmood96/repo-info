## `clojure:temurin-8-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:63e219c0f9e0ceb77d4c9c18bf38a55c0c36201dce5d9c884bb234c406d1f2d8
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
$ docker pull clojure@sha256:75f009290becdce93141c6e9dde050f5238d3255a62e73ab2dd9d400fd2f7d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105235431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d3a111c9b582880df0503ddc98ea5cebf984569462d1a223cb91d5d4f3a506`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4fe251b2ffa2ea15b60129fb8017c22152c7b8328479410dfb4fd9ee7801c6e`  
		Last Modified: Sat, 13 Sep 2025 00:03:43 GMT  
		Size: 54.7 MB (54731282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca36b65337a5d35c37624324c81de7522e6a1b2abdf580e27d889a161bb42d2d`  
		Last Modified: Sat, 13 Sep 2025 00:03:33 GMT  
		Size: 17.8 MB (17758010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c327b9c1f85a8b3b4c2dd0f7eff05a0e4bd2a016158194c70e8b6171505d265e`  
		Last Modified: Sat, 13 Sep 2025 00:03:33 GMT  
		Size: 4.5 MB (4517761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:989cb692ce9dcc2d892ac931bd8a39a9c48058167398e85a21f09a55adb8dc72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61b5a0ccad3f2bec80fa4da607c6093837f07d68443f73ff2677bf81cd91573`

```dockerfile
```

-	Layers:
	-	`sha256:df43fd0d0a1dc59cfc73772dd9097d93d19f96fee8bcd0c1bda25121d84b8a4a`  
		Last Modified: Sat, 13 Sep 2025 00:44:15 GMT  
		Size: 2.9 MB (2850398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ea337c2f9d87444b786bd8d9af9884818570d49115681d3d664e1f81c49509b`  
		Last Modified: Sat, 13 Sep 2025 00:44:16 GMT  
		Size: 16.4 KB (16443 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8620aeaff059105a0cd821cde206ec767c31980c45bb9540f1b92351b4899923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.0 MB (104046383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0cedcd54bda5779dae188ffcbd5ef72cc2e45b20a256aa781756bf85841c71`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e153b5e5a5784a92a7f899cd307d224aff0f625475fd15a730b6185658971e`  
		Last Modified: Sat, 13 Sep 2025 00:14:01 GMT  
		Size: 53.8 MB (53835605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8ecae67a92e697c201d36600b5ae791124f2363a705b3733f41c18776e05ac`  
		Last Modified: Sat, 13 Sep 2025 00:13:59 GMT  
		Size: 17.6 MB (17590935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd438e5ec2a8df165dd14e9aa8ec643e6564775e31fe51b1cd1fdcd8b62db091`  
		Last Modified: Sat, 13 Sep 2025 00:13:57 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5bcc910513e7e9a0738ad877c170f05ebd36b5f7117859734baefac1b2b507eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2867275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dff17f4fc7e1d2e399474785c5b84f7507e4582e68b1e115ada81aac0f3891e`

```dockerfile
```

-	Layers:
	-	`sha256:3a6673b17186b9b0bcea146920bb5afc104dcd730bf40fee59bbdf0cc17dedfa`  
		Last Modified: Sat, 13 Sep 2025 03:41:58 GMT  
		Size: 2.9 MB (2850711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bbb5dbb300a436b4ce708a3600e970dbe93d26c82aceace3ef6238e5a0399fd`  
		Last Modified: Sat, 13 Sep 2025 03:41:59 GMT  
		Size: 16.6 KB (16564 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:fef8174c16b443477f3d41d8317cc5cc5c7db90f77d480665498cdc306ecb35b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106711588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b21d8e202320bdf11566a9e9a0bcdbaae67dc32cdebf013e7d0903d5784f6bc`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:a438293490bbc2af66661166949a4d86358eeb39f9fadd5b0146666f05b9b9ac`  
		Last Modified: Mon, 08 Sep 2025 21:30:47 GMT  
		Size: 32.1 MB (32068762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed13d84bff762045539b913e52a0729034d3e873c719091b50c82ea6d8b6d03b`  
		Last Modified: Fri, 12 Sep 2025 23:44:39 GMT  
		Size: 52.2 MB (52165358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918217f235fdec6c2a70be342f34069358ec4fe6efee15a0fb9b74f942290d49`  
		Last Modified: Sat, 13 Sep 2025 03:21:39 GMT  
		Size: 18.0 MB (17959721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928ed231d05fe45024a52f59c4e859a8da40a9d3ceb3770d33044c19bc758a5a`  
		Last Modified: Sat, 13 Sep 2025 03:21:39 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3f9507944c11b92eafef0663014a2d7f28c6aec7b9b20520b51245c2b9be31b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2869311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c006c341f5425fb0cbe30cefae42c7a748194cd4ec6f109c214526292cc2fc`

```dockerfile
```

-	Layers:
	-	`sha256:53cbb54024530f40412d74124faf64726f2816fa3548bf070b70bd478a836616`  
		Last Modified: Sat, 13 Sep 2025 06:41:11 GMT  
		Size: 2.9 MB (2852824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:181ef23f079f79181a5ba4c17f517bd203b884d11c47c7e2f7865b1eff7d96fe`  
		Last Modified: Sat, 13 Sep 2025 06:41:12 GMT  
		Size: 16.5 KB (16487 bytes)  
		MIME: application/vnd.in-toto+json
