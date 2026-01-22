## `clojure:temurin-21-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:91cb5763a5691f5d422ebd723c2ff5f336ffafd70775edacc4e09b619d3cef08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ea4e6eccd1befacba768176deaaa1e474f41f1a93b0a55387acfa612e5969000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208331262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2bd730a656455319097dcc8c06c61d473f8328b9ce0e637d2f6c6bd232a8a89`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 01:57:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:57:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:57:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:57:31 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 01:57:31 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 01:57:31 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:57:45 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 01:57:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 01:57:45 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 01:57:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 01:57:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 01:57:46 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 01:57:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c02d17997ce3d2c82e082235ea0b5152d06ee659c4e2fabcf1e0079312f1bcde`  
		Last Modified: Tue, 13 Jan 2026 00:41:50 GMT  
		Size: 28.2 MB (28228572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101829ceb6ae1a6d9354db0e5b0710541992e4210099884a21dd18c83c53dc78`  
		Last Modified: Fri, 16 Jan 2026 05:10:26 GMT  
		Size: 157.8 MB (157826055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8c880f8fdf09105e8bd2afbbe779f6016dddbe9780d1663dcf783f2c701fc1`  
		Last Modified: Fri, 16 Jan 2026 01:58:15 GMT  
		Size: 17.8 MB (17758502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b15f322fa7ccaf9e741f655f9bd119f6c1a74c5e5bda8dfdd0313b157e5784c`  
		Last Modified: Fri, 16 Jan 2026 01:58:14 GMT  
		Size: 4.5 MB (4517703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79508369f736900d5203bb941271c88b02fd95cf5c6ad1c104e9a7b65b8cdf31`  
		Last Modified: Fri, 16 Jan 2026 01:58:14 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:84574693d5d13cddc9842dc7e4a26be951b11d144e74bbce1f359ed018e2c072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99236ed5a33515a01d5c6df727a3204153db2be721fc143e3f5e8449d85b9235`

```dockerfile
```

-	Layers:
	-	`sha256:1a15914994e5be0a93ae17814ba26bb715882195493a2f566fe130e1bc43d9b1`  
		Last Modified: Fri, 16 Jan 2026 04:46:12 GMT  
		Size: 2.7 MB (2731900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b6aca540e6d66fa4633991800227f3c68301f40cb2d89ebe8e7c5111bd3eb77`  
		Last Modified: Fri, 16 Jan 2026 04:46:12 GMT  
		Size: 18.4 KB (18402 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:823101bfec77ae6fe9b1c525b6dcba7f7db39412b794a4c4ab70d3e6ec2333bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206325840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2294006c80aca21ffdb06a0201ed43b603cd5e85cb59fa602c0b99e4b183e3cc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 02:01:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:01:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:01:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:01:44 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 02:01:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 02:01:44 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:01:57 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 02:01:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 02:01:57 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 02:01:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 02:01:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:01:59 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:01:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:09 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56b2b3f6cf16e9bd65d0c0f26a5d10f24d63110ebf7a398765cc0db4d6a7d30`  
		Last Modified: Fri, 16 Jan 2026 02:02:24 GMT  
		Size: 156.1 MB (156107636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7df76afbc6268afda91481cbf63fa47061387544150cf0db0890292712778d8`  
		Last Modified: Fri, 16 Jan 2026 02:02:19 GMT  
		Size: 17.6 MB (17592146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46de7bbf9c3e6004b250e20c96fdb888b2390107f3fdad0aec18c5b775fc72db`  
		Last Modified: Sat, 17 Jan 2026 13:51:56 GMT  
		Size: 4.5 MB (4517738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b025219863436af07280a80b7fed75710949c5ebfdda1069a0b12f208116cc37`  
		Last Modified: Fri, 16 Jan 2026 02:02:18 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:71b741d09c945eb46e7b29c3daab7d71d8c0d080ea8094016eba3f6bb68f151a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08605be06ed11d5aff6c803946b9309aadf6c38d1b17bfcb7b41e05869e80bc5`

```dockerfile
```

-	Layers:
	-	`sha256:de676ed9807eaf3b214ace2fd379cd5f8a401bbd0046d420315fe4a696625780`  
		Last Modified: Fri, 16 Jan 2026 04:46:16 GMT  
		Size: 2.7 MB (2731515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ec7d729fb7b05cd9b8ccbc00d08cdf2e96ea93c26a0f484d7a341c156c54dd9`  
		Last Modified: Fri, 16 Jan 2026 02:02:17 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:cad4fa43770c9512424b27ca2bb5559b4eb345bfb6cdb9105090ba919acac926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212490534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded14f2a34906e9e7ad344a6d8c653d9b8123fb8d93c87a71b29357349397091`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 03:27:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 03:27:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 03:27:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 03:27:00 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 03:27:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 03:27:02 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 03:28:00 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 03:28:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 03:28:00 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 03:28:04 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 03:28:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 03:28:05 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 03:28:05 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:cf92d3bf0add4f20720c3232cd336a7f7f50627989684b748675db0b2f2ce746`  
		Last Modified: Tue, 13 Jan 2026 23:17:03 GMT  
		Size: 32.1 MB (32068709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5094bf46310c703a83629a08ef35e481705d22cf663c8418d08e57c629ca01ea`  
		Last Modified: Fri, 16 Jan 2026 03:29:07 GMT  
		Size: 157.9 MB (157942940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751c535fc5f2ea89485d9c3ca465484ec68e7092770a2a102f224cef03fc1709`  
		Last Modified: Fri, 16 Jan 2026 03:29:03 GMT  
		Size: 18.0 MB (17960713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b64a286216efccb318efaab875e47bc0571342ebb9338276600c7688e967e58`  
		Last Modified: Fri, 16 Jan 2026 03:29:13 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334abf4bc4d45281691abe56bacc265b1bf49ad819b9311553f2701012638e3c`  
		Last Modified: Fri, 16 Jan 2026 03:29:12 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:149ab5bca0691d188d6f8b2697fa7145c44667e2ac8371b6c7863e97f65d1ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2752180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a2af23a053823a2a99c89dbe216e28f6f9f74303f703d32a1f94d6ea1c8368`

```dockerfile
```

-	Layers:
	-	`sha256:f479b9b956b80ab198046a7c2b4e58621f8bf90c3be741e4e5091ed45ea3a05f`  
		Last Modified: Fri, 16 Jan 2026 03:29:02 GMT  
		Size: 2.7 MB (2733733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eefed54fc6c6bf7636b43f21042dc205e891caf68447e957c715b1aff2c2324`  
		Last Modified: Fri, 16 Jan 2026 04:46:29 GMT  
		Size: 18.4 KB (18447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:d6b07582599ece2f0a7a5efadd7b7654d7d75ccbfa7050ce68af5c51d2fe00dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 MB (195893285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce21100c61dfcf82405fb43199c89260a1f921be37e0037ea8ce8bbf29442575`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Thu, 15 Jan 2026 23:18:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:18:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:18:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:18:27 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 15 Jan 2026 23:18:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 15 Jan 2026 23:18:27 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:18:38 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 15 Jan 2026 23:18:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 15 Jan 2026 23:18:38 GMT
ENV LEIN_ROOT=1
# Thu, 15 Jan 2026 23:18:40 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 15 Jan 2026 23:18:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 15 Jan 2026 23:18:40 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 15 Jan 2026 23:18:40 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3995e7e7254beb9777289fba2ebc6c1ce81d8c4bab8c8d068146f449323a74c8`  
		Last Modified: Tue, 13 Jan 2026 00:40:23 GMT  
		Size: 26.9 MB (26884415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee49ba92133d874b741829618924bc0c05855d3180b0f68c63b8b6afccf9583`  
		Last Modified: Thu, 15 Jan 2026 23:19:25 GMT  
		Size: 147.1 MB (147069856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69434feae3f38e80d56b3c0706e601a75ee8928330a7a56576dbe24ae07692ca`  
		Last Modified: Thu, 15 Jan 2026 23:19:03 GMT  
		Size: 17.4 MB (17420861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a406d372c3a8e1a6cda31b6c97a6a20824de8d7a9fb7e1a6c3ef1a0abe825c6`  
		Last Modified: Thu, 15 Jan 2026 23:19:03 GMT  
		Size: 4.5 MB (4517725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0747c68b63481f16e76c7b6615d89e1d255179468cc2e0e3aca44f731a8e3e59`  
		Last Modified: Thu, 15 Jan 2026 23:19:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d8e7caff80c018e46521a273e278b5bb1d4f9f63e4e00c370ab30bbb9b0b6cb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2742116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44994519f0a636e537448b764aaaebe808477f75cb47c291b0db9cc88ff3e90`

```dockerfile
```

-	Layers:
	-	`sha256:d35b2f0d9b1d35c78b0df80c74717f6407f59fd8128773ddbca3d26a76811376`  
		Last Modified: Thu, 15 Jan 2026 23:19:03 GMT  
		Size: 2.7 MB (2723714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e772a620c0e11eb572cd656d178f5083ba6ca2573e9f86b29c48dafb1ab19c3`  
		Last Modified: Fri, 16 Jan 2026 01:41:48 GMT  
		Size: 18.4 KB (18402 bytes)  
		MIME: application/vnd.in-toto+json
