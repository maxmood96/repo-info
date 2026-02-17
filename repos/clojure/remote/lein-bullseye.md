## `clojure:lein-bullseye`

```console
$ docker pull clojure@sha256:346f3351710624430d94a58bcc018d7319011f95c918c89a1ce87421e2000441
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:13b727b4a1ee170a4c6e20a74dc0a7f107730809770e66f5854be4f866decdc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.1 MB (167138311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b910646140d753735f6afd7c678388c47133ab89dfbfd6dfc69c34d9421aa08`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 17 Feb 2026 21:45:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:45:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:45:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:45:30 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 21:45:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 21:45:30 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:45:44 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 21:45:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 21:45:44 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 21:45:45 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 21:45:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:45:45 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:45:45 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a8544d5cf2eb550c342d359bf1f4ed62cac4d7ee86ca34c7fa7aff50ec9576`  
		Last Modified: Tue, 17 Feb 2026 21:46:04 GMT  
		Size: 92.3 MB (92256300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a2936fd76ddc5bfac581b91488f4eded64382364554f1d2a91959040cc3c75`  
		Last Modified: Tue, 17 Feb 2026 21:46:02 GMT  
		Size: 16.6 MB (16607585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88f5b35144cafe094bccd16da4bc117223ee0b1c8d29f956000ec191b401008`  
		Last Modified: Tue, 17 Feb 2026 21:46:01 GMT  
		Size: 4.5 MB (4517737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9c91e98f9fc934ea23ea4f3aed969f80e112b0bac17bb42cc76238f7a1a383`  
		Last Modified: Tue, 17 Feb 2026 21:46:01 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:074eaa088dc1d1fe826f46d0d49ed8961b2975883650e2db9930091b32f4cd8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4464485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959df99f01da942d438a688d83c5fd2000960c6df98ff90b7b04f00edf03ce0c`

```dockerfile
```

-	Layers:
	-	`sha256:7ab0577f89b0c007ca75730e05159b7ee6425c95bbb0dc24ef9b36277aa775cc`  
		Last Modified: Tue, 17 Feb 2026 21:46:01 GMT  
		Size: 4.4 MB (4445482 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:feda5d9c5884b7a6faf16cffaae67880a1e5ef80191e8e0ec89bfacd9091437b`  
		Last Modified: Tue, 17 Feb 2026 21:46:01 GMT  
		Size: 19.0 KB (19003 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a7fa3fad51f843f1e4767d3213ab05dc435756836071f47b7cae538b0e628984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.7 MB (164659790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bacef2ba77d77df8e6cb7b8c1863bfe8278b1ea6f0927a091576bc9d11e1ad0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Tue, 17 Feb 2026 21:45:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:45:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:45:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:45:14 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Feb 2026 21:45:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Feb 2026 21:45:14 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:45:28 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Feb 2026 21:45:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Feb 2026 21:45:28 GMT
ENV LEIN_ROOT=1
# Tue, 17 Feb 2026 21:45:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Feb 2026 21:45:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:45:30 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:45:30 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0742c20cdb1eb0c212cefb0ff441553e29e6ccfa92b808cca3d7e8548a6fd569`  
		Last Modified: Tue, 03 Feb 2026 01:13:54 GMT  
		Size: 52.3 MB (52258320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76aa4472156aff08da0ec7c863930846ddcc95d3c36b26a7a17d5325eeb55533`  
		Last Modified: Tue, 17 Feb 2026 21:45:49 GMT  
		Size: 91.3 MB (91288277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa2a994c48b954ba05725c302b12fffd22aad296e842c724c77b6683b418047`  
		Last Modified: Tue, 17 Feb 2026 21:45:47 GMT  
		Size: 16.6 MB (16595042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb9afa65bf23c8425a098c67656a74610e41971d2fbe7bb3434fc401e31650f`  
		Last Modified: Tue, 17 Feb 2026 21:45:47 GMT  
		Size: 4.5 MB (4517721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85c431adc452f26d6a85800974359259b07d0b3b12f7de7f1cfc932649d6352`  
		Last Modified: Tue, 17 Feb 2026 21:45:47 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:61bf506a87e07dc4776eba02ad5f96c170c4144aa3b56cb59e7e3df6e399a917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4463625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6580a238a5004fa4267ee9dcaf3efe99e77b57ee62447be81e6c1356f7315e29`

```dockerfile
```

-	Layers:
	-	`sha256:5b71ea41457bcd5a0e81dea8a006f515a99143304e99916d23c176cf935516f0`  
		Last Modified: Tue, 17 Feb 2026 21:45:46 GMT  
		Size: 4.4 MB (4444477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:656a4fe20263c3a15bd8ac30c2704e74d9d6a02dd0ace5c1dfd52e74ee010cdc`  
		Last Modified: Tue, 17 Feb 2026 21:45:46 GMT  
		Size: 19.1 KB (19148 bytes)  
		MIME: application/vnd.in-toto+json
