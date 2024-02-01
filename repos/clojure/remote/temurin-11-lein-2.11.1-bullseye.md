## `clojure:temurin-11-lein-2.11.1-bullseye`

```console
$ docker pull clojure@sha256:fda570829a676d7916b024bd7966a0ed60988b18a42863605bc35d999165f544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-lein-2.11.1-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:70c3728fbe31de832f8d17015f39a54b9b62fcfcd8a688ff7e7bafe5a4110764
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221080473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2382cc6ff93b15ad35a02adaed9f72d98e2883042a9ab276264df2dfc387c3b2`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:29 GMT
ADD file:4fa73c8d113df02c8656b74ab87563432215332f3de78446a02e5ab7d6e2ab7a in / 
# Wed, 31 Jan 2024 22:35:29 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 23:49:39 GMT
COPY dir:e1ce96bca1c423a1c79b84eacb7ae69429353a37485cc24af4161ce4b9d3ee2a in /opt/java/openjdk 
# Wed, 31 Jan 2024 23:49:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:51:39 GMT
ENV LEIN_VERSION=2.11.1
# Wed, 31 Jan 2024 23:51:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 31 Jan 2024 23:51:39 GMT
WORKDIR /tmp
# Wed, 31 Jan 2024 23:51:54 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "03b3fbf7e6fac262f88f843a87b712a2b37f39cffc4f4f384436a30d8b01d6e4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 31 Jan 2024 23:51:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 31 Jan 2024 23:51:54 GMT
ENV LEIN_ROOT=1
# Wed, 31 Jan 2024 23:51:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 31 Jan 2024 23:51:56 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:7faaa42ac0c18c9baf539c97a5c8f042d02a77b05380cb57759e4407385710dc`  
		Last Modified: Wed, 31 Jan 2024 22:40:15 GMT  
		Size: 55.1 MB (55056963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea23dca2c18f20e36988429ad3fd4728d0ec88cdfe95ee9e1b671039deae17d`  
		Last Modified: Thu, 01 Feb 2024 00:09:13 GMT  
		Size: 145.3 MB (145270965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80d2744350206e394032aaa850dfc594a424de20102ef91e9a7622bd9cf38cc`  
		Last Modified: Thu, 01 Feb 2024 00:10:08 GMT  
		Size: 16.4 MB (16353357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd98fe7fa1651207b07b212ebe8b4846921d69a07dc14ccedb0be28c1f80fe0`  
		Last Modified: Thu, 01 Feb 2024 00:10:08 GMT  
		Size: 4.4 MB (4399188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-lein-2.11.1-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ccea9a8b2979244705cf48e6c05622c1907eeab9b7352d6f03ba312874e984dd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216455922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:268b3d74f5aa915acb12a0156df300f5136218d2648c0e8e3c7285d6df9867be`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:33 GMT
ADD file:81cb49e646b9feb1ddeddea1cb6dbafa672a250f1553cc28eae09c955607236d in / 
# Wed, 31 Jan 2024 22:44:34 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:20:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 06:25:37 GMT
COPY dir:454699b64b949edd3264b234e72a891ace37d538f2726c5ec754e17e6fb3fb19 in /opt/java/openjdk 
# Thu, 01 Feb 2024 06:25:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:27:26 GMT
ENV LEIN_VERSION=2.11.1
# Thu, 01 Feb 2024 06:27:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 01 Feb 2024 06:27:26 GMT
WORKDIR /tmp
# Thu, 01 Feb 2024 06:27:40 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "03b3fbf7e6fac262f88f843a87b712a2b37f39cffc4f4f384436a30d8b01d6e4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 01 Feb 2024 06:27:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 01 Feb 2024 06:27:40 GMT
ENV LEIN_ROOT=1
# Thu, 01 Feb 2024 06:27:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 01 Feb 2024 06:27:42 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:4b6eb2d0256d18652f84fd30c1db34ce9462e535a2d96fbf2f9044db000b13f5`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 53.7 MB (53708267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5334aa60b617c8815917a660a8e4e1c07740fd9e60bb51686fab553101763ca9`  
		Last Modified: Thu, 01 Feb 2024 06:42:54 GMT  
		Size: 142.0 MB (142006500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e97c8407ce49e5213eb298d2cbcd6ae3906e2bc12d3fa4839360100ae9816d9`  
		Last Modified: Thu, 01 Feb 2024 06:43:41 GMT  
		Size: 16.3 MB (16341945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0fb1f2b6566ae0e984043d65b57249d9ef9c2e3c8001b87a1008fc79ee4d4c`  
		Last Modified: Thu, 01 Feb 2024 06:43:40 GMT  
		Size: 4.4 MB (4399210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
