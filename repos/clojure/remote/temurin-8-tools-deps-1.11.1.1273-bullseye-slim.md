## `clojure:temurin-8-tools-deps-1.11.1.1273-bullseye-slim`

```console
$ docker pull clojure@sha256:13ec4b25670da5adfcb6dafb95d4cbbca0e17d77216a1a2c99172faccd6b9bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-tools-deps-1.11.1.1273-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:48bb2fb11bd3694b2713310b06f86d84101d47446685fe9508463fda78d51b90
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.6 MB (147556517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf1af1c0dce630574ab04ebd8e05b4a61b8e52b93b27bd7169bff0d1f7ec40b`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Apr 2023 19:58:51 GMT
COPY dir:715eb4123a1bd94a1f232c902a6f3cdcc4011195a3e566c0f0ddc35dd1e83095 in /opt/java/openjdk 
# Wed, 26 Apr 2023 19:58:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Apr 2023 20:02:24 GMT
ENV CLOJURE_VERSION=1.11.1.1273
# Wed, 26 Apr 2023 20:02:24 GMT
WORKDIR /tmp
# Wed, 26 Apr 2023 20:02:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4938afe6c0690d2a6553141857742d94a7350c02b4fa57cd6a9c1b7cbe66492e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 26 Apr 2023 20:02:40 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 26 Apr 2023 20:02:40 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7773126247f89efdc56db7f90c92282e6c501ad8da6e738413eb8294ca8f168d`  
		Last Modified: Wed, 26 Apr 2023 20:17:34 GMT  
		Size: 54.6 MB (54642132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5218933cbce65649fc1d157a636b36544b061f088249d9e16be67ed2c39d786c`  
		Last Modified: Wed, 26 Apr 2023 20:19:36 GMT  
		Size: 61.5 MB (61495544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218ae1c9c0a5deb4bf1665ba72632f769f821bb899eb0fb03934c5c5376e4369`  
		Last Modified: Wed, 26 Apr 2023 20:19:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-tools-deps-1.11.1.1273-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b44cbf8f097a5cd9a183ed500ebbf9551006d2c064dbb1505d1f7043477dbc8c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145406677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2eb8de9595bae33d597c372128f9eecf1c317dd5d9418b975edcd77d60ffcd`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 03 May 2023 17:44:17 GMT
COPY dir:f6bbe63c81e220d954915791686219263d8c45918fd81b238f7c9f6b21f076f8 in /opt/java/openjdk 
# Wed, 03 May 2023 17:44:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 17:45:53 GMT
ENV CLOJURE_VERSION=1.11.1.1273
# Wed, 03 May 2023 17:45:53 GMT
WORKDIR /tmp
# Wed, 03 May 2023 17:46:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4938afe6c0690d2a6553141857742d94a7350c02b4fa57cd6a9c1b7cbe66492e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 03 May 2023 17:46:08 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 03 May 2023 17:46:08 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45323ce94562764c60b759096664441c4fd32a723ce4c04882e7478c93e9b104`  
		Last Modified: Wed, 03 May 2023 17:53:34 GMT  
		Size: 53.7 MB (53742660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a829379e7c83ae1ebf7871345d034a405f1f237abb39b77e776bad3eb1f7cb`  
		Last Modified: Wed, 03 May 2023 17:54:25 GMT  
		Size: 61.6 MB (61610670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d0d799358214ddbd2545fee8323ba7c48fb8f50cb5fed59f7072fc3f514b8e`  
		Last Modified: Wed, 03 May 2023 17:54:19 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
