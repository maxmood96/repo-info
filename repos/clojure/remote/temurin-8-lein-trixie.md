## `clojure:temurin-8-lein-trixie`

```console
$ docker pull clojure@sha256:727c7edc7ea48f8a3eca053f504d85c6edbf3e078aa4393d065f78bd5be03565
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:6d18f40faf09649de1b44d36067a34401a85803f53371d2abaa51eaa7e69d561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127120312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdfb947685e17d3da06726fb56eba0619e27c596b98a56680a0ea1d659e0699c`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:50:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:50:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:50:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:50:13 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 00:50:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 00:50:13 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:50:30 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 00:50:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 00:50:30 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 00:50:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 00:50:31 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:281b80c799ded5b9a390d2e8c59930db01ee395ab809dd34259897c660751f4e`  
		Last Modified: Mon, 29 Dec 2025 22:31:07 GMT  
		Size: 49.3 MB (49289587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ad217b125aea418bab4cab357cad85451a1d41a84d7cfbee510616606df4c9`  
		Last Modified: Tue, 30 Dec 2025 00:50:57 GMT  
		Size: 54.7 MB (54733371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f78be662865d4249847cef340f513cc9c7c77e078df1cb95cd20665075dae1a`  
		Last Modified: Tue, 30 Dec 2025 00:50:53 GMT  
		Size: 18.6 MB (18579614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26f1f879de709c557e700ad95d89ee1be9a9f95c243b1130277a76ee980db80`  
		Last Modified: Tue, 30 Dec 2025 00:50:52 GMT  
		Size: 4.5 MB (4517708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1ec0ba7ad207b248b3ece47bd0e1e3618c2a7af47131b9fb6052df3d4535ee63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3951342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf25c7d061ee14fab7dbbcbd0cc6ac1ab14ebd3ccf12b77d1056a0bc1faa662`

```dockerfile
```

-	Layers:
	-	`sha256:eded37746922e76b58209e8c91aedb84454453121de71dca02beb36852c5f87e`  
		Last Modified: Tue, 30 Dec 2025 01:38:04 GMT  
		Size: 3.9 MB (3934990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9b6f11be361670ed583246f670d7b02c72dfb79bd606815279036a71cda0540`  
		Last Modified: Tue, 30 Dec 2025 01:38:05 GMT  
		Size: 16.4 KB (16352 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e41ae354d021d5ef61c456183c51174fe3424881b4d517240d862fc559c76a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126523587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13061732175c98fa6abec54810d91b8bdd0e833bafc92fa2946728bafca982b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:54:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:54:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:54:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:54:37 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 00:54:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 00:54:37 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:54:53 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 00:54:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 00:54:53 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 00:54:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 00:54:55 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:5785abec2864dcd8d343ccd872458a50ffb2a61739bc46a79709c68c455cb8fc`  
		Last Modified: Mon, 29 Dec 2025 22:30:57 GMT  
		Size: 49.7 MB (49650193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a66de7f356fa76988e9ebe5975965d77910619e719aa96b3f18bbc6a94abb2`  
		Last Modified: Tue, 30 Dec 2025 00:55:21 GMT  
		Size: 53.8 MB (53814992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd447c0cab4246fa1d707c9b949dae43153aae3aaf23350c093c993a7b914835`  
		Last Modified: Tue, 30 Dec 2025 00:55:15 GMT  
		Size: 18.5 MB (18540668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf146a731c15aa52587d2adeaf8ae4752bee4b920c90cfa4861e1c0ec7e3323`  
		Last Modified: Tue, 30 Dec 2025 00:55:14 GMT  
		Size: 4.5 MB (4517702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:eb702fb837f094d1b47cbc8bf584ba026d723cc92401eb15424d826e7fa0a7a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3953038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3de55d122c46ceb065fa7a0aef40bb3922c8910018eb068e943cfd33dfb41be`

```dockerfile
```

-	Layers:
	-	`sha256:fa08bfbe8dc0cbd86ee29cd64e3e41270bd4ae6b1391c1351019ca87d08905bd`  
		Last Modified: Tue, 30 Dec 2025 04:49:25 GMT  
		Size: 3.9 MB (3936565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be6bbd9af59658b2b5f9408f2676f74e0cbd7a3aab8f25ea0a94c1230abd6881`  
		Last Modified: Tue, 30 Dec 2025 04:49:26 GMT  
		Size: 16.5 KB (16473 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:8cccf68f5d73936699d9d5569e5297de97296043c1ce476b349b97d8e388c4be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128438506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b07cb0b1fc14eb42cb2c2fb95cae97589f59966727389aeba27dd82c61de1a`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 05:12:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 05:12:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 05:12:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 05:12:24 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 05:12:24 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 05:12:24 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 05:13:21 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 05:13:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 05:13:21 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 05:13:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 05:13:25 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:d586c84fb9377f9b3f4030e2c3e1e9ff7b1a23a68b8abc2c48a43163a3589257`  
		Last Modified: Tue, 30 Dec 2025 01:51:01 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712597973b595c19402df1e5710d5565c7fa6467f856fa606197ec1e7e8a4aed`  
		Last Modified: Tue, 30 Dec 2025 05:14:21 GMT  
		Size: 52.2 MB (52175123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de93bdbe3bd950012b85252bf877a46db34c13a297a45f40306ae14a0a95109`  
		Last Modified: Tue, 30 Dec 2025 05:14:11 GMT  
		Size: 18.6 MB (18637099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a384b8f4ca59973c1e60baec21bfdb231c586b186139adec7268703dd2e1bfcb`  
		Last Modified: Tue, 30 Dec 2025 05:14:10 GMT  
		Size: 4.5 MB (4517767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7aa8dd08b9509e5b24316c778129fff4699c80d450cccb8b6f77698a9b32fd7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae8348c0db15b29be26b481fd2c9ebfe84ac1fa88476e3fd72daa9d0f217810`

```dockerfile
```

-	Layers:
	-	`sha256:2e54442a1c54e7bbb630bcc24b7baf50466d24b38727c7f7e0d7e0337b4ab281`  
		Last Modified: Tue, 30 Dec 2025 07:39:49 GMT  
		Size: 3.9 MB (3936581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0259e06a460b257e8bee529389f79adb6293380ba3c6074d56bce0d9b923352d`  
		Last Modified: Tue, 30 Dec 2025 07:39:50 GMT  
		Size: 16.4 KB (16395 bytes)  
		MIME: application/vnd.in-toto+json
