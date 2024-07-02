## `clojure:temurin-8-lein-bullseye`

```console
$ docker pull clojure@sha256:c00be5a973238b664aa672b626b420f9391f11dc343eab827302d5d36f39c7a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:ab45e740ddb424032ee8648964c92858f52582a642ced484952ea1ee9502d958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.4 MB (179431337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c08e22ed90c7584c4648768f980c8f034019a183d532fe214d56f41136b1d134`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_ROOT=1
# Tue, 28 May 2024 15:17:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05dedf89ef64d0942ee8834958530db343401f9c6345de96d9637144d4e253aa`  
		Last Modified: Tue, 02 Jul 2024 03:02:44 GMT  
		Size: 103.6 MB (103600204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795502a330a12fdf703f7f0d3958e0ffc87abc63f073d711c438ac452b572841`  
		Last Modified: Tue, 02 Jul 2024 03:02:43 GMT  
		Size: 16.4 MB (16351705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eec36db70c96d2da276cc5780988482b950b4f2d568e163205c63fb55bedb63`  
		Last Modified: Tue, 02 Jul 2024 03:02:43 GMT  
		Size: 4.4 MB (4398036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e3ed5093c10e484e75464f0c41532b589f9e354d6cd85da6c4390e0d30a8d6b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4189829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b594a2cea30ad58c8061424c4d36c3f3313da786a8751fe4b7227f8817d25d7`

```dockerfile
```

-	Layers:
	-	`sha256:361e0dbf9bea5447523296063a524549dd92b0773027ca98477b6ccaf50f2ef2`  
		Last Modified: Tue, 02 Jul 2024 03:02:43 GMT  
		Size: 4.2 MB (4173802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6eaac3c1e0b1eb0f02b12f0d46178a167de30e18ebe8b81c1ba93776cb242699`  
		Last Modified: Tue, 02 Jul 2024 03:02:43 GMT  
		Size: 16.0 KB (16027 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1bd2f47d21a1db86e29d125ab1afb988d08e7a264b70886293b6af436b268a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (176974604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c54b6c6fc76806269bac22d18e704f2fd31e87a5a2c91266dbf48c872b04af`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:cd3edc79f93d09aa5daffba99cc698c3fe0e02348e8dc284ef466b7e6596e68c in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_ROOT=1
# Tue, 28 May 2024 15:17:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:f975e52008de385eb513258b4912477b214cddf1c8e87877f85028d940bfcdae`  
		Last Modified: Thu, 13 Jun 2024 00:43:32 GMT  
		Size: 53.7 MB (53739581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63aa4caacc3a1e1326d77d86134d7ff7c6a2d2448547ed3ea79282943e9bf562`  
		Last Modified: Thu, 13 Jun 2024 11:22:13 GMT  
		Size: 102.7 MB (102700428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8bedc11dbc379233f2284f9d3cf637b1b97daca5c2fff8099fc23aedbd0f85`  
		Last Modified: Thu, 13 Jun 2024 11:22:11 GMT  
		Size: 16.1 MB (16136481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f1e01c33ce5ff32d13b3a0f34c950bb48a58928d3d1d35cf51e37312cd19c3`  
		Last Modified: Thu, 13 Jun 2024 11:22:11 GMT  
		Size: 4.4 MB (4398082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:6575d00d8267baf190751b11fbef1bf13abca7dad474fda4a2c7fc975960eb98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4189936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a5f55d255351aab7502d84065b1e9f7a435d31fcd9b1512183405120248761`

```dockerfile
```

-	Layers:
	-	`sha256:bea0b3ce4f0f70d92cf7e6cec4531ad50e08fcd0b20a4209775884b5f064a180`  
		Last Modified: Thu, 13 Jun 2024 11:22:11 GMT  
		Size: 4.2 MB (4173389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d0d4bc16424085afcbf53316be1192ed1d722d3c60eec73353322abda972d56`  
		Last Modified: Thu, 13 Jun 2024 11:22:10 GMT  
		Size: 16.5 KB (16547 bytes)  
		MIME: application/vnd.in-toto+json
