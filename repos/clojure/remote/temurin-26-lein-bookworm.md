## `clojure:temurin-26-lein-bookworm`

```console
$ docker pull clojure@sha256:084ed7240603b3519e72c9f3aee18739055649bedac9db689b66194a76673504
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

### `clojure:temurin-26-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:4f932f301a96c9f2ebdd3ef70a8db7e8e7771b9596a46f6c795e1f047b3c2da7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.3 MB (167269090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037b90723aecf879b9911ada0e964d8a92d147810c9b28dce728f4c42b3edee8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:19:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:19:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:19:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:19:48 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:19:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:19:48 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:20:02 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:20:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:20:02 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:20:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:20:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:20:04 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:20:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f61d660c381f4a18b6ea14b86b55fd899b137f0ce6283625326b186d457d2d`  
		Last Modified: Fri, 08 May 2026 20:20:23 GMT  
		Size: 94.5 MB (94455692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed61232075885b7fc9499b11ad0e7ac50521b6e004ce19ee28aa246fcf9a49af`  
		Last Modified: Fri, 08 May 2026 20:20:21 GMT  
		Size: 19.8 MB (19806571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e205b19c31ac1d37c4865593442f47a031e076ac148a6780e34222b69c0c9ce`  
		Last Modified: Fri, 08 May 2026 20:20:20 GMT  
		Size: 4.5 MB (4517724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65d0c46534264ff8d4de2bf4358207b5da528b63bfe93ea2e0381c35d29c3bb`  
		Last Modified: Fri, 08 May 2026 20:20:20 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e3bff25ae8765f6151f6c17c2c9ea13b02fba0fd115ce981503f89cb455cbebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f784a71afee3404c19f94ec301e45e2fff741fa7d62475370910dd3b21f48c7`

```dockerfile
```

-	Layers:
	-	`sha256:d45b488d8c616f9bcd15a8c9ea573ac0d77b9bb46ff4775666054f72f2485663`  
		Last Modified: Fri, 08 May 2026 20:20:20 GMT  
		Size: 4.2 MB (4247885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e892ccf5ecf620f72326752ba1a43bcf3996d16a9cf51fc753470628eb008bd`  
		Last Modified: Fri, 08 May 2026 20:20:20 GMT  
		Size: 19.0 KB (19011 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9590dae2e783c927dff21723e51fcb12e0cd284fc4c85ed7f24587afbe686461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165923482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9727515be2652a05e5797b48d375f8f2ad23f9dc786fffc66941721c5c1c2953`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:24:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:24:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:24:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:24:12 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:24:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:24:12 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:24:26 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:24:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:24:26 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:24:28 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:24:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:24:28 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:24:28 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09ed317c68524476dd6f4ed18402c6eaf037b00bede3089d238d542d4272ebe`  
		Last Modified: Fri, 08 May 2026 20:24:48 GMT  
		Size: 93.4 MB (93395205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4323e1710812121ecd674529988e7fa5e29310de44e8afd2b762f7d67dbc98d8`  
		Last Modified: Fri, 08 May 2026 20:24:46 GMT  
		Size: 19.6 MB (19636962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773f9d6af88aacd3b3572b07b5ad8f496aec0a9f08ab6bfb2c7d789ed7f15992`  
		Last Modified: Fri, 08 May 2026 20:24:45 GMT  
		Size: 4.5 MB (4517736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd08ce7a1cacf34cd3d681b08d527cd599f361e8ba8862fa5b431f24c4fbb77`  
		Last Modified: Fri, 08 May 2026 20:24:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:118da710e6f9bd0044d036f10ae1987acbee20afa88036d678af8212cfaf1a2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4266677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a984b18b3d7c09a55cac1457cb8594bcb344dbbe5cf625287686bad7873f0b44`

```dockerfile
```

-	Layers:
	-	`sha256:c18f2282c9d02c25efd55441f55843b621a37fa1d243e1c0101e995122de0b5d`  
		Last Modified: Fri, 08 May 2026 20:24:45 GMT  
		Size: 4.2 MB (4247521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4511ca626a1fad0dc2b0165d78340589ce6db00b9bf0caae04ccd1806e2f2418`  
		Last Modified: Fri, 08 May 2026 20:24:45 GMT  
		Size: 19.2 KB (19156 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:1a0d23d99bef9630937a2d22dc82baf62729cbbed6c6fdde7dc0b0036433aa41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.7 MB (170666877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a01d3c0709fe1d978949d6926b6ffe6725ba10fc0842e589aad83caadda1b1c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 08:50:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 08:50:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 08:50:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 08:50:35 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 22 Apr 2026 08:50:35 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 22 Apr 2026 08:50:36 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 08:51:14 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 22 Apr 2026 08:51:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 22 Apr 2026 08:51:14 GMT
ENV LEIN_ROOT=1
# Wed, 22 Apr 2026 08:51:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 22 Apr 2026 08:51:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 08:51:19 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 08:51:19 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0b84f035435acf0ec33df4748d96fad1243fd6b0ea9917f29eaa507d4c458365`  
		Last Modified: Wed, 22 Apr 2026 00:15:04 GMT  
		Size: 52.3 MB (52336735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7799edd1fe5a978cb7609406a0fd100a731ce723a98e963f7a1829eaf333b6ef`  
		Last Modified: Wed, 22 Apr 2026 08:51:55 GMT  
		Size: 93.8 MB (93781443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4872ee10eda512405033012d274f56c97bd33399718ced2cb6ce1740b5ec1a2c`  
		Last Modified: Wed, 22 Apr 2026 08:51:53 GMT  
		Size: 20.0 MB (20030521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d84b160cf5b550359a9085c67ff850186aebfb0609ea739068dc14a214acf8e`  
		Last Modified: Wed, 22 Apr 2026 08:51:53 GMT  
		Size: 4.5 MB (4517749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e27485c0b550698cbdb93ecc8e03afaa46585628ff21f0cc23d11b299c6d9c4`  
		Last Modified: Wed, 22 Apr 2026 08:51:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ed3f5a17ffecabccc4c84ebda90bb7623c39dffcf4f6db6a65ec2ddf54168084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4252760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d05a2ab491145e51d3fbf82982ebe1eaca14ee573c6886d3cafb861bf0b0242`

```dockerfile
```

-	Layers:
	-	`sha256:8efc79dd1346f71a4915ea521c74459b6be066068fe8d11b0a19843f6eeb9ff3`  
		Last Modified: Wed, 22 Apr 2026 08:51:53 GMT  
		Size: 4.2 MB (4233694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3acf10e013b0ed5a7d16cf16fcb3b24e5f896b5cb732d057d3bf048a40e09c1d`  
		Last Modified: Wed, 22 Apr 2026 08:51:52 GMT  
		Size: 19.1 KB (19066 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:c3466b261bc867d71b9f1c6cd1b7da47dfe7736089f78beaa9bbe050facc91d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.7 MB (161680752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ec89141564131f5d7485aa0e74d6d708e56a5d9f37cad5d7ba6d228b1bac84`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 22:20:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:20:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:20:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:20:47 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 22:20:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 22:20:47 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:20:58 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 22:20:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 22:20:58 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 22:21:00 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 22:21:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:21:00 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:21:00 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:124dbe049873037f973f01d877ec004bf4cd3ce5723d0b8f2067c58ad98137d6`  
		Last Modified: Fri, 08 May 2026 18:27:29 GMT  
		Size: 47.1 MB (47148023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71654bf0ab948d70880e532471e7b5acc4ab064c04bad172dfabf218407becc6`  
		Last Modified: Fri, 08 May 2026 22:21:25 GMT  
		Size: 90.5 MB (90547709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e8d833b24a812a3290e93b6eb3432dacc553161c0ab8ced45720bca6934af0`  
		Last Modified: Fri, 08 May 2026 22:21:24 GMT  
		Size: 19.5 MB (19466829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68fa910e663d05bbfc17baaa7b3b3c487bc7b907175dcaf7fad12ee1637e89c`  
		Last Modified: Fri, 08 May 2026 22:21:23 GMT  
		Size: 4.5 MB (4517761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5097c5f53d44679ffd5dcd680766091fe24bc70fd59cd3d667e0fc4fa023c2ae`  
		Last Modified: Fri, 08 May 2026 22:21:23 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e4c530efd82eedd4407d24f7dd1284c60a53e1e5336e19c9492b66c6c19e2c8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4243896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c40e1f7566a9c569a70c346985916a275668a1b930687c22035c0bc67874274`

```dockerfile
```

-	Layers:
	-	`sha256:09fcf9355d838b4129ff1cd6aa2cb0024c86a1e72096d359cec959237bb84f52`  
		Last Modified: Fri, 08 May 2026 22:21:23 GMT  
		Size: 4.2 MB (4224885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7d541fc4c63198e3ba2497810d4f448832a3166759018c7ee8963ffff4ac84d`  
		Last Modified: Fri, 08 May 2026 22:21:23 GMT  
		Size: 19.0 KB (19011 bytes)  
		MIME: application/vnd.in-toto+json
