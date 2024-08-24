## `clojure:temurin-17-lein-2.11.2-bullseye-slim`

```console
$ docker pull clojure@sha256:d255b3e2580d871953b7b5aad3d58440f7a4a2d8927a1b6722a84ab3518feee4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-2.11.2-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6c7728af6e173795d76217c9146c2f3c3a9d0f2bed0069af2021bce743a71b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224131296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92bc2772df2ca05c37c16f901a8ee22881ca0ac69a51d8c196ab934907bb78b3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_ROOT=1
# Wed, 07 Aug 2024 18:04:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07abb79a89876f8ba1079409aa46960fedd2958bebbfe9ba0e1c70e37e37c2c9`  
		Last Modified: Fri, 23 Aug 2024 20:02:25 GMT  
		Size: 145.2 MB (145166526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262c7d78d03ee34a690ae9bfa90bd9ad43d4d05a6ab09a3c27fb144631c321eb`  
		Last Modified: Fri, 23 Aug 2024 20:02:26 GMT  
		Size: 43.1 MB (43137976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c79cb024fa8bc17a3f983adbb8442978d201af62ee3c365582006e8072aecf`  
		Last Modified: Fri, 23 Aug 2024 20:02:24 GMT  
		Size: 4.4 MB (4398078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1523a3048ce1e3db7b588e4fc38e16caa2935a8ae5702dd85e18ce1fa9b49c5c`  
		Last Modified: Fri, 23 Aug 2024 20:02:24 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.11.2-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8b707b991fd32fce74470d347d0d5f0620662d76f4b5686bbe35e099433a6d13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4419178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d578bed3e9241275a21b02e40ef09c607ba8cc413e4d6bc65a336e2ddb6f16b3`

```dockerfile
```

-	Layers:
	-	`sha256:22e972180d5d738d4d2ba9fc7dad709eac116bfd29b7daab595a95ca2c0dd52d`  
		Last Modified: Fri, 23 Aug 2024 20:02:24 GMT  
		Size: 4.4 MB (4401086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b8f6d229fc3b11517aa0298807a95f0ad02a99caaf05f87fbe5f1376781d73d`  
		Last Modified: Fri, 23 Aug 2024 20:02:24 GMT  
		Size: 18.1 KB (18092 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.11.2-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f700d596ddf48d417639c37ace3dbb43a03d4f7eeeabf2bf5152a17f40617459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.6 MB (221591326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b4aa42287d8bc5fdab45587f67a7ad7c1012911f87c79eed980324f1fd284f6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:525ed0be34230ce7681869b24f133a402b8bc0a4a64bc89e368b25ccca391579 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_ROOT=1
# Wed, 07 Aug 2024 18:04:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3f559f8680cb633039b8f423453ed0a0797f65d0a9ac051861edb9ba7ac94711`  
		Last Modified: Tue, 13 Aug 2024 00:43:24 GMT  
		Size: 30.1 MB (30076087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c229b6d4698a9454e9c62693654360cc097801af308b176ca82da1b9fb41517`  
		Last Modified: Sat, 17 Aug 2024 06:14:12 GMT  
		Size: 144.0 MB (143959474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7240d6db9139ed880bbdcced5f82cbe07adb0dce0696967a1a04066000f7c0`  
		Last Modified: Sat, 17 Aug 2024 06:14:10 GMT  
		Size: 43.2 MB (43157302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103bb360f9b08bba761c86326ae953748cdd71da0ef69b3aab4b8f38a797fa1a`  
		Last Modified: Sat, 17 Aug 2024 06:14:09 GMT  
		Size: 4.4 MB (4398034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc2927fca192da7619fff72add31773bc1fbe44c60c45d4fd41779a10e1a56e`  
		Last Modified: Sat, 17 Aug 2024 06:14:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.11.2-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9b90beb57898373162dfdbdf5eee9988173fa6fa9a77b3fb02ad74786d2c27e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4425995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc1553b623bef5250130c6ce2de525c71deb467f868f2d515f238e2ad0a484f0`

```dockerfile
```

-	Layers:
	-	`sha256:dfa4bac5e2e8179a9ec07424a7b618149bb12e66804a3503a1352aa689dbb7f2`  
		Last Modified: Sat, 17 Aug 2024 06:14:09 GMT  
		Size: 4.4 MB (4407374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9ee603801fea32b4bd7110ff82c45c948331987989c3e33f04adcbed78c52e1`  
		Last Modified: Sat, 17 Aug 2024 06:14:09 GMT  
		Size: 18.6 KB (18621 bytes)  
		MIME: application/vnd.in-toto+json
