## `clojure:temurin-17-lein-bookworm`

```console
$ docker pull clojure@sha256:15c376305e1c2b12b1fa545d41606df20dacd0431d641db8335a671f357f7327
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

### `clojure:temurin-17-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:c14a7de58e16f939e6737c981eec894cc59ba9ea9568fe2455fb68ce3d00c373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.4 MB (218438519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:449fb0c3137dffa7e232b060c781ab9d4da9b32d964d6afaa4718463293bbeb4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:54:33 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 19:54:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 19:54:33 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:54:47 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 19:54:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 19:54:47 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 19:54:48 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 19:54:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:54:48 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:54:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf019ab083a93c81d17fb275de29154bb84b102c0192a5634762d4410b03c160`  
		Last Modified: Tue, 24 Feb 2026 19:55:07 GMT  
		Size: 145.6 MB (145628702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9231061b4914f436953a0d800517b72af725620e5c1c11c8e2c5687009940ab6`  
		Last Modified: Tue, 24 Feb 2026 19:55:04 GMT  
		Size: 19.8 MB (19802902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7c0e9f5069335d75d121161cd8ced1c6d62aac9f115a4453d08a237bd7fd65`  
		Last Modified: Tue, 24 Feb 2026 19:55:03 GMT  
		Size: 4.5 MB (4517709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be66d75fc02bf76ed4d73e2c384f226bc7997c19f4710f11ba0c7ba65326ae4`  
		Last Modified: Tue, 24 Feb 2026 19:55:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:465a2e1958c380117ea993e81fd5a56de5229d5164698fbefbb2350eef84afd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4300099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ba00d10447164572965d940fe355682565682c8072a8d0ea0d90c2373f7606e`

```dockerfile
```

-	Layers:
	-	`sha256:98b25f9d450947b42c97ed232777de96f2e067bbacab2471ffe1d2d90938e8e9`  
		Last Modified: Tue, 24 Feb 2026 19:55:03 GMT  
		Size: 4.3 MB (4281731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c141caa2cb12f43e39b1c8c95b2db2cfd205a74b7ddb6da94103f119bd0d3113`  
		Last Modified: Tue, 24 Feb 2026 19:55:03 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:86c9e85758d532f607509adcaa4795b78fd3504f81efa4f43f9b1224fbfec2fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.0 MB (216960352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c400e2239850bb7e5cf275ed17b16131a23d3e6dba6f4ee7cde65b2f53d8b460`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:05:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:05:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:05:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:05:05 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 20:05:05 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 20:05:05 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:05:19 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 20:05:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 20:05:19 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 20:05:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 20:05:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:05:20 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:05:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916efda5ec544349a54235d2b3e19c970b64655fd3df3e3dfecb21b4f3f942eb`  
		Last Modified: Tue, 24 Feb 2026 20:05:38 GMT  
		Size: 144.4 MB (144436198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5427f2e0386a504533be1e52d6754b0ca0bc031a6cbdef8b7d9ed4dab03039b3`  
		Last Modified: Tue, 24 Feb 2026 20:05:39 GMT  
		Size: 19.6 MB (19632810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:712c906eee5001c6b81d458e8d09c17f5a2675a0c4b45757f472304cda51cbd1`  
		Last Modified: Tue, 24 Feb 2026 20:05:38 GMT  
		Size: 4.5 MB (4517707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450accd6e3990b4a78049d92bcd8e44803d8e111494a42063ec55037d1853378`  
		Last Modified: Tue, 24 Feb 2026 20:05:38 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:1972f3065820578a19a55846fe8ac620e7fe11cc8274b924b1ee6905f14401b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4299835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cec14aff0af47aa444830ceea86ad1b9b63f8da795b2941a3376745647983ef`

```dockerfile
```

-	Layers:
	-	`sha256:23307a512a5b941040a689fd1cbb5c32bfcedaeb99a281bbdd200e392d3cf33f`  
		Last Modified: Tue, 24 Feb 2026 20:05:38 GMT  
		Size: 4.3 MB (4281346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2252e3119c8365cb6979107aaba04263ae62ea72cecccee2e3d40b9875bd222`  
		Last Modified: Tue, 24 Feb 2026 20:05:38 GMT  
		Size: 18.5 KB (18489 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:522baa99f88048881283eb90951b7ac64d1a970ee44bf4c8a61c57e6445945af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.3 MB (222317145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca74e474335d4ef0255902f0d447210a430e90651e9fe667ef80249fb056b2b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Wed, 25 Feb 2026 01:57:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 01:57:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 01:57:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:57:27 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 25 Feb 2026 01:57:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 25 Feb 2026 01:57:28 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 01:58:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 25 Feb 2026 01:58:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 25 Feb 2026 01:58:18 GMT
ENV LEIN_ROOT=1
# Wed, 25 Feb 2026 01:58:22 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 25 Feb 2026 01:58:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 25 Feb 2026 01:58:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 25 Feb 2026 01:58:22 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad0aa6d34d02956b4dd5d0e851f2871b9952fe294ac6bf261a9b69647625519`  
		Last Modified: Wed, 25 Feb 2026 01:59:14 GMT  
		Size: 145.4 MB (145438176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46af81c3eb83d358fef489c5b59a6c19bf49f7e6242bc55856fc7bd48348a3db`  
		Last Modified: Wed, 25 Feb 2026 01:59:10 GMT  
		Size: 20.0 MB (20023990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d48ddf49cd0d11d0cc9547755d7e31baf71117ef801a778065caa7cee9521a`  
		Last Modified: Wed, 25 Feb 2026 01:59:10 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b28fc0b6be0da5f4757301c997206113c3f54a5162ae3b203aca9f6b97715f1`  
		Last Modified: Wed, 25 Feb 2026 01:59:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d5907147608a87439714781bd0604ca321a84e512406b4bd8ab27f23a7c269e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4302004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2be64313ff5bd3717afbb39c08be595b00944d058428d28c2f612b502c9709b`

```dockerfile
```

-	Layers:
	-	`sha256:510431b51a0a03678320dad707105daa2aaa6b6367d3074d1b5ffca9ab592188`  
		Last Modified: Wed, 25 Feb 2026 01:59:10 GMT  
		Size: 4.3 MB (4283592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23f15a15ea525d09efae48ee51c6bc300c10b9e5fdf85ef334631787179c13d4`  
		Last Modified: Wed, 25 Feb 2026 01:59:10 GMT  
		Size: 18.4 KB (18412 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:1768196fc54fcd3a657989cced7b8b156e9057f2661d7c97dcb3c957d7776c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.8 MB (206756631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08499e2f264da4fb1ec78277286e1d598f1e849dede650efbfc67b8dbf6cc240`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 23:15:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 23:15:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 23:15:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 23:15:03 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 23:15:03 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 23:15:05 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 23:16:03 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 23:16:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 23:16:03 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 23:16:06 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 23:16:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 23:16:06 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 23:16:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:00b1871f38dea81b1982e306480bd9f97cedf7b0cb3342e4bc84925e6082ade8`  
		Last Modified: Tue, 24 Feb 2026 18:41:26 GMT  
		Size: 47.1 MB (47148087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd3be966c5469156f43eb315effdcf1fb1fc9e5e85ff6813e1a3aefb06e29b6`  
		Last Modified: Tue, 24 Feb 2026 23:16:39 GMT  
		Size: 135.6 MB (135627100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85539e814e540f9d00b7224cd49be352e35a868488f6f7321ac90e5d3c370e6`  
		Last Modified: Tue, 24 Feb 2026 23:16:37 GMT  
		Size: 19.5 MB (19463281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333f04e2e7821a02e1d51c7bbf9e2d272f6e2f615f95b1105562abf2d05356f0`  
		Last Modified: Tue, 24 Feb 2026 23:16:36 GMT  
		Size: 4.5 MB (4517733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2bd2c5557b06cc9eaa020df4c1028303778722c58a484269198e81173947e3`  
		Last Modified: Tue, 24 Feb 2026 23:16:36 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f9d949033861820eb5925bbfc85db3f217cf420bd9846e1c37c61cf8c7ec9f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4291913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e7a608d9780a4b19c731f47e83c17cedec5e6fb26cdb07ed6b5435ffa7d51f`

```dockerfile
```

-	Layers:
	-	`sha256:8481e7c789865226445cea226153fb3ebee2c32781ec77657a3becc5f6007c77`  
		Last Modified: Tue, 24 Feb 2026 23:16:36 GMT  
		Size: 4.3 MB (4273545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:661537c4e14d2498379edb7cab508bbf5191bf53210aafdbef884631700a10a0`  
		Last Modified: Tue, 24 Feb 2026 23:16:36 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json
