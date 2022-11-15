## `clojure:temurin-8-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:daf7b61b185ac0db01bb8da4147afdd05b8869e7be98af8cfb2d8f00e25196a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ed06e6327be3d3fecfeae3538b0ffdd656ae5045f901a78d787ee06f24228987
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.4 MB (196417339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eebc01646e3abc7cce829113510b3f281b7c8706df7e8d0446bfa0d9a4704011`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 17:51:10 GMT
COPY dir:53540f2d79f4eef9b2bf8c4b39ecdbbd82fb14bfcf951e14853afffd2efa2ecb in /opt/java/openjdk 
# Tue, 15 Nov 2022 17:51:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 17:53:28 GMT
ENV CLOJURE_VERSION=1.11.1.1189
# Tue, 15 Nov 2022 17:53:28 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 17:53:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1afd91b165776615eca84cce2271e5fe5d5818c55dee0f082b1304bb1464b3e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 15 Nov 2022 17:53:47 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 15 Nov 2022 17:53:47 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05516bbc03e0cd1f73865c9a4a41f11df1cc12062f6b425c2b18212f6025faf6`  
		Last Modified: Tue, 15 Nov 2022 18:06:48 GMT  
		Size: 103.5 MB (103530607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4154e2cfef0e7c1bf67e862b2df1dbfe9a527c7f5df8ade57b09d0a23a5ef9`  
		Last Modified: Tue, 15 Nov 2022 18:07:48 GMT  
		Size: 61.5 MB (61473486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9aba2a9b2729e0c726c6a0000920cf808efb2ca49796fa37b93b4323621f9d4`  
		Last Modified: Tue, 15 Nov 2022 18:07:40 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:446a591269b83ac266fac8a42309ef86a1e502099a859066635135b144e5ec88
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 MB (194280806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4abc08a7949dc4c00f94e215eb5e188a1401f55b4dddbdc8f92dbad312ef0c4b`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 05:49:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 05:49:25 GMT
COPY dir:8a3fd802e7e57a45d80b19a89e91b421563b952585d39995819354f278317671 in /opt/java/openjdk 
# Tue, 15 Nov 2022 05:49:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 05:51:03 GMT
ENV CLOJURE_VERSION=1.11.1.1189
# Tue, 15 Nov 2022 05:51:03 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 05:51:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1afd91b165776615eca84cce2271e5fe5d5818c55dee0f082b1304bb1464b3e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 15 Nov 2022 05:51:17 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 15 Nov 2022 05:51:17 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801358ff5f2e42bc914ccad34f344c2f79c73c7246811cecac0e1e3502c74b1e`  
		Last Modified: Tue, 15 Nov 2022 06:01:53 GMT  
		Size: 102.6 MB (102626554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:146b3bfef8be50ebae7ecf4244fd9e3b435286687dafafe39adf4d37ac561a0e`  
		Last Modified: Tue, 15 Nov 2022 06:02:45 GMT  
		Size: 61.6 MB (61593029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e670a6df4ef8910a679b8ee1dd5268415f4f3ceb1c81ac03c25127953d873c`  
		Last Modified: Tue, 15 Nov 2022 06:02:39 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
