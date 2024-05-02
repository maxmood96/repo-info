## `clojure:temurin-11-tools-deps-1.11.3.1456-bookworm`

```console
$ docker pull clojure@sha256:1c0bba637379cacbb3abe57e46365c1edf410be4885dd8d705b9fa639a55f1c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-1.11.3.1456-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:f4eda5109f357f579841b205c23e4204335335d1e369daf6fd0dd6024e71b672
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.6 MB (275569069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9850132f1dbdd335be0af5e4f33970f5c9de979857c88ed72e631ffd9909d0b2`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 24 Apr 2024 03:27:57 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Wed, 24 Apr 2024 03:27:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:04:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 May 2024 05:31:25 GMT
COPY dir:cf3bf634873a2f76d010dec9a72ea70ddc69381f0d8d3cb32fb43e16f4a2fabd in /opt/java/openjdk 
# Thu, 02 May 2024 05:31:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 05:34:10 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Thu, 02 May 2024 05:34:10 GMT
WORKDIR /tmp
# Thu, 02 May 2024 05:34:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Thu, 02 May 2024 05:34:34 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 02 May 2024 05:34:35 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1468e7ff95fcb865fbc4dee7094f8b99c4dcddd6eb2180cf044c7396baf6fc2f`  
		Last Modified: Wed, 24 Apr 2024 03:32:18 GMT  
		Size: 49.6 MB (49576283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae37ff616878154fce154f90ab1fc991e07a5f0fc272f49bcf57d8012db8e2b8`  
		Last Modified: Thu, 02 May 2024 05:46:28 GMT  
		Size: 145.5 MB (145504611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeb072a90c5e92086c34db7f6d624d55b042a63d693db081875b9bdfe121edb0`  
		Last Modified: Thu, 02 May 2024 05:48:10 GMT  
		Size: 80.5 MB (80487558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f08664ba32b738b8b82a659b119a8bbf57cbfa917db98b395ed74e8203695f`  
		Last Modified: Thu, 02 May 2024 05:48:00 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-1.11.3.1456-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0680c335a6aa5970d577813d7f374936623d4b40cb173cb1fc72cba4e676620e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272161999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9011b429c2f6d39a4b9f0f42d5d1d88156a60d2d792a68f71cf356a9874939dc`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:42:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 May 2024 05:29:50 GMT
COPY dir:c867ad1ba9e7953ae7814a5cf0e0df40f8d206a8555f8375af9a181bfc9862b9 in /opt/java/openjdk 
# Thu, 02 May 2024 05:29:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 05:32:05 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Thu, 02 May 2024 05:32:05 GMT
WORKDIR /tmp
# Thu, 02 May 2024 05:32:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Thu, 02 May 2024 05:32:26 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 02 May 2024 05:32:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89044dd89497a6d942edc38935a360a6f2e95d114a8247361685abb53e94aee`  
		Last Modified: Thu, 02 May 2024 05:42:10 GMT  
		Size: 142.3 MB (142304377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8173cc62db3c87271cd25c316c11e30876daad98cd536d9a29e900472b40cd01`  
		Last Modified: Thu, 02 May 2024 05:43:40 GMT  
		Size: 80.2 MB (80243661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d03654b392d92d5878c006067156ad041b1e38d3b2e0141235dba7016bb64b`  
		Last Modified: Thu, 02 May 2024 05:43:33 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
