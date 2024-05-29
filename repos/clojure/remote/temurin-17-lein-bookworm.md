## `clojure:temurin-17-lein-bookworm`

```console
$ docker pull clojure@sha256:f9912c42c9976a91f0b77b62fda8ba0616ff793f092157a596072efaa07f8101
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `clojure:temurin-17-lein-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:5f9afdd1e99d56614ba868651855942b5bdf6cd60410e4afcda2a42d30108f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.4 MB (218391391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394e49c87bc00beaaf8540db0cd06b30c10f4f9c632a2757d901a705e38a1221`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 28 May 2024 15:17:11 GMT
ENV LEIN_ROOT=1
# Tue, 28 May 2024 15:17:11 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e91a4f9d017c0f436372411d797d0f74cf387fd286c548831d6a8d41209ba1`  
		Last Modified: Wed, 29 May 2024 19:57:03 GMT  
		Size: 145.1 MB (145095011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611cb378f24ab0dfb087d71a3ea193d0b779c218811edc446916abcbbde8041a`  
		Last Modified: Wed, 29 May 2024 19:57:02 GMT  
		Size: 19.3 MB (19321482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b55f0c61b41caf6c82c6006f6e8975cc14e4074c191062b86804bfca6da2a4`  
		Last Modified: Wed, 29 May 2024 19:57:01 GMT  
		Size: 4.4 MB (4398077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db03cce7aefea1a2748fc22303e544badffe2b876dce484e257c72d75788ac79`  
		Last Modified: Wed, 29 May 2024 19:57:01 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-lein-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:df81a0d3da4ad3b0200cb47e7337aa98b262aafa29859f9858dcdf80467b0b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3966655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ccb0f471f1926d4b00d969e3c43dc7fa704806eb6152831490ea2fef38c0eda`

```dockerfile
```

-	Layers:
	-	`sha256:5f07abf407dbc8fa9085c4baf0d6e8cac11bbaa14f96ba6c649edfe043e903cf`  
		Last Modified: Wed, 29 May 2024 19:57:01 GMT  
		Size: 3.9 MB (3948676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db42d26967ae606ed5fb401299dc695f30122a7038194409a5bc10626c94dc7d`  
		Last Modified: Wed, 29 May 2024 19:57:01 GMT  
		Size: 18.0 KB (17979 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-lein-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1ccdae7d23b7e56bedd8211dd906cadeef30e4a18d7ecde93b3edd40416135eb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 MB (217243385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b94de3db4d7c76c33d391a5805da9a2281faba72c11efbb36e8df0489f4e5d5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:32 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Tue, 14 May 2024 00:39:33 GMT
CMD ["bash"]
# Tue, 28 May 2024 19:43:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 19:54:30 GMT
COPY dir:317487729b1812635c51c5f305bd9178bd957a141903eab756a1683874b5752b in /opt/java/openjdk 
# Tue, 28 May 2024 19:54:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 19:54:34 GMT
ENV LEIN_VERSION=2.11.2
# Tue, 28 May 2024 19:54:34 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 28 May 2024 19:54:34 GMT
WORKDIR /tmp
# Tue, 28 May 2024 19:54:48 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "28a1a62668c5f427b413a8677e376affaa995f023b1fcd06e2d4c98ac1df5f3e *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 9D13D9426A0814B3373CF5E3D8A8243577A7859F && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mkdir -p /root/.lein && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Tue, 28 May 2024 19:54:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 28 May 2024 19:54:49 GMT
ENV LEIN_ROOT=1
# Tue, 28 May 2024 19:54:50 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.3"]])' > project.clj   && lein deps && rm project.clj
# Tue, 28 May 2024 19:54:51 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Tue, 28 May 2024 19:54:51 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 19:54:51 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d0a7ab35eca8753def28d2c15916fa2d25792099a1b4427f44564e27bdb212`  
		Last Modified: Tue, 28 May 2024 20:14:35 GMT  
		Size: 143.9 MB (143891866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a376ce96cb4d8428e4fab6f9125d1db948a7f2ea0c2750dd57ce68d85ed40c18`  
		Last Modified: Tue, 28 May 2024 20:14:27 GMT  
		Size: 19.3 MB (19339635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb410a2079828c93f9b1990e74214167196df26868b59d460f62ff61eaef19d2`  
		Last Modified: Tue, 28 May 2024 20:14:26 GMT  
		Size: 4.4 MB (4398095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7abca54d88e0f8a55cfcacb899320081ff2f63499e7faff7bf02e8cbb85d1d`  
		Last Modified: Tue, 28 May 2024 20:14:26 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
