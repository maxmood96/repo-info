## `clojure:temurin-11-lein-2.11.2-bookworm`

```console
$ docker pull clojure@sha256:9a9a69714939d0cb5382e71c285468a035076ddd193340d01748490d96784bc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-lein-2.11.2-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:f8ca7eeee35ca07ec5a186d29b5cd278eb28b7ea76a5aabc38cd508cb2f85b68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.3 MB (261321753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47292b844b90dc10d2d18ba5958313f16e2a5f8c2cb405d4a9169418cd4ca3d2`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
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
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_ROOT=1
# Wed, 07 Aug 2024 18:04:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4324cd2542e01b3ce9fbd0cffe0e9ceb5958f8dd9115fd8630f269a4a64bdf5a`  
		Last Modified: Wed, 04 Sep 2024 23:07:44 GMT  
		Size: 145.6 MB (145550068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e85a4c88188ac0abf4bc1a11204dcc3e6cc724a93e5128fdb77ddf82b51638`  
		Last Modified: Wed, 04 Sep 2024 23:07:43 GMT  
		Size: 61.8 MB (61816913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9003b52cc3424a99dc8885ee33ff7ce999b960a98b157f0d56d72e532c34a604`  
		Last Modified: Wed, 04 Sep 2024 23:07:42 GMT  
		Size: 4.4 MB (4398038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.11.2-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:993da6df5a326e2778301cf5a8d8991226952be107655e7a4a234dcc48f2576d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6378443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82076da3f6f62c42e5e96484a891b5da88e829d2de94e6b491a35c2d847196d7`

```dockerfile
```

-	Layers:
	-	`sha256:282a6d48d9ee7b237de2fe30122e7fbab55f90472aeade6c256bf7d316539706`  
		Last Modified: Wed, 04 Sep 2024 23:07:42 GMT  
		Size: 6.4 MB (6362398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f028d0d86140aa3c1117bfa39247371e884ba7b6857b1cad674fd79995665a0c`  
		Last Modified: Wed, 04 Sep 2024 23:07:42 GMT  
		Size: 16.0 KB (16045 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-lein-2.11.2-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:20f6378001106ce404c14044da2658f816920cb580582184427eb9ff464c2c32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 MB (258015872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b4d0e96b61ca225f6ac92c2f568c1fb94055695ae2555e4469e61a674471a8b`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:e81dd8b32e45ea6e761021a3e01b6efd339dd9248a2036dc4b51a2c1de560b4c in / 
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
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 07 Aug 2024 18:04:12 GMT
ENV LEIN_ROOT=1
# Wed, 07 Aug 2024 18:04:12 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:7b24851aa36de07cd94173b8e2052846573dacc3b241620d713254e647352394`  
		Last Modified: Tue, 13 Aug 2024 00:42:24 GMT  
		Size: 49.6 MB (49588592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c7e107b4736e704c136824cd4b625750da0fdc9e8e5ad885340c116db3e802`  
		Last Modified: Sat, 17 Aug 2024 06:01:13 GMT  
		Size: 142.4 MB (142354796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84607c60dc13faca0826c669353f4c9b0ceddc10e274e8fb512f0874a40e535e`  
		Last Modified: Sat, 17 Aug 2024 06:01:11 GMT  
		Size: 61.7 MB (61674421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afb06021b18dfdddc5e70a9a3a4888857bb589973059ed80424762a8fb6c974`  
		Last Modified: Sat, 17 Aug 2024 06:01:10 GMT  
		Size: 4.4 MB (4398031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-lein-2.11.2-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:178d816c5e55d1feaae5947ae2eccbabac7281196a2086f4057e4588fab1f28f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6385900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e3930ae7f7f18ce8c2f0ab6d5fd9a4ee1b842c21342e1b3f8164a3451e6b34`

```dockerfile
```

-	Layers:
	-	`sha256:9ecfd8e4737b4a5158427ec4693a263f88780b22a84463fff2f158281ab4b473`  
		Last Modified: Fri, 23 Aug 2024 23:50:18 GMT  
		Size: 6.4 MB (6369331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f729f75f952c62449fb9253e7a5d2f19cdb27cd4442202dcbca074d1c708dd7a`  
		Last Modified: Fri, 23 Aug 2024 23:50:17 GMT  
		Size: 16.6 KB (16569 bytes)  
		MIME: application/vnd.in-toto+json
