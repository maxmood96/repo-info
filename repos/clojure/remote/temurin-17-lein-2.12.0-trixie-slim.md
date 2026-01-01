## `clojure:temurin-17-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:aa12c02dabebaa27825dc563627528913ef9d577c9b5ae573935940a37e204bc
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

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c75be7ff12ca1fee1d375dd232753112e13d664bf8c2178c16a1a4af7535b5a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195589792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2daf7d4398bff6f62190f1b25195a6502f075934c4953a5f60e95fc63a3717d8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:58:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:58:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:58:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:58:54 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 00:58:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 00:58:54 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 00:59:09 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 00:59:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 00:59:09 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 00:59:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 00:59:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 00:59:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 00:59:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c1901db754e37b643a39343cb8305dcff5e821ece8bb233169a441355fe228`  
		Last Modified: Tue, 30 Dec 2025 00:59:44 GMT  
		Size: 144.8 MB (144847922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538a78911604f7f44d170ab5095c2b15d69de16d377ff4d62fbf96037235fa0a`  
		Last Modified: Tue, 30 Dec 2025 00:59:38 GMT  
		Size: 16.4 MB (16447149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22430c022410a34ef0161efa61f7a579ce0e0cf9146931390dee8c5e58b75f1`  
		Last Modified: Tue, 30 Dec 2025 00:59:37 GMT  
		Size: 4.5 MB (4517760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4ec031994d94bc5c3069915b22be85e44ad46ed79ac865aa5855578ddd4a56`  
		Last Modified: Tue, 30 Dec 2025 00:59:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ff30d66abf1f95857af88ebce075396f32f67c73983e89f6e8710e4e57c76be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4868cce201d73e30c663c059e084d917f81e4e700036592e1abc3882e3b2b79`

```dockerfile
```

-	Layers:
	-	`sha256:34004b8c30fa218d54a22f16702e8b45d28cfd18b4e8a88efc4e9863564b1f88`  
		Last Modified: Tue, 30 Dec 2025 04:41:08 GMT  
		Size: 2.4 MB (2363438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0341084a88e79da032b37be5281950da7038fef246c9a08daa87bfc3e408d388`  
		Last Modified: Tue, 30 Dec 2025 04:41:09 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:34b8981fe3241e61b4c892100d7574740256f611596c5e0f9c36e09243a30401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194750536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bffe5d9e1dcba15dae90ee57c7ffe06e26073ce0cc6a7f6048029c9ca4064f86`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:59:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 00:59:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 00:59:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 00:59:55 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 00:59:55 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 00:59:55 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:00:12 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 01:00:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 01:00:12 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 01:00:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 01:00:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:00:13 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:00:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6333fb1275e3fcff1ec232f69ef464a04bf3ed28f6d6cc1b884d8e694326cd32`  
		Last Modified: Tue, 30 Dec 2025 01:00:50 GMT  
		Size: 143.7 MB (143679913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a48fe27cc6e1249cf6200c692938223502cb7dc88c1ccfb3df19b6bfff424d`  
		Last Modified: Tue, 30 Dec 2025 01:00:44 GMT  
		Size: 16.4 MB (16413844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1d408e15c8ad48723f63de19e6b7b82fa06dd5b6904e0b45971a5307673e8a`  
		Last Modified: Tue, 30 Dec 2025 01:00:42 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a35a0eef0509f8eaf90b95cb353e52b948322887b53cda6c67ab0d4c4f6be5`  
		Last Modified: Tue, 30 Dec 2025 01:00:42 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e148d000bc7cb19a72b98ec135ac0eb5f25ab8c8594d9cc86752d59216593dfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e87d167444e9823687dfe405c065fcbcacec0f4d6a6a83c23e95f31fa585dde`

```dockerfile
```

-	Layers:
	-	`sha256:31c0fe271969de779dc76df2670286349cdc78e2506a97c2edc731a32fcfebb9`  
		Last Modified: Tue, 30 Dec 2025 04:41:12 GMT  
		Size: 2.4 MB (2363056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdb31dffd972f0def56b5da4c17f58937c20aa0fac134434257ae2dd2c0b06cf`  
		Last Modified: Tue, 30 Dec 2025 04:41:13 GMT  
		Size: 18.5 KB (18508 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:fb9b454f02671e9960763f380e89197754a16d8c5a7423e311dac1f50b3bd31f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199125490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12277c7fae21a5199b179cf4faaf7aa3c6e4b6e635beecf595718150ad32af90`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 19:10:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 19:10:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 19:10:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 19:10:02 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 19:10:02 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 19:10:03 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 19:10:42 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 19:10:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 19:10:42 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 19:10:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 19:10:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 19:10:45 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 19:10:45 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:34b56ab3c5579c93222f3403d640c7a7f19044e9e46a2d1c6b1da60bde918efc`  
		Last Modified: Tue, 30 Dec 2025 15:11:02 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6e459b5cb1f7cbeb835d5f2c62bfb93c7f279db102bb5edccff8d14681becf`  
		Last Modified: Tue, 30 Dec 2025 19:11:58 GMT  
		Size: 144.5 MB (144525219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cee6998f71c8da637094e8d0c2880dff8d40a2d85ee8976691b8cd33adcdfe1`  
		Last Modified: Tue, 30 Dec 2025 19:11:46 GMT  
		Size: 16.5 MB (16485225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8b65bb5e88c752adbfd79aa1b3bc32b8cb075ec70be7824acd10dffc6c17d2`  
		Last Modified: Tue, 30 Dec 2025 19:11:45 GMT  
		Size: 4.5 MB (4517726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52711a743baf894f2dc9d33fff16c08af9db7045a58678b7563e4acaeb2e654f`  
		Last Modified: Tue, 30 Dec 2025 19:11:44 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:da14ff8738295c198e7f6e06bd6bd928d48a3f16446cb8ec0e1607d69dbd95c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2382849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f338c4068d91825e7c52272f7d5812f6538bc06a733676530b96f27c245a1b68`

```dockerfile
```

-	Layers:
	-	`sha256:d58be8aa117aff5c0dee57e1df3f5e6c56562bb4f0fe918a6a671a44d0918bdf`  
		Last Modified: Tue, 30 Dec 2025 22:35:43 GMT  
		Size: 2.4 MB (2364418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:852020d51294842ab876214d3d493099abd6c3abc70da9d0fa00a4375c817a74`  
		Last Modified: Tue, 30 Dec 2025 22:35:43 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:732b9223d2291e0de32f48226ad671d6946075752deeeca7966a0cd8b0103b96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191078794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcdc8bb0df493078b042e21029b6fb9f37f4a49555b4bd39b8cbe96f550ad86e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Thu, 01 Jan 2026 06:35:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jan 2026 06:35:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 01 Jan 2026 06:35:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jan 2026 06:35:03 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 01 Jan 2026 06:35:03 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 01 Jan 2026 06:35:03 GMT
WORKDIR /tmp
# Thu, 01 Jan 2026 06:36:32 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 01 Jan 2026 06:36:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 01 Jan 2026 06:36:32 GMT
ENV LEIN_ROOT=1
# Thu, 01 Jan 2026 06:36:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 01 Jan 2026 06:36:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 01 Jan 2026 06:36:48 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Jan 2026 06:36:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c47e4b223479384cb91259f631c9c203246ef873e850a7fe5e6ff70d31329ee`  
		Last Modified: Thu, 01 Jan 2026 06:41:38 GMT  
		Size: 141.9 MB (141889571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0591ee09b2863914415e637a3ba7b7d5114b6a4955e460a07d0fc4a3b9f3b360`  
		Last Modified: Thu, 01 Jan 2026 06:40:56 GMT  
		Size: 16.4 MB (16397866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e85171745efb01db392846d6e6fe56b52bbd6d7b8211054c36949ed33e16378`  
		Last Modified: Thu, 01 Jan 2026 06:40:55 GMT  
		Size: 4.5 MB (4517798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8eb6db56aae90e171960e18f1ec188bddeb42891a4711e3a1673403d8a7c4c`  
		Last Modified: Thu, 01 Jan 2026 06:40:55 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:43147db8897a1a1a8c249abc857ebc749a9d8486097f91bac06d2d211816a1da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2371998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad40619b0a0b68b799348bda9a8ab86df25a589c1ff2954411ee323bcdc9419d`

```dockerfile
```

-	Layers:
	-	`sha256:fe3b9be83ee0fdfd0a259ea3ac25871303bc85b5e9c10a7855061dd5472b7026`  
		Last Modified: Thu, 01 Jan 2026 07:35:29 GMT  
		Size: 2.4 MB (2353567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf800a7f03af0c78d4b017177f43ff2fd942884f7c790896d079f6e09582884a`  
		Last Modified: Thu, 01 Jan 2026 07:35:30 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:66773a9fcfa3dfa73801b615a3411371a1d0630c44af81100b9e78e49c29682c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.7 MB (185694618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19b48a07d72c81cb78da63baaa5a873b3bc877b576cff581143c25856e2ae76b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 02:02:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 02:02:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 02:02:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 02:02:49 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 30 Dec 2025 02:02:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 30 Dec 2025 02:02:49 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 02:03:02 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 30 Dec 2025 02:03:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 30 Dec 2025 02:03:02 GMT
ENV LEIN_ROOT=1
# Tue, 30 Dec 2025 02:03:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 30 Dec 2025 02:03:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 02:03:04 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 02:03:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d897bdc1fa613e96ab09f619b299b82896bea52ad484e0bad5fc9aba413ed88c`  
		Last Modified: Tue, 30 Dec 2025 02:04:01 GMT  
		Size: 134.9 MB (134859069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2545f476809a0307f0d561da4aa7362ade1d2eaa252f08d51e1fe218834eacb6`  
		Last Modified: Tue, 30 Dec 2025 02:03:38 GMT  
		Size: 16.5 MB (16482960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351fa2187a60abfd75ae772d1ccda43366dbea7fde9147d5307d5628cb606acd`  
		Last Modified: Tue, 30 Dec 2025 02:03:36 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd60a1c88777c1402e93f0f3f113a67f47911fb5d8d65bb0a99c208952366c90`  
		Last Modified: Tue, 30 Dec 2025 02:03:36 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:265a804d3d627aaa60a01ad008a62b374702a04609a4bb9dad6db7f21131a8bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2378252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dbc8523a093c9fbb01d16ef0bc06bc074cee745dcbe171858d32fd604ea3d41`

```dockerfile
```

-	Layers:
	-	`sha256:cde79fc43086919b6cb5ec784d07d5b05e8b1b835c4eca9cfd690fa02ac6665a`  
		Last Modified: Tue, 30 Dec 2025 04:41:22 GMT  
		Size: 2.4 MB (2359865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51c6ecafb26dca0d35c7dd0a5848aadfd7d1a45990969d971bf08b2e412e57f5`  
		Last Modified: Tue, 30 Dec 2025 04:41:23 GMT  
		Size: 18.4 KB (18387 bytes)  
		MIME: application/vnd.in-toto+json
