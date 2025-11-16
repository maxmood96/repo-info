## `clojure:temurin-25-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:98ab812d2d327ba1bb17761ef307b1c3744d1fe7978b8a63486a9e74f913b3f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-25-lein-2.12.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:ca99e27b42b3ba260bf6b2592319801f09a526bcc023affc928713d9bde4b75f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.4 MB (164428259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f19147a69698ad9b8a6f89517c2dd2946d0479573e37512495d71bf5ac8bc67a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:55:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:55:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:55:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:55:53 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:55:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:55:53 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:56:09 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:56:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:56:09 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:56:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:56:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:56:10 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:56:10 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d26240918ed29e7a1f6f95cb371f7f2e163c3315f5188fb12c0229b4cb929be`  
		Last Modified: Fri, 14 Nov 2025 00:56:44 GMT  
		Size: 92.0 MB (92045286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6470f79aabf541de216b8f895295f42d0cd7f1975f634d71387ac9b9834adcfa`  
		Last Modified: Fri, 14 Nov 2025 00:56:36 GMT  
		Size: 18.6 MB (18579215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3956dfc8f7bcec5827814fddf62233514e9e5da00522973bd64271461ea594b`  
		Last Modified: Fri, 14 Nov 2025 00:56:34 GMT  
		Size: 4.5 MB (4517702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95804850ae56e7509a41b5215014739de03bdecc61aff81ed31a06c9aafd54f9`  
		Last Modified: Fri, 14 Nov 2025 00:56:34 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:39726331c89a515848d95d41787e844bf5b25644fa5a840451b8b277774d27ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3783661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e4658498c5376133387b7513c26db216cb575b22b04a4ff2ff031d441cff88`

```dockerfile
```

-	Layers:
	-	`sha256:a6d35f8bd83c9870ff3443d004b662b869529da37f13c78ae95ca4209cafca33`  
		Last Modified: Fri, 14 Nov 2025 01:47:09 GMT  
		Size: 3.8 MB (3764682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf4b08525403e78862b164f68c0bcc66f812517bb4827f424b3a65fa0e0d3534`  
		Last Modified: Fri, 14 Nov 2025 01:47:10 GMT  
		Size: 19.0 KB (18979 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4ab9855fc431c72cdbb766f3b7097f189d47a330ec12935a3f553d2904cd2078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.8 MB (163761055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79be501ddff344ab6cab36e671455912ddceba9d94ec5560165a7ac2aa5d4a3f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:58:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:58:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:58:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:58:01 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:58:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:58:01 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:58:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:58:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:58:18 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:58:19 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:58:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:58:19 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:58:19 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d6a4b0851697eb6099ea74fc5db7127975d5e85a94605052574483294a78b4`  
		Last Modified: Fri, 14 Nov 2025 00:59:00 GMT  
		Size: 91.1 MB (91052512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e853e4ebf2b5e4bef82fac96b658ffa9ce5713cca34c931914b2f7586ebe9e`  
		Last Modified: Fri, 14 Nov 2025 00:58:50 GMT  
		Size: 18.5 MB (18539981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5547ea27f6affe556c7c6636a0d039b21613c3e4518c7384688000c31eb87dd2`  
		Last Modified: Fri, 14 Nov 2025 00:58:47 GMT  
		Size: 4.5 MB (4517703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da1d5ee70c81319012838a7de701b709b291efd9b1a99a5fbedf0f250eb3ec4`  
		Last Modified: Fri, 14 Nov 2025 00:58:47 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:eda8ced7a101db5f9f172ff1b3fcc1e754b4b6c7395116348da14e6e4dc4d0c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3784704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa2962136a776929f7a69441619790df6ec097f13ba3f14be76a0f257658ee78`

```dockerfile
```

-	Layers:
	-	`sha256:0e498c987581cfe13d2b7564a4add413510116a1099c17bdda17a065167059a7`  
		Last Modified: Fri, 14 Nov 2025 01:47:15 GMT  
		Size: 3.8 MB (3765580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d96faaf6161fc9ef1997a9ebfd1725dacc10d1dfe90b98eb08b21a9bc544c8de`  
		Last Modified: Fri, 14 Nov 2025 01:47:15 GMT  
		Size: 19.1 KB (19124 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:f82ec1dd5e1763e5a05f53a844226719a8e2c7d2839e1ef744e75ee257618742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.9 MB (167875680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076c7d6755d21b9ad2a1da0831ac0d49c86bdb4e7d2f7a2ae13bbc9ff12409e5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 07:37:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 07:37:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 07:37:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 07:37:21 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 07:37:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 07:37:21 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 07:37:52 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 07:37:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 07:37:52 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 07:37:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 07:37:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 07:37:55 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 07:37:55 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3c335bb15935da0eae5ce30111cfa6a289c813162bada9fd389d8ae5510d5d66`  
		Last Modified: Tue, 04 Nov 2025 00:20:22 GMT  
		Size: 53.1 MB (53110127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fca0d27d8996ef66dcabcb59cfb3c0eebdf10bc7ec89045b01223b384d9ee00`  
		Last Modified: Fri, 14 Nov 2025 07:38:48 GMT  
		Size: 91.6 MB (91610768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fb34974afe3a9f6cf6fa69b21f0698d90894bea00d8b36d9ec1d7323d0e651`  
		Last Modified: Fri, 14 Nov 2025 07:38:41 GMT  
		Size: 18.6 MB (18636603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4535a48d42b16d261af5af0f314c597c4df80bf3448941abfa9aa45c79634a8b`  
		Last Modified: Fri, 14 Nov 2025 07:38:40 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773b8a298e804f5b2d3550b225591be831fd7829d04ed1a27095a92ca5d67774`  
		Last Modified: Fri, 14 Nov 2025 07:38:40 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:611dd14de4019454a6a561c8a6f66bca252295baa29563f02442243d2e2b934b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3786025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fedd5bfefb761d0c659f2c6d7751517b1e16d583915213f21f8eb8d0128dbe1f`

```dockerfile
```

-	Layers:
	-	`sha256:328f865fcfc95033fbe84b32d15b7e6d711172993080fed384eecc62f2764852`  
		Last Modified: Fri, 14 Nov 2025 10:34:47 GMT  
		Size: 3.8 MB (3766990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68578873e2e42a67d127a9a730713202f4f31c915d004fba90c12244d6e58e58`  
		Last Modified: Fri, 14 Nov 2025 10:34:48 GMT  
		Size: 19.0 KB (19035 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:f1b6287879e3d06bd98205151da01e55127990ecfa0e4e1ace6a6d86b0dccb30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164724188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9d0a1247b2680b95edeb833b37073c8a5aa94c774c3510e0a79a9649d47786`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Sat, 15 Nov 2025 22:18:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 15 Nov 2025 22:18:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 15 Nov 2025 22:18:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Nov 2025 22:18:32 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 15 Nov 2025 22:18:32 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 15 Nov 2025 22:18:32 GMT
WORKDIR /tmp
# Sat, 15 Nov 2025 22:20:07 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 15 Nov 2025 22:20:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 15 Nov 2025 22:20:07 GMT
ENV LEIN_ROOT=1
# Sat, 15 Nov 2025 22:20:24 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 15 Nov 2025 22:20:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 15 Nov 2025 22:20:25 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 15 Nov 2025 22:20:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:de6b66e2abcf55248485e438d6def9b92cf28773b7cd7896ee78f9409b6e7526`  
		Last Modified: Tue, 04 Nov 2025 00:27:48 GMT  
		Size: 47.8 MB (47770924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a46ebd6f56fdb6d1c0e17f14db200e703d8de3e8f2d436ad48d3420edcd35b6`  
		Last Modified: Sat, 15 Nov 2025 22:24:32 GMT  
		Size: 90.8 MB (90752842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8686d2d2bcffde798f6788424fb2c4210142caadd5112f8d09bcca3015ec7a64`  
		Last Modified: Sat, 15 Nov 2025 22:24:31 GMT  
		Size: 21.7 MB (21682202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fc351e41199be0c1c8ced35856d73a5d3eeb61b8075692bb476b9b390ac5a5`  
		Last Modified: Sat, 15 Nov 2025 22:24:26 GMT  
		Size: 4.5 MB (4517791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb652f67b2883a1c9cd340eec0e4e79d2fbf3552c9624c1052c839872a210012`  
		Last Modified: Sat, 15 Nov 2025 22:24:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2fabcdac608057e8b58abaab97c71eb34495c7ce89d68bf140a462eb237bd37a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3774195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0b3dfbcb28f4ce7c39500419bfbd475f1611e339c10cdbd82ef8c28609e7a18`

```dockerfile
```

-	Layers:
	-	`sha256:7ef9a7a9cfce5482b2ae0c35a161b015c727afa4cb0da6f2768a02f76486ad79`  
		Last Modified: Sun, 16 Nov 2025 01:34:32 GMT  
		Size: 3.8 MB (3755160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7cb402949819222fd08391799916071d981d2f8f57e108e77801803743c6042`  
		Last Modified: Sun, 16 Nov 2025 01:34:33 GMT  
		Size: 19.0 KB (19035 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:05503519b1e6f2ecca4f44689f2f798c74f93b21a200fa9fdac8b0e0e6d6766d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160701313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea31118afaf2a166fbe800deb0d9975a5196c6b1df794c6a07593a2f33f050ef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 01:03:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 01:03:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 01:03:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:03:26 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 01:03:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 01:03:26 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 01:03:39 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 01:03:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 01:03:39 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 01:03:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 01:03:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 01:03:41 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 01:03:41 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:48bd359f940d437208e8579c571291503fa327e04a66a6c8d918cfe93cae2e1e`  
		Last Modified: Tue, 04 Nov 2025 00:19:45 GMT  
		Size: 49.4 MB (49352299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f341851c0a404acd46e39bc75b770150829c4182f3a6c3691b43c7ac0b5bebe`  
		Last Modified: Fri, 14 Nov 2025 01:04:20 GMT  
		Size: 88.2 MB (88210669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b6e813a0b1295caf7f1a7abd507e5ed3a0809ec24bfbf64571f53ee11469c4`  
		Last Modified: Fri, 14 Nov 2025 01:04:13 GMT  
		Size: 18.6 MB (18620175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bbab46fe790e7d50e4b4c7d0a1fad26586c4db113ea3be63b95ed77b6363dd`  
		Last Modified: Fri, 14 Nov 2025 01:04:10 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cce1c85b4f8a2abb4537cbd6db0c5b28fd00e06b94bb1a11e93a22646fd8985`  
		Last Modified: Fri, 14 Nov 2025 01:04:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:53c4af0edf4ac1b8ce07db4411aac5ba1a7e032ec3b6c37fa42d157b3ad9470d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3782636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7e3f7f163fe454c82edf34e568c32d22b3696082f137e2cae2005f61147d95`

```dockerfile
```

-	Layers:
	-	`sha256:0553f1e84ee4963e4cb88093f17fe7eebc9352f3c9ee5eef6bbc57111aa7359c`  
		Last Modified: Fri, 14 Nov 2025 01:35:15 GMT  
		Size: 3.8 MB (3763657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd249064a59bfd6e78559ed21d89b0f0af0dcdf60227c74519bef8c52ccacb7`  
		Last Modified: Fri, 14 Nov 2025 01:35:16 GMT  
		Size: 19.0 KB (18979 bytes)  
		MIME: application/vnd.in-toto+json
