## `clojure:temurin-20-tools-deps-1.11.1.1413-bullseye-slim`

```console
$ docker pull clojure@sha256:16b769b9ada145b138291cfb5e565d081e81a9acfe3c034ccdca341623d8fcea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-20-tools-deps-1.11.1.1413-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c472ec41057890fb5af1cb1d9063e6a4b7f7bf6bc1aba2ebdfb27c09f1c8942f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246704725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6dd19a627da14925031b62e7530151c4c79ecd397ff6fffcdbe4c2d19f7ac57`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:22:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 Sep 2023 07:31:08 GMT
COPY dir:6a540db71f2a37db361084aee8addd6817cd7c4f18237e6f852a38e98bdb4182 in /opt/java/openjdk 
# Wed, 20 Sep 2023 07:31:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 07:31:56 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Wed, 20 Sep 2023 07:31:56 GMT
WORKDIR /tmp
# Wed, 20 Sep 2023 07:32:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 20 Sep 2023 07:32:13 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 20 Sep 2023 07:32:13 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 20 Sep 2023 07:32:13 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 Sep 2023 07:32:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54609089935fe1ea947dcddf61947fe2eb3d029159a79ff7091d0d6c63ca4682`  
		Last Modified: Wed, 20 Sep 2023 07:39:30 GMT  
		Size: 153.8 MB (153791726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4485253ef148a307e53e1c3e6745251e527a196585fd20465ab7f477825f310b`  
		Last Modified: Wed, 20 Sep 2023 07:40:06 GMT  
		Size: 61.5 MB (61494276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93466e930bb6540ff60fd962ea3545790a3ac59fb63927d0a1ea03fe8d623e1b`  
		Last Modified: Wed, 20 Sep 2023 07:39:59 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ae95fcef2300ef58f6f98050c6e3b6f4fcc97b2d8bd5d8b80ea36b9ddc0ba3`  
		Last Modified: Wed, 20 Sep 2023 07:39:59 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-20-tools-deps-1.11.1.1413-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fcec17686bfa9d522892625709f69818fc7dd4e363e6685524660fe2244a2e8a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243795192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74be85e41e613089102b454051a086119d3ff3075b08bb16e3d7afbf7bd47618`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:53 GMT
ADD file:abd1ad48ae3ebec7a6ecc8ce3016c25be2afcbaedfcb904bc89b1ce59400aef0 in / 
# Thu, 07 Sep 2023 00:39:54 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 06:46:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 Sep 2023 09:12:11 GMT
COPY dir:d35c6357dd030960bb6081f48b2bc10afb3da11efc1525ff916214b03be70ddf in /opt/java/openjdk 
# Thu, 07 Sep 2023 09:12:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 09:12:54 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Thu, 07 Sep 2023 09:12:54 GMT
WORKDIR /tmp
# Thu, 07 Sep 2023 09:13:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 07 Sep 2023 09:13:09 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 07 Sep 2023 09:13:09 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 07 Sep 2023 09:13:09 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 07 Sep 2023 09:13:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f96ab15157043879c2ff23e0556e798eba6a6ff3d7fd5d1384de223bb9f66f1d`  
		Last Modified: Thu, 07 Sep 2023 00:43:41 GMT  
		Size: 30.1 MB (30062903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cafa72c7ae14770a22f427e0e8f845d7d272129d4cdc17983ea6e3a5a747cab`  
		Last Modified: Thu, 07 Sep 2023 09:19:28 GMT  
		Size: 152.1 MB (152120058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62226970eb71aaf6eb7817c2ee7cd44d7ce2530c829f142054d291d48e423dac`  
		Last Modified: Thu, 07 Sep 2023 09:20:05 GMT  
		Size: 61.6 MB (61611215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7cbe5cfbe682fad33417fdb9f53235059c19bb396f7870de56ef2b5d338860`  
		Last Modified: Thu, 07 Sep 2023 09:19:59 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c238abad4ce2faf116eb0f8ff5ad6ed3a47625a3091358cd5bfc3be62565832b`  
		Last Modified: Thu, 07 Sep 2023 09:19:59 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
