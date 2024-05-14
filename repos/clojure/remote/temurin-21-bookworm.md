## `clojure:temurin-21-bookworm`

```console
$ docker pull clojure@sha256:6dc04d6ab32e7680e7d3bf2467987b64b59d09858de74f9ce9ceb67a220c8783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-21-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:26bd61c38fc48cedf8a78cd6bdc7d22c5efb934242bdf2f6604b95bf17e63b28
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.6 MB (288563305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e491d14d441d790568dac362b82894949285db12b5a2c501bba630d9ab8439ad`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:15:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 May 2024 02:15:15 GMT
COPY dir:2191d32deb04bfc59d7fcf2244f16c5ecbe60498375dcea5599e5d16a61b7305 in /opt/java/openjdk 
# Tue, 14 May 2024 02:15:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 02:28:17 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 14 May 2024 02:28:17 GMT
WORKDIR /tmp
# Tue, 14 May 2024 02:28:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 14 May 2024 02:28:36 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 14 May 2024 02:28:36 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 14 May 2024 02:28:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 14 May 2024 02:28:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5be90d7d7d6d7d1f579f73dbd213ea6d494ee85ca125960d6a369dc85906100`  
		Last Modified: Tue, 14 May 2024 02:35:20 GMT  
		Size: 158.5 MB (158498245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfff5cb3efda255ddd02e57277353ca7261bed070c6ecba0d66a959adc08f50b`  
		Last Modified: Tue, 14 May 2024 02:45:15 GMT  
		Size: 80.5 MB (80487658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce2c7fdb8f594c3785ae9627644a2b615f37770ea4116219d095461cd53e3d6`  
		Last Modified: Tue, 14 May 2024 02:45:04 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8750e88e31403c889b030c37a1195f0cbd057a442b87984abe7ffe8a556e2d46`  
		Last Modified: Tue, 14 May 2024 02:45:05 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-21-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:51c268760796e65354eb731d76ba30869048504e36f7fbc0b9ea7c5fdc71ed79
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286524821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea3081d96211d497d12ab8a2fa0ac798617edc9f4de88e3de3b35d1d8e0c549e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:32 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Tue, 14 May 2024 00:39:33 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:57:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 14 May 2024 01:57:58 GMT
COPY dir:96a90c8e1c03defb238a6d560d8927dc81a1a58af3fce1471cbce5249ed27f38 in /opt/java/openjdk 
# Tue, 14 May 2024 01:58:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 May 2024 02:08:54 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 14 May 2024 02:08:54 GMT
WORKDIR /tmp
# Tue, 14 May 2024 02:09:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 14 May 2024 02:09:10 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 14 May 2024 02:09:10 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 14 May 2024 02:09:10 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 14 May 2024 02:09:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03342e04b8899a174cdf243acd9baec9e244ebf5ce6d5907b7b983118dc6acf`  
		Last Modified: Tue, 14 May 2024 02:14:47 GMT  
		Size: 156.7 MB (156665568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e249b6a28fbf3845c0d44bcbf734474501a89bf325219e208b3bdf51a29073e2`  
		Last Modified: Tue, 14 May 2024 02:24:01 GMT  
		Size: 80.2 MB (80244851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9d19c274f456b30db649fee7815b55665e7335ed6e1a8d78503f424e3e4e66`  
		Last Modified: Tue, 14 May 2024 02:23:52 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526185263501341e67883cdca17685afdcf12faefb56fe015568f89c2d72fe3e`  
		Last Modified: Tue, 14 May 2024 02:23:52 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
