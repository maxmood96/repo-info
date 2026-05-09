## `clojure:temurin-8-lein-2.12.0-bullseye`

```console
$ docker pull clojure@sha256:ab2773b2b5f80e3a47f0b6e7598e897949410a59fac33af40b4a1a80ee0933eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-lein-2.12.0-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:a80a04bcb7681f7be0a21445fd3b79dc4d58b36c40c9ca7f97c7ccaa4badaea7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130080802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54161952071409d35137e23194244f3889de96c1783c44833ec13611c78b0eb1`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:14:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:14:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:14:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:14:00 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:14:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:14:00 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:14:15 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:14:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:14:15 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:14:16 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:14:16 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a158290ef3bc83a470b5c65c567ff0bb2a6cc3c6505b6cb8d3054500e1458a1c`  
		Last Modified: Fri, 08 May 2026 20:14:35 GMT  
		Size: 55.2 MB (55170111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c718db3d991e3ef5fe522c5fcafd45c4087f3e596a0e88f79e42a30e07eade1`  
		Last Modified: Fri, 08 May 2026 20:14:34 GMT  
		Size: 16.6 MB (16629603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385cc03f9f4a3e4656f4b770e8082ed8ebcc7d0fba96ad25661d4076ac78ca23`  
		Last Modified: Fri, 08 May 2026 20:14:33 GMT  
		Size: 4.5 MB (4517713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:bf6aa0629463cc095464d0b526750bd6b022b886338c7e1bf94a3d944460fa09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4623221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a5ea138ca4181b4f98f3266e6bb60392aa841af0ca1a1b4b6e3e68a07658628`

```dockerfile
```

-	Layers:
	-	`sha256:87dc8982d4089015e1bdd7f2763f9d8ccc60d66482bf6af73b9e18bccaaa64f3`  
		Last Modified: Fri, 08 May 2026 20:14:33 GMT  
		Size: 4.6 MB (4606851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47106fa7796e013d46009f3d3650d51207e3dde977f19a210a0bf927cbe29f4f`  
		Last Modified: Fri, 08 May 2026 20:14:33 GMT  
		Size: 16.4 KB (16370 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-lein-2.12.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:898c65ebf71e9287c5f0fa9c50a5895c2e0b39e8d4330c3dac1bf8c4305adf0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.6 MB (127639166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d56889c9501d62bff914692c8e526d6b8ba392f1d3b2c526a70ff96601ac95`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 20:18:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:18:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:18:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:18:34 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 08 May 2026 20:18:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 08 May 2026 20:18:34 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:18:47 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 08 May 2026 20:18:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 08 May 2026 20:18:47 GMT
ENV LEIN_ROOT=1
# Fri, 08 May 2026 20:18:49 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 08 May 2026 20:18:49 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12b6a467874998b3612540bb45c100aae35859e4af5e3a1e3a16ae05257de53`  
		Last Modified: Fri, 08 May 2026 20:19:07 GMT  
		Size: 54.3 MB (54251616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56451a2b7c290353d4218a7b6db021d5e74645ca89ae87509ca3dfb535ae7af1`  
		Last Modified: Fri, 08 May 2026 20:19:02 GMT  
		Size: 16.6 MB (16616549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b67bea7e11c05550881ffa2b7764acc37dcbe78e9352386b9319aa51ad509ae`  
		Last Modified: Fri, 08 May 2026 20:19:01 GMT  
		Size: 4.5 MB (4517759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-lein-2.12.0-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:4e43f9edc9c9fdb1a57d9fc1ebd3532a256bc2a7217a7bd5b2a5c7a700c6cd53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4623016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8920227043d3a3d82920b78daadb52f793298cf7d955aede93a79e1486237025`

```dockerfile
```

-	Layers:
	-	`sha256:7fb380f5fd79a848e23996d2ce89cd1be0b4f2757279205964d9d3fe0a51e0f6`  
		Last Modified: Fri, 08 May 2026 20:19:01 GMT  
		Size: 4.6 MB (4606525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df0c8b6a8bf27462475e6b792fd9623725882353d8eba73b84c19d273f185145`  
		Last Modified: Fri, 08 May 2026 20:19:01 GMT  
		Size: 16.5 KB (16491 bytes)  
		MIME: application/vnd.in-toto+json
