## `clojure:lein-bullseye-slim`

```console
$ docker pull clojure@sha256:1d474975aaba8b24d36f0e11ebc0207360089dd0bb23cd851c2d12ed776845a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:bcf9bf77205c281e269ead6264483007b39548d3bc19f7ecb84981c228133fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142371118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b29c9461630ae3d8f930a3bdb993123d4e6a6edc1cc05cf42f7d23767b0d2137`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 03:00:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:00:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:00:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:00:35 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 03:00:35 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 03:00:35 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:00:51 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 03:00:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 03:00:51 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 03:00:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 03:00:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:00:53 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:00:53 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2def39ba61d018877eab029bb49f5312188fcf3f564be382981f921d932f625f`  
		Last Modified: Mon, 16 Mar 2026 21:58:52 GMT  
		Size: 30.3 MB (30257826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7271d37d5ec7d26c4ea913c8110ee38cade6170846be08d4a22532a8bb56f6ce`  
		Last Modified: Tue, 17 Mar 2026 03:01:09 GMT  
		Size: 92.3 MB (92256296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50a8859603e9e94b2eb464dd9e016be0a5eb0cd7702483cbb0bf8d3ce464b5d`  
		Last Modified: Tue, 17 Mar 2026 03:01:08 GMT  
		Size: 15.3 MB (15338820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741af4830e32541cd3a0c25d3999ac429d535aaf012a20e4cf4057f082f35ad6`  
		Last Modified: Tue, 17 Mar 2026 03:01:07 GMT  
		Size: 4.5 MB (4517749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51c6303fad0e271aa29c21241db9fda61ea6c750323ed9f6591643edf213fb5`  
		Last Modified: Tue, 17 Mar 2026 03:01:07 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2f50d099b785636539aa7e81e81a073e5fec974327d35b27c30ed2306feede50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be52be0b230bb54307f55c50ea8b693dfc10597038b049266c944c2e95c09381`

```dockerfile
```

-	Layers:
	-	`sha256:a1a1820143ad4f3c5742c26d9b65555378849c6886157a5125e069d455ea892d`  
		Last Modified: Tue, 17 Mar 2026 03:01:07 GMT  
		Size: 3.0 MB (2995642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cfa013a02fb5612fab644ff83018793def900ae636affda729547f404e69720`  
		Last Modified: Tue, 17 Mar 2026 03:01:07 GMT  
		Size: 19.1 KB (19058 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bb16a190cf055711293032cfa56fa7f680468625f24a59e1cc590f2c4b2b5dd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139878191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efb69fd095756c70cccc9dd216b9b46b4cf20e9f38ba5da5483680b6e66b5d86`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1773619200'
# Tue, 17 Mar 2026 03:05:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:05:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:05:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:05:26 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 03:05:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 03:05:26 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:05:41 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 03:05:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 03:05:41 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 03:05:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 03:05:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:05:43 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:05:43 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:345f33ba283982a717a4e5e736aae0d965b9ea4497df11e15c24675df605ff01`  
		Last Modified: Mon, 16 Mar 2026 21:53:13 GMT  
		Size: 28.7 MB (28744526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69edc4821208584609ba50a1f7945b66c6105aaaf91851514f4b787b157b25e`  
		Last Modified: Tue, 17 Mar 2026 03:06:02 GMT  
		Size: 91.3 MB (91288272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70a7243a5af502efb828216d67426d3af3d613841620074674e708cbd210d04`  
		Last Modified: Tue, 17 Mar 2026 03:06:00 GMT  
		Size: 15.3 MB (15327227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5190d8234a19015dd1a2e21ced1e1070bed2f9feacaab3131b082d53a9285e49`  
		Last Modified: Tue, 17 Mar 2026 03:06:00 GMT  
		Size: 4.5 MB (4517737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c58fbbda8d45de4f93649787f294d75f058029a5d99048d8a818f1042fed492`  
		Last Modified: Tue, 17 Mar 2026 03:05:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:787c1986d0ea71329566c5031e6011d4d342eecb6cf0f022932f69067774eed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff49921e3320c6edf6c756cde7ea617b6e0fe2b01ebb1cdee7cd67f67c62ecb`

```dockerfile
```

-	Layers:
	-	`sha256:e81f289880262a9aef25ffdcc1dd9b2952b80f722d55798568a3c58f1751042a`  
		Last Modified: Tue, 17 Mar 2026 03:05:59 GMT  
		Size: 3.0 MB (2995272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9bec187a10d73ec77f6a2675c609466d9fec064b001d260e783c63d022eca51`  
		Last Modified: Tue, 17 Mar 2026 03:05:59 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.in-toto+json
