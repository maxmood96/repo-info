## `clojure:temurin-8-tools-deps-1.11.3.1456-bookworm`

```console
$ docker pull clojure@sha256:7297a66d0fc28817e94e4c664fe339c048b5d9e3ac8e13e9f731cd4248a2d372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-tools-deps-1.11.3.1456-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:9b36c6031e79a8218544c913513f754ab4e9b8611d77b152573cdb29fba8ca3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233665018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ed878dd77d9acb8e3aa4b9d9d1b3b53e8f87da287824afeed6012e3c18c166`
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
# Thu, 25 Apr 2024 19:27:27 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Thu, 25 Apr 2024 19:27:27 GMT
WORKDIR /tmp
# Thu, 25 Apr 2024 19:27:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Thu, 25 Apr 2024 19:27:47 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 25 Apr 2024 19:27:47 GMT
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
	-	`sha256:7ca0f70e9bb9615f3e2051293d2e72ccbc24658dcfff9afa585be803e74ff7cd`  
		Last Modified: Thu, 25 Apr 2024 19:46:26 GMT  
		Size: 80.5 MB (80487979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfce4a2b6ac02630457a97de84df44955b589120635cc9c3605a0c154e96a776`  
		Last Modified: Thu, 25 Apr 2024 19:46:17 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-tools-deps-1.11.3.1456-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d27adabcf5db513b5ac2e97d7358f81d9ab26a71de3cbd588de89c64b3ef552c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.6 MB (232557035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dcd62affcd675cbdd4818785dfe87da191acc8681cfd82dc7172866a5e70f21`
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
# Thu, 25 Apr 2024 19:44:05 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Thu, 25 Apr 2024 19:44:05 GMT
WORKDIR /tmp
# Thu, 25 Apr 2024 19:44:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Thu, 25 Apr 2024 19:44:21 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 25 Apr 2024 19:44:21 GMT
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
	-	`sha256:c6f4a107652b2c15304e30a4b67d982e7ef431eba563f216714e165c7e1dbe6b`  
		Last Modified: Thu, 25 Apr 2024 20:01:10 GMT  
		Size: 80.2 MB (80242946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114d109936b7226c9a1f885c14b8e306f4a0adc9c2a417d026a6387dbddef578`  
		Last Modified: Thu, 25 Apr 2024 20:01:00 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
