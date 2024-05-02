## `clojure:temurin-11-lein-bookworm`

```console
$ docker pull clojure@sha256:2f8f94d5744657a63eea4ce0f9dc39ad7d26f941e0baab3102412898f449a19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:f154c77827f01bb26b511744cf5414af58577db25d0f9f733c4f7b5781fa3452
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.0 MB (218997371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:779fdb5c877b7bc9d34d823ab856e8ab41dc195df3ff9513f9e143c09f7cd61e`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:27:57 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Wed, 24 Apr 2024 03:27:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:04:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 May 2024 05:31:25 GMT
COPY dir:cf3bf634873a2f76d010dec9a72ea70ddc69381f0d8d3cb32fb43e16f4a2fabd in /opt/java/openjdk 
# Thu, 02 May 2024 05:31:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 05:31:26 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 02 May 2024 05:31:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 02 May 2024 05:31:26 GMT
WORKDIR /tmp
# Thu, 02 May 2024 05:31:47 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 02 May 2024 05:31:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 02 May 2024 05:31:47 GMT
ENV LEIN_ROOT=1
# Thu, 02 May 2024 05:31:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj
# Thu, 02 May 2024 05:31:49 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:1468e7ff95fcb865fbc4dee7094f8b99c4dcddd6eb2180cf044c7396baf6fc2f`  
		Last Modified: Wed, 24 Apr 2024 03:32:18 GMT  
		Size: 49.6 MB (49576283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae37ff616878154fce154f90ab1fc991e07a5f0fc272f49bcf57d8012db8e2b8`  
		Last Modified: Thu, 02 May 2024 05:46:28 GMT  
		Size: 145.5 MB (145504611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dcf43f48325bafa1e2fcc0881f3a21ddce298c54e082fda50aa5762e45f512f`  
		Last Modified: Thu, 02 May 2024 05:46:19 GMT  
		Size: 19.5 MB (19518349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2ac610fbd525d9121cdc37bac6361e6cf0776d195561c7bc00128a76bb2bed`  
		Last Modified: Thu, 02 May 2024 05:46:18 GMT  
		Size: 4.4 MB (4398128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fe9ca45477685695359ff1154c722214ba921b2d12997dd637a4473232ae097e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.7 MB (215655605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdaf991fa8eddc96e0c1534b3b1fef4fbefe262fc8f3e8a5cc7753945c63684f`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:42:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 May 2024 05:29:50 GMT
COPY dir:c867ad1ba9e7953ae7814a5cf0e0df40f8d206a8555f8375af9a181bfc9862b9 in /opt/java/openjdk 
# Thu, 02 May 2024 05:29:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 05:29:54 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 02 May 2024 05:29:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 02 May 2024 05:29:54 GMT
WORKDIR /tmp
# Thu, 02 May 2024 05:30:12 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 02 May 2024 05:30:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 02 May 2024 05:30:12 GMT
ENV LEIN_ROOT=1
# Thu, 02 May 2024 05:30:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj
# Thu, 02 May 2024 05:30:14 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89044dd89497a6d942edc38935a360a6f2e95d114a8247361685abb53e94aee`  
		Last Modified: Thu, 02 May 2024 05:42:10 GMT  
		Size: 142.3 MB (142304377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e555488f12e9fc9c21d64d9ffb9b0d8523391aca52ac45d0b5165973cd7c7b4`  
		Last Modified: Thu, 02 May 2024 05:42:03 GMT  
		Size: 19.3 MB (19339743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91a76311b4f1b371490238da3a0ba05cf1ca259ffd32d924835ccf0fd3005a2`  
		Last Modified: Thu, 02 May 2024 05:42:02 GMT  
		Size: 4.4 MB (4398144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
