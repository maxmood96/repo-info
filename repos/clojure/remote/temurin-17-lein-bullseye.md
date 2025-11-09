## `clojure:temurin-17-lein-bullseye`

```console
$ docker pull clojure@sha256:fcbcca576e782ed272e4e95c15c34f39c9fb4f6b8bc689766405f1b2b693a66e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:3fae4dcb0325768d9e0cebb2923ceb2a15d325fecf8670e0d13987579c2fa1a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.7 MB (219730522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dafb96f6fcc318791178cf165eef38b028a8aabb46fed0dcd00b9064f9e97bca`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Sat, 08 Nov 2025 18:42:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:42:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:42:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:42:38 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:42:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:42:38 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:42:51 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 18:42:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:42:51 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:42:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:42:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:42:53 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:42:53 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b51cef6f04b362121745398e6168e8f9a54a1dd6f12779e017eb75363f565f`  
		Last Modified: Sat, 08 Nov 2025 18:43:13 GMT  
		Size: 144.8 MB (144848032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebbea598232db11bb2c5fc693a53c79c6a1e41860b02c4af45007b863aaaf90`  
		Last Modified: Sat, 08 Nov 2025 18:43:19 GMT  
		Size: 16.6 MB (16607603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947d490253c6ef6655f9d7d34a12860631be9ed6d2822a69787596965116d537`  
		Last Modified: Sat, 08 Nov 2025 18:43:17 GMT  
		Size: 4.5 MB (4517764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0090680aef0fa73b3cea68439f15ff4334b5932360e175cb6bf016bc331f14`  
		Last Modified: Sat, 08 Nov 2025 18:43:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b5d3d64a59c3728ad0f52c56b1e90a7b2ecabf7a9e0d678c3a6a9dfbf0450538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff453ff3df93e97352edcb10519dd781921614d9bd5754bbd9fd5327ca31874`

```dockerfile
```

-	Layers:
	-	`sha256:4b18f08d7417323dc9cfa908a2451443b2f634c598fa7181e29dc09f048e82c0`  
		Last Modified: Sat, 08 Nov 2025 22:42:45 GMT  
		Size: 4.5 MB (4476190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dfb6a07d59323ac17b905fe2eae6aded856673ac0296a4807d63d85ed114b77`  
		Last Modified: Sat, 08 Nov 2025 22:42:46 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:68a7027ad7855b73c07c22868422ed1366101862698317a199b1464cd71b8ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.1 MB (217051103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9713940edbad23182479154c6c8fd354a5bf73cf7371574c8798a398a56f03a8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Sat, 08 Nov 2025 18:42:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:42:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:42:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:42:00 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:42:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:42:00 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:42:13 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 18:42:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:42:13 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:42:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:42:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:42:15 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:42:15 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74f519a29ea735ab7e588a22b76f7ef04c72e3e79ef341e7c2c64d229f4cf9c`  
		Last Modified: Sat, 08 Nov 2025 18:42:36 GMT  
		Size: 143.7 MB (143679949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae84cfb3925b3b39aa62eea2b73a11ff793b5545d96a3aba6a8458b5bf5497f`  
		Last Modified: Sat, 08 Nov 2025 18:43:00 GMT  
		Size: 16.6 MB (16595000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6a735143932a34b2d90be8120a7a686a2174d8ef0b6b58102b82f68ad2033f`  
		Last Modified: Sat, 08 Nov 2025 18:42:58 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a43a5f315545f61c9a4014f47963e966083098f56bfd9fcb712ef1fbf5bc5aa`  
		Last Modified: Sat, 08 Nov 2025 18:42:57 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:dbe7e147eb1ad036932cbfb4ae3a8c9ed5a3cbbef079ed1fc33c3838505f0b30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4493653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b133a9977d47a2fd260a60ce40a401a7e484704683fb715f499e6de9dda7040a`

```dockerfile
```

-	Layers:
	-	`sha256:693fd45f0cefc7a6bf2b580ac4d60cca5acfd74cce16305df835418fd861ceaa`  
		Last Modified: Sat, 08 Nov 2025 22:42:51 GMT  
		Size: 4.5 MB (4475164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:976a904067004f53ef8ae338de8ba1fbef81abe277d244425ddf632ba6b93b6f`  
		Last Modified: Sat, 08 Nov 2025 22:42:51 GMT  
		Size: 18.5 KB (18489 bytes)  
		MIME: application/vnd.in-toto+json
