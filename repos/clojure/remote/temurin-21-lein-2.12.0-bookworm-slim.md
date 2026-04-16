## `clojure:temurin-21-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:942539a668fd4b9287c2e8481864416abaaae566b419e0f6948c64ff8868e97f
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
$ docker pull clojure@sha256:981f1f91431702c18c31b34ceb2ee4d60a419ba5f257231013fb462ce4a519ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.4 MB (208371150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f03cfa4d5e877ec8b197bacae1227c072c152d4619973e8a88f2bf265e580cd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:04:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:04:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:04:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:04:51 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:04:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:04:51 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:05:05 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:05:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:05:05 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:05:07 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:05:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:05:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:05:07 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05872aa57fc078c39450aba3cf9a64e70a5a5a171da1330406d81d8a6f3bb512`  
		Last Modified: Wed, 15 Apr 2026 22:05:28 GMT  
		Size: 157.9 MB (157857059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9274415961bae54d3b6d6b6e09d4e0b6cb1f1a3b4e86781940ce6eb057eda7c`  
		Last Modified: Wed, 15 Apr 2026 22:05:25 GMT  
		Size: 17.8 MB (17759577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca73d11719c445a27b4fa0273bf062ae09e113fecb171500b15306a3e23b9b0d`  
		Last Modified: Wed, 15 Apr 2026 22:05:24 GMT  
		Size: 4.5 MB (4517752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c25e7eb6c7f64e70f54e1bcc3f70c01f365321344820af4613e10de53c76401`  
		Last Modified: Wed, 15 Apr 2026 22:05:24 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4e372c0460183b349969e913029192635a5a0a48b2c3dcde6f72214e8b41b854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc57066acaf4eaa1aeb8964cfa4c493118792b4c99e8473001ed45a10422ed51`

```dockerfile
```

-	Layers:
	-	`sha256:fa151ba8cbe43691e2b11b88f9b04eee8fa5df004ee0440b0a48a83312d93d80`  
		Last Modified: Wed, 15 Apr 2026 22:05:24 GMT  
		Size: 2.7 MB (2731902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1208fcca673f99d57925682e91d3044a00f8a6d96a5779d0efb6fafbfd6c2863`  
		Last Modified: Wed, 15 Apr 2026 22:05:24 GMT  
		Size: 18.4 KB (18402 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d33416bfedd627d81204c386c5ecaedd6b73422dc975826c1c94dcbdc63e0ea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.4 MB (206360389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f04a7242f73734690d3f5174be4401ad9417e204f9c4814dd9896a258635a98`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:16:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:16:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:16:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:16:18 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:16:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:16:18 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:16:32 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:16:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:16:32 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:16:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:16:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:16:33 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:16:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ba59254af04770c533e084097f80ebee49f02e23b49f086eb0120592dd64ff`  
		Last Modified: Wed, 15 Apr 2026 22:16:55 GMT  
		Size: 156.1 MB (156133056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e0ec750eeaa9d5f1614bff62b699fc484a37d19cab6001b5ac714619134278`  
		Last Modified: Wed, 15 Apr 2026 22:16:52 GMT  
		Size: 17.6 MB (17593029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d2fc0f126b6c15d818821ab9a20b4b40ee6c11447c400fea05c5b306a079fd`  
		Last Modified: Wed, 15 Apr 2026 22:16:51 GMT  
		Size: 4.5 MB (4517709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad174ea9237dd3d1d7ab0919af46d6307c59c016037fe6178a797cefa800cd3`  
		Last Modified: Wed, 15 Apr 2026 22:16:51 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:db62ce5b3a17b40eecc274ff03c80dcd0e60c18b0b0372759653c3b5d339d010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42237981abab2dd0d304b48cb3671e5662e9427848ffd4211b7be5f47ff054ea`

```dockerfile
```

-	Layers:
	-	`sha256:2181a6a13ba705b551197a5ef0d0344003de771de98574f20d0af98b09a3aa92`  
		Last Modified: Wed, 15 Apr 2026 22:16:51 GMT  
		Size: 2.7 MB (2731517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab1f6aa2f9f04622d912d629be9425275362aa4a2e3ba76e60473e5b7ea0ff40`  
		Last Modified: Wed, 15 Apr 2026 22:16:51 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:8b722d2e6b53caf1b892de49cbe8b5f87bb8c7a28c874c6185cd434326cc423f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212535220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7fc6ab8a1e575c476a1aa0f62c40691336bc763a7926e7d3439219570c1919b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 14:45:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:45:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:45:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:45:56 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 14:45:56 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 14:45:56 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:46:22 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 14:46:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 14:46:22 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 14:46:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 14:46:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 14:46:28 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 14:46:28 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b1c56220ca211bc9d02f1ed5c589465809676b6ab2cef705f1e2fb8e9726de76`  
		Last Modified: Tue, 07 Apr 2026 00:09:42 GMT  
		Size: 32.1 MB (32078464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e0e1fa8857b496e254e0f7876a400c7f64ae5a188234bb52567d6106153125`  
		Last Modified: Tue, 07 Apr 2026 14:47:20 GMT  
		Size: 158.0 MB (157977538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9467f8e5a50611513dbebd8150f956c3228ea28b4485b26cbbc53c5c4272ad38`  
		Last Modified: Tue, 07 Apr 2026 14:47:17 GMT  
		Size: 18.0 MB (17961032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb147bae3da656b40077aebd83395cb2a0f7a281462eedea837424db95064d1`  
		Last Modified: Tue, 07 Apr 2026 14:47:16 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803043ed401b9b8a4677326778532ac979b6c21613578986f71ba7212f59cb03`  
		Last Modified: Tue, 07 Apr 2026 14:47:16 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7d8223f7b7c72c12a408e1bf0dabbae9ba1e6982049f7457db316b2e112d1008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2752182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82e662aaa45fc61ed2011652e234f8eba870b33b31cb1c419463663b5195137`

```dockerfile
```

-	Layers:
	-	`sha256:3e77a648e44603b7224c241de3751e19f9a6a22a3d753883c7d54d2ba31fe37a`  
		Last Modified: Tue, 07 Apr 2026 14:47:16 GMT  
		Size: 2.7 MB (2733735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fda921e4c52ffc0c0975f28c7aabc5ca6125a2eb6bbf5fa306f88442aa96e00`  
		Last Modified: Tue, 07 Apr 2026 14:47:16 GMT  
		Size: 18.4 KB (18447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:97997f95140d3491ee7ff60661ded687d05a0b5aab147748b8c624bc6c0f6a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 MB (195937000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227e700fce6bfc087e77a25d2983a9fe91a96623f38269f36388bd7d0bfef23f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 00:40:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:40:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:40:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:40:54 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 16 Apr 2026 00:40:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 16 Apr 2026 00:40:54 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:41:05 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 16 Apr 2026 00:41:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 16 Apr 2026 00:41:05 GMT
ENV LEIN_ROOT=1
# Thu, 16 Apr 2026 00:41:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 16 Apr 2026 00:41:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:41:06 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:41:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd421cfbec05ead7490c0e191741bdb8b9fb15851b64ebc7d7a1a85cfd730eb9`  
		Last Modified: Thu, 16 Apr 2026 00:41:33 GMT  
		Size: 147.1 MB (147105251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c2e311d7e38163274b2a681a89af9377d8764f9696d20e360d0131e6ec69eb`  
		Last Modified: Thu, 16 Apr 2026 00:41:30 GMT  
		Size: 17.4 MB (17421978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada32501017a819262f31a771b28fa2542dbf9bf3e1132f8e6db168c3e065062`  
		Last Modified: Thu, 16 Apr 2026 00:41:30 GMT  
		Size: 4.5 MB (4517708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c0922ace32adcb7223d76b6a5743346c4291f82e832c9ffad553e6eb922e83`  
		Last Modified: Thu, 16 Apr 2026 00:41:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:85fa8ce09144166e541b93e94efc66a3348059162e51cd1a316164da8d2599b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2742119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53bac9c0c4cce22bcd1db9bdf568d2779af8695b265a2cc929738b6428d8f25a`

```dockerfile
```

-	Layers:
	-	`sha256:411836356eb2ea1e288438b988c11d94b6139302eb5e30359d4a2e3b05b49147`  
		Last Modified: Thu, 16 Apr 2026 00:41:30 GMT  
		Size: 2.7 MB (2723716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc81f614acd6e2a8f2bf46f63b50accc36f4c4374910a9d8568abd1671099c6b`  
		Last Modified: Thu, 16 Apr 2026 00:41:30 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json
