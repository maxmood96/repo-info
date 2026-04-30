## `clojure:temurin-11-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:2968cabcb192a597c66c0b6bd8b2f6cbf452e6b575366c6987674c151c3bacfc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:509cf9c066447376ab89bc3585f97dd1c4dc5457d3df93bba50265e9b618d723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.4 MB (196399820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e2ee1180956e87602fc3e65e8fb8c02fa485fe48168326f3dc507d7820e800b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 29 Apr 2026 23:14:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:14:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:14:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:14:42 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 29 Apr 2026 23:14:42 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 29 Apr 2026 23:14:42 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:14:55 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 29 Apr 2026 23:14:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 29 Apr 2026 23:14:55 GMT
ENV LEIN_ROOT=1
# Wed, 29 Apr 2026 23:14:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 29 Apr 2026 23:14:56 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3eb1d54a8fd96c811fffa556d192cf4aed876de6757a076bb99cc7e724b736`  
		Last Modified: Wed, 29 Apr 2026 23:15:19 GMT  
		Size: 145.9 MB (145886252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c333cd643804837930f943843a78fa8d08b57249f198ad2299c93eb000d1a3c`  
		Last Modified: Wed, 29 Apr 2026 23:15:16 GMT  
		Size: 17.8 MB (17759563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f904bfc1a70fde04f15701104f2852f4406444ab8305d9649f0dd02c634102`  
		Last Modified: Wed, 29 Apr 2026 23:15:15 GMT  
		Size: 4.5 MB (4517721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:938508f49e1a3c9acc9a3e38246080c7279ee10a62e1521e80cca63a893f1670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2766605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:475bbdcee1f712b0fdec09e3d52b14d01765592ca96d7aaa74a8ea9268693f89`

```dockerfile
```

-	Layers:
	-	`sha256:b09aeb99a824869ec960ff84270d100bf1d118b0cb23e6d82a8c0f1b1155f78c`  
		Last Modified: Wed, 29 Apr 2026 23:15:15 GMT  
		Size: 2.8 MB (2750193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e059bcc6480538dad410ec6e12423706697d0b6607608be98f656f37af97e73e`  
		Last Modified: Wed, 29 Apr 2026 23:15:15 GMT  
		Size: 16.4 KB (16412 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f23291ba48801496818bbb38b1e9161b80ec143b609780f40be4513cc8695e69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.8 MB (192810878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38241897cd3f579e7a07793229c89091476dacbee66bfb06cff7c9384bc276db`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 29 Apr 2026 23:14:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:14:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:14:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:14:03 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 29 Apr 2026 23:14:03 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 29 Apr 2026 23:14:03 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:14:17 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 29 Apr 2026 23:14:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 29 Apr 2026 23:14:17 GMT
ENV LEIN_ROOT=1
# Wed, 29 Apr 2026 23:14:19 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 29 Apr 2026 23:14:19 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728416c9fefc01ce85204d0b38ed48456c0f80ce0df70f4e0d807c4d064b3673`  
		Last Modified: Wed, 29 Apr 2026 23:14:38 GMT  
		Size: 142.6 MB (142583979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575c70493d55e31c9d13ee6c58c6e5693042b4002e454e4e6c645209245af97e`  
		Last Modified: Wed, 29 Apr 2026 23:14:35 GMT  
		Size: 17.6 MB (17593030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62123379daf1fabf9f1f9d54d20d8927288457ccb4ddc06728c58a257bf31d3a`  
		Last Modified: Wed, 29 Apr 2026 23:14:35 GMT  
		Size: 4.5 MB (4517723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c754284e9e3c4a91460ae9778b544f9c61013af6be3258ed5502fb3d2f374572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2766958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd3b15e8cc2b55f959304f535bfe45b5a1b9cfce721b9c11af17aeef1f5ee02e`

```dockerfile
```

-	Layers:
	-	`sha256:68ad9792f55deb77ada9d054ba9cb55b2eb39ea0c47349cf831f086be7b9f9be`  
		Last Modified: Wed, 29 Apr 2026 23:14:34 GMT  
		Size: 2.8 MB (2750426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8285721d0e26d49dea8642c76a7e62af331a6858353a3d4eed06a78d2f8a0f7e`  
		Last Modified: Wed, 29 Apr 2026 23:14:34 GMT  
		Size: 16.5 KB (16532 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:494bcf5cc336731afcc72008859850df85696598ddd6a784e4e6589bae9927f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187667138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2baf1bed73afa2d26f1f831c62c127e035987866854c7d8e723563230c850372`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Wed, 29 Apr 2026 23:24:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:24:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:24:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:24:01 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 29 Apr 2026 23:24:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 29 Apr 2026 23:24:01 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:24:39 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 29 Apr 2026 23:24:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 29 Apr 2026 23:24:39 GMT
ENV LEIN_ROOT=1
# Wed, 29 Apr 2026 23:24:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 29 Apr 2026 23:24:46 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:0bcb46f6315f7a2c8ddde875fca21de96c94e451046e6692f77a99aca489f3be`  
		Last Modified: Wed, 22 Apr 2026 00:15:02 GMT  
		Size: 32.1 MB (32078402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708b07913b504d6aaadb438509b6f4cb2908200d51c3b63cefa839b8f462833b`  
		Last Modified: Wed, 29 Apr 2026 23:25:32 GMT  
		Size: 133.1 MB (133109605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981ef6b365a8558894288ba2c7f1b4ed3aebd6be819a4a902fe237425ee5c179`  
		Last Modified: Wed, 29 Apr 2026 23:25:30 GMT  
		Size: 18.0 MB (17961345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee863aad4141f6fff0754fa66985efe073486e44d5f33e19b8c5b552591a3d3`  
		Last Modified: Wed, 29 Apr 2026 23:25:29 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:38175df4cd04a0abaf040eed5d5acef7ca6d1c5bb1fc78095505bd4225261f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2767867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d872b5c422aea1f38cbb3bc28ee9c8b7c5cd0ca580b3c0bf2c991d56700ea955`

```dockerfile
```

-	Layers:
	-	`sha256:8598e726a2f1e06c7b6d83af75212d1312be9b943e20329d6e712c0008b089f9`  
		Last Modified: Wed, 29 Apr 2026 23:25:29 GMT  
		Size: 2.8 MB (2751411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f2e5b299afe4c82d5d2c283b479ca3a4c7bdbfb53b43525095caf91e6a1ba1e`  
		Last Modified: Wed, 29 Apr 2026 23:25:28 GMT  
		Size: 16.5 KB (16456 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:1073845fea06a914178d205933a302355b77a0e501eb7435d46f4bc97ba41892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175483998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ce9ab316be692f4ca9c384f099a0ebc0d1e5c987fb4395af2fd4af6cdb4bd7`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 29 Apr 2026 23:13:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:13:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:13:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:13:31 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 29 Apr 2026 23:13:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 29 Apr 2026 23:13:31 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:13:41 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 29 Apr 2026 23:13:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 29 Apr 2026 23:13:41 GMT
ENV LEIN_ROOT=1
# Wed, 29 Apr 2026 23:13:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 29 Apr 2026 23:13:42 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb51d1f6103c562773e5ad9b244bea0d905640ceeb1f8ac3e09c56a4396e5429`  
		Last Modified: Wed, 29 Apr 2026 23:14:06 GMT  
		Size: 126.7 MB (126652697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df2947cfb44a9c7361d06d2241f7704e2078535e5c5cfeb47b5ba2c5807b7c7`  
		Last Modified: Wed, 29 Apr 2026 23:14:05 GMT  
		Size: 17.4 MB (17421991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dff3bb9322504cb736b0b42224da7c4081ef898a7e0c4c4f446e60c669e34b1`  
		Last Modified: Wed, 29 Apr 2026 23:14:04 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1ca6425fd91ff74a7d89db603437bbba9c3c350efdb4e6441ee1ba8dc873e1f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2758423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7a801c79180886b18e2a1b747f8001485c2d127b62780f175fb16a44fafcd5`

```dockerfile
```

-	Layers:
	-	`sha256:e521abc0f61871380fe08eb46b886ced977fde445840294273d48970b3f931be`  
		Last Modified: Wed, 29 Apr 2026 23:14:04 GMT  
		Size: 2.7 MB (2742011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a7ce1d0705911edb6d8515907ef0c102c3dcc588259030928d0feaffdfda49`  
		Last Modified: Wed, 29 Apr 2026 23:14:04 GMT  
		Size: 16.4 KB (16412 bytes)  
		MIME: application/vnd.in-toto+json
