## `clojure:temurin-8-lein-2.10.0-bullseye-slim`

```console
$ docker pull clojure@sha256:59fef7e985bf8f5c41377b42c79fb32f970053129859710eed4b1c3b33fe6b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-lein-2.10.0-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:cd027ba32b416d9590a749186d6fecbc1d2201bb7132dcca87df68b00bf720f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (151993854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b255b47ac5fffbf536cd04bf562d95b422ea9943e96a38107dd506d172493a4a`
-	Default Command: `["lein","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 04:54:00 GMT
COPY dir:a294625293e4e40913c98181a9aeff55bc5e737b728d424dfdc884f576bd8f8d in /opt/java/openjdk 
# Thu, 11 Jan 2024 04:54:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 04:55:53 GMT
ENV LEIN_VERSION=2.10.0
# Thu, 11 Jan 2024 04:55:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 11 Jan 2024 04:55:53 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 04:56:08 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 11 Jan 2024 04:56:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jan 2024 04:56:08 GMT
ENV LEIN_ROOT=1
# Thu, 11 Jan 2024 04:56:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 11 Jan 2024 04:56:11 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174aa11106f2d3d4da01484fac2da5df4e3ce9ec4196afe1ba0d6908551deaf2`  
		Last Modified: Thu, 11 Jan 2024 05:15:12 GMT  
		Size: 103.6 MB (103598261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d61c5f0e9e8c026a4dc58e6502d1e23a1ed053888959364215d48997b54e030`  
		Last Modified: Thu, 11 Jan 2024 05:15:53 GMT  
		Size: 12.6 MB (12578358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d7f4b7a30677af675cc1f2716d5ecdcc084922d684e6b375843a1e5b97d2ce`  
		Last Modified: Thu, 11 Jan 2024 05:15:52 GMT  
		Size: 4.4 MB (4399280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-lein-2.10.0-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4b8dd5711000aa6d2521f07fdbf0e0ccb3a84cd4ecadd7df2f1dec0a7a6d253b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.7 MB (149730515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:991957f2372a53a31d39f9501974eda745e7dbee3b7f71488c4abf230d0e2cd1`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:00:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 06:55:48 GMT
COPY dir:95966e8772805277b939f0a555f93ce7d7e01898449cdb0fb69c182fe80d4021 in /opt/java/openjdk 
# Tue, 19 Dec 2023 06:55:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 06:57:17 GMT
ENV LEIN_VERSION=2.10.0
# Tue, 19 Dec 2023 06:57:17 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 19 Dec 2023 06:57:17 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 06:57:29 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "b1757ce941e4cbf15cbf649b7b4f413365e612da892d22841ec1728391bb66af *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 19 Dec 2023 06:57:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 Dec 2023 06:57:29 GMT
ENV LEIN_ROOT=1
# Tue, 19 Dec 2023 06:57:31 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Tue, 19 Dec 2023 06:57:31 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8460c2429b384c138ca104a8d205038e1877169d7a2d55c0430c97fdacb19c12`  
		Last Modified: Tue, 19 Dec 2023 07:13:30 GMT  
		Size: 102.7 MB (102701538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5488d8ca0599e7ea8e3bfcde73495aca214c22514b1be6884c4b93084182a303`  
		Last Modified: Tue, 19 Dec 2023 07:14:10 GMT  
		Size: 12.6 MB (12565703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b80c55838b67716e63512aadd08b29d1fd4091a6557e6fe662d2e2166f28a3`  
		Last Modified: Tue, 19 Dec 2023 07:14:09 GMT  
		Size: 4.4 MB (4399222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
