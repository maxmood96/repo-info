## `clojure:latest`

```console
$ docker pull clojure@sha256:bef87f3096a96f40f0d451acccc0472bb8b74601947c1343bd26f27b454c0d79
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

### `clojure:latest` - linux; amd64

```console
$ docker pull clojure@sha256:6876a96b9caf1d91675d325203a1699cc0b3db4b6093408866fb361dface3d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239920253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b97731e7e34f1abf1782ed3a05f36ec6ebf2a47f20aa398e1cec39a8d95ef4c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:48:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:48:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:48:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:48:32 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 08 Dec 2025 23:48:32 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 08 Dec 2025 23:48:32 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:48:45 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 08 Dec 2025 23:48:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 08 Dec 2025 23:48:45 GMT
ENV LEIN_ROOT=1
# Mon, 08 Dec 2025 23:48:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 08 Dec 2025 23:48:46 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:48:46 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:48:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:48:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:48:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:48:58 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:48:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04996cb956706c0a8dbf84c71d0ea0bc432900866baa9adbfe85cc00b6246c8`  
		Last Modified: Tue, 09 Dec 2025 04:35:45 GMT  
		Size: 92.0 MB (92045295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc0cded79483636926ef293bbf504ef52183ed9d2915cf9f3b3ff9be510610c`  
		Last Modified: Mon, 08 Dec 2025 23:49:28 GMT  
		Size: 19.8 MB (19802894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc40f9620c777268e86025d3d3bfa7a4c8e1cb55caae5cf671f264b5f49d2366`  
		Last Modified: Mon, 08 Dec 2025 23:49:27 GMT  
		Size: 4.5 MB (4517724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0fbe3fe5fe16de7c42cdfb2ceab1e7fcb299fcfa54de8a7907bfe9c53a6a16`  
		Last Modified: Mon, 08 Dec 2025 23:49:36 GMT  
		Size: 75.1 MB (75072534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a2d38563af6b599050179539ec379c4642d90fd94a4e28fcaa93b8992bec33`  
		Last Modified: Mon, 08 Dec 2025 23:49:28 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395b743e0bf8ceadd6ce62bb68484df9ec172ead61416da0b151a8422f4740c8`  
		Last Modified: Mon, 08 Dec 2025 23:49:27 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:4e66518b89c1a9e8f915ea90f9e3eb99e7c33d3aac78eeb56e6ecaa17c8a5378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7444334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd7a6a787d111b0f229242c0168c87dfdda9a6de989ffcf266a5cca259d34560`

```dockerfile
```

-	Layers:
	-	`sha256:61ab9202e9f1733ca5ea9e32dee18be832e589f6f0001270e00654a80f987645`  
		Last Modified: Tue, 09 Dec 2025 04:34:36 GMT  
		Size: 7.4 MB (7418725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca4d688d33391d37494bd1487a400da3cd755ea695c61404d1085b425e05d36a`  
		Last Modified: Tue, 09 Dec 2025 04:34:37 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:81ec40ded8abd9fa49c3745608cd173baf524622399cdfde25c0489bef9f9d75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.7 MB (238687755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b71bb633f25ddc30668bc874d46ee971effc64dc233cc008858d19dc3ca59bc5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:57:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:57:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:57:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:57:26 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 08 Dec 2025 23:57:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 08 Dec 2025 23:57:26 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:57:40 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 08 Dec 2025 23:57:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 08 Dec 2025 23:57:40 GMT
ENV LEIN_ROOT=1
# Mon, 08 Dec 2025 23:57:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 08 Dec 2025 23:57:42 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:57:42 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:57:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:57:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:57:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:57:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:57:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe28eb5139a077860f00475eb04bdc47e546c09148afbd1d3fecbe9ee4c203d`  
		Last Modified: Mon, 08 Dec 2025 23:58:37 GMT  
		Size: 91.1 MB (91052515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4aba18e68f968705cee94c08af8f2774245b1a2a37f23c3328df37681b8dfe9`  
		Last Modified: Mon, 08 Dec 2025 23:58:27 GMT  
		Size: 19.6 MB (19632137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ac78feff5f6366c42f6e8ebc2173df0341f9cd1a9625e112da1393e22c264d`  
		Last Modified: Mon, 08 Dec 2025 23:58:26 GMT  
		Size: 4.5 MB (4517752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25c57d57bafdfb1080b23591c51f34375729b377a3cfbb20c95de7336fdee4f`  
		Last Modified: Tue, 09 Dec 2025 05:08:38 GMT  
		Size: 75.1 MB (75125206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d7a7c40608eef3c983f5e51176bd9456fbfa8c21c83826e4b9f040dda7a103`  
		Last Modified: Mon, 08 Dec 2025 23:58:25 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5176fe50892e89d679219cf3d9fcb85cf25cd7e0defef26ffc4fcfad78500d8`  
		Last Modified: Mon, 08 Dec 2025 23:58:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:7454e830d54b848c7ed017b4104558708a954f1271e7a56e4e76e2ec87f67368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7450194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d7d3cb5609af6cd959c62be4d32f1341b280e4fc282d3d4ee22162e8a688b5`

```dockerfile
```

-	Layers:
	-	`sha256:83c1a53b641cd038d2f22a10b6bd406705eb7a69db791ce39390e131c7f01219`  
		Last Modified: Tue, 09 Dec 2025 04:34:44 GMT  
		Size: 7.4 MB (7424461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d67b5658258c523dc71968d3097a6f1bbdefde56d2adc0cbb5cfa21edfcdaaa9`  
		Last Modified: Tue, 09 Dec 2025 04:34:45 GMT  
		Size: 25.7 KB (25733 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; ppc64le

```console
$ docker pull clojure@sha256:18a8c08dc8cb1464707dc3dab5f83e711cb2fdbc0a2823788825aa6dcb6402d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.2 MB (249153835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d078775b58d808464808550629b7f69ba082f7ccdcc5f8efd7b1d48d2d8a7413`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:34:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 22:34:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 22:34:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 22:34:22 GMT
ENV LEIN_VERSION=2.12.0
# Mon, 08 Dec 2025 22:34:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 08 Dec 2025 22:34:23 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 22:35:12 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 08 Dec 2025 22:35:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 08 Dec 2025 22:35:12 GMT
ENV LEIN_ROOT=1
# Mon, 08 Dec 2025 22:35:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 08 Dec 2025 22:35:17 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 22:35:17 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 22:35:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 22:35:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 22:35:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 22:35:55 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 22:35:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c088128ea77bb5c706bb00930020ea2fba147060275f49c5a7be6b54af5ca7c8`  
		Last Modified: Mon, 08 Dec 2025 22:17:06 GMT  
		Size: 52.3 MB (52326977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbeeb5c6058bd793bb98336cf15f96291626b642ff5b9461a0723bb0f77fc9eb`  
		Last Modified: Mon, 08 Dec 2025 22:36:56 GMT  
		Size: 91.6 MB (91610764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be781a3ac1a4f6d9f0a37c15905238450552f33e0d7f3672a1c47afd7ebeab6`  
		Last Modified: Mon, 08 Dec 2025 22:36:51 GMT  
		Size: 20.0 MB (20021660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c45adbbe470ce5178d26de2fd84d72b3eba3031e1fb5213e0d278e7d4c1dddd`  
		Last Modified: Mon, 08 Dec 2025 22:36:50 GMT  
		Size: 4.5 MB (4517760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f7b179b5797b3322e01f3664880695155005f7f0f866ed39967a3a706b9a1f`  
		Last Modified: Mon, 08 Dec 2025 22:36:58 GMT  
		Size: 80.7 MB (80675604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913cd3414bbec64961037fb03e95fa75fa4fda550d15f1551a8ad8c099b48e9c`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062e8abad5ff5925edcbdc79535b28a8cab5b52b99291bdfca44dc358163d5f8`  
		Last Modified: Mon, 08 Dec 2025 22:36:49 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:a8e456241f1adc1e4aa39b5c3dd3280f5abba05b08e5e0913d57320c15d0cc06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7450873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea7cb38db83f380cd0d19973a54fa8ce1cc80c872574d4c94acbe26249ddf043`

```dockerfile
```

-	Layers:
	-	`sha256:3bbe488328feaa901d081df926e44767d78036e51b9afd249c0b4d64209758f8`  
		Last Modified: Tue, 09 Dec 2025 01:34:46 GMT  
		Size: 7.4 MB (7425225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2c5e8df60398f8e938b76b5552f12560f60f9cd063c38211eee7f22b14e94b8`  
		Last Modified: Tue, 09 Dec 2025 01:34:47 GMT  
		Size: 25.6 KB (25648 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:latest` - linux; s390x

```console
$ docker pull clojure@sha256:65aa2f39960bd2114260a14d0a8639e1ea3edc028239a300d93a01865c814202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233550371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920e48fdacf17b2fbcb25468f0748ad53f8b40a480a54635f819648dcb40cd00`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 01:24:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 01:24:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 01:24:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:24:12 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 09 Dec 2025 01:24:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 09 Dec 2025 01:24:12 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 01:25:00 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 09 Dec 2025 01:25:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 09 Dec 2025 01:25:00 GMT
ENV LEIN_ROOT=1
# Tue, 09 Dec 2025 01:25:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 09 Dec 2025 01:25:03 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 01:25:03 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 01:25:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 01:25:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 01:25:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 01:25:18 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 01:25:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f1896ba83f603ad81e0d8cb48b496e763b4b781a68efe11f1b6de9da929514ea`  
		Last Modified: Mon, 08 Dec 2025 22:15:09 GMT  
		Size: 47.1 MB (47137665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6024d0cf3f3c2e42efef958fee18109019160ed5dc0afc14b97b74565341a9`  
		Last Modified: Tue, 09 Dec 2025 01:26:10 GMT  
		Size: 88.2 MB (88210741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cb6a978e4eb335173c5bf398c9021ede3e48c0f47432745ee80f1f35c3c606`  
		Last Modified: Tue, 09 Dec 2025 01:26:01 GMT  
		Size: 19.5 MB (19460754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59534ae50a9c9efe1e86ba8ed8735edf45ed1a1d59031cfde2f10ffef9869acb`  
		Last Modified: Tue, 09 Dec 2025 01:25:58 GMT  
		Size: 4.5 MB (4517724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487402319fc546b7b9caa984ee0c1d0ab2f7d08a047143769a5cdf3b3cc69d49`  
		Last Modified: Tue, 09 Dec 2025 01:26:05 GMT  
		Size: 74.2 MB (74222415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35fced32aeb667e82e775e5950334b04b9a5f7c2456fa84ad380bfa1fdd22793`  
		Last Modified: Tue, 09 Dec 2025 01:25:57 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e82b761ab97508570c57947ed91b030a646ee75a25084525975e38c17d553b2`  
		Last Modified: Tue, 09 Dec 2025 01:25:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:latest` - unknown; unknown

```console
$ docker pull clojure@sha256:0c330c7f0edf9d43fc0c2d2f4cfd4ddda343a992807345a0b4dc704a6469a228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7438201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27e542c6877a04da967a1218a9ce8af591e4d68ceb180604d541f3a237dff23`

```dockerfile
```

-	Layers:
	-	`sha256:cd02839b96a59ca10ffde7071bd436fb0204fe6499267ea5031428a5f9753d4a`  
		Last Modified: Tue, 09 Dec 2025 04:34:55 GMT  
		Size: 7.4 MB (7412592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bac50895d98d1753ba2728bb858b55c027114f35543bb510a8755525e5c52e24`  
		Last Modified: Tue, 09 Dec 2025 04:34:56 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.in-toto+json
