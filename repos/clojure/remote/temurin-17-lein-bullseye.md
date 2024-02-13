## `clojure:temurin-17-lein-bullseye`

```console
$ docker pull clojure@sha256:6251663de235cd195401f9e9d3a493b3031cf332dd10b9b955d62878d63bdf32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-lein-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:511b983b6a5045c1b5675d730e5e276154fea3403fdc1698469e7a892e47bd45
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.7 MB (220729377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25fff18434094ec18e2b229cb4daea57a33ecb96ebc310ba7a371f04aacd486`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:32 GMT
ADD file:1bf1a123da85382e70ea251091b98fd8b4a1972e4c4e84d392443a4e20b7a135 in / 
# Tue, 13 Feb 2024 00:37:32 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 01:59:34 GMT
COPY dir:2765b9c6732dde1d622a6314ea7119038a6031d832e1ec655de4889b7fd05a2e in /opt/java/openjdk 
# Tue, 13 Feb 2024 01:59:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 02:01:37 GMT
ENV LEIN_VERSION=2.11.1
# Tue, 13 Feb 2024 02:01:37 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Feb 2024 02:01:37 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 02:01:52 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "03b3fbf7e6fac262f88f843a87b712a2b37f39cffc4f4f384436a30d8b01d6e4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 13 Feb 2024 02:01:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Feb 2024 02:01:53 GMT
ENV LEIN_ROOT=1
# Tue, 13 Feb 2024 02:01:55 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Tue, 13 Feb 2024 02:01:55 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Tue, 13 Feb 2024 02:01:55 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Feb 2024 02:01:55 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:09e2bc8a597c33b54cccaf52f2e21798e2e0df79ab6cb33d3b1dfd4b33a57512`  
		Last Modified: Tue, 13 Feb 2024 00:42:21 GMT  
		Size: 55.1 MB (55084838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7038720c6253652e061d4b6f774aaf3955e68140b3088439919b8db57fbd91`  
		Last Modified: Tue, 13 Feb 2024 02:17:09 GMT  
		Size: 144.9 MB (144893168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa39058ce4a62156e97b4f5b007348125e9df58aca76a0abeec039517518c8d`  
		Last Modified: Tue, 13 Feb 2024 02:18:02 GMT  
		Size: 16.4 MB (16351780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3117970fcbe99e899d05ef4c604c00b437cc34a7ac724d6ee2b7fbbcece47ced`  
		Last Modified: Tue, 13 Feb 2024 02:18:01 GMT  
		Size: 4.4 MB (4399192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2092ca71f4a12199fc1927f5f1bdb5fcf13e7cade3de5ed584ecfddd3f35d5b2`  
		Last Modified: Tue, 13 Feb 2024 02:18:01 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-lein-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dcbc26e4f6adb90d85ee40b6bd65b8f752971cc2c68df80e5a5b622219e0579f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.2 MB (218182642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52c0bc997076c46626b4a34a0975696371830703327f7fda5c2381b9d8c91398`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:27 GMT
ADD file:46791e28a2eef97a17393ff5cf2928d2e721f9380340a34c7d2e85053edec7c1 in / 
# Tue, 13 Feb 2024 00:41:27 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:55:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 02:05:36 GMT
COPY dir:1e33e1b9b4d5ff1fcafcf70a5b147d046ddd08f2a0ffd21b97536e3a6e636c5f in /opt/java/openjdk 
# Tue, 13 Feb 2024 02:05:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 02:07:13 GMT
ENV LEIN_VERSION=2.11.1
# Tue, 13 Feb 2024 02:07:14 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 13 Feb 2024 02:07:14 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 02:07:27 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "03b3fbf7e6fac262f88f843a87b712a2b37f39cffc4f4f384436a30d8b01d6e4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 13 Feb 2024 02:07:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 13 Feb 2024 02:07:27 GMT
ENV LEIN_ROOT=1
# Tue, 13 Feb 2024 02:07:29 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Tue, 13 Feb 2024 02:07:29 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Tue, 13 Feb 2024 02:07:29 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Feb 2024 02:07:29 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:4245faf914201feff648b048cbaf6c46414d24a56e29e4cff1f82ac1b151d326`  
		Last Modified: Tue, 13 Feb 2024 00:45:14 GMT  
		Size: 53.7 MB (53721486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b93abada80d7a4cca39f20b2fb149ebf7e2868c862d216131fb6c28cc287e7`  
		Last Modified: Tue, 13 Feb 2024 02:21:10 GMT  
		Size: 143.7 MB (143720884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6684cb08a162da1f317d954ad0e3b253cdb2dbb0ec2360660886f2605b08d446`  
		Last Modified: Tue, 13 Feb 2024 02:22:03 GMT  
		Size: 16.3 MB (16340655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfdcc553af0c519b80907fcf10581a1d70d5b53ee24f517c87f6437b7a62325c`  
		Last Modified: Tue, 13 Feb 2024 02:22:02 GMT  
		Size: 4.4 MB (4399219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a775cdf95da5e6835307f83684b58199ff57f530cc33125d9386c6c834831352`  
		Last Modified: Tue, 13 Feb 2024 02:22:02 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
