## `clojure:temurin-11-lein-bookworm`

```console
$ docker pull clojure@sha256:cec78be3f13cc8f3a248f889a42beb2bd72c7fffbf3e3de75a582713336aee61
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:149af4f524e8ea610cb9d393f5ffc6e49e3ab34ac8f11dc6d2180a9dcdd1c43f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.7 MB (260667363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75adc573f5c725333f33fcc5f22ed908fe901a7eb5f13113a7460f724a954a8d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b406ab550b4de255fd2ff0fb62ae66241c6dd7c3d079153103cf76f9ee74b03`  
		Last Modified: Wed, 09 Apr 2025 02:18:20 GMT  
		Size: 145.6 MB (145598775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75908eb1c8123915e60bb3a52095a5a5422e23f794de8f73e98dffa0574de37`  
		Last Modified: Wed, 09 Apr 2025 02:18:19 GMT  
		Size: 62.1 MB (62063864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec34f50a7fc4925732dcd4d4fe87adc59d5262d75ee2ba9b0bb5add82a361df`  
		Last Modified: Wed, 09 Apr 2025 02:18:18 GMT  
		Size: 4.5 MB (4514151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:bad497534f68fbc6f3ed12ffbe06e1de9eee98ed70aa42121df35c74ad9ef255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6572216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eba890a9944c5aa0ba7a341bb10ff24da0a83c9e4130fde3404814327a06db9`

```dockerfile
```

-	Layers:
	-	`sha256:010f65e47eb093e74d868271b9131f4288149a457cd7101e5bb63fc5701f7833`  
		Last Modified: Wed, 09 Apr 2025 02:18:18 GMT  
		Size: 6.6 MB (6555784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c082f11690584e6755619df7bd9564db2835327b0563b98bd2b0a7c22fc255f`  
		Last Modified: Wed, 09 Apr 2025 02:18:18 GMT  
		Size: 16.4 KB (16432 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:12ff7df967040a46309172545f4976adc7d94755df2e4d1ee4db75738db1b07a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.3 MB (257264052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d1535357bed76b51bc09af068a4588299cc483ab2679eec1a3211c386ad694`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d926e90db35cca6126785829dde031c8fcebbfdb21acc2a6b6101133a074bc9`  
		Last Modified: Wed, 09 Apr 2025 17:20:35 GMT  
		Size: 142.4 MB (142385537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2644d8f3ab49f0b8c4318f0b1d84bce7a95a61f2a0463b140826c124df3615a`  
		Last Modified: Wed, 09 Apr 2025 17:20:34 GMT  
		Size: 62.0 MB (62036864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4709152a668078d799e275848ef815afba9e3921fed41046e5727c221e4969be`  
		Last Modified: Wed, 09 Apr 2025 17:20:32 GMT  
		Size: 4.5 MB (4514150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:6c81d13005d13eb647a04e00bad02797241f77945de96891d2976fd814121614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6578650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec698fb3ac1348fed9539bc0e154250d822a4e2204d4b62d4d2c56a743b99ba`

```dockerfile
```

-	Layers:
	-	`sha256:724b1c9a2d25aeafef40304efa38c56b27605f6ff42948c59fa60e19e5496f0a`  
		Last Modified: Wed, 09 Apr 2025 17:20:32 GMT  
		Size: 6.6 MB (6562096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:983808603312e1db51e749455b4753e4aa17b2e61386ecf16053e41bd9bd37b5`  
		Last Modified: Wed, 09 Apr 2025 17:20:32 GMT  
		Size: 16.6 KB (16554 bytes)  
		MIME: application/vnd.in-toto+json
