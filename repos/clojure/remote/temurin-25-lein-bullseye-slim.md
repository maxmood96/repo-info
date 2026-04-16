## `clojure:temurin-25-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:f7a0df8f01df496654e7f9d8e22bdb2809de9b52acec96852693e267e7c6035e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a556b1218c7ba8fe619f34a3b6a801fe3eba8b1bad49bd74f8e621d379257995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142371260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b1199fb94436cf971d8eadc5041f5082f796aca2298d3c0c99be64e09ec6d2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:06:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:06:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:06:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:06:16 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:06:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:06:16 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:06:31 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:06:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:06:31 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:06:32 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:06:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:06:32 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:06:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30a4bd162b1146e9afdcd2ff28c821f0f3e82bec4199a386d433a1f436d35a1`  
		Last Modified: Wed, 15 Apr 2026 22:06:51 GMT  
		Size: 92.3 MB (92256316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841c3b227dcdbccee83e558a949705614981652cbd70dd06d939f6823210b74f`  
		Last Modified: Wed, 15 Apr 2026 22:06:49 GMT  
		Size: 15.3 MB (15338782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47acdb682be6d803a9383aeb8b8e4e02505b8cde8d32e365d8b5d28c7a959661`  
		Last Modified: Wed, 15 Apr 2026 22:06:49 GMT  
		Size: 4.5 MB (4517715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed408a68361a0d14068338ae35354fb87567e991abd893ac7817b16b8611ff1c`  
		Last Modified: Wed, 15 Apr 2026 22:06:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8ceff25744d861d5c50acddbc65108a5db8a22e5520956cdac44ef6784629400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f897986a0355943197f347dd31c5e668f371ae49f178c568ed998397fd4b03ca`

```dockerfile
```

-	Layers:
	-	`sha256:a7c7baf857404260529854258b93020121f6c23c8874d05d9a406ec19a56307d`  
		Last Modified: Wed, 15 Apr 2026 22:06:48 GMT  
		Size: 3.0 MB (2995642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1fd91595402f024c074df827dcc16244f6c87e1ec4d223966eb25cce28c424eb`  
		Last Modified: Wed, 15 Apr 2026 22:06:48 GMT  
		Size: 19.1 KB (19058 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:165a4fddba4f2e50b7267088c8d61faffabdf642b11a3927b4b1bbcc2b574ee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139878334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910eae00a89aaa43b0cbeb6bd39053f8402467a9114eec7f28d85d8bb28bd8f3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:17:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:17:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:17:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:17:48 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:17:48 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:17:48 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:18:01 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:18:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:18:01 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:18:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:18:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:18:03 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:18:03 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a9a01c563ffc65cc1f7d0bcc73e776c4b3e530e99cc6ad7b0d8a89ec978665`  
		Last Modified: Wed, 15 Apr 2026 22:18:23 GMT  
		Size: 91.3 MB (91288275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e539b16593248f3a605a92828a05795a7189b2162035a5c9198b1a704b1d02`  
		Last Modified: Wed, 15 Apr 2026 22:18:21 GMT  
		Size: 15.3 MB (15327205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e959e58691a846643f16f963e198675b9df7cc6593b810c68c28d3eb8f1c701`  
		Last Modified: Wed, 15 Apr 2026 22:18:20 GMT  
		Size: 4.5 MB (4517738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0013c6530f7be2722746c9e31cff263620eb391b18094cae2b11b0e07064267`  
		Last Modified: Wed, 15 Apr 2026 22:18:20 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4b91418369e9adeec52b6910ad31f7c1b1f61911e94146ed414fae107af1d818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3014475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637d04745baae8165ecd5611fac47a351b1045f36178adab228efabc5de0d6ca`

```dockerfile
```

-	Layers:
	-	`sha256:43db3fd27fc8f5d383e97bd918c3c3ed557b1e551ff5515b6fde401ac6c3847f`  
		Last Modified: Wed, 15 Apr 2026 22:18:20 GMT  
		Size: 3.0 MB (2995272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e179e048e2265f74587b1fd33999c5b99e467679a6e0f8579358dfbe739d75a`  
		Last Modified: Wed, 15 Apr 2026 22:18:20 GMT  
		Size: 19.2 KB (19203 bytes)  
		MIME: application/vnd.in-toto+json
