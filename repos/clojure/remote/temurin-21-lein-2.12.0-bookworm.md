## `clojure:temurin-21-lein-2.12.0-bookworm`

```console
$ docker pull clojure@sha256:448d440ae6dc149136d1d4f36aaf463d3e1a884c2a058a0efc58ab50d4b671dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-lein-2.12.0-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:4f37b214680aa713f6fc9192ed7f4db0114c5595c0bf83792d12f92bc64177c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230628335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d21a92a4bc8359aa7ad2de39e6e0fb87857a33851cdf0e14e7534e6926f3344`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 01:57:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:57:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:57:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:57:04 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 01:57:04 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 01:57:04 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:57:18 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 01:57:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 01:57:18 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 01:57:20 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 01:57:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 01:57:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 01:57:20 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c1be109a62df95316ceac87ea501079f32e17f36b636865a860841b7db06100c`  
		Last Modified: Tue, 13 Jan 2026 00:41:15 GMT  
		Size: 48.5 MB (48481622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03612d5d3d57084277be48f9ee41b6d30905d39bcd12557bf3db215e0fb492bc`  
		Last Modified: Fri, 16 Jan 2026 01:57:45 GMT  
		Size: 157.8 MB (157826055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf53cad2f05b7e7cbb095eb934dafa346ddd25d857d9e80766af04349219ef9`  
		Last Modified: Fri, 16 Jan 2026 01:57:53 GMT  
		Size: 19.8 MB (19802476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5a9148b2bb18770db485f2ce8211c146aa000afff5687c26f889cc9ce88c9f`  
		Last Modified: Fri, 16 Jan 2026 01:57:42 GMT  
		Size: 4.5 MB (4517754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf6ed9eea387c9a8a5490d11f0ff0d709a0b0c56098d4908817667dd05f30bb`  
		Last Modified: Fri, 16 Jan 2026 01:57:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8f98f2501d3b15730b66d336e533daacbe6a009365d268d9ebb7945025d8e5c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4303249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c74a59d91e526b287f5a658b03acb0a568c3b09e5daac61726e5ef59216f40`

```dockerfile
```

-	Layers:
	-	`sha256:0bfc7b57d94781a6fde272f1f8ecd1d2af7c3688d345060e419e2cf265def5fe`  
		Last Modified: Fri, 16 Jan 2026 04:45:55 GMT  
		Size: 4.3 MB (4284231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:436f876372894b2fe25926920b46755d411dd0fe9cb7e58ddadc59705ef3d531`  
		Last Modified: Fri, 16 Jan 2026 01:57:41 GMT  
		Size: 19.0 KB (19018 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cc734975a831cdd050f6475df163261b72fd69ece3584fdc9fef708a8559ed89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.6 MB (228624594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18791ab7d39273da50e7111322b68c2258a54512dae3116118f496819823487e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 02:01:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:01:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:01:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:01:16 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 02:01:16 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 02:01:16 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:01:29 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 02:01:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 02:01:29 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 02:01:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 02:01:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 02:01:31 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 02:01:31 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c028b7070606cb054395e1ad6c32b2961c7382d8aa2995ad84d00e44d30edf4d`  
		Last Modified: Fri, 16 Jan 2026 02:01:54 GMT  
		Size: 156.1 MB (156107636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f329e919a6f52eec13d44a2bd9c189c33a44465fbef53e4b8aa999c95f58a9ec`  
		Last Modified: Fri, 16 Jan 2026 02:01:51 GMT  
		Size: 19.6 MB (19632756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e69ef213159dbcb3f59d2d03d3b053379a34f2dc2edd694b275187fe1ae257`  
		Last Modified: Fri, 16 Jan 2026 02:01:51 GMT  
		Size: 4.5 MB (4517702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc5f91ce7fd4d55579d47995b9f18f67f7e8682f5d16896f779129feb95b55b`  
		Last Modified: Fri, 16 Jan 2026 02:01:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9df95ba5b18ac70d2e15151e73dc63cf9a3d466836aa7ec3ccd19902910432bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4303032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51d8b220e064c94bf3d32634c185bf3c94c52abd0954ff18a661557347a8c654`

```dockerfile
```

-	Layers:
	-	`sha256:cb70eae793482361f89abc2a226a58c5d33f3991f30279e044437b6b1e0d4717`  
		Last Modified: Fri, 16 Jan 2026 04:46:00 GMT  
		Size: 4.3 MB (4283870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a01d1424b7470a10d7554bf6b36954a73de3b9bedec0cf72a050482646adf08`  
		Last Modified: Fri, 16 Jan 2026 02:01:50 GMT  
		Size: 19.2 KB (19162 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:ada8bfd9abfa7ecf466306635c136dbf59c42ba46b0bc6b0c5c0b65074e9b953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.8 MB (234811026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad6a20fd511f02a3860fadd86b272a3b915240846295f341001760ce5dd4385f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1768176000'
# Fri, 16 Jan 2026 03:27:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 03:27:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 03:27:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 03:27:00 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 16 Jan 2026 03:27:00 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 16 Jan 2026 03:27:02 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 03:28:01 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 16 Jan 2026 03:28:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Jan 2026 03:28:01 GMT
ENV LEIN_ROOT=1
# Fri, 16 Jan 2026 03:28:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 16 Jan 2026 03:28:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 03:28:06 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 03:28:06 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7fcf9f2b462d6af06c3ad2420b999e6b092984c4723ebac480c428a5d837d3b7`  
		Last Modified: Tue, 13 Jan 2026 00:40:14 GMT  
		Size: 52.3 MB (52327376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b81e238ae58948d8dc745be1e6898b971765c75d8be7f14150f15f3e10660ba`  
		Last Modified: Fri, 16 Jan 2026 03:30:07 GMT  
		Size: 157.9 MB (157942941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f983a34166d5030b106a1729d522fffeee6b3b73474e47aee8b228bf23b72f02`  
		Last Modified: Fri, 16 Jan 2026 03:29:02 GMT  
		Size: 20.0 MB (20022539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d859a52b0f4ef005fb6a16db2f97fec50e92a93954e2227b967c5dc4184646`  
		Last Modified: Fri, 16 Jan 2026 03:29:13 GMT  
		Size: 4.5 MB (4517740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f907dcc14128e331dff2f1dacba2d4260334f397d3bb6c4bb6e50871d710b6a`  
		Last Modified: Fri, 16 Jan 2026 03:29:01 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:050a1f84c961210408c94cbe935ac10bed99d40051e03192bf44695e25657266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4305178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e8b7a629c02f070951e291debe390033e14198943e859719c49cc12364418b7`

```dockerfile
```

-	Layers:
	-	`sha256:731e9a3ee9092375921ba6af0a4aa7da81b91c7a6dad119005e55618db9bfd8b`  
		Last Modified: Fri, 16 Jan 2026 03:29:01 GMT  
		Size: 4.3 MB (4286104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8d83e85a386a16bc9aaed5b13e401b8a56f9e8f1c63ba8df0fee7cc1dec681f`  
		Last Modified: Fri, 16 Jan 2026 03:29:01 GMT  
		Size: 19.1 KB (19074 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-2.12.0-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:7f9d8c9451623f2e5ee86ea212c57eb8c605d3b9447c43e5257ae777b0ef84fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 MB (218188471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae395741062830fbeb7821f589eb5631ebb1e4e3711a625b8bd62abca65e9f8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1768176000'
# Thu, 15 Jan 2026 23:17:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:17:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:17:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:17:33 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 15 Jan 2026 23:17:33 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 15 Jan 2026 23:17:33 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:17:44 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 15 Jan 2026 23:17:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 15 Jan 2026 23:17:44 GMT
ENV LEIN_ROOT=1
# Thu, 15 Jan 2026 23:17:46 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 15 Jan 2026 23:17:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 15 Jan 2026 23:17:46 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 15 Jan 2026 23:17:46 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:533e1723f6efd3a2dac5ef2d710062f1e6292bf061b83d41b908fe862b8922dc`  
		Last Modified: Tue, 13 Jan 2026 00:40:26 GMT  
		Size: 47.1 MB (47138430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52650cbece299c36a25f9b264b30831b318ce46d9f17a6e071347f2cc958579c`  
		Last Modified: Thu, 15 Jan 2026 23:18:14 GMT  
		Size: 147.1 MB (147069857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1344203172139adbfeabac0db31cb3a31e508fe8ff67a24da46fe3e2b4795700`  
		Last Modified: Thu, 15 Jan 2026 23:18:11 GMT  
		Size: 19.5 MB (19462055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4169f18f941f0dc05b8ae38eadb4976deb96c40a18146b845c36a059d2dc4bd2`  
		Last Modified: Thu, 15 Jan 2026 23:18:11 GMT  
		Size: 4.5 MB (4517701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af395a235a2394fa6bacb97213ea95bbc639aba28484b6fe594ce75741af0d9`  
		Last Modified: Thu, 15 Jan 2026 23:18:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-2.12.0-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e1f9d24d6f720e55ec022d3e6f96b53a1512f1e4ecebbbfc341a849ce42ff88c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4295063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50dc07f3025679237e45d26035bdc9390e7f1ad0c6a63f7cacfa50cc89d715c0`

```dockerfile
```

-	Layers:
	-	`sha256:3a9d47bcee6a2b11143efb82ca62dbb6e63b3ae42d19d41250af922798ad61bd`  
		Last Modified: Fri, 16 Jan 2026 01:41:38 GMT  
		Size: 4.3 MB (4276045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1edd640bac424136022eca81abdae7e542dd25ff1bfdac360bd15c85105cda44`  
		Last Modified: Fri, 16 Jan 2026 01:41:39 GMT  
		Size: 19.0 KB (19018 bytes)  
		MIME: application/vnd.in-toto+json
