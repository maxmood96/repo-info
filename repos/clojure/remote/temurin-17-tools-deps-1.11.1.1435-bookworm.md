## `clojure:temurin-17-tools-deps-1.11.1.1435-bookworm`

```console
$ docker pull clojure@sha256:7af8ff82d2c468f97ced18d6acdf338015b94191c345d15da5ecdd8ba4d62bf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.1.1435-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:bef9b211c1901ac4abe536fe28a16fb0032c1e7c3591f49c0cdadc215a93054d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.9 MB (274938511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96527f7197ff03adefe57f89657cd5d8b63a9defccbe34fdcf6f5615885ac682`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:46:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 14:09:55 GMT
COPY dir:3be96ae7faea81e90455993c99b71c9b45986c7e71f70fc577ab97699c92b508 in /opt/java/openjdk 
# Wed, 06 Mar 2024 14:09:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 14:15:39 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 06 Mar 2024 14:15:39 GMT
WORKDIR /tmp
# Wed, 06 Mar 2024 14:15:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 06 Mar 2024 14:15:59 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 06 Mar 2024 14:15:59 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 06 Mar 2024 14:16:00 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 06 Mar 2024 14:16:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16509130f52dbe6d465329f39db40d29a6c2c14281e633450baff6de75121859`  
		Last Modified: Wed, 06 Mar 2024 14:28:11 GMT  
		Size: 144.9 MB (144893104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:606b70c9c9b1a25d867e2bc02af7aa522780a6b39f57fe029395d8cc2de93eff`  
		Last Modified: Wed, 06 Mar 2024 14:31:06 GMT  
		Size: 80.5 MB (80491784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b874d850d1cf5addfa0274a0a96f9a340aa449150f5be5496de684a7cee09f`  
		Last Modified: Wed, 06 Mar 2024 14:30:56 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0cf0fecb2385e0b852b3c37c1b62cfdb90273ef8ab904bc73533a9e7195825c`  
		Last Modified: Wed, 06 Mar 2024 14:30:56 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-1.11.1.1435-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:91059739aa9bda6d5cb7c5c9627245e0e1ed4f4527ce847b3249ebbc5fc5a847
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.6 MB (273568909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b35769ec2e6eb9e92db3b5b3bd27c8cd49ac14d4ae8e7a6dcc0d54d25fa45809`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:10 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Tue, 13 Feb 2024 00:41:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:53:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 06 Mar 2024 13:22:48 GMT
COPY dir:4a8c697909e89d854b955537d3c80fbcec33336dd00fb9805f3c0a9edf3861db in /opt/java/openjdk 
# Wed, 06 Mar 2024 13:22:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Mar 2024 13:27:46 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 06 Mar 2024 13:27:46 GMT
WORKDIR /tmp
# Wed, 06 Mar 2024 13:28:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 06 Mar 2024 13:28:02 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 06 Mar 2024 13:28:03 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 06 Mar 2024 13:28:03 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 06 Mar 2024 13:28:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd9e4d0e4feed501f9183f335a260b7c3ffdfd6dc1fd1de88bd150909f9355e`  
		Last Modified: Wed, 06 Mar 2024 13:37:56 GMT  
		Size: 143.7 MB (143720890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bf9a268afab8b96affa66b481f3dc19bbf56e976e10d12caa4a9d5ae015198`  
		Last Modified: Wed, 06 Mar 2024 13:40:34 GMT  
		Size: 80.3 MB (80256038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe01cf7b654dc649f6406b75562cc9c6ba28223cc026477a0a190b56de266dc4`  
		Last Modified: Wed, 06 Mar 2024 13:40:27 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88610b3a80a4def877c9a6d3eefeffafa61e3bbaef46e5d6245a13eed0aae5f7`  
		Last Modified: Wed, 06 Mar 2024 13:40:27 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
