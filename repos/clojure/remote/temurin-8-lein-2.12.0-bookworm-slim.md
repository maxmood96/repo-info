## `clojure:temurin-8-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:90ab1b72832e2b90d1a967384aa1ffb554e03a32707768cf37b050c1ef4c28de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f0df1a8fef19561bb33d0a1f7a0647c023bd61d2fdb5ca19fb5166e89d23b58f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 MB (105683754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104667906732a6b0f8eaee9495d637145ba21d7dd90488e500eb27980a911656`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:00:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:00:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:00:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:00:26 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:00:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:00:26 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:00:41 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:00:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:00:41 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:00:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:00:42 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6f43718b58f17e5db8204af0b9a651c9cf2fc3901c66adef851e6fce68ac23`  
		Last Modified: Wed, 15 Apr 2026 22:00:56 GMT  
		Size: 55.2 MB (55170069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131ffa8d8efe2a7e19ead7a7f14147a4fd251bdd70b679da7e8ee23ec87e7d99`  
		Last Modified: Wed, 15 Apr 2026 22:00:55 GMT  
		Size: 17.8 MB (17759611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcc6eb8142292505bcd8c1dbb08fd2df7ed4c3a4065d6aa1303393a9a5637db`  
		Last Modified: Wed, 15 Apr 2026 22:00:53 GMT  
		Size: 4.5 MB (4517710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a41c51ee4b9cc862d1d9a682c6acc50e9657435866140f429ce770498057481d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2867439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83bbf39b954a66b8ca15a80840330cb1b8f46b4882222f1cf36cba0e64458a8`

```dockerfile
```

-	Layers:
	-	`sha256:4724672476f8f70077c7f5aae1f4b88eeb71d84c7c0f20d59902943bd40f08aa`  
		Last Modified: Wed, 15 Apr 2026 22:00:54 GMT  
		Size: 2.9 MB (2851039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa84a99d0e1d2a2c2e40907782658cfea92ce8aa381c2bad88822ff5c2196dee`  
		Last Modified: Wed, 15 Apr 2026 22:00:54 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8ae6602143d287c26e84495367a7637e50d867bf2f015298fd008983c4c19b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104478606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229e89d1d13385b218eefcbd342067cdcb7d0d03f923e1557b7e96c0f7c6ba73`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:12:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:12:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:12:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:12:06 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:12:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:12:06 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:12:20 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:12:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:12:20 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:12:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:12:22 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45aba1fedc2627497a5e3ee01d69181a5226afadea238f6c42d5d10aebc2830e`  
		Last Modified: Wed, 15 Apr 2026 22:12:36 GMT  
		Size: 54.3 MB (54251613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea01582a9c3311791d00eee0f494a541e8ab30570e5a87b0c556e5479a9ffdf`  
		Last Modified: Wed, 15 Apr 2026 22:12:35 GMT  
		Size: 17.6 MB (17593058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183300ae526d3f796ddd6fe1abd4cf747a664f46b75f21e5961d3155f69965ea`  
		Last Modified: Wed, 15 Apr 2026 22:12:34 GMT  
		Size: 4.5 MB (4517737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1ae242806cb3ebc05c7a9a8f14dc533968dd1530ffc333507d0c4f41e1842fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2867875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:533ce1cb406216fb4397204459046b76a1d8474bdf9b6e571b93299b5aa73125`

```dockerfile
```

-	Layers:
	-	`sha256:937cb792b4e2fd2709f61a7d51f85cf594ae43ec3f92d2e3a4d360632da1c6a1`  
		Last Modified: Wed, 15 Apr 2026 22:12:34 GMT  
		Size: 2.9 MB (2851354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dcbd1189d6e046eb49589c48f352a17ff7ac2fc5b08a9138e6663c25cee29c6`  
		Last Modified: Wed, 15 Apr 2026 22:12:34 GMT  
		Size: 16.5 KB (16521 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:725148cda1acf6ed7ffd4f237957e1813eb0af206631ad30de39d0701eb4331a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107207760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a713c0d0a6c3ac2f798e46d770107f4ecfac5abd68813e24f896e4f67df1900`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 14:21:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:21:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:21:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:21:25 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 14:21:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 14:21:26 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:22:01 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 14:22:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 14:22:01 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 14:22:07 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 14:22:07 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b1c56220ca211bc9d02f1ed5c589465809676b6ab2cef705f1e2fb8e9726de76`  
		Last Modified: Tue, 07 Apr 2026 00:09:42 GMT  
		Size: 32.1 MB (32078464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef0ca85ab92bd3ffb3fe25036c18fe06d6d124a5859fb5b8e910ab095f07e02`  
		Last Modified: Tue, 07 Apr 2026 14:22:42 GMT  
		Size: 52.7 MB (52650390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc50d14036b69ed3bcc7f29ba454958a96314e6e64f7a72ba4892a3d8299229`  
		Last Modified: Tue, 07 Apr 2026 14:22:41 GMT  
		Size: 18.0 MB (17961108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:793ef4d05d4d636b3f93902f20ed942365c0f1ad00bf755974a9714520cd0552`  
		Last Modified: Tue, 07 Apr 2026 14:22:40 GMT  
		Size: 4.5 MB (4517766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a02247dcc7704885168cbecc04bef8fd315076dc8ebe210a71792c5030454f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2869911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dfeba393d94f9b6794453735254271075f128a801c555cdd13c7da280fe1f74`

```dockerfile
```

-	Layers:
	-	`sha256:826c7484a251193eae9a8d18f8146282d0752f6ec53d9cc0143f57e1331bd082`  
		Last Modified: Tue, 07 Apr 2026 14:22:40 GMT  
		Size: 2.9 MB (2853467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9726fbc794cfb1012f0252a45095ab93634b8f9f2579bac813ddf75eb40850a0`  
		Last Modified: Tue, 07 Apr 2026 14:22:40 GMT  
		Size: 16.4 KB (16444 bytes)  
		MIME: application/vnd.in-toto+json
