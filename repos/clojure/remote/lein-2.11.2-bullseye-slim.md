## `clojure:lein-2.11.2-bullseye-slim`

```console
$ docker pull clojure@sha256:a25bc4db112c609837bd33c7e32d7b1b68003434105c5f91f67a1c8860171cd0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:lein-2.11.2-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0792b13eb50788d4ebd40a0cdc5ab28fc4fef3eea0b5881e82c961bc0ba9cddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235682034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6510215ca6a6821408bd03b162ad06696b26dfe24ea5778c791837bdbb8a1c5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
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
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb8ccb55ebd9389eaa4c26834df31ebe31e3454bd6ff483bbf9d05cc2dda59a`  
		Last Modified: Mon, 28 Apr 2025 22:08:06 GMT  
		Size: 157.6 MB (157634520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd13bb6517a593286825e59398def0f660729914f747eeb3b660b636c621244`  
		Last Modified: Mon, 28 Apr 2025 22:08:04 GMT  
		Size: 43.3 MB (43278319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01f8efcd5ca3b804f1edaa76ad624ca51cecc9e18c157e363e21c1e0e214f45`  
		Last Modified: Mon, 28 Apr 2025 22:08:04 GMT  
		Size: 4.5 MB (4514163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83879f2829a30f9929dc20ec8fdf6cebee50d6b38068cd19ab28af0081d47dc8`  
		Last Modified: Mon, 28 Apr 2025 22:08:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.11.2-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:519e5aa869bccdc0d98c4aecb41f10742f114af236b8d049b61da3b5462a212d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4593053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5146b9e9718e2bc9d355d299b7ba98cc1843ea3e8fab508519f57aa1ec3e17c`

```dockerfile
```

-	Layers:
	-	`sha256:13a462e94a036a8e5e84e4c4d5e40e3dbe4adc1dea5710c7e8e7936b1c528472`  
		Last Modified: Mon, 28 Apr 2025 22:08:04 GMT  
		Size: 4.6 MB (4573933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecb48ee6ae278191329f39882f6e9b0bd0dcb19d0536a56817022143f32c29f8`  
		Last Modified: Mon, 28 Apr 2025 22:08:04 GMT  
		Size: 19.1 KB (19120 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:lein-2.11.2-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8e7e5fda778c9ec666fff22e4dbc68bc866ee6cf5c399fbd5dc3a9334fc096f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.5 MB (232502221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e17c3fe05752135058ca8527e90c74b61d139bd5badc017e5f2115afa388bc0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
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
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb91d4429e152a4ef12cdda1f1c22c8aa83ef90eec350facd6ba0b74134ad97f`  
		Last Modified: Wed, 30 Apr 2025 01:47:24 GMT  
		Size: 155.9 MB (155928805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5991ae6f75af6017bd57020f5a1bd421fe71aad9f473bbb3d1a68e98a4d6b8`  
		Last Modified: Wed, 30 Apr 2025 04:49:17 GMT  
		Size: 43.3 MB (43314202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406b99687a11d3065a3b7a407ce05d2fd6e6f7ebaabb3f7f1445c47dde60b644`  
		Last Modified: Wed, 30 Apr 2025 04:49:16 GMT  
		Size: 4.5 MB (4514140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefc80613e97d93c56311677a15af0897bb02b05ff6036d86e2375664214a1ad`  
		Last Modified: Wed, 30 Apr 2025 04:49:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:lein-2.11.2-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5c033ccd069905090b3d0868ae43117540670336386bf6b2f2028a04627f472d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4598885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af4295783c3c800dab486c9ac4711ceed01fa407ae04357b3aa05c2bb980d8e`

```dockerfile
```

-	Layers:
	-	`sha256:006679ece18eae399f8d3ac7cad96a75fb05a4f36c4d4fc53b282761f9b42436`  
		Last Modified: Wed, 30 Apr 2025 04:49:16 GMT  
		Size: 4.6 MB (4579621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b38fa32237da347edeca9cfb0f816ce47710fddfbbd41b95a5b4494b8e5c63ef`  
		Last Modified: Wed, 30 Apr 2025 04:49:15 GMT  
		Size: 19.3 KB (19264 bytes)  
		MIME: application/vnd.in-toto+json
