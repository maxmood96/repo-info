## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:a71711a574e3cd6faf688db9cfd0988ec28145d7ae0138c9ecbbe2bd93c422fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:89eadc2758cfbef90b034e3adea09cbe92d848a33a318cfe4bf0d4d04aaaaa53
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.4 MB (196424538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b79db81f30ca0e503709161358ea36be9c535b6cc56cb0b10a13144a0114a517`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Nov 2022 01:06:16 GMT
COPY dir:53540f2d79f4eef9b2bf8c4b39ecdbbd82fb14bfcf951e14853afffd2efa2ecb in /opt/java/openjdk 
# Sat, 05 Nov 2022 01:06:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 01:10:05 GMT
ENV CLOJURE_VERSION=1.11.1.1189
# Sat, 05 Nov 2022 01:10:05 GMT
WORKDIR /tmp
# Sat, 05 Nov 2022 01:10:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1afd91b165776615eca84cce2271e5fe5d5818c55dee0f082b1304bb1464b3e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Sat, 05 Nov 2022 01:10:24 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 05 Nov 2022 01:10:24 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44770319b57989fffd145e48755d83843c0b9ca57cc5daa5ce8fd5ff705e3972`  
		Last Modified: Sat, 05 Nov 2022 01:22:08 GMT  
		Size: 103.5 MB (103530625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681bcf564708eb5844cb6c706ffae7d4b293ba42a9d686332585c7b5e75e1279`  
		Last Modified: Sat, 05 Nov 2022 01:24:33 GMT  
		Size: 61.5 MB (61473258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9462d43738e153aae109614d56b22f9e6d924391224c406ab3c8c5c498a7415`  
		Last Modified: Sat, 05 Nov 2022 01:24:25 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:10acd09a27d7d61a39e231305aac4b51ace59d3da0864812005f348afbdd1355
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 MB (194283948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a921c0534af8f47fe930381822169170919fed3465b5d2813caac5d4d0579aef`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 04 Nov 2022 23:07:51 GMT
COPY dir:8a3fd802e7e57a45d80b19a89e91b421563b952585d39995819354f278317671 in /opt/java/openjdk 
# Fri, 04 Nov 2022 23:07:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Nov 2022 23:11:02 GMT
ENV CLOJURE_VERSION=1.11.1.1189
# Fri, 04 Nov 2022 23:11:02 GMT
WORKDIR /tmp
# Fri, 04 Nov 2022 23:11:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1afd91b165776615eca84cce2271e5fe5d5818c55dee0f082b1304bb1464b3e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 04 Nov 2022 23:11:16 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 04 Nov 2022 23:11:16 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee1f441f545c19bf4b3a8cf835cc8fa7a9a80b78c85b47e4cfa93821a1095caf`  
		Last Modified: Fri, 04 Nov 2022 23:20:16 GMT  
		Size: 102.6 MB (102626601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b0e845c9f634d313526a604dc169ea8b8d0cf7fac13cb56acb085ffb9f023a`  
		Last Modified: Fri, 04 Nov 2022 23:22:08 GMT  
		Size: 61.6 MB (61592818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38164c1a9878294bfef11e737d813a97c46f9ae71d4d90b81028c120a0155abd`  
		Last Modified: Fri, 04 Nov 2022 23:22:02 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
