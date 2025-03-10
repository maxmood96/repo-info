## `clojure:temurin-8-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:9f945c6090986a306235d820847dec54d1efbb672d8ac60dda1ca4415ed3a428
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:acea703bcc6952f758031dc768ee0cdbd1baaab22c738159c9745d243d1368d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184190818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:918323feac6d711f2ac5fca47fc80f37aafa19410582d259d7e5903bfaa022cd`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a620bda9e83d7e83c8653abceacecfcaa2a8f57abb4940cee8d11272c9891846`  
		Last Modified: Mon, 10 Mar 2025 17:40:00 GMT  
		Size: 54.7 MB (54721234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798f930ec4ef84124070cbb0e250d09692a9ef22af104c44066d1c5d3a6fec5a`  
		Last Modified: Mon, 10 Mar 2025 17:40:00 GMT  
		Size: 81.0 MB (80992841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97d0111debc963de118b2a119b13de2ca7d26449d85128c558d2982c20c68fd`  
		Last Modified: Mon, 10 Mar 2025 17:39:58 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f99eb29a8bc254066fd4dfaf72519d2de07ea8a2acb7b1a60637a2de5187f6f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7306942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ffc5254d22269fd4a1a6c3b8116ccdfa30e355ac5c0c37f499886747402a54f`

```dockerfile
```

-	Layers:
	-	`sha256:dfd08cd2c58a6e7bce63942e138e2c21d7ac04351c781bb6bcce66c15388ec73`  
		Last Modified: Mon, 10 Mar 2025 17:39:58 GMT  
		Size: 7.3 MB (7292706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26ac9f4ddf787cf7cba906216efa69830f83f1929213a1f36ecbf02471ecdeb9`  
		Last Modified: Mon, 10 Mar 2025 17:39:58 GMT  
		Size: 14.2 KB (14236 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0a047c32f53c6bbb35e872bf38c62b8b506c3d9ecfce6665b094d77fad8b0a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (182974156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16f85fa1fe80011c8dd94b440a26f8eead2335b20834dc8aaa09814517a24379`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b0d2f3905b70af21adfac6b08366c98b606a145eef94ef8bf8cdc1e632c115`  
		Last Modified: Mon, 10 Mar 2025 17:41:47 GMT  
		Size: 53.8 MB (53822760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df1e15f1a92ca97f4753a98425c054c09ade4977d9782e607b915dc411c9cfb`  
		Last Modified: Mon, 10 Mar 2025 17:41:47 GMT  
		Size: 80.8 MB (80842741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb73853ce1ee72d4f8dd5841a192673f2c172e651f76c8818f48b160fb70ad13`  
		Last Modified: Mon, 10 Mar 2025 17:41:45 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3c979e59e4a74a9aede8adab878b1d2a0b93bb8ac50c7337f64f11f6a6fb45d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7313521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca2a8a36ecec0b6f221795e8bad396acdcdc13a2b613b44dccf77e8f6ee2f33`

```dockerfile
```

-	Layers:
	-	`sha256:59ac883de76b2dbe9e94e08063df5a0392025c183a183054e42d3e6b4b20358a`  
		Last Modified: Mon, 10 Mar 2025 17:41:45 GMT  
		Size: 7.3 MB (7299167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ec5622f1b7da9a037a2c4b29c598e04fa261bf3069914fb7fbf76c7b847fc16`  
		Last Modified: Mon, 10 Mar 2025 17:41:45 GMT  
		Size: 14.4 KB (14354 bytes)  
		MIME: application/vnd.in-toto+json
