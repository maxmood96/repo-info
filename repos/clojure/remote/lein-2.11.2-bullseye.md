## `clojure:lein-2.11.2-bullseye`

```console
$ docker pull clojure@sha256:144112b35159f2ff98822ed9353ba0535cf2aa701a89904c8380ba57842d007e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:lein-2.11.2-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:abaa20065cb85e2fc630a352bb13732d9bafbf14e68fd8010f669ec8332c6baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268697703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7587eb2e90cacad33e8aa9e54bf1c98c31431842aa110d5881bf9258a44300c4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a957e88b15ed9bc7dbca2841656020e011a8fcc17d0ee33943cab748c9adfb6`  
		Last Modified: Wed, 02 Jul 2025 16:11:49 GMT  
		Size: 157.6 MB (157634517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d490dd495c3866478b0f54050e2828116ba94c3132185402ce7022dd1dd057`  
		Last Modified: Wed, 02 Jul 2025 04:17:04 GMT  
		Size: 52.8 MB (52793789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee9b7d698548595907babe8dea9822378194557ad1b1d29665a7926317b6940`  
		Last Modified: Wed, 02 Jul 2025 04:17:05 GMT  
		Size: 4.5 MB (4514148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bb18d2205a1d2e1b6079273f498fb000d7e0f7a7025a7031de130299792a96`  
		Last Modified: Wed, 02 Jul 2025 04:17:00 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.11.2-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3a3a0741ae9b1ed11264900edbb4f85cb2b1a19463592604d955d5fc8cc60cc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6806368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2112508745b239023d91a518d2e1cb31903bea57418feff1f4b95f8c88300235`

```dockerfile
```

-	Layers:
	-	`sha256:f3fa02a0a09895e50171442879f1334c9d888f78e1d1b04d74bb97c782093125`  
		Last Modified: Wed, 02 Jul 2025 06:34:37 GMT  
		Size: 6.8 MB (6787304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f550c320961ca2b34128d30a42ea5931729e40627f36c7af4ce68706729e9a73`  
		Last Modified: Wed, 02 Jul 2025 06:34:38 GMT  
		Size: 19.1 KB (19064 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.11.2-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c70b59f4dfbe3b3c49af936e8311b9c53a38bbcebd35b979b4a9e6073b691687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265528875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aea13142013719c1bec8eddd7209995ead2352f0146047e0cd975df193a313a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:df45b4853b6fce6b81d1ac6218d861c6d7c8c14da4be409d42ee4bfdf0737e71`  
		Last Modified: Tue, 01 Jul 2025 01:15:18 GMT  
		Size: 52.3 MB (52252254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58e510cae3c2f52c0dcc3d8cd29b20a551d12ebcbeb7f0b7c1dd44e2de6a21e`  
		Last Modified: Wed, 02 Jul 2025 15:56:17 GMT  
		Size: 155.9 MB (155928828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b603233b30b87b692a227ebb863f3ded9a16f2a37024dac3fabe03a3cdea7a`  
		Last Modified: Wed, 02 Jul 2025 16:12:31 GMT  
		Size: 52.8 MB (52833185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e09b546b18cd8c1c7e0923f59181e8f28e77f8753162e47b0b359e9efe7f48`  
		Last Modified: Wed, 02 Jul 2025 16:12:32 GMT  
		Size: 4.5 MB (4514178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0b5665d24d1cf10b0e0784a99d480715a72f96344b2db4e0450c5e66d7d76c`  
		Last Modified: Wed, 02 Jul 2025 12:44:05 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.11.2-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:df6480daabcf413ba7376875dcc5ad61c4746b55d58b144abb31153b6d78e0c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6811569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c46042f2397dbe2cf0102291ed48e7a76ea84d9a4d2c67b35a9b2346fb5103`

```dockerfile
```

-	Layers:
	-	`sha256:b52e6cf1618fb62553ed8f367737b2630d2e12594eb7c14cf1732248cafd7779`  
		Last Modified: Wed, 02 Jul 2025 15:34:37 GMT  
		Size: 6.8 MB (6792359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8d8fb99e4d18bf9cf3de9a05e716d89a498f73855982f769e18f9338ab8d502`  
		Last Modified: Wed, 02 Jul 2025 15:34:38 GMT  
		Size: 19.2 KB (19210 bytes)  
		MIME: application/vnd.in-toto+json
