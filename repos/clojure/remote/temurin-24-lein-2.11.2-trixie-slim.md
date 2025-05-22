## `clojure:temurin-24-lein-2.11.2-trixie-slim`

```console
$ docker pull clojure@sha256:1b35f2473db5712277344041210b634d790a481ac10065d009925e2428e2cce6
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

### `clojure:temurin-24-lein-2.11.2-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:413032b3505da44bd082bac46a1cbb7259d5e47b258f755a5c00f5909fbaec72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.0 MB (178035316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640877af90f6fd392d4d0431c526cbbc113cfea3f56680c378030a7b72833ce7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ced038dea045df288fe9bdbe03117ca66fe2a071217e196ac86ed07f965fe688`  
		Last Modified: Wed, 21 May 2025 22:27:59 GMT  
		Size: 29.8 MB (29755384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c6388de7ca26fe58c6d508a3af9b734d615c477fc056e1919b53e1a079c429`  
		Last Modified: Wed, 21 May 2025 23:33:57 GMT  
		Size: 90.0 MB (89952022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4634bf197e2e0d95adcc66e100f595dddf02e8f0b5eb6ccc7afd31a8c83b9d22`  
		Last Modified: Wed, 21 May 2025 23:33:56 GMT  
		Size: 53.8 MB (53813286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792e7c2ced555609e33bc81f9e809748564ed9fc04eba1801c6ed148dfddd6b3`  
		Last Modified: Wed, 21 May 2025 23:33:55 GMT  
		Size: 4.5 MB (4514195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af4cfa4b2533e6cde8f4d52afab9ac21d6fe5f37ee27d882864e94ae8f145ca`  
		Last Modified: Wed, 21 May 2025 23:33:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.11.2-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:00f97e19ab1ea6e0fd4384dca2d6fea730d521f7ea9bfa4abbb16790bc9195f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4132789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67ac3947efaacb2dd071b6cea421a1d1d1263785a1af38f082061f304065fc45`

```dockerfile
```

-	Layers:
	-	`sha256:5e849f7f7c49f336f4d6e238191f2b53d2741bb6083f671ed21888e6fbbcae9d`  
		Last Modified: Wed, 21 May 2025 23:33:54 GMT  
		Size: 4.1 MB (4114358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3a9941b5d3cd678e83a2531029fd784c14b75f8303a71b7fa70c77e86a0a04f`  
		Last Modified: Wed, 21 May 2025 23:33:54 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-2.11.2-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d36e1adadb48eb37079e5a68450426fe0837efd46035081f8c526d45635fc671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177593114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784d125b0bc1a7698ff940bf2641251f7a8003dd5ccada82ae9e915df1d04681`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:d0342bfffaba1a8be0950e44b5334c6cf9a05d9eedd81a042ec7813ac91850a4`  
		Last Modified: Mon, 28 Apr 2025 21:23:36 GMT  
		Size: 30.1 MB (30130233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf78d6205bb385dbaea21715ebe2773e6352d0ca5870bdfcb0e246524d354c9f`  
		Last Modified: Tue, 13 May 2025 18:09:24 GMT  
		Size: 89.1 MB (89091185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7a196124bd04a361c532c52e3ca381d0d7e2ef34b79b2f52b9f39f41feb90a`  
		Last Modified: Tue, 13 May 2025 18:09:23 GMT  
		Size: 53.9 MB (53857109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cec617ac6634db22b84baf62eb3f718cdcbbca70fb55507975b8a936829b680`  
		Last Modified: Tue, 13 May 2025 18:09:22 GMT  
		Size: 4.5 MB (4514158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3c2a35562f8e7554010702c0b860c0a787b1d4285c2f64f0ed4fdf211c080c`  
		Last Modified: Tue, 13 May 2025 18:09:21 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.11.2-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5399162e0688e2ed320e7bfefe293012923ec9f48feb40e2219b46984d172dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4094675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc07395bc6a9786a59863350926a8673cc48188aecc398d29d6b12a34d5bde4`

```dockerfile
```

-	Layers:
	-	`sha256:91848f2c7fe6b9064c6a4cb80dd1f03d3fbf0edb563709d791572ce4f8439036`  
		Last Modified: Tue, 13 May 2025 18:09:21 GMT  
		Size: 4.1 MB (4076123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e608abc81b294bb24180df720f74620faf96d2db06eeb0f72c13a490e34d5ac3`  
		Last Modified: Tue, 13 May 2025 18:09:21 GMT  
		Size: 18.6 KB (18552 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-2.11.2-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:870b93cde9e72e59d94ea5a73678b2ff3117cd1fd4014e5e13ee05588bb52817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.9 MB (186887912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b43cf8d2bd6fbf577fcf8d86483681d4d2e653e86cd14907e6647a54aa7eea4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:a739447e8599431e1e4996b4b6d4022822d37eddea9a3737acbea74b8a860d49`  
		Last Modified: Mon, 28 Apr 2025 21:25:59 GMT  
		Size: 33.6 MB (33577694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8803762d089e91a891a211912215216c857d1bcb4d597780a3b0fa903fd22f`  
		Last Modified: Tue, 13 May 2025 19:37:16 GMT  
		Size: 89.9 MB (89920243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e2e3685a2c9bbe4006454a7e6baf16a5686d63d941d9af8016731e883dfaed`  
		Last Modified: Tue, 13 May 2025 19:37:15 GMT  
		Size: 58.9 MB (58875372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8743b9b51d8dca6fe56c733a0e7cdaa609084fc188dcddeffbf990fe86a42297`  
		Last Modified: Tue, 13 May 2025 19:37:13 GMT  
		Size: 4.5 MB (4514174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd34420e7709e7542db33b8407a77a8ebda8328336b0e2b2f11328fef5fdf80d`  
		Last Modified: Tue, 13 May 2025 19:37:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.11.2-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0dafb6d0d8cf67bc90148a7809f4afcb9a884de01d8bb550d5726f61d05dd0bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4094111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a943da6249271d0a2515958015ec6f8c860f495f078b9549b6cff9e5b51c6f`

```dockerfile
```

-	Layers:
	-	`sha256:92a9cd073da99229b3602661bdbf3ed3f4355083f8c958b28718c109e1d5455a`  
		Last Modified: Tue, 13 May 2025 19:37:13 GMT  
		Size: 4.1 MB (4075636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0de75cfdcbc3eb1e2b7597fb4b98e7f080273a1f5ad5966da6a3aff6ff44d56`  
		Last Modified: Tue, 13 May 2025 19:37:13 GMT  
		Size: 18.5 KB (18475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-2.11.2-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:fcfe9c2f3da3df76f477751c8cdf43b7b11e419c1b62f4830867dcab59d90672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.4 MB (173395653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95102aafea0bc2e535437c050f2d53f41c9e141cc22c41f2c36d2a588a086146`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f092cb6a76bde9a7b3c337ea49e8a7adec71062dc5df097be99d3975e92bc53a`  
		Last Modified: Wed, 21 May 2025 22:38:21 GMT  
		Size: 28.2 MB (28245354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48520921fd3b539bfda2058ded0f2724c28bfb9b6163fa249dc8bc5476454af`  
		Last Modified: Thu, 22 May 2025 00:47:54 GMT  
		Size: 87.6 MB (87622251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904d4f67db7759495cbd29e40ff7275a19f0a1ea0606f29c1e736380677c6a0d`  
		Last Modified: Thu, 22 May 2025 00:47:49 GMT  
		Size: 53.0 MB (53013393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390db2eaf38b07c90b4b68eb155408cbc435e75316a5135cbe1d6624948a3c35`  
		Last Modified: Thu, 22 May 2025 00:47:41 GMT  
		Size: 4.5 MB (4514226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe11f49e3e4e539228fc5973b9fd1e74ebebea872881a092cd653bf1b0ad8201`  
		Last Modified: Thu, 22 May 2025 00:47:40 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.11.2-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d9f2df3f312a7725c5a426b1a1444a095eb3db2201f7c7fddd009580027fdc1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4122208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb8265e918868439e12df557af0f71f8092daa2ab24440f5c8770a28ee102b5`

```dockerfile
```

-	Layers:
	-	`sha256:d43cbe2916d7f8f5d873e255fe7a31b10b8956cee8e8e6fa7d320f7bd931c3c0`  
		Last Modified: Thu, 22 May 2025 00:47:41 GMT  
		Size: 4.1 MB (4103734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e5b89e317dfecc5fa9dd055aff89dc1fd9b77f60e6adfc6283606b1d1bfdbce`  
		Last Modified: Thu, 22 May 2025 00:47:40 GMT  
		Size: 18.5 KB (18474 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-2.11.2-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:2f572fc99ad42a26c3181df9a3ae4724c8c1540e56067432b63a6c951b71ea3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.4 MB (174435775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52f4381a0fa2e28a8c1b11a3a09f52224ba135b17ab71d76903b7278cb3641de`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 May 2025 03:53:36 GMT
ENV LEIN_ROOT=1
# Tue, 13 May 2025 03:53:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7cbda353d6047374e3da60bdf79ae89f8047840010f0964c87a8f2714e146106`  
		Last Modified: Wed, 21 May 2025 22:32:10 GMT  
		Size: 29.8 MB (29829620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23819e9a6f660656140faefb0803a95a0ac0d02661346d1fc445aafdafc5e949`  
		Last Modified: Thu, 22 May 2025 04:08:52 GMT  
		Size: 85.2 MB (85216727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80351f929d16b9fba983fbb19597015039fb342dce508c84301c0d6fed3b2c4`  
		Last Modified: Thu, 22 May 2025 04:08:52 GMT  
		Size: 54.9 MB (54874807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9fa2bc97a14873c28e3cd4add8d0708f9d339710a88433341c241caff2f88d3`  
		Last Modified: Thu, 22 May 2025 04:08:52 GMT  
		Size: 4.5 MB (4514193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46bfe13420b51b6b58947433925b9c0d68930327d28a41af49469b469b9e66e7`  
		Last Modified: Thu, 22 May 2025 04:08:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-2.11.2-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e2d195a4d25ffc7e6866ad431992c65e4c1918eea21bb977552b8a213dbe8120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4131316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03db9e906838766ddcdd4b19dab7a1daa405e511c781d6d55533324fe13b2b95`

```dockerfile
```

-	Layers:
	-	`sha256:36c46df86da4560ec4cd07e8198f1e0c151315292e1ec0edd46f155d29176ca9`  
		Last Modified: Thu, 22 May 2025 04:08:50 GMT  
		Size: 4.1 MB (4112885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d6668a207dcaf5c78374f116982e12acb8f6dc721bef41e8dbcea37362254a9`  
		Last Modified: Thu, 22 May 2025 04:08:50 GMT  
		Size: 18.4 KB (18431 bytes)  
		MIME: application/vnd.in-toto+json
