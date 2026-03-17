## `clojure:temurin-21-lein-bookworm`

```console
$ docker pull clojure@sha256:d1d99823eaee948e4a701a7f8943701f3f4348178896189058b1b4b24b813727
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

### `clojure:temurin-21-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:978c911a01f815fa61fda0bf03853475c8bac029a2c03e105787f4014d888ec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230666613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577e0e61a8990363234b761c7c4c58ab2846dcd7d45a8d876dd36484b04b106b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:58:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:58:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:58:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:58:57 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 02:58:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 02:58:57 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:59:10 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 02:59:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 02:59:10 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 02:59:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 02:59:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 02:59:12 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 02:59:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930bc417d09576f8fe90d17d3184225b0988d0fd97d77fe8d4a89039591e4ef0`  
		Last Modified: Tue, 17 Mar 2026 02:59:32 GMT  
		Size: 157.9 MB (157857094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5cb81c6d68e825398e5a40cf5ac3b351e3bbce99483e0e985ef5c731f5bff2c`  
		Last Modified: Tue, 17 Mar 2026 02:59:29 GMT  
		Size: 19.8 MB (19802770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7a93a89efa1f071e10fb87f8f4b467c72580df3ba659a337a76d41e4f78c0d`  
		Last Modified: Tue, 17 Mar 2026 02:59:28 GMT  
		Size: 4.5 MB (4517738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d67d0ffb6b386dba0d6066be1c4418669280b1fd6d04420d1093c36a7c13a36`  
		Last Modified: Tue, 17 Mar 2026 02:59:28 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:166a215c999595ee416c4ccd2537d816402005c4c4f68d6d49c6501e65c77181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4303251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:541a030944c8959311968bedc21befe7d36fd8d2aae31663c1dabb23537d42de`

```dockerfile
```

-	Layers:
	-	`sha256:5725fc82ad8b2fb978c24b83117f896cb89b5ae8b5cbe69404ef68648d0444ee`  
		Last Modified: Tue, 17 Mar 2026 02:59:28 GMT  
		Size: 4.3 MB (4284233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91419f9ccf832b630946b8488c03cb24eb2bfbb431679dbc7e9d351f30a0658e`  
		Last Modified: Tue, 17 Mar 2026 02:59:28 GMT  
		Size: 19.0 KB (19018 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:63153b3e84bc588df70dc7b02a87484b73095a9e649c38b1a977b4afd71de1c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228657110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b09aafb3b5fc9eb1e3fb5604d26966d1b9cb524b84c2c434fd5fe7c1c22cb264`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 03:03:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:03:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:03:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:03:45 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 03:03:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 03:03:45 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:04:00 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 03:04:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 03:04:00 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 03:04:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 03:04:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:04:02 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:04:02 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82faeaf178d6892a9733fed8753cf36fdb693e9b1c18cd729d56fb092ecc6f8a`  
		Last Modified: Tue, 17 Mar 2026 03:04:26 GMT  
		Size: 156.1 MB (156133067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10618d908006e446b646f467a009b1fbb4122d5dc93e51e820521c2b439a98e9`  
		Last Modified: Tue, 17 Mar 2026 03:04:24 GMT  
		Size: 19.6 MB (19632833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fed25a44e85539c226c19b1362c3584a44203c55404aa0e3e49672d3d4fafe`  
		Last Modified: Tue, 17 Mar 2026 03:04:23 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d412391dda2782e063498737a627815f249bd184614183f971c0c9f54dd110`  
		Last Modified: Tue, 17 Mar 2026 03:04:23 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8e09dd8f65f1b1a92978107a6dcbed1e9ce1aa01f63cca0ea45901e0962ca344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4303035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a18a469e655a88eabc6e74d47eb6f77f31a54c760ca92dcbbe5a93d60e78d1a`

```dockerfile
```

-	Layers:
	-	`sha256:8ced9821c1a2edffedb1e3204d9cf86223c4fb8f1c817ae669b184cd431133a9`  
		Last Modified: Tue, 17 Mar 2026 03:04:23 GMT  
		Size: 4.3 MB (4283872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b11c44fcefcbc27d2946a24ec45524998e5f239314d1fa6d4cfad1ce598a4bd8`  
		Last Modified: Tue, 17 Mar 2026 03:04:22 GMT  
		Size: 19.2 KB (19163 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:d69a5933846f14a7776c62922f4a2f102868098c86f7362de2bf188654c82ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234856274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe469ed31c4570d6c6cc8760ac75452e2041e4e07015d9fc4163b3a561789ab`
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
# Tue, 17 Mar 2026 18:35:16 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 18:35:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 18:35:16 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 18:35:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 18:35:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 18:35:20 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 18:35:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c072e92b832614e86d956c6381c6b7617944feae3193ea5691e9506870844136`  
		Last Modified: Mon, 16 Mar 2026 21:51:19 GMT  
		Size: 52.3 MB (52336698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fbb79ec0e62d97d7f7a307c9ff90dd94c14b4ef06ecb05232fe909cb1db302`  
		Last Modified: Tue, 17 Mar 2026 18:36:06 GMT  
		Size: 158.0 MB (157977514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e74b6573a5fd70ca59ee12f326cd27650b62399b2f6f59cd76c40244091de4`  
		Last Modified: Tue, 17 Mar 2026 18:36:01 GMT  
		Size: 20.0 MB (20023869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0083f66e764952f0ab3a5d58c6b6f61041dcb41eb92ed2b40621bb43f55480`  
		Last Modified: Tue, 17 Mar 2026 18:36:01 GMT  
		Size: 4.5 MB (4517764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eafa5721227ea8c5d0edc8d59e3da6a2ecbbe327662779c4e2e7f5f232eaf7e`  
		Last Modified: Tue, 17 Mar 2026 18:36:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2616f2254ca7e6407af6015dba0e19b092dc6640fc3f1a88ff995931769dc54d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4305178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf639a7730bbb982970c15a9b82c8eb29b6b1d4b45af791ed14daa22894b3846`

```dockerfile
```

-	Layers:
	-	`sha256:4c13cd731c90307f92c226cb288c7bd067d46f7f7dc54c4f1641aa8f35667192`  
		Last Modified: Tue, 17 Mar 2026 18:36:01 GMT  
		Size: 4.3 MB (4286106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93fbc5b6441c9a0034a339179cffb1f8bc99fd84aff277833398827c48eae6a5`  
		Last Modified: Tue, 17 Mar 2026 18:36:00 GMT  
		Size: 19.1 KB (19072 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:a7f672008930310875eb9178494f57e5f17ee7a72ef34fc9189a379c9bae91a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 MB (218234561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:886b8605b0ea849792c538f0f15d77e6ea9f804a7b443b90ad0bb1641e5e8852`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 11:38:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:38:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:38:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:38:46 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 11:38:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 11:38:46 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 11:39:08 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 11:39:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 11:39:08 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 11:39:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 11:39:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 11:39:12 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 11:39:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7dbc3949555449666cc7651209b926019d3fc7f1511f7ebcd8979762b12d59c1`  
		Last Modified: Mon, 16 Mar 2026 21:51:27 GMT  
		Size: 47.1 MB (47147919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a07871cae43295b592ace8562a64ff035a9e265aa9079f2c6446e201ec2e62`  
		Last Modified: Tue, 17 Mar 2026 11:39:47 GMT  
		Size: 147.1 MB (147105213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a5ed8c1314996df6f3756641b4c79c114e84ae02b39861ed772c3e8a261ac9`  
		Last Modified: Tue, 17 Mar 2026 11:39:45 GMT  
		Size: 19.5 MB (19463254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ea7b0171004e3eff00d492b652390e3653be73c23983ad023eeb34d0128726`  
		Last Modified: Tue, 17 Mar 2026 11:39:44 GMT  
		Size: 4.5 MB (4517747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c5451ae6c3aa0a599308d6ae3b35ae55992d559ed1186391228b39e79f7ce0`  
		Last Modified: Tue, 17 Mar 2026 11:39:44 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:69052e7d701182d8b7c2f370ecb53409f44647ba9c80914c4c1a13493adbc450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4295065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ade527c8a934b3310b2ab02aa7c48019c6a9950a8c32b596e41adda75641fd`

```dockerfile
```

-	Layers:
	-	`sha256:bec9b74142c7d8b7344e75f283db7d03aee7c568ecda62352881c8f977677fb3`  
		Last Modified: Tue, 17 Mar 2026 11:39:44 GMT  
		Size: 4.3 MB (4276047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bbe5adc642c8d2191b5100fba016ec6df1855d494bf654267a3906981d95d69`  
		Last Modified: Tue, 17 Mar 2026 11:39:44 GMT  
		Size: 19.0 KB (19018 bytes)  
		MIME: application/vnd.in-toto+json
