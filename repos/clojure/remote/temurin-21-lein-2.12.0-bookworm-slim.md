## `clojure:temurin-21-lein-2.12.0-bookworm-slim`

```console
$ docker pull clojure@sha256:40bf1a33a22bcd896a4f2838b9dd2ba843a52ddc9f209d64faf1203b2900cdcd
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
$ docker pull clojure@sha256:6000fb6fac21c3bebccc777bdbb611c34de9b0e556197b3f5b2ee100c137fbcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.4 MB (208370330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ae41a9c995ccfce32ccf294233eea9c57abd60ccbdd163ff8c85eb91ff2eba`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:15:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:15:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:15:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:15:26 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:15:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:15:26 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:15:40 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:15:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:15:40 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:15:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:15:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:15:42 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:15:42 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee62c887e7b7775bb162c253a68aad15df7f355f95b99a1fa980057d0146c51`  
		Last Modified: Tue, 07 Apr 2026 03:16:03 GMT  
		Size: 157.9 MB (157857048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeaf24d6ba290e071ba1fe89ae2f0dff752765a33e4420c6a44267a551e417e7`  
		Last Modified: Tue, 07 Apr 2026 03:15:59 GMT  
		Size: 17.8 MB (17758770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e15b5928973de60afed41a70cd770417c9aea1937c8f4f1170073f728c2f59`  
		Last Modified: Tue, 07 Apr 2026 03:15:58 GMT  
		Size: 4.5 MB (4517752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01bc54877f0781f37bd0bbb14f1a742b78136850559c83ed17463d08c5995ba`  
		Last Modified: Tue, 07 Apr 2026 03:15:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a62714c6a9f701cfb7279830f44746ad083ddb70c307f0457c013ab9246e7cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bfffaee02ab0ce18ddc756bfe3a2c52c4990932778be59913421c45a56679d8`

```dockerfile
```

-	Layers:
	-	`sha256:83f06d51068629c3c5d5832969625bb221ce22b913ce7660ac5021c4a164e573`  
		Last Modified: Tue, 07 Apr 2026 03:15:58 GMT  
		Size: 2.7 MB (2731902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c0dedca7d9085e47e901a8422548fa8bcc37b835faf1072fe3ff008c704cba3`  
		Last Modified: Tue, 07 Apr 2026 03:15:58 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:69a58a65ca46a53733cbbf947b86910da24a465182c2c22def1506ddb93f853c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.4 MB (206359141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf24c029ed204f40c051163b70ce804189937ea6705b526cebc12b7292cc9873`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 03:26:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:26:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:26:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:26:16 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 03:26:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 03:26:16 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:26:29 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 03:26:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 03:26:29 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 03:26:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 03:26:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:26:31 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:26:31 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebe053e45f6932f9fb53d2bc3e61c0c967170a0a65e27e2217cd550622a4b4f`  
		Last Modified: Tue, 07 Apr 2026 03:26:53 GMT  
		Size: 156.1 MB (156133058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a8f0bd8fd2c15bdafc053910e5e7b89883b1fb1e9f8263ef35e216c799df81`  
		Last Modified: Tue, 07 Apr 2026 03:26:50 GMT  
		Size: 17.6 MB (17591774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bda30d05e2468e550968cd137eda4e8c6f781938011955c1b622cf4f01540977`  
		Last Modified: Tue, 07 Apr 2026 03:26:49 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889c6fd76b3411970d2a24cec867b025cb9438f0fd378953cc4a71dea37de48d`  
		Last Modified: Tue, 07 Apr 2026 03:26:49 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0ffec7f0d524a0e868fd32eb7671c6f4d2489675dd99d3418fa85ffa032356fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2750041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011448411fb2ff2adad87b6bd15591553455a38c60b17921e15cd7eec120c3e9`

```dockerfile
```

-	Layers:
	-	`sha256:dfa4d8ddeaa2fd1b781f120fc051df09c8e9f94c4e7ef674de6b5647d07dc0e9`  
		Last Modified: Tue, 07 Apr 2026 03:26:50 GMT  
		Size: 2.7 MB (2731517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:103d58e3dae7ae7c7c870fee701b3658f6ab2988b27fac3f8e009968c9463d4a`  
		Last Modified: Tue, 07 Apr 2026 03:26:49 GMT  
		Size: 18.5 KB (18524 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:8243c0b1dadc01dfe52e667ac9be749343a3a014a8d310e74b721f0ef7b93c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212535116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27d0ceab1957b5cd59fae5de8fe93750e68464b0c2ea32f2df86e544ccd0f90`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 18:34:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:34:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:34:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:34:34 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 18:34:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 18:34:34 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:35:15 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 18:35:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 18:35:15 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 18:35:19 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 18:35:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 18:35:20 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 18:35:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7a0392d98c02d4219c67a8e3d3837c1ac5d4af6836b9264bdd6c427cc7a24f76`  
		Last Modified: Mon, 16 Mar 2026 21:51:26 GMT  
		Size: 32.1 MB (32078368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08aa22040562fcd55bbeb76a004a8c37c790885d218b8fc4c0ba2c08d72b2f3`  
		Last Modified: Tue, 17 Mar 2026 18:36:05 GMT  
		Size: 158.0 MB (157977514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2eece990e92df31d2e852e56f82cb0bd5c737bc773f31d4e15ac3e60a6a5a7c`  
		Last Modified: Tue, 17 Mar 2026 18:36:01 GMT  
		Size: 18.0 MB (17961057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f621f9f3a43486340774b7088e98cebfdd6a82d0dceee0c56ff6f588c11346d`  
		Last Modified: Tue, 17 Mar 2026 18:36:01 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eafa5721227ea8c5d0edc8d59e3da6a2ecbbe327662779c4e2e7f5f232eaf7e`  
		Last Modified: Tue, 17 Mar 2026 18:36:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:97b176f9936569d23d084773dd38fc2298757c7dce0472694633e216eaf2b28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2752182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1490933a7cd17184c4306af183bfae426369a3ac9ec7574dcc5d77924cd56bb0`

```dockerfile
```

-	Layers:
	-	`sha256:296d8b3107fe43e140dce8479793a0a78aa062a45db8d717378701c32418bd52`  
		Last Modified: Tue, 17 Mar 2026 18:36:00 GMT  
		Size: 2.7 MB (2733735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25a8637319da0fbe118bcc918530acb847f38e5b9820922792479b695e35a42d`  
		Last Modified: Tue, 17 Mar 2026 18:36:00 GMT  
		Size: 18.4 KB (18447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:360d5621d3087d565fcf13ad27a2af946e71380a7060b1e856d78b049e8d3192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 MB (195936068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff22b601b1cc531cc2971d8bfff52e0c50756aff156e0fc3971e45be3bab0e7a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 05:44:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:44:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:44:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:44:24 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 07 Apr 2026 05:44:24 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 07 Apr 2026 05:44:24 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:44:35 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 07 Apr 2026 05:44:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 07 Apr 2026 05:44:35 GMT
ENV LEIN_ROOT=1
# Tue, 07 Apr 2026 05:44:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 07 Apr 2026 05:44:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 05:44:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 05:44:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e7319be332fb7a0de839eaf561970a3169c636f32f76719336639dcb74ddbe`  
		Last Modified: Tue, 07 Apr 2026 05:45:06 GMT  
		Size: 147.1 MB (147105212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c8695870041696b0baef42f660e35174b4d3ded26cdef965aa550003e74ad6`  
		Last Modified: Tue, 07 Apr 2026 05:45:03 GMT  
		Size: 17.4 MB (17421088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69837b1082e7caa5909ef7ee562802cb68a920b97c3745fd6dcb6ff6ae63cfb1`  
		Last Modified: Tue, 07 Apr 2026 05:45:03 GMT  
		Size: 4.5 MB (4517704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43738b78ff262fcbc2051add1bd8c3a2e83167682d93a2dc8ebdf86ac07a982f`  
		Last Modified: Tue, 07 Apr 2026 05:45:03 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e5f42724f93846e415b4e0a7c4d5d114f05ed412fdddbcdf8577b78db529f618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2742118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c7d2de312e7e2b1f9caad837ce5d447cefb4738a2bd08f829adc83f0b54d10`

```dockerfile
```

-	Layers:
	-	`sha256:cf448a6bf315f630c3a21382744f84ba97f7146650280b3c12934b5275eae531`  
		Last Modified: Tue, 07 Apr 2026 05:45:03 GMT  
		Size: 2.7 MB (2723716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0174745aab370acb3a4a284fed2ab8dd06b5b71957dfb2dee63eda646f9bd6ba`  
		Last Modified: Tue, 07 Apr 2026 05:45:03 GMT  
		Size: 18.4 KB (18402 bytes)  
		MIME: application/vnd.in-toto+json
