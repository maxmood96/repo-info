## `clojure:temurin-17-lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:49f44bf3c2d509ce1c03ba49129f5825021bfd0589cad8aa68592baa2f1bf3a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-2.12.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:71d45268179e785c860d40a5bbece7fb02d82410ea8543d027f893901819e8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195743745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84fc1179c28e4430a7aee0810d681906c41cc944b018dc017da8e75e03899107`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:03:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:03:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:03:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:03:39 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:03:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:03:39 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:03:53 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:03:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:03:53 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:03:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:03:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:03:54 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:03:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa73787dcdd9fdf0056a4b06a1522683b2cd68995fb345ac209cbac473f4acb1`  
		Last Modified: Wed, 15 Apr 2026 22:04:14 GMT  
		Size: 145.6 MB (145628750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ebe7241defb4ae8e7d65b89f7d06acde33b32da3b09c7324037c5ee3362339`  
		Last Modified: Wed, 15 Apr 2026 22:04:11 GMT  
		Size: 15.3 MB (15338834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e8821db7f46d1d2365438a021df564ef673493afd034d5312d7b71b09fd2b3`  
		Last Modified: Wed, 15 Apr 2026 22:04:11 GMT  
		Size: 4.5 MB (4517713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4740efec010473fe8e8518565e88cdf911d4ffd21c218b12d3f528c620b105`  
		Last Modified: Wed, 15 Apr 2026 22:04:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3a62546f7154c022e4794f10f16de5376716aa4e6f81cbd411ac21c071013d5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3045984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0cd6a86baf85f63fba0ef2ea09b441eb7bf85f908f2670cd39b0617fb9a3a0`

```dockerfile
```

-	Layers:
	-	`sha256:de24d0f9d668ae9ca01a10a0e0bf66198273aaff65ccb430aff81fff6486e83e`  
		Last Modified: Wed, 15 Apr 2026 22:04:11 GMT  
		Size: 3.0 MB (3027582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df3803e2d2b48f9feb4ce18825f4c524e9b7e3317419434f47da6e98bc934715`  
		Last Modified: Wed, 15 Apr 2026 22:04:10 GMT  
		Size: 18.4 KB (18402 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2b7b5577d2d1472698a9ef65e8c3b3bd311c08db9641ddcae04aa31d002df95f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (193026275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25224da0a1a57593f9aea313fc6f96419b61b68c4603e67bc83014260cd2857`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:15:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:15:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:15:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:15:01 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:15:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:15:01 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:15:16 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:15:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:15:16 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:15:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:15:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:15:18 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:15:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3492d03c4429b4399393752dfdfedaf4d5edd18acc568ed743c3b84c834b3d4d`  
		Last Modified: Wed, 15 Apr 2026 22:15:41 GMT  
		Size: 144.4 MB (144436187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44d695ffd24876d1a3e1dcadbbc6161f6a09a1861d5742470a156bd0371eb90`  
		Last Modified: Wed, 15 Apr 2026 22:15:37 GMT  
		Size: 15.3 MB (15327257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12ac00fd7db838795990a59715ae4e9a574f568f1544b38a39e7e386baf11e2`  
		Last Modified: Wed, 15 Apr 2026 22:15:37 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e68dd5e6231d395b29f7d0fea3b0fb4d878a0523c8e9280269875aabfdff00`  
		Last Modified: Wed, 15 Apr 2026 22:15:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b2082ae31b26dc6168cd71dd2e7124f6be56dfc4aab697848b674639a1491603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3045714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370dc6a1d5320a8a266c32d927fc2496e5f0b2cdf8b05e0dab3b56a0ba107e69`

```dockerfile
```

-	Layers:
	-	`sha256:2c6cf923dbbcf17579cc9cfa7c03706cf1b426d305d8c37825dd1fa9de9dbb6b`  
		Last Modified: Wed, 15 Apr 2026 22:15:37 GMT  
		Size: 3.0 MB (3027191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a1ab8848a4c850c29aea39cb7c4558e31c6e8dde65e4029650f0e7d0a39e573`  
		Last Modified: Wed, 15 Apr 2026 22:15:36 GMT  
		Size: 18.5 KB (18523 bytes)  
		MIME: application/vnd.in-toto+json
