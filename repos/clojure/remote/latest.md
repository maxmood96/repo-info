## `clojure:latest`

```console
$ docker pull clojure@sha256:14f30e1f5d33cd3c80cb88d7ade31c191fea0cf4da4e51a72823ae3288823e7a
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

### `clojure:latest` - linux; amd64

```console
$ docker pull clojure@sha256:c1de772333d76dab1d923a7c135450501a2dfab7b1e1e4533026c4778d8e0904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.4 MB (305369551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fde00ab2656a5bed80fb7e7b92a65e39fea7cddd18e58d79570f3238f8cab3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 16 Aug 2025 23:31:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 16 Aug 2025 23:31:29 GMT
ENV LEIN_ROOT=1
# Sat, 16 Aug 2025 23:31:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d2d752424bec099aafc6be3b7696ffebd9f83768430c311d566b21dc12cb11`  
		Last Modified: Mon, 18 Aug 2025 18:50:13 GMT  
		Size: 157.8 MB (157804773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c310d7f455c6d3057e296509fe51979bbd164f1e8645284d74741a455c9e7c`  
		Last Modified: Mon, 18 Aug 2025 17:08:56 GMT  
		Size: 62.1 MB (62084225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a908d116fd3d875e7575ba686c0eb939b6e1ffa3656c055388928c67cb8306`  
		Last Modified: Mon, 18 Aug 2025 17:08:45 GMT  
		Size: 4.5 MB (4514156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f593f93bd6962da6df4e317344885a16744ceef42bba1ef934fc0ed8fb3afbf8`  
		Last Modified: Mon, 18 Aug 2025 17:09:13 GMT  
		Size: 32.5 MB (32470810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acedb1f043fe8225cdd5939cd3ba23ab8dcf9302b0712d62a6b13e8187cead37`  
		Last Modified: Mon, 18 Aug 2025 17:08:45 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd84213af684e9f9c88ab417aaf1a2d83a3dbcccd5c96b90166f5f84df827b1`  
		Last Modified: Mon, 18 Aug 2025 17:08:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:24d22cad65864de3052982cda8caece0da573885fb93e6fbd570fe98be206bd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac96d9942d8ab18b827b90d5ad0d60b9f90d5d898daaa6190cb2ddf5d950db77`

```dockerfile
```

-	Layers:
	-	`sha256:c8020bc35fefe2b5377c3688a2a78409dc2e0029a76f70cc528e5c6403635539`  
		Last Modified: Mon, 18 Aug 2025 18:34:26 GMT  
		Size: 7.5 MB (7464588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c57836d7ec97c385816198a9cc1e8f23549c70276e4ab7b163d4d7bdb34d391a`  
		Last Modified: Mon, 18 Aug 2025 18:34:27 GMT  
		Size: 25.7 KB (25674 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b904f010dd3937ec1b74dce8628f95bbeced971b5e7c4a457284517bbb02b864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.4 MB (303366069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af2b6e25030e85c96cf71589b8c87003d3311bee00ecfbc397972a5959e4be1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 16 Aug 2025 23:31:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 16 Aug 2025 23:31:29 GMT
ENV LEIN_ROOT=1
# Sat, 16 Aug 2025 23:31:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2f78888ab9c57e95226c3244d90e801f0c238e605329f20de72d1f2676edd7`  
		Last Modified: Mon, 18 Aug 2025 19:02:08 GMT  
		Size: 156.1 MB (156081244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77414d354042d82c6e88bb0fb7123299d95f34013bc63dc9015c300d075ca84`  
		Last Modified: Mon, 18 Aug 2025 17:26:15 GMT  
		Size: 62.1 MB (62069068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d880f134aff57aa7da0a1e88d934ea22212951ccb8028e2bfa2b26e2ea112718`  
		Last Modified: Mon, 18 Aug 2025 17:26:08 GMT  
		Size: 4.5 MB (4514158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e498a3f3c647ac972994533f4fcc427405e96bf336f481197992d773f97c5e`  
		Last Modified: Mon, 18 Aug 2025 17:26:11 GMT  
		Size: 32.4 MB (32358071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb2e7482e1a8343565e09c72720a639d9cae96864dfcd847a2d1467d7c5541be`  
		Last Modified: Mon, 18 Aug 2025 17:26:07 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a15c083f8249df0472a29d46cb4a75ffc6237dba97d0440cdd1ef6b3cc4e988`  
		Last Modified: Mon, 18 Aug 2025 17:26:07 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:03eee24c4afa5a848a401fc6421ae8a174b20b0bf125c807e0d2e2bfa476b298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7496125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207b351a913ce89198028e7b5666f12c3693ba69eb0bbb217ae209c07e081de8`

```dockerfile
```

-	Layers:
	-	`sha256:a9c682d0fd4b2d7f794ea3d36eedb5a0e280470425711a8f10fd409a9d24732a`  
		Last Modified: Mon, 18 Aug 2025 18:34:34 GMT  
		Size: 7.5 MB (7470327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c090b491ac83694f97e3be28c9b9c4207e6bd44f851b35d44adb6ed6dea0dc14`  
		Last Modified: Mon, 18 Aug 2025 18:34:35 GMT  
		Size: 25.8 KB (25798 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; ppc64le

```console
$ docker pull clojure@sha256:878e53e56c7c918b33bd83b75530e754dfc32b8f613d7dc68589c47608f15912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.2 MB (315185949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885ecfe4cc6b65858c3bb96e6984ff7c71bf0f0870347450d7d6529e4c009b3b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 16 Aug 2025 23:31:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 16 Aug 2025 23:31:29 GMT
ENV LEIN_ROOT=1
# Sat, 16 Aug 2025 23:31:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:33bc01697f2fcceb00fe53fe1bf433b48dc127c82c1555f61eeddeda9d72ff40`  
		Last Modified: Tue, 12 Aug 2025 23:05:53 GMT  
		Size: 52.3 MB (52338077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21178e342602edd12ca410499981adb42800eb941f19d77cad58cb797945aa34`  
		Last Modified: Wed, 13 Aug 2025 22:01:26 GMT  
		Size: 158.0 MB (157963474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c263420206d00133af94f1437dfd245a1a3a8f4cb1a9504d86890386c591d9f9`  
		Last Modified: Mon, 18 Aug 2025 16:57:12 GMT  
		Size: 67.3 MB (67318954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f5bdbc80af3ab1b08e7b107a1c862cb99020816e77fb3b10d880f5abc30658`  
		Last Modified: Mon, 18 Aug 2025 16:57:14 GMT  
		Size: 4.5 MB (4514204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa63c8ff741e841247eb20fa5663057cee24fea6304cf7deb7666c500fa23cd`  
		Last Modified: Mon, 18 Aug 2025 16:57:17 GMT  
		Size: 33.1 MB (33050167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c3d76786b2f9cc4ec7965741c1c17691547482337bde797faf292c955eff53`  
		Last Modified: Mon, 18 Aug 2025 16:57:19 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cedc6c2188596a356b1cbf30f6ce8f6bb4f3d4c8fa572c202b95c679fe8bc3fc`  
		Last Modified: Mon, 18 Aug 2025 16:57:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:d6f9a27e3a03488d00324cb0b3587fed4870f90367edf2f80ef1b886e144dde5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7495494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db3d0a8f5b33b58a6b0ad6e77022320e9c47d5f9878808791f7f8a727866e91`

```dockerfile
```

-	Layers:
	-	`sha256:11625a5586d030bc3242a17cc9c678ca20643b427bee38eb81577a4f1c77d019`  
		Last Modified: Mon, 18 Aug 2025 18:34:43 GMT  
		Size: 7.5 MB (7469780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f031bcb085b612e367d83338045fb479425e4f1a6ac10d925ede4d5d304d84ae`  
		Last Modified: Mon, 18 Aug 2025 18:34:44 GMT  
		Size: 25.7 KB (25714 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; s390x

```console
$ docker pull clojure@sha256:e3c89ce5d94e3c194f509d3f8f19fd08470744b46f41df89808d0088da06abb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292050329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cd295186dbcf8086341c77bf2946827340840cc7b2b4fb04caf686fcab7ea3e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 16 Aug 2025 23:31:29 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 16 Aug 2025 23:31:29 GMT
ENV LEIN_ROOT=1
# Sat, 16 Aug 2025 23:31:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:635b31fd21bf059b6af0abf57b343066d0218ebb3e0b679927cc1752427a72da`  
		Last Modified: Tue, 12 Aug 2025 20:53:37 GMT  
		Size: 47.1 MB (47149866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b459e3f0007c17bde237e108936432cad214c379e785f9e98e38f4ecd5eb115`  
		Last Modified: Wed, 13 Aug 2025 10:02:46 GMT  
		Size: 147.0 MB (147026949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b440b45e7ec283045c2fedd2fd1dd7a8dba5866c757f0efa397dc7a83bf238`  
		Last Modified: Tue, 19 Aug 2025 00:35:56 GMT  
		Size: 61.1 MB (61102791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc45fda15f79441d7ec88a560a7a9a431b3c44bfd89f60d50d34e790d85b9fe`  
		Last Modified: Tue, 19 Aug 2025 00:35:49 GMT  
		Size: 4.5 MB (4514188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2adb92adef78f68ebfe85fe801141d66cd0612643380107ebebe987c379b572`  
		Last Modified: Tue, 19 Aug 2025 00:35:55 GMT  
		Size: 32.3 MB (32255459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c88e2c9dc339aa42e657c56f52e545e5ffd576a1c7768e08891f6262221488`  
		Last Modified: Tue, 19 Aug 2025 00:35:49 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1a5f03cacca6ed54423d230770c9cfb729df7352fb158549aa748e953af545`  
		Last Modified: Tue, 19 Aug 2025 00:35:49 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:327e0206e765591348249563ccd15f32741b8bb1159d5de0f924cfda359f08d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7481581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee823f9d71bade98ec6ababfc6a472df7563b6ccd74e363f5c8644be3e0c5c6c`

```dockerfile
```

-	Layers:
	-	`sha256:5af09eb7dbcc43dce795bec2f7813c9f82989a34afbd985d2f69b805359d1e06`  
		Last Modified: Tue, 19 Aug 2025 03:34:35 GMT  
		Size: 7.5 MB (7455907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7de8403522244c3c490b8f79eb176662e1742f6b97bec2e945986d6bc6ae1d00`  
		Last Modified: Tue, 19 Aug 2025 03:34:36 GMT  
		Size: 25.7 KB (25674 bytes)  
		MIME: application/vnd.in-toto+json
