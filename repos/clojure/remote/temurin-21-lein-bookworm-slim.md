## `clojure:temurin-21-lein-bookworm-slim`

```console
$ docker pull clojure@sha256:24ca9682d5ee67a8e588c0e941446b7de64a13606be6254b00dfb8615ad79d29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3bd488d3db7eb4c0f3d7cd7b442a27bce8dc69a98fb287d7950d8c58eb075440
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241840539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d2652f6f3f3e236766372a4d34b9adadd67aa7e50b385ce2aa280af0ca205f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_VERSION=2.11.2
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_ROOT=1
# Mon, 28 Apr 2025 17:24:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5af5d1b17e2607a82bc87ff333ec8679389ea14a0a5604dba0c8797a8387bc6`  
		Last Modified: Mon, 28 Apr 2025 22:07:44 GMT  
		Size: 157.6 MB (157634490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab76b3995cf9394c51302a69d73c6e3435fe694880a74e06bf7c39a285a7ada`  
		Last Modified: Mon, 28 Apr 2025 22:07:40 GMT  
		Size: 51.5 MB (51463782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6532e0e2fc1849e53042135850515bfa99fcc878519545971c7c0b3ca0c33672`  
		Last Modified: Mon, 28 Apr 2025 22:07:39 GMT  
		Size: 4.5 MB (4514195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c935e5aa87b0752efc6f295a7bb7e1fbbe17b510b9cd5d6d91e7653f0aa17e7`  
		Last Modified: Mon, 28 Apr 2025 22:07:39 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8114d537ede335fdaf38bac43be3eeb17b564f78dd3758df9c853d2f29c126e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4344709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fec694fe9f0e65eaa1cc9560db445678e8ca1bc04507a45ecd929bb8b3a18d2d`

```dockerfile
```

-	Layers:
	-	`sha256:8b6bc3271847b72c39b12df1566796e4ce596c17cb09d69c6e248de3541ec714`  
		Last Modified: Mon, 28 Apr 2025 22:07:39 GMT  
		Size: 4.3 MB (4325589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d939e3f3cc954978c9250d2475163d08b540567b33f16e1dac0538249c2943d4`  
		Last Modified: Mon, 28 Apr 2025 22:07:39 GMT  
		Size: 19.1 KB (19120 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:61c9c0bd8862a7004378e75b49258d5b8ea8556cdbac6a715a284fcaef31fa5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239940801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b4a79e7cb9799319251925734046bf2a14479929354aafa29b73d591d70b6d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_VERSION=2.11.2
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 28 Apr 2025 17:24:54 GMT
ENV LEIN_ROOT=1
# Mon, 28 Apr 2025 17:24:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d4ab5dd15c9d773ed92bfed06df23b5bcc8c8b6efafa0f418a37de8edda2a2b`  
		Last Modified: Wed, 30 Apr 2025 01:45:46 GMT  
		Size: 155.9 MB (155928800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932e7d61fe1f4beda84c643f1c3af477970bb76e6f7f70d4aacf2ccf1be13411`  
		Last Modified: Wed, 30 Apr 2025 04:47:50 GMT  
		Size: 51.4 MB (51430778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a96f21a1ab17d5c3c1ceebd090b08106ba6ed2b187c15289f02552977fa5bfb`  
		Last Modified: Wed, 30 Apr 2025 04:47:49 GMT  
		Size: 4.5 MB (4514172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172c18924fa4855c7c13dc9eeb8385a2bb2437e889841e59c4a540481fdb89a8`  
		Last Modified: Wed, 30 Apr 2025 04:47:48 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ae29243bdc3aa97500831a929b45f0c74c022c7a918547eb12641f048b64fc2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4350569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f876f5f9f34e0f15918dce6c0ac9be607c7d3cc167a9eed87704fc20d8a62c1e`

```dockerfile
```

-	Layers:
	-	`sha256:ab2cba101ae71d6100c01c9daebb49dd1118543c107494a21838152121415b13`  
		Last Modified: Wed, 30 Apr 2025 04:47:49 GMT  
		Size: 4.3 MB (4331305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b1b684c8dba097c557c9482053c273d4b2e1ab82fbdbe745ba3e300d97a2a86`  
		Last Modified: Wed, 30 Apr 2025 04:47:48 GMT  
		Size: 19.3 KB (19264 bytes)  
		MIME: application/vnd.in-toto+json
