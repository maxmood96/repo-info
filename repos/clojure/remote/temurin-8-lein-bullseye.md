## `clojure:temurin-8-lein-bullseye`

```console
$ docker pull clojure@sha256:e52de4fdbe37625f61a88a4ea5706005d19eba6f9abcb3f0bbbd38631d8fc4c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:d1325b3669037bb535da78d0f55cd130e9abbc6f0e3f7034e7737ac9520e2f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130051790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8741c52e0c0dbc26dd980f0a5255eaf05e6965b901f4694b9bd49f114db9878`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 23:17:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:17:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:17:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:17:38 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 05 Feb 2026 23:17:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 05 Feb 2026 23:17:38 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:17:54 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 05 Feb 2026 23:17:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 05 Feb 2026 23:17:54 GMT
ENV LEIN_ROOT=1
# Thu, 05 Feb 2026 23:17:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 05 Feb 2026 23:17:56 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043ae01e9e4400da2edd386ee7cb55a26f7fe62a877f01cf30af219fdc4e6231`  
		Last Modified: Thu, 05 Feb 2026 23:18:11 GMT  
		Size: 55.2 MB (55170117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd3d173e72255201c0fca4a4f5f03cfef60c6d480319dc045861e6a7a4110ab`  
		Last Modified: Thu, 05 Feb 2026 23:18:10 GMT  
		Size: 16.6 MB (16607640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1856a722d87f32d7fbbbcc56bf6c49ba456ce3788bc0094c325cec9990f1bd6c`  
		Last Modified: Thu, 05 Feb 2026 23:18:10 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:bfedfc24dc349f0ed7c30c4ca9b50d13a047ca1bffb9fc71febbb72913f30e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4614801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88cdd500ef4093cd29630f805a6ff3378583598d0d037d2e638cf9c45100616c`

```dockerfile
```

-	Layers:
	-	`sha256:815f2566b84176021d74a3f1f72c8e1b9eb4f536cf785f603f1991f0e7fe65ce`  
		Last Modified: Thu, 05 Feb 2026 23:18:10 GMT  
		Size: 4.6 MB (4598431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36e8d46fab26f1ec1237f13093161ba134401afd41f0b93b10bec5072a8e7696`  
		Last Modified: Thu, 05 Feb 2026 23:18:09 GMT  
		Size: 16.4 KB (16370 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f04754456224d058c52195cd002465a5d404fb06bd70a6830a1e116446e4d5e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127622705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adb5873f6bee4798f532dec5209ad600a1e4a76df1cf44d9f80bdf640cf9e6fc`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 23:01:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:01:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:01:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:01:19 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 05 Feb 2026 23:01:19 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 05 Feb 2026 23:01:19 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:01:36 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 05 Feb 2026 23:01:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 05 Feb 2026 23:01:36 GMT
ENV LEIN_ROOT=1
# Thu, 05 Feb 2026 23:01:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 05 Feb 2026 23:01:37 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:0742c20cdb1eb0c212cefb0ff441553e29e6ccfa92b808cca3d7e8548a6fd569`  
		Last Modified: Tue, 03 Feb 2026 01:13:54 GMT  
		Size: 52.3 MB (52258320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bde5efcb33d27d06e84e3f23cc59a1f3fbc32b08ab1888d46dc1293f22731ad`  
		Last Modified: Thu, 05 Feb 2026 23:01:51 GMT  
		Size: 54.3 MB (54251630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b37b91ff79f281f4d0d7cce82e566456e88800e25ec765b1975a75569cfda84`  
		Last Modified: Thu, 05 Feb 2026 23:01:50 GMT  
		Size: 16.6 MB (16595023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13306c674d78b38ff9e358b812fe59bd1c9bb472da41cd763105ba7408459841`  
		Last Modified: Thu, 05 Feb 2026 23:01:50 GMT  
		Size: 4.5 MB (4517700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:cfeff23d02d8e1b6a9788e8867e27a6633136365d04692a711b9cfec52c75e68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4614595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c5da76b7e2bc02d3b5de3cf1543cc83618cee071212a9c4e3c8c30eb4fbce9`

```dockerfile
```

-	Layers:
	-	`sha256:d2f8463e3e74f4abfa4d80319386f72094bae70fd712573bdd2832f64e5268db`  
		Last Modified: Thu, 05 Feb 2026 23:01:49 GMT  
		Size: 4.6 MB (4598105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8394d95bb9e8353f01d2a7436ffdf1302948f24213f065aae68cea0ec4b17aea`  
		Last Modified: Thu, 05 Feb 2026 23:01:49 GMT  
		Size: 16.5 KB (16490 bytes)  
		MIME: application/vnd.in-toto+json
