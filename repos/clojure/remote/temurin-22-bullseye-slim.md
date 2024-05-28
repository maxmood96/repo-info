## `clojure:temurin-22-bullseye-slim`

```console
$ docker pull clojure@sha256:abbec3d360ed70dee89faebeed62131e26496a584bbf8c1ea9ca697dad344c75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-22-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8e298c6d2a87d1e227db97c29da32d49d2b665954dc8d247ea96246761713647
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.8 MB (246776672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a9ab6326fad0f0b08f21e1f6688c03a0ee5e56504cd73ac4721f9ef741b0fd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
CMD ["bash"]
# Tue, 28 May 2024 21:22:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 21:43:57 GMT
COPY dir:26aa9b736de249ab67b8c50e579c4c188c999c32408e8bbdcde37c30c2d0e7d3 in /opt/java/openjdk 
# Tue, 28 May 2024 21:43:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 21:46:12 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 21:46:12 GMT
WORKDIR /tmp
# Tue, 28 May 2024 21:46:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 28 May 2024 21:46:30 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 28 May 2024 21:46:30 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 28 May 2024 21:46:30 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 21:46:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01710f433932007e4f0503c5a6457a281f080bcace9cb82c7b6dff77761855df`  
		Last Modified: Tue, 28 May 2024 22:05:49 GMT  
		Size: 156.7 MB (156714933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca4ca10395e0e4fa3f1e76678e5d745a795f980d2eebf29a8ef93bda33d4ab0`  
		Last Modified: Tue, 28 May 2024 22:07:27 GMT  
		Size: 58.6 MB (58626791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e228effaac87bfe8434ab9850a4d2f851f80f086aa36bf7f2841398ed2c94e4`  
		Last Modified: Tue, 28 May 2024 22:07:20 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f4bd220fb2bbaad08eed7fc906fb0b19e7e6d450264484fefe16b2d9119a52`  
		Last Modified: Tue, 28 May 2024 22:07:20 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-22-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:281dc8f4e23cc448e893e20195b2c240e5be5f96b2c9ef60aa5f0b7f21b809e1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243573706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff8152e5fb96f8e726bc9b4ec58d6ebaf2768c1086aca1795ec525b1ef6e5e8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Tue, 28 May 2024 19:45:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 20:03:07 GMT
COPY dir:8db4aa7d00469f3c784932412aa95caf68b05146a02559362a91df21ce463ad4 in /opt/java/openjdk 
# Tue, 28 May 2024 20:03:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 20:05:03 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 20:05:03 GMT
WORKDIR /tmp
# Tue, 28 May 2024 20:05:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 28 May 2024 20:05:18 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 28 May 2024 20:05:18 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 28 May 2024 20:05:18 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 20:05:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a13a65c57016b28359f586eff3a4b25400f9c7f0f0debe3ae646a1af81eced9`  
		Last Modified: Tue, 28 May 2024 20:22:33 GMT  
		Size: 154.7 MB (154737731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aacfee50a6bf727307a8d7c98e2e8555c7f4be08cb67af8c3050740895dc6482`  
		Last Modified: Tue, 28 May 2024 20:23:55 GMT  
		Size: 58.7 MB (58748051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf2a36a01b5badd8ac2ecaee096735d7f6bc92f263386a51641952492ed26df`  
		Last Modified: Tue, 28 May 2024 20:23:49 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2149848655306f415d5a85b92d5f5a1d8815ed6d292bb3ffa949944f025094c9`  
		Last Modified: Tue, 28 May 2024 20:23:49 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
