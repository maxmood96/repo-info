## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:040a2dce130e85231dae1b12b09751b59fd4be79e5664fc45651e39ba469d1b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8b94f8735803c8a3e6a829567f7a527b97d6f40d49e9e094aa7df785894ff86b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.3 MB (235319258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:badcd12e390bba166baea5bbedc6e367ffdddc0bd06667a791ce097f394a5a88`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:48:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 14:03:14 GMT
COPY dir:9807503b62b5ec57f5790350ba2323b4402a31264d57970336b28a606d7a3a68 in /opt/java/openjdk 
# Wed, 06 Mar 2024 14:03:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 14:08:42 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 06 Mar 2024 14:08:43 GMT
WORKDIR /tmp
# Wed, 06 Mar 2024 14:09:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 06 Mar 2024 14:09:00 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 06 Mar 2024 14:09:00 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b81ae9e98f49cc29c0ab057f1252129d8ce2d72eb0e68b0cc28dea6a0f9685dd`  
		Last Modified: Wed, 06 Mar 2024 14:23:57 GMT  
		Size: 145.3 MB (145271155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbb9823c582eb5653573a5eb0ae79fbe1587d69d8fc54fc3c3f9dfec1659e98`  
		Last Modified: Wed, 06 Mar 2024 14:26:57 GMT  
		Size: 58.6 MB (58625062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1df413a0806e4fc72b245b3334ac1938e0ad18c4912d804e8db5ee3a3ae2c62`  
		Last Modified: Wed, 06 Mar 2024 14:26:50 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ef0fb753d42b105aef29bbf58bda17c5dbf334c6dd4d9a799eafce5353625aa3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230831249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2058e64f7e83de381c4e6c29b14df9b4e56815f927daadc51ed9e58c2a7387d6`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:56:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 13:17:20 GMT
COPY dir:774c748cac67d918432726696917d770e1c557a90a62f56899a68f5b5861f304 in /opt/java/openjdk 
# Wed, 06 Mar 2024 13:17:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 13:21:54 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 06 Mar 2024 13:21:54 GMT
WORKDIR /tmp
# Wed, 06 Mar 2024 13:22:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 06 Mar 2024 13:22:09 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 06 Mar 2024 13:22:09 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e29c8b4b8407175ca98aa52e0e9c0ab05943a911b8f39dda5790f1454c2e6d`  
		Last Modified: Wed, 06 Mar 2024 13:34:32 GMT  
		Size: 142.0 MB (142008478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8db874e71d546472a8a6db3379d992d579720448c5fead37b0295d4804e306`  
		Last Modified: Wed, 06 Mar 2024 13:37:02 GMT  
		Size: 58.8 MB (58751076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0782185757d054e3c8d54cf24844577d8b83d046e0c1b3d2c53fd8b503565ad`  
		Last Modified: Wed, 06 Mar 2024 13:36:56 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
