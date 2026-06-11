## `clojure:temurin-17-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:e51c81a008b5deb10f60192b684381d2d4cf49ff37b08c0c3a40980e1e7e0899
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
$ docker pull clojure@sha256:1ac68808498d4b48c015cc9e3b0f650d12b5817e27e03ebc6a2755ad45f61603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.3 MB (200323373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76daa01cc459e6ec11e96b80d648105a52b4226c04410a35e4d387994692c2c5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 05:54:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 05:54:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 05:54:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 05:54:25 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 20 May 2026 05:54:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 05:54:25 GMT
WORKDIR /tmp
# Wed, 20 May 2026 05:54:53 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 05:54:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 05:54:53 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 05:54:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 05:54:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 05:54:57 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 05:54:57 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:562cecbb5aa529d280e58ef1f95f14cdcd37a90c5ea9181798a78377e934e6e7`  
		Last Modified: Tue, 19 May 2026 22:35:14 GMT  
		Size: 32.1 MB (32075742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6633021a99f451d585b657cbca0d3fbc241ffb487dcadb3e2ad6afd10c777642`  
		Last Modified: Wed, 20 May 2026 05:55:35 GMT  
		Size: 145.8 MB (145766094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235dc93bf338b8a2fa1703b28351190a08d373b4c5230e123bff8e25b092f8d1`  
		Last Modified: Wed, 20 May 2026 05:55:32 GMT  
		Size: 18.0 MB (17963351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084a80655d3522c46078131406f30839be6fedb688a9c68f0db0c993d0506f43`  
		Last Modified: Wed, 20 May 2026 05:55:31 GMT  
		Size: 4.5 MB (4517758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a7fe2d7f58494436ad08661d2a5fa3481c7fd74b0df195dbddd606a0c8dcba`  
		Last Modified: Wed, 20 May 2026 05:55:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5078660531e646d82a4cefabf835268de594bb8cb8942f0f8e31adbcdcb919c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2751129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32bcbf9f584e2e2169163041b57e72882304e705c5437d1096c4c2182aaa659e`

```dockerfile
```

-	Layers:
	-	`sha256:a69cdefc45130805cae1827d300758450a630e48d9f4a0b62f0a530d1a4c07df`  
		Last Modified: Wed, 20 May 2026 05:55:31 GMT  
		Size: 2.7 MB (2732528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7eee6b2b063a2eb23ca152faa06566a28b91fd9b1802c7b1e33beb488a307f70`  
		Last Modified: Wed, 20 May 2026 05:55:31 GMT  
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
