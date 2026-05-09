## `clojure:temurin-21-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:beeec2565df9af77660938db0a59edd4c036c6c6e38275bf5391c624738bbf90
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
$ docker pull clojure@sha256:4f64bd799b962e1a9098ae55fa60c971a9b8fe4df533dcea4c14b58e223d5d30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.7 MB (208680913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b65db38fade73b4ffa7f9b240c9176cd937f599dd13c6045f2beeb37e07c133a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:17:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:17:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:17:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:17:47 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:17:47 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:17:47 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:18:00 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:18:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:18:00 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:18:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:18:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:18:02 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:18:02 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a6e49ae81a36bee694d9f79c53e461e986fc8b3dc6abf87ebfe0811e5fa4fe`  
		Last Modified: Fri, 08 May 2026 20:18:23 GMT  
		Size: 158.2 MB (158166923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97bfb65c452f078a05b4e2991b49755ea6269fd1a23d67905af375b6036c677e`  
		Last Modified: Fri, 08 May 2026 20:18:20 GMT  
		Size: 17.8 MB (17759545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22798fe1b1619c4567d20818da5a169ba9ae10ad9f92d317928c8d530bd36469`  
		Last Modified: Fri, 08 May 2026 20:18:19 GMT  
		Size: 4.5 MB (4517734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b196b1394a8f20bd2d4e879a6ece960289445f04142c9bc783d38cd900b634`  
		Last Modified: Fri, 08 May 2026 20:18:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:06f1607ca546ca4de2d156f005cb3572573826175dd1649474aa8b560592ca18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2751086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad1b265f358741173a9901ab37dae3e4d808aa560eda641c8800b00be78a4e9`

```dockerfile
```

-	Layers:
	-	`sha256:51aa000251babfcd5dfb6e3505782c5a85876ea76bb2d9503708e279257b14c7`  
		Last Modified: Fri, 08 May 2026 20:18:19 GMT  
		Size: 2.7 MB (2732529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91f47d784acb775dd64ee0f2fbe70d8888c9bc471151c5a6826fae27e991f1c5`  
		Last Modified: Fri, 08 May 2026 20:18:19 GMT  
		Size: 18.6 KB (18557 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:90e02f317de5e0c004c7bd8d6ef29e20f5d1837dd54c3d964a7380877d64f6bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.7 MB (206688480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f04cb82eedb84613074a0538453927c361c99a38f59556551aee9ef0433e036`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:22:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:22:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:22:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:22:07 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:22:07 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:22:07 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:22:21 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:22:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:22:21 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:22:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:22:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 20:22:22 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 20:22:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1cbfa9b2825397e21e091e9a360abca57697217d64d73bc8b97c67048878e4`  
		Last Modified: Fri, 08 May 2026 20:22:43 GMT  
		Size: 156.5 MB (156461168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5f196ba19308dd16c49a4fdf60a9c75357f945a3dcb53177949f8db21c72b2`  
		Last Modified: Fri, 08 May 2026 20:22:40 GMT  
		Size: 17.6 MB (17593005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8761e0725a26665e736943f59ccaca8020fe8e301e00f4ed20ac3071ac1070f`  
		Last Modified: Fri, 08 May 2026 20:22:39 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21979b45337143fdb1f6ad3456cf3bf9083b5bab2651494b9453c64179bcd1d3`  
		Last Modified: Fri, 08 May 2026 20:22:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b7cab0d4f51668b33d3178b8239e0db143031bb3fd6826d5d6fc468488fd471d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc25677fe85e2707ccc121063db0e4e5ace11039f683ad5758bd097a99120a76`

```dockerfile
```

-	Layers:
	-	`sha256:98cbf1165592b756e87aeaff85e0bb72bb815fd3f0943ce022a7e157228b1e37`  
		Last Modified: Fri, 08 May 2026 20:22:39 GMT  
		Size: 2.7 MB (2732144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2869c09d56ea40d6dc726892d73560a1a5abbd5b20ce649ec767a6a879580c9c`  
		Last Modified: Fri, 08 May 2026 20:22:39 GMT  
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
$ docker pull clojure@sha256:afff0d07e7a8aa0f5206f1d47497f7c6ceda07f58ff065f1e68d4fb5e19f7020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196220098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94ce6ae2e4899240fbf45a7e635667f71da1740101e551bd6f8b37300f33d767`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 22:16:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:16:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:16:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:16:57 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 22:16:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 22:16:57 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:17:08 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 22:17:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 22:17:08 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 22:17:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 22:17:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 22:17:10 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 22:17:10 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9927e4ebf9213259a4ef5a3246c16010c9dc3952f2cdaf14171591311e8b7dc5`  
		Last Modified: Fri, 08 May 2026 22:17:39 GMT  
		Size: 147.4 MB (147388334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabab6e19f33d709cd422c6f08f1dd543b04bb09675b908084de86468baff377`  
		Last Modified: Fri, 08 May 2026 22:17:37 GMT  
		Size: 17.4 MB (17422005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8b130d909024f3fc2e1a072d124ec222e9f4b15695d9f03f653f9c3a30a25f`  
		Last Modified: Fri, 08 May 2026 22:17:37 GMT  
		Size: 4.5 MB (4517729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a1562a228fd92e6f34ccead4a2b2873fa503c36133fcf070b21b190b204006`  
		Last Modified: Fri, 08 May 2026 22:17:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:04d0d3da8996044bcc4bd88e7bc06d720ab36fb437a076b4c59920bc8370be16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2742900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13d22382ef4b1cbbdf59a899eef47dacb995311b942f2dd5f830aee6600dbac`

```dockerfile
```

-	Layers:
	-	`sha256:6d517197aebc98f067ed54d4284baa4c73d7c1d805a7b6d5b3164e9dfeb24152`  
		Last Modified: Fri, 08 May 2026 22:17:37 GMT  
		Size: 2.7 MB (2724343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:312083a5dbf621aedb044fb3a027abd623ad01b9f4e52dc78d5e1d251c18dfa2`  
		Last Modified: Fri, 08 May 2026 22:17:37 GMT  
		Size: 18.6 KB (18557 bytes)  
		MIME: application/vnd.in-toto+json
