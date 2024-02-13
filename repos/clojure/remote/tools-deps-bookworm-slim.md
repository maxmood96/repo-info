## `clojure:tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:7e4d1176d08422fd1c88675d09c50e5d09a6111e6db7bb2344fc2bed10f89047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:48d6c3bba6a9b44ca5042859f2b74a6d3c62651041583acc4fc763354a433bb5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 MB (257770096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15115b5469cada3a908e1536cf210e2b6602bd9afdc0e600890ef4e41d402e7d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:47:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 02:04:14 GMT
COPY dir:64a8841762a9afbd2fb8b4cf497b2dee87765737d44ff0387ce1cfc51371c9a2 in /opt/java/openjdk 
# Tue, 13 Feb 2024 02:04:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 02:05:59 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Tue, 13 Feb 2024 02:05:59 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 02:06:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 13 Feb 2024 02:06:18 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 13 Feb 2024 02:06:18 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 13 Feb 2024 02:06:18 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Feb 2024 02:06:19 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6584afe528baa6e2714ec675351d17acf5bdb28756f21582641fc558ac73ed`  
		Last Modified: Tue, 13 Feb 2024 02:20:22 GMT  
		Size: 159.6 MB (159582932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:307164c92e3351c5014acf4f66ca7374e098922690fa38d0b3b44afea5c54c70`  
		Last Modified: Tue, 13 Feb 2024 02:22:15 GMT  
		Size: 69.1 MB (69062060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404f63d9bc0a0e9706beca1a3159d53c76c8aeb55f84c15addd0786c1eab7f48`  
		Last Modified: Tue, 13 Feb 2024 02:22:07 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03744f0d3c5cfad3b7d144be176835c17cfcce5057120fb34d7f0e5976bb395e`  
		Last Modified: Tue, 13 Feb 2024 02:22:06 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d610c152bf194281b87bc43e6ec6df7feb5668cf78125be7e0561008e72f1cf6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255759261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179e32d935abaa1f6df7f6c20bd536fffe58390f29400855ca45e677a3521e64`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:55:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 02:09:18 GMT
COPY dir:ab40534e435f9942975c0e8b5454d6b7a8d69c445f8e0758c1bd9c500e157fca in /opt/java/openjdk 
# Tue, 13 Feb 2024 02:09:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 02:10:51 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Tue, 13 Feb 2024 02:10:51 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 02:11:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 13 Feb 2024 02:11:07 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 13 Feb 2024 02:11:07 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 13 Feb 2024 02:11:07 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Feb 2024 02:11:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e52067d70268135532011ee3c716818e124283b635dfc7901c4412acbb040e6e`  
		Last Modified: Tue, 13 Feb 2024 02:24:16 GMT  
		Size: 157.8 MB (157784588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2fb8d624bae9d262374ec071fb95e2a686f61af33e2f3404d6b505432aba0e0`  
		Last Modified: Tue, 13 Feb 2024 02:26:06 GMT  
		Size: 68.8 MB (68817298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36687c05e9841fd877267a87bb1f9859a97ba6e4b07bb9f3c45044aab0aaadb`  
		Last Modified: Tue, 13 Feb 2024 02:25:59 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b5e0810ed0387e5bf630d940ecf119bde1fa45587f47bf4689f1bc221f039c`  
		Last Modified: Tue, 13 Feb 2024 02:25:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
