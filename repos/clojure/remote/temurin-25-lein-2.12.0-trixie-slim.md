## `clojure:temurin-25-lein-2.12.0-trixie-slim`

```console
$ docker pull clojure@sha256:853def1682f0198f120facf5639b2729cc7d0beb569613cd48f81ecf34653274
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

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:624fc05224d3edb24309ba88032d39887121d404f6d55eeaff8c2d92bf63af35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142788974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e4076635fb0cb931d908087031de873bb58c6ae69da1c6deaa809302f1bdfe`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 18:45:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:45:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:45:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:45:49 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:45:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:45:49 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:46:04 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 18:46:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:46:04 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:46:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:46:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:46:06 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:46:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d50de83c740d1e27c26dbb901dd8cd6bf563e2575c7323a228dd0c2986b7317`  
		Last Modified: Sat, 08 Nov 2025 18:46:43 GMT  
		Size: 92.0 MB (92045302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4263add4986a935527e33c5010f2f18213d8bfe09f083bc387b3589d160cff78`  
		Last Modified: Sat, 08 Nov 2025 18:46:36 GMT  
		Size: 16.4 MB (16447411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a64206bb4495e54919deeeea8230def838a956630d67387f14680349e993a7`  
		Last Modified: Sat, 08 Nov 2025 18:46:35 GMT  
		Size: 4.5 MB (4517728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82c2396d59a2727c5c870b6045f64e5a268260edf478034a5312e183ffa6e19`  
		Last Modified: Sat, 08 Nov 2025 18:46:34 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:169f614dab93427096ecaac4c19cdec338695d491428aa575b6e2d2cdd0ad152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76974a49d9449a791cd00c90baefcc40c6e865be63d5f84119386cef26bbb6ba`

```dockerfile
```

-	Layers:
	-	`sha256:ceeb5716f784c1afbe6d427148cbb3e57668a20055c6d41c9ee29661197aa817`  
		Last Modified: Sat, 08 Nov 2025 22:35:45 GMT  
		Size: 2.3 MB (2314760 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f58806acd3aa03a7ebe252fdd57fe115e5934e753a3d33493b61807c13506f0`  
		Last Modified: Sat, 08 Nov 2025 22:35:46 GMT  
		Size: 19.0 KB (19034 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c391b8068c99bb376fd794dec273ce6f36891f19ca39d99e4555c0bad2ac564b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142126557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:518351483a5fc103d0866545881e32e61754e32e0ae34243e62a545d3280e309`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 18:45:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:45:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:45:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:45:32 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 18:45:32 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 18:45:32 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:45:48 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 18:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 18:45:48 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 18:45:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 18:45:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:45:50 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:45:50 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bef0405a6a1cfb7b6b6ac1854e980b56719699466d6b1f891183419d5723275`  
		Last Modified: Sat, 08 Nov 2025 19:41:49 GMT  
		Size: 91.1 MB (91052529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca1493b0ea5b1ec53accf7b7cf1d54d6c66d24d67c4c19ffda930e660ed2ca4`  
		Last Modified: Sat, 08 Nov 2025 19:41:35 GMT  
		Size: 16.4 MB (16413538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986afc75c6812b09987e94d35feff2e290bc17fbdd8c55aa7e39b912fb496e83`  
		Last Modified: Sat, 08 Nov 2025 19:41:36 GMT  
		Size: 4.5 MB (4517762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1c5704d98c118b92f900404714f05bdce588ee1ad2342b0f0234e271c4b525`  
		Last Modified: Sat, 08 Nov 2025 19:41:33 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fa2a65c48052a1c61623ebd8dc6b064a75343cd82604fabb46830692a410109d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d731a3133f81a788e2b1faf5d91b63819e246a175052e5246346c449785e318`

```dockerfile
```

-	Layers:
	-	`sha256:eb2d0f302dd804f0b37a4c394c05d595e063425e8b112d154b5efe3c9f5994ca`  
		Last Modified: Sat, 08 Nov 2025 22:35:50 GMT  
		Size: 2.3 MB (2314399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f493250f2c11238c857b1bd76f74f5fc46ae0d4250786daa232d2dc5b8b61ff7`  
		Last Modified: Sat, 08 Nov 2025 22:35:50 GMT  
		Size: 19.2 KB (19179 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; ppc64le

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

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

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

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:31724ebf73b919089f33c3947a4cf618cbd438fa7e3af4ebb1b4c51835cdc8ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139944433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16ea719d7657698904f8ea69ed0b6fe5ae650789fa6455e714c985827935a5bb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Fri, 07 Nov 2025 07:06:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 07 Nov 2025 07:06:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 07 Nov 2025 07:06:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Nov 2025 07:06:38 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 07 Nov 2025 07:06:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 07 Nov 2025 07:06:38 GMT
WORKDIR /tmp
# Fri, 07 Nov 2025 07:08:06 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 07 Nov 2025 07:08:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 07 Nov 2025 07:08:06 GMT
ENV LEIN_ROOT=1
# Fri, 07 Nov 2025 07:08:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 07 Nov 2025 07:08:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 07 Nov 2025 07:08:22 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 07 Nov 2025 07:08:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b43db7c4a1d787e387c72aaa92b0496c45b522bc0b3dbb0a44428976e33faeb`  
		Last Modified: Fri, 07 Nov 2025 07:11:59 GMT  
		Size: 90.8 MB (90752402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14187d8628f0ad96596d2239925b433b93044634f5009aad0ea06a64db1b2a99`  
		Last Modified: Fri, 07 Nov 2025 07:11:54 GMT  
		Size: 16.4 MB (16398033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8612a82a4b887c0f2a9d9c577bdc772b63b001640db3b4d1d318810c6fdccee3`  
		Last Modified: Fri, 07 Nov 2025 07:11:52 GMT  
		Size: 4.5 MB (4517782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7c63c6f8041e9c1d65727bf6e297e98d0352f5f2a5b33b0ac99fd1c995b5a4`  
		Last Modified: Fri, 07 Nov 2025 07:11:51 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:62d189664a7d34927426a185e1c743709a43e4f7a768d92ba670a77c765b3728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2325893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e3e5e7b3e97421e538c16ddd23f5107751d543be977936cda4811e63a14075`

```dockerfile
```

-	Layers:
	-	`sha256:14b2922274be43ddb24aaf598a926666bacdbe70df191217a81f92e1889afe51`  
		Last Modified: Fri, 07 Nov 2025 10:34:39 GMT  
		Size: 2.3 MB (2306803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d62e74b3f203895c8c0f3772199f931ce66b8db8a44dc39cb8d73c7628f0abe`  
		Last Modified: Fri, 07 Nov 2025 10:34:40 GMT  
		Size: 19.1 KB (19090 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:30cca3da11f3899fb76212302f305d995c7a8380bff9c3819405b4dbed6b1089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139049998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c648e1b304456f8a63789b0d0e57abca734d4f1dd482aab764ea69c114844665`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 20:40:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 20:40:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 20:40:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 20:40:12 GMT
ENV LEIN_VERSION=2.12.0
# Sat, 08 Nov 2025 20:40:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 08 Nov 2025 20:40:12 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 20:40:43 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 08 Nov 2025 20:40:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 08 Nov 2025 20:40:43 GMT
ENV LEIN_ROOT=1
# Sat, 08 Nov 2025 20:40:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 08 Nov 2025 20:40:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 20:40:46 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 20:40:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0875292777271dfec52272a481583511bcd8559433138dbc7ada6556390ae03`  
		Last Modified: Sat, 08 Nov 2025 20:41:27 GMT  
		Size: 88.2 MB (88210682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84dbb99e7a4fc302d15a9074313090bf045bd5f9c4c2db6e02ebaa5919b7b156`  
		Last Modified: Sat, 08 Nov 2025 20:41:20 GMT  
		Size: 16.5 MB (16483728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fba70369a8cc4858f69f28247436cb8e850c8a8520097986ab9d78daecddf5`  
		Last Modified: Sat, 08 Nov 2025 20:41:19 GMT  
		Size: 4.5 MB (4517765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00d282daa3703541c35d46760c768a75895c8e59f8a0a24ad4d3dbdee550f78`  
		Last Modified: Sat, 08 Nov 2025 20:41:18 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-2.12.0-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:93ae5885418d49906273511692a327d54882547679f5973a525876b438df9880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2332768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:459b0f3f9ef40ae8bfe14e44cc38193b8bf8986d921bec58c0c4ec4019eda389`

```dockerfile
```

-	Layers:
	-	`sha256:e8dafeb160d2f5371cc869d40279cd4a864d679dba1ece3ad02fb0112057b021`  
		Last Modified: Sat, 08 Nov 2025 22:36:01 GMT  
		Size: 2.3 MB (2313735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e68e5718c6df0febdeafe145d7e78482f5440caa8b9693156151bccce3f6c260`  
		Last Modified: Sat, 08 Nov 2025 22:36:01 GMT  
		Size: 19.0 KB (19033 bytes)  
		MIME: application/vnd.in-toto+json
