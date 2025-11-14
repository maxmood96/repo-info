## `clojure:temurin-17-lein-bullseye`

```console
$ docker pull clojure@sha256:5365db7fe00555ac3166680d81fc88eb9d61b0e176763b4e8a2336b8f61c2db4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1dbc7f7cb56eb4d6111c41cb7564c982594285b66c605cd8d7d666b8330fe431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.7 MB (219730424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ba8b70e984f56561e26a8bca7b9880e95601943a16674e590b9914f3c1569b2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Fri, 14 Nov 2025 00:52:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:52:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:52:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:52:17 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:52:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:52:17 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:52:30 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:52:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:52:30 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:52:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:52:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:52:32 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:52:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd55f1a6dea1f2e8ad20773875480a0fdec039342cc6a3dd1d8b2ad6dc9ecf1`  
		Last Modified: Fri, 14 Nov 2025 03:29:46 GMT  
		Size: 144.8 MB (144847948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7014e84af568fbeae9c231e5e9f242f786ab432546879d22034a8557191a04`  
		Last Modified: Fri, 14 Nov 2025 00:53:00 GMT  
		Size: 16.6 MB (16607599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ebafd775a5e73e6c1209d5f67a6766c06086aff5bfe3a17b5dd21d90601ce3`  
		Last Modified: Fri, 14 Nov 2025 00:53:00 GMT  
		Size: 4.5 MB (4517753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c870782169dc51f9c0cbd55c1e07b78aed4c78c96c590e11913f37780740f7f1`  
		Last Modified: Fri, 14 Nov 2025 00:52:59 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:48313c8129ac5ee3d2d55cdc420eb30b435ce2a5aa73aabe05b0641096473025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4494557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d47b3b2cb7307f8e98f9ba6deecd05a573b06200f89cc5410754475eb34f6fa9`

```dockerfile
```

-	Layers:
	-	`sha256:38b69471161f1103926af297d8b45016f4d34621b4934a2476ab79d83a1dcf35`  
		Last Modified: Fri, 14 Nov 2025 01:40:02 GMT  
		Size: 4.5 MB (4476190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71329379dbb74ce14969a8d091a90a4972fb670c4cda1e7384a9d95f0673cf55`  
		Last Modified: Fri, 14 Nov 2025 01:40:03 GMT  
		Size: 18.4 KB (18367 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fb06f76acc01bfb711448f2ddb64564b74ae9a00780833331d3c49b020ec3c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.1 MB (217051074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041057c2a87ab105e5d7a20baccfee0297083c7e6145f61ef4edb472c6871bab`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Fri, 14 Nov 2025 00:54:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:54:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:54:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:54:02 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:54:02 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:54:02 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:54:15 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:54:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:54:15 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:54:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:54:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:54:17 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:54:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1914285197fb8156f3f7b990673fc1082412802e2b9348e1ec55800a26156a18`  
		Last Modified: Fri, 14 Nov 2025 00:54:38 GMT  
		Size: 143.7 MB (143679914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d012f27a879a969b97a2b25cbf60faa501b0c03fb222dcb0d32909f0e20fc31a`  
		Last Modified: Fri, 14 Nov 2025 00:54:43 GMT  
		Size: 16.6 MB (16595022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da688351f0bdd35019f63b37cd4b6f044e7a66a98cd545d758c5a4a1ed1d9065`  
		Last Modified: Fri, 14 Nov 2025 00:54:44 GMT  
		Size: 4.5 MB (4517741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38d6feaf3c9fb9affa8aeb0b9c8df5831c4d9b209c5321fd002e1a72752c1f7`  
		Last Modified: Fri, 14 Nov 2025 00:54:42 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a5bc8e664f86808cef9882122bacb64a2d9f84931ee328f2a1142879770903ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4493653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8960164c131dd750836bccebe0b28d13d9933fcda380c96e24ec9e9740f8717`

```dockerfile
```

-	Layers:
	-	`sha256:2b62fead5fa5f58348b70eeebac61dc19bd1529199ff86ff538bbf6ae3a38475`  
		Last Modified: Fri, 14 Nov 2025 01:40:08 GMT  
		Size: 4.5 MB (4475164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:965a879396fe370977f7c2aaeba993dd6d9bf11418f0bcdcd6a2091ce740c29b`  
		Last Modified: Fri, 14 Nov 2025 01:40:09 GMT  
		Size: 18.5 KB (18489 bytes)  
		MIME: application/vnd.in-toto+json
