## `clojure:temurin-8-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:32fca99247d422114e5656f61da15319e8650ada639431e4754ca2bfcd5879c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e7acddd2f21f5e35b00125eac6c2f533045c7f73493e9a615f1167411204e01e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105237656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a068535e56d3a3fab48ea87d47e5297d55c28ade104f5f5f117b822b6a6da6d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:50:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:50:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:50:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:50:04 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 00:50:04 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 00:50:04 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:50:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 00:50:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 00:50:18 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 00:50:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 00:50:20 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c22a42c356cdf8489016df7ba7f2c456806879c87c013ce33289ecec26648d`  
		Last Modified: Tue, 30 Dec 2025 00:50:44 GMT  
		Size: 54.7 MB (54733371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3681a3a2d905f5200c44526f9fe8256bc6f5997d757a7f542eadbbcba5aee8da`  
		Last Modified: Tue, 30 Dec 2025 00:50:45 GMT  
		Size: 17.8 MB (17758087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c07f341343ffbc97a1826c5b98f9d7e33b7cec24cd2b4c9f9e96c48ff15fb8`  
		Last Modified: Tue, 30 Dec 2025 00:50:40 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b9d4e31c3d5fda872790dd1518ec44a3281377ff6158a1396e406419b22619c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c810edf17898d2680a40d722e7f44956c657ffd2d05c9312c08e33521911ffe6`

```dockerfile
```

-	Layers:
	-	`sha256:54161f78d231cdfbc9ad62a55e61097af699341d0209785884eb1b024426698c`  
		Last Modified: Tue, 30 Dec 2025 04:48:58 GMT  
		Size: 2.9 MB (2850398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c61371f3b29e7451bde7d6b93e43486228c85f1d51efa64041224b41210c3ea3`  
		Last Modified: Tue, 30 Dec 2025 04:48:59 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e7f7dc3a26dd11bc40de5eb088a47c5d125930499aac1a3846c44e0bbda18399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.0 MB (104026089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a667a5180d3bc7a848fc5ca77739511c7923df12ccffc233fd71705503e631`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:53:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:53:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:53:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:53:24 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 00:53:24 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 00:53:25 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:53:38 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 00:53:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 00:53:38 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 00:53:40 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 00:53:40 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06b6161f1a8fcd0539f34d05c4fbadd1e270cf47feef766ef80c58d7299c0dab`  
		Last Modified: Tue, 30 Dec 2025 00:54:05 GMT  
		Size: 53.8 MB (53814997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee132af2773ccb74bfba08946e255d31a595d0c477060d6f1d692e7a5a81289`  
		Last Modified: Tue, 30 Dec 2025 00:54:01 GMT  
		Size: 17.6 MB (17591103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b46e2743e09a3662d0d1e91601ae4ebbac2e63490396f91f7d46d3aca1364ca`  
		Last Modified: Tue, 30 Dec 2025 00:54:00 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ebb91eec6f14bd8fcb14235642f782f030bf6e67a1b0d6a05b601eb47779baa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2867232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57733c1e66f6fae5e27adace274847a9600743edee62b56f1a525573f07d684`

```dockerfile
```

-	Layers:
	-	`sha256:8f7e1e19a2c09a32106e583de62369e5ec8f0d8746bbaa306485fdcba66f81c9`  
		Last Modified: Tue, 30 Dec 2025 04:49:03 GMT  
		Size: 2.9 MB (2850711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e20b1a148fb705e5575fe77858a97c11712c23d09e9fa294d7197be2eb9a369d`  
		Last Modified: Tue, 30 Dec 2025 04:49:03 GMT  
		Size: 16.5 KB (16521 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:a06b3e26869448b2ffcd1040f99515069c200ae1e05a3699903e7319e0347f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106721368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:452a2ed3db353354cfae5b116302f85b02e2ceb1876341061c6962a5544dd134`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 05:10:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 05:10:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 05:10:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 05:10:59 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 05:10:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 05:10:59 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 05:11:32 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 05:11:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 05:11:32 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 05:11:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 05:11:36 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b7648f01f6858fc79caf032b4b9ed2f7e43e57f4621dc8cb36e84eb86399065b`  
		Last Modified: Tue, 30 Dec 2025 01:48:36 GMT  
		Size: 32.1 MB (32068844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294a0af0a5f1d7909ae6111a947cb6482d2e009c862439fa97b16a3ed543effa`  
		Last Modified: Tue, 30 Dec 2025 05:12:19 GMT  
		Size: 52.2 MB (52175137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:845c41a49c6d736e8a6ea2e1b21f6114251a0d50759b7c9e10ea356dda63a0f3`  
		Last Modified: Tue, 30 Dec 2025 05:12:11 GMT  
		Size: 18.0 MB (17959592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb83160f6c884b501dd41e5871ce01029d46e1e057bc57f694aa18b3015b11e`  
		Last Modified: Tue, 30 Dec 2025 05:12:10 GMT  
		Size: 4.5 MB (4517763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dc0698784bd3050fc838584b9930cb872a1c743e4e85679a1a523eb6c9ad1948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2869268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb9f3d27e92e197a325fa35558a3baf9589ac1cee154ecb9657c8ccdb216dc3`

```dockerfile
```

-	Layers:
	-	`sha256:5e5576a49d177783e0d9a6c72e50910d219d7c1ae62f864fb3242d594abc0933`  
		Last Modified: Tue, 30 Dec 2025 07:39:42 GMT  
		Size: 2.9 MB (2852824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:293db6da3b015db4e21a294a539a8915862d1b66ad1a90c4932149df5b9a0b8f`  
		Last Modified: Tue, 30 Dec 2025 07:39:43 GMT  
		Size: 16.4 KB (16444 bytes)  
		MIME: application/vnd.in-toto+json
