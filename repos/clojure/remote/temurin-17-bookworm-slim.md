## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:df47e4d796623c01a468078f904d8eaaa6a2abbd0f6662ee1722d362dc169886
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:17f550da7767f149cd3b01da665da851af80a720ecb7a5c1ad10853ba53c0858
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.3 MB (243313258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1671c516f564d57db678d7fba29d4ede6b010d5c0f25757f96264072e4ff448`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:16:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 May 2024 02:23:41 GMT
COPY dir:d78c0cec90816231fd61ebcd7c27b07c1af0064b89c255fd2a157e0b344541d4 in /opt/java/openjdk 
# Tue, 14 May 2024 02:23:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 02:25:25 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 14 May 2024 02:25:25 GMT
WORKDIR /tmp
# Tue, 14 May 2024 02:25:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 14 May 2024 02:25:43 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 14 May 2024 02:25:44 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 14 May 2024 02:25:44 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 14 May 2024 02:25:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f139631dc7eac251e06861f977db34c9d0199c3dd88ea8e7ef5acc5855b21ce2`  
		Last Modified: Tue, 14 May 2024 02:41:10 GMT  
		Size: 145.1 MB (145095149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22a579fcb69a19a950cd867101d0928310bad3b09dd9a9f0e524ad1962e2e3b`  
		Last Modified: Tue, 14 May 2024 02:42:37 GMT  
		Size: 69.1 MB (69066686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de76f1bc0f22242bc94fa4be66505946ac9c95a6b3cb3fba4a9d1823de3cc2fe`  
		Last Modified: Tue, 14 May 2024 02:42:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d513fc9e20a498c9017d00b09c0cc84e3731de189f7a528b968f39916dce11`  
		Last Modified: Tue, 14 May 2024 02:42:29 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:856b4027e3fd2e07e90e48a676b35d8bdb464761c38235cf814da66b65314e39
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241890667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03c9c4a62e3911cded25e4c2a1272be42499a84e43d2f44fee2c4c1d311a77c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:59:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 May 2024 02:05:12 GMT
COPY dir:317487729b1812635c51c5f305bd9178bd957a141903eab756a1683874b5752b in /opt/java/openjdk 
# Tue, 14 May 2024 02:05:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 02:06:44 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 14 May 2024 02:06:44 GMT
WORKDIR /tmp
# Tue, 14 May 2024 02:06:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 14 May 2024 02:07:00 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 14 May 2024 02:07:00 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 14 May 2024 02:07:00 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 14 May 2024 02:07:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f65c66f63db4485129e4cce1c89986153e9c3b263a3466929ae8053ba04ea3d`  
		Last Modified: Tue, 14 May 2024 02:20:19 GMT  
		Size: 143.9 MB (143891868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8c6d0cbd3c14147442d2458316eba544b30de991ba479771c4d4c540596b889`  
		Last Modified: Tue, 14 May 2024 02:21:36 GMT  
		Size: 68.8 MB (68818281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3299f74b93c859ac1e9fa6cbbebe17fda1cbb6de480b3ed21bd44f6db6a988c`  
		Last Modified: Tue, 14 May 2024 02:21:28 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f73668def4a9d80019ab994921aab7295cf65615766cd9ab76d47ac57a7d3f`  
		Last Modified: Tue, 14 May 2024 02:21:28 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
