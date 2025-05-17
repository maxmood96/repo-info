## `clojure:temurin-8-lein-trixie-slim`

```console
$ docker pull clojure@sha256:bdfcffc5c1eda290d122a28717f96b91eb86e3a1dcc04361cf4a155aca48c54b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-lein-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a044b9e7cfeaef7dad2abdee6dc0fe24472403bda06c8720c968b57e57c0c0c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142797189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c2f294225fd249cddebdde2b02208ba09aa2e256be1075a3652c1ffc702dea`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:3ae34fc80ed56f2b3a9a0b682b58e28e57fe981f5e514c3f687044f4b967608f`  
		Last Modified: Thu, 08 May 2025 17:06:40 GMT  
		Size: 29.8 MB (29753912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c13874b33798a337016f791194bb7e61be946f9cc2a04c97836c5ac8d0f1543`  
		Last Modified: Sat, 17 May 2025 08:40:06 GMT  
		Size: 54.7 MB (54716157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6c8412aa2bccec7db0b1759a07fc9a900a936dc54598d74f6ad3bcf2f6015b`  
		Last Modified: Sat, 17 May 2025 14:00:38 GMT  
		Size: 53.8 MB (53812878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6846cca5deb4b7d1c7d28ba4e0edfb1e1a365e57e952e2a293fc85d82742c3`  
		Last Modified: Sat, 17 May 2025 08:39:53 GMT  
		Size: 4.5 MB (4514210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a4ce6b996269297f9a13e2f285a7900aab361dbfd3e2bdecdbb0482c4c594be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4257823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb1046568411fae0a0266c192e6d3a04fa3b7c80a91ca3da8efde7e011ceb34`

```dockerfile
```

-	Layers:
	-	`sha256:2eef4fbf6802dba05f90b8ab1610663958af3b83cb84a7386a304e4ed94fbb93`  
		Last Modified: Tue, 13 May 2025 17:53:41 GMT  
		Size: 4.2 MB (4241390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22bb6ebc8569f912897d321b88f59d64d2f58fca42f05599d1c8f1e0d992305a`  
		Last Modified: Tue, 13 May 2025 17:53:41 GMT  
		Size: 16.4 KB (16433 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ca82cccab934decb58d43108f2b9350049fc5f6162c869fca9e5492e75be74c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142332462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053404b7264e06a5336cc7930127818be2a00dbf4213888058051592f7d3506c`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:d0342bfffaba1a8be0950e44b5334c6cf9a05d9eedd81a042ec7813ac91850a4`  
		Last Modified: Thu, 08 May 2025 17:31:22 GMT  
		Size: 30.1 MB (30130233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f7d0ac33a92caa5a19b42990018d98913c7f66e7505f06fda9bb39796c5cbf`  
		Last Modified: Tue, 13 May 2025 17:54:29 GMT  
		Size: 53.8 MB (53830516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60087ca3b86c3c531922fefee2703dee0af803e6d6b24379552477fc70aaac6d`  
		Last Modified: Tue, 13 May 2025 17:54:29 GMT  
		Size: 53.9 MB (53857546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160727fcff11ffa77277d331efaaec9438f3bdb8d6132519208f27344d6dc78b`  
		Last Modified: Tue, 13 May 2025 17:54:27 GMT  
		Size: 4.5 MB (4514135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c8ae12bdee755801823b7cfa03bc5f82e34f763df5e6c19c3e613d46ff7c92d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4264344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdaf582fef67fd332e00779c97570ba7f70670bc27945bc6e9129663cc63e91b`

```dockerfile
```

-	Layers:
	-	`sha256:c0fa523a368e91d1d20745959dbf116dfb6bd29e60e032d1ce6091b5df395846`  
		Last Modified: Tue, 13 May 2025 17:54:27 GMT  
		Size: 4.2 MB (4247790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf995de5686e59e29b1abf9c793b9611991381d69297f990e6c5f0804d96b6c3`  
		Last Modified: Tue, 13 May 2025 17:54:27 GMT  
		Size: 16.6 KB (16554 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:0424d8927596dd464e0e7a5cdd52a1544b097d2474b9d1c25a9afe1800e7d4b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149135169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8691d2c61cad952dfed9fa3493a4ee7f1581076f1dfd729ce3e6d5c010a44415`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:a739447e8599431e1e4996b4b6d4022822d37eddea9a3737acbea74b8a860d49`  
		Last Modified: Fri, 09 May 2025 00:17:30 GMT  
		Size: 33.6 MB (33577694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ff01908b868a75c17f94ffc5626215722b986fb8c1aeb2606b9cecf365a22f`  
		Last Modified: Tue, 13 May 2025 18:05:52 GMT  
		Size: 52.2 MB (52167960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5a04d89034e01f93f7382be056cc3bb287ca7abe1145e7e3262580a22b10ca`  
		Last Modified: Tue, 13 May 2025 18:05:52 GMT  
		Size: 58.9 MB (58875334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a06647df2f4c18ace3698b5bae8fd662a22bbf5cfe35350dfe42846a867a13f`  
		Last Modified: Tue, 13 May 2025 18:05:51 GMT  
		Size: 4.5 MB (4514149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0396c7124c50efb520e45db4f91535378db45c089413f9ca2bf9d5b205a705fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4262374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be4b4325c7f11ed63dc86dc52ebed0c370a4968875b3b724195669e0f8681d2`

```dockerfile
```

-	Layers:
	-	`sha256:278250edf2e764089ba08f9606da988b434d1d9691c63d9e395c968e7025c6a3`  
		Last Modified: Tue, 13 May 2025 18:05:50 GMT  
		Size: 4.2 MB (4245897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94f61184cfe2666a4063823a2e7abeb6e3c7729369749926ff31c95a23341ae1`  
		Last Modified: Tue, 13 May 2025 18:05:50 GMT  
		Size: 16.5 KB (16477 bytes)  
		MIME: application/vnd.in-toto+json
