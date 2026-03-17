## `clojure:lein-2.12.0`

```console
$ docker pull clojure@sha256:ea203b3cf93e0b543257abd486b17989a69708f110d9a52a1ef726f6d76dd6b9
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

### `clojure:lein-2.12.0` - linux; amd64

```console
$ docker pull clojure@sha256:dda87f3735bd53d44ae751a3171e94c5c93800fec00b7ad47143d8d26b170df7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.1 MB (165065873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd75efd8a494b20a55e64720c2c838ad7decc08e3695f3ce5baf56d6a1106536`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 03:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:17:22 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 03:17:22 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 03:17:22 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:17:35 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 03:17:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 03:17:35 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 03:17:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 03:17:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:17:37 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:17:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9d2f29087bcd6d99efd909a99095549425cd63e27c71b3bf37f108c6b7c370f9`  
		Last Modified: Mon, 16 Mar 2026 21:52:42 GMT  
		Size: 48.5 MB (48488584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba37027903e3ce8e11c6641089105c56221793f9d9ce3463dacd48725772e20`  
		Last Modified: Tue, 17 Mar 2026 03:17:54 GMT  
		Size: 92.3 MB (92256289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3cf668906ad5fe23dcdbbe07f42440adccb57e74e46aad03d12521026f7acf1`  
		Last Modified: Tue, 17 Mar 2026 03:17:53 GMT  
		Size: 19.8 MB (19802820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb41b3781828e48d1662db1f1fa8742470a5000a03517547ac4188a0332dbe05`  
		Last Modified: Tue, 17 Mar 2026 03:17:52 GMT  
		Size: 4.5 MB (4517751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76718a17c7bee18be69a80eb43093ff2d9698d2a32fc64b0d55cfadeb088976`  
		Last Modified: Tue, 17 Mar 2026 03:17:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:4c65b695b4aa12600d6f2220a5c3f245f8339b56d293800c500197874d539da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4271286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc17e747c9b113d09567c47a3ab7dfa44a5d7ac461d2de0199ba9539687e35dc`

```dockerfile
```

-	Layers:
	-	`sha256:d271ba2946f07c1180727bc905c5205288b068cd47968058463bde6caac1e830`  
		Last Modified: Tue, 17 Mar 2026 03:17:52 GMT  
		Size: 4.3 MB (4251027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b25ff14abe54b680d903468d5a36850d619c648590f4f8adbe095def21a6164`  
		Last Modified: Tue, 17 Mar 2026 03:17:51 GMT  
		Size: 20.3 KB (20259 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1524c92f499ab605de414c38d16445f6a2c3624f45d31dd83032eaf44dcaa2db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.8 MB (163812255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78b09e0cb20c23f1f778699c203a00d8ff396eb5b8c863f35c4a851058fb794a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Tue, 17 Mar 2026 02:59:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:59:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:59:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:59:28 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 17 Mar 2026 02:59:28 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 17 Mar 2026 02:59:28 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:59:42 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 17 Mar 2026 02:59:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 17 Mar 2026 02:59:42 GMT
ENV LEIN_ROOT=1
# Tue, 17 Mar 2026 02:59:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 17 Mar 2026 03:05:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:05:12 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:05:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2ea98bb5eec9d02a0d7b59638c683db4e1e749f998a317bc731e9506f8480b12`  
		Last Modified: Mon, 16 Mar 2026 21:52:02 GMT  
		Size: 48.4 MB (48373032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cece5b6ef31d6e20939b80c25fefcac12a67ad13331af290ac6355366f11c6b7`  
		Last Modified: Tue, 17 Mar 2026 03:00:34 GMT  
		Size: 91.3 MB (91288265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b501d289d1d1d30a8e352b2ef0a484ed0beba9826e6435663b567bcea7e6a391`  
		Last Modified: Tue, 17 Mar 2026 03:00:32 GMT  
		Size: 19.6 MB (19632776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85fb3316e3cedc8023538b8853dfc5b8a260ccfd3189de1e6fcf70133d4d225c`  
		Last Modified: Tue, 17 Mar 2026 03:00:31 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634c4250f8a39987c4ee4386dd5e237ff1d3c09500e53564bddd3fb7f27b593b`  
		Last Modified: Tue, 17 Mar 2026 03:05:22 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:7cda77850b9f6d523463d8a46684be5c294fe3b02277232917d8cdebfe87a9a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4271163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94d1a75dbdb053530ccece9411cf75c3e7366741383318a5a83926fdd8445df5`

```dockerfile
```

-	Layers:
	-	`sha256:4c20d5728accf13914f5fb3290d3d3a6e827828484a82061c08853ef16ee6bee`  
		Last Modified: Tue, 17 Mar 2026 03:05:22 GMT  
		Size: 4.3 MB (4250711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa4dfe0fd5f21806ff5576ccea402bd136063685352eeb7d20f0aeb546ad6fdc`  
		Last Modified: Tue, 17 Mar 2026 03:05:22 GMT  
		Size: 20.5 KB (20452 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0` - linux; ppc64le

```console
$ docker pull clojure@sha256:c3cd0395383cf9609d391624fe0b5248669461ea33a9525e34f880869a5bd713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168511829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2817c5200b4c4e58bb86ef4ae1b57ac3126c05fcb0c1176fdefadb16195e9780`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Wed, 25 Feb 2026 01:40:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 01:40:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 01:40:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:40:44 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 25 Feb 2026 01:40:44 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 25 Feb 2026 01:40:44 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 01:41:24 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 25 Feb 2026 01:41:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 25 Feb 2026 01:41:24 GMT
ENV LEIN_ROOT=1
# Wed, 25 Feb 2026 01:41:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 25 Feb 2026 02:14:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 25 Feb 2026 02:14:13 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 25 Feb 2026 02:14:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bab868bc9e6457cefbe0a5145acf421b2bdda0c0ceaa18c23cdb26dd06a94f2`  
		Last Modified: Wed, 25 Feb 2026 01:43:08 GMT  
		Size: 91.6 MB (91633010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2c130e1abc8f2d79fcc9209acb23596aaa4495d6ccc0b5a262c9f6bc0330ab`  
		Last Modified: Wed, 25 Feb 2026 01:43:05 GMT  
		Size: 20.0 MB (20023809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc95acb35de425f9b852c4f09629a64667b1c0300f5fe50f2f1f9be19798d51`  
		Last Modified: Wed, 25 Feb 2026 01:43:04 GMT  
		Size: 4.5 MB (4517785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d104e41b0419e575120df8fdb0c09d667e240b91320c39e1fcaeb2bbc78f2dc9`  
		Last Modified: Wed, 25 Feb 2026 02:14:34 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:a277a684f63ee329d3d9e5e5f7ce8ff59aaf5706f4e3a93359349fa481009538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4256575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c53b5177ada2ff000bdd9e3fc600b92f3843a0165d87361ed867f8c738c3e552`

```dockerfile
```

-	Layers:
	-	`sha256:2dd31bbf2ff8f083a2e7a82f637fd3f8c26e23448cab26fa3852cde6479b8375`  
		Last Modified: Wed, 25 Feb 2026 02:14:34 GMT  
		Size: 4.2 MB (4236236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f65e284dafcccabcd3990a348e980f8e7cb59228e33bfb5c0c8b3383b02731e`  
		Last Modified: Wed, 25 Feb 2026 02:14:34 GMT  
		Size: 20.3 KB (20339 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.12.0` - linux; s390x

```console
$ docker pull clojure@sha256:c2f1b98c97c6996b4ce0e95d88d2cb4c074f36f0945b6c7943e213b03633758e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.4 MB (159363453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e8935f7458cc27bc59af405f76ffc099db752566615dec62b1d73e16b30bfde`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 23:22:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:22:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:22:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:22:55 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 23:22:55 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 23:22:55 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:23:28 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 23:23:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 23:23:28 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 23:23:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 23:23:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 23:23:33 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 23:23:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:00b1871f38dea81b1982e306480bd9f97cedf7b0cb3342e4bc84925e6082ade8`  
		Last Modified: Tue, 24 Feb 2026 18:41:26 GMT  
		Size: 47.1 MB (47148087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a2c7f155ba43475a58ce53d7548c5de702bcc0cc952b4fe414a2ed67d07e94`  
		Last Modified: Tue, 24 Feb 2026 23:24:09 GMT  
		Size: 88.2 MB (88233846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0accba8e8bb193d30badc398ede5cd3a52d379e0697e202d2a353ae242b9fc5`  
		Last Modified: Tue, 24 Feb 2026 23:24:10 GMT  
		Size: 19.5 MB (19463370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bfc72ce3173d03aaba2a8ff34788bc2a481eb2fc9fb81a6e8fbbc0ced65958`  
		Last Modified: Tue, 24 Feb 2026 23:24:10 GMT  
		Size: 4.5 MB (4517721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96ef88544195ce61329fbc1b7f5f4512519ff70e67c75ad3b671679bc3bc383`  
		Last Modified: Tue, 24 Feb 2026 23:24:09 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.12.0` - unknown; unknown

```console
$ docker pull clojure@sha256:dfee7ba01559eac1ec479380ddd3b6d13eb213e1adb34def4bac418512cfb3d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4247662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3aef64086b536c0bacc03056ded2cc59543df7fa5e894d92f591db2d59644f1`

```dockerfile
```

-	Layers:
	-	`sha256:c4bb2d92a1f74b357e0032c73271a4d69b6c40cc6da079937af07b6091cd314a`  
		Last Modified: Tue, 24 Feb 2026 23:24:10 GMT  
		Size: 4.2 MB (4227403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f31493ec117d4d59e1cb0a328d7df17e9ea69380a73d485e77dc76fb932266d`  
		Last Modified: Tue, 24 Feb 2026 23:24:09 GMT  
		Size: 20.3 KB (20259 bytes)  
		MIME: application/vnd.in-toto+json
