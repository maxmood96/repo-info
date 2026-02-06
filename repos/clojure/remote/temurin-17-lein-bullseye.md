## `clojure:temurin-17-lein-bullseye`

```console
$ docker pull clojure@sha256:09fcd766f6ab1972a94d7b3dd5867149629dc7c9be0e5c101da6d318b8b5ad15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e1fc17e7ac82dad291b877d078d518f76d86873025e98e9e4e6c2f1e83f64af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.5 MB (220510470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:546945e451411d7bd71a42ca8d4c1337aa537416c35f8212f8194ae74b0508c2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 23:03:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:03:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:03:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:03:59 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 05 Feb 2026 23:03:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 05 Feb 2026 23:03:59 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:04:17 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 05 Feb 2026 23:04:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 05 Feb 2026 23:04:17 GMT
ENV LEIN_ROOT=1
# Thu, 05 Feb 2026 23:04:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 05 Feb 2026 23:04:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:04:18 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:04:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49fb8a732e3083a5b89b656ff862381d29eae790f57f9a92db19ae8405cb30b`  
		Last Modified: Thu, 05 Feb 2026 23:04:39 GMT  
		Size: 145.6 MB (145628408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141eb5cc669dc6c8b1800ed6d62ed1fe3c36d7617bd69f843652a3932e0eb9cf`  
		Last Modified: Thu, 05 Feb 2026 23:04:37 GMT  
		Size: 16.6 MB (16607644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9dd6739da5618f143a6fa330a2b84d66f7ed33f87e7a178c4b3c98243f2258e`  
		Last Modified: Thu, 05 Feb 2026 23:04:36 GMT  
		Size: 4.5 MB (4517729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee9b4d9abc1b32ffec30c6910f833302972be9e83b59dcd234a7c8ccd442476`  
		Last Modified: Thu, 05 Feb 2026 23:04:36 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:30580758c1280e0b7e31e4b71dfc91ad8656ad7f13ee3e6387f12b449fbab05f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4495809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5225693e919822b75df5425f2e3a21502024e49e2cda12af77f9d0e3bca092f8`

```dockerfile
```

-	Layers:
	-	`sha256:df4eb784fd0968d8f3193799af91adcff23e248d352549623f87689f0a893904`  
		Last Modified: Thu, 05 Feb 2026 23:04:36 GMT  
		Size: 4.5 MB (4477442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e54bd16223aa887b1b9b62c1093d23afe140fca986ac730646f934ccfe61222`  
		Last Modified: Thu, 05 Feb 2026 23:04:36 GMT  
		Size: 18.4 KB (18367 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:93d1ace1609186a3f7bae0197e72acd17155452491fe6cf85cfd1f1728681aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.8 MB (217807752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b84c7aa795b85048b9fc7e32ae9c22d768c76f8815d43da89877de1d3e049d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 23:04:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:04:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:04:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:04:59 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 05 Feb 2026 23:04:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 05 Feb 2026 23:04:59 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:05:16 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 05 Feb 2026 23:05:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 05 Feb 2026 23:05:16 GMT
ENV LEIN_ROOT=1
# Thu, 05 Feb 2026 23:05:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 05 Feb 2026 23:05:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:05:18 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:05:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0742c20cdb1eb0c212cefb0ff441553e29e6ccfa92b808cca3d7e8548a6fd569`  
		Last Modified: Tue, 03 Feb 2026 01:13:54 GMT  
		Size: 52.3 MB (52258320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489da778c3ae112900df750376f83f7c8873e1c932941614d078408d19f38aba`  
		Last Modified: Thu, 05 Feb 2026 23:05:39 GMT  
		Size: 144.4 MB (144436239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc313ac8b5344bb34d3a7fcd83f1c20c9c55a3391720608c450da28387813ab`  
		Last Modified: Thu, 05 Feb 2026 23:05:36 GMT  
		Size: 16.6 MB (16595030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78073828c606c9327d1dcff06de8b54f447ef4821fec87e60d5aefd7a77335b9`  
		Last Modified: Thu, 05 Feb 2026 23:05:35 GMT  
		Size: 4.5 MB (4517733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d68a7d9af1583b3b62c13bcb713b0eb67e60965265eb024ec6f70dd235ce1ad`  
		Last Modified: Thu, 05 Feb 2026 23:05:35 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e5c6f035e1fd2945acde0308c28539928f49383639377df2b6011a16fb3f40dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a45a46e4e7857a943d97d70afa21fdc8e79f12b248be202e9d97e8c1c53522`

```dockerfile
```

-	Layers:
	-	`sha256:5e34497a9cb138949ae955faa8f788c652b542b32babe88854a200687de8b9ca`  
		Last Modified: Thu, 05 Feb 2026 23:05:35 GMT  
		Size: 4.5 MB (4476416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6f9fccc3c920c0cce93211d70a89086173d2f17976fe5a8ddd9eb93fd7741a9`  
		Last Modified: Thu, 05 Feb 2026 23:05:35 GMT  
		Size: 18.5 KB (18489 bytes)  
		MIME: application/vnd.in-toto+json
