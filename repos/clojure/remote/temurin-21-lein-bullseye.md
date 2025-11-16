## `clojure:temurin-21-lein-bullseye`

```console
$ docker pull clojure@sha256:74b99817d59afe1ce64f6931364fc5c6f333b7c411fbd22bd5e2fb65127f5f59
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:ab611eab4cfdf978c9c3f7fb33ef131074390f846016ef66dd2274765e06df3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.7 MB (232708482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:868551c1d68ef858d0d78438746c00cd1da95091e48bd7c956c6c1b23f8a8df6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Fri, 14 Nov 2025 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:53:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:53:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:53:53 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:53:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:53:53 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:54:07 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:54:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:54:07 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:54:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:54:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:54:09 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:54:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03cb4c502f7be8fd3e28ea83935d5dcd6a7e53dc49af4d9e845efcd5dad29a4`  
		Last Modified: Fri, 14 Nov 2025 08:50:28 GMT  
		Size: 157.8 MB (157825981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ace9edbbcf9d56efcfecf426e536a69d55c15353d9572c97c9dae7d5b4fdea9`  
		Last Modified: Fri, 14 Nov 2025 00:54:37 GMT  
		Size: 16.6 MB (16607630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6408913bf322d5174b4c65b7a8c758d237d16b4225c96deb6ba1caa3e4c039be`  
		Last Modified: Fri, 14 Nov 2025 00:54:36 GMT  
		Size: 4.5 MB (4517748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fbca3b465349410b1167c7a6029de9da8aeec4e5e3cf4e577c4180e28a9176`  
		Last Modified: Fri, 14 Nov 2025 00:54:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d1dcd7bc2cd23bf9584cf74bbbfee8d008736f797976dc53f37c5bccf26082d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4497660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107880e2a0a33686beff9dc85dcba8d0ff8cdb82bc1b971a3de65471acb3a3cb`

```dockerfile
```

-	Layers:
	-	`sha256:d4614e46165379c5bb570f1dca93c3f4db47fedb3ac18ec92ae74d571a19c98c`  
		Last Modified: Fri, 14 Nov 2025 04:39:29 GMT  
		Size: 4.5 MB (4479292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af3ff7e9d2d3e6f5d0519c8483646cc416c259b5e7d4dbc1c7935dfb15b1b50d`  
		Last Modified: Fri, 14 Nov 2025 04:39:30 GMT  
		Size: 18.4 KB (18368 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1227af476e64b22e46ff8e9fa7f81290d55b6819e3790ea98a4cc33ebd095409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229478825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ebd35292f92351817f43bd2604aa4bef45ba61c296939ba9b5bea0d71065af`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Fri, 14 Nov 2025 00:55:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:55:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:55:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:55:55 GMT
ENV LEIN_VERSION=2.12.0
# Fri, 14 Nov 2025 00:55:55 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 14 Nov 2025 00:55:55 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:56:09 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Fri, 14 Nov 2025 00:56:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 14 Nov 2025 00:56:09 GMT
ENV LEIN_ROOT=1
# Fri, 14 Nov 2025 00:56:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Fri, 14 Nov 2025 00:56:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:56:11 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:56:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034b0db75b5740988691fc20354c0dcf3088e88290637bbc6eeb4283b627c371`  
		Last Modified: Sun, 16 Nov 2025 01:32:57 GMT  
		Size: 156.1 MB (156107673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e763c294094c8b7f72df24abe0ceae92cbb2899444927205c7270d7e1070f0`  
		Last Modified: Fri, 14 Nov 2025 00:56:38 GMT  
		Size: 16.6 MB (16595010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78feb3820779c02c10f5b99dc3c47165bbcdfaa206f834aadf7126cca3080d5`  
		Last Modified: Fri, 14 Nov 2025 00:56:38 GMT  
		Size: 4.5 MB (4517744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a014c014347ef06686b7f687b251c0fc074241980e4eb8e6d9c76032238e35`  
		Last Modified: Fri, 14 Nov 2025 00:56:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:010a8e402d16c6ca173886e87d7e70e7b48097dd60207cecbc94b8d9df833ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4496754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57ba124bdcb782fa3cdc736312f05470c0fb3754e9c1327f22db487f3e1ba60`

```dockerfile
```

-	Layers:
	-	`sha256:cfb79f8af6942e87e8f0fae6e69c6ac6ff66225b598f3505026c4afbb4046a75`  
		Last Modified: Fri, 14 Nov 2025 01:45:18 GMT  
		Size: 4.5 MB (4478266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2d7b75133e2f711d96f9740c558cfec37442203a18b38d38e31d413a9925795`  
		Last Modified: Fri, 14 Nov 2025 01:45:19 GMT  
		Size: 18.5 KB (18488 bytes)  
		MIME: application/vnd.in-toto+json
