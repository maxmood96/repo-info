## `clojure:temurin-11-lein-2.11.2-bullseye`

```console
$ docker pull clojure@sha256:70fbc5ca86d0fe55ca2f58a69099b49d5a90492668b93b174687c970ff67e924
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-2.11.2-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:490c948db8b8c2818d7458822e7627cac1329a5442e561e834930636b81c5358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.7 MB (256721606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:264d3c2247694813c8af5379d0909246e8927b4155c622b5f91064489006dbcb`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 26 Aug 2025 17:11:52 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 26 Aug 2025 17:11:52 GMT
ENV LEIN_ROOT=1
# Tue, 26 Aug 2025 17:11:52 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:078965fc7cf303b72cc4eef5479dc2dbf5bc84fb8e6052a89b9b5362e14b3651`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 53.8 MB (53755344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc1b375f938c9f1ad67eff1d80717f8c34ca50b82830ae94665bf4e76217ae1d`  
		Last Modified: Tue, 02 Sep 2025 00:17:13 GMT  
		Size: 145.7 MB (145658232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78421c5f7fe6c6ee78dfc70fdebbcb6ea20c36b9e87a6e82c97acfd8c4611deb`  
		Last Modified: Tue, 02 Sep 2025 00:18:04 GMT  
		Size: 52.8 MB (52793795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b8c20d6c155ac479723b4b3e3c1d4b75ad53fea939068ebbc8027d187d5d4c`  
		Last Modified: Tue, 02 Sep 2025 00:17:57 GMT  
		Size: 4.5 MB (4514203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.11.2-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:4fff90bf02725e21349933988dc80404e96c79d953bf82e986caab0506036c6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6820134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7babb15736a83a25f56e0aa4d7179bdc02ef7e938f9259715995aeace8c69557`

```dockerfile
```

-	Layers:
	-	`sha256:6d62d704188c753e79da5de268ce7c1abf55788aa347d519390131d54f2b191f`  
		Last Modified: Tue, 02 Sep 2025 03:36:19 GMT  
		Size: 6.8 MB (6803701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35b70c318c15835a956713cbd161c5a32a4c55ae36dcbd54d499f3957e0c3167`  
		Last Modified: Tue, 02 Sep 2025 03:36:20 GMT  
		Size: 16.4 KB (16433 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.11.2-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a45b33c945a62f4e150cf8d8a345203661f9716a127cf8b658ab6b49e366f4ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.1 MB (252056428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46e5a399a9a31cd190e840bbc552957fa94cda8d23ad3ab1c58d5badf4c920c0`
-	Default Command: `["lein","repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
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
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:7b68ea47bc3cd8615e51fdbe0976cb4999ba56ce8764e755543a4521d69a32f6`  
		Last Modified: Tue, 12 Aug 2025 22:08:57 GMT  
		Size: 52.2 MB (52248409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6978e422a603f55c10edbdbff2aef6a2a5b1bc52fcf21a4f30138d5fd0059bb`  
		Last Modified: Sun, 17 Aug 2025 10:22:40 GMT  
		Size: 142.5 MB (142460557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c31eb8f8bcf114397d3fc7b0913cec8ba753ef38b9ed21e4118577f2faae64`  
		Last Modified: Wed, 13 Aug 2025 14:13:58 GMT  
		Size: 52.8 MB (52833287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b923b329033e703830c05aed26c393e5ac2861659455d88bf0f64ac31fa6c245`  
		Last Modified: Wed, 13 Aug 2025 14:13:34 GMT  
		Size: 4.5 MB (4514143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.11.2-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:6ccf3e06ebee95c69393c78ffd6201adf20626ffdcc764779ace8b3a034dd14c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6825903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee56b13941386a5e84ee9a997c9bcfe9495a40e4e5b6d8468406fc9d0046d9bd`

```dockerfile
```

-	Layers:
	-	`sha256:6de75941e3c6338868a3709693781562f878a4ed4bde1a5dfe5f9ffdd6119d42`  
		Last Modified: Wed, 13 Aug 2025 15:35:44 GMT  
		Size: 6.8 MB (6809350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:021d526e7f9d45fa730b825b9d279e0561bef2241ea3143d5141b310118d3ea7`  
		Last Modified: Wed, 13 Aug 2025 15:35:45 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json
