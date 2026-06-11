## `clojure:temurin-26-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:c8acdd99e67a2d0625be22d01df86aa172e066e55fd04d3e865b296c5d6b418b
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

### `clojure:temurin-26-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a4cecd0ae6d0ff9a37601e309a2186ce8dde5e0d2bbec43780335544ea4f3dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.0 MB (145040263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd2dda4bda97998113e8e01ac26f658ecc693cdf4df1c840820f79bbcaf7e48b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:21:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:21:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:21:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:21:35 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:21:35 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:21:35 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:21:56 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:21:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:21:56 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:21:58 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:21:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:21:58 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:21:58 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7d85cedab5e503826e8c41fa1a366835f281c3e903f3df029f3128185e4ee7`  
		Last Modified: Thu, 11 Jun 2026 01:22:16 GMT  
		Size: 94.5 MB (94524364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0f7f9aa56d5fa07c4153b3efc354b2b7dfe5c2ada5285155c52244eb87e5b0`  
		Last Modified: Thu, 11 Jun 2026 01:22:14 GMT  
		Size: 17.8 MB (17760094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d9863d907c0b4d6b96360544ecd28956c641d737abd2f1301c2c1e8908bef6`  
		Last Modified: Thu, 11 Jun 2026 01:22:14 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb6452a7f5eec44c12ca10438d7e888e07a9cf957e7d3e5c9b4ae516578edc6`  
		Last Modified: Thu, 11 Jun 2026 01:22:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:14d2cecfb4e060b496fcc611a93376f67056bf820c10c6c2edc7f6a8b3cb9e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2714154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fec5c761995d2cec2463032867d49e53eeaab06e856521c2621aaaf8ccc6a7d`

```dockerfile
```

-	Layers:
	-	`sha256:86f503de1169667dd1cb90a39d051c92643fdd4a744b43e62671193a6f390340`  
		Last Modified: Thu, 11 Jun 2026 01:22:13 GMT  
		Size: 2.7 MB (2695604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ca9d0b1a51b33f78c8795763220a3b30e3334bf4ff3fcd003102262e90cd96d`  
		Last Modified: Thu, 11 Jun 2026 01:22:13 GMT  
		Size: 18.6 KB (18550 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a954a930ecb69644cc6f4a880c3adfdcff7c9f3858ca5f1e35b856c46305a489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143738767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdae8adacb1176b8b8234a333ac65553901f2d9692fead3b36729ef42b7bff17`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:25:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:25:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:25:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:25:38 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 01:25:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 01:25:38 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:25:55 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 01:25:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 01:25:55 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 01:25:56 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 01:25:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:25:56 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:25:56 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be672714995d926592a61ba26a633b1f3f3d71e4af0965f297bbad36ceed1a1`  
		Last Modified: Thu, 11 Jun 2026 01:26:14 GMT  
		Size: 93.5 MB (93504349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a158ab567cc0e28b1e665df4f4f931cd2412453aab8e376254b57b46904f04`  
		Last Modified: Thu, 11 Jun 2026 01:26:13 GMT  
		Size: 17.6 MB (17593962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d7096a06152637452f2b39695417f2180fe8c89abd5cfaa1569d5bcc8ea672`  
		Last Modified: Thu, 11 Jun 2026 01:26:12 GMT  
		Size: 4.5 MB (4517722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ade2f9862519c6d65ff19e625e87156752fc3d509e7bef35677bcfdefc87a4`  
		Last Modified: Thu, 11 Jun 2026 01:26:12 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d280c8a0f21bbe07c29a1debdefef8dbe7a63f808761f0d22b1889bb92e9caa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2713887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64c9ed2a7334eca1c4edf800f42c65be362cea75e6912fe0a7b28b3d25cf27c`

```dockerfile
```

-	Layers:
	-	`sha256:dded71fe1261177eea21b611300cab026cd145122f7193b71da523db7a2522bc`  
		Last Modified: Thu, 11 Jun 2026 01:26:12 GMT  
		Size: 2.7 MB (2695216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35b387dbcdc34d234c981cfa4a2ded97aaf5baae5ad9a9592bd0d88b8153532d`  
		Last Modified: Thu, 11 Jun 2026 01:26:11 GMT  
		Size: 18.7 KB (18671 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:ca2ca4d80467a0a137b6e4b08bfc63155b8c804e6af62f8a80a6c05d636f5232
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148465798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bad7e1b0be2c2ef2c911187d29e438ee1749c9dc3bff11c04659487de597338`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 09:50:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 09:50:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 09:50:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 09:50:03 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 09:50:03 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 09:50:03 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 09:50:30 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 09:50:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 09:50:30 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 09:50:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 09:50:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 09:50:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 09:50:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:23f7cdee3ef2598b081c2b848fee95730a7ab2b1cc5b726c72dcb8c2fe3632f7`  
		Last Modified: Thu, 11 Jun 2026 00:21:33 GMT  
		Size: 32.1 MB (32081941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f46f239b276d689990cc6b2bd012c161df5f6f63e0a47f8e010857cf9c83c4`  
		Last Modified: Thu, 11 Jun 2026 09:51:11 GMT  
		Size: 93.9 MB (93902055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5bcd477cddae9fb720808674828657aaa5626a08d12107aedcda01a6d935184`  
		Last Modified: Thu, 11 Jun 2026 09:51:09 GMT  
		Size: 18.0 MB (17963655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c40a07552db7c39ccd5cbedbd2f575f332cde8fdab498148aab7ec295f97f3`  
		Last Modified: Thu, 11 Jun 2026 09:51:09 GMT  
		Size: 4.5 MB (4517720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45cae1287bb16aaaa2ae48c4d7fa7c89660cda0ce328b65307ec10cf70376ead`  
		Last Modified: Thu, 11 Jun 2026 09:51:08 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6b7beeae6bbf08d7eaabbf9da587b5c5d87db57564b7185a27ef3522743e8731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b61d4c30d2672fa2ea58ebad4ebb75018d6da7427ba5f89e751382d2d579ad5`

```dockerfile
```

-	Layers:
	-	`sha256:12f111c499366be70783245502cfc73f74bef0feb44a0596cf7fd17cd0b3dae7`  
		Last Modified: Thu, 11 Jun 2026 09:51:08 GMT  
		Size: 2.7 MB (2681373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef5a6a967ffb5d8e9116a5c54db51a7640affbd4496ab01d6ec4a8c0eff1c208`  
		Last Modified: Thu, 11 Jun 2026 09:51:08 GMT  
		Size: 18.6 KB (18594 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-lein-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:5bbc204692452515c810e8be7cdd501f2ab018098f29eacedb61b35c8704be8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139372569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ddb5296beeaa49a4afdfb408882123aa3b1627e948e0caae9b483ba90bc8e0a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 03:15:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:15:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:15:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:15:32 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 11 Jun 2026 03:15:32 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jun 2026 03:15:32 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:15:42 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 11 Jun 2026 03:15:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jun 2026 03:15:42 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jun 2026 03:15:44 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 11 Jun 2026 03:15:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 03:15:44 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 03:15:44 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c95e0687f25470aace14b514fbf30caeca0dadb23874709d13232572d3ce19c`  
		Last Modified: Thu, 11 Jun 2026 03:16:09 GMT  
		Size: 90.5 MB (90536949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:674b9f079b8f328b24a9b63f38e72c13505ef09051d512856fcacef97c3d1405`  
		Last Modified: Thu, 11 Jun 2026 03:16:08 GMT  
		Size: 17.4 MB (17423968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995a677820afdc73e3b6c13f4f1ecbbfe8578bba05ff9cb030fd757dd7626209`  
		Last Modified: Thu, 11 Jun 2026 03:16:08 GMT  
		Size: 4.5 MB (4517717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5f21dfcd4a0a0b505e61926c9829eafcda5da6b32362843e2760fcb3a0917a`  
		Last Modified: Thu, 11 Jun 2026 03:16:08 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d69f99adb4c25a04006a36878fab6fb8f6fa17e66ac248d80564273f4566422f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bd420d07bade96bd4f8c3e5fa846f0816fd8117c8d5617dde11258e2aa8bd5a`

```dockerfile
```

-	Layers:
	-	`sha256:16459b4f4c204e8781eb0d9293f85904d4ebc398f22245ae2c2915d1cfa5e39c`  
		Last Modified: Thu, 11 Jun 2026 03:16:08 GMT  
		Size: 2.7 MB (2672604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baa814b625147563c47ef25e3c34dd52759e8cd29123de0a4d9b238523b12764`  
		Last Modified: Thu, 11 Jun 2026 03:16:08 GMT  
		Size: 18.6 KB (18550 bytes)  
		MIME: application/vnd.in-toto+json
