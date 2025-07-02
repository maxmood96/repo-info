## `clojure:temurin-24-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:66782d217eed1bdf7a649332c508d4eb95ec357e0766ef9797b49fb720560526
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:54079ddd18945fe618ff029234a7e562ea3f139ad963ada9d63280d9e6eec66b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.0 MB (168002422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd9323841255188f3d7fd32bbc34aa1afe8c62245f1cb973415f9370ee625d97`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:cc41ef31545f10925901837c6dea7e184299788097caaa3fabb57ed109c52a98`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 30.3 MB (30256047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8609c9c73f9c388dc1a614c2ece6016f03c02073c3f53602b9ca4bc4cb7741`  
		Last Modified: Wed, 02 Jul 2025 04:17:44 GMT  
		Size: 90.0 MB (89952000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d480915c60b0bff7548ab625ee05add0859e9a7cb53eb991c901e9bdc1d835d`  
		Last Modified: Wed, 02 Jul 2025 04:17:34 GMT  
		Size: 43.3 MB (43279775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d42eccce149ccd78d864934999355e820ee16c6076a268356d82dee96ed0e8a`  
		Last Modified: Wed, 02 Jul 2025 04:17:28 GMT  
		Size: 4.5 MB (4514172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d4f21e2580c4bc7f15ce10ba6087c641e0203ebf7fb0133b60761a7703ce6d`  
		Last Modified: Wed, 02 Jul 2025 04:17:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:70e3277b09ab300041b056122b2e488b28b4ee8070e303cff9739093e8d71145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4699832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b88d77c2248423f65b6e24d15912799b0959f0646b55644fc1c44e53a6f938`

```dockerfile
```

-	Layers:
	-	`sha256:30e888a01cc4c98def7384451cbe2cc11abdd1d4660ad2a1aa645b07c710b783`  
		Last Modified: Wed, 02 Jul 2025 06:41:33 GMT  
		Size: 4.7 MB (4681381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93ed397b7cdb30d3ca65b089070574b42a1dfa5e6f4c828a7805bcf3a034fd91`  
		Last Modified: Wed, 02 Jul 2025 06:41:33 GMT  
		Size: 18.5 KB (18451 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0f39a0ccdf4c8409aa7c15d44d6b3441bf302ee5fdb314ffae6f4cb33e70e4a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.7 MB (165666716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:090ac531862bb3aa649e62b944e9602301b047c160f557355cfc025a95246e67`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_VERSION=2.11.2
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN set -eux; apt-get update && apt-get install -y git gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 07 Jun 2025 17:38:11 GMT
ENV LEIN_ROOT=1
# Sat, 07 Jun 2025 17:38:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.0"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:00ce3d02ade4a2c8e5e37b1a218bb5c24c995bd8757095b89316c42854286fe8`  
		Last Modified: Tue, 01 Jul 2025 01:15:35 GMT  
		Size: 28.7 MB (28744140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70f5a28c76e18532e41dffe087e67fc70d78bc8a4a7d0b30373b001b9fc6a5c`  
		Last Modified: Wed, 02 Jul 2025 12:57:49 GMT  
		Size: 89.1 MB (89091234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5946c5cfcaa14cd9adcc3624aa12d2730aa8f40601127664208e4f90dacb527`  
		Last Modified: Wed, 02 Jul 2025 12:57:41 GMT  
		Size: 43.3 MB (43316752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92501aa7b0ccbbdc79892a7a00a8f00690a39f604a82c1955b7c82db2a671cbe`  
		Last Modified: Wed, 02 Jul 2025 12:57:38 GMT  
		Size: 4.5 MB (4514161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796b28f7d427571a9d53068b2fa9925f7fda888ad8d12441b0b4b795fc4d40d0`  
		Last Modified: Wed, 02 Jul 2025 12:57:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c264ae9511fbcb08d35bcefa606702319ef16f12c81c2dfe261bb0e227237ce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4705614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46115dc2561ebde25c69504818a5d4878f3b561975771e63343d9599df71ce0`

```dockerfile
```

-	Layers:
	-	`sha256:d9dcfce67d16340700774ac1da89bd16ddd2cc57da1c5d71cba143b256e62fbe`  
		Last Modified: Wed, 02 Jul 2025 15:42:34 GMT  
		Size: 4.7 MB (4687042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc622730a2eb5321e91f03c7f631e9b508e49c73fe9074071e7627f90e110eef`  
		Last Modified: Wed, 02 Jul 2025 15:42:34 GMT  
		Size: 18.6 KB (18572 bytes)  
		MIME: application/vnd.in-toto+json
