## `clojure:temurin-17-lein-trixie`

```console
$ docker pull clojure@sha256:15cddd07c22e9a2495290511f9122ba60dcef86c33f1d1f8894f55a481a019ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-lein-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:d84572362bafa2d64984deed448d755a1d7159d2db8512fa4863c7a7376b153c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.0 MB (218019672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e257912bc2dd8c6b81abbf65e73283f02ab72a0ba4f980f05c471f4fc28c39e5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:04:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:04:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:04:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:04:27 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 05 Feb 2026 23:04:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 05 Feb 2026 23:04:27 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:04:53 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 05 Feb 2026 23:04:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 05 Feb 2026 23:04:53 GMT
ENV LEIN_ROOT=1
# Thu, 05 Feb 2026 23:04:54 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 05 Feb 2026 23:04:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:04:54 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:04:54 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe4ab7ff6b3b44c15f44bb6bac45aba681cb1149046e38d236424b1e382fda0`  
		Last Modified: Thu, 05 Feb 2026 23:05:14 GMT  
		Size: 145.6 MB (145628457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72f961f7a3021a808cf9a0731202f281a5c990a3b7616ee325e7eda6252654b`  
		Last Modified: Thu, 05 Feb 2026 23:05:11 GMT  
		Size: 18.6 MB (18580123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0931d5df5604e301d998934a25986f6b24a6b2e9beb439aa1a0ac046061a0fe3`  
		Last Modified: Thu, 05 Feb 2026 23:05:10 GMT  
		Size: 4.5 MB (4517709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a492bd71b65d77f6a2026856378f3fc14c77d92b6bc8260ec27aa3bbf9fde94`  
		Last Modified: Thu, 05 Feb 2026 23:05:10 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:cf1a2f9a1dec5343bae0c5ffb996dd941ef62e54ffb4c3727d934ff44f7d31f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3833843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af940122ce11c6fbb22233f8a925eb20d0ee34f0c456d530d2b1bc41f60d97d`

```dockerfile
```

-	Layers:
	-	`sha256:9a06778d5c572d72b4191316eab676a8fcbac35a50253abd2cf52b06266729a9`  
		Last Modified: Thu, 05 Feb 2026 23:05:10 GMT  
		Size: 3.8 MB (3815491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36052247c5fe5675620e3ce726aa62476abd22f6d0a4bd4bb0c010defdc63d8a`  
		Last Modified: Thu, 05 Feb 2026 23:05:10 GMT  
		Size: 18.4 KB (18352 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6863f30e3f83f78203e5d9d1a567167fb59cf3c51c7abd2fd0afc2f3de3ec963
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.1 MB (217147781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0938f85feb3368793142de6579787b043313d4e8ff5b41d4e141c26c7ee4e7c7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:05:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:05:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:05:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:05:06 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 05 Feb 2026 23:05:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 05 Feb 2026 23:05:06 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:05:24 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 05 Feb 2026 23:05:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 05 Feb 2026 23:05:24 GMT
ENV LEIN_ROOT=1
# Thu, 05 Feb 2026 23:05:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 05 Feb 2026 23:05:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:05:25 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:05:25 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a1569030170a2048665bfb0a42b6e258f3a7b85cabd14c56b13a0a8522ec3f`  
		Last Modified: Thu, 05 Feb 2026 23:05:41 GMT  
		Size: 144.4 MB (144436235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83df3b3a1f6033b6c820d97a0a2662a3d9f028f9ea88f9cfe5f642495663dc64`  
		Last Modified: Thu, 05 Feb 2026 23:05:43 GMT  
		Size: 18.5 MB (18541389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df07b0744ae685bd1fd87d6a68e445f4173219caa9fb5621cda772c0ba0ee509`  
		Last Modified: Thu, 05 Feb 2026 23:05:43 GMT  
		Size: 4.5 MB (4517711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9d8400cf868ff3ab662d1fe2f85d6754224d16370e0d9eb8334b16b4028d18`  
		Last Modified: Thu, 05 Feb 2026 23:05:43 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1858db65fe18ce99c9d0229e1d97e9fd7f7c67e285ca2e09c58a9057d109de3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3834841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c0efe56d44e5c27ff0347e7f0011a19f770e8a307a82737801285647e31460`

```dockerfile
```

-	Layers:
	-	`sha256:c2ad7c2950ea0fa9b9f854c8d7d1cf1758d89496a6fda972bba24728be6da44e`  
		Last Modified: Thu, 05 Feb 2026 23:05:43 GMT  
		Size: 3.8 MB (3816368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b2d0841183f5038f33f1fdce8861b0800c96255cc7c3a01bc9457511c112789`  
		Last Modified: Thu, 05 Feb 2026 23:05:42 GMT  
		Size: 18.5 KB (18473 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:9e2fb5cebbc1543a7ccf9cb5074cfbd975894e583c8fc32718a0a01b9e5b2778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221706131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c07179cb88c0796857f50392a968ebc5acee375db30092212aab981e09512d3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Fri, 06 Feb 2026 00:25:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:25:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:25:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:25:39 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 06 Feb 2026 00:25:39 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 06 Feb 2026 00:25:39 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:26:40 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 06 Feb 2026 00:26:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 06 Feb 2026 00:26:40 GMT
ENV LEIN_ROOT=1
# Fri, 06 Feb 2026 00:26:43 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 06 Feb 2026 00:26:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:26:43 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:26:43 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806148462c30ed1bfef62eebe515a501af99978464a4710c612e54794c9190dc`  
		Last Modified: Fri, 06 Feb 2026 00:27:41 GMT  
		Size: 145.4 MB (145438280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb381847d5bbcab850990c682a5fd4166f64b4421cea17cefdb9d4c042b52ea0`  
		Last Modified: Fri, 06 Feb 2026 00:27:38 GMT  
		Size: 18.6 MB (18637559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9971672d11d1eef1e71cede9eeb1d52f0e383f3a38589588050c1e26bb30994`  
		Last Modified: Fri, 06 Feb 2026 00:27:37 GMT  
		Size: 4.5 MB (4517746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77b7411a3582a4afe9f66d6c676372cbaeb32d07f4fea67c806e61c96e18f73`  
		Last Modified: Fri, 06 Feb 2026 00:27:36 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a51cbc79e196c6b0015d5c3d966c89877c364c7370cdfb921a4a72767cf3f6de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3834887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb78582bc07539f391197d61763178d582133f7d1fdd7699c16de79bc369ed2`

```dockerfile
```

-	Layers:
	-	`sha256:aa70cea0b22eaeb28d912197c2a63a98aa4da88cc9ff50dd964518e6dea62204`  
		Last Modified: Fri, 06 Feb 2026 00:27:37 GMT  
		Size: 3.8 MB (3816491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cc73bc7f9c1d0dff70b608e59abd0dbed8b2e38bb40f2d779cd7a1d397b2d02`  
		Last Modified: Fri, 06 Feb 2026 00:27:36 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:401e3ce48270dd4bbf160daabe320e7e794b87b0ea64f0cb2a84f8e92294d9ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.7 MB (212716454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280bee791cf7be4c31124e5e18ef9068808a7038d4325acc1bee40ce17232fee`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 20:13:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 20:13:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 20:13:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 20:13:51 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 05 Feb 2026 20:13:51 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 05 Feb 2026 20:13:51 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 20:16:15 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 05 Feb 2026 20:16:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 05 Feb 2026 20:16:15 GMT
ENV LEIN_ROOT=1
# Thu, 05 Feb 2026 20:16:33 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 05 Feb 2026 20:16:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 20:16:33 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 20:16:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:618efd37f74728f7dcba60c231fad7f2d777dc65e4da32d0adae5e032e1fd125`  
		Last Modified: Tue, 03 Feb 2026 07:13:10 GMT  
		Size: 47.8 MB (47776763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8715f0f462c27c39b67aba65879f61c571d7691a6bbfdcec6aed27eeb28ae68`  
		Last Modified: Thu, 05 Feb 2026 20:20:41 GMT  
		Size: 141.9 MB (141889578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39f4bda650cfdcfae48ee2e1ff7d18298a1d3bbb859a11cf4bca3d174e926fe`  
		Last Modified: Thu, 05 Feb 2026 20:20:24 GMT  
		Size: 18.5 MB (18531887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185666daa5d6540a047c9ce44bc731d33aa468da2e5aae3854a6b78042552413`  
		Last Modified: Thu, 05 Feb 2026 20:20:20 GMT  
		Size: 4.5 MB (4517795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28481884be0a4f341ec9b041b03cc78e4e2180bed88e86bd78edf33d89bfc10f`  
		Last Modified: Thu, 05 Feb 2026 20:20:17 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a685245080defba5fb10a558aa8f0739061735dc6b5545d6453f9009a333024a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3821193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a15fed9ae6a458efd330526c6d6f8495c8bf004655e4cffbb40441a7b80f3af`

```dockerfile
```

-	Layers:
	-	`sha256:a60676cac8a59e35f063575ffe855f2eac5c3d6e5b3c5a369f798f94493cc09b`  
		Last Modified: Thu, 05 Feb 2026 20:20:19 GMT  
		Size: 3.8 MB (3802797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a6e29abffd531221836d3d9419cbeb4995a16b9da4af94df103631f41ce672`  
		Last Modified: Thu, 05 Feb 2026 20:20:17 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:e53a8a41bcaa9703f4782c77d0e0307ae8bac97df2b9d7c831f94bda8eae2a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.1 MB (208120654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a63deb9ceb853a9d3454e05283cddea21347ca07045b869af34e78c426ec1d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 23:02:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:02:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:02:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:02:58 GMT
ENV LEIN_VERSION=2.12.0
# Thu, 05 Feb 2026 23:02:58 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 05 Feb 2026 23:02:59 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:03:13 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Thu, 05 Feb 2026 23:03:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 05 Feb 2026 23:03:13 GMT
ENV LEIN_ROOT=1
# Thu, 05 Feb 2026 23:03:15 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Thu, 05 Feb 2026 23:03:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:03:15 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:03:15 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf389a6a5e627a977a7dfe9ebcff8ac8e498c97e8faf5da41be1750104836fd7`  
		Last Modified: Thu, 05 Feb 2026 23:03:42 GMT  
		Size: 135.6 MB (135627054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02ef38df03da0b49fbffd11150a7a51e7089bdd7f8349cccb102fa9859d21d0e`  
		Last Modified: Thu, 05 Feb 2026 23:03:40 GMT  
		Size: 18.6 MB (18621052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a4dcdf92cb1706ae03c806b5702d4db313a4989aff9cc45df8671f955e64c1`  
		Last Modified: Thu, 05 Feb 2026 23:03:39 GMT  
		Size: 4.5 MB (4517740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d35e3614e90b3db736cbd318d8f8ef4ea7c9e9fb68aac4cdf3578bc16d5c107`  
		Last Modified: Thu, 05 Feb 2026 23:03:39 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e6d3beebcccb0cc5af92eef9275980ebbb5ebb727603462b8e40eb1a4527f55a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3830269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f6652a0e68b1612ab1ee96f3bbc591daafd36171d0a79e3f922f78b9c7f822c`

```dockerfile
```

-	Layers:
	-	`sha256:7e61f4f9cabea16e13d27b29ceb7f7a8f034c75f7430c61f2dec53d2e683ba66`  
		Last Modified: Thu, 05 Feb 2026 23:03:39 GMT  
		Size: 3.8 MB (3811918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b49d463eaf0bbafda682ba2e8e4ec7b29b5ae9f9003a571e31ba436f260c6ef9`  
		Last Modified: Thu, 05 Feb 2026 23:03:39 GMT  
		Size: 18.4 KB (18351 bytes)  
		MIME: application/vnd.in-toto+json
