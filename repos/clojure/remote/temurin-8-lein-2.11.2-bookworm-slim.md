## `clojure:temurin-8-lein-2.11.2-bookworm-slim`

```console
$ docker pull clojure@sha256:cfa46b81ed4f64c675c1f3796f12c84abe5c977dd2e9add2f1fe7a9c3878427d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-lein-2.11.2-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:23c91606c980363a41ec7981920a8c944b5d83eab923b02b611a6ec0537b3248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.9 MB (138915181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad559c6d68c61e3a4876e11f2633ffd39daa122022dba49c248257bb2829c4a7`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 29 Jan 2025 19:11:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 29 Jan 2025 19:11:46 GMT
ENV LEIN_ROOT=1
# Wed, 29 Jan 2025 19:11:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c33faa9bea88c46d23500b46eaf18e9b6b136e36c1b4b2a542bd267e96be7c`  
		Last Modified: Fri, 31 Jan 2025 02:13:46 GMT  
		Size: 54.7 MB (54721258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900fe2257760ebcc60dedf3cb02128b3ced9580397bdd413e38462e02f2db609`  
		Last Modified: Fri, 31 Jan 2025 02:13:45 GMT  
		Size: 51.5 MB (51467265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2567a6ba793a6b23ede8d84bb622365ccf7fea4ac16dd37dd420960adc68b947`  
		Last Modified: Fri, 31 Jan 2025 02:13:45 GMT  
		Size: 4.5 MB (4514209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.11.2-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ab70b58dcef6eadd544c353f2de2e45bf00a4bab3b139f33ad07ee2692e23320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4458489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5358ff117426045b3af81ac42ab6bc730b2624b9b5974cf60e95a10e7de1f74b`

```dockerfile
```

-	Layers:
	-	`sha256:dcf57706879b5687a3084851f711368ca6aea1ca24ce715c56b07f9bc1179817`  
		Last Modified: Fri, 31 Jan 2025 02:13:45 GMT  
		Size: 4.4 MB (4442039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94c9fd9c452d4909a24721a859b22eebbb86192510333a59fabd05338f2ea31b`  
		Last Modified: Fri, 31 Jan 2025 02:13:45 GMT  
		Size: 16.4 KB (16450 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.11.2-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:275ff31fd6d149ef61989d343904d774c76aac6f39cf227d6203a314bc7981f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.8 MB (137808124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff782ffa69ca1d33ce385c16ec8ff6f6bdf614651bad0d624c664e8c13b05ca`
-	Default Command: `["lein","repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 29 Jan 2025 19:11:46 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 29 Jan 2025 19:11:46 GMT
ENV LEIN_ROOT=1
# Wed, 29 Jan 2025 19:11:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df06cce5db22c11379358b8770d8e45c7b8def7c35a6910da2a498720c17d0f6`  
		Last Modified: Fri, 31 Jan 2025 04:52:25 GMT  
		Size: 53.8 MB (53822735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af543648c1793cc477c873892ea1c43dcca81a8084f93cfd11cd12d39c043216`  
		Last Modified: Fri, 31 Jan 2025 04:52:25 GMT  
		Size: 51.4 MB (51430170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68de94c6f6c5cfe733c807bb52527494e325bc10b1e02dddf4d1b74c368b4912`  
		Last Modified: Fri, 31 Jan 2025 04:52:24 GMT  
		Size: 4.5 MB (4514156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.11.2-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9421c1318bcc2fbd4af98c62d0e194abfed9af4f0d71a5d8992880a0fc197a7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4465001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7560d3cf906194123a9929f8a7d612e7777d608da06b069bccc4bca2159342c4`

```dockerfile
```

-	Layers:
	-	`sha256:8e68e0b6182cf5c5410cfe184f45c6e70fe9b68968855710e106a1fb07642fa3`  
		Last Modified: Fri, 31 Jan 2025 04:52:24 GMT  
		Size: 4.4 MB (4448429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02f461a50a54e42b1b10082ae50c028e79e75137fd0d10760ba531d9295a8a6f`  
		Last Modified: Fri, 31 Jan 2025 04:52:24 GMT  
		Size: 16.6 KB (16572 bytes)  
		MIME: application/vnd.in-toto+json
