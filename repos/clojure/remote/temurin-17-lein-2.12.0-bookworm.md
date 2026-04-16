## `clojure:temurin-17-lein-2.12.0-bookworm`

```console
$ docker pull clojure@sha256:2683561b19551fad03b1d7f2c95f5af6830009e8f38d1de27d1b9bd17a3c957d
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

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:2a06aa5cf249918d5856cedb5966ad42fa2a86bde4d9fb1026d3e590166e7383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.4 MB (218442295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ba954b98933fa7ab003b8fb7b542b32752a184a5fb723a1266fbef90a598e0c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:03:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:03:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:03:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:03:25 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:03:25 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:03:25 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:03:39 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:03:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:03:39 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:03:40 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:03:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:03:41 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:03:41 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b252c630167cf24ddcb96e9049c357a8e53c23860234b17f2484c8a6938db5`  
		Last Modified: Wed, 15 Apr 2026 22:04:00 GMT  
		Size: 145.6 MB (145628767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93cb73b36cd520c620cd62e934579b8db443e1fcb137eff7fc5fd866ad0c2933`  
		Last Modified: Wed, 15 Apr 2026 22:03:57 GMT  
		Size: 19.8 MB (19806562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29f71da71587f4547304d0edf6f937169b2ec24e947270616e5323d25e3c0d5`  
		Last Modified: Wed, 15 Apr 2026 22:03:56 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8369d8ebbd1d0f801785398d94b22c3a30fa2e3349362557f02e498c1ca78e7`  
		Last Modified: Wed, 15 Apr 2026 22:03:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:50a204a0b7ddd85e9d0ec93c5d9753e1e75577b1cc4f4ab2a6290d62da43dd34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53cef8932e762c9ffc09cc66067e16910e819d7abeab918893f2b22ef9df8124`

```dockerfile
```

-	Layers:
	-	`sha256:bb84e8e019ef597883060740a5657da294eb07f0abbad05dd8ac28909868d9bc`  
		Last Modified: Wed, 15 Apr 2026 22:03:56 GMT  
		Size: 4.3 MB (4281731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9f15edcce852d6a2156b8c2f9ba08a571672ae5c25fa3ebc5a138ddea9b462d`  
		Last Modified: Wed, 15 Apr 2026 22:03:56 GMT  
		Size: 18.4 KB (18367 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:274372d85875ebc8021d3157bfbe8ad114859b2705d0bc35fec8546163eef256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.0 MB (216964705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a24e1fe7d4a5089010205dd9d2718de077d4b3f4d53c53761c654fe24433e3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:14:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:14:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:14:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:14:49 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:14:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:14:49 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:15:03 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:15:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:15:03 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:15:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:15:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:15:05 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:15:05 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d18064635f6a1e1bbbd445454443eaebd87254ade9c53b4165b5e1f2a0db256`  
		Last Modified: Wed, 15 Apr 2026 22:15:27 GMT  
		Size: 144.4 MB (144436187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d0e70ab29d492c1d651d2a004f21bf6521fce8dad34391b1f7146182611433`  
		Last Modified: Wed, 15 Apr 2026 22:15:24 GMT  
		Size: 19.6 MB (19637072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b228dfbe930d7c044230fccdf9b8a1ef8aa5c58c1946323fabc81901fc4c670`  
		Last Modified: Wed, 15 Apr 2026 22:15:23 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:879b5c0f66856f23bae4d2d8c0d5b668d6c7f95277e4917fd4b6a72ce177d3ab`  
		Last Modified: Wed, 15 Apr 2026 22:15:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:230500a0b701b513a7d40ec9ab73b905fce674ec955cb24e3d2307c66b4abf47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4299835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:629ae99c7dd19d48829c226b54c446e42d5edc7c397b8bebbf5ac76f45988188`

```dockerfile
```

-	Layers:
	-	`sha256:bf1c7592e475e19c192742ebba83fb998c8ef56a7532a37e24b28922259bedd6`  
		Last Modified: Wed, 15 Apr 2026 22:15:23 GMT  
		Size: 4.3 MB (4281346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:407a0c76ac56181b53c534a23ba8882a82d28fd230ec9b5eb502e173c902680f`  
		Last Modified: Wed, 15 Apr 2026 22:15:23 GMT  
		Size: 18.5 KB (18489 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:d647228ea8dc82ee9f372ac45967ad36e54ff34dcc1b033e66836bf64e5dd7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.3 MB (222317201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b0eb6809189ceed14d9659866b9e516f1be3f1987aab88f7aa51257aef77b26`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 14:37:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:37:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:37:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:37:01 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 14:37:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 14:37:03 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:37:36 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 14:37:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 14:37:36 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 14:37:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 14:37:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 14:37:42 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 14:37:42 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358c872239542a9bb50f47b623d9a261564b534e153d9618343a4775810c5781`  
		Last Modified: Tue, 07 Apr 2026 14:38:26 GMT  
		Size: 145.4 MB (145438242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547bfc3f9b63002b3f532edd3db27af33811a90b8b288f1bdac282429ccefc0a`  
		Last Modified: Tue, 07 Apr 2026 14:38:23 GMT  
		Size: 20.0 MB (20023831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792af8f63037389031e469ab6ce46e42215a11cd2668540bf34ba90ae3bc56f8`  
		Last Modified: Tue, 07 Apr 2026 14:38:22 GMT  
		Size: 4.5 MB (4517761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e79d737139081982b8811b394099b326c6811a9930990796f9c3cf9b0cbc27`  
		Last Modified: Tue, 07 Apr 2026 14:38:21 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5f6a49044868630c0deffc6c3321be4d30ea2680862b0ca2077c4eb097f61278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4302004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f00fbe655363f59f9c326e5f1a8bea440dcfa2ae426dc41ca3cd78d9c2c5fc4d`

```dockerfile
```

-	Layers:
	-	`sha256:03dc016b69ea25dffca64f1da58cc7a040598a0f9c1bb95ec2476389f6a42c73`  
		Last Modified: Tue, 07 Apr 2026 14:38:22 GMT  
		Size: 4.3 MB (4283592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05ae06542f328bc97ff3c6ffb44df4f6626d60b84061db9264f907bf3595e9a3`  
		Last Modified: Tue, 07 Apr 2026 14:38:21 GMT  
		Size: 18.4 KB (18412 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-2.12.0-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:26beb62c6992af72470c4cbb89f1e1f1860be15ae7c4ce72fab74214a2912331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.8 MB (206760056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131497afc9aa3283dd8d57217bb3f1b089197638eaca3ae4b34392b08c387823`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 00:37:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:37:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:37:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:37:55 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 00:37:55 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 00:37:55 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:38:07 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 00:38:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 00:38:07 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 00:38:08 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 00:38:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:38:08 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:38:08 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:40ecbf1d4e17f6b072e6cef463823baec601d9f21c9dc33d98bd258448a986f6`  
		Last Modified: Tue, 07 Apr 2026 00:10:32 GMT  
		Size: 47.1 MB (47148084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d779a8613edca5b69035d6c0c92c01b0a4a763bd78341f5f58fd98ed1021aab7`  
		Last Modified: Thu, 16 Apr 2026 00:38:36 GMT  
		Size: 135.6 MB (135626974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8359a9ea6fd8314306210689aadafd132d61691418b2a919f0808d34cba48a7e`  
		Last Modified: Thu, 16 Apr 2026 00:38:33 GMT  
		Size: 19.5 MB (19466858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d016f495f61dcdafdef85f8e0b47c7d64c1acc94c05f87d0b2efaec85e3800f`  
		Last Modified: Thu, 16 Apr 2026 00:38:33 GMT  
		Size: 4.5 MB (4517711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e40b111bfccdee8f7d9eda3883766d60ae4e506280701f24c8e0a5aedd2896`  
		Last Modified: Thu, 16 Apr 2026 00:38:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b1f2ab70986dfacc4005d2565e523a645ba397fe1be1e21a6c70259155815a86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4291913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e02d0ceda7d06d5143fc653eedb1326859bff73ca3ecfd2cf1e17c1cca70cfea`

```dockerfile
```

-	Layers:
	-	`sha256:ae144a745cc137cc91cdc70555f2f304e8ef6f92429d10c5fb8d44fbf403e1db`  
		Last Modified: Thu, 16 Apr 2026 00:38:33 GMT  
		Size: 4.3 MB (4273545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b24e75150fafcc2171203112797d1520f2a0d83301e0a531d2b9f0d71114c217`  
		Last Modified: Thu, 16 Apr 2026 00:38:33 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json
