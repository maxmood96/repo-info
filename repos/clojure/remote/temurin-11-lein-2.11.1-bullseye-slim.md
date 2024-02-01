## `clojure:temurin-11-lein-2.11.1-bullseye-slim`

```console
$ docker pull clojure@sha256:f7ead4a84b41c7bdc803e4474f1868b9d024ce37404b1ebcb52809473b32a127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-lein-2.11.1-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c584903c5cc812a30647928873dc15073c7e3a662e18b99fe55750881e720b83
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196151447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c916b4fde0d791b414421893c1450c100f59c5f4c04b5eea9828bde89c153db`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 23:50:14 GMT
COPY dir:e1ce96bca1c423a1c79b84eacb7ae69429353a37485cc24af4161ce4b9d3ee2a in /opt/java/openjdk 
# Wed, 31 Jan 2024 23:50:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:51:59 GMT
ENV LEIN_VERSION=2.11.1
# Wed, 31 Jan 2024 23:51:59 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 31 Jan 2024 23:52:00 GMT
WORKDIR /tmp
# Wed, 31 Jan 2024 23:52:14 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "03b3fbf7e6fac262f88f843a87b712a2b37f39cffc4f4f384436a30d8b01d6e4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 31 Jan 2024 23:52:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 31 Jan 2024 23:52:15 GMT
ENV LEIN_ROOT=1
# Wed, 31 Jan 2024 23:52:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 31 Jan 2024 23:52:17 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237cb6d9dedd71662d3dfef2792a61299af8d4b495bbb2a1e8f51c6f89c22ddd`  
		Last Modified: Thu, 01 Feb 2024 00:09:34 GMT  
		Size: 145.3 MB (145270936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b2b19eb58919532ca2ebc0765fb9eb10586b9258bf016e485cd8a13e984907`  
		Last Modified: Thu, 01 Feb 2024 00:10:18 GMT  
		Size: 15.1 MB (15063493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2676c27be9dd1da0d13e3e7e5c27582e5dc3bb19202835f6ed3ec37bad1f762`  
		Last Modified: Thu, 01 Feb 2024 00:10:18 GMT  
		Size: 4.4 MB (4399191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-lein-2.11.1-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ba4d79cdd0edde74f1863ee9bde603a6dc81a2171adfb2c3ca48eac0a4094702
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191521033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:660c882b6a8681daf3a14451101390de120939f9473d53819f63b4ff68f42462`
-	Default Command: `["lein","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:42 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Wed, 31 Jan 2024 22:44:42 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:21:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 06:26:11 GMT
COPY dir:454699b64b949edd3264b234e72a891ace37d538f2726c5ec754e17e6fb3fb19 in /opt/java/openjdk 
# Thu, 01 Feb 2024 06:26:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:27:45 GMT
ENV LEIN_VERSION=2.11.1
# Thu, 01 Feb 2024 06:27:45 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 01 Feb 2024 06:27:46 GMT
WORKDIR /tmp
# Thu, 01 Feb 2024 06:27:59 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "03b3fbf7e6fac262f88f843a87b712a2b37f39cffc4f4f384436a30d8b01d6e4 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 01 Feb 2024 06:27:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 01 Feb 2024 06:27:59 GMT
ENV LEIN_ROOT=1
# Thu, 01 Feb 2024 06:28:01 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 01 Feb 2024 06:28:01 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eddf8729def8f436a94b509a37f4bf17c7819ac995ef5769ed48da7ddd3b0b64`  
		Last Modified: Thu, 01 Feb 2024 06:43:10 GMT  
		Size: 142.0 MB (142006498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811f4021e67e318c7c990192efed98ac67fb050e1ad7aad9a7f5f533a748d1ae`  
		Last Modified: Thu, 01 Feb 2024 06:43:50 GMT  
		Size: 15.1 MB (15050997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:745b16d9b6f2c017e2ea799c7bc104295ba337dc207517b7ecd125f167e1e72a`  
		Last Modified: Thu, 01 Feb 2024 06:43:49 GMT  
		Size: 4.4 MB (4399204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
