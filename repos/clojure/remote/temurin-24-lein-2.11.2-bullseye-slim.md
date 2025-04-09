## `clojure:temurin-24-lein-2.11.2-bullseye-slim`

```console
$ docker pull clojure@sha256:bc8de51f49eb38db2128cfdd793895046e5e82c29093a12c1ac94ab9088a10bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-lein-2.11.2-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:06ca44f7b9f7d339c42fca98cffe6ff00fb28e9fe4db4d9f6ec801b2d60a1305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.0 MB (167999540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:381697f707ffd1933dfdc431a6d1bff0433be40b7537b5b966b9bfceaec1186b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_ROOT=1
# Wed, 26 Mar 2025 16:17:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1934697c68042ae195bd92bbf95ee7c721f3f5451ff1b9fba3d1d6cd0fa90441`  
		Last Modified: Wed, 09 Apr 2025 02:19:38 GMT  
		Size: 89.9 MB (89949048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a70437fa78e0a302a6e97a636a2d2286fd5a31fefe08d1aa1f1b444cecaef255`  
		Last Modified: Wed, 09 Apr 2025 02:19:37 GMT  
		Size: 43.3 MB (43278487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d556a0714322d19e7e9393429f3151ff93c6274fff36b53a2dd6ffaec45a11`  
		Last Modified: Wed, 09 Apr 2025 02:19:35 GMT  
		Size: 4.5 MB (4514157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24fe1ce86ed21161ddb39aa1cf530082071a1fa6161e50e124ee4b3dca0be073`  
		Last Modified: Wed, 09 Apr 2025 02:19:35 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.11.2-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:49ca174b31883d76d99841cb2d8ad90b8f7942dff8a5c08a2bac1f526ead30fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4539197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5ebfea9a099642a7d321e0b00f2e4a178b59807eb3231f2f08caca85040e4ef`

```dockerfile
```

-	Layers:
	-	`sha256:03379d3e2db62e0e894c2eaa62b0c48c0e821fb73971c8182c0a0b68bd9e4f1a`  
		Last Modified: Wed, 09 Apr 2025 02:19:35 GMT  
		Size: 4.5 MB (4520747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa246fb437f40b27dd748a6fe1679bfc84aeaad797afe3910f9b482697372036`  
		Last Modified: Wed, 09 Apr 2025 02:19:35 GMT  
		Size: 18.4 KB (18450 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-2.11.2-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9fde8bf66ee45a6a9b3777bf35d85fe7347b7dba47a23a4bb93d265c0673f725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.7 MB (165670960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f586e6059a0f138c289642f1917ca07cd51eb21862b37f747a301328d36752ee`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_ROOT=1
# Wed, 26 Mar 2025 16:17:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:59627ca2e9712141a7d131bec6c9931f8ecea11eac34d96bd1213ccea68e18e5`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 28.7 MB (28749498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468d4121b83272eb440de71d531e8e18529eeb8b0e17efbde785ed87b3576297`  
		Last Modified: Wed, 09 Apr 2025 17:50:30 GMT  
		Size: 89.1 MB (89092779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d34bcf3e02d3b84a35690a7f0021354705f1cd4e7f62f92a653569be13b057`  
		Last Modified: Wed, 09 Apr 2025 17:50:29 GMT  
		Size: 43.3 MB (43314062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b88765352a2904ea648bfa46522412241b044dacac9be36d0c2a71d2ab052a`  
		Last Modified: Wed, 09 Apr 2025 17:50:27 GMT  
		Size: 4.5 MB (4514192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff947784f9caa94c88a7187a68ec613f479d9ff3ebbd06c970d1a4414b7c2ae`  
		Last Modified: Wed, 09 Apr 2025 17:50:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.11.2-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5bc08bea3d4a2607aa3aafc75254fe021cbe6fa10d91731a95bbe0189e212320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4544980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db1d365cbf90fedffac392a063fe9b9d3695c281377ec6673bc8c167ad50fb6`

```dockerfile
```

-	Layers:
	-	`sha256:441351282ab54f6d85b8aa67402dcb01e8cd87b9b57b2f7657187d6ca877c961`  
		Last Modified: Wed, 09 Apr 2025 17:50:27 GMT  
		Size: 4.5 MB (4526408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f8c8c9db40a7e4093d00af3135bd16124b3fbd1424d2a0e03c63cd73d8a3144`  
		Last Modified: Wed, 09 Apr 2025 17:50:27 GMT  
		Size: 18.6 KB (18572 bytes)  
		MIME: application/vnd.in-toto+json
