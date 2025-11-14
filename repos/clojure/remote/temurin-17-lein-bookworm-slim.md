## `clojure:temurin-17-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:9932017e2584123d281715c4234b7f28ca299425d5aed6d51eafe6c2d7bee1f4
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

### `clojure:temurin-17-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0ca2efee0879467f57f35c847e31360f4620d5a8ac7dc60a33da51f89bf0aff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.4 MB (195352736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e60d79b614f40c417977bbbe71f532af08288dc084f9093f0bcb404fb6a4bf10`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:52:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:52:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:52:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:52:12 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:52:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:52:12 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:52:25 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:52:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:52:25 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:52:27 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:52:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:52:27 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:52:27 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dfec4cda76f28dd4a15bb5191d18c9a492e1bf940b9f814ecfa7e601203cf81`  
		Last Modified: Fri, 14 Nov 2025 15:01:40 GMT  
		Size: 144.8 MB (144847946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f8be502491f51662dbdec4fb3dc6a2b6a579d258ea95fff0eca17c5137be0f`  
		Last Modified: Fri, 14 Nov 2025 00:52:56 GMT  
		Size: 17.8 MB (17758077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed88ceddd0dcd585fbef99b4e3539742e0c998ff80b8927ff1729438dad480cb`  
		Last Modified: Fri, 14 Nov 2025 00:52:53 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa59359c501116cf7f48a5a5b778d6aa332addde23abc075fe07f7a80ba60475`  
		Last Modified: Fri, 14 Nov 2025 00:52:53 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e508f423a2f0e4c8af5c213e18262c0f27dee3a32c9d3a6c5e34e01d2c80ec84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2747191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac6383a681398cc7d48a91a07a243f8790f4cf425d179181ce15d5c6a825563`

```dockerfile
```

-	Layers:
	-	`sha256:f3747f0b0931283de55bbbe1b94b8b8760ae0e7a763e259c146045f83ac6dcd4`  
		Last Modified: Fri, 14 Nov 2025 01:39:53 GMT  
		Size: 2.7 MB (2728788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:181c5db639915f442401225e465b3da7e69eb280d899e934e1eaa331a244ce95`  
		Last Modified: Fri, 14 Nov 2025 01:39:54 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cbdfdbe136111474f3e6f9f95b40956a1af797c166cc8e4ad0959a0dc0b00543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.9 MB (193891591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ea196fde8c870c8671cec83631b0bb106d1a4534ed97e62b199c7b02be32c4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:54:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:54:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:54:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:54:01 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:54:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:54:01 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:54:14 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:54:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:54:14 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:54:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:54:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:54:16 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:54:16 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad13d2bbd74e011d304ff7750d6f05ff7ca072680cd5f2194a35b57a3ad38263`  
		Last Modified: Fri, 14 Nov 2025 00:54:36 GMT  
		Size: 143.7 MB (143679910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2692adede6812f386634520f69f4979a40f5987f2dcdf025da8f020249c6925f`  
		Last Modified: Fri, 14 Nov 2025 00:54:45 GMT  
		Size: 17.6 MB (17591120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a47b493810c645df593cd1d647ecbebb93e4c118fc8fb4d637acba75a288a91`  
		Last Modified: Fri, 14 Nov 2025 00:54:43 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6878b403404c6965b955127f999efcbcf2235a7d9529984678c2123ec2ec9bbe`  
		Last Modified: Fri, 14 Nov 2025 00:54:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2659feb613d59c1b24fdfcdb577a5e96a4c0082ed2d5a714cc2393665b3876de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2746926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc40deb3d250bc28c77530623095ccf3f285fc47fb5c1b772c64a910d20adf4c`

```dockerfile
```

-	Layers:
	-	`sha256:69380d5122ceb2c0e6a12b6b19800267713b0841e0c5f13b8184355650c45fc6`  
		Last Modified: Fri, 14 Nov 2025 01:39:58 GMT  
		Size: 2.7 MB (2728403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9ce2c5b33657b4a46890d35469b1a644ef5da7ca96e7d52c844bb47dd57385e`  
		Last Modified: Fri, 14 Nov 2025 01:39:59 GMT  
		Size: 18.5 KB (18523 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:db5c86415d2eb959193c98727aeca0d70f7de061de8e9e72c9dd6ecf7a42e409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199071904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc0118ee57541f63b3ae71bb18596c12a68499461d90de09abd0f474c51a459`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 07:00:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 07:00:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 07:00:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 07:00:57 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 07:00:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 07:00:57 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 07:01:24 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 07:01:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 07:01:24 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 07:01:27 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 07:01:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 07:01:27 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 07:01:27 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b176331cf478c057cf81bcee97bd0229df3da42a81c5204530e734e42ea70f4`  
		Last Modified: Fri, 14 Nov 2025 07:02:08 GMT  
		Size: 144.5 MB (144525224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b2d23d9313173082ef031a655371eac2e53f5f2a5b2ef394e316995679cec1`  
		Last Modified: Fri, 14 Nov 2025 07:02:14 GMT  
		Size: 18.0 MB (17959585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7052dddd64d4ad550b889cdf4dd6362f8c8dd3b7f26b3291b4152256779b5c7b`  
		Last Modified: Fri, 14 Nov 2025 07:02:13 GMT  
		Size: 4.5 MB (4517760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f255d12b6bca815e0e19b398b793e4c1ced6ed27da46ce9869106839063c3241`  
		Last Modified: Fri, 14 Nov 2025 07:02:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:47b79b2d219dafd27b0b5c83359b10af711e7bf00a69479e0954e916756703dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2749067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185d55261de6d4a04bb3ae68e7c56d6b45f21d841c8eb66d0a8a8b564c626e50`

```dockerfile
```

-	Layers:
	-	`sha256:feb3965c955dff1980ef6c5d66ad0d10aa2d251d7e25a3c60858fde684442abf`  
		Last Modified: Fri, 14 Nov 2025 07:37:17 GMT  
		Size: 2.7 MB (2730621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66a388fb41b44f1e57de9e37f06dc442f9569e22e13924c310e1059ba8b9ec86`  
		Last Modified: Fri, 14 Nov 2025 07:37:18 GMT  
		Size: 18.4 KB (18446 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:422c718bc6d4fb79595494e57be72d8314e4b21356374ecbb61654d6e4782fbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.7 MB (183681549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c93d55aff38ffc8d6bee86dc45091a3204167a8214a8043e3b26c022cc1d34cc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Fri, 14 Nov 2025 00:55:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:55:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:55:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:55:27 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:55:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:55:27 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:55:37 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:55:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:55:37 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:55:39 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:55:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:55:39 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:55:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ce5e7df93c7febf25e35259674232a1818f8d088f849e2c5e02b3f099c63d8`  
		Last Modified: Fri, 14 Nov 2025 00:56:03 GMT  
		Size: 134.9 MB (134859063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463731879700248a9a60a67bd955b68ff20e62e3963130943dc9836a6db1309f`  
		Last Modified: Fri, 14 Nov 2025 00:56:09 GMT  
		Size: 17.4 MB (17419759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff01aef9cc28620e145a6b128f9e189141e80c85dc588cc279e4dfd8bd3dc1f`  
		Last Modified: Fri, 14 Nov 2025 00:56:09 GMT  
		Size: 4.5 MB (4517745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d4116f38f4086e5f0e5a4d4cdcc53ef13eb7ee3abe310f98fbcc6104f404ab`  
		Last Modified: Fri, 14 Nov 2025 00:56:08 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6c54b9615888f009fbc5119b5f5798b6d1cd516807eb21b91f38c0136df8e725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2739005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03087c30943ebc3ce13a7460ada8216423b2d74c66073dfad371f06cdcda9eea`

```dockerfile
```

-	Layers:
	-	`sha256:24a0826221f2b6a7a3814530b2de69fa990f6df2345081edc4806c9cc6dda5ae`  
		Last Modified: Fri, 14 Nov 2025 01:40:07 GMT  
		Size: 2.7 MB (2720602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:508a716d284860206f690d359ab5f0198d8d9eea812b463e6e2f1c7826ead65f`  
		Last Modified: Fri, 14 Nov 2025 01:40:08 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json
