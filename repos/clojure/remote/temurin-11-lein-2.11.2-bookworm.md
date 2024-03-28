## `clojure:temurin-11-lein-2.11.2-bookworm`

```console
$ docker pull clojure@sha256:77b90f99af505f9ae41d24c774f9a7681993e015001f7c9132dedb83a2e37964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-lein-2.11.2-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:ef9a1b14696c374b6ab0ce33d75335fe8693c8dd3dbb87f181a4f58cc085b27c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 MB (218738566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47083ca2a898c2f6c86de87578b6f13e0c6bf8699351faee137cd8953fdbaaa3`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 12 Mar 2024 01:20:46 GMT
ADD file:b18b4c32dd8042f45097997c732dc29b3917fd7d5f337f9e772eee5875fbe6f1 in / 
# Tue, 12 Mar 2024 01:20:46 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:10:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 02:58:02 GMT
COPY dir:4cef005a87cd4606dd69ccb04c755a46f4aa2c925fb1aacc59928d64687208f2 in /opt/java/openjdk 
# Thu, 28 Mar 2024 02:58:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 03:01:35 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 28 Mar 2024 03:01:35 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 03:01:36 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 03:01:52 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 28 Mar 2024 03:01:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 03:01:52 GMT
ENV LEIN_ROOT=1
# Thu, 28 Mar 2024 03:01:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 28 Mar 2024 03:01:55 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:71215d55680cf0ab2dcc0e1dd65ed76414e3fb0c294249b5b9319a8fa7c398e4`  
		Last Modified: Tue, 12 Mar 2024 01:25:15 GMT  
		Size: 49.6 MB (49552196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a875645a27e3ccc8bfba72105d6bf6ac46ec1c8cbe99056efaa0a86db4bfd0f4`  
		Last Modified: Thu, 28 Mar 2024 03:19:12 GMT  
		Size: 145.3 MB (145271224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b33bc00ef9a1b14f311e31b0be14e43da3fd847c44fab84bcd34b5cb1c577e`  
		Last Modified: Thu, 28 Mar 2024 03:21:04 GMT  
		Size: 19.5 MB (19515994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57649eae4280f1504182782b77510baae3631ff93525f9993bdfa6180cce607`  
		Last Modified: Thu, 28 Mar 2024 03:21:03 GMT  
		Size: 4.4 MB (4399152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-lein-2.11.2-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6b140d7583f2fdac5ac8a0d15011a4f05c00c949451b11c92567222e9bd80d01
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215333937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609790e45f4440105dde7f18d8e1c00706de1ab5b07f33e8f53bfe4e6e36385d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:26 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Tue, 12 Mar 2024 00:45:27 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:42:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 02:32:13 GMT
COPY dir:d5fb8d9a38dea7496f2aff176bc9a34bbca80551c2dc57109d2dae5907a339ee in /opt/java/openjdk 
# Thu, 28 Mar 2024 02:32:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 02:35:06 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 28 Mar 2024 02:35:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 02:35:07 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 02:35:22 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 28 Mar 2024 02:35:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 02:35:23 GMT
ENV LEIN_ROOT=1
# Thu, 28 Mar 2024 02:35:24 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 28 Mar 2024 02:35:25 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095e0c8804330303f34a1bc5a23f03e613b1984ea526d87d9d7910e9b5449ef4`  
		Last Modified: Thu, 28 Mar 2024 02:49:26 GMT  
		Size: 142.0 MB (142006296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3502cfa5ef7959873c53eaf0aa90bb6f9b863220e30a0855d87a59f3615d63c`  
		Last Modified: Thu, 28 Mar 2024 02:50:55 GMT  
		Size: 19.3 MB (19337486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce006a7bf3446ed9f12341fb5faf30128b12d8c86bb5f5692c0595cca7edfe5d`  
		Last Modified: Thu, 28 Mar 2024 02:50:54 GMT  
		Size: 4.4 MB (4399171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
