## `clojure:temurin-26-lein-2.12.0-bullseye`

```console
$ docker pull clojure@sha256:b85cb7343423ce52587e4179a442eac383113a3e36258fbd308a3fd213ed7997
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-lein-2.12.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:3618b197ffe596b7449880615eeabdf3a6e37466188ee222e1fa6fd1a9ed8245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169366282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3db29bab13dd673b6aad890e75611773d9c6989f125c2663b3fb1ef4584a9ead`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:07:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:07:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:07:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:07:32 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:07:32 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:07:32 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:07:47 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:07:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:07:47 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:07:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:07:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:07:48 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:07:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85b35dda053cd1566393489fc889d72a36ba6e348cc62b9d59b89c78629c346`  
		Last Modified: Wed, 15 Apr 2026 22:08:09 GMT  
		Size: 94.5 MB (94455691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe5b3e0df04cd3cf349b914c77028e59668600535563f34f568abe57b49147b`  
		Last Modified: Wed, 15 Apr 2026 22:08:07 GMT  
		Size: 16.6 MB (16629642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7eea90cdb5f233a9685d9b28f6d3810b4f4a031462155fe6d63a28cda82b3d`  
		Last Modified: Wed, 15 Apr 2026 22:08:06 GMT  
		Size: 4.5 MB (4517728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee7f5aea94615d460b2ca688f63220a7f88bb490e5ed5fe32328b62f6c2cacb`  
		Last Modified: Wed, 15 Apr 2026 22:08:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c7eabba9bff0ec0b6bab3d96d30bbb393916a554143fd931662f4e2e6706665f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4469726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aeddaf7c46da351fd1108ee2c9b3c18149c41593d99f54c5d87b1284b49659a`

```dockerfile
```

-	Layers:
	-	`sha256:705837c9ebc6a7b9be1877a125447803c6ecf8b0127d3d6d03c20c2adf3281b3`  
		Last Modified: Wed, 15 Apr 2026 22:08:06 GMT  
		Size: 4.5 MB (4451366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15d8285c386f58235b3de19a722675052bb0a295c33d2554b5a02a0c0a77886d`  
		Last Modified: Wed, 15 Apr 2026 22:08:06 GMT  
		Size: 18.4 KB (18360 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:21519782a6a688f3189a488adbcbc8ae78152ab5dcbde563c3ec845659738642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166777474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d3053c5c068b95e8ba638c933a4323e841f16b013922b881a67487f396ed05`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:19:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:19:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:19:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:19:08 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:19:08 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:19:08 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:19:22 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:19:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:19:22 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:19:24 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:19:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:19:24 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:19:24 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4f31b4168371b96faf1b996c50cccf6ff60ee172d8c70e0cd02c4e5706106e`  
		Last Modified: Wed, 15 Apr 2026 22:19:45 GMT  
		Size: 93.4 MB (93395215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b472fca6dd89f61532c2dc745ea6a02759e5f44683412d6883d22b680b94b7`  
		Last Modified: Wed, 15 Apr 2026 22:19:42 GMT  
		Size: 16.6 MB (16616471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d6cb7544194f24c0c3372f9eaa47d719eb9bb532d43f74457d52e855003714`  
		Last Modified: Wed, 15 Apr 2026 22:19:42 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b6e113ec8668eb031677354b353a170a31386b93889217aa1f4283091c6422b`  
		Last Modified: Wed, 15 Apr 2026 22:19:41 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a247d8c8c2ede193ace3d81b4716addf2b548933694f39640706aed1d2860ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4468819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caf2a8cd4b72541cb6a1de4107bd9cea7a52133df28b9a247d70607855e1bb3d`

```dockerfile
```

-	Layers:
	-	`sha256:eca3b6b907bca6ad73cd91d655522f1524aa8f5aa7816904163fb485f2232f91`  
		Last Modified: Wed, 15 Apr 2026 22:19:42 GMT  
		Size: 4.5 MB (4450337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b6991125fa84bc27e8ee6e3b13934355f9f85320c4c1a04e94c257930c1d7d1`  
		Last Modified: Wed, 15 Apr 2026 22:19:41 GMT  
		Size: 18.5 KB (18482 bytes)  
		MIME: application/vnd.in-toto+json
