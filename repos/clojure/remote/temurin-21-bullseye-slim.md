## `clojure:temurin-21-bullseye-slim`

```console
$ docker pull clojure@sha256:ef8913fb533a3bc350132716d028f7990c8d69335efcd234c3149e672d508263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-21-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:47f2abd1effe9638b6d5c0a362409a59ffd54c85eb505358c0f55666b785b5cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.6 MB (249631417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a12e91d79ac62cea56572793793c5f07cc54646d552705a379b8dee567e7af`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 00:00:43 GMT
COPY dir:64a8841762a9afbd2fb8b4cf497b2dee87765737d44ff0387ce1cfc51371c9a2 in /opt/java/openjdk 
# Thu, 01 Feb 2024 00:00:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 00:02:20 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 01 Feb 2024 00:02:20 GMT
WORKDIR /tmp
# Thu, 01 Feb 2024 00:02:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 01 Feb 2024 00:02:37 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 01 Feb 2024 00:02:37 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 01 Feb 2024 00:02:37 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Feb 2024 00:02:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b668cf4df59e3af807197b127df9475f34a4b40745288cac55e444f58acc501`  
		Last Modified: Thu, 01 Feb 2024 00:16:52 GMT  
		Size: 159.6 MB (159582943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d3599d7916c2bde8d5491b0c15ef8810dafd21935c0ef4e858becc8518b3ea`  
		Last Modified: Thu, 01 Feb 2024 00:18:31 GMT  
		Size: 58.6 MB (58629630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac7ae32b6bbaed9aea5d8c0632d572020123c708a8b715a8d7de116bc320940`  
		Last Modified: Thu, 01 Feb 2024 00:18:25 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bafb63586e5fad3077900e75a2dfb7cb6fffefa65cacdef8cfa00f8d1f3b395`  
		Last Modified: Thu, 01 Feb 2024 00:18:25 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-21-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2c015ec54ab7d64c77b0e19e14c11d001586dfcd408e26ddd1b1b6020ea81a97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246606398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96bc4b57d8c6806cf8c9f4401efabaca4299a6861af433febd5aef2556ae1dca`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:42 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Wed, 31 Jan 2024 22:44:42 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:21:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 06:35:27 GMT
COPY dir:ab40534e435f9942975c0e8b5454d6b7a8d69c445f8e0758c1bd9c500e157fca in /opt/java/openjdk 
# Thu, 01 Feb 2024 06:35:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:36:50 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 01 Feb 2024 06:36:50 GMT
WORKDIR /tmp
# Thu, 01 Feb 2024 06:37:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 01 Feb 2024 06:37:04 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 01 Feb 2024 06:37:04 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 01 Feb 2024 06:37:04 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Feb 2024 06:37:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7265af14829ab368e25a6f2911215d9ed78709fa3b1a9380838869f70e1c9f54`  
		Last Modified: Thu, 01 Feb 2024 06:49:54 GMT  
		Size: 157.8 MB (157784600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bf2449fd1050b6749b82830bc80e4c55829b617f0bec413a9523eae4fe8abc`  
		Last Modified: Thu, 01 Feb 2024 06:51:31 GMT  
		Size: 58.8 MB (58756446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd720ddbf0aaaae805f8f56a22e3c67a42c5a2d5bab154393b63b57486d621f7`  
		Last Modified: Thu, 01 Feb 2024 06:51:24 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2abe7582e7e6e79e0509047021aebd100e244f4b3769d3c63a4c61381d992b3`  
		Last Modified: Thu, 01 Feb 2024 06:51:24 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
