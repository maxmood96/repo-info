## `clojure:temurin-21-lein-trixie-slim`

```console
$ docker pull clojure@sha256:dd11264e5b6e0cb9db60d252d4f23eca4ddeba5903367f1cf40179b70e7da311
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

### `clojure:temurin-21-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e8485d77f5f1fc6e766906b84f0773349a97ee766d9fc4b237c7191d8d600b8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.9 MB (208913338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:568c236d7b900cf37e3cbd2124b0b6e42be32f1d01ecb17b6b6b33eedc83da08`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:21:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:21:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:21:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:21:36 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:21:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:21:36 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:21:53 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:21:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:21:53 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:21:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:21:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:21:55 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:21:55 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b278f77c099c1f3c0a591eb2403d4c67eb53152b80e3dc63636d093e12879f`  
		Last Modified: Fri, 08 May 2026 20:22:16 GMT  
		Size: 158.2 MB (158166903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d207db39721fc21a1725f78127eeaf49f844420f6a11d1cf581d5eb4d2810ea8`  
		Last Modified: Fri, 08 May 2026 20:22:13 GMT  
		Size: 16.4 MB (16448039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df788d40c8eed733286dd9b652db0bae4492046e136dea34e6099fd032bd43f`  
		Last Modified: Fri, 08 May 2026 20:22:12 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bcd047e3503d5994822b5b643c60594fbc2b7bb50a0370d1f33043ba6d3524`  
		Last Modified: Fri, 08 May 2026 20:22:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5d0ce18ee89ac3db209a404acd73188c6e8da61e0efe5eba8a3205d7ae64dc9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67bc74bfceb5f1f242bb971bb815a63464043eb8a508116bd30cf677c8a62ef7`

```dockerfile
```

-	Layers:
	-	`sha256:47d397b2bde257e45305d0e80ee0512f835f2f755486ad6827dea12294b13dc1`  
		Last Modified: Fri, 08 May 2026 20:22:12 GMT  
		Size: 2.4 MB (2367267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4fbe3c3a57c75d9fbf50441899e6f34aef94bd411d8079ac5d61e2d4b0479e9`  
		Last Modified: Fri, 08 May 2026 20:22:12 GMT  
		Size: 18.5 KB (18541 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:47f8e168768692ad10e866943c2208e56451da1fbdc43a31600f06cee1ccd32d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.5 MB (207536845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838c495cdb81299573b35a9f581a30e612e40b999f3461d84e0637ae8fd97318`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:22:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:22:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:22:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:22:30 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:22:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:22:30 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:22:46 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:22:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:22:46 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:22:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:22:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:22:48 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:22:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f468be9e56d2bffc1b12b6ebf37558f5162eb2d608017a6addba0712b7a02b`  
		Last Modified: Fri, 08 May 2026 20:23:08 GMT  
		Size: 156.5 MB (156461131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68dc9e1daafe95206af571e8e6ebb861768c298411b7a34d835b8e08e7861b1d`  
		Last Modified: Fri, 08 May 2026 20:23:05 GMT  
		Size: 16.4 MB (16413926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6298cce60a932fd4c00723efbeffb1b1b6f755724b4ff01ed80f27693de68028`  
		Last Modified: Fri, 08 May 2026 20:23:05 GMT  
		Size: 4.5 MB (4517716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c00f108409a2db9ae428d5c8830fdbf1c9b91f4b8c37c1badcd2f8543b5daea`  
		Last Modified: Fri, 08 May 2026 20:23:04 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5a09aa4abd07c52fd9d918ec067519e382e9c0d7b90e3d6f02cae5b6d345db4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c91bdfbea2edf906c7cbe51667344fc65b9802045093c19758c353a687d4c0`

```dockerfile
```

-	Layers:
	-	`sha256:ae551ec460288048e6ee1907f7105a72cb4bedb6c3f8ebb4aa4c8270a217e48d`  
		Last Modified: Fri, 08 May 2026 20:23:05 GMT  
		Size: 2.4 MB (2366885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3a4ea5fccc629faa6580ff62fead50bcabf58ff67b82703cba84783850fd572`  
		Last Modified: Fri, 08 May 2026 20:23:05 GMT  
		Size: 18.7 KB (18660 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:28574b943b06e5cad80d35a88eef103606aaf7dc061b367003a6e4e61c8202d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.9 MB (212944842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc5f5e790679987c8702e305e538594ba2da651900e83fa699f10c13fa7b82c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:37:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:37:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:37:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:37:56 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 09 May 2026 02:37:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 09 May 2026 02:37:56 GMT
WORKDIR /tmp
# Sat, 09 May 2026 02:38:28 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 09 May 2026 02:38:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 09 May 2026 02:38:28 GMT
ENV LEIN_ROOT=1
# Sat, 09 May 2026 02:38:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 09 May 2026 02:38:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 09 May 2026 02:38:32 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 09 May 2026 02:38:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9429fc219825eaf2a233c26bd84cdc3eef77eb70dd8fad888800a28c7609e2e4`  
		Last Modified: Sat, 09 May 2026 02:39:07 GMT  
		Size: 158.3 MB (158343282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a97f5535a33704a2284317f217669ef9547b72e15c55ad265eed80f9b193ff4`  
		Last Modified: Sat, 09 May 2026 02:39:04 GMT  
		Size: 16.5 MB (16485319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c213aa45eb7fb8f47e57016c8e79ed3cdc0cb2b7e4a785996a07f36fccf85a3`  
		Last Modified: Sat, 09 May 2026 02:39:04 GMT  
		Size: 4.5 MB (4517727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c889bcaf8b826620210f8fd07c82995f5a6c6ba6fa75a6025f853c4963892474`  
		Last Modified: Sat, 09 May 2026 02:39:03 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4c510ce170cfb02c8ce59531e3f46d21eb091781ab609208b7f5273fce18d1da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5fc0282545aaf49725896a0ef7a5fe05a6ea909d305f6c0a87747969c74969f`

```dockerfile
```

-	Layers:
	-	`sha256:fe395f7b15182d58a648dd405f8c4cdbf816a210f2456fe598a44a0fc7cb5fdd`  
		Last Modified: Sat, 09 May 2026 02:39:03 GMT  
		Size: 2.4 MB (2368247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39b594a5fb82830e0abf446e22d70b1baea0f6455cede7c666f11d0a1edfe5e2`  
		Last Modified: Sat, 09 May 2026 02:39:03 GMT  
		Size: 18.6 KB (18585 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:b3e5249c60e1ab16f6739bb1a53dd26dd0a35d1006a9b8036e14b33ed1331fd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.4 MB (206413440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0d94ca7d63dd701d6239946f0c74f9b2414cfc414bdbc515a438aee1acc79c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Fri, 24 Apr 2026 18:16:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 24 Apr 2026 18:16:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 24 Apr 2026 18:16:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2026 18:16:48 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 24 Apr 2026 18:16:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 24 Apr 2026 18:16:49 GMT
WORKDIR /tmp
# Fri, 24 Apr 2026 18:18:22 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 24 Apr 2026 18:18:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 24 Apr 2026 18:18:22 GMT
ENV LEIN_ROOT=1
# Fri, 24 Apr 2026 18:18:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 24 Apr 2026 18:18:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 24 Apr 2026 18:18:37 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 24 Apr 2026 18:18:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad178a1c7448a34e9758387fe35c9fb467bae057770eff7c342592f312ccf326`  
		Last Modified: Fri, 24 Apr 2026 18:22:57 GMT  
		Size: 157.2 MB (157216929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d8d5bb99659ac446823bd986ba7aaebb4359d8245f51a158267b5fb9836090`  
		Last Modified: Fri, 24 Apr 2026 18:22:37 GMT  
		Size: 16.4 MB (16398105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed686f3e67b722a06180ab7dc921dbdb821a832d2dc2c4012668608966f06962`  
		Last Modified: Fri, 24 Apr 2026 18:22:34 GMT  
		Size: 4.5 MB (4517783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdc0929a98b5977e836091e1728431a5f0643531a73781aa0b844f6c5d65d0e`  
		Last Modified: Fri, 24 Apr 2026 18:22:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:83eac27c2435ef3f9fdb5c4e332cdf41674ade244acb58d2447dc86a0c59d7f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2432a564daf558b97d26b1125dae5ebded413b703ab84e590298a095dd1f912`

```dockerfile
```

-	Layers:
	-	`sha256:8ec030d455dfa553e88eea42a437e49c5c78a73cb3a6c354701356e6de9c5a54`  
		Last Modified: Fri, 24 Apr 2026 18:22:33 GMT  
		Size: 2.4 MB (2358688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38d112fb32dff53d527d532d219cc28fa70443c447724962a4b21381e7424af2`  
		Last Modified: Fri, 24 Apr 2026 18:22:32 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:27672dd429abb3cc0c2caf82666c655075ac5cd79d5c2d50420d03eee734ac43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.2 MB (198230750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b335592692bc5fa331c9c613de912187416ea0522c54ebf917c26afa3ce58c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 22:17:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:17:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:17:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:17:44 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 22:17:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 22:17:44 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:17:57 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 22:17:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 22:17:57 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 22:17:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 22:17:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:17:59 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:17:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322bcf3d705f2cea437ef1917f9da7ff28c4e9884b7d8a103b1f9bdb9098e5dd`  
		Last Modified: Fri, 08 May 2026 22:18:28 GMT  
		Size: 147.4 MB (147388345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c776938b94a0ddfc616faad79c42ce66b6119441041dd8639e91541cc84715`  
		Last Modified: Fri, 08 May 2026 22:18:24 GMT  
		Size: 16.5 MB (16483912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cc3875c4956742fd02970c897b3b884ff672b140e34d8d6ffde538d892d8fb`  
		Last Modified: Fri, 08 May 2026 22:18:24 GMT  
		Size: 4.5 MB (4517717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f5282ab9dce70556c7f891ab52706eeff5acf228a7a39ff3aa935dc1880b08`  
		Last Modified: Fri, 08 May 2026 22:18:24 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8bcc636a9009f5033b9d0a2a48be7190d7be81ef08cb41eb85a21c9665ad91b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2382235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d44c1867dc1e86bd942ad75fda9cf82e45c6ed9404fbfbf54bb0d41590eef2`

```dockerfile
```

-	Layers:
	-	`sha256:386ab9818eb0dd91cdfff2f893306ad5fa1455bb51411a1b7ca44d05591743f8`  
		Last Modified: Fri, 08 May 2026 22:18:24 GMT  
		Size: 2.4 MB (2363694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65f69438fbb24e5998751a0b1117377a180ec58ab6294144712a72f84940a40f`  
		Last Modified: Fri, 08 May 2026 22:18:24 GMT  
		Size: 18.5 KB (18541 bytes)  
		MIME: application/vnd.in-toto+json
