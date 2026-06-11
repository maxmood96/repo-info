## `clojure:temurin-17-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:2fe826ea3532324e2959ad0ea7da3481d51de4224d7353f00dbb9e3021ed86d4
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

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:681ce08314a9dccd6e18a834fb5b979e77d537c79d2c69fbd602cc43cef3b162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.4 MB (196421325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59321a85abd1855beb02d87995561cae75ae93342087cdace8482408e089b2c3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:18:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:18:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:18:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:18:26 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:18:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:18:26 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:18:39 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:18:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:18:39 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:18:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:18:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:18:41 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:18:41 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d5998215e0ebfa78e795096878429b19f2f6136419db89cd07d4b516f8c08a`  
		Last Modified: Thu, 11 Jun 2026 01:19:01 GMT  
		Size: 145.9 MB (145905480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3396282d7bb0587f007e01112ff9a9af9b2a07a7c78a4b9bc8dd5f20dcf9af4`  
		Last Modified: Thu, 11 Jun 2026 01:18:58 GMT  
		Size: 17.8 MB (17760066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6581f6b9d7406fa7aa95bce053fec5e9b4cf642a53959ef767c50c2aafe73696`  
		Last Modified: Thu, 11 Jun 2026 01:18:57 GMT  
		Size: 4.5 MB (4517727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b0ed013085a02dcbb88bf42e70ed138644f92a46c2f87d22fd977860a9f590`  
		Last Modified: Thu, 11 Jun 2026 01:18:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5fd452ec338919ae307fc5d9b9e8d2c6ced337c7a93ae08b7d192c18eb067127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2749269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f16e483449af228ff6bcc67fee3fe750929ac684e36378e42383ff6fdafe49c`

```dockerfile
```

-	Layers:
	-	`sha256:38ed7ad7ae23c8b1c1761b9057a4df6b5ca4cd7bb724539d1107c0fa0efc9109`  
		Last Modified: Thu, 11 Jun 2026 01:18:57 GMT  
		Size: 2.7 MB (2730713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5f648cc8bcc011baa1977fc893e13364b2b4c389ececdb86e756874e9e75e82`  
		Last Modified: Thu, 11 Jun 2026 01:18:57 GMT  
		Size: 18.6 KB (18556 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a00c67f3cc5e979932eda41b266b341278c5455768ec6fb703976fa3fced7829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.0 MB (194958873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:433f57ee7e602ad74ac138f30f3108c3e107b40fdd9c2a5d0d0860c35b35f001`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:22:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:22:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:22:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:22:16 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:22:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:22:16 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:22:28 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:22:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:22:28 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:22:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:22:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:22:30 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:22:30 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34665481baf21942daa410f35caea1e50a728d40d3ec04d21a949112ea196d5a`  
		Last Modified: Thu, 11 Jun 2026 01:22:51 GMT  
		Size: 144.7 MB (144724360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3a5eb48d54941b89b0cf8a44ad0ff257c806d32f31e76fdb7003387cf142fd`  
		Last Modified: Thu, 11 Jun 2026 01:22:46 GMT  
		Size: 17.6 MB (17594018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05830c6a7ba1e0471de710d20644f5f61d5b12adfa685df4b8c986bbf6f5caeb`  
		Last Modified: Thu, 11 Jun 2026 01:22:46 GMT  
		Size: 4.5 MB (4517761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1429e13ce7bebd80b740f82145b641eac47be668f2539768df36f53a5f53ad`  
		Last Modified: Thu, 11 Jun 2026 01:22:45 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:16c3a6cc1a62365b520b4684c255b3015a215adedb60e46ea921b479718037da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2749004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f0682c9f7bbf45ea5888bda5af76b97a6620aa008ae0f3def2e8bb7a68d8a0`

```dockerfile
```

-	Layers:
	-	`sha256:8a74e11231c15b55a05ecefe10f0a87cd1bd5f4979aa95e1eff00b60fd2b4968`  
		Last Modified: Thu, 11 Jun 2026 01:22:46 GMT  
		Size: 2.7 MB (2730328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eee49afb991cf4033155fa49262cd68d25581ceeddc181a518c1cdc920ffcbf7`  
		Last Modified: Thu, 11 Jun 2026 01:22:46 GMT  
		Size: 18.7 KB (18676 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:7d4a05a5d57e0e5a4aec0280bb0c8e9d55c8f264a5bb9a0c5384bc24b9269149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.3 MB (200329946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97141e3215f9251718f8c4270ad5a2349bb306ec2cd7073df50836eacbc15c48`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 09:29:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 09:29:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 09:29:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 09:29:22 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 09:29:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 09:29:27 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 09:30:03 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 09:30:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 09:30:03 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 09:30:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 09:30:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 09:30:09 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 09:30:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bab2c1eb2f066d3ff6bab086dbc5fafbc50c746db8da2cc3d2b22fadc81c442`  
		Last Modified: Thu, 11 Jun 2026 09:30:52 GMT  
		Size: 145.8 MB (145766120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3006d96eea0d654b464dce29cf23356b30b601e61f848b463ff4a7416dae3a`  
		Last Modified: Thu, 11 Jun 2026 09:30:48 GMT  
		Size: 18.0 MB (17963689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96c2e121303454ee1b663ca9e37b8ad980eafebf12397c780c7353844bddd57`  
		Last Modified: Thu, 11 Jun 2026 09:30:47 GMT  
		Size: 4.5 MB (4517765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03da98766f4ccd9a7f85ead2372931d9ad2d5ff19b5270d3cd06b7b757af7120`  
		Last Modified: Thu, 11 Jun 2026 09:30:47 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4045ef35975a2af45cf0851896bdc94a4e4ab81aeb04615ca1260e38549ab917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2751147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a30291d02f2bbc5f284d2eb8f71ab7579b0c3c6abeb69613afdb2891cebc2049`

```dockerfile
```

-	Layers:
	-	`sha256:9736a4461e6a7e9ce977c46a89220905a42bc5796fa6bca268357c623117da0f`  
		Last Modified: Thu, 11 Jun 2026 09:30:47 GMT  
		Size: 2.7 MB (2732546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:111ec8aaedf48806dfb7901c20e1cabf2ba5599fb69a707afa890b55ae7fc551`  
		Last Modified: Thu, 11 Jun 2026 09:30:47 GMT  
		Size: 18.6 KB (18601 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:5c5d96a9fd12b7d6db8faa8523d631e6c55951814ce81c655a32ef2fa14c7ba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184746145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23412db5bda998b65234ab7759bf08895a95e5979fe030d315c3c0947eedcb7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 03:08:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:08:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:08:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:08:53 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 03:08:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 03:08:53 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:09:04 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 03:09:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 03:09:04 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 03:09:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 03:09:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 03:09:06 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 03:09:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0df9523820e83a5b63feeb7f96fdbb885f9dae313fed2f41bfabf8b2e65e98c`  
		Last Modified: Thu, 11 Jun 2026 03:09:36 GMT  
		Size: 135.9 MB (135910407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17320c3114a231c3f5d13381f734314169f66775046ef9e7c3b98c567bf643bd`  
		Last Modified: Thu, 11 Jun 2026 03:09:32 GMT  
		Size: 17.4 MB (17424058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbc1aab060cd0da85f38c6bb19d9aef709854c4c8d1374b19def7fea84c498f`  
		Last Modified: Thu, 11 Jun 2026 03:09:30 GMT  
		Size: 4.5 MB (4517745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efa8960691352496df2159c7359f5ade404b8e502a09d2e93c926f2064a8b81`  
		Last Modified: Thu, 11 Jun 2026 03:09:32 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2d1f9929dcf26cda3d0e3e07af04961568f12353d6e62609e5fbb078ecc21208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2741084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5357e98d608c4a2def5c83eca9882e5fc58819824a4d719ed160ec65fefc61f`

```dockerfile
```

-	Layers:
	-	`sha256:7d12021c67dcae6942429ff8f3062544315e6a34cd92e63c8caf0e92d53b8a44`  
		Last Modified: Thu, 11 Jun 2026 03:09:32 GMT  
		Size: 2.7 MB (2722527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49ec3f68d2c26feb4d95c90722201a14337553c1eba679c3f7d79249b9800365`  
		Last Modified: Thu, 11 Jun 2026 03:09:32 GMT  
		Size: 18.6 KB (18557 bytes)  
		MIME: application/vnd.in-toto+json
