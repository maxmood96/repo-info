## `clojure:temurin-17-lein-bookworm`

```console
$ docker pull clojure@sha256:654f31d58d6de34ae195e864211674075255e145bfe3fb6b425fa2dcc9a373ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:b3ddd11dbcfd083899b013d7da117faddc2e9fb60ba02b0d9bb787a2d4c791f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.3 MB (261290153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d93e2158c9bfa2f0f4ad1abe98c580cf21c960773e181b72fc80b9cb23650e2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:36 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Wed, 04 Sep 2024 22:30:36 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV LEIN_VERSION=2.11.2
# Fri, 06 Sep 2024 16:59:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 06 Sep 2024 16:59:26 GMT
ENV LEIN_ROOT=1
# Fri, 06 Sep 2024 16:59:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09ea730adac53d3e05df211317da6a0d71fb6e9092fb15330e7872ee9afb3a4`  
		Last Modified: Tue, 17 Sep 2024 01:56:45 GMT  
		Size: 145.2 MB (145166536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0430f5020fa80658f7f3c50a3ce4ec2177f387f3333a7abc5a5e116f8b6d2f6b`  
		Last Modified: Tue, 17 Sep 2024 01:56:44 GMT  
		Size: 62.1 MB (62052283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c41e4cd2fb861f85a5f5ce7cad5486cfbcbdd8b2b623ae59bbd0e63b6d2ad6`  
		Last Modified: Tue, 17 Sep 2024 01:56:44 GMT  
		Size: 4.5 MB (4514202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d2f8a09fd0621d54d5cf45aaaf69035a1cb23924d07b14ab94d0bf565d37f4`  
		Last Modified: Tue, 17 Sep 2024 01:56:43 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:11ec369365821b4e03a71af1af6c987391e6f3141a3727fc7177a3b5160a491d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6389122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05997a9e60223553917ca90dae4944ccce7c07eb437650325dc244b5af68a5ec`

```dockerfile
```

-	Layers:
	-	`sha256:2cc57865f8fcd5eaab443db12f8fd0f26b4a6c45229dbc2dae98a8ad24ac51f7`  
		Last Modified: Tue, 17 Sep 2024 01:56:44 GMT  
		Size: 6.4 MB (6371080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39a2eb6f0c46832ea1506311307f6502fb8b97a535c904532864461eb2a41a50`  
		Last Modified: Tue, 17 Sep 2024 01:56:43 GMT  
		Size: 18.0 KB (18042 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fbb2880e81746704197d1907fe64a03ebd5608bfe1e5aa608933f2cdce46ba73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260091696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c14478c0d558c6bb05e69e69b549baab50bb46573df45e102c41220477c8704b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:42 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Wed, 04 Sep 2024 21:39:43 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV LEIN_VERSION=2.11.2
# Fri, 06 Sep 2024 16:59:26 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN set -eux; apt-get update && apt-get install -y make git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 06 Sep 2024 16:59:26 GMT
ENV LEIN_ROOT=1
# Fri, 06 Sep 2024 16:59:26 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7200d0857db89d07cbd5e5cb92b246c83e764f2907e18fd7164a637ac306e4`  
		Last Modified: Tue, 17 Sep 2024 04:30:16 GMT  
		Size: 144.0 MB (143959449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777dbe34315db2fc399fb669e44fded60af711a8ec4043be75fce3ff153bb607`  
		Last Modified: Tue, 17 Sep 2024 04:30:15 GMT  
		Size: 62.0 MB (62032004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0e802c564f255f0023a1f25d406aa839ae5cd83d6e5b379bfaa0a27f8bb9e0`  
		Last Modified: Tue, 17 Sep 2024 04:30:13 GMT  
		Size: 4.5 MB (4514190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ec108b9e76bb751a6a3670b371d86161f4baebe6ebcc14f36dafc8a21a1f8f`  
		Last Modified: Tue, 17 Sep 2024 04:30:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:65dbb9172ebc5386597cbdc6b89e8d50b51e101aa1cc77807c5177303476c780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6395963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15fece09b9d30e11f3fc8e5a70a7d0e1660a509ffb74792602bafbd84b860de1`

```dockerfile
```

-	Layers:
	-	`sha256:7afffb727b501b5f1f7d080af4d63aa0f66d8c4b90dabb09e2dce0aee33d333d`  
		Last Modified: Tue, 17 Sep 2024 04:30:13 GMT  
		Size: 6.4 MB (6377398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:110ca42a04e5c01ec8c7b16ed1bcf0ce542ea53357941ff8792cdcb0c7c21351`  
		Last Modified: Tue, 17 Sep 2024 04:30:13 GMT  
		Size: 18.6 KB (18565 bytes)  
		MIME: application/vnd.in-toto+json
