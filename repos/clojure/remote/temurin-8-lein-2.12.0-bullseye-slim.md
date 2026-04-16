## `clojure:temurin-8-lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:77422acdb23e75469528894f821623ea076854044adc90715d9f8782b36cfca9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-lein-2.12.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e7eabaf256ae58b1d9c955a82f6587e69e7f7b3080ee73a7f004a4d18437f43e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105284652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77754ac203a34af65b0027061456a0b2eb1b520d78dac0be99b7cda7717ea0b7`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:00:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:00:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:00:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:00:38 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:00:38 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:00:38 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:00:52 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:00:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:00:52 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:00:53 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:00:53 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ccd20bf91cccfce6531f295a874c225a9be34c83dc806eba8c8beb3f42c3068`  
		Last Modified: Wed, 15 Apr 2026 22:01:09 GMT  
		Size: 55.2 MB (55170083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27e3502f86aa92f10c4b2af3e0ced2de766c091d3088e1e6e655a09ceb1b0fe`  
		Last Modified: Wed, 15 Apr 2026 22:01:08 GMT  
		Size: 15.3 MB (15338806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8b6185add1c4774e0d4c6e7e3c99c26a4a631adaf2df9a6f60e772bd11750e`  
		Last Modified: Wed, 15 Apr 2026 22:01:07 GMT  
		Size: 4.5 MB (4517712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b1dbb33fd041a8c4dd66a53ce0547655f55de09f5944efa40ce15bac74041b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3164971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0724cc21a645bc45ad575d1bf879adb493f4aa54d8ec192d5e2f0dcaa838a83c`

```dockerfile
```

-	Layers:
	-	`sha256:13d5e033c8fa1c8372fb0c8b933d1c19d158e065c7c9e159d6c728ff87f82697`  
		Last Modified: Wed, 15 Apr 2026 22:01:07 GMT  
		Size: 3.1 MB (3148571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e57fdbd53af65b86ce7fae48d94eea5320a73e23867bcd76eb5e87dc992e2ebb`  
		Last Modified: Wed, 15 Apr 2026 22:01:07 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4d1679aa1ae31a198c85b10cf6a3c3a56b134243c6885bb13ee7ed074a48772f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102841272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b3f013804885c085c5b114e78c0780e28b031296f7e54e29ac93ce556963af`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:12:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:12:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:12:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:12:13 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:12:13 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:12:13 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:12:27 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:12:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:12:27 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:12:28 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:12:28 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74a53ed7b4492344cea07ef60879a80d7870eddda7737edae3fcd23dfe993f55`  
		Last Modified: Wed, 15 Apr 2026 22:12:42 GMT  
		Size: 54.3 MB (54251614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267ede738cff40890be3344414febcffe434af1677e9cb474e9f2c993b68e2f2`  
		Last Modified: Wed, 15 Apr 2026 22:12:41 GMT  
		Size: 15.3 MB (15327224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35cb250a3cb92dfce3b0424dd3b7f0c6a03455b6e40ed8d1a9185712da37d72`  
		Last Modified: Wed, 15 Apr 2026 22:12:41 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7f399ebd57b4d474c1cfc3208a9668fd987192fcca67cf35b55ca2d8445763c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3165401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed755d9235d855f5733766288f5a5d24de6d37850b827515469765ffe48bd41`

```dockerfile
```

-	Layers:
	-	`sha256:6e60fdaabd75f958b8b2e0609f4b243afbf5eb1d2d2af9ba3175a95659830830`  
		Last Modified: Wed, 15 Apr 2026 22:12:41 GMT  
		Size: 3.1 MB (3148880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7279007fdea4342fe3357c3685e656641be14237b3f2431df50fc9461d4513e7`  
		Last Modified: Wed, 15 Apr 2026 22:12:40 GMT  
		Size: 16.5 KB (16521 bytes)  
		MIME: application/vnd.in-toto+json
