## `clojure:temurin-17-lein-2.11.1-bullseye`

```console
$ docker pull clojure@sha256:4b7976a8d1c77c447289850c0fbff28d634bc56f166f740f3dad461abe94b762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-lein-2.11.1-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:a7d21a4c991c8f75b6cb14a8fed149c9c83456e7052af6b6c66ed18a63154edd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220703061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff43f2f9a06cdc69b7d3187b771cd10ccbf86956490ef1a773edfde4b81af45`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:29 GMT
ADD file:4fa73c8d113df02c8656b74ab87563432215332f3de78446a02e5ab7d6e2ab7a in / 
# Wed, 31 Jan 2024 22:35:29 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 17:19:15 GMT
COPY dir:2765b9c6732dde1d622a6314ea7119038a6031d832e1ec655de4889b7fd05a2e in /opt/java/openjdk 
# Fri, 02 Feb 2024 17:19:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 17:22:15 GMT
ENV LEIN_VERSION=2.11.1
# Fri, 02 Feb 2024 17:22:15 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 02 Feb 2024 17:22:16 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 17:22:30 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "03b3fbf7e6fac262f88f843a87b712a2b37f39cffc4f4f384436a30d8b01d6e4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 02 Feb 2024 17:22:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 02 Feb 2024 17:22:31 GMT
ENV LEIN_ROOT=1
# Fri, 02 Feb 2024 17:22:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 02 Feb 2024 17:22:33 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Fri, 02 Feb 2024 17:22:33 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 02 Feb 2024 17:22:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7faaa42ac0c18c9baf539c97a5c8f042d02a77b05380cb57759e4407385710dc`  
		Last Modified: Wed, 31 Jan 2024 22:40:15 GMT  
		Size: 55.1 MB (55056963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6042788be26bf5907bf073b4e97419650a74e28626818034fb050958a263abc`  
		Last Modified: Fri, 02 Feb 2024 17:36:38 GMT  
		Size: 144.9 MB (144893169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832f05f86c5833e81f6885901fa2a598176dce85164ba824ce3d9b351f0dee5d`  
		Last Modified: Fri, 02 Feb 2024 17:38:03 GMT  
		Size: 16.4 MB (16353368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866e58d17b3cb6f6a035bcfe00f6e4b17c85b5bf7069fe0610f3804448a5f168`  
		Last Modified: Fri, 02 Feb 2024 17:38:02 GMT  
		Size: 4.4 MB (4399160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dfa303544df776e7c2fef7935d5566c4f6be7d6bda21662d0e76bc7d1c5b072`  
		Last Modified: Fri, 02 Feb 2024 17:38:02 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-lein-2.11.1-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7a04017d0a11993d361e6756103b43d8c8f8c7648141cc974c180c4dc983dcf9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 MB (218170780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8740fc8060ee54afd8109ff0f08e4093f97827567e5fd8754ba10028335c0495`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:33 GMT
ADD file:81cb49e646b9feb1ddeddea1cb6dbafa672a250f1553cc28eae09c955607236d in / 
# Wed, 31 Jan 2024 22:44:34 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:20:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Feb 2024 08:28:07 GMT
COPY dir:1e33e1b9b4d5ff1fcafcf70a5b147d046ddd08f2a0ffd21b97536e3a6e636c5f in /opt/java/openjdk 
# Fri, 02 Feb 2024 08:28:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 08:30:49 GMT
ENV LEIN_VERSION=2.11.1
# Fri, 02 Feb 2024 08:30:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 02 Feb 2024 08:30:49 GMT
WORKDIR /tmp
# Fri, 02 Feb 2024 08:31:03 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "03b3fbf7e6fac262f88f843a87b712a2b37f39cffc4f4f384436a30d8b01d6e4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Fri, 02 Feb 2024 08:31:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 02 Feb 2024 08:31:03 GMT
ENV LEIN_ROOT=1
# Fri, 02 Feb 2024 08:31:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 02 Feb 2024 08:31:05 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Fri, 02 Feb 2024 08:31:05 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 02 Feb 2024 08:31:05 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4b6eb2d0256d18652f84fd30c1db34ce9462e535a2d96fbf2f9044db000b13f5`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 53.7 MB (53708267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:523444442ef38521daa043679e098a4bc371abf52c97c5b3cc69543c2795e1f4`  
		Last Modified: Fri, 02 Feb 2024 08:44:13 GMT  
		Size: 143.7 MB (143720935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e84b313fbf2daeb5317a2768db0e73e5f07444b69613286103c5d3d7b7854a65`  
		Last Modified: Fri, 02 Feb 2024 08:45:30 GMT  
		Size: 16.3 MB (16342012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f32f951362e1cfe59a475a2829d69797961c8a2d329a4fcc428876c62352df5`  
		Last Modified: Fri, 02 Feb 2024 08:45:29 GMT  
		Size: 4.4 MB (4399165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1c9cdadb8d35054fbe9775b1b763b843c94727a6d6a3cfa3737c0ab06efa60`  
		Last Modified: Fri, 02 Feb 2024 08:45:29 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
