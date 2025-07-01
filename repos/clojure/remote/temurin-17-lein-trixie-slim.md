## `clojure:temurin-17-lein-trixie-slim`

```console
$ docker pull clojure@sha256:cae4fc5b1f5b19770ad839040e4f5e9706960323eddb7415048abc479647091e
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

### `clojure:temurin-17-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:50fddf465e6aea7035fbe3e0189c2e4295f940c6ff87696e7542ae8c024c7451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232806864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80407fbc5811c93b974b16c46d9854fc7907967952ba1b72dcb89214bd9b5bcd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f7f88c6d7f710176d487a3ac59c7790f981832a06bfc197dbe4a74d73b1407b7`  
		Last Modified: Tue, 01 Jul 2025 01:14:56 GMT  
		Size: 29.8 MB (29761106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d752d463e78837347a43a28dca75a279e1210908e82f23e65801c5f397f078d0`  
		Last Modified: Tue, 01 Jul 2025 02:39:19 GMT  
		Size: 144.6 MB (144634963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a5683ebb5071c4b6ce3bdd4e020efb9013f98964363ff3ac0ed00920eb38c5`  
		Last Modified: Tue, 01 Jul 2025 02:39:36 GMT  
		Size: 53.9 MB (53896176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be00927380b0fb9b9f877e3eb2345a2079753c53da643d7db9d2b4e2bd8f97f0`  
		Last Modified: Tue, 01 Jul 2025 02:39:32 GMT  
		Size: 4.5 MB (4514191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2d8996eb7e4bc0b6e45820d044c801c57d0220756896963e4aad7a6cfe07a7`  
		Last Modified: Tue, 01 Jul 2025 02:39:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b5cc805fd091417137c36385a833424ca0a8f644b9228b6c3a83297aedc41fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4295903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f0306ad3655217bee74334a483ebff33f25fe3d7ac8b74b7fbab7a0f3c1843`

```dockerfile
```

-	Layers:
	-	`sha256:1c929676461ad3673f9b4c98ce577213cf5b0d458b515cc7dc884dfcbc25b49d`  
		Last Modified: Tue, 01 Jul 2025 06:37:44 GMT  
		Size: 4.3 MB (4277466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:448b5a303fbeb31953bfef07d3bc6152393edf2f22a23b541f29f295b7472c18`  
		Last Modified: Tue, 01 Jul 2025 06:37:45 GMT  
		Size: 18.4 KB (18437 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:780ef4fe336a0619d584e6cce9f9b8ad95a49d02e6007c870dd0f84bde2b2d77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (232015375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e64479a1dec7f97e8d689909413be4d8d80ca47723ab9a8e100e35d3cd526171`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c3306e90503bf56d5d575fca0323e4953fc66cffec788094159d11570a81151f`  
		Last Modified: Tue, 10 Jun 2025 22:53:04 GMT  
		Size: 30.1 MB (30121041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814f7774d0b60cf22bdadcce74d94c3fcb5808f2d71325882a1282b787e889c7`  
		Last Modified: Sat, 14 Jun 2025 08:36:52 GMT  
		Size: 143.5 MB (143512634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd40c6bf6b26a219f8eefead4a8a396d6b9071bb3d6eaf09a5118e3e6652881f`  
		Last Modified: Wed, 11 Jun 2025 08:29:05 GMT  
		Size: 53.9 MB (53867061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9edfe713922bdbb0283cb0c6e230c6a029ff3b19f88cdded9aa575d38c4dae6`  
		Last Modified: Wed, 11 Jun 2025 08:28:52 GMT  
		Size: 4.5 MB (4514208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46ab77b9c1421ee08b6ed4040a796d18084080abe024ed7b52b96bcccb14c58`  
		Last Modified: Wed, 11 Jun 2025 08:28:50 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3325e49a91e91eb73ad9ac24be4fae294866143d2d59db456f3e8bd75a5541f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4301723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c223666f2c4a243eeb3e6761a83b184bfcd1e0670a22482a4e108d8d91f1490`

```dockerfile
```

-	Layers:
	-	`sha256:862ce661f9d3bf98ba36793345a0039ec9b44d04ca6409a7fe7b7a3fc92a11ae`  
		Last Modified: Wed, 11 Jun 2025 09:38:15 GMT  
		Size: 4.3 MB (4283164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5ea1fcdd7f7352c47c4816f4c0ffb5bd4508744b882ee39084c793a856322ac`  
		Last Modified: Wed, 11 Jun 2025 09:38:16 GMT  
		Size: 18.6 KB (18559 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:82d9aa202f704d0c234fa7823913bef3e7c8a6f8d7ca445d4a021078275872e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.3 MB (241263495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60c773e9aa3dbd2884bce8c7f4a5fccef6af3af6e820bd2131ed63a1debb4d8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2adebcab7d76ecb14ead3f70af8ca34e5abca513c2fcbd9f40e3af1e18442ccc`  
		Last Modified: Tue, 01 Jul 2025 01:19:23 GMT  
		Size: 33.6 MB (33586035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7c76c33e89d8d234c685147ef17003512fb41891617f72e9998041e1838c54`  
		Last Modified: Tue, 01 Jul 2025 08:47:41 GMT  
		Size: 144.3 MB (144280554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:731ae0687b197da26b3724ad1658a7e7be25137f365f3ec610193fa37626846b`  
		Last Modified: Tue, 01 Jul 2025 08:47:57 GMT  
		Size: 58.9 MB (58882291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b5cf9fdea4d19f8f57d16d74eb5f568413cfa0458f20dbea6512ac247c6c56`  
		Last Modified: Tue, 01 Jul 2025 08:47:54 GMT  
		Size: 4.5 MB (4514187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a04ca0fb77442367d3e90a4a5b3e27646fe5e9a71ba97cf6fedf62972698758f`  
		Last Modified: Tue, 01 Jul 2025 08:47:54 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:90c135225617c9e7d40697e5336642ca02700f565344ec9b2e8a635f7b89e5f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3685836ddf94d2d443dcbe7b5f6ae98815218a06c606a44f59c4ed71a353a8d9`

```dockerfile
```

-	Layers:
	-	`sha256:5491ee8b8e513ed5bafad7404ad3d0625a3a8e403e3ee325d5776cde5546a6f3`  
		Last Modified: Tue, 01 Jul 2025 09:38:02 GMT  
		Size: 4.3 MB (4281532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2bbe29e163be1a40ea829ceb0354729f6f903b310aad20e443fe081aa698d1c`  
		Last Modified: Tue, 01 Jul 2025 09:38:02 GMT  
		Size: 18.5 KB (18482 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:b9e078db03c990cf3db85e1d1d5710ede373c163f9d987fca3a0829f7c3b2bc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.3 MB (224280485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4840f84e4b6aa6335c82509c79841d69683c4037cabf69092b08c4557f8e70`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:43faa9a2f25436afce0db8221e3c0e223102f73a33b0cd47eb32294e8033b203`  
		Last Modified: Tue, 01 Jul 2025 01:24:44 GMT  
		Size: 28.3 MB (28258970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b044d6ffc3783b16fe8050c13a2002d45e9199e735ad5aaf6c25079b6f8e3aa`  
		Last Modified: Tue, 01 Jul 2025 02:40:27 GMT  
		Size: 138.5 MB (138492480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8e43d7ff0afc471096153f447ee5dca72b93018e3b1f252894c37835ee5622`  
		Last Modified: Tue, 01 Jul 2025 02:40:36 GMT  
		Size: 53.0 MB (53014374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e120b48f00e63472d8fa3feebb6d345630539f5d837c68b6ef4b7df03542ed`  
		Last Modified: Tue, 01 Jul 2025 02:40:36 GMT  
		Size: 4.5 MB (4514232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9fc3a09d9d50d0bfa6560196d6f671b1437130c257b98ffc0eb60c7745b999`  
		Last Modified: Tue, 01 Jul 2025 02:40:34 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c888f7996f73911b172ddc75d8537b02710457b4f3c99f9d31d4077d7700ac83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4283408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:599ffb2e164346ca22f6ccfa46c7b932396ecc8699ceca78e138e2f19ed5df6e`

```dockerfile
```

-	Layers:
	-	`sha256:55635232291bc398260b547bab4c73e4e360e1c52c2723b4bea5f71cc4914e14`  
		Last Modified: Tue, 01 Jul 2025 03:35:49 GMT  
		Size: 4.3 MB (4264926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79c4cf42025599829f7770085267011a432af13076772b6808595d6e62b57fa5`  
		Last Modified: Tue, 01 Jul 2025 03:35:50 GMT  
		Size: 18.5 KB (18482 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:f718e91ff322d2f1b69465819617ce4e5ab42e46bb997538d235fb2a96bf5fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 MB (223899468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63cc5f5a659b0ebe97715c72e06478020374ef20f43e5d532ba8ac0e21ece074`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:728fbd29b8599bd56dcb8703b5c428523bcf0f3d48c5e95804f60267a128a3bc`  
		Last Modified: Tue, 01 Jul 2025 01:19:25 GMT  
		Size: 29.8 MB (29838345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45862aa2123546ffa489bdc843a3498ad23f176c0071dd028fb28da9492e803`  
		Last Modified: Tue, 01 Jul 2025 08:12:44 GMT  
		Size: 134.7 MB (134673559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea382bb9d61b6b44809a92a67d1d6940fc0149c521d1553d63f6e47a0bfe9fe`  
		Last Modified: Tue, 01 Jul 2025 08:13:06 GMT  
		Size: 54.9 MB (54872963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69dc72f18a7f1af067f66f7e7b3042608eebf7aad23528fe94143ed6b75213ea`  
		Last Modified: Tue, 01 Jul 2025 08:12:58 GMT  
		Size: 4.5 MB (4514173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29c838c1738f9e179cc775c1f764d055182c5b1da747c8037255da507a0ee02`  
		Last Modified: Tue, 01 Jul 2025 08:12:56 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9714a3c457fe7a42029e8b379fc8780cc6144368e4f6bd408f4e20673bdd25a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4291883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2970a3b8616e100a45744b9c67b82abaa7216aa3c93d18c8641a9f9751ca139`

```dockerfile
```

-	Layers:
	-	`sha256:6cb33ee1d14b7753f28ca898dd69c927655987d0de2406da068ba924a4114755`  
		Last Modified: Tue, 01 Jul 2025 09:38:09 GMT  
		Size: 4.3 MB (4273445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0990277b8d82aed959367897751252622752fd9ad723dfde37d729bc10acced1`  
		Last Modified: Tue, 01 Jul 2025 09:38:10 GMT  
		Size: 18.4 KB (18438 bytes)  
		MIME: application/vnd.in-toto+json
