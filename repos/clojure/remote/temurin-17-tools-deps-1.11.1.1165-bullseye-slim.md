## `clojure:temurin-17-tools-deps-1.11.1.1165-bullseye-slim`

```console
$ docker pull clojure@sha256:ac72cc56e5a8f468f0c4dfb60f4e8918d429fb40395d9dcd6c4ef5ac35378cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.1.1165-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:19522026c89fd1c2b18f60accef92d51a919f0fcd4f40d77099a2f0ee0f35122
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.0 MB (285029244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98cd1d0a5427343d4a9ff0037dc51f0cb711596f710cf67451a3657ef6cc810a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 03:56:40 GMT
COPY dir:09afbf947759009c57336c17f70cd71239c5d8b0170793151aec66483cdd0976 in /opt/java/openjdk 
# Thu, 06 Oct 2022 03:56:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 03:59:38 GMT
ENV CLOJURE_VERSION=1.11.1.1165
# Thu, 06 Oct 2022 03:59:38 GMT
WORKDIR /tmp
# Thu, 06 Oct 2022 03:59:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "72d662bdc99b79037f9e34996272384de35e01e0416d8eb79cc940ee0f0fc808 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 06 Oct 2022 03:59:55 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 06 Oct 2022 03:59:55 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 06 Oct 2022 03:59:55 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 06 Oct 2022 03:59:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef3d95ee3a8969f154e4e82981119ffbe3fb6d2183d260566ed8ba03b8fc6f8`  
		Last Modified: Thu, 06 Oct 2022 04:12:33 GMT  
		Size: 192.1 MB (192137622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3316d3c6c2db7fe516e0e5038b4bde3b4d227527ec57a8ce46581cbbf62b320`  
		Last Modified: Thu, 06 Oct 2022 04:14:55 GMT  
		Size: 61.5 MB (61470501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5a6da6d1c866cebb2001d55274033238f979900fcc1c9523f344a51f1285644`  
		Last Modified: Thu, 06 Oct 2022 04:14:47 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb7313c2645794e5229e2a4f271a124f18a724df501831e07d5ee1ff9bc3efd`  
		Last Modified: Thu, 06 Oct 2022 04:14:47 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-1.11.1.1165-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c5bda424d1d5a50290c3d2b7efe15d2c7583ab37ac455f017cc9c4444858cc3a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.4 MB (282362411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80bc80d3bc9ad4f6644fb25c23bd8692aba9bd691b00e4aa6148d87352b7cdf2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 06 Oct 2022 02:39:47 GMT
COPY dir:dc2bc1e50ab42c5231433386b6bc2a9cff04b310112464fb4909efc66be10627 in /opt/java/openjdk 
# Thu, 06 Oct 2022 02:39:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Oct 2022 02:44:05 GMT
ENV CLOJURE_VERSION=1.11.1.1165
# Thu, 06 Oct 2022 02:44:06 GMT
WORKDIR /tmp
# Thu, 06 Oct 2022 02:44:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "72d662bdc99b79037f9e34996272384de35e01e0416d8eb79cc940ee0f0fc808 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 06 Oct 2022 02:44:25 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 06 Oct 2022 02:44:26 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 06 Oct 2022 02:44:26 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 06 Oct 2022 02:44:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd853b0df38079bcf0a5945a7e8ed2935d92b2270210148614164b9ddd8b48b`  
		Last Modified: Thu, 06 Oct 2022 03:01:36 GMT  
		Size: 190.9 MB (190904238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc13514022eac274f2f85103b0a2af35b9f7776fb07ca9922559e4054a396af`  
		Last Modified: Thu, 06 Oct 2022 03:04:25 GMT  
		Size: 61.4 MB (61392760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:856051b37fa385e628efe641d0b6a2b2bab84c8dace4ee209306f16b5727c6b1`  
		Last Modified: Thu, 06 Oct 2022 03:04:17 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8966d90a373ea2b908a963fff166830c86ab7479d19e997ad8755ba8f1a218d8`  
		Last Modified: Thu, 06 Oct 2022 03:04:16 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
