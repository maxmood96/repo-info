## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:c38e1e3484f6d256adb488eef73ecc4954be3a2091d76e56fa45f58141ac1393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:5f7834094f884843ede8846b60722712f9c8e66c7d0908e259c3a526686e0639
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.2 MB (275160430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf05e60c89ce4f30e397b0045eb7026ef99feb49c802b7a8a2cc55f25f4f9aaf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:27:57 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Wed, 24 Apr 2024 03:27:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:04:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 May 2024 05:36:36 GMT
COPY dir:d78c0cec90816231fd61ebcd7c27b07c1af0064b89c255fd2a157e0b344541d4 in /opt/java/openjdk 
# Thu, 02 May 2024 05:36:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 05:38:58 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Thu, 02 May 2024 05:38:58 GMT
WORKDIR /tmp
# Thu, 02 May 2024 05:39:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Thu, 02 May 2024 05:39:16 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 02 May 2024 05:39:17 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 02 May 2024 05:39:17 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 02 May 2024 05:39:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1468e7ff95fcb865fbc4dee7094f8b99c4dcddd6eb2180cf044c7396baf6fc2f`  
		Last Modified: Wed, 24 Apr 2024 03:32:18 GMT  
		Size: 49.6 MB (49576283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3d2bb219021f5a0f51f710d9afc9a3f7ea8570ead7c981bf3dde54ff59ff77d`  
		Last Modified: Thu, 02 May 2024 05:50:02 GMT  
		Size: 145.1 MB (145095139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6d0279157ce808c032f9445ec6ceb90a4d344e37dcad79ff447b123438e406`  
		Last Modified: Thu, 02 May 2024 05:51:45 GMT  
		Size: 80.5 MB (80487988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a30a874b44a960dabd789ee4447cbd2a6de745a18d3fd6d2835e928f1666f6`  
		Last Modified: Thu, 02 May 2024 05:51:36 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47ab10a7e2128adf36b2943e8a4cacc99b77362d3233548e1a9f5857151b2ba`  
		Last Modified: Thu, 02 May 2024 05:51:37 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:66d2ee6810347a4518a6b05f7f1ba2de8c480d81a543f3c55632611be38954cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.7 MB (273749789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15b17c3b3853f3e261f1d38e295f116932d3a10d6cc4c5bd82936bc9051ebaf3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:42:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 May 2024 05:34:02 GMT
COPY dir:317487729b1812635c51c5f305bd9178bd957a141903eab756a1683874b5752b in /opt/java/openjdk 
# Thu, 02 May 2024 05:34:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 05:36:08 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Thu, 02 May 2024 05:36:08 GMT
WORKDIR /tmp
# Thu, 02 May 2024 05:36:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Thu, 02 May 2024 05:36:24 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 02 May 2024 05:36:24 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 02 May 2024 05:36:24 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 02 May 2024 05:36:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c191e5e52826fad3dddc86efe964528ec951aa9c2e292e7e267adae803be26`  
		Last Modified: Thu, 02 May 2024 05:45:24 GMT  
		Size: 143.9 MB (143891830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e25933238997c487c011d67414c15b48ce549509c01116caaaca3c303972081d`  
		Last Modified: Thu, 02 May 2024 05:47:01 GMT  
		Size: 80.2 MB (80243604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e7692c93107c12f6ed16ab12a91ce8334dae6aa80a4a0d17a25012b2dcd7f7`  
		Last Modified: Thu, 02 May 2024 05:46:53 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d24395bec3edd34e550714b160082cc6e88ea3b12cd02a53b97bec72d6ecdb3`  
		Last Modified: Thu, 02 May 2024 05:46:53 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
