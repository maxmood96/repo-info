## `clojure:temurin-21-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:982fd2370e6ceffe0195ad92f67557eeacb4df167340075ca28cce9b64d42087
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:967b1f98353bf324b7f261e93d7f7f29d8a05cb1c0042187cc7767cbe1c11d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.9 MB (207899147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1be6f43c05752b75b4a32f6596fb7bc8f1d463b37179d9fdf085a93dd39e09f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:456a3213e1b1f193dc759cd05f6f8422428b8c4bd45ef40fbf41ba43bdce8570`  
		Last Modified: Mon, 08 Sep 2025 21:12:48 GMT  
		Size: 30.3 MB (30256068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7ac8b4da8383b23a5d3381bd6ac605f89a8bc5771da29f9deb41541953b599`  
		Last Modified: Sat, 13 Sep 2025 00:03:45 GMT  
		Size: 157.8 MB (157804765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2b0ec06de28b308b45c43eaa407132f4640cdbfe72a9f9c99ca7caee389f44`  
		Last Modified: Sat, 13 Sep 2025 00:03:55 GMT  
		Size: 15.3 MB (15320185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a84118835971c72ce349ad08c92dd61c1679256b21f2baf195c8fd5642654ef`  
		Last Modified: Sat, 13 Sep 2025 00:03:54 GMT  
		Size: 4.5 MB (4517699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2237c045ec56bcc1444674e416f463ba73507800ddf07d228a9cf4edbb18907`  
		Last Modified: Sat, 13 Sep 2025 00:03:54 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d8c17511ba84e13d447e679d3d86f79506cba6797b524e0e90187f432e95b9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3040780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca60f877ea328ae8c585fa6a8e7f011fb0c29218611e9aea98a56274b864514`

```dockerfile
```

-	Layers:
	-	`sha256:b0f4efc9426f35e87de1036a150c9bab5e287573ae6a7dfc70ac6a6e22782503`  
		Last Modified: Sat, 13 Sep 2025 00:35:06 GMT  
		Size: 3.0 MB (3021672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e62acfb37067cf4b16342f99eb69dedb2c854b92c95d794d42ab650d2c9c630`  
		Last Modified: Sat, 13 Sep 2025 00:35:07 GMT  
		Size: 19.1 KB (19108 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:85f24c10d16f7adb72f75dd99f94db9e1d0b9879bfba982b484f7dbdc9f436a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232916490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f40f34095334c5e606acd4d8a067dbebb33ddb66eb941794f06f858f49696a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Fri, 12 Sep 2025 17:48:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 17:48:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 17:48:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 17:48:33 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 17:48:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 17:48:33 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 17:48:33 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 17:48:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 17:48:33 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 17:48:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 17:48:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 17:48:33 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 17:48:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8568e9af3ab25a29d98aac9a07896467a19253e72e5be0cf09cd3982ac4444d0`  
		Last Modified: Mon, 08 Sep 2025 21:15:52 GMT  
		Size: 28.8 MB (28750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e1b611343fd7687edcc090479785e60a32c0e60e2df9ee681a3fee8e4bd8fe`  
		Last Modified: Fri, 12 Sep 2025 23:43:50 GMT  
		Size: 156.1 MB (156081189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad75bcd20ac7ab50379800e8bc8e8cb88e6bb2040f8279abc997a23e6663923`  
		Last Modified: Fri, 12 Sep 2025 23:43:57 GMT  
		Size: 43.6 MB (43570250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1543afc1f218708d1b72f4a907b1cbf58624a9355aa72bee0b17069d96b8275a`  
		Last Modified: Fri, 12 Sep 2025 23:43:54 GMT  
		Size: 4.5 MB (4514166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935858cef1e02e1e9fbdfd1612280d71308d7bf8c811c10452c4994b857c8a6c`  
		Last Modified: Fri, 12 Sep 2025 23:43:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c67ba35f65f804f67d248484aff3add654e5051e9ee5bfa5b34a3c56af5482d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4758874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ae5ce25f505cecdb383e01b2ed905a7a92ee9775029e4a34dfc9473f8ac405`

```dockerfile
```

-	Layers:
	-	`sha256:d4d5e5284dde05f033ac61f0708efdc807b07c08e17ba571cffd642d65c035cf`  
		Last Modified: Sat, 13 Sep 2025 00:35:11 GMT  
		Size: 4.7 MB (4739609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b60726d6b3115f9c4c77efc52f81f61ff321698e01df28789dd495c215c547c8`  
		Last Modified: Sat, 13 Sep 2025 00:35:11 GMT  
		Size: 19.3 KB (19265 bytes)  
		MIME: application/vnd.in-toto+json
