## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:e3aa2f08d8a60cef5dd19a413e29a1cec3d380792e651ac7bceeb2c90217d226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:40490084845e267b8a1b155c25d0fd42ef6b31853e5ffeadb6824ebe9535e891
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.8 MB (300803843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7271f65f86277c1bf7ed81302b47a0c5045c6ddf6852be997881b8ea0816fbb`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:42 GMT
ADD file:26702ba2c3e94cb21cdb3c550cf01cf848823d160f3417b559116d4c718e5df0 in / 
# Tue, 25 Oct 2022 01:43:42 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:32:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Nov 2022 01:11:42 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Sat, 05 Nov 2022 01:11:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 01:16:41 GMT
ENV CLOJURE_VERSION=1.11.1.1189
# Sat, 05 Nov 2022 01:16:42 GMT
WORKDIR /tmp
# Sat, 05 Nov 2022 01:16:57 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1afd91b165776615eca84cce2271e5fe5d5818c55dee0f082b1304bb1464b3e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Sat, 05 Nov 2022 01:16:57 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 05 Nov 2022 01:16:58 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:17c9e6141fdb3387e5a1c07d4f9b6a05ac1498e96029fa3ea55470d4504f7770`  
		Last Modified: Tue, 25 Oct 2022 01:47:28 GMT  
		Size: 55.0 MB (55046332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888ca723db20161bd481e5a8af9ae7b9145b403d0fa3f2f444e7c6a21909570c`  
		Last Modified: Sat, 05 Nov 2022 01:25:58 GMT  
		Size: 198.5 MB (198455847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f792717f93f222dd50b0c72f2e8fb31d7ce01cd7f83acccdee11bfd68972f9a`  
		Last Modified: Sat, 05 Nov 2022 01:28:15 GMT  
		Size: 47.3 MB (47301045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e595deaaae79d8f2e4ed76c52fc9a0a6e8c78effa8c33de5dc2ec37ce7ccf6c`  
		Last Modified: Sat, 05 Nov 2022 01:28:09 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2986fcbe79b735474cfe289bb6af8692f50a8b4f1c31d4c23b7d8aec36a22a04
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.2 MB (296198198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46388cef9e8b46e0fb8aa7033697c7b05273639a27d6c53dce9b25f957e61dd3`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 25 Oct 2022 05:45:55 GMT
ADD file:b16745ece8ef84c028d7e9ac4bf026ac64f885d4170bfcc9d435f237144a1b99 in / 
# Tue, 25 Oct 2022 05:45:56 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 23:53:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 04 Nov 2022 23:12:15 GMT
COPY dir:5aa0292cc524fb250468b6c5a859d971d75bcb0dd4bed7cfb9f10423858de6d6 in /opt/java/openjdk 
# Fri, 04 Nov 2022 23:12:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Nov 2022 23:15:31 GMT
ENV CLOJURE_VERSION=1.11.1.1189
# Fri, 04 Nov 2022 23:15:31 GMT
WORKDIR /tmp
# Fri, 04 Nov 2022 23:15:43 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1afd91b165776615eca84cce2271e5fe5d5818c55dee0f082b1304bb1464b3e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 04 Nov 2022 23:15:43 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 04 Nov 2022 23:15:44 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8e1d92e7d04d2a9a9880cb45dc3c32c2805912cd86abed96d0ada3ff28748205`  
		Last Modified: Tue, 25 Oct 2022 05:48:40 GMT  
		Size: 53.7 MB (53701966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89422e3bba4e9ae7d9df0676636eb6b1edefecaba3fbeccf62fea3f8a444364e`  
		Last Modified: Fri, 04 Nov 2022 23:23:14 GMT  
		Size: 195.2 MB (195201089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8c793a45a5a1e47ab9d6d46fcf54f37e324fa66ddd77a2cdf5c1e5a5643b14`  
		Last Modified: Fri, 04 Nov 2022 23:25:09 GMT  
		Size: 47.3 MB (47294525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f87fc76ef070811dda55d6fc088b7486a94688bedf13e34c41b987f7dfade90`  
		Last Modified: Fri, 04 Nov 2022 23:25:05 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
