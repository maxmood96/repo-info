## `clojure:temurin-11-tools-deps-1.11.3.1456-bookworm`

```console
$ docker pull clojure@sha256:412a5daca1b144322ae4c0791d0657739bd8864c437e9a7274b2a1b2aef2e930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-1.11.3.1456-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:2e6790bb1466f064bd39080ec301ecd1253fc0f0a171c3313033a04b23eebaaf
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.6 MB (275569299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50f62f42c945eca00331f85b2c8458694f8d200209f6f44613d0003ca1a33f0`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 28 May 2024 21:19:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 21:27:14 GMT
COPY dir:cf3bf634873a2f76d010dec9a72ea70ddc69381f0d8d3cb32fb43e16f4a2fabd in /opt/java/openjdk 
# Tue, 28 May 2024 21:27:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 21:30:02 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 21:30:02 GMT
WORKDIR /tmp
# Tue, 28 May 2024 21:30:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 28 May 2024 21:30:22 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 28 May 2024 21:30:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3444b8efdeb1d026bf11d8b7cf0328ae0a64d6119ca2d7d9706f99ac7c33a70`  
		Last Modified: Tue, 28 May 2024 21:52:59 GMT  
		Size: 145.5 MB (145504610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94736540db67f5ee4dabf54e737e5c6fa8b8d86422cee4a77c20ddccd54513d3`  
		Last Modified: Tue, 28 May 2024 21:54:47 GMT  
		Size: 80.5 MB (80487682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffffa305b118d7f7ef1027921683a97f52eb1a90d3ca93599948283c23065344`  
		Last Modified: Tue, 28 May 2024 21:54:37 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-1.11.3.1456-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b04258f437aa17becd8ae5886834cffc45ff2f30e338ae56ae1075bda559c187
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272163207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c4c64a735f7470cf26d9a127cef3c83df768222fd6d41387a72f3dc6f1b1f2`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 14 May 2024 00:39:32 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Tue, 14 May 2024 00:39:33 GMT
CMD ["bash"]
# Tue, 28 May 2024 19:43:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 19:50:22 GMT
COPY dir:c867ad1ba9e7953ae7814a5cf0e0df40f8d206a8555f8375af9a181bfc9862b9 in /opt/java/openjdk 
# Tue, 28 May 2024 19:50:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 19:52:38 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 19:52:38 GMT
WORKDIR /tmp
# Tue, 28 May 2024 19:52:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 28 May 2024 19:52:55 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 28 May 2024 19:52:55 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb8062e3a19463de6ca9a059efe4590b709d39e2ef448fe456d0c78f122260ae`  
		Last Modified: Tue, 28 May 2024 20:11:10 GMT  
		Size: 142.3 MB (142304343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18a16bf414cf0f709d394ab5df4c9dbf21feb424b5aa745c570c5aab3576408f`  
		Last Modified: Tue, 28 May 2024 20:12:43 GMT  
		Size: 80.2 MB (80244858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8ea72324cb1f472a33ca6e9f3ede04d1594be0d5658f3032c8131328cacfb5`  
		Last Modified: Tue, 28 May 2024 20:12:35 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
