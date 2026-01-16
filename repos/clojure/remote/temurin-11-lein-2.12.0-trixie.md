## `clojure:temurin-11-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:84d7b51a8796226cc96043922cc6408e8187cecf0bd42c6d46656eb3ae44af48
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

### `clojure:temurin-11-lein-2.12.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:1c793aa9499237e8c6a999e35b7887072643ef222bec84c6e97421ddcd5902b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217349650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe90117645e7de272299fc2819c89f463a1c8a311ba0f72186504d2b62a01cd`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:25:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:25:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:25:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:25:18 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:25:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:25:18 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:25:34 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:25:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:25:34 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:25:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:25:35 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e78e7bb435066daae0345d54d76378d787c55f699b77d975f071f5a7cc2f39`  
		Last Modified: Tue, 13 Jan 2026 03:32:51 GMT  
		Size: 145.0 MB (144966652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30f2b9c5dd52397824894cee1d40a5f989a6e1c7c3f466b705ee9c7b6aba407`  
		Last Modified: Tue, 13 Jan 2026 03:26:06 GMT  
		Size: 18.6 MB (18579641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b049d3ed725160340b4fa65abb8321e0b3d0ebc62042a444a594802afb45908d`  
		Last Modified: Tue, 13 Jan 2026 03:26:05 GMT  
		Size: 4.5 MB (4517704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:eccac69a53f07c61686e7aef35ca6a901ce38fc1f29fcf472e3e19ce6d76834a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3850741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37f065251c17d055c659eada79b8bf53d4a94f98aafa6ce437f28c5735ceae6`

```dockerfile
```

-	Layers:
	-	`sha256:b591464b296fd6fe8bb756778caf0c1aa81db0b009948b4fee8ef56b0d4be736`  
		Last Modified: Tue, 13 Jan 2026 07:37:44 GMT  
		Size: 3.8 MB (3834378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3d76d9ab921b21c41e99efdca0d1ba336e48884c97ce781654ea194bebb257f`  
		Last Modified: Tue, 13 Jan 2026 07:37:45 GMT  
		Size: 16.4 KB (16363 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9c31db9a07ceaff8045b5d78cb85f331db909423e6a6e8823822c8acdbf354aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.4 MB (214438232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e70a1df8aed535fa7764a0b5bc2b46eed158811cc37ebb009103db24c7aa34d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:30:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:30:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:30:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:30:13 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:30:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:30:13 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:30:30 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:30:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:30:30 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:30:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:30:32 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1fc5c15a487a75f5c5ebeac9018f34cc49ed65f983cd77d9f604b2a8b7ab70`  
		Last Modified: Tue, 13 Jan 2026 03:33:52 GMT  
		Size: 141.7 MB (141731575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360d0af006b51b61f8e7933e352df2c54f1c5131ed12f758d92025eb3b01205e`  
		Last Modified: Tue, 13 Jan 2026 03:31:01 GMT  
		Size: 18.5 MB (18540796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8927005dc2f6bb055fad658890924e3402ad71fd4fd72f6f1c583ea853e993fe`  
		Last Modified: Tue, 13 Jan 2026 03:30:57 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9d29f3182aa9f02364fadd07cc2a405795a3fe03c8e42159608248e1f7d8e623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3852358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f7589cf5785c36e26c617ac8fb7905014240802dcecd7c8cbdf5b5cc54be9c8`

```dockerfile
```

-	Layers:
	-	`sha256:a099d33fee1deb6405e4f8b347481714bb1e52c4927a696b4d3c12247543c1a9`  
		Last Modified: Tue, 13 Jan 2026 07:37:49 GMT  
		Size: 3.8 MB (3835873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3986403668cdc13a52a661df3910e39297089d741c92b4fa34056ebc205cf9b8`  
		Last Modified: Tue, 13 Jan 2026 07:37:50 GMT  
		Size: 16.5 KB (16485 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:f77fadea11878c5097f576d0c819d81092682e39858e13b74b20f9b67eae4f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208343917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d2b85cbf41afc183d8e1c3050d6d9e1e18a48f8e19b58f5908eb6c31ed40419`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 12:16:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 12:16:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 12:16:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 12:16:34 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 12:16:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 12:16:36 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 12:17:25 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 12:17:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 12:17:25 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 12:17:28 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 12:17:28 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6ff412c1efdf82a2030de7bb593b97f09e02e2b337f615eb1c3faedeef765d44`  
		Last Modified: Tue, 13 Jan 2026 08:45:58 GMT  
		Size: 53.1 MB (53106962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5c8d7e74beea5fe4ca8673fcbe7c993895d0e5cbc89d157ae4f5ff10ed05ef`  
		Last Modified: Tue, 13 Jan 2026 18:41:36 GMT  
		Size: 132.1 MB (132081949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9d6f883cffa7c832b8da70c10b177bf0e0dd33db0d5c0b050fb893728755d4`  
		Last Modified: Tue, 13 Jan 2026 12:18:22 GMT  
		Size: 18.6 MB (18637225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f53e2e1b3bc76c51fbd4ec45995b97f611695e2e8cba7a4c364789faa6409607`  
		Last Modified: Tue, 13 Jan 2026 12:18:18 GMT  
		Size: 4.5 MB (4517749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e0d998e087bce81459b84ee2b53ae20511db0f79a002f07131467ec00267093f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3851171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c66707afb88673d4b347ec5c8b10037e1f828f6e7bb16fc8e2cdabf5e6dc1d`

```dockerfile
```

-	Layers:
	-	`sha256:c8aef7514375fb6983b8099a0e1425cd32504dc4447d01c4eca594d2b728f01c`  
		Last Modified: Tue, 13 Jan 2026 13:34:56 GMT  
		Size: 3.8 MB (3834763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b4c727bfcaaf746b1398180e3ff512115dc69a8f75c0f35b6bb4c8cd7e1991d`  
		Last Modified: Tue, 13 Jan 2026 13:35:04 GMT  
		Size: 16.4 KB (16408 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:42e5c99d326e3e945be2b6c4db1d55e80f8d026a84a214b3afb292169711392a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198182012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aca03f81a1b1ff36cd49710d39cf54e8d4123fba2e975e2c2ee33562dcaea99`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Thu, 15 Jan 2026 23:10:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:10:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:10:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:10:51 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 15 Jan 2026 23:10:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 15 Jan 2026 23:10:51 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:11:10 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 15 Jan 2026 23:11:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 15 Jan 2026 23:11:10 GMT
ENV LEIN_ROOT=1
# Thu, 15 Jan 2026 23:11:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 15 Jan 2026 23:11:12 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:9de0288d81a9602539c9f3015fc521191e25eebfe6442c22cb974ea3a486f3a8`  
		Last Modified: Tue, 13 Jan 2026 00:41:55 GMT  
		Size: 49.3 MB (49348704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96aae73d6ca9c475bb213977dcd29121719a295968930d64b57e8491e3a1f0e1`  
		Last Modified: Thu, 15 Jan 2026 23:11:54 GMT  
		Size: 125.7 MB (125694843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de9bae4406cf2439c57383f0423b7a7b5b3a60b43e463d6c99b7c434d6b024f1`  
		Last Modified: Thu, 15 Jan 2026 23:11:43 GMT  
		Size: 18.6 MB (18620683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca46c915fa4e3898b3d680c3931e3db4362d6f619eb657fef1057d678c2be94`  
		Last Modified: Thu, 15 Jan 2026 23:11:46 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ebabaf913605460119b175cde36703ffbfed515f97ed6550d2fdfafef52410d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3847172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0a6d7a936dcbcb523ed7da6acd9b9ef6487540a9bd7b3085ebcc0aab94502ba`

```dockerfile
```

-	Layers:
	-	`sha256:caf7f93c7ebef48ef91d22e1b134e543a8a32f591edc5c42109e1dab5b67b118`  
		Last Modified: Fri, 16 Jan 2026 01:37:49 GMT  
		Size: 3.8 MB (3830809 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcc3f8b576fe6ed079dbe14b1e91ffc8b7579b4f42188500609e10eaddd508c4`  
		Last Modified: Fri, 16 Jan 2026 01:37:50 GMT  
		Size: 16.4 KB (16363 bytes)  
		MIME: application/vnd.in-toto+json
