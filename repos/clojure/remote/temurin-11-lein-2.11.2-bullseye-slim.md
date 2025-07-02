## `clojure:temurin-11-lein-2.11.2-bullseye-slim`

```console
$ docker pull clojure@sha256:e9a8500ca804ed01d288e43693c4342e1c442e54a154b4351efad46f25eb5a78
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-2.11.2-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f96551dcff2797c1307cbec3ea928ab7d18bdd730380811d1a904cc86ef9818e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.7 MB (223685879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40cf55260a38bda2c2a89e5e99a8ea8004ed8ef3d546e0f7e19437b24690cfc1`
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
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
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
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f60f00dcc0f671e4052ecd35c992a08489bb8d39b1dd2313761f335e65192abd`  
		Last Modified: Wed, 02 Jul 2025 04:16:15 GMT  
		Size: 145.6 MB (145635736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d13b7bea265d7b363e4cbb9b199a869fb3b13b096d8934d7f592dae0c45c4e`  
		Last Modified: Wed, 02 Jul 2025 04:16:14 GMT  
		Size: 43.3 MB (43279847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc529725dc84cdcc483cef5d60c3b009166f67b0df9876cc665e571362d7ade`  
		Last Modified: Wed, 02 Jul 2025 04:16:13 GMT  
		Size: 4.5 MB (4514217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.11.2-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:59fa0b46977cee98d770b1ec3ee605ab7bb0ccc8184484fca0065ffb4d5f6275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4767339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd56c8dfc9506f4251d5eb77dac9e903a0a76755c3504de925b6e09302843cd`

```dockerfile
```

-	Layers:
	-	`sha256:ada3998cab69ca5aca0aeca904fbee666bc3aee17eb09f30d967e2c5e34eb49b`  
		Last Modified: Wed, 02 Jul 2025 06:35:51 GMT  
		Size: 4.8 MB (4750876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0a9177755107e9355952c895a4d0cedfd5f1fde6a0567816a143995ff5b3fd1`  
		Last Modified: Wed, 02 Jul 2025 06:35:52 GMT  
		Size: 16.5 KB (16463 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.11.2-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:519db74de582f76c39e3eda708aea9de00cb6b922ecb93d20fb14fa19f5aae7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.0 MB (218995833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4578603179a57c6ea69f999454462d0149dc5579c6acd4dab52b302561db59`
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
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
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
	-	`sha256:00ce3d02ade4a2c8e5e37b1a218bb5c24c995bd8757095b89316c42854286fe8`  
		Last Modified: Tue, 01 Jul 2025 01:15:35 GMT  
		Size: 28.7 MB (28744140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd3a9e6918453f2c489bf587b46ba0d4ae0d4119e108c41f5aaf2474444f623`  
		Last Modified: Wed, 02 Jul 2025 11:44:55 GMT  
		Size: 142.4 MB (142420682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4780ab3714330c5c64468ceb6b0dd089c460a126a7223c58ecd18036cfdd1fdd`  
		Last Modified: Wed, 02 Jul 2025 12:19:54 GMT  
		Size: 43.3 MB (43316820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1bef1a0668542e2ae978ac133e15274e21826602a8b2572dcf6286732c0b5e0`  
		Last Modified: Wed, 02 Jul 2025 12:19:49 GMT  
		Size: 4.5 MB (4514159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.11.2-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fa9e66509da0b59bac6dd30b26c43fe09937c5b280689905edb0d76c392fdbe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4773742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c1f89bda3a49be03c0f9b815413fd2b59cdd69044966e2cbaeec39aa64d24b`

```dockerfile
```

-	Layers:
	-	`sha256:6364afb2b639ce59d0e9851530e05b37a8c1a0606190c76fdfa0c26357d45c4b`  
		Last Modified: Wed, 02 Jul 2025 15:35:56 GMT  
		Size: 4.8 MB (4757158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b3b4b458af3c53b326b9f964c4465414befe9b15d47bd43f13cdfa3a170b855`  
		Last Modified: Wed, 02 Jul 2025 15:35:57 GMT  
		Size: 16.6 KB (16584 bytes)  
		MIME: application/vnd.in-toto+json
