## `clojure:temurin-8-lein-2.12.0-bullseye-slim`

```console
$ docker pull clojure@sha256:2d789a7a821746c95c109634caf6d2deb0924f7939df1a8e349d0126b9d9896d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-lein-2.12.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0e71a22a8971422b60a3d6dde35b9b98669b2a0ea0782808ea1475f99fc8cecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105284598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a98c55af4dc7c2c23acc7e6a445d9efeb5334990e5249374828e5806e5a7f1`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:14:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:14:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:14:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:14:15 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:14:15 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:14:16 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:14:28 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:14:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:14:28 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:14:30 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:14:30 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:77e30ef52aeb52d8466baf0f50b54ed2fc0b421f44c49e5bf93682b27110f4d3`  
		Last Modified: Fri, 08 May 2026 18:22:59 GMT  
		Size: 30.3 MB (30257958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b614afc9007820be825a05347a260eda9fb44ef2bc91dd9c14a9e0ccfbd2a9`  
		Last Modified: Fri, 08 May 2026 20:14:44 GMT  
		Size: 55.2 MB (55170060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67b845e3919da297a7ff57fe0017ac3de86d0b1541181b0cb9e066817cc5004`  
		Last Modified: Fri, 08 May 2026 20:14:43 GMT  
		Size: 15.3 MB (15338784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cf33db515144609d3cc840ea26f4b0410541ad3a2fca81acb43da92ec18d88f`  
		Last Modified: Fri, 08 May 2026 20:14:43 GMT  
		Size: 4.5 MB (4517764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d247ed56c06dbc7c8a4be364cf76b61856e1be1146d0818a9247bd4d233f6c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3164971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4fbffec1df812ea8d2a981ed6daa81d45e4ce295ae7d88265da2ab11fa6a62`

```dockerfile
```

-	Layers:
	-	`sha256:cedb5ed67edaa30991ee8ea27a06d2974efd862afcd1081811908433a1cb6bf0`  
		Last Modified: Fri, 08 May 2026 20:14:43 GMT  
		Size: 3.1 MB (3148571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c45a6a0c621798e4dcbb040262bc05f6f50df08a6ecfdec4f2ae8e7e057bc6cc`  
		Last Modified: Fri, 08 May 2026 20:14:42 GMT  
		Size: 16.4 KB (16400 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c61cb87a4940c4395b7f661607978862b517620a4d4323cb8123dde84fc123f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102839233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c25710ae374ad6a47e6df0dcc374afd24324559825161938955e003ecae7aa8`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:18:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:18:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:18:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:18:50 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:18:50 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:18:50 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:19:03 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:19:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:19:03 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:19:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:19:05 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ab0f13d792ff9100407906fb422a0b62a8b437abde4c245e03f0366814be9aae`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 28.7 MB (28742591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d94e3c1d23bb3d21380f000557c242b8faa2676d5226c0234d92fa4e541b440`  
		Last Modified: Fri, 08 May 2026 20:19:19 GMT  
		Size: 54.3 MB (54251613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d3caeaf2fbee585105747205b43a8d119c8f2c5cfd6f47cf8eda1e8bcebe76`  
		Last Modified: Fri, 08 May 2026 20:19:18 GMT  
		Size: 15.3 MB (15327236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67fa9af394b5b6505ef3ee8f98aa046b0f754066ee9029707cbad0f9e1e732d1`  
		Last Modified: Fri, 08 May 2026 20:19:18 GMT  
		Size: 4.5 MB (4517761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:12f547012632a53ba54080f569906241bfe2d8fdfe42fe25fc719c517296c71a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3165400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa4bc01cc8b335a8b3f3e1326e927c4874fe6dea8628f7c14a988b113844f8e`

```dockerfile
```

-	Layers:
	-	`sha256:3d416332937128173a780cc3b74da237ac1c5ba1daddf36890adb822c655c953`  
		Last Modified: Fri, 08 May 2026 20:19:17 GMT  
		Size: 3.1 MB (3148880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9255edd151eeb9cfb223c9f4f97dc19675271a5cca46d386c85a7ba1cca7b797`  
		Last Modified: Fri, 08 May 2026 20:19:17 GMT  
		Size: 16.5 KB (16520 bytes)  
		MIME: application/vnd.in-toto+json
