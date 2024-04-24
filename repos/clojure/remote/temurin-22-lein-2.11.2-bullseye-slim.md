## `clojure:temurin-22-lein-2.11.2-bullseye-slim`

```console
$ docker pull clojure@sha256:091b7f0c4d036ae466baac918e09f69c8d21077f53e926be2cf5c74a065a9a0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-22-lein-2.11.2-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c7c86c8095e4ccadb4c585984157670f4f5c5a5adf0cd2270057f9f0b514589b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.6 MB (207613521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa85b6d1d5b166c544e9b83f0cfe1090f3032c881a917a4250a978b63d45e876`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 21:34:51 GMT
COPY dir:26aa9b736de249ab67b8c50e579c4c188c999c32408e8bbdcde37c30c2d0e7d3 in /opt/java/openjdk 
# Wed, 24 Apr 2024 21:34:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 21:34:53 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 24 Apr 2024 21:34:53 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Apr 2024 21:34:53 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:35:08 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 24 Apr 2024 21:35:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Apr 2024 21:35:08 GMT
ENV LEIN_ROOT=1
# Wed, 24 Apr 2024 21:35:10 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 24 Apr 2024 21:35:11 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 21:35:11 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 21:35:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086f333d7ea40659a9a5e7a8b1ae8ac89112d5aaed9f665450c7a728aeb3bf32`  
		Last Modified: Wed, 24 Apr 2024 21:56:58 GMT  
		Size: 156.7 MB (156714948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c825144544b253ba41dc424f29f5965d3043e64d134dffd84d5eac5d2256b9`  
		Last Modified: Wed, 24 Apr 2024 21:56:46 GMT  
		Size: 15.1 MB (15064739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d7e824c1d808d6c4bb411c658e6c69c6f3ff10a4bf2b18f8b9aecda0f7e87f`  
		Last Modified: Wed, 24 Apr 2024 21:56:46 GMT  
		Size: 4.4 MB (4399169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae41fe97e5061c97cfe4d0ef191c91308c46e48d4272070ec65ea4a3f6eac1e`  
		Last Modified: Wed, 24 Apr 2024 21:56:45 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-22-lein-2.11.2-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b05b72e1ffd614db19e52992251ca37dc3230d631236d10c882ce9377d2f4bff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.3 MB (204277200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce4dbab5387252ac4274bb054d1c5a23b0971199e447e84b445e7eddb32a273`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:44:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 19:17:17 GMT
COPY dir:8db4aa7d00469f3c784932412aa95caf68b05146a02559362a91df21ce463ad4 in /opt/java/openjdk 
# Wed, 24 Apr 2024 19:17:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 19:17:20 GMT
ENV LEIN_VERSION=2.11.2
# Wed, 24 Apr 2024 19:17:21 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 24 Apr 2024 19:17:21 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 19:17:34 GMT
RUN set -eux; apt-get update && apt-get install -y gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 24 Apr 2024 19:17:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Apr 2024 19:17:35 GMT
ENV LEIN_ROOT=1
# Wed, 24 Apr 2024 19:17:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 24 Apr 2024 19:17:37 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 19:17:37 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 19:17:37 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b0d6af894922630c0bf5aae1320817996daadf3bc262b667f8bff3921d8676`  
		Last Modified: Wed, 24 Apr 2024 19:36:08 GMT  
		Size: 154.7 MB (154737725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21398e4e829d5f637df1d4aa853f805f5a820c1748513d4d4c6259ca297b4547`  
		Last Modified: Wed, 24 Apr 2024 19:35:58 GMT  
		Size: 15.1 MB (15052580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f999e5d927594dd4bb0d733fd219e2c5583ec8e15055ac99abcf3694eed977`  
		Last Modified: Wed, 24 Apr 2024 19:35:58 GMT  
		Size: 4.4 MB (4399157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ecca9533e1708dbabad22fabafbccb5ce8ae37069a5214185fff0b28e5ece7`  
		Last Modified: Wed, 24 Apr 2024 19:35:57 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
