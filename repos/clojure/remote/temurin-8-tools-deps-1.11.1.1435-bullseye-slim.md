## `clojure:temurin-8-tools-deps-1.11.1.1435-bullseye-slim`

```console
$ docker pull clojure@sha256:d7c36628925b140b933be0fa6fa40ac856a1af1e6deacee88dc3b55cc9b72e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-tools-deps-1.11.1.1435-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3607816fc568fbc5c09279217d3d073447582d2a5d2fba4708dd88eb98fb8846
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193640077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e410dabc6713b857838af28f52b92e2e9f1adc92fcf93c8222ceabd69f4e8da`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 23:44:36 GMT
COPY dir:7a6a87e7bb8d56b27d71b1f614847d2afb4282190a48214e2e48b164fbef7bc7 in /opt/java/openjdk 
# Wed, 31 Jan 2024 23:44:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:48:03 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 31 Jan 2024 23:48:03 GMT
WORKDIR /tmp
# Wed, 31 Jan 2024 23:48:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 31 Jan 2024 23:48:20 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 31 Jan 2024 23:48:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f1c7bfdaddc71e83c67b85b893fc8356c320085ad7fd07d8155f9936128564`  
		Last Modified: Thu, 01 Feb 2024 00:06:04 GMT  
		Size: 103.6 MB (103591889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f67e2b7271c5b14876e4341dd105a3c2a306c022b0e8d929f77eb3a87351328`  
		Last Modified: Thu, 01 Feb 2024 00:08:05 GMT  
		Size: 58.6 MB (58629743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d697d729c5b49ef3d8eef0eb0eb63e5f02d1a6ab9fdb3510a69fd787ddd16cf`  
		Last Modified: Thu, 01 Feb 2024 00:07:58 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-tools-deps-1.11.1.1435-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e10e78caacbb78b624539803546d9777eaef01a999e1f2cab925ffab934b54fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191524635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0ae68eaa3e6c96b08015374a81bbe01d5a0b0b9b7c997eb0a5a079d42cb731`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:42 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Wed, 31 Jan 2024 22:44:42 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:21:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 06:21:13 GMT
COPY dir:d67e1a8d4006c4d31bb089f955cdf6054ae46936c41fb4bbc9c830e6a49d11d6 in /opt/java/openjdk 
# Thu, 01 Feb 2024 06:21:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:24:09 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 01 Feb 2024 06:24:09 GMT
WORKDIR /tmp
# Thu, 01 Feb 2024 06:24:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 01 Feb 2024 06:24:24 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 01 Feb 2024 06:24:24 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e843c549a84c35b323e6c68534d42548cf20689935e9bb3e3ddcddf0dc445f8`  
		Last Modified: Thu, 01 Feb 2024 06:39:51 GMT  
		Size: 102.7 MB (102703026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f367e7db28857cfd80846f59a8d8d3f97b56fb6aca09ed907261401b4f1c976d`  
		Last Modified: Thu, 01 Feb 2024 06:41:56 GMT  
		Size: 58.8 MB (58756659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2171edb016c310777d00ba18ec8b53826323f9ba419d3feb03fc30bc5e5729b3`  
		Last Modified: Thu, 01 Feb 2024 06:41:49 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
