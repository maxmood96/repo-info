## `clojure:temurin-8-lein-trixie`

```console
$ docker pull clojure@sha256:8312984d44409d1e2a06df0cea2a1a7ac11fccee9e59e277dc892f08b2be708c
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
$ docker pull clojure@sha256:4fbf38f2cd59430a0cbf626496e6159083dc4f3bca75e51d46081ee51f2b8284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.0 MB (175010003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e404c37931fd4d3dd67612126aabb5e94aacf3482cb27096c895a2304bcd56a1`
-	Default Command: `["lein","repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b72fed6e2775feec9291a4bd4b416f996dfc503eda11eaa00def55711302b4ce`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 49.3 MB (49263877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8071acca33ed54aaf47491fbed510ceb02c693347ebaade20187e2d8698c6768`  
		Last Modified: Tue, 01 Jul 2025 02:37:38 GMT  
		Size: 54.7 MB (54716181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cff6cab9c2bdb62f145c64c05b9585438eb9da64ce9c3278b56087a7b608c5`  
		Last Modified: Tue, 01 Jul 2025 02:37:23 GMT  
		Size: 66.5 MB (66515746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7295b73e16d41971c93da23fe5af5ac82de8ea2266e11c65ec5039a5f1e92eca`  
		Last Modified: Tue, 01 Jul 2025 02:37:19 GMT  
		Size: 4.5 MB (4514167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b1d34ec8d6e566315e3cd51e3fc50bb3fcc72623fc03b378dd3d93baeae668a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6585921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca73000daf109f9a6651373c9b152a206068684bb8b839d52e81f257d3a75187`

```dockerfile
```

-	Layers:
	-	`sha256:e548e3a2a6d9a47099c2ff48c5532ccce41173df530bdaa8b1d4439a089bd95d`  
		Last Modified: Tue, 01 Jul 2025 06:42:50 GMT  
		Size: 6.6 MB (6569519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edea0b4765e24dfc79f60c6e4ead13824e62487189a723957dfb523c23ca257a`  
		Last Modified: Tue, 01 Jul 2025 06:42:50 GMT  
		Size: 16.4 KB (16402 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a038d5577bd217988795488a4029851e69480c96f345cdfc2d3232f7f696a23c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174450967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00b6ce2a0c8b6b228fef71574e606c3aba13e751665168558675902fe642ae71`
-	Default Command: `["lein","repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:546a427a0109bbde3a869c6a4ff1ed90ec74768e7fd82dd00441608d83416632`  
		Last Modified: Tue, 10 Jun 2025 22:52:49 GMT  
		Size: 49.6 MB (49621528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e948c49136968a1b57aa01ee8a86e87fbd22e38d9f9f9e7742582a1e17d4598`  
		Last Modified: Fri, 13 Jun 2025 17:46:01 GMT  
		Size: 53.8 MB (53830497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7ad06550611aab3cfbf276bd1a9422dc3fb1265227b00d8d9a1d2d9a7716f5`  
		Last Modified: Fri, 13 Jun 2025 18:04:27 GMT  
		Size: 66.5 MB (66484739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e44bf079bed4275c63f5fdaedd8d1788e0d91e9c08345f8bdd98811bc6fe7e3`  
		Last Modified: Wed, 11 Jun 2025 08:18:17 GMT  
		Size: 4.5 MB (4514171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5bcdfc9740311adefe509b9ce7d0ba5db54b1d48fe6a6828fddbd41a4a8676da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6593700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d07587d7511ff40290cebf85bbd9c2b7e896d4875342754c1dc1694e58192819`

```dockerfile
```

-	Layers:
	-	`sha256:78f48c1887f9b2495e1399750c067cdfe7f9251db5978013bf75402c6211ac87`  
		Last Modified: Wed, 11 Jun 2025 09:43:24 GMT  
		Size: 6.6 MB (6577176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57e049ad78592c41df5a3667dbafb33bda110696a97befb74898dd3cdc75711c`  
		Last Modified: Wed, 11 Jun 2025 09:43:25 GMT  
		Size: 16.5 KB (16524 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:3e11c08e7ce8fef349ecd6b2e8715d2031a8cb2a5492a5b5f138e546719876ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.3 MB (181300672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8901b83a8c0bb88f6d06602a2bc0465238c421d9ba76f5543dc3c2786b508f`
-	Default Command: `["lein","repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:5c6a246a80c20351fe842a314b6b3f8561a5ceaea736decf36fe380b29e53224`  
		Last Modified: Tue, 01 Jul 2025 01:18:57 GMT  
		Size: 53.1 MB (53097236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c704c5e7bf6faeb686430ea5965b30fe5f7b7db2f17dfb3e5c0cac06e198c96`  
		Last Modified: Tue, 01 Jul 2025 08:18:28 GMT  
		Size: 52.2 MB (52167961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a40dafdea7aa295276aeb052286a4db34ab46d39812e00bfbf70a6a44e7acf8`  
		Last Modified: Tue, 01 Jul 2025 08:18:25 GMT  
		Size: 71.5 MB (71521229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ceaaa15866a2e41912812d19b73626738bf6a8e55e6c0ca35993145338ce75`  
		Last Modified: Tue, 01 Jul 2025 08:18:17 GMT  
		Size: 4.5 MB (4514214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3afeee6b43a1436414b07e9d2f2ede6b2b8889928f438cb021cc130192ddfbba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6590667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e491fb80fa1242e45e25f202c2feab2adeab9570a36d084f8161219650ea899c`

```dockerfile
```

-	Layers:
	-	`sha256:5bcbfd7eeb82d027736327d8c54b7c41028270e1f8e3e5d803292c4eb068c07e`  
		Last Modified: Tue, 01 Jul 2025 09:42:24 GMT  
		Size: 6.6 MB (6574220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31d66f7407162df3c156037adda7d9ec60c61d4449dc2494ba48f15ba6aa3d5a`  
		Last Modified: Tue, 01 Jul 2025 09:42:24 GMT  
		Size: 16.4 KB (16447 bytes)  
		MIME: application/vnd.in-toto+json
