## `clojure:temurin-11-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:0f7745d5c1130594377505e855a6c164c14c389f04ad877f1bf39ecbaa2d220f
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

### `clojure:temurin-11-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8d5072dc840d820690d23d3ab6030a5440e8c973606a5a38289168c7936bf25d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196320511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384d2ddd28b08b8282911ca06f7fe2a105e32b51f9b889f83abb9a37d796e73a`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:02:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:02:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:02:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:02:10 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:02:10 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:02:10 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:02:25 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:02:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:02:25 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:02:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:02:26 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68b348288f592db1b2069e93d1cd0473f8b37355800ec37267a4d9969c6aed2`  
		Last Modified: Wed, 15 Apr 2026 22:02:45 GMT  
		Size: 145.8 MB (145806832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cc2f394383ec97f32f4d2c61a0f6e93c84508d4f960ad31bf827c14393679a`  
		Last Modified: Wed, 15 Apr 2026 22:02:42 GMT  
		Size: 17.8 MB (17759600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f62ad3878c87a082c3b4a35b60b430a55e448bba42d7e6cc5b1eb6854b80d7`  
		Last Modified: Wed, 15 Apr 2026 22:02:42 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9838168ee740b2ea24b838dbd67b3091b81044a7ae9259070f3bcdcd70fef6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2766602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b02a64acc2164ea8ba43aa4bf06b5b04810687d8f68de12dd4fb46a75186948c`

```dockerfile
```

-	Layers:
	-	`sha256:05e7c9b33dad63ab342f55d7442f52bfef69a881ef8dfa55fda05befb3086f7d`  
		Last Modified: Wed, 15 Apr 2026 22:02:42 GMT  
		Size: 2.8 MB (2750191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d4617f891b2d6d2dc24a79638e0f387aac4f0a357e2b9131ab726da111cc775`  
		Last Modified: Wed, 15 Apr 2026 22:02:41 GMT  
		Size: 16.4 KB (16411 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:63d0e6fddffb8cc8c5fe41baaa14e4c6f18fc2e02083d47209e1edde63d63364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.7 MB (192727696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e263b8ea17e8ecbde948a7ada1d677252feae0fa5c0e3ab0141200b4a5a6ade8`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:20:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:20:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:20:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:20:07 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 02:20:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 02:20:07 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:20:21 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 02:20:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 02:20:21 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 02:20:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 02:20:22 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7f8d2c4ca9db471bf1eaedacd1638cc9cac53407b3dfb16a04a85d9ab22c92`  
		Last Modified: Wed, 22 Apr 2026 02:20:43 GMT  
		Size: 142.5 MB (142500806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbd9121de3f98e3c683e6a44d863648cdb47113c6123708250cd4f011facdd6`  
		Last Modified: Wed, 22 Apr 2026 02:20:40 GMT  
		Size: 17.6 MB (17593038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3f0ed6fdfbde9b83f584f3d5729087841ffb86814a4c9138f681fd03dad3cf`  
		Last Modified: Wed, 22 Apr 2026 02:20:39 GMT  
		Size: 4.5 MB (4517706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1800e93a9a71adc5ee98889f1e2dd71e34cea06c3eec4f2ae69d69336fb8ca9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2766956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f425420a6ffd404949623fde762dab3832a0037e541206eb2abdf9c9b2036f`

```dockerfile
```

-	Layers:
	-	`sha256:8784a6c986e0dcd4edf94971ee308d86eccf0ede029f4ffabb4c98d44f9b9739`  
		Last Modified: Wed, 22 Apr 2026 02:20:39 GMT  
		Size: 2.8 MB (2750424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d5a3e04592938a24101da5344dab402076df88f596b2c6f8fa894aea12fb7b2`  
		Last Modified: Wed, 22 Apr 2026 02:20:38 GMT  
		Size: 16.5 KB (16532 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:6af395b818cce8cddfb3e3b5473f88d8d07df3a06f19df746df46a0f90fb9b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187554982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2061297c5e3bf7e2b5f3053d00f68aab066ae91e5d9b3b3f5d65c1c6a132c280`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 02:39:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:39:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:39:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:39:38 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 02:39:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 02:39:38 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 02:40:03 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 02:40:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 02:40:03 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 02:40:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 02:40:09 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b1c56220ca211bc9d02f1ed5c589465809676b6ab2cef705f1e2fb8e9726de76`  
		Last Modified: Tue, 07 Apr 2026 00:09:42 GMT  
		Size: 32.1 MB (32078464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c2b4249a5f9d02d5abe9b0b44777395a74fe0b79fd16dd95566bff1dc3ac16`  
		Last Modified: Thu, 16 Apr 2026 02:40:45 GMT  
		Size: 133.0 MB (132997415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe4839b3ed8038b966d81e2dc17fa5f0fdd36c7302218efdc50fb19d5757c37`  
		Last Modified: Thu, 16 Apr 2026 02:40:42 GMT  
		Size: 18.0 MB (17961340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166e08d417a063b4d4b35b99fa474bcd7e70028ac122d38bd829d289f97fa1b1`  
		Last Modified: Thu, 16 Apr 2026 02:40:41 GMT  
		Size: 4.5 MB (4517731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5dc7f2023071249d58f6ac3d76b53178384075a69eb226ab26e84b3c9d3f6688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2767865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a746cf81cb2f9c9bf8049fc61d2d0229825fd8222a004a9f91a848ad3a1697e`

```dockerfile
```

-	Layers:
	-	`sha256:983a3bf81a0ec01ec43b9fc86aa1566fd7d28053631ddb8b69b4f850824458b1`  
		Last Modified: Thu, 16 Apr 2026 02:40:41 GMT  
		Size: 2.8 MB (2751409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f73927c9a54c51c2a92a73ed0cc417eb98d9e3df924be297c63d474a99a9a841`  
		Last Modified: Thu, 16 Apr 2026 02:40:41 GMT  
		Size: 16.5 KB (16456 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:4e6b2129af14aa028a0efc8821982e404e989afc3ce742a26cbde04d3e58c8f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175393509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16bbe981913bd55415dc80b5aeac201e1e677e0536f648858aa2aa20506fb18e`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 00:34:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:34:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:34:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:34:59 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 00:34:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 00:34:59 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:35:09 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 00:35:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 00:35:09 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 00:35:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 00:35:10 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3136158d6d52c18c8b86a696a972abe97e7e16324bf358cbdcffb25ae4dfaea6`  
		Last Modified: Thu, 16 Apr 2026 00:35:35 GMT  
		Size: 126.6 MB (126562154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b4f0f6d4807f7d0419cf509b1a29f45445a3368291f843772b4926f768b610`  
		Last Modified: Thu, 16 Apr 2026 00:35:33 GMT  
		Size: 17.4 MB (17421972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd036995dba17ab497900596eb6f7fc9aca9fcd75fe603340889453650c7069c`  
		Last Modified: Thu, 16 Apr 2026 00:35:32 GMT  
		Size: 4.5 MB (4517717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7953d089a20b2ef3be0ffc88b49fa966bb0fea4a061c9b4772fe2a5387080de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2758421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ad38e66fb4e346bdb8c7033ac34be2ed0011da53645920f2dc4fca85493cf34`

```dockerfile
```

-	Layers:
	-	`sha256:f664e8d38421bf519042709bdd54f0d23ba53a7966de0dd379d583a229a0b058`  
		Last Modified: Thu, 16 Apr 2026 00:35:32 GMT  
		Size: 2.7 MB (2742009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c9e0f3a5a73e6e1e658a1fb8f88a31e028fd0ee64e65f8601cd0d6e4199ea41`  
		Last Modified: Thu, 16 Apr 2026 00:35:32 GMT  
		Size: 16.4 KB (16412 bytes)  
		MIME: application/vnd.in-toto+json
