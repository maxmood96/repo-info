## `clojure:temurin-21-lein-bookworm`

```console
$ docker pull clojure@sha256:c3607439b9aed641b598b236df59ae12bbdd110f6444451fe7fa399158400548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-21-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:6d0acafa0889314f7c7eada627448f029862be43de8cd63d123811e2b1471d0e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233083430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2efda003c0bca9f71f9fabc5974ec7116d5b7e1c46b050ef952eb8a024f8ddda`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:05 GMT
ADD file:6d9e71f0d3afb0b288cf2c06425795d528a142872692072ab1cd1ad275b67d1f in / 
# Wed, 31 Jan 2024 22:35:06 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:41:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 23:41:29 GMT
COPY dir:64a8841762a9afbd2fb8b4cf497b2dee87765737d44ff0387ce1cfc51371c9a2 in /opt/java/openjdk 
# Wed, 31 Jan 2024 23:41:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:41:31 GMT
ENV LEIN_VERSION=2.11.1
# Wed, 31 Jan 2024 23:41:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 31 Jan 2024 23:41:31 GMT
WORKDIR /tmp
# Wed, 31 Jan 2024 23:41:48 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "03b3fbf7e6fac262f88f843a87b712a2b37f39cffc4f4f384436a30d8b01d6e4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 31 Jan 2024 23:41:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 31 Jan 2024 23:41:48 GMT
ENV LEIN_ROOT=1
# Wed, 31 Jan 2024 23:41:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 31 Jan 2024 23:59:40 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 31 Jan 2024 23:59:40 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 31 Jan 2024 23:59:40 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6a299ae9cfd996c1149a699d36cdaa76fa332c8e9d66d6678fa9a231d9ead04c`  
		Last Modified: Wed, 31 Jan 2024 22:39:27 GMT  
		Size: 49.6 MB (49583754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c299f193861b5d2b1adc713471ff68491754a53d8441f8b4078311e342849d`  
		Last Modified: Thu, 01 Feb 2024 00:04:55 GMT  
		Size: 159.6 MB (159582922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8930c89778f32bc9786d72d28fe8401a5cff1184bec0747a00df510744ea1e0b`  
		Last Modified: Thu, 01 Feb 2024 00:04:25 GMT  
		Size: 19.5 MB (19517131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3126dc6615218f7f1a58df2978e35a3206115d8b9a471be5e76650e7973ed8e7`  
		Last Modified: Thu, 01 Feb 2024 00:04:24 GMT  
		Size: 4.4 MB (4399223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38bf355b95305f2d6a59c526ae2aafb1c6ea7362c24e7d69f95dffdb8621d9b8`  
		Last Modified: Thu, 01 Feb 2024 00:15:28 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-21-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fe8e3716be2dddacab3faa554c71cf9b337057144e0dc33c0d608a06b2b690a2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231137435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a2bc03dd1ff08ae4916a3e0091745c0632b147752692d8c4491f03a99d6850e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:15 GMT
ADD file:8bc7f537dd3dc4b92ec9006080fd563cc79205ee1ec3f456d03e869125a5bc21 in / 
# Wed, 31 Jan 2024 22:44:15 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:18:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 06:18:22 GMT
COPY dir:ab40534e435f9942975c0e8b5454d6b7a8d69c445f8e0758c1bd9c500e157fca in /opt/java/openjdk 
# Thu, 01 Feb 2024 06:18:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:18:26 GMT
ENV LEIN_VERSION=2.11.1
# Thu, 01 Feb 2024 06:18:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 01 Feb 2024 06:18:26 GMT
WORKDIR /tmp
# Thu, 01 Feb 2024 06:18:42 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "03b3fbf7e6fac262f88f843a87b712a2b37f39cffc4f4f384436a30d8b01d6e4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 01 Feb 2024 06:18:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 01 Feb 2024 06:18:42 GMT
ENV LEIN_ROOT=1
# Thu, 01 Feb 2024 06:18:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 01 Feb 2024 06:34:32 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Thu, 01 Feb 2024 06:34:32 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Feb 2024 06:34:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:66932e2b787d33a94ee3eb8b489be6e6838b29f5c1d732262da306da9b1f2eed`  
		Last Modified: Wed, 31 Jan 2024 22:47:40 GMT  
		Size: 49.6 MB (49615296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f111917e60b82ad9b0f922efe4aa47bf72c7fa9d4456fcc76e7bdcf523cda38`  
		Last Modified: Thu, 01 Feb 2024 06:38:45 GMT  
		Size: 157.8 MB (157784591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883f94a05f3b057d3a5b6a28cda2cd84b4d520a607d3ee2ec0ebfff062c8f3ba`  
		Last Modified: Thu, 01 Feb 2024 06:38:34 GMT  
		Size: 19.3 MB (19337939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26fdb1ddf872b705416b91471f1f489a48d92d802c337cfb527d62a440cfee4a`  
		Last Modified: Thu, 01 Feb 2024 06:38:33 GMT  
		Size: 4.4 MB (4399212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d9f40e69a9b23e9883e1bf7a739d9ee20901579e4fe05fddbd66b6e699119f1`  
		Last Modified: Thu, 01 Feb 2024 06:48:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
