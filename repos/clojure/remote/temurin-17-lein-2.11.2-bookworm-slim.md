## `clojure:temurin-17-lein-2.11.2-bookworm-slim`

```console
$ docker pull clojure@sha256:417f0f4c0b8c04447187fc24279147fea53e1bd69db75e0cbc039f434e368198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-lein-2.11.2-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:875000e7f42a4b18d000d05e53855239a57259b19d05a39d2b6887c4e2019f0a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 MB (195901902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a992c113fc67743d167e94f2338cfa30c6bedc4b13d02d1c6bc42247b8cb035`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:11:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 03:06:45 GMT
COPY dir:88c5118aff6896f6ed535dcde576d68ef88ded459cca013e0f9beb3e430ebb52 in /opt/java/openjdk 
# Thu, 28 Mar 2024 03:06:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 03:09:53 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 28 Mar 2024 03:09:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 03:09:53 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 03:10:08 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 28 Mar 2024 03:10:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 03:10:08 GMT
ENV LEIN_ROOT=1
# Thu, 28 Mar 2024 03:10:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 28 Mar 2024 03:10:11 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Thu, 28 Mar 2024 03:10:11 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 28 Mar 2024 03:10:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db34d09da7ef0b7c10d1180bf5afb0a7cc04cfc2fef22a109260b226f6f0804c`  
		Last Modified: Thu, 28 Mar 2024 03:24:38 GMT  
		Size: 144.9 MB (144893128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8009189df857b461aad4755a64c58a15d3224ce7ff08edc1e420aa03e98aceb4`  
		Last Modified: Thu, 28 Mar 2024 03:26:15 GMT  
		Size: 17.5 MB (17485021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2959a77ee2336e20d8e6b197b421b938847614f04287fc7b3b02e2e46404cf`  
		Last Modified: Thu, 28 Mar 2024 03:26:14 GMT  
		Size: 4.4 MB (4399171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d807c7087bab003965d99768d263cfe1ae898cf45c792d1e5959d6306c10aec`  
		Last Modified: Thu, 28 Mar 2024 03:26:13 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-lein-2.11.2-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:96171ec1679992be310b66c292730aa38e7d64b5d190df4900893a5153bfa315
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194586214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6318ed4da3d1f6b7f12efd5470470057289d1e4fd31fabfcef31e682da5aa224`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:44:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 02:39:31 GMT
COPY dir:a5d0039514ccd79689a0ea6094d70ca92113e8cbcc38d473b7c0fcc04a1f496a in /opt/java/openjdk 
# Thu, 28 Mar 2024 02:39:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 02:42:01 GMT
ENV LEIN_VERSION=2.11.2
# Thu, 28 Mar 2024 02:42:01 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 02:42:01 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 02:42:15 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Thu, 28 Mar 2024 02:42:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 02:42:15 GMT
ENV LEIN_ROOT=1
# Thu, 28 Mar 2024 02:42:17 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Thu, 28 Mar 2024 02:42:17 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Thu, 28 Mar 2024 02:42:17 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 28 Mar 2024 02:42:17 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76dbb1a530d50bcec96fcd7bbb7abc3fb7a765a01bdf5b5dd96e07107640e6b8`  
		Last Modified: Thu, 28 Mar 2024 02:54:00 GMT  
		Size: 143.7 MB (143720921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01361b9b40879e21203a57f735a363992a924bcce82ccc39b1c2d95b4a1bd75`  
		Last Modified: Thu, 28 Mar 2024 02:55:21 GMT  
		Size: 17.3 MB (17309246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330dcc08501961ab9670b9c4f36b24fc642a545b786cc32f797057322b10e24e`  
		Last Modified: Thu, 28 Mar 2024 02:55:20 GMT  
		Size: 4.4 MB (4399211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a14cd5a89a44b60be30647319b030dd50e8a5fceb5e8a6ab5f0510fb95a81e`  
		Last Modified: Thu, 28 Mar 2024 02:55:19 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
