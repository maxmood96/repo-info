## `clojure:lein-bookworm-slim`

```console
$ docker pull clojure@sha256:2d9b8ee39e4f424b033c58812a3c86c8e514f14ac8a960650e54e1183209bded
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

### `clojure:lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ece216637666bf6787d9766bea5484970e0de7d376727abafd38b31d02d05451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.1 MB (143088535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30de1503f03670bb441070ab712e4ab0ece95173e5ef32bda1968f8b3c61cc6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:19:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:19:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:19:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:19:01 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:19:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:19:01 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:19:16 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:19:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:19:16 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:19:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:19:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:19:17 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:19:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1100a9ace8dcbc40a26712ecee68a42394613c9b46b75f051f35098c1ca07482`  
		Last Modified: Fri, 08 May 2026 20:19:36 GMT  
		Size: 92.6 MB (92574572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29051eed9fb1afdaa1c903c501819d6bd39ec29e40466ce7238b166648f7e962`  
		Last Modified: Fri, 08 May 2026 20:19:34 GMT  
		Size: 17.8 MB (17759535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03615be620330dd99527f684063c841e19b580d0194d6380b795175354199063`  
		Last Modified: Fri, 08 May 2026 20:19:34 GMT  
		Size: 4.5 MB (4517717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa4334086f140183e683e44e19af8c6365bb59ba4db14f77f5d3f725070bb57`  
		Last Modified: Fri, 08 May 2026 20:19:34 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2a90ec20239007702d8bd6ade9521bbc7be90bdd3b90986209363dd6a0db42af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2717943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31559863a54ad9357349366a3e08ac6761982354a6489fde34e18a70f80cca7f`

```dockerfile
```

-	Layers:
	-	`sha256:540f4ee2f9ce073ff8d96cbded0f78c80902090043d24604cce741583a8ab577`  
		Last Modified: Fri, 08 May 2026 20:19:34 GMT  
		Size: 2.7 MB (2698733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbc09bad3cf40669731b46e513bdefec20ecf736eadddd885b86efcb157368c6`  
		Last Modified: Fri, 08 May 2026 20:19:33 GMT  
		Size: 19.2 KB (19210 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ffbcacbf4057e6922522b450f0f02263db32d04153e438d4cc5c5967607e77ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141769608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6834dfccaea725a99469c8760b12c140ab4ae681d7c14deca5a05c19b747fe44`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:22:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:22:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:22:57 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:22:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:22:57 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:23:11 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:23:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:23:11 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:23:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:23:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:23:13 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:23:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31052a2c6c7a34e6b9841ad35dab1dfaa0c49a562e795b25b45ad29662637d1e`  
		Last Modified: Fri, 08 May 2026 20:23:31 GMT  
		Size: 91.5 MB (91542268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d171a044cd60c186883611bcc2ad0839cb0a5cdd0bbf063368f9169e594c49f7`  
		Last Modified: Fri, 08 May 2026 20:23:29 GMT  
		Size: 17.6 MB (17593005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2a3065777327d25d03beac4d370bec181c30e2b2c8c750478f51d92a88cc63`  
		Last Modified: Fri, 08 May 2026 20:23:28 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd623b46acadb614f19e5e3b6976fa4e09ba670a5b55f404e1e75a9106df7e2`  
		Last Modified: Fri, 08 May 2026 20:23:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:343ee3b1225217ebf1fe08aeb2aa8151360d1506f099ef187a19c8a821211c30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2717726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3072dd7a28d1ed67618c59f6c7caccb1aaa929b60f7d84ed8f005ba837cbbe13`

```dockerfile
```

-	Layers:
	-	`sha256:05b63ca7c7cbb471ac51bfc1867a338c92d91f64c6482483a842fb6343ea457d`  
		Last Modified: Fri, 08 May 2026 20:23:28 GMT  
		Size: 2.7 MB (2698369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffbf81033b192fcf2670b6568379f2732e2417c3ce0b243b50a9f38ae14c539f`  
		Last Modified: Fri, 08 May 2026 20:23:28 GMT  
		Size: 19.4 KB (19357 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:8d1c89e086c336a061c2579000318c690e78f9678648dce6fd82080ea372f2f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.5 MB (146471939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73ab3646525799a834c431495de1c69a3fa5d2ced545af1314eb024fbb7c1364`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 01:43:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 01:43:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 01:43:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 01:43:56 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 01:43:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 01:43:56 GMT
WORKDIR /tmp
# Fri, 08 May 2026 01:44:37 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 01:44:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 01:44:37 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 01:44:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 01:44:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 01:44:42 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 01:44:42 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0bcb46f6315f7a2c8ddde875fca21de96c94e451046e6692f77a99aca489f3be`  
		Last Modified: Wed, 22 Apr 2026 00:15:02 GMT  
		Size: 32.1 MB (32078402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de1619367effbb8009b986da2ea9fbc4fb9ea6adb3d628cb1ec99649f247618`  
		Last Modified: Fri, 08 May 2026 01:45:16 GMT  
		Size: 91.9 MB (91914008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04147a14efd079f09579035ff8f47b7906c74945cb73748252e38be066c66c8b`  
		Last Modified: Fri, 08 May 2026 01:45:14 GMT  
		Size: 18.0 MB (17961353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce1379bdf4712c3b38dec097678550de8cf3bee45421aca03ec9a8906f28f18`  
		Last Modified: Fri, 08 May 2026 01:45:14 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:365882b7054523ae69b0caa8ce305241d2d2c4434508fee016af4c628a65af12`  
		Last Modified: Fri, 08 May 2026 01:45:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e399b2a32aadaf755dd107b8b8d80b35e0893012b68a5cfa2c3f0ab528a7f488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2703158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a87ae73a4fcc9d3c85a8aad20f32d4d41d2e2d7a51e6ef735d1c752b53dc7151`

```dockerfile
```

-	Layers:
	-	`sha256:6169cf8137d3db1215755298d9e684432631f0bfb19fac7781aeb63336960266`  
		Last Modified: Fri, 08 May 2026 01:45:14 GMT  
		Size: 2.7 MB (2683890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:363654b67ee91f893f36d75d08c90826054f8179ae7247e018970084b9ba5e4e`  
		Last Modified: Fri, 08 May 2026 01:45:13 GMT  
		Size: 19.3 KB (19268 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:74463311f88999e00e3eb5ef5b4230acb974a51c787fd2bd9b8c752faabf53f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137252085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecdb803ee88b11f73ef7bb2eaceca123a88c7f6c96bbab92263125b85dadd4a1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 22:18:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:18:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:18:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:18:59 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 22:18:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 22:18:59 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:19:09 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 22:19:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 22:19:09 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 22:19:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 22:19:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:19:11 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:19:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e2a98e90054a6c9a3c4e497f6656030195d43c38235d9e7c561af6ea94fc09`  
		Last Modified: Fri, 08 May 2026 22:19:35 GMT  
		Size: 88.4 MB (88420316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3966c37e95f2cef5eeafdb81c76199edf31dea2be63d090f3771d693622c33`  
		Last Modified: Fri, 08 May 2026 22:19:34 GMT  
		Size: 17.4 MB (17421981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3152785f569a9939cd3e65cdf6c919ad475c171c11e693f92a315cd29f76dde1`  
		Last Modified: Fri, 08 May 2026 22:19:33 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bd3ce40ed185361313ba94973634d7070666209fccccd5266fa1257939ab0d`  
		Last Modified: Fri, 08 May 2026 22:19:33 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ba102cc0ed7d0f6e8fd3037833904629132721b993579802c6ab930472541adb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12a629e9fb78cb3e0b827531a05a7c861589644b92ef1044351d9382399246a0`

```dockerfile
```

-	Layers:
	-	`sha256:be6054c2a0f3d8d4ca5264f7e22f326ddd533e42be93ac740bbbcf3d64a50a35`  
		Last Modified: Fri, 08 May 2026 22:19:33 GMT  
		Size: 2.7 MB (2675109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20fb7ac65835c86af611540df28585460429c758aeb81f7437e5696b17c5e1ad`  
		Last Modified: Fri, 08 May 2026 22:19:33 GMT  
		Size: 19.2 KB (19212 bytes)  
		MIME: application/vnd.in-toto+json
