## `clojure:temurin-8-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:723ac74de6e8a61bfdc5f38d116f92774e655f5c645be000ee8f9404d149b085
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e8f968477d1940aaa55b503a133a48e0bf2a66a6dd089cb7cc7c10027960b2f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132771488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c7ff10dcafcdc7f99707fc4c6d5b2488488975f52ef9fbb307630f58509dbb1`
-	Default Command: `["lein","repl"]`

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
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef0548d224b83376a60f405481ba646f0d97ea531021f41cb2801a144591656`  
		Last Modified: Tue, 08 Apr 2025 01:35:19 GMT  
		Size: 54.7 MB (54721226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0b406cb045f0afad42ed625f5237ffb4597a1e7032390c3b6b99879084ff71`  
		Last Modified: Tue, 08 Apr 2025 01:35:20 GMT  
		Size: 43.3 MB (43278612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c6dfea969a44b93c835f5b6c36949b1bf215cd6c7459ee4681e3a5a0dd03f0`  
		Last Modified: Tue, 08 Apr 2025 01:35:19 GMT  
		Size: 4.5 MB (4514199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:edcbf95c8519f9029f202726420678d4430d5f44c8b76aca82cbfaeecdb8d631
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4708178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4628a47186a43b4659b91344ad803a5d2111334d5b5a7b503f35ecee38cff5f2`

```dockerfile
```

-	Layers:
	-	`sha256:381b9165f797af5c580ad6ba5c1aa50b35abf130df74bc20d3f37eb94222a41f`  
		Last Modified: Tue, 08 Apr 2025 01:35:19 GMT  
		Size: 4.7 MB (4691727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bae63fd64820876f7fce6485d2630da6be017fe26d60183493ac974c04b91a27`  
		Last Modified: Tue, 08 Apr 2025 01:35:19 GMT  
		Size: 16.5 KB (16451 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d63358960979860d6787a998c0e7cbdcc602fa7298e74094d06534a5373cd9b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.2 MB (130192789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c62fedcbf6d293ca16edb11382eddb23c5da25881de2f7d914ade93bbf6875d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 08 Mar 2025 19:45:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Mar 2025 19:45:48 GMT
ENV LEIN_ROOT=1
# Sat, 08 Mar 2025 19:45:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0beb154d80ddf299833a8f5c917f8e13c0c4020b2126ace13eb5937913cfc1`  
		Last Modified: Tue, 18 Mar 2025 00:11:30 GMT  
		Size: 53.8 MB (53822777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bd5040a86da73aae84c10820ec16c3f974df102d9c6378f4703e3355246209`  
		Last Modified: Tue, 18 Mar 2025 00:16:54 GMT  
		Size: 43.1 MB (43109901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425395072fa9c07597cc499675c5dfeaa30abcace8c491769fa1cb73740c8912`  
		Last Modified: Tue, 18 Mar 2025 00:16:53 GMT  
		Size: 4.5 MB (4514156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eb61ff32b9429c318ad2897729846d92a7ff7abe4ae544e0dbe80fbd3feab33f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4712715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8cab987c3a6d2132f7df5db7780c5f47635feb08c42aba5acbb58e58cf27f15`

```dockerfile
```

-	Layers:
	-	`sha256:a749d83bbef3897094be8bfdbd552cb0e5e35f1baf31718023fb1d27670c9cf3`  
		Last Modified: Tue, 18 Mar 2025 00:16:53 GMT  
		Size: 4.7 MB (4696143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c90af566a6600181638ba109df725ebe95521902af767b89fa9ea0996f0a6288`  
		Last Modified: Tue, 18 Mar 2025 00:16:52 GMT  
		Size: 16.6 KB (16572 bytes)  
		MIME: application/vnd.in-toto+json
