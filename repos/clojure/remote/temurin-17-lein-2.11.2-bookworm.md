## `clojure:temurin-17-lein-2.11.2-bookworm`

```console
$ docker pull clojure@sha256:23adc787175dfb6458738a5afc6ffb0cd98f4b63f6fc99f3a8a52b1b88b3a4aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-2.11.2-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:fe3abbc9a67f26e2dae08b2c6e17a93920e7ede56f6eb6090bc8a0622d24b520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259635474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e081ae3fe7be2845191473bc808c660b58ff828f5e7a5be9e34e3a9ca6a28b6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc04dbff0a4d215f45a72d8cef989bc7ce5ef11e59cd0907a215064667d4133c`  
		Last Modified: Wed, 09 Apr 2025 02:49:09 GMT  
		Size: 144.6 MB (144566524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15448cf35a034281a208566957da510de72cf1e2e445c0598c0d6bd2b473199c`  
		Last Modified: Wed, 09 Apr 2025 02:49:08 GMT  
		Size: 62.1 MB (62063813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfb28a5e8afa501ff58b93755773b29f67dde2bc3318d99d96b7ad843ddba71`  
		Last Modified: Wed, 09 Apr 2025 02:49:07 GMT  
		Size: 4.5 MB (4514165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919b594829d5ceabfd429b6191e6095cf9cd8ca81998a9c905d41dca9febebe8`  
		Last Modified: Wed, 09 Apr 2025 02:49:07 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.11.2-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d856579e3f4633a9bb4b2e9497db01111675eed8e0b1d16291bdb796f59c282a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6554066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf1fc5d3a3bebb7a77068a8a7c0632ffa4facca9d2e60b6774169d604907e6f0`

```dockerfile
```

-	Layers:
	-	`sha256:b6bfe4f3d869cd1329954312888d551a2d1dc258fccc057e40977d8b4a1138f6`  
		Last Modified: Wed, 09 Apr 2025 02:49:07 GMT  
		Size: 6.5 MB (6535643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84b4ee114e753fabca4f0b3744ed7d06e592f150553a08c51b692bccf30418f5`  
		Last Modified: Wed, 09 Apr 2025 02:49:07 GMT  
		Size: 18.4 KB (18423 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.11.2-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8a9846fe8e58ed39a6bd007cd6c6b3904973da8888c0799dddbb3435ae4790b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.3 MB (258333545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f18245c9a80473a9b5486543f75e497aa0536b0ab859c528c3aa9c0900ce32`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5e91e8e96d8f5d24cdce2a10001dede19a57e329cfcef9040f34b97b4b9226`  
		Last Modified: Wed, 09 Apr 2025 17:29:25 GMT  
		Size: 143.5 MB (143454606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781b207a75b73767e3bca0e5af2ee60d5da3a52334dbbf0a3b463b1a3588bc68`  
		Last Modified: Wed, 09 Apr 2025 17:29:23 GMT  
		Size: 62.0 MB (62036852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc47d6fb18e13f03cb55a3eac704b260ab7e16c203acda7a1944c4335c20504`  
		Last Modified: Wed, 09 Apr 2025 17:29:22 GMT  
		Size: 4.5 MB (4514189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13674d580c0b566b4b7bbd6657a334eb876eae3fd0e3fc7a6488e1612ab1d51`  
		Last Modified: Wed, 09 Apr 2025 17:29:21 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.11.2-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:bb72937eca348440976fa919a8d1162c1174258c3d7fd525d3f7fed7e1448ebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6559881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a59689592e6b1dd014610cb4faecaf834386fccf25de7fb0ed4b3a8d5de81d0`

```dockerfile
```

-	Layers:
	-	`sha256:6214334bbca11cf5b71e693ecf83ab033672e33d2162f5ff4327ff86c23835c7`  
		Last Modified: Wed, 09 Apr 2025 17:29:22 GMT  
		Size: 6.5 MB (6541337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a96f9ad8e02806c08168204696d6a26d301cbe279c11eb4aa95e24b153081a51`  
		Last Modified: Wed, 09 Apr 2025 17:29:21 GMT  
		Size: 18.5 KB (18544 bytes)  
		MIME: application/vnd.in-toto+json
