## `clojure:temurin-25-lein-trixie-slim`

```console
$ docker pull clojure@sha256:f6f28154092daaf8dd90c008d0e71e1f631ce1b26c83cc15315dc88e7af9cdfc
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

### `clojure:temurin-25-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1c97ce2df71fd8c438ef85ff4c911dfd4b3addfade6ca45137c0762fccbb1535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142784428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2743853fbb0c0c8dfa97a39f602477986d22676e9d61890ab7647d1278a2b58a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:39:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:39:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:39:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:39:04 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:39:04 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:39:04 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:39:19 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:39:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:39:19 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:39:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:39:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:39:21 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:39:21 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e622cfd90ee4f20468128734003e4bfbfacce9a9dc146058e5686c530ec21d96`  
		Last Modified: Tue, 13 Jan 2026 03:39:54 GMT  
		Size: 92.0 MB (92045295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbd7f5dedaf43232a8ae5aa3438a3e10521846b9f26d4d506223508709cc95c`  
		Last Modified: Tue, 13 Jan 2026 03:39:46 GMT  
		Size: 16.4 MB (16447284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5537515b8f730fd7ae47c35d26637b0c8714b211da44ceea6936e5b9c3c4fb`  
		Last Modified: Tue, 13 Jan 2026 17:25:44 GMT  
		Size: 4.5 MB (4517737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3b9a4f089d6756e1f63380f94b9d588e3f25d82caa106f409174911fd66949`  
		Last Modified: Tue, 13 Jan 2026 03:39:44 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cfaf2dfeb07e0b6f15c0699fd444dbbfe40240e1d037a35ff8c4fc261ef8be8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c5d6b4cdab7065dc08b3f161f32dfa6be377d92aeda90177cafbcf4d238b211`

```dockerfile
```

-	Layers:
	-	`sha256:4b4f5721bf10d6353d041b8f3c98cea0862eef5a3e49f6485ef3e69b550eba1b`  
		Last Modified: Tue, 13 Jan 2026 07:36:05 GMT  
		Size: 2.3 MB (2314816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952a27c5a2efbbf343e2f86ce245d5571e1d50cc8d76e0606fe2cd8e0401613f`  
		Last Modified: Tue, 13 Jan 2026 07:36:06 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:02c718965aac3b630bd2cf24e73f7b44696654888c3f28e4a69d7626e7bf4918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142118652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daa9f311845d28a918420c9f01122aea22544b19409c6970711a2034de174a1b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:42:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:42:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:42:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:42:41 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 03:42:41 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 03:42:41 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:42:57 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 03:42:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 03:42:57 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 03:43:00 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 03:43:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:43:00 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:43:00 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc013bb09d937e72ce85390e91dd0612e3cfe341d79f34a1abd420f7b877e64`  
		Last Modified: Tue, 13 Jan 2026 03:43:34 GMT  
		Size: 91.1 MB (91052514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff1d088c53cfd5ac4bd494b0af31870149fc209e41f9bb8521e4f54694511e4`  
		Last Modified: Tue, 13 Jan 2026 03:43:29 GMT  
		Size: 16.4 MB (16413956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926b893bf265422e4fd43a4a6e1309f0d7f4328ce93cd9a049afdd610ada8b2d`  
		Last Modified: Tue, 13 Jan 2026 03:43:26 GMT  
		Size: 4.5 MB (4517711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af755647c4c7b7faf6f44e2ec63345ef69743d952a697e61b74047233afe44ef`  
		Last Modified: Tue, 13 Jan 2026 03:43:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7bd29cec4fd529ab4633219ce8de98181ebdc5231cea185b3b380f21f1f1a67b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51fb3de59c5e4b02107e1c31eda3779cd3584746228ef214efd9360b04538181`

```dockerfile
```

-	Layers:
	-	`sha256:0a64edb1cda6688581fd8657316ebe32e0ab6101eb4cb3888466fcf95186404c`  
		Last Modified: Tue, 13 Jan 2026 07:36:10 GMT  
		Size: 2.3 MB (2314455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:611a665fca06c9d3c5cf2de2eb7e46dca31aa478ff4fc869d3f5f920dc9becab`  
		Last Modified: Tue, 13 Jan 2026 07:36:11 GMT  
		Size: 19.2 KB (19179 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:886dbc45fd7d3ceb884ab4f03da236b875d2d8fcac56a92477d8fb95e64065dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146210047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8fea6432dfcf33a10c7fe8dda9bc02b24f8ac3f43f4cc2eb0aaca1c89db88d7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 05:50:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 05:50:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 05:50:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 05:50:41 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 13 Jan 2026 05:50:41 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Jan 2026 05:50:42 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 05:51:33 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 Jan 2026 05:51:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Jan 2026 05:51:33 GMT
ENV LEIN_ROOT=1
# Tue, 13 Jan 2026 05:51:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 Jan 2026 05:51:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 05:51:38 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 05:51:38 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:13 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c0cb0513db188945a72749dd6a780b91b0fa6d24c747bb4737feab787c2e02`  
		Last Modified: Tue, 13 Jan 2026 05:52:32 GMT  
		Size: 91.6 MB (91610788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3586f7cbb5c5764fa9f14b0e5e26106beb6e82861f9d1037765391386c7396ce`  
		Last Modified: Tue, 13 Jan 2026 05:52:26 GMT  
		Size: 16.5 MB (16485462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493f6012a9f708aab71b078f8ed7ced57b38ae8d37b9c9928859eca5753c11c1`  
		Last Modified: Tue, 13 Jan 2026 05:52:25 GMT  
		Size: 4.5 MB (4517768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58bbf5fc69289b7bc97d9ceb09578ef3b29e006203f91be9e54ca56e7c71e51`  
		Last Modified: Tue, 13 Jan 2026 05:52:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ed958a13219d39a53d7a9d1a54c503089879b2ba5ae709db66a05fe0f1ae9876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2336196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21e08d2f0f2a1facc4d3ce8452a5330f24f794f6d038263692e666c6d14410b`

```dockerfile
```

-	Layers:
	-	`sha256:fddf40dbebeeaab02501eeebe14dc6af3920d7b69ed1bddbec93bf41b8d451ca`  
		Last Modified: Tue, 13 Jan 2026 07:36:37 GMT  
		Size: 2.3 MB (2317106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:496d5bd99720961c2ea92a6de0337f7fb4f8b3e035bc64e2bcb03dae7c504e6c`  
		Last Modified: Tue, 13 Jan 2026 07:36:37 GMT  
		Size: 19.1 KB (19090 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:98bd97f7da94b04c70f5c690248c396909864aaec16cf66e3cda8180b7a537c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139942042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0f956d62f96f6c2d1fc7720a5d66542029874f5988cfbd59c269b0bb5c8d142`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Thu, 01 Jan 2026 07:30:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jan 2026 07:30:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 01 Jan 2026 07:30:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jan 2026 07:30:35 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 01 Jan 2026 07:30:35 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 01 Jan 2026 07:30:35 GMT
WORKDIR /tmp
# Thu, 01 Jan 2026 07:32:04 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 01 Jan 2026 07:32:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 01 Jan 2026 07:32:04 GMT
ENV LEIN_ROOT=1
# Thu, 01 Jan 2026 07:32:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 01 Jan 2026 07:32:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 01 Jan 2026 07:32:21 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Jan 2026 07:32:21 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a09886da888ac7f39c6c9f60f721941a5a3cc3ed273e4d20352388b50fb5af`  
		Last Modified: Thu, 01 Jan 2026 07:36:11 GMT  
		Size: 90.8 MB (90752859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4809340366dabeee7446bfef1c9430edd6aced6075aa4c14861cdb274ae8b082`  
		Last Modified: Thu, 01 Jan 2026 07:36:01 GMT  
		Size: 16.4 MB (16397836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483da57381707f5798e42be6df179f839c90ea4b2f6c6e7c680e238d5ac7f920`  
		Last Modified: Thu, 01 Jan 2026 07:36:01 GMT  
		Size: 4.5 MB (4517788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b22dcbdce2eb2b0ce5e249fb8a0bd633ba430ee21fcbe4930530bbdbbf8797`  
		Last Modified: Thu, 01 Jan 2026 07:36:00 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9d9867ffb5eefb293d9df5f02d9d933702431d7a48fa8d9e6b942656429d79d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2325901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375be7215430e83b634b548dab69a401386d0acd9741d530e4c87047dc276285`

```dockerfile
```

-	Layers:
	-	`sha256:95ad62ba696e7ed6b7f904e40f0cec1913376b2bd8da9a29c2c5033bba16aef7`  
		Last Modified: Thu, 01 Jan 2026 10:35:08 GMT  
		Size: 2.3 MB (2306811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c250f59a91d6e671e1acd6d5d3b283c04a8d5528acba645a7704bc27fed7f74`  
		Last Modified: Thu, 01 Jan 2026 10:35:08 GMT  
		Size: 19.1 KB (19090 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:253703d5c9373cf3b91b49b5d9a0c0a2e9913b8ba4236595ea973dc1c244a196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139045356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ce53171cc49e272907126812140caa0417ba57b838269401cfe5086c38e29a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Thu, 15 Jan 2026 23:23:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:23:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:23:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:23:10 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 15 Jan 2026 23:23:10 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 15 Jan 2026 23:23:10 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:23:23 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 15 Jan 2026 23:23:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 15 Jan 2026 23:23:23 GMT
ENV LEIN_ROOT=1
# Thu, 15 Jan 2026 23:23:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 15 Jan 2026 23:23:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 15 Jan 2026 23:23:25 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 15 Jan 2026 23:23:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:43 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2b60cbc839537ac9d2d64e95bf99e1c19c3b75f06175e544fbfafc8cc5fea1`  
		Last Modified: Thu, 15 Jan 2026 23:24:08 GMT  
		Size: 88.2 MB (88210671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181ce5dfe9b484262a7d1f2d45a10d603a7e14f778b0f8a489988dd4ce969fad`  
		Last Modified: Thu, 15 Jan 2026 23:24:00 GMT  
		Size: 16.5 MB (16483100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee5d985dfd304bb5400ddfd11aad3324665d74ecb4ed4d0869aeff9c74bd7d0`  
		Last Modified: Thu, 15 Jan 2026 23:23:59 GMT  
		Size: 4.5 MB (4517745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ce7eddd94e5026e0958fcaa0ab9176e5eda37cac5892f32612ae81c227d5a1`  
		Last Modified: Thu, 15 Jan 2026 23:23:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:28fd4627b2b2576563b1e193e162c2d925fb850bc50927ac5fbdd56d242c6670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2332825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3366679e4c9a570b8896e6ac7411f4ba9ffa8454b161a3f36ec211425481fdfc`

```dockerfile
```

-	Layers:
	-	`sha256:773cbf54d3740f71f4006fde4dc4e34b741c366fde6351013464189f0e00851b`  
		Last Modified: Fri, 16 Jan 2026 01:36:24 GMT  
		Size: 2.3 MB (2313791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14f7230f5a07c1db1f981ab8137b84204c20ec470687f1cc244298f0c620637d`  
		Last Modified: Fri, 16 Jan 2026 01:36:25 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json
