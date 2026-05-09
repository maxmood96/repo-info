## `clojure:temurin-11-lein-bullseye`

```console
$ docker pull clojure@sha256:136b61b885682f0b4bc0d50a68f8a57b853a1302ec8f9286163de0e1655a6d36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e5dec5f91daf7bad6bb21c435f3716cb936844d07efaf7ba60a896c9ff84bdf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220796912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:506814a9ff5f4b7c1c4bb89253fe75de4daaa0532905933bacc835445e7169b3`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:15:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:15:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:15:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:15:36 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:15:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:15:36 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:15:50 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:15:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:15:50 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:15:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:15:51 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8d3d8f7dfb124ded26abcc75a13b426c7daf76e262ba291825ca2c7ee02748`  
		Last Modified: Fri, 08 May 2026 20:16:11 GMT  
		Size: 145.9 MB (145886217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa73cfe8c19f31828de7cd8b3c5fa22e5f45acaace4ce6452c14c8ee7a81ec1f`  
		Last Modified: Fri, 08 May 2026 20:16:08 GMT  
		Size: 16.6 MB (16629594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6441146faaeca8ad1558f19023c586b08ea0d6db1e274fb4cbc777c7f0c60f23`  
		Last Modified: Fri, 08 May 2026 20:16:08 GMT  
		Size: 4.5 MB (4517726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7e0d85cd6fc11906598ddf517dbbe0dd63cfef68430a3f2dc0199c3b92ed1d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4522541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6b0bde07bb1232cc4f216afa6c2f08d3a4550067e72e2982009a46c50f9b8b`

```dockerfile
```

-	Layers:
	-	`sha256:a6ba505736be6d82911d520f75a717eebcc66b057788dc7f3efd5d35dd1ca02a`  
		Last Modified: Fri, 08 May 2026 20:16:07 GMT  
		Size: 4.5 MB (4506005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ba65de8130cd45d3ee3e9b3f91ae87716c7cb5c255268372648bf60399e63f5`  
		Last Modified: Fri, 08 May 2026 20:16:07 GMT  
		Size: 16.5 KB (16536 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:138614a5de1eb74e578e7ddf069780b10ae839cb872513b0103dc0e20026c91a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.0 MB (215969750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e50c83bf68db793c6df7ed294ffb442358be0be4da100f5fed614ce949417a2`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:19:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:19:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:19:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:19:57 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:19:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:19:57 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:20:11 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:20:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:20:11 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:20:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:20:13 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bea5c4bcd2c056096849667d2efacf67550add9a59e40006282f3404143a26`  
		Last Modified: Fri, 08 May 2026 20:20:33 GMT  
		Size: 142.6 MB (142582233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4450be3634334bae4500cc24d107f28416db09a3893b3c21c58075f439711b00`  
		Last Modified: Fri, 08 May 2026 20:20:30 GMT  
		Size: 16.6 MB (16616535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d686fc36e9a4960894a221deeaf4d6e9546943eba530be4027d915ee32b334c6`  
		Last Modified: Fri, 08 May 2026 20:20:30 GMT  
		Size: 4.5 MB (4517740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3b6abcd7b299c727d2ca035e4f256597e8e7661fea1609e0f4c7348481f0d8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4522254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c967641620190e7ac662afda4db4d959d1e2e0d384c74285e431ec8c9a6ce0`

```dockerfile
```

-	Layers:
	-	`sha256:81f0d44d730d048c41f26fc1211521d7e7c8f5a75a846a75b741216cc09df623`  
		Last Modified: Fri, 08 May 2026 20:20:30 GMT  
		Size: 4.5 MB (4505597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b888058fb15dbbdd24cabee97d9c9c77f796802b69c3dfb3a7c7eb692a5c2eea`  
		Last Modified: Fri, 08 May 2026 20:20:29 GMT  
		Size: 16.7 KB (16657 bytes)  
		MIME: application/vnd.in-toto+json
