## `clojure:temurin-8-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:3001dc9a82fdb78948a530f7a0fb1fd77fb3e29c2d2351ca510d1f3e2e8a62e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:126caafaf61c993f297bed3382c9f15d59ac983d3ea51b2c4334507e13e38aed
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227722789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a298b2a5c02a5ab63e21d60de6e32fb2c1130a4e6d749721fa6fb7dda9a0c39f`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 01:28:14 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 14 May 2024 01:28:14 GMT
CMD ["bash"]
# Tue, 28 May 2024 21:21:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 21:21:59 GMT
COPY dir:54f5f76f9b290ecbafc047cf196165b69f1cb32e49c8748c35e250f5e316fcc0 in /opt/java/openjdk 
# Tue, 28 May 2024 21:22:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 21:24:49 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 21:24:49 GMT
WORKDIR /tmp
# Tue, 28 May 2024 21:25:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 28 May 2024 21:25:11 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 28 May 2024 21:25:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a994756e2bcc85e9592f03390cf7ac4885fe8bceda768359da23044921c9699d`  
		Last Modified: Tue, 28 May 2024 21:49:47 GMT  
		Size: 103.6 MB (103600110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8f131c389776efe61c4f37ae14a544239d9fa875acc3160242df115528a601`  
		Last Modified: Tue, 28 May 2024 21:51:31 GMT  
		Size: 69.0 MB (69022662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d89352749c1e91a3b985959367bba543ee4f9f0e592bf5835cf9587dc6fd76`  
		Last Modified: Tue, 28 May 2024 21:51:23 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9b59786c165896398a2c370115aaf023dc1c60f9773b3010ed7254602d0e9411
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.6 MB (225577453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06479a9236a9fbb850f6b4509cf7add08b70926b3e5f1f0bf4b3eb03edd9a886`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 00:39:47 GMT
ADD file:43721c605da3f74f0c3f71384780fc0e57e2478b88197672caaf4baa3eddab23 in / 
# Tue, 14 May 2024 00:39:48 GMT
CMD ["bash"]
# Tue, 28 May 2024 19:44:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 19:44:54 GMT
COPY dir:f816a852ac21a5e29532918ac40e44b27f618ca8c5c539e334f114f460fe4b51 in /opt/java/openjdk 
# Tue, 28 May 2024 19:44:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 19:47:54 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 19:47:54 GMT
WORKDIR /tmp
# Tue, 28 May 2024 19:48:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 28 May 2024 19:48:11 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 28 May 2024 19:48:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:078d9526cc72763b2db16388f6b511c18a73e3e7f9d229364b3b85a6b5277bc8`  
		Last Modified: Tue, 14 May 2024 00:43:13 GMT  
		Size: 53.7 MB (53738990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e844c65ceb9c225912fa63d86b8984a4857ab0b02e6946162ed47cb3974aa95a`  
		Last Modified: Tue, 28 May 2024 20:08:12 GMT  
		Size: 102.7 MB (102700129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7281679cc8e1db84e070ff0171ad3880e54928ec1ec35f4ad02381aae53af9a`  
		Last Modified: Tue, 28 May 2024 20:09:54 GMT  
		Size: 69.1 MB (69137716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a6e014bf1029e0240a71e89475be5c2766a2bbd5ce80315d8125e9ab4930c1`  
		Last Modified: Tue, 28 May 2024 20:09:45 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
