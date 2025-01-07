## `clojure:temurin-23-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:b49a056075c91699510adb0fcd65ff2af3983928b8e2f060b87380650b631fe6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5fad73e13803d020dcce7976d1bf9855aa4fff354c0e20a8dd513e272936e1db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243126409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0946abca413aa4a97cddf1c8890677671d5d84b93077897d5e58bb2a843876ae`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_ROOT=1
# Thu, 03 Oct 2024 17:49:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Tue, 24 Dec 2024 21:32:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a259facd0a555e91d42b92dab42362049c009a3f0c34948d00093091f458b655`  
		Last Modified: Tue, 24 Dec 2024 22:38:47 GMT  
		Size: 165.3 MB (165295091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420efbb756f1420211ec58cf305d9dde53df9faefda080d932b8838e35ac56c8`  
		Last Modified: Tue, 24 Dec 2024 22:38:45 GMT  
		Size: 43.1 MB (43064096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3911fd0f86881ead5df7302d0b940eb9b3df93fc0bf53d629285b7d1d240ef3`  
		Last Modified: Tue, 24 Dec 2024 22:38:45 GMT  
		Size: 4.5 MB (4514153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4091b125f92220bbc8d98b356f01f9d31ea0e997fe788e4ef17e77fd0b1945`  
		Last Modified: Tue, 24 Dec 2024 22:38:44 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cc5b9563874aeaa73abf12bfc760ce887627e48945e88a5cd12121386e15e994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4591633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f685d45bcd1d5c68db4f28bab637ab23236f93fd81403399c18667237208e5`

```dockerfile
```

-	Layers:
	-	`sha256:d23c27caed931cf0cca1a88ac11c1652630e6e7d6fdad866eed9a7ccca937305`  
		Last Modified: Tue, 24 Dec 2024 22:38:45 GMT  
		Size: 4.6 MB (4573176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9faf775123fe3f2cbc7db5c6f2ffb092359a028b9f33516c0588d21335a391a3`  
		Size: 18.5 KB (18457 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:071d3c72eb7e5c2b61ed0b00d7671bb332b5216984143c892921c628b7cfe281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.7 MB (239651400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c4b18b6656473a8a3a360fb2b600f758a44195089be5b88ba3271e544d3a6e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 03 Oct 2024 17:49:34 GMT
ENV LEIN_ROOT=1
# Thu, 03 Oct 2024 17:49:34 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:879a6187682fc52c69294a2f450abdb54e257a50e8133ec6e89cb140345be6ce`  
		Last Modified: Tue, 24 Dec 2024 21:34:50 GMT  
		Size: 28.7 MB (28744853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5b4fb805b80b71c3e0694a62a0807be3fbcc30b4f67cf6fa8370c3421f0982`  
		Last Modified: Wed, 25 Dec 2024 07:39:53 GMT  
		Size: 163.3 MB (163281786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4404f73aef6003c39af1a81f34cd7be8f42239947797ea53ca15d111c95a8c54`  
		Last Modified: Wed, 25 Dec 2024 07:39:46 GMT  
		Size: 43.1 MB (43110170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ff2426e0ba62062fa1494c21d182e161c2869d3f1cfc33a410a196808fdf7da`  
		Last Modified: Wed, 25 Dec 2024 07:39:45 GMT  
		Size: 4.5 MB (4514163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e139e2f522a692e3c10b91824bf86b3d7bae26b65ce2c09d844fd37829667d15`  
		Last Modified: Wed, 25 Dec 2024 07:39:44 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b0ff3101871fbdb330736fd362fb68b8da61d08e8e5d5c874c0e43e94d60af01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4596797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b02b4f277d01f9fb7ea2ded3ea7588200415cdfe7f6cfc18f4abf43e92c27b04`

```dockerfile
```

-	Layers:
	-	`sha256:174d14e69a293fa08a3d4b9a70e260e1cb20e1d909003195e6a1987c23f2c9df`  
		Last Modified: Wed, 25 Dec 2024 07:39:45 GMT  
		Size: 4.6 MB (4578219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97d86e37c260d47665ba33aeae0419e769b0847cdf9b98d48fa9d451e88e291c`  
		Last Modified: Wed, 25 Dec 2024 07:39:44 GMT  
		Size: 18.6 KB (18578 bytes)  
		MIME: application/vnd.in-toto+json
