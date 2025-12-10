## `clojure:temurin-21-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:ec5f10593ec4c46c87589b5438599101d84dede1fc6228ce62fbf29cff7c2b8c
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

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e5e3dc0abf56f1cb81a34cd06a145aff2feb89cfe62adebb08c201b33082a5e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208330679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243862bb8e430a3af80a31aae4bed51f6bae97cc25f6603a634c58ea6754bfbe`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:53:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:53:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:53:53 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 08 Dec 2025 23:53:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 08 Dec 2025 23:53:54 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:54:07 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 08 Dec 2025 23:54:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 08 Dec 2025 23:54:07 GMT
ENV LEIN_ROOT=1
# Mon, 08 Dec 2025 23:54:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 08 Dec 2025 23:54:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:54:09 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:54:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3815ebc0618ee88028d33be7a71ea90439dbb76a9804345571205faad9cd6b`  
		Last Modified: Mon, 08 Dec 2025 23:55:29 GMT  
		Size: 157.8 MB (157826042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25488413832f86187c7c6171855edf6623172c8f43a06d25ee3d86f5e8260d9`  
		Last Modified: Mon, 08 Dec 2025 23:54:39 GMT  
		Size: 17.8 MB (17758034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b138bafa14eda32c221bdb3dbe29223f625d2f904b3859c1087cabc8caa493e`  
		Last Modified: Mon, 08 Dec 2025 23:54:38 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa822ffbc53bd14e8317790f6694bd611a4beb9ef1a7cb715deac2ce347fc8f1`  
		Last Modified: Mon, 08 Dec 2025 23:54:37 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1cb5e9fe6f7dcd5e711facf074ef838fbf5ad02a28e4ab1ee41560850fd4d956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d1abba0d7ece6f1a8967ed825b975e70487675156f4cd7d0bd35e4b5b07045`

```dockerfile
```

-	Layers:
	-	`sha256:68241e7a953491de6973a202bd495accd95f7e9bd50688e4dec5d6290ebfb4d4`  
		Last Modified: Tue, 09 Dec 2025 04:43:08 GMT  
		Size: 2.7 MB (2731890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:691ceb365ad962819a414be285cbbb9b678f59077f72d15294a084e6ded5a268`  
		Last Modified: Tue, 09 Dec 2025 04:43:09 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2e4efd01468657d137681baa705a2cffb011e43285c5d5b72a70b52c10329567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206319132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:147676b7f6d6860a9318ec17206d81140343b5d3967c65f8f3c3d6104a6f3580`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 00:01:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 00:01:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 00:01:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:01:40 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 09 Dec 2025 00:01:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 09 Dec 2025 00:01:40 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 00:01:53 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 09 Dec 2025 00:01:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 09 Dec 2025 00:01:53 GMT
ENV LEIN_ROOT=1
# Tue, 09 Dec 2025 00:01:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 09 Dec 2025 00:01:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 00:01:55 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 00:01:55 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f062724698c6915caded43f6c1a0623f95522f041889529f3b9220ecc780cb`  
		Last Modified: Tue, 09 Dec 2025 00:02:42 GMT  
		Size: 156.1 MB (156107673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ce14bf944da3385ca8448e6f591a4929c6572c667e888e56f64384006c35cc`  
		Last Modified: Tue, 09 Dec 2025 00:02:22 GMT  
		Size: 17.6 MB (17591090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3f82c7af4a8a5d9b507389f88faa18ef622db15f96d86c7faffa8689f4c865`  
		Last Modified: Tue, 09 Dec 2025 00:02:21 GMT  
		Size: 4.5 MB (4517713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314d7465ca200d309998d3a2cf2d0078ab5813ad140c1ae471d736bc75dd14b0`  
		Last Modified: Tue, 09 Dec 2025 00:02:21 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cae4824b066d9133c496258459b7602458e7ed90436577a27754818688046553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d9b4ba083c788677c8f26ec1280614e899ffb22a790d43e808410e4d838085`

```dockerfile
```

-	Layers:
	-	`sha256:6ca00e8803c7c0f7cd3aabc639b974f9450b835640ddea15e587d32dc74691ec`  
		Last Modified: Tue, 09 Dec 2025 04:43:13 GMT  
		Size: 2.7 MB (2731505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db86c8d8fb649884504628cdd280a6861f7b24e68f963a9502f5187f64ff3ae2`  
		Last Modified: Tue, 09 Dec 2025 04:43:14 GMT  
		Size: 18.5 KB (18523 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:20dd9ecff742a2efb09be79b38d677de8cc5900d9b947af7df1e22f7c1eedfca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212489737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54ee18b0d6cfabbf59bcf919ac2995be6cd546b9d1356d2639d6b7ec6c99f419`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 16:22:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 16:22:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 16:22:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 16:22:00 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 09 Dec 2025 16:22:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 09 Dec 2025 16:22:00 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 16:22:49 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 09 Dec 2025 16:22:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 09 Dec 2025 16:22:49 GMT
ENV LEIN_ROOT=1
# Tue, 09 Dec 2025 16:22:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 09 Dec 2025 16:22:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 16:22:54 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 16:22:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:85c696326521b18996e4f030a7e27e2c57ad4956710f12ec3011da2c017e09ad`  
		Last Modified: Tue, 09 Dec 2025 09:15:52 GMT  
		Size: 32.1 MB (32068845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d170adcd864f030aabc5ba607c417b8b9efd1bdb3b13f20e801de697b8e3a11`  
		Last Modified: Tue, 09 Dec 2025 16:27:29 GMT  
		Size: 157.9 MB (157942949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e0379203d8a94f8db055259f642a8b5073b1bcfcaf5148760d881d69299c47`  
		Last Modified: Tue, 09 Dec 2025 16:23:45 GMT  
		Size: 18.0 MB (17959757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a3142fa95056ac335fa47b0a53ba5a8c7efb8de10589f6e06141efce7d2fad`  
		Last Modified: Tue, 09 Dec 2025 16:23:44 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ae82c5510fc21bca3cf7adb1a08599cd6e6221f0f523e2ae8f3c2305218f87`  
		Last Modified: Tue, 09 Dec 2025 16:23:44 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:81239a8f2487db4cf86fb5e8006618b66509bc240db664c6027cefe52ed4b09c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2752170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b445ca5b2532d6eb2f87772d84b7e9d924eb792895ad9800c9a73d050bf6bde`

```dockerfile
```

-	Layers:
	-	`sha256:f3a155bf91aff41f5948e894e502dc119ebf88ebc85650d159db7f2acece29f4`  
		Last Modified: Tue, 09 Dec 2025 19:36:41 GMT  
		Size: 2.7 MB (2733723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c727ffa1d13667da3e601c9575aa312f2e2b0acea19622adec707f26ec444d54`  
		Last Modified: Tue, 09 Dec 2025 19:36:42 GMT  
		Size: 18.4 KB (18447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:3c3e0c67f6f366e9c13e7e734c0360d2daa817c310829b2b8086fddfd5db520c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 MB (195892273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014a37a702c4a0f291402ce49dd7a68d84688d0090ce96cf0bd2054062427112`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 01:30:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 01:30:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 01:30:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:30:42 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 09 Dec 2025 01:30:42 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 09 Dec 2025 01:30:42 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 01:30:53 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 09 Dec 2025 01:30:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 09 Dec 2025 01:30:53 GMT
ENV LEIN_ROOT=1
# Tue, 09 Dec 2025 01:30:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 09 Dec 2025 01:30:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 01:30:55 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 01:30:55 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:00a29f44cb5b31bbcf043ec5426ee1c018bb26435350712cb5e48d56c6d95792`  
		Last Modified: Mon, 08 Dec 2025 22:15:04 GMT  
		Size: 26.9 MB (26884429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89aa0de067223d3ecb4c513f6bcf0d76802a026b7899386bbea2d37a24c9a5ba`  
		Last Modified: Tue, 09 Dec 2025 01:31:22 GMT  
		Size: 147.1 MB (147069831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7d83e10a269f9bd5fe29e1e37695169208ea29473acb8a56b87a2c01b2433d`  
		Last Modified: Tue, 09 Dec 2025 01:31:31 GMT  
		Size: 17.4 MB (17419839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0549efec880639a9b3cef7690625cf68534e43c9750dd9381070b97935ed257c`  
		Last Modified: Tue, 09 Dec 2025 01:31:26 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533ec3ddf79c87d0ae7327b7b2755f5bdc171a2974ef31f978bc1093336d90c7`  
		Last Modified: Tue, 09 Dec 2025 01:31:26 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ba7eda503d054f881210e7532aa74ce81095020857efadefb4591a4f6bb0bfc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2742107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bfd10093eb85d3a0206a2c87c560cc7013cc317c3e3964302d579485026a2b4`

```dockerfile
```

-	Layers:
	-	`sha256:f525aefa4361147da2c0ebf4cf2e29e460cc95726019c2c4efc6fe963664310b`  
		Last Modified: Tue, 09 Dec 2025 04:43:21 GMT  
		Size: 2.7 MB (2723704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:846ed979a40091146f0b1b275c0793e4a86eb0dcd0d7cdc6c9d6ee98ee96ac3c`  
		Last Modified: Tue, 09 Dec 2025 04:43:22 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json
