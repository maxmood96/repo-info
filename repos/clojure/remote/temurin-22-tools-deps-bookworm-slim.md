## `clojure:temurin-22-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:02bfc809f50a7dce5d4b008d3e226f1d36b1ef1aabe8d1c0f50662af51ffb180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-22-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9c147afefe5c3acc7a2b7fb379d14a3c220c5bbfe0116f26e1c63a48f226210a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.9 MB (254932903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ceb4fb038d83e7f0191a90f2bad3358f28636d37cc1854edb8efcfcc6355646`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:03 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 14 May 2024 01:28:04 GMT
CMD ["bash"]
# Tue, 28 May 2024 21:21:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 21:42:58 GMT
COPY dir:26aa9b736de249ab67b8c50e579c4c188c999c32408e8bbdcde37c30c2d0e7d3 in /opt/java/openjdk 
# Tue, 28 May 2024 21:43:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 21:45:23 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 21:45:23 GMT
WORKDIR /tmp
# Tue, 28 May 2024 21:45:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 28 May 2024 21:45:42 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 28 May 2024 21:45:42 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 28 May 2024 21:45:42 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 21:45:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14e41f3a6982bbc491d8ad8df2f57d34f510b2164888a7ef95f1247a4b6ce77`  
		Last Modified: Tue, 28 May 2024 22:05:08 GMT  
		Size: 156.7 MB (156714925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69acc56f3147f66f7a40abb7f740955b70216cb3c191bb34eb2264a806d41c6`  
		Last Modified: Tue, 28 May 2024 22:06:51 GMT  
		Size: 69.1 MB (69066549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aedfbf4b149cae3e6fbc2c732173a12604b0bc5436db74906d666b195221108c`  
		Last Modified: Tue, 28 May 2024 22:06:43 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e8334ce38b45b0ee9e5d1f633d1216f7e453534ca3b67d01afc9595248173e`  
		Last Modified: Tue, 28 May 2024 22:06:43 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-22-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e9ab38f71e0700526de17ada914d6732f40796ff17b3201586f0e0738da40cce
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252736563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d153c90fb102db4f15a8f1658ea60681510390ebfcec5bdbc2f3e99bb918298`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:40 GMT
ADD file:e23ba17afc7850bcca9e73ba5022db9f0a80c6a0250585fd3f50a1960226474b in / 
# Tue, 14 May 2024 00:39:41 GMT
CMD ["bash"]
# Tue, 28 May 2024 19:44:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 20:02:15 GMT
COPY dir:8db4aa7d00469f3c784932412aa95caf68b05146a02559362a91df21ce463ad4 in /opt/java/openjdk 
# Tue, 28 May 2024 20:02:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 20:04:24 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 20:04:24 GMT
WORKDIR /tmp
# Tue, 28 May 2024 20:04:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 28 May 2024 20:04:40 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 28 May 2024 20:04:40 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 28 May 2024 20:04:40 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 20:04:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:24c63b8dcb66721062f32b893ef1027404afddd62aade87f3f39a3a6e70a74d0`  
		Last Modified: Tue, 14 May 2024 00:42:56 GMT  
		Size: 29.2 MB (29179503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0d69f3d78e64bd747e1c78e304dba8ab3618928d50e632af98143081a1774b`  
		Last Modified: Tue, 28 May 2024 20:21:56 GMT  
		Size: 154.7 MB (154737693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a8935c09c56ed1f5efe44f0ca7fb12a4e2e4be79a69d7a3ebf2afe22a617bb9`  
		Last Modified: Tue, 28 May 2024 20:23:21 GMT  
		Size: 68.8 MB (68818352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75bde09ab23f12a6c627b44611a692efe0ac2b6d14dbe5bbdcb723d306d148ac`  
		Last Modified: Tue, 28 May 2024 20:23:13 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e051a1be10d6861b8fc7bf690a2425cc754562a17a25ac573ea5ca3eeffa5868`  
		Last Modified: Tue, 28 May 2024 20:23:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
