## `clojure:temurin-11-lein-2.12.0-trixie`

```console
$ docker pull clojure@sha256:b6145d444863f62a204d8f2f6db37872d14e6fb2fd100ad5f3e6457437598c55
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

### `clojure:temurin-11-lein-2.12.0-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:b4f32f4d2e8553db1cd852afcee11eabfe0e5f9fafabbb066b8e194340f7359a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218291709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70b5eaf1e44496da327e40fd782521cbd17b673ab94611bae6bba223200b068`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 29 Apr 2026 23:14:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:14:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:14:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:14:43 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 29 Apr 2026 23:14:43 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 29 Apr 2026 23:14:43 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:14:58 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 29 Apr 2026 23:14:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 29 Apr 2026 23:14:58 GMT
ENV LEIN_ROOT=1
# Wed, 29 Apr 2026 23:15:00 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 29 Apr 2026 23:15:00 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:3b32e3bb7338c216b077e95920ae53332d81bd57f4a7393bc324432d5a3f88a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:56 GMT  
		Size: 49.3 MB (49302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5641d3a6e97cfa09683d4495d3383c3afcb5e1af41012442383ff392f4ee24e5`  
		Last Modified: Wed, 29 Apr 2026 23:15:18 GMT  
		Size: 145.9 MB (145886246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2860f43ef3f3c3608a1c00c916037bc02e862908afdf4f078cb6767cf2473ef`  
		Last Modified: Wed, 29 Apr 2026 23:15:15 GMT  
		Size: 18.6 MB (18585587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36fa48d746c55bf20f09c7a14719fa76f4554bd95781c7c24aabfd388b71b9b`  
		Last Modified: Wed, 29 Apr 2026 23:15:15 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:91f9fe90eff31e2ce50758671aa9559dc7b1c93f2138fb0f1e3a2afa1ec1097a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3852034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6397b3b9f7699282e356442e6e9c369ecabcfc5b48961f88808960f519f3d26`

```dockerfile
```

-	Layers:
	-	`sha256:b57c19b921bbbf0cd40f8012095fe2f58ae7767dc644a792b40d9955108bc1e5`  
		Last Modified: Wed, 29 Apr 2026 23:15:15 GMT  
		Size: 3.8 MB (3835670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36870ad4944614f20efe0f4ea24dbac96be06a38d4449d97aed8b3055bd84218`  
		Last Modified: Wed, 29 Apr 2026 23:15:14 GMT  
		Size: 16.4 KB (16364 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ba41b110b9590b30f692c9c7d47a460f8eb755a7c62ed910f26bb11cb53fba07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215316423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2ffd004ad142671555bfdccd8e6b4e0f16cdb6655067002c062727c45cd89df`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 29 Apr 2026 23:14:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:14:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:14:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:14:24 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 29 Apr 2026 23:14:24 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 29 Apr 2026 23:14:24 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:14:40 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 29 Apr 2026 23:14:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 29 Apr 2026 23:14:40 GMT
ENV LEIN_ROOT=1
# Wed, 29 Apr 2026 23:14:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 29 Apr 2026 23:14:42 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:6e7932d5cb5573d1bff4fb8801baad19fc72d2ae741bb046333573653944f5a5`  
		Last Modified: Wed, 22 Apr 2026 00:16:45 GMT  
		Size: 49.7 MB (49669245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1847c42d906610f4e7f0da970361c9f6503c696326e0a4cfa91a57474cf05c47`  
		Last Modified: Wed, 29 Apr 2026 23:14:58 GMT  
		Size: 142.6 MB (142583978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93af101131fc861d5b6279d5bda3723bc3e7cd56e7030c15aa39d8be410f12f7`  
		Last Modified: Wed, 29 Apr 2026 23:15:02 GMT  
		Size: 18.5 MB (18545426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d789441854638c82dc2d2fb940fd5c55f6e19cf47fcf6214a0f93bdcbcbac9d`  
		Last Modified: Wed, 29 Apr 2026 23:15:02 GMT  
		Size: 4.5 MB (4517742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bbab5b117b0923f8893eb4f28ba023b1da103d017b36763892426df2a2193605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3853650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde2980aa37bb14a94d98430ee542717da55542c564ec2b1cffca0da65f09121`

```dockerfile
```

-	Layers:
	-	`sha256:075274824115ddb13b61feece99e4f9cae3760c036ac099e7ac25ab33025c8b1`  
		Last Modified: Wed, 29 Apr 2026 23:15:01 GMT  
		Size: 3.8 MB (3837165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df94516aa72d073c610a5e7037741883867789695cd4a09deef6996c47e7c5bc`  
		Last Modified: Wed, 29 Apr 2026 23:15:01 GMT  
		Size: 16.5 KB (16485 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:b61cc7b4c99e854fb61fc04fccc3216430cd4c3cf83a0082284eb273d8a0abc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.4 MB (209391501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d80367f385146523cf844ed84ada99abfcdc10a6ac428f65e2fa4fa15da5af`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 29 Apr 2026 23:26:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:26:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:26:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:26:19 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 29 Apr 2026 23:26:19 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 29 Apr 2026 23:26:20 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:27:14 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 29 Apr 2026 23:27:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 29 Apr 2026 23:27:14 GMT
ENV LEIN_ROOT=1
# Wed, 29 Apr 2026 23:27:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 29 Apr 2026 23:27:20 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:0fab4f6170940889900b2327e1b3c62dace993eab8074ca7d33d1ffeef137c08`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 53.1 MB (53122984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83d3f9164ab25430162fda4ae96737ee70b192a586d3cbba3df6cdb4585addd`  
		Last Modified: Wed, 29 Apr 2026 23:28:16 GMT  
		Size: 133.1 MB (133109620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db19ad95ca64106c6a3e0e8889f2b0e683105ca314259a86effa50182bf18a1`  
		Last Modified: Wed, 29 Apr 2026 23:28:13 GMT  
		Size: 18.6 MB (18641110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59ff2de3e0a5b011e038334f320aebecb5dd1a43329276e4c54e28bf83ad20e`  
		Last Modified: Wed, 29 Apr 2026 23:28:12 GMT  
		Size: 4.5 MB (4517755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2ff70c767f948c8814db85a8e7f85f17e9f1493c7afd72e812af5a305aa3f8c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3852461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f0448744b005d46e978796867d85e1f06c93457b7937e594ae83d7bbc7ce20b`

```dockerfile
```

-	Layers:
	-	`sha256:a4b9511a6c78de4b544ebf57859ee6ac3ea76ed4376221f26fec90da32886422`  
		Last Modified: Wed, 29 Apr 2026 23:28:12 GMT  
		Size: 3.8 MB (3836055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:534a72c5eac6d20b5b1acf993ee53c2d14dc1c5b01ba7cd11e6b17b43f8b9f3f`  
		Last Modified: Wed, 29 Apr 2026 23:28:12 GMT  
		Size: 16.4 KB (16406 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.12.0-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:2d57cb1358e21616037aeb7fac34ce9d80d333b140d9b56dbc481c9950c1790b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199169317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2785c19a43f025337a80736c06a0c394993376f0fbf8caf8a58bb40eb3fd4add`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 29 Apr 2026 23:13:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Apr 2026 23:13:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Apr 2026 23:13:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 23:13:53 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 29 Apr 2026 23:13:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 29 Apr 2026 23:13:53 GMT
WORKDIR /tmp
# Wed, 29 Apr 2026 23:14:11 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 29 Apr 2026 23:14:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 29 Apr 2026 23:14:11 GMT
ENV LEIN_ROOT=1
# Wed, 29 Apr 2026 23:14:13 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 29 Apr 2026 23:14:13 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:943402c24d6e7299016c00f751297dfb5fc1821547fdd1d9c56a206079784185`  
		Last Modified: Wed, 22 Apr 2026 00:17:09 GMT  
		Size: 49.4 MB (49372106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3e96a498eedeba06f7eeeef03757ec4a5de489cdb2735c62011540f27ec753`  
		Last Modified: Wed, 29 Apr 2026 23:14:39 GMT  
		Size: 126.7 MB (126652714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d900321ae0c64c69e1e6539c1f1a0da4e0f902966e1018136bc628056ba905`  
		Last Modified: Wed, 29 Apr 2026 23:14:37 GMT  
		Size: 18.6 MB (18626705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e51f7901d0e61751a68dc6c15d35cbd3f377cfd405f270d41f69a86958853a7`  
		Last Modified: Wed, 29 Apr 2026 23:14:37 GMT  
		Size: 4.5 MB (4517760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.12.0-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:da9f7b6f4b30519c30359392e945b66ab353e1ac6cff28af3e79934bc0dd3d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3848465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8173e214b1497abc78fdca9b67b8e2934f55743be6ba0d488f6b07b254ed124e`

```dockerfile
```

-	Layers:
	-	`sha256:db15ad82c9bc7bcba9573bdfb4cf5e219303005270eed0b0793177e7888e7591`  
		Last Modified: Wed, 29 Apr 2026 23:14:36 GMT  
		Size: 3.8 MB (3832101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b180d4e68e3f32f2942a6904279e7c94dba63b9c183ca9431c6758452635fde`  
		Last Modified: Wed, 29 Apr 2026 23:14:36 GMT  
		Size: 16.4 KB (16364 bytes)  
		MIME: application/vnd.in-toto+json
