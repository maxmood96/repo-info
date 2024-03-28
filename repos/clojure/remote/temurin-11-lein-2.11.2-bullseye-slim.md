## `clojure:temurin-11-lein-2.11.2-bullseye-slim`

```console
$ docker pull clojure@sha256:5e5344b7310392878e18f46b578b7b7a95bccfa807f2ed22bc07843adc099d6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-lein-2.11.2-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e26c11ad50f1ec1b018ace05253a5775d68e1b3561673041d4be2b766e3e98d8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196156442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e79335d633a09e14f597d4325cfa26e151c5b45aae95083a22930cd287bb315d`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:12:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 02:59:44 GMT
COPY dir:4cef005a87cd4606dd69ccb04c755a46f4aa2c925fb1aacc59928d64687208f2 in /opt/java/openjdk 
# Thu, 28 Mar 2024 02:59:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 03:02:44 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 28 Mar 2024 03:02:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 03:02:45 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 03:02:59 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 28 Mar 2024 03:03:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 03:03:00 GMT
ENV LEIN_ROOT=1
# Thu, 28 Mar 2024 03:03:02 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 28 Mar 2024 03:03:02 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765e80b34419cc4d75a074af22d808e72a16040aef302be6b97f83f87c3cea68`  
		Last Modified: Thu, 28 Mar 2024 03:20:12 GMT  
		Size: 145.3 MB (145271223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d6749045533d4e8a5315d0b04ac6cfd1b9e582271c6129f7250227e85c209e4`  
		Last Modified: Thu, 28 Mar 2024 03:21:31 GMT  
		Size: 15.1 MB (15063526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac96dcc4e50590d7702ca106fcfa6708bb5e8ef3b355ae062635cd47c54fc378`  
		Last Modified: Thu, 28 Mar 2024 03:21:31 GMT  
		Size: 4.4 MB (4399204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-lein-2.11.2-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:970e83f3020099ccea8ba0337c14f637ae97f9155774195d832b626fa43cffae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191527728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09cb2d95462afd94d00b6d3289ee66ecf074bb18259a7f835a13f2439ec4e6d5`
-	Default Command: `["lein","repl"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:45:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 02:33:52 GMT
COPY dir:d5fb8d9a38dea7496f2aff176bc9a34bbca80551c2dc57109d2dae5907a339ee in /opt/java/openjdk 
# Thu, 28 Mar 2024 02:33:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 02:36:09 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 28 Mar 2024 02:36:09 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 02:36:09 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 02:36:23 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 28 Mar 2024 02:36:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 02:36:23 GMT
ENV LEIN_ROOT=1
# Thu, 28 Mar 2024 02:36:25 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 28 Mar 2024 02:36:25 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff8a31a2022acad9a6b7593ce2e2b45a1ce4aeb662d6311f16bc5d6ea9a4339`  
		Last Modified: Thu, 28 Mar 2024 02:50:17 GMT  
		Size: 142.0 MB (142006322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8fe85aa4d705cba9584c29148aa697a735a5667f59a1b21d43922605753245`  
		Last Modified: Thu, 28 Mar 2024 02:51:22 GMT  
		Size: 15.1 MB (15051133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a371c6ad82f19b1e23844851671f79e22afda6128c4116e7299c95c09e686f`  
		Last Modified: Thu, 28 Mar 2024 02:51:22 GMT  
		Size: 4.4 MB (4399157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
