## `clojure:temurin-17-lein-bookworm`

```console
$ docker pull clojure@sha256:26c66bb1a6b3445d97721a9014821761537f24fe313513031ac602d4810de65b
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

### `clojure:temurin-17-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:b6b3806a12697c4ea6d652ab288b2e65b9f9c9b653f624c2258cb19c92e7f672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.7 MB (218738809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c86ab1a4c5a93b99642f4c9b27df42ec76706d64cd727395b483f59cd3df6992`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:17:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:17:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:17:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:17:58 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:17:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:17:58 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:18:13 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:18:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:18:13 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:18:14 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:18:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:18:14 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:18:14 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2455d0702da8b68dc13fc1ae1bd2cafbaeefb6f3875a5a221f004318a893e54`  
		Last Modified: Thu, 11 Jun 2026 01:18:34 GMT  
		Size: 145.9 MB (145905475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c25e7f6f5b1f4197a6a669e4f799d57d1229aa92ec883fb6a7dc22a2a1b01b`  
		Last Modified: Thu, 11 Jun 2026 01:18:31 GMT  
		Size: 19.8 MB (19813122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af06065c644f31b14b4dfe368dfb05830c454b5401478cb5cee6cef5de122e40`  
		Last Modified: Thu, 11 Jun 2026 01:18:30 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef9b2e4686097543fcca09bb36db10c83a79077fac17e0bd93810d45ea9decc`  
		Last Modified: Thu, 11 Jun 2026 01:18:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:89a4ba23f5785d4883b591281d6e785fc390483650ba1ec7e14192152d06b94d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:091cd3918f41b3070c498fdd12751a1dc2f1e2d69eb92d48af314a879b160abe`

```dockerfile
```

-	Layers:
	-	`sha256:7629bd21bf3605f1602fb0c9e51b7b8e13ec7c99aac9d2f36add3869454d6dc5`  
		Last Modified: Thu, 11 Jun 2026 01:18:30 GMT  
		Size: 4.3 MB (4282394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d7f02d9bf3ce70be6f09158cb6decfe997280b2a5a5d26edd57cda2c5471278`  
		Last Modified: Thu, 11 Jun 2026 01:18:30 GMT  
		Size: 18.5 KB (18522 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cdeeba82a06495c6dfd483019f9b8f74bc67d3074c700b6638156d6ae89acfad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217274412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f174b30155397538180a64df0e894ffa007a10407f019ae05b25a5d8bf46a89`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:22:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:22:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:22:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:22:20 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:22:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:22:20 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:22:35 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:22:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:22:35 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:22:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:22:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:22:36 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:22:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7adf2ae4902585365afd00dc1fde38f6d8f4170001db43ba1fda91487774042`  
		Last Modified: Thu, 11 Jun 2026 01:22:57 GMT  
		Size: 144.7 MB (144724358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9303d2303c00c6e5b22b5989b9d051da82a10ce7abf7fefb2ceb45d6516e28`  
		Last Modified: Thu, 11 Jun 2026 01:22:55 GMT  
		Size: 19.6 MB (19642898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e7b636cb66918d8e636c5c90f123ed27d2ec73c10f0c979d4c7a78022f6ad2`  
		Last Modified: Thu, 11 Jun 2026 01:22:54 GMT  
		Size: 4.5 MB (4517711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e0934d8846356fb2be09a32e4cdac4fd4aba4d2025612d49fbfa498cc3e956`  
		Last Modified: Thu, 11 Jun 2026 01:22:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8fbfb893312ea8b9b1b91832dff9d865ec95fc6e49c388705269a224c2687671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d959cceb0f64a1f4ab2fb8c94669213071b8de353fe6b9d5917ba6d9f58c876f`

```dockerfile
```

-	Layers:
	-	`sha256:387ceee2a6bae7b9aa0016cc10fd5adf10a10e0d11b47ab4af58ed918e9acb29`  
		Last Modified: Thu, 11 Jun 2026 01:22:54 GMT  
		Size: 4.3 MB (4282009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:600a9334eaab2c70b7bb7d85e72a7f7f387d46b314fe1c77afdc55fdc38c0a96`  
		Last Modified: Thu, 11 Jun 2026 01:22:54 GMT  
		Size: 18.6 KB (18643 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:f9c85ef558223b7a95a0792da77040f5269d0c2d4b4a566e99688bcb532d6b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.7 MB (222664845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b0c39e0f3b62f0fa4fc9bfc22e9a6410cee7d36a40d085edb7fc44bad054bf8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 09:29:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 09:29:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 09:29:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 09:29:22 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 09:29:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 09:29:27 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 09:30:03 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 09:30:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 09:30:03 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 09:30:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 09:30:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 09:30:10 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 09:30:10 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:88b94a58fac236a778527a3293ccd0ff4d309bff0bf314017ea5af603908fa2e`  
		Last Modified: Thu, 11 Jun 2026 00:21:34 GMT  
		Size: 52.3 MB (52346670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bab2c1eb2f066d3ff6bab086dbc5fafbc50c746db8da2cc3d2b22fadc81c442`  
		Last Modified: Thu, 11 Jun 2026 09:30:52 GMT  
		Size: 145.8 MB (145766120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d77b568a360cf2543403b6426ef372c55060d6f8cb10cef8c70f984aa590f1e`  
		Last Modified: Thu, 11 Jun 2026 09:30:49 GMT  
		Size: 20.0 MB (20033862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5f04a95ab79b8a163d39a7d8d0876192533862168ad507f52cefc29883d6ad`  
		Last Modified: Thu, 11 Jun 2026 09:30:48 GMT  
		Size: 4.5 MB (4517763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229d94f52f43962caa9681cf9b83e373e78b7ac8871ceb46c5fbc8b379dc60ee`  
		Last Modified: Thu, 11 Jun 2026 09:30:48 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d77ba446acd94fa3179591e0fa01aa7732a1612e1ee6df42b647ee7177dc1459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4302821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3e843aae92f73ace64915c1ce26c42698a9fe3d5938195fd4c2d2773e84780`

```dockerfile
```

-	Layers:
	-	`sha256:0fbbd669b5f407ebe7f7fa2a7405f4e7dda6c19a41137b016c6f308f8becc6f6`  
		Last Modified: Thu, 11 Jun 2026 09:30:48 GMT  
		Size: 4.3 MB (4284255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f3326871b5415a7323f9a91f4e39107a5fc89c667f4b0a208c5350aea1c0880`  
		Last Modified: Thu, 11 Jun 2026 09:30:47 GMT  
		Size: 18.6 KB (18566 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:1bb97fb004d0b1496fecc57faa82b66de8c58daeb5b55b288d6bdf32205182ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.1 MB (207065043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fd1b11c1f5c45ea8b9450e54b2d2ce4b0ea8aed9b50c963e12532bfd9f84674`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 03:08:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:08:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:08:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:08:43 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 03:08:43 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 03:08:43 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:09:04 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 03:09:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 03:09:04 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 03:09:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 03:09:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 03:09:06 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 03:09:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b041a55a85cc0e47dd570746852cc1b0fee042f3a03eb250b9f896ac4aa74a3d`  
		Last Modified: Wed, 10 Jun 2026 23:41:01 GMT  
		Size: 47.2 MB (47161500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a926c439affe882834bbc28f308a8c4852fa7e61999319fb64f635b6bec189cb`  
		Last Modified: Thu, 11 Jun 2026 03:09:33 GMT  
		Size: 135.9 MB (135910383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101cd9b7ecf847003376f99e2602a3318f6dd13569c2e36c2224b27f5322fd23`  
		Last Modified: Thu, 11 Jun 2026 03:09:31 GMT  
		Size: 19.5 MB (19474985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbc1aab060cd0da85f38c6bb19d9aef709854c4c8d1374b19def7fea84c498f`  
		Last Modified: Thu, 11 Jun 2026 03:09:30 GMT  
		Size: 4.5 MB (4517745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e873c67277c69d91f1f6192bb4e1816d2151b4934af2259fc25910fc8826925a`  
		Last Modified: Thu, 11 Jun 2026 03:09:30 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:505ba7849371fb1ad7c995d2ddc4fd428702ce87c19979e1da1e8d152af3dce1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4292729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d1361745f090f18be1a9aeef457f866255a227a104452e969764b1472e8a5a`

```dockerfile
```

-	Layers:
	-	`sha256:1fd2fda6c87cc1b71e40e744322a55952e07040d9daad4187cec6ceb13be1d2a`  
		Last Modified: Thu, 11 Jun 2026 03:09:30 GMT  
		Size: 4.3 MB (4274208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:788110b32839b1305e3fb0bd5bbd9c5047e1fe5891359c6f1365dfca53dbb129`  
		Last Modified: Thu, 11 Jun 2026 03:09:30 GMT  
		Size: 18.5 KB (18521 bytes)  
		MIME: application/vnd.in-toto+json
