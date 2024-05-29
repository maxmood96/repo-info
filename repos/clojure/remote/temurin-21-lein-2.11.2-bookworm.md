## `clojure:temurin-21-lein-2.11.2-bookworm`

```console
$ docker pull clojure@sha256:7fbc12527b2d9a16a3355767db25ef0f7ee4060eceb0184ae0d92480ec665ec3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `clojure:temurin-21-lein-2.11.2-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:36010443afdda983a0ac6aca806b8d2b1929ce5dd4b6e24b390bbdde198616a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.8 MB (231794228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72066c8c9c23779203108fefbb197a69e4c85d3b7aae08f54ef97cf856c96d02`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf0a1d80f0581b1ab77de62dd18bb0ed981175dc08bdd952a8eb5c7f01ebc1c`  
		Last Modified: Wed, 29 May 2024 19:57:14 GMT  
		Size: 158.5 MB (158497942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a7f5b86f69da64d9152463f257a1308d882fde1b3d55608f781ec410b23d0e`  
		Last Modified: Wed, 29 May 2024 19:57:12 GMT  
		Size: 19.3 MB (19321431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7fc6e7abaf2199b5f30f8f8392b3787b0ea712b4d82cf786264ed80bec6fc1`  
		Last Modified: Wed, 29 May 2024 19:57:12 GMT  
		Size: 4.4 MB (4398033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059705f667555ad2990c68041b60af6ebd75eb9f1f656f88912a488d17ab0665`  
		Last Modified: Wed, 29 May 2024 19:57:12 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.11.2-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4ffd7ccb24c56190b40cd3dea076d264096d039bab1154b67f5e6cdb1c1f0da7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3970452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffffc67534092d6ba164d4c277cbbe43519759e18a41ba86abc0da2deeb8e66f`

```dockerfile
```

-	Layers:
	-	`sha256:27c4aff246b19a3078dec7949b5015897cf667bc9a499a16944937bd83b319a1`  
		Last Modified: Wed, 29 May 2024 19:57:12 GMT  
		Size: 4.0 MB (3950574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4042bc39b9a0691511ca0b9c74895afb751eacf54dee28d288987f0d0ba2bb87`  
		Last Modified: Wed, 29 May 2024 19:57:12 GMT  
		Size: 19.9 KB (19878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.11.2-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:78081fcd3babc09ec1a1117c207c6b7d422020498a22a131e6fe0c0bdf7f6b07
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 MB (230017110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:757d4f1348bd178953925b3ec7371ae93f401ac28532868e328a076c1615b831`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:32 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Tue, 14 May 2024 00:39:33 GMT
CMD ["bash"]
# Tue, 28 May 2024 19:43:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 19:43:16 GMT
COPY dir:96a90c8e1c03defb238a6d560d8927dc81a1a58af3fce1471cbce5249ed27f38 in /opt/java/openjdk 
# Tue, 28 May 2024 19:43:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 19:43:20 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 28 May 2024 19:43:20 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 28 May 2024 19:43:20 GMT
WORKDIR /tmp
# Tue, 28 May 2024 19:43:36 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 28 May 2024 19:43:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 28 May 2024 19:43:36 GMT
ENV LEIN_ROOT=1
# Tue, 28 May 2024 19:43:38 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj
# Tue, 28 May 2024 19:58:35 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Tue, 28 May 2024 19:58:35 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 19:58:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876b5a53959bd941f43a1015323f50ba6e3858b9a2fb1453a7b61f9d4dd305dd`  
		Last Modified: Tue, 28 May 2024 20:07:28 GMT  
		Size: 156.7 MB (156665559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb676fa21d846602bc80463b426186d8cdd53f2f3622d52d187e9806378491ac`  
		Last Modified: Tue, 28 May 2024 20:07:18 GMT  
		Size: 19.3 MB (19339625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc5e9e443c37646b869479d4527989b27e71a4242c4ea7fcac30733865f4878`  
		Last Modified: Tue, 28 May 2024 20:07:17 GMT  
		Size: 4.4 MB (4398142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08623e751846f0708315900ae2128df9ed8af530d8e66aef91bd3b8f530d75e8`  
		Last Modified: Tue, 28 May 2024 20:17:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
