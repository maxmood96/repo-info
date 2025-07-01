## `clojure:temurin-11-lein-bullseye`

```console
$ docker pull clojure@sha256:dada6156d3d9ced48f7f919a15c6bc01ba360ca7217150f1566d3daf3495adf9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:5b2b01da17b4ea1d0553d59c900988ad41f7f7a99128c4f55d2664fc9d2872e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.7 MB (256698237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:455b243d7fc7a4cbf7aecadc82828c531c3fc545152c9e1fe4938bb633c54585`
-	Default Command: `["lein","repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
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
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800592c58c765a98f06ae554a42e6e0c31ebbdcfbb5500279d94df190db126fe`  
		Last Modified: Tue, 01 Jul 2025 02:38:17 GMT  
		Size: 145.6 MB (145635638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a823377e0fcbe54aa80573621c1e1b783915ab730c59e21c6cb377285be88165`  
		Last Modified: Tue, 01 Jul 2025 02:39:04 GMT  
		Size: 52.8 MB (52793554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa65291f8a8ee6d6030a55112c887f0402c69a9ad8769ab19ecedcdda7f55f7b`  
		Last Modified: Tue, 01 Jul 2025 02:38:47 GMT  
		Size: 4.5 MB (4514191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1883f47b90485ea51bb4186c4fbb78d79d47d1c7d48b907abeb89628066271b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6820134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30388cd04dc5982bf7d709f89b0f49530bac9b33f2a5a5ba98804fd0cfcb0282`

```dockerfile
```

-	Layers:
	-	`sha256:09683ac4af52589da289683d47260282841ab5582f78c8bffa9f4b6eb920c091`  
		Last Modified: Tue, 01 Jul 2025 06:35:46 GMT  
		Size: 6.8 MB (6803701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da3ca7e0f5bd6d9e34769559dfb019d98bc05b3969d56c4021be82bebf4ac88`  
		Last Modified: Tue, 01 Jul 2025 06:35:47 GMT  
		Size: 16.4 KB (16433 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:67d699c4cbd0ff3942e23274761add46a8be22858f177a529656e3e7686e9c2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.0 MB (252020335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c2e4dd2ba07ecf4ee7a3351ede809a593a15a5b02071078dc3e7569830902b5`
-	Default Command: `["lein","repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
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
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:df45b4853b6fce6b81d1ac6218d861c6d7c8c14da4be409d42ee4bfdf0737e71`  
		Last Modified: Tue, 01 Jul 2025 01:15:18 GMT  
		Size: 52.3 MB (52252254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b068decccd3f64ab597744c3957bac88f2e12d807a02f894920187eca517cc`  
		Last Modified: Tue, 01 Jul 2025 12:07:11 GMT  
		Size: 142.4 MB (142420643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa3aa2a0dded13093b889e30f4a05aef55f736c54033e107cd2e77beb0b3e04`  
		Last Modified: Tue, 01 Jul 2025 12:07:08 GMT  
		Size: 52.8 MB (52833195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e370f0ed219ebdbd6485cfdd1daae4f0e40d2b584d3a7e42d6d7db3cbac86f`  
		Last Modified: Tue, 01 Jul 2025 12:07:32 GMT  
		Size: 4.5 MB (4514211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:81de70dc6414ab1e2797459db463d7ec9e2ef34e6c609502e46ea652404dd967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6825903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b73c3fafe0f5323f518661c13d4920179ad042da646f4916ea483df062a3c979`

```dockerfile
```

-	Layers:
	-	`sha256:1db1eb270fd52556c05e5acb9894344cdb45da474833122c0bafb5de8e247df2`  
		Last Modified: Tue, 01 Jul 2025 15:35:29 GMT  
		Size: 6.8 MB (6809350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3232c9905711c61a84afc79b9df0707d0f58ee056549143b213cb6c30ec70aa`  
		Last Modified: Tue, 01 Jul 2025 15:35:30 GMT  
		Size: 16.6 KB (16553 bytes)  
		MIME: application/vnd.in-toto+json
