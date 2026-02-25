## `clojure:temurin-8-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:fc8ab791f07587c70713ca69c27ef50ffb4069e2d0bc3ae57b7d72757d661ca9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f26b881406c7e6e68ce904370dc4a8b2eecc40ee3c10a85a58e7d830f01227fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 MB (105682899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:202f1ab28c0806fde9aa9ac53c2ab99cfbadaaf02dbdac128d8868ad50ad8382`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:52:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:52:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:52:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:52:18 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 19:52:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 19:52:18 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:52:32 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 19:52:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 19:52:32 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 19:52:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 19:52:34 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97aae01c62b9df7f3fbf2a11f54b94522290106e9776dc061fb344f48a9f4677`  
		Last Modified: Tue, 24 Feb 2026 19:52:48 GMT  
		Size: 55.2 MB (55170084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd38697e22235554c6b5356f941b130d6bb6c3fdad748f85525ecff76fa26ff`  
		Last Modified: Tue, 24 Feb 2026 19:52:47 GMT  
		Size: 17.8 MB (17758754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32da94fac9f0be80f598b69bc92e74f00b7a71103cd9147777109a18dae9f0ee`  
		Last Modified: Tue, 24 Feb 2026 19:52:46 GMT  
		Size: 4.5 MB (4517750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a3a81a3b8fe591e7a0ae1349e9b1f97564365e9b03c44d330e58442529245029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2867439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32759879af1a3c1bd0faa366400861873a9b826ed81a4f6e7a8daba9497c65bd`

```dockerfile
```

-	Layers:
	-	`sha256:396356cfaa93e2622521d6687247d2e44e9113a62ec7bd99c23cbef3d94e0bab`  
		Last Modified: Tue, 24 Feb 2026 19:52:46 GMT  
		Size: 2.9 MB (2851039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ba8047265815b99c6b2e69c55c8d9b9487e76bf63d23bb98ab7cb36de55013f`  
		Last Modified: Tue, 24 Feb 2026 19:52:46 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ff2ae89b9d9020c4d1e14fc7fb1dd7913e167d959fa7b3fe0cd4249cb89d05d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104477285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54cdcad31500491e14d6c851379e93e1dd3cb3d6304ed688b3d1204ac33de5db`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:02:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:02:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:02:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:02:34 GMT
ENV LEIN_VERSION=2.12.0
# Tue, 24 Feb 2026 20:02:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 24 Feb 2026 20:02:34 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:02:47 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 24 Feb 2026 20:02:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 24 Feb 2026 20:02:47 GMT
ENV LEIN_ROOT=1
# Tue, 24 Feb 2026 20:02:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 24 Feb 2026 20:02:49 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5899fd4281eb802180094cd7248a180de2d7f4dd4fadc1ad27cbfc97e09414b`  
		Last Modified: Tue, 24 Feb 2026 20:03:03 GMT  
		Size: 54.3 MB (54251619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d52984f6aa080fa920771cbeaa2e26663ced7abc2ff80d5dd9f9f224d5b664a6`  
		Last Modified: Tue, 24 Feb 2026 20:03:02 GMT  
		Size: 17.6 MB (17591797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2733ba46a24a4d28097af717903c1c3664fb5e539a1e305932898725347180`  
		Last Modified: Tue, 24 Feb 2026 20:03:01 GMT  
		Size: 4.5 MB (4517756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f6a458dd7131d6cd6861a4cdebb9eb5c62301f2bcad830070e8661c0bcee49c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2867875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236369b7f1c3e23cac071fad1c5554b64f0f65971c04190bc65667dae6842a86`

```dockerfile
```

-	Layers:
	-	`sha256:cdec86537e11ea9f4aa9eaaeca5fc64dabe1b16ff375be65f378f1bcb1bf5421`  
		Last Modified: Tue, 24 Feb 2026 20:03:01 GMT  
		Size: 2.9 MB (2851354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a3d996c416f752b0d99ae0ab67d06fc8b52c2ad454ae3cacfe87fe0f3cf8f48`  
		Last Modified: Tue, 24 Feb 2026 20:03:01 GMT  
		Size: 16.5 KB (16521 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:68faf30aac54f611f0b31fbb1ed6f0e72a679a0db0d9acfe28014892a93b4ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107207596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3a393070480d48d73058a387f41e9791557f9c016c6a4830c103c93a7a3900`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Wed, 25 Feb 2026 01:42:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 25 Feb 2026 01:42:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 25 Feb 2026 01:42:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 25 Feb 2026 01:42:23 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 25 Feb 2026 01:42:23 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 25 Feb 2026 01:42:23 GMT
WORKDIR /tmp
# Wed, 25 Feb 2026 01:43:09 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 25 Feb 2026 01:43:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 25 Feb 2026 01:43:09 GMT
ENV LEIN_ROOT=1
# Wed, 25 Feb 2026 01:43:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 25 Feb 2026 01:43:20 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:3def25e912c223ee8b3899e5ca048b2439f856f438ac690293817fbc0291fb36`  
		Last Modified: Tue, 24 Feb 2026 18:41:49 GMT  
		Size: 32.1 MB (32078334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea2f1da9d19213630e76b4b1f91db09749f3dbcc124c3818bfc80ad54656799`  
		Last Modified: Wed, 25 Feb 2026 01:43:48 GMT  
		Size: 52.7 MB (52650395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a498db05d6320cb1f19adbf256b778a5876facab96d5b3a3c9d71d2fc8d6036`  
		Last Modified: Wed, 25 Feb 2026 01:43:47 GMT  
		Size: 18.0 MB (17961093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f874cbb7d8e2ccea031d96ab428bb2d277b54b6ff47f97357d178f4e7c2650`  
		Last Modified: Wed, 25 Feb 2026 01:43:46 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cb9428081530cdf78e1b32b0f1092484d56a3b1f81b6ece88e55bb065721bd10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2869911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c290791579e22ca78fdb6e070e20a1f1d689ceeb8bb15bfc8395b6c8ecb7bbb`

```dockerfile
```

-	Layers:
	-	`sha256:5ba7c6a33f7a27692edd36962d4cd3a8a2819537ae801b3166f6520b39ee415a`  
		Last Modified: Wed, 25 Feb 2026 01:43:46 GMT  
		Size: 2.9 MB (2853467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc76aaec3738caa9dae634b5fdefe43b3abfb8d19374a6f0a81b62794a855827`  
		Last Modified: Wed, 25 Feb 2026 01:43:46 GMT  
		Size: 16.4 KB (16444 bytes)  
		MIME: application/vnd.in-toto+json
