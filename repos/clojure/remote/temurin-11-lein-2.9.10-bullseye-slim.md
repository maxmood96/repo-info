## `clojure:temurin-11-lein-2.9.10-bullseye-slim`

```console
$ docker pull clojure@sha256:4a1cbf854f3a2776f7f88844e2d6a1cad027628930442306b8d9956ea1baf1de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-lein-2.9.10-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:506d06aa412698a7d97d04993572aa6892427c6ec894f9007555dc8ee01496b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246925173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc6d6d27dc58e9d8392e59b6278d51090a5f663c8971947baa6183f00dc6f8d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 03:51:16 GMT
COPY dir:e3c63d67b32fccda756dd62000a0cf47da966d18fe6f1f25cd1f37b60881f0ec in /opt/java/openjdk 
# Thu, 06 Oct 2022 03:51:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 03:53:22 GMT
ENV LEIN_VERSION=2.9.10
# Thu, 06 Oct 2022 03:53:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 06 Oct 2022 03:53:22 GMT
WORKDIR /tmp
# Thu, 06 Oct 2022 03:53:38 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "dbb84d13d6df5b85bbf7f89a39daeed103133c24a4686d037fe6bd65e38e7f32 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 06 Oct 2022 03:53:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 06 Oct 2022 03:53:38 GMT
ENV LEIN_ROOT=1
# Thu, 06 Oct 2022 03:53:41 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 06 Oct 2022 03:53:41 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411b6cb0e944ff13c8e89f4a886c731ea8293c8f3dbc5d78ed1df2e6fbef5b9`  
		Last Modified: Thu, 06 Oct 2022 04:08:54 GMT  
		Size: 198.1 MB (198124981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddfcae34d2ca26f40f806b9d03102d770b9283c3d50b59fa35d9007e00fc3c2a`  
		Last Modified: Thu, 06 Oct 2022 04:09:49 GMT  
		Size: 13.0 MB (12981425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad274822cee716c7a929edced0745417b0db5d2ca110716e9327acd8999a20d8`  
		Last Modified: Thu, 06 Oct 2022 04:09:49 GMT  
		Size: 4.4 MB (4398665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-lein-2.9.10-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3fb2d7d095dbaaf2884b271832861ac590ef2e6ec39165f218e8d6bd73a46170
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.1 MB (242093719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d930897d2e54d66b0e8b33cd8818f3efdd0dae6c6c09c0ebb562addd853548`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 02:32:30 GMT
COPY dir:0dc06d70d42a32ae203bdf41d3806f1204b90ca101c4efe4662ba862f2c76b8a in /opt/java/openjdk 
# Thu, 06 Oct 2022 02:32:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 02:35:04 GMT
ENV LEIN_VERSION=2.9.10
# Thu, 06 Oct 2022 02:35:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 06 Oct 2022 02:35:06 GMT
WORKDIR /tmp
# Thu, 06 Oct 2022 02:35:21 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "dbb84d13d6df5b85bbf7f89a39daeed103133c24a4686d037fe6bd65e38e7f32 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 06 Oct 2022 02:35:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 06 Oct 2022 02:35:23 GMT
ENV LEIN_ROOT=1
# Thu, 06 Oct 2022 02:35:27 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 06 Oct 2022 02:35:27 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bfdcb0b9c92e9c3da0e6ca913cb8d3cf77c13d55a20c234730a5896afdec4a`  
		Last Modified: Thu, 06 Oct 2022 02:57:34 GMT  
		Size: 194.9 MB (194866592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ae5658a90a9e283041a0d5ce0b636b8b0e1f0b3ce901c2fb1d188b47c5f9f4`  
		Last Modified: Thu, 06 Oct 2022 02:58:38 GMT  
		Size: 12.8 MB (12764171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72b9afb7f59bf52f3aa5d489ed9fd06822593836ab07617861c42572489bf29`  
		Last Modified: Thu, 06 Oct 2022 02:58:37 GMT  
		Size: 4.4 MB (4398561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
