## `clojure:temurin-8-lein-2.12.0-bullseye`

```console
$ docker pull clojure@sha256:054e0b129408e37841855b27b02dc094ea82ecead6856d1727223dceeb4167bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-lein-2.12.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:cac41d4d5e24fce1a7a568e5e41d6c9500a2422a02c633ff33be1354c3e6691d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130109437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa4e0df854e32f99cbdacadcb12af66f37b34581aa488a6eaf006df03a32050c`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Tue, 12 May 2026 21:45:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:45:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 12 May 2026 21:45:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:45:30 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 12 May 2026 21:45:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 12 May 2026 21:45:30 GMT
WORKDIR /tmp
# Tue, 12 May 2026 21:45:42 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 12 May 2026 21:45:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 May 2026 21:45:42 GMT
ENV LEIN_ROOT=1
# Tue, 12 May 2026 21:45:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 12 May 2026 21:45:44 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e91aeb97172d61874c651c49d2520e8d80d759bb61fb8512153f56c5f7348f`  
		Last Modified: Tue, 12 May 2026 21:45:57 GMT  
		Size: 55.2 MB (55198701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7719ea5768df84f3f6561722798924b72403319a0d954655efd8e4d752ac6a`  
		Last Modified: Tue, 12 May 2026 21:45:56 GMT  
		Size: 16.6 MB (16629612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0ba6313640b39009c8cfa55d6671da0713354dcd356f24391af45ab3deb640`  
		Last Modified: Tue, 12 May 2026 21:45:56 GMT  
		Size: 4.5 MB (4517749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:28a207161d3ba88886a12e62c55f2c69e5447ccbb377ede7e2b8a17c20d556e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4623375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2938bc2d836576561d33b6bd905fb4d78912960ba4542e201f06019210320375`

```dockerfile
```

-	Layers:
	-	`sha256:2fd27f0e4f722d9fa27a84f2982051d434ef6037e513c6542629afc540dceeb5`  
		Last Modified: Tue, 12 May 2026 21:45:56 GMT  
		Size: 4.6 MB (4606851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a5f420cacdaa3b8b4f69dd5463ea09cc61b7a19d8881435f0a09d18e866ca6b`  
		Last Modified: Tue, 12 May 2026 21:45:55 GMT  
		Size: 16.5 KB (16524 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1c15001494e1ce6cabfbf6316b9b214d7524c98cec43503232b4bcc5c7fed442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127660469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79006e87431e4d78647c6b64698cd44d1ee5ac4d0a8ecfb843965a5187b0b942`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Tue, 12 May 2026 21:45:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:45:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 12 May 2026 21:45:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:45:14 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 12 May 2026 21:45:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 12 May 2026 21:45:14 GMT
WORKDIR /tmp
# Tue, 12 May 2026 21:45:27 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 12 May 2026 21:45:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 May 2026 21:45:27 GMT
ENV LEIN_ROOT=1
# Tue, 12 May 2026 21:45:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 12 May 2026 21:45:29 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39e131659535dfeccbd1a3a5b816d3b7f32abcdcc92b5abf272427f730b01fe`  
		Last Modified: Tue, 12 May 2026 21:45:43 GMT  
		Size: 54.3 MB (54272965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b09d879174defe5474a749560b532611c248dffa2cc9426d038886203a16a1a`  
		Last Modified: Tue, 12 May 2026 21:45:42 GMT  
		Size: 16.6 MB (16616547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a85a5a876e38e27dee9f7dda1df5a817ea8f77b918aef06d2b938f818853ad3`  
		Last Modified: Tue, 12 May 2026 21:45:41 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:4496795c394f634ce28a709cef45d5fe2100c74e1821a3cb628366618e2b98f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4623170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b389b152ee876808f9a7e21cad264ee6fd61013858f1c3e0f8c3df9ec405871`

```dockerfile
```

-	Layers:
	-	`sha256:724cfbfcf720377e30410f1250f631618ed0872432a2b16d72dcfed248ba56d7`  
		Last Modified: Tue, 12 May 2026 21:45:41 GMT  
		Size: 4.6 MB (4606525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef7131ff1f2f50a251421b27b0fa9416cc8e6fdc2f430db5fddc4db1c2ee3d1c`  
		Last Modified: Tue, 12 May 2026 21:45:41 GMT  
		Size: 16.6 KB (16645 bytes)  
		MIME: application/vnd.in-toto+json
