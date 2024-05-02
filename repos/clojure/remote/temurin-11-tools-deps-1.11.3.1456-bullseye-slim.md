## `clojure:temurin-11-tools-deps-1.11.3.1456-bullseye-slim`

```console
$ docker pull clojure@sha256:51fe1339c3b1fbebd79fe0115cd29e501a78bcfb8ec97c79634cf84bf43633d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-1.11.3.1456-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9d31120d612dea9481088a5b21e783848caa6f0db0061ed1f8692c168159969c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.6 MB (235564966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ab01344bc2823871858f5c2311a069db9f99b943a765f01b6ca8211b6ac88c5`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 May 2024 05:32:55 GMT
COPY dir:cf3bf634873a2f76d010dec9a72ea70ddc69381f0d8d3cb32fb43e16f4a2fabd in /opt/java/openjdk 
# Thu, 02 May 2024 05:32:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 05:35:28 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Thu, 02 May 2024 05:35:28 GMT
WORKDIR /tmp
# Thu, 02 May 2024 05:35:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Thu, 02 May 2024 05:35:46 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 02 May 2024 05:35:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081ca8515cf2999fc67475b477aa76fcb7134cbdf2209d9be8b6fe4d25804cb2`  
		Last Modified: Thu, 02 May 2024 05:47:27 GMT  
		Size: 145.5 MB (145504611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f95bef2a1a3388e73325ace62934828484bd7b1988747d3398f07a6aba374b`  
		Last Modified: Thu, 02 May 2024 05:49:01 GMT  
		Size: 58.6 MB (58625474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed02dda9f386f5d015a41652d130f7eeed1761a5106b89fa1475d826eb8d308`  
		Last Modified: Thu, 02 May 2024 05:48:54 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-1.11.3.1456-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:763df9f12b7ad2f7bdc9f7680343b2e3b4884698dec0619ec858e68b0f440e7b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231141195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7035970ced6482707ac29bf57c1a2adecf0a1689d7039f0f91dc2354dfbd2e92`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:44:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 May 2024 05:31:09 GMT
COPY dir:c867ad1ba9e7953ae7814a5cf0e0df40f8d206a8555f8375af9a181bfc9862b9 in /opt/java/openjdk 
# Thu, 02 May 2024 05:31:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 05:33:12 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Thu, 02 May 2024 05:33:12 GMT
WORKDIR /tmp
# Thu, 02 May 2024 05:33:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Thu, 02 May 2024 05:33:25 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 02 May 2024 05:33:25 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47454ded192101c0d37473879a630a0b06f8c38619c60da0859950d1987b84e`  
		Last Modified: Thu, 02 May 2024 05:43:02 GMT  
		Size: 142.3 MB (142304375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd81b4a915ef4ee329854d5612d03c395dc6ced3700399c33835aa747edc286b`  
		Last Modified: Thu, 02 May 2024 05:44:28 GMT  
		Size: 58.7 MB (58748866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3434015a2309295d0cb00b6ef4e28afb6ce4b874be1dff13b1d553d414d8abe`  
		Last Modified: Thu, 02 May 2024 05:44:22 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
