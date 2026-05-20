## `clojure:temurin-8-lein-trixie-slim`

```console
$ docker pull clojure@sha256:6cc0eb753ca3a5b121d4698b490e9301c046c40ea09a921b2fe35626b3477298
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ce60b036113fd365227db201643549bc8824c9afc2f4f95695d4a7bca60ffd55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.9 MB (105944548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3970f71cc440d4a5ee956e8f5b9897d8a1cebd1f63715a3a2d3a4b0aad8aae45`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:56:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:56:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:56:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:56:20 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 19 May 2026 23:56:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 19 May 2026 23:56:20 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:56:35 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 19 May 2026 23:56:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 May 2026 23:56:35 GMT
ENV LEIN_ROOT=1
# Tue, 19 May 2026 23:56:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 19 May 2026 23:56:36 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:692256d54441d556e604c280c71753ac5d55cf487a1838adb36ffc2882d5d397`  
		Last Modified: Tue, 19 May 2026 23:56:49 GMT  
		Size: 55.2 MB (55198685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e00aac9384e9fefa694e5b1bd693cd0fafed87bf7ffa2fe09db7ceca268ad41`  
		Last Modified: Tue, 19 May 2026 23:56:48 GMT  
		Size: 16.4 MB (16448147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb27c3257d8f052b3e51e6df952588a9370e337a001273e55e5e39e93a26ac45`  
		Last Modified: Tue, 19 May 2026 23:56:48 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:aedfdf6b63afc1d81cba0c868e082398b8d70ecb003c27b26377de240d489260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2502355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205abe60b2cfbfc8f996389411e572bfa4c250e5236e27ecc755553ebe896926`

```dockerfile
```

-	Layers:
	-	`sha256:81dc883a3804a1ba2bdcc29e0b49633d5b29682dde8a36d4edd3a4b039fe6080`  
		Last Modified: Tue, 19 May 2026 23:56:47 GMT  
		Size: 2.5 MB (2485819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7eb0f3f5aa7281c9f003a1aff5d547d4fe41a8781b9cdc29f213c53477e4fb5e`  
		Last Modified: Tue, 19 May 2026 23:56:47 GMT  
		Size: 16.5 KB (16536 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:61ea6a7ce5b6a9ce909a732fe8b27c7acd5e487c679d262f5533e8d893860d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105346824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee645db86a0587ac6b0fc67ff65a028ab33ddca02df7f6ddc093b7049298442d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:03:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:03:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:03:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:03:25 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 00:03:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:03:25 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:03:44 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:03:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:03:44 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:03:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:03:46 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa64a52fb10af27921f15bfa4a2f9c8430e12cbb0e781cfa5868fb6ce1dce49e`  
		Last Modified: Wed, 20 May 2026 00:04:00 GMT  
		Size: 54.3 MB (54272922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a65bd235d804b4bc601105db2743b291c17136baaa76c0771c402e0fd54c1c`  
		Last Modified: Wed, 20 May 2026 00:03:59 GMT  
		Size: 16.4 MB (16414229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d749395bf1dac0afc665eafb40810614e08c936cc75bd70e465a2ba3b43a525`  
		Last Modified: Wed, 20 May 2026 00:03:58 GMT  
		Size: 4.5 MB (4517722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c7ffd239d3a7d41fcd79b183b6d55021103ad4e91bda4267a40dc7be11282c13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2502785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8994e5993ffd58b0f7e50ac97853c6b9306ca311389630ea0af6f5347acbbab`

```dockerfile
```

-	Layers:
	-	`sha256:5c5fd27fc86b402d026097324f0af6cabfc87090ff9983321d681d93841c842b`  
		Last Modified: Wed, 20 May 2026 00:03:58 GMT  
		Size: 2.5 MB (2486129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d30a279404787a514587ecc383e61ec0f12547bdbba94e0775a87bf123028292`  
		Last Modified: Wed, 20 May 2026 00:03:58 GMT  
		Size: 16.7 KB (16656 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:450f519b521c21929deec5e05a010ac527dbf1e7991735c7d189e000908348aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107270411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33dacc41ad875d3fa009ba5e332eb6f2d9c2e30b5b77381d314a38d85fd38c96`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Tue, 12 May 2026 21:49:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:49:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 12 May 2026 21:49:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:49:10 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 12 May 2026 21:49:10 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 12 May 2026 21:49:11 GMT
WORKDIR /tmp
# Tue, 12 May 2026 21:49:42 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 12 May 2026 21:49:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 May 2026 21:49:42 GMT
ENV LEIN_ROOT=1
# Tue, 12 May 2026 21:49:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 12 May 2026 21:49:46 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6108e5c2a2245ec0c51d22b23687faec2598356811a7675057929aac5f8deda`  
		Last Modified: Tue, 12 May 2026 21:50:14 GMT  
		Size: 52.7 MB (52669152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73eea7c64b122d3ca1bab5daf54c95cf74edd79e9e722f81850194881650d9c8`  
		Last Modified: Tue, 12 May 2026 21:50:12 GMT  
		Size: 16.5 MB (16485373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89c436a1ee97476ba6326351e407457b4b175f610e510b3e25ded6cd8e38d46`  
		Last Modified: Tue, 12 May 2026 21:50:11 GMT  
		Size: 4.5 MB (4517767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5ced0475b3d03ac879502ddd9b82d7a17039b7c0d79d1b669f5258affa1475d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2503932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd7fe389b016206657a721d6240c64ed90ced96a5f121e352a6303dbbba58d6`

```dockerfile
```

-	Layers:
	-	`sha256:ff4f1c7a043438ab4ea8741518e306cb5fe1b0f8c173b1800e6478643116f676`  
		Last Modified: Tue, 12 May 2026 21:50:11 GMT  
		Size: 2.5 MB (2487352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46679d1fde88f3d1f53b8c239f30b63938b52ebc6ea7e3178815691378678760`  
		Last Modified: Tue, 12 May 2026 21:50:11 GMT  
		Size: 16.6 KB (16580 bytes)  
		MIME: application/vnd.in-toto+json
