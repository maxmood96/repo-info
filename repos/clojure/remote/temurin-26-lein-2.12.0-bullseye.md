## `clojure:temurin-26-lein-2.12.0-bullseye`

```console
$ docker pull clojure@sha256:2aa18d48d7c89a718adf50ece24636ad8d3135db57edde666a8fd195c5352c3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-lein-2.12.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:84ff8ddab17a2c4b0081e86d0014eafafd458eafed458f7078f3ea3cb7b99fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169366172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbff7dd5f77edbb513be29b440bca3f2c4ff1d88b15ca844bee8c744a70e75ad`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Thu, 09 Apr 2026 23:36:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Apr 2026 23:36:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 09 Apr 2026 23:36:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Apr 2026 23:36:46 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 09 Apr 2026 23:36:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 09 Apr 2026 23:36:47 GMT
WORKDIR /tmp
# Thu, 09 Apr 2026 23:37:00 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 09 Apr 2026 23:37:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 09 Apr 2026 23:37:00 GMT
ENV LEIN_ROOT=1
# Thu, 09 Apr 2026 23:37:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 09 Apr 2026 23:37:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 09 Apr 2026 23:37:01 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 09 Apr 2026 23:37:01 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c4be10a33f1ff15e7adf2910283fafda5370fee38703fef98de5c1a5e3f8c1`  
		Last Modified: Thu, 09 Apr 2026 23:37:20 GMT  
		Size: 94.5 MB (94455691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7398fb8cd6ff1ab920697a4c8c44135dbe5e91f707d9eb9e5be00e756db3837`  
		Last Modified: Thu, 09 Apr 2026 23:37:18 GMT  
		Size: 16.6 MB (16629550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0bbfc6dc889d05ceee62020f48bc4745dca1ee649fc072dfefbdfb60ec6cba`  
		Last Modified: Thu, 09 Apr 2026 23:37:17 GMT  
		Size: 4.5 MB (4517709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b6adadd136ff852e311af6402e7f349856c8fabfadd6617c07ae5851db5841`  
		Last Modified: Thu, 09 Apr 2026 23:37:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b6ef29399718db026f841035e873ce5d3827a25d69114ba8dd1ae0869a803f5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4469727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf41bcf9bb204d5fac2ecc99aee785f908bb665499f3037964752f3238f7db5a`

```dockerfile
```

-	Layers:
	-	`sha256:5fc9e61d45c3429f744fbb8463f065ac2e9cf1f47439291f78ebc2ded4a6fbf9`  
		Last Modified: Thu, 09 Apr 2026 23:37:17 GMT  
		Size: 4.5 MB (4451366 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e8097df56940e859a35e82dcc531f2f3f4fe20cb24e50232010b7ed6d457bf6`  
		Last Modified: Thu, 09 Apr 2026 23:37:17 GMT  
		Size: 18.4 KB (18361 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-2.12.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:22eab0070c7691eb5cfd70f4c5dde6c30f500fee81162e021f57e5910af1217f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166777494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3905ad1729532861bfbb999795957b0a07b5d3f2d706e71cf70e23ccbcfc9e9f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Thu, 09 Apr 2026 23:36:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Apr 2026 23:36:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 09 Apr 2026 23:36:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Apr 2026 23:36:23 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 09 Apr 2026 23:36:23 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 09 Apr 2026 23:36:23 GMT
WORKDIR /tmp
# Thu, 09 Apr 2026 23:36:37 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 09 Apr 2026 23:36:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 09 Apr 2026 23:36:37 GMT
ENV LEIN_ROOT=1
# Thu, 09 Apr 2026 23:36:38 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 09 Apr 2026 23:36:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 09 Apr 2026 23:36:38 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 09 Apr 2026 23:36:38 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb1271af4b4f48118ef33d93b7b304957babdc592cfed3e1e27a01c318d85a8`  
		Last Modified: Thu, 09 Apr 2026 23:37:02 GMT  
		Size: 93.4 MB (93395170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6075766221254c74e08bd21755c1be3d693a21ec0867f8d5d154e72839aa2173`  
		Last Modified: Thu, 09 Apr 2026 23:36:56 GMT  
		Size: 16.6 MB (16616568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f40ea6da4ce4f6ba0d27f238c7539bcd2d8f1150800cbddd3de3391ab72b1e`  
		Last Modified: Thu, 09 Apr 2026 23:36:55 GMT  
		Size: 4.5 MB (4517711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186712124de96f0c70313dca4a790ff6af38fcb035d3c752fc4b3e35d82bdef5`  
		Last Modified: Thu, 09 Apr 2026 23:36:55 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:ac6d44adfd7f5ced6778a33772d28c03d95871c3253147f7582271735e885884
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4468819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70752e28c71fed361f5bd610dd60cfff75b86c8afe487d34d86e70887c3ce895`

```dockerfile
```

-	Layers:
	-	`sha256:33fcc1c457001e9ffad08209273bbae73071638007ab13ba0165e520950b1c08`  
		Last Modified: Thu, 09 Apr 2026 23:36:55 GMT  
		Size: 4.5 MB (4450337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c23b6aebff5740b3e56e5e021dfe623195a2d72d337bd032626c1d3e3b9ec88`  
		Last Modified: Thu, 09 Apr 2026 23:36:55 GMT  
		Size: 18.5 KB (18482 bytes)  
		MIME: application/vnd.in-toto+json
