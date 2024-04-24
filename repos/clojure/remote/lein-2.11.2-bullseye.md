## `clojure:lein-2.11.2-bullseye`

```console
$ docker pull clojure@sha256:9cb1dd53824d342b016d4751b6184add46a371658c30bca29127ef4088781407
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:lein-2.11.2-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:ded565eaeca113a44198f073d332c766231630cdf7d3b1ea36978dad4c09a1fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.4 MB (234351698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aacca8c2a57c5f56910e46d5fbd03f09cd51d7456b181765df062606a18ec9be`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 21:29:47 GMT
COPY dir:2191d32deb04bfc59d7fcf2244f16c5ecbe60498375dcea5599e5d16a61b7305 in /opt/java/openjdk 
# Wed, 24 Apr 2024 21:29:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 21:29:49 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 24 Apr 2024 21:29:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Apr 2024 21:29:49 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:30:04 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 24 Apr 2024 21:30:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Apr 2024 21:30:05 GMT
ENV LEIN_ROOT=1
# Wed, 24 Apr 2024 21:30:07 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 24 Apr 2024 21:30:07 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 21:30:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 21:30:07 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d9385d4608e531503b27c9f1751bf5d9d34e1278318925ecd583df6963dd5a`  
		Last Modified: Wed, 24 Apr 2024 21:52:38 GMT  
		Size: 158.5 MB (158498231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0fad91fb8bdcc8a91b39a883792a7b8403198c4e80fcd6342211bb7d3617fc7`  
		Last Modified: Wed, 24 Apr 2024 21:52:27 GMT  
		Size: 16.4 MB (16354974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c62e82711b2fc56114989335784e989b8ef48952d81a83f78f1fa785fc1a13`  
		Last Modified: Wed, 24 Apr 2024 21:52:26 GMT  
		Size: 4.4 MB (4399223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f085daa77613918f809162d9b97b4d1f773b059b82f1bf0e1a306d179373040`  
		Last Modified: Wed, 24 Apr 2024 21:52:25 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:lein-2.11.2-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6ab4bdc6bca5ac957823d51ebca2e320abece450ad7b367d1aa46e957995032d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231149005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80079d9d1cba63cd62269c319e1c788ece0e5985dcef79672996776280946ece`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:46 GMT
ADD file:3ebbb50438ec23ebe0c880a5421d505922771b7bd4202b5c8f839702dd726036 in / 
# Wed, 24 Apr 2024 04:10:46 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:44:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 19:13:14 GMT
COPY dir:96a90c8e1c03defb238a6d560d8927dc81a1a58af3fce1471cbce5249ed27f38 in /opt/java/openjdk 
# Wed, 24 Apr 2024 19:13:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 19:13:18 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 24 Apr 2024 19:13:18 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Apr 2024 19:13:18 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 19:13:32 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 24 Apr 2024 19:13:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Apr 2024 19:13:33 GMT
ENV LEIN_ROOT=1
# Wed, 24 Apr 2024 19:13:35 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 24 Apr 2024 19:13:35 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 19:13:35 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 19:13:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:64d502aff46d2ed56e6228994304818b354d02b13d6122492c5d3e0886c92897`  
		Last Modified: Wed, 24 Apr 2024 04:14:26 GMT  
		Size: 53.7 MB (53739959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7477453a8f7ede5b3451af062fdfd3ed3ce2cfea8195773533d15844f17ea0e9`  
		Last Modified: Wed, 24 Apr 2024 19:32:22 GMT  
		Size: 156.7 MB (156665520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2d61b02795ec6ea853d613d45f048be7850bb717782a327fd93359c78dd6f1`  
		Last Modified: Wed, 24 Apr 2024 19:32:16 GMT  
		Size: 16.3 MB (16343963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b1a24590f00c4f8791a948bd5d56dfd3856102775edad38f140974b31ceef3`  
		Last Modified: Wed, 24 Apr 2024 19:32:13 GMT  
		Size: 4.4 MB (4399162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96dc430ce0c5bc82d7a402540f4f0895e81592989760f26dd7c73943a52e139`  
		Last Modified: Wed, 24 Apr 2024 19:32:12 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
