## `clojure:temurin-21-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:5cd8fdfc29e2b381e0a5d0ffd0a534ede65dcd87ea5168c8fb44b8eebcfab541
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1cb0c48d8cc8319bed3b746a5eb9a16eca6fad75b468c4bce2e3d288229385f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.9 MB (207921409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26590b43d26387e81b6e3d1b4ef7700fadde94f279c7841c00365a8b004b5d8c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Sat, 08 Nov 2025 18:43:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:43:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:43:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:43:57 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:43:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:43:57 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:44:11 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 18:44:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:44:11 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:44:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:44:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:44:12 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:44:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977a11021b1e8739ef70a03594a27b853f8524cc230a3c649f984aad414aef53`  
		Last Modified: Sat, 08 Nov 2025 23:04:28 GMT  
		Size: 157.8 MB (157825965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1ebcf594be62c73a2df1a879c38e8d87fa2001636edf222699eba14fea12e5`  
		Last Modified: Sat, 08 Nov 2025 20:40:38 GMT  
		Size: 15.3 MB (15318715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae966d01aade6547f4a5728e10c35871ffaf5e9ee1fbde1aa254a09b2241f43`  
		Last Modified: Sat, 08 Nov 2025 20:40:37 GMT  
		Size: 4.5 MB (4517704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01603e6844c5a5cc4e85b7036d1610572af1511ffb534f39a27ad110aca6c94f`  
		Last Modified: Sat, 08 Nov 2025 19:30:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:751562770c6d69040c345a184ad62f0cf445dfad687accbc0030e6e508391eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3039415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99720077be425776e136190f518fce61ffd5b822b70fea4f4864d7e8e9817028`

```dockerfile
```

-	Layers:
	-	`sha256:9a64716ad0219fcd086dfec2b4822810718a1a34ed6833696663e2526e3c7ffe`  
		Last Modified: Sat, 08 Nov 2025 22:47:39 GMT  
		Size: 3.0 MB (3021012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b04fe35a69a0d44344b119f6f8b90a3e71b76be669765acff6ff39c2dc3824f2`  
		Last Modified: Sat, 08 Nov 2025 22:47:40 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:75933f50d2d56fa9d06141ae40d5bac53785007a1506b0aeb4b6ef523042a9a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204680224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef20a290bc58c67437d5e00b68ca5b7d4b030bf3b0701d4d7bf159994a81fe3d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Sat, 08 Nov 2025 18:43:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:43:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:43:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:43:33 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:43:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:43:33 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:43:46 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 18:43:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:43:46 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:43:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:43:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:43:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:43:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1157830f8bd0081931b19e6afb21452a22166e22161414c8674fcd509dd524`  
		Last Modified: Sun, 09 Nov 2025 08:27:41 GMT  
		Size: 156.1 MB (156107663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55fcf2941396d18e3ddc5a15bc9076f4c529f9443349d0bb2afef6d6d0026640`  
		Last Modified: Sat, 08 Nov 2025 18:44:32 GMT  
		Size: 15.3 MB (15305841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7428a66631b59665b31b47f841982765cc666a85a47ff907edb49b7d7fc5a89d`  
		Last Modified: Sat, 08 Nov 2025 18:44:30 GMT  
		Size: 4.5 MB (4517739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ff90e532243b7b1017ceac5ce3048ca20bc0f34847993c82af1a3d196a8c9a`  
		Last Modified: Sat, 08 Nov 2025 18:44:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2dfefbb11df91a2ffc5e02abbfa21ee0b3ba4ad750fbf0ea7501480f280f0143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3039145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a31e00eb66ddb6277c6818f137478f9c4bbe57b74956e2f516c9e5376fbed7`

```dockerfile
```

-	Layers:
	-	`sha256:582ccda2075efd6a3a0af58a5d20a61c91b52642373804ad80db6712ca55789e`  
		Last Modified: Sat, 08 Nov 2025 22:47:44 GMT  
		Size: 3.0 MB (3020621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb22584d68338d003379109dd74fe3a29e5ba93f2a33b2b635b3cc345949901b`  
		Last Modified: Sat, 08 Nov 2025 22:47:44 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json
