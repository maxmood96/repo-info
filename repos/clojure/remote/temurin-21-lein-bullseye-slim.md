## `clojure:temurin-21-lein-bullseye-slim`

```console
$ docker pull clojure@sha256:fcf0b9ab8680918ea12c0af5ca1adc9de2b13ee52b13b3d1ddc8e3850f0ba82f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-lein-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:19c8e5a82490bd770ef0df24c1c10d4aea2d4d2a4bcab008319a47c6294c7dfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.0 MB (207972084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c513407ff6ed8ff37850ad7fa506a97b6b33db1ebed77599dbcf4ad04f2556b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:04:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:04:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:04:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:04:53 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:04:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:04:53 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:05:07 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:05:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:05:07 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:05:09 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:05:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:05:09 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:05:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c5aae4d85d45d625605212da6465fcde1b86c689c04fd3cf30af826946c349d`  
		Last Modified: Wed, 15 Apr 2026 22:05:29 GMT  
		Size: 157.9 MB (157857082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ed2771fe87fb6251360c2d74bb0592b9f2eda77161f474e19d53ef34f37ff8`  
		Last Modified: Wed, 15 Apr 2026 22:05:26 GMT  
		Size: 15.3 MB (15338814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ca5cb2719e50c3b3623c1623eac99ebfce16e59b4c16dee1ba74df3fa9c5ef`  
		Last Modified: Wed, 15 Apr 2026 22:05:25 GMT  
		Size: 4.5 MB (4517740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe79b45799dfe351e1251abec58ddb31f44bb4f95ea2a712546432460513dcdf`  
		Last Modified: Wed, 15 Apr 2026 22:05:25 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:03a4156b57adb5be0c89fe7c63aaf58024dd6ee811a1621764d9d99ea2555367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3f2ac8a6cb92e2d37798a067b21a2ae2e0b2bfe731a7e4d79ef5b02d47287b`

```dockerfile
```

-	Layers:
	-	`sha256:df12b0f10fbede21beb9a516a6392c58ccaa30ce618c8b1ad74dc2d0733a2990`  
		Last Modified: Wed, 15 Apr 2026 22:05:25 GMT  
		Size: 3.0 MB (3029434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01c3da16c527dc829034c4ddf04b56466b66a8eac35254ccbef55517dbcbc8b8`  
		Last Modified: Wed, 15 Apr 2026 22:05:25 GMT  
		Size: 18.4 KB (18403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-lein-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9b8ed90bcc7093ef021c83c7109f47967a18407bbaeb9d5bbeeb361f5b26cdbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204723145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c3ca72818fb1b884d83f924c9620a3b540d3853655f797d14d13b04f863d45f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:16:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:16:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:16:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:16:27 GMT
ENV LEIN_VERSION=2.12.0
# Wed, 15 Apr 2026 22:16:27 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 15 Apr 2026 22:16:27 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:16:40 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "12a9c5e3a2471619ca3d64a7462f920fdf713ae8959eb4fcd6257c23332b5aa4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Wed, 15 Apr 2026 22:16:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 15 Apr 2026 22:16:40 GMT
ENV LEIN_ROOT=1
# Wed, 15 Apr 2026 22:16:42 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.12.1"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Wed, 15 Apr 2026 22:16:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:16:42 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:16:42 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04e3bf8143064c29ecccc1d3d2ef1339f4d540cd0c2e535df4281d3cf16d436`  
		Last Modified: Wed, 15 Apr 2026 22:17:08 GMT  
		Size: 156.1 MB (156133091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa722bfe7fd193b408811db867e7b2d7ab9f5abf5ed65f3cee9ccd12421c07c`  
		Last Modified: Wed, 15 Apr 2026 22:17:00 GMT  
		Size: 15.3 MB (15327223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a90ef3c9aa914b09f38644b6ca68d0616da78961bb723001d52ccaede5d860`  
		Last Modified: Wed, 15 Apr 2026 22:17:00 GMT  
		Size: 4.5 MB (4517714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88fc08c9080921a1437f7c7ce6ef4319d4cc535cffc4a632dea0d3eb0048a2ee`  
		Last Modified: Wed, 15 Apr 2026 22:17:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-lein-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d129a6ca30a3b47fd382e938bef1e4fb0cb8f189f121726bf3ff78e487b4868a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3047565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dd6aca833e40962b37281d4de466df0534a49784f28de471c68dd3567772b09`

```dockerfile
```

-	Layers:
	-	`sha256:6a3b438ec5872c89a0515f5b0bbc621d1397c932bba1fe8232b907041ee56023`  
		Last Modified: Wed, 15 Apr 2026 22:17:00 GMT  
		Size: 3.0 MB (3029043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6976c8b93f194de5804a403470b6b2265137cbd094413809d173825565713fba`  
		Last Modified: Wed, 15 Apr 2026 22:17:00 GMT  
		Size: 18.5 KB (18522 bytes)  
		MIME: application/vnd.in-toto+json
