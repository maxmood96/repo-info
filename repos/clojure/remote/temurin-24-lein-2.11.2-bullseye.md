## `clojure:temurin-24-lein-2.11.2-bullseye`

```console
$ docker pull clojure@sha256:ccf58c1116e847641bdcb05fb95155378e00e22d037f21f8c7bc7fbb600cbff4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-lein-2.11.2-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:6fc29efc6c9380c12167549321200cf539589a8382a3a76b94f6fc2479241a71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (201003635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f46611cc76a1417ab3d27215f8864c875dd2ff48f1f9b9268faea5ba71ed4a3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_ROOT=1
# Wed, 26 Mar 2025 16:17:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775415687efdb13aa667b90fca7d9c935fce414b865b6dff748aaed8ad61cb60`  
		Last Modified: Wed, 09 Apr 2025 02:19:22 GMT  
		Size: 89.9 MB (89949102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a5595b7b2e9e68b98124f5812bd6191744c645bdb3d3e4cfc6be7d8e570af6`  
		Last Modified: Wed, 09 Apr 2025 02:19:21 GMT  
		Size: 52.8 MB (52791389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa110e633d8bf394cd95d5673de93d20067dac6af9f84f09db94df86c7ad1e7`  
		Last Modified: Wed, 09 Apr 2025 02:19:20 GMT  
		Size: 4.5 MB (4514185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa13c36cf9d369b2f090a54e45774e15e19b76cb03073b9ccaf9aed58a88fdd1`  
		Last Modified: Wed, 09 Apr 2025 02:19:20 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.11.2-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:5d5bacced59541da6382b4ec93375d6ca30bbcb15202a49da94dfb5714ec1a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6590750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e715c382f2eba6b34d979c9e398aac8afaec8850af37c233ce83036eb0c16ee6`

```dockerfile
```

-	Layers:
	-	`sha256:fe612818a0646703e47e5ef1523dd99a2d06be56a0f1f523ab7820266a6fa05e`  
		Last Modified: Wed, 09 Apr 2025 02:19:20 GMT  
		Size: 6.6 MB (6572334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7ad4d47e9aec6c141dbef31f9e5876a0cac1b6b55fe1058b186f1f5a2c69a93`  
		Last Modified: Wed, 09 Apr 2025 02:19:20 GMT  
		Size: 18.4 KB (18416 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-2.11.2-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:331403d2cbb92a94b3feb6fc266d4918a58c38cdfe39bc2a07da30c0f408550a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.7 MB (198692897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d692c688f88671778e5357dcc0641a08bcd1d2eb923912cf9a6765ea00e880d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 26 Mar 2025 16:17:22 GMT
ENV LEIN_ROOT=1
# Wed, 26 Mar 2025 16:17:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67679d6635369ee795534b11343dd855f46be72a101f3e77e223b4db82f4cada`  
		Last Modified: Wed, 09 Apr 2025 17:49:33 GMT  
		Size: 89.1 MB (89092739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0290823565349f6afca3845a2aa2eb5bccf301aa94a6e684146e107f7c341932`  
		Last Modified: Wed, 09 Apr 2025 17:49:33 GMT  
		Size: 52.8 MB (52831319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fce340296485c504d180bd3678f309d7103a07a0c7eed7e400d73beeada7f74`  
		Last Modified: Wed, 09 Apr 2025 17:49:31 GMT  
		Size: 4.5 MB (4514188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21c209a6b41aa4f2059cfe53ef457596fc2c29fe8d268614e46fa5891a58cd2`  
		Last Modified: Wed, 09 Apr 2025 17:49:31 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.11.2-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:4793b11af5cd4dacfbd231392f8eb22bc585522c3818dfa7fecd4d79800938a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6595899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ab3aad617f9890ac2ed6aed363c4c46187c8eaca3666a5f3f84e78a3201c21`

```dockerfile
```

-	Layers:
	-	`sha256:212532fc1692b18d08acf4861ce3a6c087608246db88c7aeda4ec1d1c6583212`  
		Last Modified: Wed, 09 Apr 2025 17:49:31 GMT  
		Size: 6.6 MB (6577362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d14af2f9e50172fb5fa4ced6e96fb454a3d96e7879650810d97d5941ec7cb8ab`  
		Last Modified: Wed, 09 Apr 2025 17:49:31 GMT  
		Size: 18.5 KB (18537 bytes)  
		MIME: application/vnd.in-toto+json
