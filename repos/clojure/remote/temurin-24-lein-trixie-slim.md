## `clojure:temurin-24-lein-trixie-slim`

```console
$ docker pull clojure@sha256:f70725623afe8d3adf7c98b24476a7376156fb63946f96a2e089c8885548dc4d
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

### `clojure:temurin-24-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:09f8818b12dda10dd9e57884cae01f97d090270eb6bf1a9064587505ca5d3756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140714189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf60e1e5068435919e14c1b39acce39c1e75163eafdd886eafa68d00ee9a9015`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e80f2b9cb74063549d25b23ac8027d88d1f5b5e8044d137af70c197956674d`  
		Last Modified: Sat, 13 Sep 2025 00:10:38 GMT  
		Size: 90.0 MB (89975190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7052764e5d700e30cf8a4a089d58613c23f40ea5a0419b26b8dc12fb22dc27bc`  
		Last Modified: Sat, 13 Sep 2025 00:10:36 GMT  
		Size: 16.4 MB (16447373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2884e0ad195de0a969db8fec955f2824465f7f8679bd8c7777c897abde33ba0a`  
		Last Modified: Sat, 13 Sep 2025 00:10:35 GMT  
		Size: 4.5 MB (4517702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636176ee35f2998d96b00d0878145187c9222d536e946323bdab75ecfc5d2ecb`  
		Last Modified: Sat, 13 Sep 2025 00:10:35 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8f0e0ea1e3be43df3a15b0c9de149bbf1ea94be6012576e82c1f0706d979f25d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2332459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f1724cdd66241e20a647e1abd1c5653a9babc2f6f457d0702ed5d3991eefa2`

```dockerfile
```

-	Layers:
	-	`sha256:5b7aab9a38c4b16771be91e990f5bbaf0fc775ec14c4d6234f839ef53b642c37`  
		Last Modified: Sat, 13 Sep 2025 00:42:54 GMT  
		Size: 2.3 MB (2314036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:978c62d1fd0c94d23860dd35e049dccfeac54ffc1e978f77a0e2911ca3b320f9`  
		Last Modified: Sat, 13 Sep 2025 00:42:54 GMT  
		Size: 18.4 KB (18423 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:54eebd602baad3d201f8f6efc863ac8bde4cdfe6b9db637fd353a7dac1fa6d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.2 MB (140160878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c99ebe3535ab37274620b3cd8e2653c7971a2b2f6aff4f00795cc554f7142db5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8173011bcb8293eb2bf45b5cadf17673ca90c9859ba3dcbf1828b686706b0ce8`  
		Last Modified: Sat, 13 Sep 2025 00:17:35 GMT  
		Size: 89.1 MB (89092551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5958f71e8985d4c5d1ba77d99b6a1572f6b53e79744f62d432b335bc70ef4ae1`  
		Last Modified: Sat, 13 Sep 2025 00:17:28 GMT  
		Size: 16.4 MB (16413532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00cb2039e6fbf28830e81ee7e867f17f85379218a0a687f35ad748f6cac6320e`  
		Last Modified: Sat, 13 Sep 2025 00:17:27 GMT  
		Size: 4.5 MB (4517735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263f48deb5208f42a38c2d01f3f1047642b225d4274db6d1a0702843ca57c1d3`  
		Last Modified: Sat, 13 Sep 2025 00:17:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:73168ccf5cb62caf33a2fbd42611c1e0ca09604b867c20f5d2a77992d755b643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2332194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d309924c5e1c28461e29b310352b5b67a535c256b15f80adb747ac35fac20a2e`

```dockerfile
```

-	Layers:
	-	`sha256:c6f12b829fb7bd6e018a242f5e6ffdf1e34d0b807b70d2977744fca0228acf07`  
		Last Modified: Sat, 13 Sep 2025 03:40:58 GMT  
		Size: 2.3 MB (2313651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c40a67a5e272f881da08b8bd0a1511a0280eb76be172cc4dbdb4e03650589c4`  
		Last Modified: Sat, 13 Sep 2025 03:40:59 GMT  
		Size: 18.5 KB (18543 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:7f6fee4bca67f20dbe96b1fbb969741142d0a5a8b6ba4ff16eecacda90b94f07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.5 MB (144517134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea66c83cf8a4ed219e964afdfc073e8b39f2d38c0b1f7938a9847c771e33c2a3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab6532f47259b4baefc4644a9d2f6e61e29f5697fdc7617b9491b02a2197399`  
		Last Modified: Sat, 13 Sep 2025 03:55:52 GMT  
		Size: 89.9 MB (89918195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959da20e9b5770bb92f2d8f4c14fad723160ad88642b96429b9e46ab9bbd25d8`  
		Last Modified: Sat, 13 Sep 2025 03:55:49 GMT  
		Size: 16.5 MB (16486419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6faea1f4fa6d5312353b51fdc138d842dd6766cbabcccceeea524ddf57c4bc`  
		Last Modified: Sat, 13 Sep 2025 03:55:48 GMT  
		Size: 4.5 MB (4517739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384306a9a1363ec43edec0a317c2565d8d5c24bc40c924c4d55c4b37ae2fe382`  
		Last Modified: Sat, 13 Sep 2025 03:55:48 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d8a78a8b7f9928675c17fabe99b7d28699d2748289070a04be61690931902a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde49d81cc123f12fddc27901fbb99b611d775678d8cbba693bd51fc01d90f43`

```dockerfile
```

-	Layers:
	-	`sha256:374d930aa9800380ab5c77fb577f334aac5c2ef772a996c4ad16b6ed580f79bd`  
		Last Modified: Sat, 13 Sep 2025 06:40:15 GMT  
		Size: 2.3 MB (2316314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db8fb5b1c66005b8d79933bfdf8f21427cc230043d397d8b7c325512680d62fb`  
		Last Modified: Sat, 13 Sep 2025 06:40:16 GMT  
		Size: 18.5 KB (18467 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:9c672561cead50b2acec4cd747e87701fec9af319f3097b63de2dbd59d91f6eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.5 MB (173481905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7f474a15a7a3e52f4c4b43f3a15224a5f43bedb9ed35aa0793d603d7d7ac8a8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 26 Aug 2025 17:11:52 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 26 Aug 2025 17:11:52 GMT
ENV LEIN_ROOT=1
# Tue, 26 Aug 2025 17:11:52 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e5802301b5e43e1938fc4d3c6e84951cc5aa9881aa25362f5d2cc7bb7be4c9e`  
		Last Modified: Fri, 05 Sep 2025 19:32:11 GMT  
		Size: 87.7 MB (87670403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751afe25195e774385cd6fb0c2d3f6391a399baf7d143cfe9cd33a282b5a882e`  
		Last Modified: Fri, 05 Sep 2025 19:32:12 GMT  
		Size: 53.0 MB (53025204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605515f26bd424c85cb9821e56702a3da59e7d175dbe667e11559dc5effad28e`  
		Last Modified: Fri, 05 Sep 2025 19:32:04 GMT  
		Size: 4.5 MB (4514244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e00aaab22e4668985c4a013ba2eab3f1af85533316b4e94c741181da4b41b7`  
		Last Modified: Fri, 05 Sep 2025 19:32:03 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0e6cc6d99eb2d6562b1b7ed2507cbeab4842c750d858ab5aab8df8e5cb35575a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4235981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6903531418fe32c078d2bf07f9a1c4642fe7d3fd92b86886de38a368cd96bee4`

```dockerfile
```

-	Layers:
	-	`sha256:be2aea3c9386e01ee11e5029b214dd5cbd4d85ecbd9499376891e085e12bc2fc`  
		Last Modified: Fri, 05 Sep 2025 21:37:47 GMT  
		Size: 4.2 MB (4217506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:878a6223f804be9e24d990391d0b786da651f9d7fca9bd7816d9a3fce04a0947`  
		Last Modified: Fri, 05 Sep 2025 21:37:48 GMT  
		Size: 18.5 KB (18475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:7c7154db83aac3617f780a317aaf389c7648dd0e2b2538b6ae83e279edef4670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136061192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddeca6dd957678c582edf645b2979cab9862130abfe9217e1bf21b9f0f5c352e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 12 Sep 2025 20:29:18 GMT
ENV LEIN_ROOT=1
# Fri, 12 Sep 2025 20:29:18 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001f899a0035f92502563c4bdaed319ad7f7d929742ec096c4bb55d3733e094a`  
		Last Modified: Sat, 13 Sep 2025 03:21:52 GMT  
		Size: 85.2 MB (85226409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa3d24e621e1005fa0cfb019245623f400f697ba3b7438ea66189c20d2cefba`  
		Last Modified: Sat, 13 Sep 2025 03:21:34 GMT  
		Size: 16.5 MB (16483705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3b0f23381791727790ab9c1df00560e246299487d4e717c169a1f1b95e9b20`  
		Last Modified: Sat, 13 Sep 2025 03:21:30 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1fd59a5ab8a04f9c0b14256f2a6ee6654114ca6d8a230c6b4c5181a0a589cc`  
		Last Modified: Sat, 13 Sep 2025 03:21:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:44927564358142ad1c3f5b512674c2e40d8a4762d2d48dc73179e559821a0ee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2331434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92c1de435c48279e91d8aec0f5166ba7ba29a5bea893bb44ab7da92e4cfe2192`

```dockerfile
```

-	Layers:
	-	`sha256:34f7fa74ed060265167c58bfab1c7834c624bea31d7fdc7c593ad19882542660`  
		Last Modified: Sat, 13 Sep 2025 06:40:20 GMT  
		Size: 2.3 MB (2313011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bb0fb97402298ee3da4c8e260ebc286d0b88e08c2a97a0efecc121542e1cefc`  
		Last Modified: Sat, 13 Sep 2025 06:40:21 GMT  
		Size: 18.4 KB (18423 bytes)  
		MIME: application/vnd.in-toto+json
