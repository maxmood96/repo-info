## `clojure:temurin-22-lein-2.11.2-bookworm-slim`

```console
$ docker pull clojure@sha256:fdbe47154714c46c4ba433ec1c23ff9a9cb65fea2fd1c40ccfa1791df725c35c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-lein-2.11.2-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:401719b1247f4249901fe74361708af539e845b77e7ae4222713a4f7c6a143d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.2 MB (241227292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09ffbf8a00dfccb4685f35c26ecca0a9e7d4ac8b600673ca5ba46b36af13093d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_ROOT=1
# Wed, 07 Aug 2024 18:04:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3c4bf3f699279d533d4c3a0937f07c30bd2fcb155240e81521a055ebaa17a9`  
		Last Modified: Tue, 13 Aug 2024 01:11:48 GMT  
		Size: 156.5 MB (156481616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebc525f6e4fa179583dcb55c49eff0d243d061da0cfe9616d791110c2317876`  
		Last Modified: Tue, 13 Aug 2024 01:11:47 GMT  
		Size: 51.2 MB (51220976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2980285a20585b6f8137cf1f68012035d05c5184da74b7170367cdab2417c2ff`  
		Last Modified: Tue, 13 Aug 2024 01:11:45 GMT  
		Size: 4.4 MB (4398040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49c62c652232978feed1a10d07aeeca0b6578db1f1d1178ba69d000121ee0b3`  
		Last Modified: Tue, 13 Aug 2024 01:11:45 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-lein-2.11.2-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5bab05814f6e0d516a06063f9243c84956c036bc73315e8bc9118f8e1ecbae2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4171095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143380af9f2b1c451ce803b16958d5dc770083bb5b5619d8fa420a987c69a283`

```dockerfile
```

-	Layers:
	-	`sha256:bb31432e05b80f6d9a88a216604d828a5405ea4e975d3da17fd968b3b7888ba4`  
		Last Modified: Tue, 13 Aug 2024 01:11:45 GMT  
		Size: 4.2 MB (4153003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:117bcd42163ec1f64ed484946498b143c0091c9d13c5ee8bd3a126f9a4db9f8b`  
		Last Modified: Tue, 13 Aug 2024 01:11:45 GMT  
		Size: 18.1 KB (18092 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-lein-2.11.2-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:744a67219baf31adb1bc0a4218215018ff9014e2c7c407c9d4f2000fb67d1935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.2 MB (239154167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36128d8ee4a9fce1ff167ee02c76f0820f491d90b099908ca315892b5a8e6687`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:51 GMT
ADD file:9b9556e1f3168a82eb85577dc07d85b2e7c1a72c5c35a4003f00042dd27b4fa2 in / 
# Tue, 23 Jul 2024 04:17:52 GMT
CMD ["bash"]
# Thu, 25 Jul 2024 20:19:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 25 Jul 2024 20:19:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Jul 2024 20:19:09 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 25 Jul 2024 20:19:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 25 Jul 2024 20:19:09 GMT
WORKDIR /tmp
# Thu, 25 Jul 2024 20:19:09 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 25 Jul 2024 20:19:09 GMT
ENV LEIN_ROOT=1
# Thu, 25 Jul 2024 20:19:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 25 Jul 2024 20:19:09 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 25 Jul 2024 20:19:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:262a5f25eec7a7daccd94a64695e41acca5262f481c3630ef31289616897aa40`  
		Last Modified: Tue, 23 Jul 2024 04:20:29 GMT  
		Size: 29.2 MB (29156571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7f2eca2f194e40017ac8fef9f5d14b15efaa72a7dca868db3e663fe43a543f`  
		Last Modified: Thu, 25 Jul 2024 21:28:13 GMT  
		Size: 154.5 MB (154503730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:256bf5e882a2b05b41379f7c835601a8ae0a46e17023daca24decd17741ac797`  
		Last Modified: Thu, 25 Jul 2024 21:28:10 GMT  
		Size: 51.1 MB (51095346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0638784f559d37d38bf1165948b64d3d2c7de4852fa065cab4c83ae5489ed587`  
		Last Modified: Thu, 25 Jul 2024 21:28:09 GMT  
		Size: 4.4 MB (4398092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3eb997c59f9fdbdef483927098bab9d3d1af9862f84ccb1268d2b53b37fa85`  
		Last Modified: Thu, 25 Jul 2024 21:28:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-lein-2.11.2-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:161d6829f51387a37ba6af620416fc1dce5b915c9a227be05e9cb48b093fbed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4177950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8808036703fa5485aed93b26cb586aa1a9930fb966e01dd724fc2412d96cabd`

```dockerfile
```

-	Layers:
	-	`sha256:23c9933b5081d3c4b6918979346d5c1de553916a489583741cd6454e1568bef9`  
		Last Modified: Thu, 25 Jul 2024 21:28:09 GMT  
		Size: 4.2 MB (4159329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e399a874ec77c29624e11df9f9e371b0eb7b4816577da0d10c2cc41d2a1a93af`  
		Last Modified: Thu, 25 Jul 2024 21:28:08 GMT  
		Size: 18.6 KB (18621 bytes)  
		MIME: application/vnd.in-toto+json
