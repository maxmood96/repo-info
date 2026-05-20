## `clojure:temurin-21-lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:b6cec6e7205d4cc189aa85375d9ac7010b815d0ba35a54131fb200b1f3338ebd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-2.12.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:eb308d508db9837c0e4a2deca9768f3c0b3d67bc6a299df7199a0dffb96bf9a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.3 MB (208281504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dbd8af7117717719d0934229440f7ed0ca314467ab0af433d36f4be01dd5c2e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:59:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:59:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:59:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:59:36 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 19 May 2026 23:59:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 19 May 2026 23:59:36 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:59:49 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 19 May 2026 23:59:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 May 2026 23:59:49 GMT
ENV LEIN_ROOT=1
# Tue, 19 May 2026 23:59:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 19 May 2026 23:59:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 19 May 2026 23:59:50 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 May 2026 23:59:50 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8419f4a27c97b0c111ab0dc77e0159bd3abfadcb948d4a49cf6dd6670703b84e`  
		Last Modified: Tue, 19 May 2026 22:36:35 GMT  
		Size: 30.3 MB (30257598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55cf54b8ab450c6b7da5a47a36a3662447abf688cdde3c463723942e0ee40ba5`  
		Last Modified: Wed, 20 May 2026 00:00:13 GMT  
		Size: 158.2 MB (158166905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62016e430cc256fa5c47ba52c0f7bb17898cae0dd6a0dd9519c65f5e74083f59`  
		Last Modified: Wed, 20 May 2026 00:00:10 GMT  
		Size: 15.3 MB (15338864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e848bb883f6a045b5907f7716dc4e89310ab24a350f16ab8920f46f9acdf28`  
		Last Modified: Wed, 20 May 2026 00:00:11 GMT  
		Size: 4.5 MB (4517710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85420da7ccb16c50797b958c8f48023b26a688e94724a7fac9fb50ba1a5aabfe`  
		Last Modified: Wed, 20 May 2026 00:00:11 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:47c3d168aa657cd78d6fbb52de96dfb8dfa4395e4e169ed5fcc5da3617aaa92f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3048618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8766bab23b49b6c82d961413c730a74c89d3a344264d5a6f3032288e7823b2d`

```dockerfile
```

-	Layers:
	-	`sha256:da42b845237cfe014fbcef2f50dbde366c407192e0b4b79b02dc9ee01dbbdbdc`  
		Last Modified: Wed, 20 May 2026 00:00:10 GMT  
		Size: 3.0 MB (3030061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7a1db91249071e2ab04473bd257b93efcc07f4d747fd6fb96e2e1573bee59ee`  
		Last Modified: Wed, 20 May 2026 00:00:10 GMT  
		Size: 18.6 KB (18557 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3bd75dedd49dbc4c0225a7bc33cce7cc0f5d4ab79f32336abdc4fbd8164679e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.0 MB (205049653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09064c11015c97e7355dc07684f0c8260298503ab5c2e963ec3cd925a9d85db`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Tue, 19 May 2026 23:28:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:28:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:28:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:28:49 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 19 May 2026 23:28:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 20 May 2026 00:06:35 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:06:50 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 20 May 2026 00:06:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 May 2026 00:06:50 GMT
ENV LEIN_ROOT=1
# Wed, 20 May 2026 00:06:51 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 20 May 2026 00:06:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:06:51 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:06:51 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2b99ba6638377be8e7e1e9a328ebb001513ab9f700c8168d404eed03437c7ce5`  
		Last Modified: Tue, 19 May 2026 22:36:47 GMT  
		Size: 28.7 MB (28742972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733fff2d2e0188060c0c313378432b6714fcebf95b7e03f8b19ace142be74064`  
		Last Modified: Tue, 19 May 2026 23:29:43 GMT  
		Size: 156.5 MB (156461329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d306bb4359a524ee434f0b5840eb939d8fec086890ebc152206c8ef31cdcdb24`  
		Last Modified: Wed, 20 May 2026 00:07:01 GMT  
		Size: 15.3 MB (15327215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eae04316727e9f79acb4ab56a4f62de142add67eb823927c1e5303756a28936`  
		Last Modified: Wed, 20 May 2026 00:07:00 GMT  
		Size: 4.5 MB (4517708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62761f590731031b30253986c2a37cd8d6af097ebcb0e9cd494a84f8e88e1779`  
		Last Modified: Wed, 20 May 2026 00:07:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5d47128a53fe80a74aa7d8637d42d7785201826fdc4b9889e061f8bf5ebad4ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4bcc377bb8776d1857cee173c7307e19f96fc715606d020cbacabc89f20d48`

```dockerfile
```

-	Layers:
	-	`sha256:5c4a488a23de316816914df8419a3220aca61959992d7962deebbd3b522b9122`  
		Last Modified: Wed, 20 May 2026 00:07:00 GMT  
		Size: 3.0 MB (3029670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:102f19f60502a9d152872a5f96b16fc55cc45af5d613cf4c1b904f53c432cf04`  
		Last Modified: Wed, 20 May 2026 00:07:00 GMT  
		Size: 17.7 KB (17723 bytes)  
		MIME: application/vnd.in-toto+json
