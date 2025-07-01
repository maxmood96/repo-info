## `clojure:lein-2.11.2-trixie`

```console
$ docker pull clojure@sha256:65f1203755ccaf6faf6e1de86ecca424ff88cfc7bbcb3cf868e9a47e7135297c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:lein-2.11.2-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:8349e64a97001b207e0c8501de0136cd34bc490c50fa3a4123815690d88b52c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.9 MB (277928750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6216551f4e0da7934b26ee6c6ed4dde7ce9dd7fea7b5af383ac770f46ed3c94`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
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
	-	`sha256:b72fed6e2775feec9291a4bd4b416f996dfc503eda11eaa00def55711302b4ce`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 49.3 MB (49263877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeeb77ea9ffc1619c7a4e3ecbb32fcb20777aaef5631a80b7022d896153638c4`  
		Last Modified: Tue, 01 Jul 2025 13:21:45 GMT  
		Size: 157.6 MB (157634503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347c4857cfffec40cbfad45bf6337e1642ed080ff16e9d4d2f689bf6946eda34`  
		Last Modified: Tue, 01 Jul 2025 13:22:04 GMT  
		Size: 66.5 MB (66515743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8612af22bdfb90b5f45fa45ec498300753160b01b43d9f4976bec06306db5eb0`  
		Last Modified: Tue, 01 Jul 2025 13:22:07 GMT  
		Size: 4.5 MB (4514199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e9b3dcff49a05d41aa8b420b9d90aed488e2894996103a2e1ba03cc5ec0395`  
		Last Modified: Tue, 01 Jul 2025 13:22:07 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.11.2-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d44f3732d05f8e5734375a054d83f680ea2501a5b9809ad9be22031aaec3101f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6470680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0014d43370486c2bddad45839ac18be554c6eb701d5659e7e80a9ffa8852a57e`

```dockerfile
```

-	Layers:
	-	`sha256:549f5566dc897356fc93ee696964d63e15cffddb8d2fd76e4f1453c69db6e28f`  
		Last Modified: Tue, 01 Jul 2025 06:34:58 GMT  
		Size: 6.5 MB (6451643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a00f931a4a15dee821e56cb3745ce3aedee9b3035c1964ce84edf101981ddb6f`  
		Last Modified: Tue, 01 Jul 2025 06:34:58 GMT  
		Size: 19.0 KB (19037 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.11.2-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:92eef3f77a4b21887e6eea56017db030478e3761de015b86831efeff2b439a45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.5 MB (276535208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6361155b776295e990f2b0df53ee1c959d6b54851d28091aef463f144d6fdbc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1751241600'
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
	-	`sha256:2581a046e315a4b3013d50a17da46bcffbba144014a55d733fa55c3bafc6b7ab`  
		Last Modified: Tue, 01 Jul 2025 01:18:05 GMT  
		Size: 49.6 MB (49630154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b9e80def4c9a1d31012db33fa85b62b5dd56fca51ed6af66eefb9d462a783e`  
		Last Modified: Tue, 01 Jul 2025 12:30:48 GMT  
		Size: 155.9 MB (155928808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f14b1fc71f031fa5e7221cb1ec85c0c6a7f13bc3016b972a9952bf6fc3f1b8`  
		Last Modified: Tue, 01 Jul 2025 12:31:15 GMT  
		Size: 66.5 MB (66461683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0711e226b877e8941988c278864e7c21dddc556a91b9d26ffdbbb217e11668b`  
		Last Modified: Tue, 01 Jul 2025 12:31:00 GMT  
		Size: 4.5 MB (4514136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faab7eed6bf23cac8de5fb16a6bc834634c6a21a2187d9dc8880fb2c9250b94`  
		Last Modified: Tue, 01 Jul 2025 12:30:59 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.11.2-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a09af6f394c143d60d1416397299dd582b76b122a59ef9bdc64ddf3bc88980fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6477812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8b1c39814b2b330cb703784a8059d742eba01e8cbc1da4d2ace5e469ddbce0`

```dockerfile
```

-	Layers:
	-	`sha256:72762fb990cb2fdf68e96a168a1c6d4a2f0b607b7ebfdf7db16db77cf02b9053`  
		Last Modified: Tue, 01 Jul 2025 15:34:45 GMT  
		Size: 6.5 MB (6458630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c597790c36a173b7f89ec11ac0adf823a9463be1059d79073fa3d145943feaac`  
		Last Modified: Tue, 01 Jul 2025 15:34:46 GMT  
		Size: 19.2 KB (19182 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.11.2-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:50ff70f44b48ebc162c5110d3f5953ab3180c18ed500f04da23c3cb112075156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.9 MB (286938360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e2be352bff14de6ab677c8dfadb250da0ae957cb798c8cbd115798f1145b47c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
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
	-	`sha256:5c6a246a80c20351fe842a314b6b3f8561a5ceaea736decf36fe380b29e53224`  
		Last Modified: Tue, 01 Jul 2025 01:18:57 GMT  
		Size: 53.1 MB (53097236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc7c6d506806bd280e9e75eeb1542eb6e3a8fda98921026f2d537f223a0edc2`  
		Last Modified: Tue, 01 Jul 2025 13:32:25 GMT  
		Size: 157.8 MB (157804905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0442e14dbb52197d54e3e3d85046afad743fa0b0aa4557fdf27324305a3954`  
		Last Modified: Tue, 01 Jul 2025 09:01:08 GMT  
		Size: 71.5 MB (71521648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb14985c1f18feeec359d823f45ef9aac118b11427e4080508ae929095dc6ba3`  
		Last Modified: Tue, 01 Jul 2025 09:01:05 GMT  
		Size: 4.5 MB (4514142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbf25981f9aa158bb3efd2e0bb22d809411cb6fb1896c1bc1745f1258b6f3fac`  
		Last Modified: Tue, 01 Jul 2025 09:01:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.11.2-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3dbd34edbc7901bbe9d45e7473156d52b93a2bcace8a04c9468702b3e215b440
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6474856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89360056d0a74bcd7579160822a6b9330457c0abe2518d21dfc8330ffe4a5c63`

```dockerfile
```

-	Layers:
	-	`sha256:e5d9ffbcca9cd1143232df65372d671e2c0dab2d14a36b154aa0f562f5da26e2`  
		Last Modified: Tue, 01 Jul 2025 09:35:05 GMT  
		Size: 6.5 MB (6455763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4ea8f2519dd2687cd0dbdfba62c7f8f2c7e7a1576359749bf7bae66cd71f99e`  
		Last Modified: Tue, 01 Jul 2025 09:35:06 GMT  
		Size: 19.1 KB (19093 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.11.2-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:14c495f2f4f7d75155222b2288575697f125e4cabdcd3f0060ba892f6108e1bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.3 MB (271347994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d09e059e16a389f2eda3530799a1eaa0c7b8148f4a4fe72db0a9c044f8f1b1c0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1751241600'
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
	-	`sha256:a19cda6d0aca0ae93b23898ddaa4518ab5077c7011f945c7a7e4a2cacb08ca5f`  
		Last Modified: Tue, 01 Jul 2025 01:23:18 GMT  
		Size: 47.8 MB (47750158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e076e085e4924513404df674a4b5cdd11b691d0a99549b6d4e3c46e86877f1`  
		Last Modified: Tue, 01 Jul 2025 03:02:40 GMT  
		Size: 153.4 MB (153449649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64236ec3b9693317967042b3c1ede01da19a17437e6494410b123df37020b359`  
		Last Modified: Tue, 01 Jul 2025 03:03:06 GMT  
		Size: 65.6 MB (65633518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1115b73ce5915fa77da467b56694929a37e1589dab3b91dfef0344b2516507`  
		Last Modified: Tue, 01 Jul 2025 03:02:54 GMT  
		Size: 4.5 MB (4514241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2da84c6dfb905102d586efce0131f847fb774e8814a10c968c28dff6b718500f`  
		Last Modified: Tue, 01 Jul 2025 03:02:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.11.2-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7b5d794ff1036191b4620c92466adf4fd7fe9ef79f9420cb358e1e9bffb4cd8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6458569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67139eee8aec154ab83e374cb9cc0923d4b18f1f1108a7551ba3813f6ea92b00`

```dockerfile
```

-	Layers:
	-	`sha256:5e476829d6d472ecc0349b3853289e7d884c240c461d2fb61aca835f0cc3334e`  
		Last Modified: Tue, 01 Jul 2025 03:34:42 GMT  
		Size: 6.4 MB (6439477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aedc61d5c7d6c7aea8b75e9f52fae314ec85b14a8681d32a219f0e76b7e970cf`  
		Last Modified: Tue, 01 Jul 2025 03:34:43 GMT  
		Size: 19.1 KB (19092 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.11.2-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:264e914d81e7e5efd888d7d0a207b34e1c3241049c6a5ac4192b3ee65b563497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.3 MB (268262091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66cbec53fa19ad7ba24b2366834c663ea3c99e45cca837df9275f67ca9f6ddec`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1751241600'
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
	-	`sha256:48de1d8f52c0a2a00375babc11bf69628b8225862d3b6ebbb2205e4ae2f3e96a`  
		Last Modified: Tue, 01 Jul 2025 01:19:00 GMT  
		Size: 49.3 MB (49343660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e01cf6c04a398e587786425ca5ff74d6a15f413fa4bc6373eda72ad291890c5`  
		Last Modified: Tue, 01 Jul 2025 13:21:29 GMT  
		Size: 146.9 MB (146911003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a066039ce21d8910ee16da41714545b7cca5a65e967fe530bb723b52f1af4e6`  
		Last Modified: Tue, 01 Jul 2025 08:19:24 GMT  
		Size: 67.5 MB (67492832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab056ec2d2cdfa0fd7b41e566c6f5f4da76d1014ed37e491a3299371e3148c06`  
		Last Modified: Tue, 01 Jul 2025 08:19:17 GMT  
		Size: 4.5 MB (4514169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832b4d3534392127dad117ce574783d8e78e582037111cfab934673eb9ffb34f`  
		Last Modified: Tue, 01 Jul 2025 08:19:15 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.11.2-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:baa8e08d0fa0d1c4e5563a23fae04e7714425098c9757701c22bc588d8fd4778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6466657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d29d3933fc914fd2fe7c9e943310f7f0eda61cc64d75790911eeb15c0f0b32`

```dockerfile
```

-	Layers:
	-	`sha256:44c348412f867916c60375e1ff7fcfdb14335cd3444864ef6c90e8eb36c65424`  
		Last Modified: Tue, 01 Jul 2025 09:35:14 GMT  
		Size: 6.4 MB (6447620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1aaf5cc13d0b3de4699afb91481c0b7cd58035596babc8841435afcc287cadc0`  
		Last Modified: Tue, 01 Jul 2025 09:35:15 GMT  
		Size: 19.0 KB (19037 bytes)  
		MIME: application/vnd.in-toto+json
