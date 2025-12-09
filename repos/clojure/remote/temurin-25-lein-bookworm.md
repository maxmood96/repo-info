## `clojure:temurin-25-lein-bookworm`

```console
$ docker pull clojure@sha256:baceb2efe71068ce4519819f5334c03493e9c832913c77758e69bf1825668b53
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

### `clojure:temurin-25-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:a6db67b6caee9a8bfc3f8d78352b84ea9a0f033d8c0f63b1ea1cedd3e06bb324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.8 MB (164847075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8834e996a1038fae0a38cd36e2f9f8f06039fb3110635d924833872fd42f68`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:48:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:48:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:48:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:48:32 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 08 Dec 2025 23:48:32 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 08 Dec 2025 23:48:32 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:48:45 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 08 Dec 2025 23:48:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 08 Dec 2025 23:48:45 GMT
ENV LEIN_ROOT=1
# Mon, 08 Dec 2025 23:48:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 08 Dec 2025 23:55:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:55:20 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:55:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04996cb956706c0a8dbf84c71d0ea0bc432900866baa9adbfe85cc00b6246c8`  
		Last Modified: Tue, 09 Dec 2025 04:35:45 GMT  
		Size: 92.0 MB (92045295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc0cded79483636926ef293bbf504ef52183ed9d2915cf9f3b3ff9be510610c`  
		Last Modified: Mon, 08 Dec 2025 23:49:28 GMT  
		Size: 19.8 MB (19802894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc40f9620c777268e86025d3d3bfa7a4c8e1cb55caae5cf671f264b5f49d2366`  
		Last Modified: Mon, 08 Dec 2025 23:49:27 GMT  
		Size: 4.5 MB (4517724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0218d419ce2ac605fbed018e3303b929bde00880c704e07961dc1e55d6dbfba6`  
		Last Modified: Mon, 08 Dec 2025 23:55:32 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:be82dd8369a82465ba01a37c5361612ef28e842f5be8a658af052d96ce05c6bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4251856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3986d644d983a107a47908301bcea072b5bfe9c9cdfd1f6122a275d0e82dd477`

```dockerfile
```

-	Layers:
	-	`sha256:9cb06e4f5fa658b278d31960b16916fba1fd5ac7cb15dc2f611481cbfe821e33`  
		Last Modified: Tue, 09 Dec 2025 04:34:45 GMT  
		Size: 4.2 MB (4232396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e0dea69cac3131889fbe885e3df68ba511a2d461955ff2828b2906884155397`  
		Last Modified: Tue, 09 Dec 2025 04:34:46 GMT  
		Size: 19.5 KB (19460 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a280b0f43d48966775a24cb963eb34da5330cde0f8a8088f7a18341a998dd1fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163561902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81659992c33723fd7f8ce21bc107a10c83098d0f8b2698e372c6f17a9ef8aded`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:57:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:57:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:57:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:57:26 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 08 Dec 2025 23:57:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 08 Dec 2025 23:57:26 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:57:40 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 08 Dec 2025 23:57:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 08 Dec 2025 23:57:40 GMT
ENV LEIN_ROOT=1
# Mon, 08 Dec 2025 23:57:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 09 Dec 2025 00:02:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 00:02:51 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 00:02:51 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe28eb5139a077860f00475eb04bdc47e546c09148afbd1d3fecbe9ee4c203d`  
		Last Modified: Mon, 08 Dec 2025 23:58:37 GMT  
		Size: 91.1 MB (91052515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4aba18e68f968705cee94c08af8f2774245b1a2a37f23c3328df37681b8dfe9`  
		Last Modified: Mon, 08 Dec 2025 23:58:27 GMT  
		Size: 19.6 MB (19632137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ac78feff5f6366c42f6e8ebc2173df0341f9cd1a9625e112da1393e22c264d`  
		Last Modified: Mon, 08 Dec 2025 23:58:26 GMT  
		Size: 4.5 MB (4517752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f1f37cc49ed7281852b2dd39475cc4336f3e26d8d97aefb5026611caad7ae`  
		Last Modified: Tue, 09 Dec 2025 00:03:03 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2999e89aa785c27095130e0ffbf408a4b38708db865046bd9c90b1ab17aec5a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4251733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913298fddb8eda5dd04e41c8e9daf72ddffef66ceeb541ca3a92fc135c3759d3`

```dockerfile
```

-	Layers:
	-	`sha256:60e8dbc5367066d98cede94a11abe37c782e9e82f20b0c7d8923dd1cca58d173`  
		Last Modified: Tue, 09 Dec 2025 04:34:51 GMT  
		Size: 4.2 MB (4232080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd87d8084e118a8911820e52672ac6e675394cb18df563faf4fda79bb6e4d46e`  
		Last Modified: Tue, 09 Dec 2025 04:34:52 GMT  
		Size: 19.7 KB (19653 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:b083e1506f50b10c4046a03bebc0c273fc1068d8e48093bfb193f1dbb6f88fe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168477588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c719f11c94378dcb2bfe878e3bd1d0606c415c0bfdb556057d26d5e0fa3804f2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:34:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 22:34:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 22:34:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 22:34:22 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 08 Dec 2025 22:34:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 08 Dec 2025 22:34:23 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 22:35:12 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 08 Dec 2025 22:35:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 08 Dec 2025 22:35:12 GMT
ENV LEIN_ROOT=1
# Mon, 08 Dec 2025 22:35:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 08 Dec 2025 22:46:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 22:46:01 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 22:46:01 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c088128ea77bb5c706bb00930020ea2fba147060275f49c5a7be6b54af5ca7c8`  
		Last Modified: Mon, 08 Dec 2025 22:17:06 GMT  
		Size: 52.3 MB (52326977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbeeb5c6058bd793bb98336cf15f96291626b642ff5b9461a0723bb0f77fc9eb`  
		Last Modified: Mon, 08 Dec 2025 22:36:56 GMT  
		Size: 91.6 MB (91610764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be781a3ac1a4f6d9f0a37c15905238450552f33e0d7f3672a1c47afd7ebeab6`  
		Last Modified: Mon, 08 Dec 2025 22:36:51 GMT  
		Size: 20.0 MB (20021660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c45adbbe470ce5178d26de2fd84d72b3eba3031e1fb5213e0d278e7d4c1dddd`  
		Last Modified: Mon, 08 Dec 2025 22:36:50 GMT  
		Size: 4.5 MB (4517760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c549a863c28666fa69ea0faaef9ab639cb5536d899f363902fc8de5051e76287`  
		Last Modified: Mon, 08 Dec 2025 22:46:26 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:690e343be125eb3c961c9d89ab9ae2aaa5b27e74916c2b4850cb24cc9aba9130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4255928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44de673a5ce422af48833e30d85030f2a80a0663719f362beb9d3edf00220c7b`

```dockerfile
```

-	Layers:
	-	`sha256:bb6593c15b8c0c40c31a0380518f4b137259fce80aab9503e64659d668196f39`  
		Last Modified: Tue, 09 Dec 2025 01:34:51 GMT  
		Size: 4.2 MB (4235589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c50a8ef67fc25c7bc04f0748b4cbbdd27a4cb2756e4fd88c695932c4d7f3eb28`  
		Last Modified: Tue, 09 Dec 2025 01:34:52 GMT  
		Size: 20.3 KB (20339 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:94d521e6a98c9e0763ef9be733e0410a23ac1a1867d8b252b543de45800c4ede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159327308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ac9b794db8a2f0a167e29a338d8e0e9e8c8351da368f8a2161255810390171`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 01:24:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 01:24:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 01:24:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:24:12 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 09 Dec 2025 01:24:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 09 Dec 2025 01:24:12 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 01:25:00 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 09 Dec 2025 01:25:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 09 Dec 2025 01:25:00 GMT
ENV LEIN_ROOT=1
# Tue, 09 Dec 2025 01:25:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 09 Dec 2025 01:32:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 01:32:57 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 01:32:57 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f1896ba83f603ad81e0d8cb48b496e763b4b781a68efe11f1b6de9da929514ea`  
		Last Modified: Mon, 08 Dec 2025 22:15:09 GMT  
		Size: 47.1 MB (47137665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6024d0cf3f3c2e42efef958fee18109019160ed5dc0afc14b97b74565341a9`  
		Last Modified: Tue, 09 Dec 2025 01:26:10 GMT  
		Size: 88.2 MB (88210741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cb6a978e4eb335173c5bf398c9021ede3e48c0f47432745ee80f1f35c3c606`  
		Last Modified: Tue, 09 Dec 2025 01:26:01 GMT  
		Size: 19.5 MB (19460754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59534ae50a9c9efe1e86ba8ed8735edf45ed1a1d59031cfde2f10ffef9869acb`  
		Last Modified: Tue, 09 Dec 2025 01:25:58 GMT  
		Size: 4.5 MB (4517724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb218e399fcb110e92d91764402b9a37ccba1bb660b8fdadf7b7fc1e46866db5`  
		Last Modified: Tue, 09 Dec 2025 01:33:15 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8a59b1106317d2c92d1fa9c32e3aa914d681b0c31715744e2c9ac5d897c9c885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4247017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:016b27e5e0b2d653e1407c76cc62986c26f310368b8d87a7e6faf4392dd12364`

```dockerfile
```

-	Layers:
	-	`sha256:4260704d44d624ece0fd0091e5c3909a0470a92592e2ae205e1868762f3ee0ab`  
		Last Modified: Tue, 09 Dec 2025 04:34:59 GMT  
		Size: 4.2 MB (4226758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85014a3585da3118444744553f794c960f4c3b60cabbab6f127abebe5318063a`  
		Last Modified: Tue, 09 Dec 2025 04:35:00 GMT  
		Size: 20.3 KB (20259 bytes)  
		MIME: application/vnd.in-toto+json
