## `clojure:temurin-8-tools-deps-1.11.1.1435-bookworm`

```console
$ docker pull clojure@sha256:1a1961d24ad698d099f91d41ce2ec4b2c56487d5e221e6d4dff7cd8aee74fe76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-tools-deps-1.11.1.1435-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:df7332f4edf10f7401b02ec8b402a677d7d181d0155492473ae18c042ea589b1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233669319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbfefe9cbff0032c52086fe7ee33862c21ef1a6494fe1a24f22abf9229c1a447`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 24 Apr 2024 03:27:57 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Wed, 24 Apr 2024 03:27:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:04:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 21:13:39 GMT
COPY dir:54f5f76f9b290ecbafc047cf196165b69f1cb32e49c8748c35e250f5e316fcc0 in /opt/java/openjdk 
# Wed, 24 Apr 2024 21:13:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 21:16:22 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 21:16:22 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:16:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 21:16:41 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 21:16:41 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1468e7ff95fcb865fbc4dee7094f8b99c4dcddd6eb2180cf044c7396baf6fc2f`  
		Last Modified: Wed, 24 Apr 2024 03:32:18 GMT  
		Size: 49.6 MB (49576283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c0852faaab04d655f913386e0af6c14a4412d28e791543c7cdd1d53c23bf06`  
		Last Modified: Wed, 24 Apr 2024 21:40:04 GMT  
		Size: 103.6 MB (103600140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63981d54604dbdd197e8981aa1fa6b829e0a4c5a1780f41b5fafe305cfc024b3`  
		Last Modified: Wed, 24 Apr 2024 21:41:46 GMT  
		Size: 80.5 MB (80492277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09800548718b93606618ca455ec746300fde089726e23c900afe92b41477efc6`  
		Last Modified: Wed, 24 Apr 2024 21:41:36 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-tools-deps-1.11.1.1435-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3dfa3b808b245f1693119e1ead2424813e5854c87db2bc97e70699264eb6c695
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.6 MB (232572636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119cacd9c5a547da7fe06b15858eff06595aab7ea61be2c66c1c21f9e44987a0`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:42:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 18:59:42 GMT
COPY dir:f816a852ac21a5e29532918ac40e44b27f618ca8c5c539e334f114f460fe4b51 in /opt/java/openjdk 
# Wed, 24 Apr 2024 18:59:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 19:01:54 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 19:01:54 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 19:02:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 19:02:10 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 19:02:10 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a326c3125dc8673964b82d25ba8518ec98242bdf3b9b32ce6bc1024a14e290b`  
		Last Modified: Wed, 24 Apr 2024 19:21:24 GMT  
		Size: 102.7 MB (102700132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21894755dfe4ec9695341af4f1600359920395e9e158693c61771d3cc5695cf6`  
		Last Modified: Wed, 24 Apr 2024 19:22:49 GMT  
		Size: 80.3 MB (80258548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb007692a02cd499ca25a4e28f9fddb4f6675ed747d013b6ace55dbed717d958`  
		Last Modified: Wed, 24 Apr 2024 19:22:40 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
