## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:feedb0cd1527bdc923da6dfc57a07cd56e2372ac1e473041f4bd3b385f146d89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:39c869974b3eae9ddf99b78e3a2a346571d85fa208420692580e1f0343dc1adb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275347229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ce9607b581f4c579b9a207afaac33eb33ac8a61f3eb42e48584c0067b11c3e8`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:05 GMT
ADD file:6d9e71f0d3afb0b288cf2c06425795d528a142872692072ab1cd1ad275b67d1f in / 
# Wed, 31 Jan 2024 22:35:06 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:41:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 23:48:31 GMT
COPY dir:e1ce96bca1c423a1c79b84eacb7ae69429353a37485cc24af4161ce4b9d3ee2a in /opt/java/openjdk 
# Wed, 31 Jan 2024 23:48:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:52:27 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 31 Jan 2024 23:52:27 GMT
WORKDIR /tmp
# Wed, 31 Jan 2024 23:52:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 31 Jan 2024 23:52:46 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 31 Jan 2024 23:52:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6a299ae9cfd996c1149a699d36cdaa76fa332c8e9d66d6678fa9a231d9ead04c`  
		Last Modified: Wed, 31 Jan 2024 22:39:27 GMT  
		Size: 49.6 MB (49583754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8afe2d1272b0c5e9161314942fa02036caab8b5f924665169595a113d2b85488`  
		Last Modified: Thu, 01 Feb 2024 00:08:30 GMT  
		Size: 145.3 MB (145271031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6678ab51c2be5efb91426ceff67b14aae9b9bcfa86788ecd2b520a8cf271e8b9`  
		Last Modified: Thu, 01 Feb 2024 00:10:39 GMT  
		Size: 80.5 MB (80491828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82276f55b24c2ee4a4c4d5cc71c22a4a1a5176f7a2f5f9a4d19eba2737d07cf2`  
		Last Modified: Thu, 01 Feb 2024 00:10:30 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:daea9fbe21e56eb6e135fcab8be433aadec58fbe607ad290fee9d7cd90122feb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271881635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a28f8c873d414b8efbc26c8d5558cb4237f45a4938b0731e20d4a8e6facd701`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:15 GMT
ADD file:8bc7f537dd3dc4b92ec9006080fd563cc79205ee1ec3f456d03e869125a5bc21 in / 
# Wed, 31 Jan 2024 22:44:15 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:18:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 06:24:31 GMT
COPY dir:454699b64b949edd3264b234e72a891ace37d538f2726c5ec754e17e6fb3fb19 in /opt/java/openjdk 
# Thu, 01 Feb 2024 06:24:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:28:08 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 01 Feb 2024 06:28:08 GMT
WORKDIR /tmp
# Thu, 01 Feb 2024 06:28:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 01 Feb 2024 06:28:25 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 01 Feb 2024 06:28:25 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:66932e2b787d33a94ee3eb8b489be6e6838b29f5c1d732262da306da9b1f2eed`  
		Last Modified: Wed, 31 Jan 2024 22:47:40 GMT  
		Size: 49.6 MB (49615296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e0ac421e55bb8543ff3500ddf65c130f2d08b742a21b53522bcaa47b27c222`  
		Last Modified: Thu, 01 Feb 2024 06:42:18 GMT  
		Size: 142.0 MB (142006502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf378039e0b6aa91b5ac1717451cf668d89626d654d7fdbfa043de75af1f799b`  
		Last Modified: Thu, 01 Feb 2024 06:44:09 GMT  
		Size: 80.3 MB (80259219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b7cf1994a064e6efc0c5fc74af1950af6426b654e058805ef10e06105df183`  
		Last Modified: Thu, 01 Feb 2024 06:44:00 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
