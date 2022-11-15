## `clojure:temurin-11-tools-deps-1.11.1.1189-bullseye-slim`

```console
$ docker pull clojure@sha256:830ca8eb783a20f7b1ab4cc2fedae7477b3c98e3c581959b5bc66c6d08933d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-1.11.1.1189-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:164b67fd70567f9ca4c82d5916b3dcba2ace6c1748d714f0f4ca875b332fbbef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.3 MB (291342718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b804cd5704f4318ea05758e2f70ed4198aa339c1a8e4cba65b875c88d941784c`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 15 Nov 2022 04:04:54 GMT
ADD file:d08e242792caa7f842fcf39a09ad59c97a856660e2013d5aed3e4a29197e9aaa in / 
# Tue, 15 Nov 2022 04:04:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 13:05:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 13:06:05 GMT
COPY dir:039751b2f6c905ea6e5bf7be1061a4abdf10c194a9bb43ba41c6aa90a55e71df in /opt/java/openjdk 
# Tue, 15 Nov 2022 17:54:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 17:56:34 GMT
ENV CLOJURE_VERSION=1.11.1.1189
# Tue, 15 Nov 2022 17:56:34 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 17:56:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1afd91b165776615eca84cce2271e5fe5d5818c55dee0f082b1304bb1464b3e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 15 Nov 2022 17:56:53 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 15 Nov 2022 17:56:53 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a603fa5e3b4127f210503aaa6189abf6286ee5a73deeaab460f8f33ebc6b64e2`  
		Last Modified: Tue, 15 Nov 2022 04:08:47 GMT  
		Size: 31.4 MB (31412630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59f3a54c9da4f17e8e6ada892097489f0887a8e9965cfb5089fefdc32210d7e`  
		Last Modified: Tue, 15 Nov 2022 13:09:11 GMT  
		Size: 198.5 MB (198455813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceecf6d23084108c1924368f7b87b1bf30820e656399c9a3af9c6f2cbb66a43a`  
		Last Modified: Tue, 15 Nov 2022 18:09:43 GMT  
		Size: 61.5 MB (61473659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c973cde0535379d862c56155d77a7b598dbfc112f884ae6b0bdbfd2260accc8`  
		Last Modified: Tue, 15 Nov 2022 18:09:35 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-1.11.1.1189-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0c8a5c20d110b5cdf108cfcee733e5b7a8ac65dedf63f835934ca1f6b730f1c4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.9 MB (286855608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb6b3c4eeab4e6469227e8f83de061b0ef028aa066cd96b3d592f913ea69b390`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:20 GMT
ADD file:1dad2420090b3d6ef5df8d1f7f2878b22f8687b8dba008a63800f6c74b36dee9 in / 
# Tue, 15 Nov 2022 01:41:20 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 05:49:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 15 Nov 2022 05:51:59 GMT
COPY dir:5aa0292cc524fb250468b6c5a859d971d75bcb0dd4bed7cfb9f10423858de6d6 in /opt/java/openjdk 
# Tue, 15 Nov 2022 05:52:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Nov 2022 05:53:37 GMT
ENV CLOJURE_VERSION=1.11.1.1189
# Tue, 15 Nov 2022 05:53:38 GMT
WORKDIR /tmp
# Tue, 15 Nov 2022 05:53:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1afd91b165776615eca84cce2271e5fe5d5818c55dee0f082b1304bb1464b3e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 15 Nov 2022 05:53:51 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 15 Nov 2022 05:53:51 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f3ac85625e767ee0ec42b5a2ef93880251cd973b86f77124c4ed39bccd2f8bf9`  
		Last Modified: Tue, 15 Nov 2022 01:44:35 GMT  
		Size: 30.1 MB (30060605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7cde71cdd6ac565f043bc4ec8903ab809981c13bc3c9e55dd5b7290a1bb0801`  
		Last Modified: Tue, 15 Nov 2022 06:03:30 GMT  
		Size: 195.2 MB (195201143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d368e65daa5b4712194c2588c82c420e4ad1918a3960a78a6dbe3e688af67fac`  
		Last Modified: Tue, 15 Nov 2022 06:04:23 GMT  
		Size: 61.6 MB (61593242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7466b0c80129d751a65bc762ddb632844270d48b6f8918d83f967d72a9edffc5`  
		Last Modified: Tue, 15 Nov 2022 06:04:17 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
