## `clojure:temurin-21-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:58f4cb1566abcf1d75de0dab675a3c6616406687df2677ea4c658e3f07a88dee
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

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7d443d8b0239d64abcb44e9a635ad05a9a277c833c17343b7b156c45d5152348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.7 MB (208680953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d5c5103827754b488abfdf667038444293176934a0cb2f3dd02975a7cf1d933`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:26:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:26:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:26:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:26:27 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:26:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:26:27 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:26:41 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:26:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:26:41 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:26:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:26:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:26:43 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:26:43 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2f11661ff1e0429f0c7434e465d66c42d45cc84dca5317d1b833dc543c78dd`  
		Last Modified: Fri, 08 May 2026 00:27:00 GMT  
		Size: 158.2 MB (158166935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43344bed2d1d1a30c3296e0bb7772d334acc3f68ae8d8a7b3148234b93c5c09e`  
		Last Modified: Fri, 08 May 2026 00:27:01 GMT  
		Size: 17.8 MB (17759588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aafa964211a22db99b04a6719f1a33856f0dae3f96f01272a540ccf6f567313`  
		Last Modified: Fri, 08 May 2026 00:27:00 GMT  
		Size: 4.5 MB (4517749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a06dcd4eeb2d188b0aa5bf5a72b73420ef247d83586abb67ccbffc7e5305c4`  
		Last Modified: Fri, 08 May 2026 00:27:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d317601205f2c35cdc53c79b1329aef8d9f5aea3fb144b696fe1e571d32d5cd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2751086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9afda69b4586b7df308fc4efdb2964b50b403c900698d728e17d86b5206936`

```dockerfile
```

-	Layers:
	-	`sha256:20a3da2544553b18836f410e9b4d835bae0b44f13f4e8e956f75734f73347ab0`  
		Last Modified: Fri, 08 May 2026 00:27:00 GMT  
		Size: 2.7 MB (2732529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:338eabd6df05ed7f9bac1ea18347228095164865dc255d5084705d99053d3699`  
		Last Modified: Fri, 08 May 2026 00:27:00 GMT  
		Size: 18.6 KB (18557 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:139d709907bdef773c9d91ea191963cc44efdede89a7c283914f210f013a032e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.7 MB (206688562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b767ef6562b665d64ca4394c5cc718a7bda34027dc6c976387e6ec92b1053a90`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:25:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:25:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:25:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:25:54 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:25:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:25:54 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:26:08 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:26:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:26:08 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:26:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:26:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:26:10 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:26:10 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3de7f78aa45fc18c54b11ef3274cf81e4ad39ae74c71dae612e578a0a6b374c`  
		Last Modified: Fri, 08 May 2026 00:26:45 GMT  
		Size: 156.5 MB (156461190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0be464c4f8cf8ca06d2c324888808fb8a806369944f9b229082f501a7c75f3d`  
		Last Modified: Fri, 08 May 2026 00:26:28 GMT  
		Size: 17.6 MB (17593084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef417f066177f042e4fa6ec2415156fbce3d58ab0317b751d8e748c8a77128a9`  
		Last Modified: Fri, 08 May 2026 00:26:27 GMT  
		Size: 4.5 MB (4517745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f5363954d85e22afa5ff9d3dfc4152329e155b84823d6a288d9ac9f8447a9d`  
		Last Modified: Fri, 08 May 2026 00:26:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0e771c4cf40acd263dc4c7ba95788822e77d58eb0b6f7c9c694405d22e7d4ccd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf74be86c206cf97ac1faf4dd734d483761d1cef27c36d5a8787e6d86c9e0bf`

```dockerfile
```

-	Layers:
	-	`sha256:4bbc36b498e6edc583d519ec57fa76dad3dfc869940d3fc7d5c89bc907ea39eb`  
		Last Modified: Fri, 08 May 2026 00:26:27 GMT  
		Size: 2.7 MB (2732144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:564239f72d15398380acc4725f18c779e89ae44eef7b7c91cd429ba182eef9f7`  
		Last Modified: Fri, 08 May 2026 00:26:26 GMT  
		Size: 18.7 KB (18678 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d45a2d64a8cc4aacf1d07c9ac0f374818f7abe95862ed8cf18415f160d0d424f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.9 MB (212901176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb403172c046ae2da95f76a3dc7f82cd1a877b9170c6a4a84cb75843e45c197`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 01:36:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 01:36:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 01:36:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 01:36:40 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 01:36:40 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 01:36:40 GMT
WORKDIR /tmp
# Fri, 08 May 2026 01:37:12 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 01:37:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 01:37:12 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 01:37:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 01:37:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 01:37:16 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 01:37:16 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0bcb46f6315f7a2c8ddde875fca21de96c94e451046e6692f77a99aca489f3be`  
		Last Modified: Wed, 22 Apr 2026 00:15:02 GMT  
		Size: 32.1 MB (32078402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030929f85e28291d6f68f9b323b1a7234dec490966f0e6af5276563600fd14f1`  
		Last Modified: Fri, 08 May 2026 01:37:52 GMT  
		Size: 158.3 MB (158343282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0b49624ae89d0e44d22491ab805748ba2b761561867023032558555693f3dd`  
		Last Modified: Fri, 08 May 2026 01:37:49 GMT  
		Size: 18.0 MB (17961308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db575a812d7fb7a154d9d302f71ee1d0f232f7aaef04afa9b3f0de3dc5d6768`  
		Last Modified: Fri, 08 May 2026 01:37:48 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d25d9e91ddae9f20761d1fb9f2b6fee1e9be8d4e518be4ef66c0bbf4611145`  
		Last Modified: Fri, 08 May 2026 01:37:47 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d292732be88900f82266a2091154de9e417f16bcfc76be5289fab829737dae6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2752963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f828ebb28cba7b0ed644564d052be5a3c4be94f919997f5744fe0189eebb5778`

```dockerfile
```

-	Layers:
	-	`sha256:347db25adbd698882a776aabeb4f570202e6447ca39820e09f266a3e663c5671`  
		Last Modified: Fri, 08 May 2026 01:37:47 GMT  
		Size: 2.7 MB (2734362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7fdbf78229c4da0fa5820c2c2c5e0b936884d46db244777165603828358e531`  
		Last Modified: Fri, 08 May 2026 01:37:47 GMT  
		Size: 18.6 KB (18601 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:8ec28f3bad8a060998153de2e3efba2087d0ac06e40c293d9715d291d22b6118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196220082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bdae1714a26d769b0b7bf66702c8790a9e4e809be9d92eaab39680e2d4ec465`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:31:29 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 00:31:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 00:31:29 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:37:23 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 00:37:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 00:37:23 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 00:37:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 00:37:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:37:25 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:37:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e045616b012e2611cf7d6acc9aa9f73d8631d846574663f28d8de156f1de70`  
		Last Modified: Fri, 08 May 2026 00:37:55 GMT  
		Size: 147.4 MB (147388391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d77b07ae54f0f88e26dab119b24ad3d86f8983a6222722c6746c2e22de57bd9`  
		Last Modified: Fri, 08 May 2026 00:37:53 GMT  
		Size: 17.4 MB (17421970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304587cf26b8477fb58f021fe4de1524373d2530ff75a586ebd56846ce729bf9`  
		Last Modified: Fri, 08 May 2026 00:37:52 GMT  
		Size: 4.5 MB (4517728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d584837e0b507ed2fac902cc119f99b286074cf2c8b85404b6becdd859d72d9`  
		Last Modified: Fri, 08 May 2026 00:37:51 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:71a09149562b293c9e2f8a663b9dbfa33162c75271818737339596cefee1fd70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2742899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74e82fff5e08c885ec2fcd3d500f463ca69acaa485b888b93f6bd06a7de1c60a`

```dockerfile
```

-	Layers:
	-	`sha256:c00a2d9e518c2cede80594f1515b83616cdeb302c3163eb20995cd0342d0cb6b`  
		Last Modified: Fri, 08 May 2026 00:37:52 GMT  
		Size: 2.7 MB (2724343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db309475994b604d5f431ae6bef5dbd796fc0ec58ae8eba8b4c368463f914317`  
		Last Modified: Fri, 08 May 2026 00:37:51 GMT  
		Size: 18.6 KB (18556 bytes)  
		MIME: application/vnd.in-toto+json
