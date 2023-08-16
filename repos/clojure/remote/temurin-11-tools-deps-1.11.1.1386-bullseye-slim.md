## `clojure:temurin-11-tools-deps-1.11.1.1386-bullseye-slim`

```console
$ docker pull clojure@sha256:e81108d30bfc944fc3ebac93cdd20319d74a28904bbc539b63962c56fe06430a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-1.11.1.1386-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3f2b4095f990c2f411d699330343122cde10b924dbda15bae91438ac871e7e58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.8 MB (237751179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e30df1b39fd9e8355e7d8790c0be71e13a1c50973a59a7fdd106c0effe7ee077`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 16 Aug 2023 01:00:09 GMT
ADD file:2d91c2e03d02bfa16fe4f766d851b351d93d33f84751ad96c985e64ea024ec28 in / 
# Wed, 16 Aug 2023 01:00:09 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:02:38 GMT
COPY dir:72d046f3e284b8eca8066a837ab8a68f91b4cf5355de7f6803a8ee9b7ce3d682 in /opt/java/openjdk 
# Wed, 16 Aug 2023 18:05:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 18:07:42 GMT
ENV CLOJURE_VERSION=1.11.1.1386
# Wed, 16 Aug 2023 18:07:42 GMT
WORKDIR /tmp
# Wed, 16 Aug 2023 18:07:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3a09e2df4d3abd89b5b1286af0133a36a525ff3acfe1432f98b5c24b170940e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 16 Aug 2023 18:07:59 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 16 Aug 2023 18:07:59 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:14726c8f78342865030f97a8d3492e2d1a68fbd22778f9a31dc6be4b4f12a9bc`  
		Last Modified: Wed, 16 Aug 2023 01:05:12 GMT  
		Size: 31.4 MB (31417678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209f416efba54d09e37495a54336ac55d40fc467f753f97e78f060748b4513e5`  
		Last Modified: Wed, 16 Aug 2023 17:06:20 GMT  
		Size: 144.8 MB (144831672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28118c6505705ff4c96dc8d797d68a9820ae5350b59a25fdbce056a02490b4eb`  
		Last Modified: Wed, 16 Aug 2023 18:17:11 GMT  
		Size: 61.5 MB (61501212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d18a4f49e09af8e98a4009ad2546cddb6a3c46647976ce106faa8cfdd238bd`  
		Last Modified: Wed, 16 Aug 2023 18:17:03 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-1.11.1.1386-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a8ce3a2134afca34ce300201e70458e5043c3d8de812674b8de7c505e6c78abe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233244854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bf45261440edf96fe07968b598e83da91f2a418d669a71ea175691d94542c74`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:22:18 GMT
COPY dir:6acc55ac013a722a8db4af8f0ce8de9270cd9aeb372e6c734b449d15adcc5218 in /opt/java/openjdk 
# Wed, 16 Aug 2023 17:22:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 17:24:44 GMT
ENV CLOJURE_VERSION=1.11.1.1386
# Wed, 16 Aug 2023 17:24:44 GMT
WORKDIR /tmp
# Wed, 16 Aug 2023 17:24:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3a09e2df4d3abd89b5b1286af0133a36a525ff3acfe1432f98b5c24b170940e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 16 Aug 2023 17:24:58 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 16 Aug 2023 17:24:58 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1e09cb30a1ef0915a1ffb7a7e09dbfbbd6ca50b0de70ef22c1ecb37d83b229`  
		Last Modified: Wed, 16 Aug 2023 17:31:53 GMT  
		Size: 141.6 MB (141565229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ae777a59f28c076a592701a94a6576b77dfef62cf457b05295ebe5aed57338`  
		Last Modified: Wed, 16 Aug 2023 17:33:19 GMT  
		Size: 61.6 MB (61616191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e679cc8d10f38b54ccdd41b80ce85a44bbc2b0abb4bd0546f61cdcd422e82769`  
		Last Modified: Wed, 16 Aug 2023 17:33:13 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
