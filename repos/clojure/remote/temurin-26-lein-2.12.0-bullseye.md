## `clojure:temurin-26-lein-2.12.0-bullseye`

```console
$ docker pull clojure@sha256:000c55c5e8d60e3bda6bd1bf0a39065ef820a812b2410bd4bfba3e4a7f0cc2bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-lein-2.12.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:51d3ee59b3887788407f21af14f03189aad1d4466a766ea761d041e9198bff51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169444009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c411e6df28409b731989c5846e3692b663f74bafcbda7f782a6342bda5633e9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:21:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:21:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:21:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:21:42 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:21:42 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:21:42 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:22:02 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:22:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:22:02 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:22:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:22:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:22:03 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:22:03 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09102f023c87843d93093cbb21d0fac3649798429fc205bae4e344b0eee8e64b`  
		Last Modified: Thu, 11 Jun 2026 01:22:24 GMT  
		Size: 94.5 MB (94524364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88545cb4c1ce8b77b29ff911fb078d0fe0ab2d52bc2725a5af7608f33c459fa5`  
		Last Modified: Thu, 11 Jun 2026 01:22:22 GMT  
		Size: 16.6 MB (16629747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25268276290e5a84a2e2a8cba7d1d386b22946269e96831b3f68a9df4161e76b`  
		Last Modified: Thu, 11 Jun 2026 01:22:21 GMT  
		Size: 4.5 MB (4517701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2cbc70839068a51eabb35afb1fe5273fe3def3011b39c95fa22ae80fd94ec9`  
		Last Modified: Thu, 11 Jun 2026 01:22:21 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:9071b8f23e3826bda7f4c920b907246afa327cee1db3c0bee9a37526fe71dc7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4469898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b7aa7c0593ab0af55c8eb76c9d0ac7e7d7717b36b47893d48d59cd9a8bc49c`

```dockerfile
```

-	Layers:
	-	`sha256:5fe7dbb597247f5e0d8f208599d29d515ec409c9cfb7b857c4b71d5de647c726`  
		Last Modified: Thu, 11 Jun 2026 01:22:21 GMT  
		Size: 4.5 MB (4451384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89d45561e276af7148b7128741fb012053a772bf37c385943f8123cccb343852`  
		Last Modified: Thu, 11 Jun 2026 01:22:21 GMT  
		Size: 18.5 KB (18514 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3e85005c7d3c571ba8b69d0e91a1dc69de8d4c9fd6e7253b9de70f29b757f6ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166903377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a61411a53066c97e6444f1989e8bc2292fb499482600df6b9b5fda51e667a797`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:26:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:26:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:26:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:26:02 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:26:02 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:26:02 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:26:19 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:26:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:26:19 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:26:21 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:26:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:26:21 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:26:21 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80dc7a7b7a5d949784a66311cad0ee83656706aed30d8b9ff71fb8161896d8f`  
		Last Modified: Thu, 11 Jun 2026 01:26:40 GMT  
		Size: 93.5 MB (93504334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03654328a03c95a29e1759f8e7e11a15cec6552b910f7a0beb6ba4233c43834a`  
		Last Modified: Thu, 11 Jun 2026 01:26:39 GMT  
		Size: 16.6 MB (16616773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe65fa994398c4bb407bf237667d016e3f388cad7250f8172c365a7221232f0f`  
		Last Modified: Thu, 11 Jun 2026 01:26:39 GMT  
		Size: 4.5 MB (4517728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4526feed21664252b4d6fdd006fd6c76c61bdda14cc313549c2d9543daa61bce`  
		Last Modified: Thu, 11 Jun 2026 01:26:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:60d8d1179eba6640ac995ff3de77b0ffcb028ed4ebd3286900a7c73bb87fa92d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4468991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca63dc8d18fc10eddf8657d0451c8d4d79feb2ce94bdd5dadd375343dbaee871`

```dockerfile
```

-	Layers:
	-	`sha256:bf471792086146db1cac16ce561d4ef2fa00ab7db2d71d4e1c2db5fb2cac49b1`  
		Last Modified: Thu, 11 Jun 2026 01:26:39 GMT  
		Size: 4.5 MB (4450355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbe43dfe0813131beae9d2baada184ed54b1bb9b6fa3fd0d650f672c108275dd`  
		Last Modified: Thu, 11 Jun 2026 01:26:38 GMT  
		Size: 18.6 KB (18636 bytes)  
		MIME: application/vnd.in-toto+json
