## `clojure:lein-trixie-slim`

```console
$ docker pull clojure@sha256:5e41879bc73ac533e2392ade732c0d609d550799a13ff30e3d0e32530548f9ed
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

### `clojure:lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5391d4101ce0a4344f541f203cfbae5450f1687c8c77b5ecc5b6010e55d85300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142789072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb261d3fd0d7048ab928d2426cf554c60ab0e07cf2b21adb920d015ba7dac24`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:55:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:55:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:55:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:55:42 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:55:42 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:55:42 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:55:57 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:55:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:55:57 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:55:59 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:55:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:55:59 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:55:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88e4ea9c7610eae94c40db25cf311aa715f53cbd47ae73b7b39fd221c3dc316`  
		Last Modified: Fri, 14 Nov 2025 00:56:31 GMT  
		Size: 92.0 MB (92045298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8691373b699d3d4d3ee6ae0596e8462dd2d03795b949dd28e455e45a355f578`  
		Last Modified: Fri, 14 Nov 2025 00:56:24 GMT  
		Size: 16.4 MB (16447482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831326fc8d96f564db5fcdb0931008a3b9629ea2cc75d77a1d3d2dcae2b288fc`  
		Last Modified: Fri, 14 Nov 2025 00:56:22 GMT  
		Size: 4.5 MB (4517760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcde40df2ccc94f6211102d41c020e0d4d2918a653aae7c36336e79c633bb1ff`  
		Last Modified: Fri, 14 Nov 2025 00:56:22 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:84916ff737ce03442fb28b66d213d443c0ea35a607a1d0a2b9c6f60ac4865521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510cead42c7ae7fc595362f1fafe62731938db789adcc7a1c3bc46c3da62b503`

```dockerfile
```

-	Layers:
	-	`sha256:6961aa062be330e2795b7433f6f8843310cf22c409b81bc425d6e42fb8fca345`  
		Last Modified: Fri, 14 Nov 2025 01:47:18 GMT  
		Size: 2.3 MB (2314760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0981a73497c3a091d70bcd2e27153d56491919b17e550edb5d4e0be52120fb2d`  
		Last Modified: Fri, 14 Nov 2025 01:47:19 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:280e4bdcdc42dbbdeda6c6277ad0de781d3591542172fb570849f0cb7a216580
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142126520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84dece784f2bf218246a1cb74ac6927bdc63e815d110b59ce7aff0afb7eb8688`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:57:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:57:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:57:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:57:59 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:57:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:57:59 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:58:15 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:58:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:58:15 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:58:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:58:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:58:17 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:58:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262cc0685394031f6ff3f3d0a86490a12fae03ec5c20c9024d342feed10288dd`  
		Last Modified: Fri, 14 Nov 2025 00:58:54 GMT  
		Size: 91.1 MB (91052512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0dc4cb261b42faa272543273d93e02a679029af51157ee72b89960e9d14d87`  
		Last Modified: Fri, 14 Nov 2025 00:58:42 GMT  
		Size: 16.4 MB (16413536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61e52f972a53978c4f3f1ec875e6c0d44ce7897898f7dfe855e12d66b2a520a`  
		Last Modified: Fri, 14 Nov 2025 00:58:41 GMT  
		Size: 4.5 MB (4517745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:507cb8cf59539e896fbb4754b66cad54c669652925f17b30f71b34a4550b2fdf`  
		Last Modified: Fri, 14 Nov 2025 00:58:41 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5771c05fcfdc0b79f50a684ba5019e73c176095d19d80190332d0e92abce6d33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ef99681b64dcf270cc3bf9b257a18e77baffdc1b463d793ba4689806b45d6f`

```dockerfile
```

-	Layers:
	-	`sha256:0eb83cbe39ead97c820e2fc5a2dd9a822ffd2086f77f2d3281c4e00cf50e5083`  
		Last Modified: Fri, 14 Nov 2025 01:47:23 GMT  
		Size: 2.3 MB (2314399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cb9d0ab2246f4e887ce746ed0d5c0ccd522a13a1eca1c020a5dcda2067049bd`  
		Last Modified: Fri, 14 Nov 2025 01:47:23 GMT  
		Size: 19.2 KB (19178 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:f1913b19873d8690aa52127246ac8efcc3d2d31c7dcf73974bc52208504fe821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.2 MB (146213973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0185f6eea76de4b9dd6a314ce5c1440e31d95134144b2fc68b16494414863a15`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 21:50:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 21:50:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 21:50:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 21:50:52 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 21:50:52 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 21:50:52 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 21:51:22 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 21:51:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 21:51:22 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 21:51:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 21:51:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 21:51:26 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 21:51:26 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cf4e8b84d3ef0d8674350cf270e37134e319d3eeaa20958d07a8901e83de35`  
		Last Modified: Sat, 08 Nov 2025 21:52:16 GMT  
		Size: 91.6 MB (91610755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146a1cd7ba04e5ae119adb9afea484923708d8ac63ef3d5149a6c3fb0f5c55e2`  
		Last Modified: Sat, 08 Nov 2025 21:52:10 GMT  
		Size: 16.5 MB (16486388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275eae78f6def346da47234cd053b60d406f577eaef7fec75f5a3194a4bf14f5`  
		Last Modified: Sat, 08 Nov 2025 21:52:09 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03bebacf9ef8babc2e78e5bf9ac09d6c511fde3f16ceacc533f9fe98c3b9eb6`  
		Last Modified: Sat, 08 Nov 2025 21:52:09 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5ff777b0b61bd25609a426c24207f24dcf4c04b334cbe26fffb22018519a5266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2336139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799ad4a8e925a472d0737045b56b5febd1b9e6d03137223117be85114c6fc887`

```dockerfile
```

-	Layers:
	-	`sha256:3244c279c1fe66de388722d3726be513c1c373baf488bfa2095562dfb90bea6a`  
		Last Modified: Sat, 08 Nov 2025 22:35:54 GMT  
		Size: 2.3 MB (2317050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbe301b80c82f2bff36c31c0169312ed88ad7a5e2c11a21ba0e24c0dadafc67a`  
		Last Modified: Sat, 08 Nov 2025 22:35:55 GMT  
		Size: 19.1 KB (19089 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:bcbd4b49a52200edaed85be8a6236599fdfbc176f40470914bf419857902b2f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139944898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf44a2113b2547bc225dd277881393b2d65cb60a5a6f6cafc3b98eb4f739bc8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Mon, 10 Nov 2025 04:37:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 10 Nov 2025 04:37:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 10 Nov 2025 04:37:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 04:37:43 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 10 Nov 2025 04:37:43 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 10 Nov 2025 04:37:43 GMT
WORKDIR /tmp
# Mon, 10 Nov 2025 04:39:12 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 10 Nov 2025 04:39:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 10 Nov 2025 04:39:12 GMT
ENV LEIN_ROOT=1
# Mon, 10 Nov 2025 04:39:28 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 10 Nov 2025 04:39:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 10 Nov 2025 04:39:28 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 10 Nov 2025 04:39:28 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65bdf934bab212db989f237b784a2a17e7c8de762196739b48dc1cdde3c370ef`  
		Last Modified: Mon, 10 Nov 2025 04:43:23 GMT  
		Size: 90.8 MB (90752912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20d63165d920c23ed4f83d5d33f3a33076315bcc405901922203b2a717fb31a`  
		Last Modified: Mon, 10 Nov 2025 04:43:23 GMT  
		Size: 16.4 MB (16397985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e12e5893287ee99a6bd04f57f514b07d017802dc505d6182d7f5c0b75f3a82`  
		Last Modified: Mon, 10 Nov 2025 04:43:22 GMT  
		Size: 4.5 MB (4517786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51df18ab90c283e0053a420d66e16b8d7d2374c1aae9451cf8e7d6b64cfb74d0`  
		Last Modified: Mon, 10 Nov 2025 04:43:22 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c2505073b51eaa0a83ab2df8586d9c24e9aa5d1352f3d63d874d0a07a569c8aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2325907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eecec62eaa26e2b0ba503d864782fef507446606651b8e55e985568e56299d7`

```dockerfile
```

-	Layers:
	-	`sha256:19d96c04a80d106adda2c1e35a5ec363fde20085f67c1a90483653779fea627b`  
		Last Modified: Mon, 10 Nov 2025 07:34:40 GMT  
		Size: 2.3 MB (2306817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:550e0a60f73421e88a23d1eb2b855191e14ec4301547815c41de60c24f01ee77`  
		Last Modified: Mon, 10 Nov 2025 07:34:40 GMT  
		Size: 19.1 KB (19090 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:d39b8d98022c00176aa312f4c751de9ecdd09ee9e7104b80b68749b98234ebf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.1 MB (139050051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6865925defa4c2c701d75099f7717b0b0cc5ea42818b64820241a2a35172be05`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 01:03:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 01:03:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 01:03:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:03:58 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 01:03:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 01:03:58 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 01:04:15 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 01:04:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 01:04:15 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 01:04:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 01:04:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 01:04:17 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 01:04:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68938204a636f823d8b918e7681930804615472d355c8f63462626916e8c77d3`  
		Last Modified: Fri, 14 Nov 2025 01:05:03 GMT  
		Size: 88.2 MB (88210741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d48a0e42f41a603f4157f708814c5b3efc370de7fe84d135ab1a4de25a99c75`  
		Last Modified: Fri, 14 Nov 2025 01:04:48 GMT  
		Size: 16.5 MB (16483743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1edcaf3bf8c2643d28260aa4d4a7201ddc01c68b728f875670b5b33bcbd773d`  
		Last Modified: Fri, 14 Nov 2025 01:04:45 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9513280532d676da26d67afa8a35c4e72828b70be0c767300fd5373a9165f0ad`  
		Last Modified: Fri, 14 Nov 2025 01:04:45 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f36ee78bcfe6a6b739a97899d4ba539eba219c8e5cceb480e527c0044d105881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2332769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8988e16620a64647238fbf29b7d0992df6fefa10e26d037ae918c2145ea8c2e1`

```dockerfile
```

-	Layers:
	-	`sha256:3a5cc379c09b8a7bb2adc2fd8723a9c3ddc1b9a9e90586e5854c49e1d05d207e`  
		Last Modified: Fri, 14 Nov 2025 01:35:18 GMT  
		Size: 2.3 MB (2313735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7baf2f06185ee34f06ae943f175c5cda0d6bc32389b6564e42ae3016f84a614e`  
		Last Modified: Fri, 14 Nov 2025 01:35:19 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json
