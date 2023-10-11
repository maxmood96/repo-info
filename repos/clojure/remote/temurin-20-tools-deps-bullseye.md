## `clojure:temurin-20-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:3833144a12f75802243e60892e8979e317cffa229e46eba7f26387de9a096af4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-20-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:86a24443ce28e2b9725065bee66e41a844e9c13c87d742242eda5e1302cefa4d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280752120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf00cf0a5ab4906d4d4bc620b82f96508e68f498129aebb8184a3ed2fbc11a0e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:01 GMT
ADD file:8a9222387b89a9ac763fd72610ce01ab17f64387cbfde30a6af1861a82030aad in / 
# Wed, 11 Oct 2023 18:35:01 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Oct 2023 19:00:08 GMT
COPY dir:6a540db71f2a37db361084aee8addd6817cd7c4f18237e6f852a38e98bdb4182 in /opt/java/openjdk 
# Wed, 11 Oct 2023 19:00:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 19:00:58 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Wed, 11 Oct 2023 19:00:58 GMT
WORKDIR /tmp
# Wed, 11 Oct 2023 19:01:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 11 Oct 2023 19:01:15 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 11 Oct 2023 19:01:15 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 11 Oct 2023 19:01:16 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 11 Oct 2023 19:01:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:69b3efbf67c2d9a46fdfdc8480b5a03ef73e9999a53aad57213447784f01eb6e`  
		Last Modified: Wed, 11 Oct 2023 18:39:54 GMT  
		Size: 55.1 MB (55058028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a97d10df8953529ff1f6df60971c7b84c95227d824b6ce97ce2bfe2cc85bf3`  
		Last Modified: Wed, 11 Oct 2023 19:09:21 GMT  
		Size: 153.8 MB (153791728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100e441d20ecd603d7978f27261695a133690d5be05c565d5c2bdde8a778aa83`  
		Last Modified: Wed, 11 Oct 2023 19:10:06 GMT  
		Size: 71.9 MB (71901347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c1f9a60b43320c2822b75ff2f0bc84f12f391fb6f3190ebbb3d4d303cd3f203`  
		Last Modified: Wed, 11 Oct 2023 19:09:56 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24959f58cab0df91aa5de325a55382839b30dc5cc0aaa770be9cfdb2f07771bb`  
		Last Modified: Wed, 11 Oct 2023 19:09:56 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-20-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e50f8adccac82739fc8cc19c47333570df76e19e7921fce7c50cdeeb6bc7d944
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.8 MB (277846049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e05008fa0c5db0dd1d1eacadc29a279aed2d76843ff25bb7a38fb46b090c40c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:58 GMT
ADD file:e1a6c6c976e5e7c53eb2a7343a7a763b46e56828588535f4c79e63d6ec08198d in / 
# Wed, 11 Oct 2023 18:24:58 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:45:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Oct 2023 18:53:22 GMT
COPY dir:d35c6357dd030960bb6081f48b2bc10afb3da11efc1525ff916214b03be70ddf in /opt/java/openjdk 
# Wed, 11 Oct 2023 18:53:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 18:54:17 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Wed, 11 Oct 2023 18:54:17 GMT
WORKDIR /tmp
# Wed, 11 Oct 2023 18:54:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 11 Oct 2023 18:54:32 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 11 Oct 2023 18:54:32 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 11 Oct 2023 18:54:32 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 11 Oct 2023 18:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:dd0dc10f921f4b3b65b17f20d367374079e6cb4e26531624ee64caaaf4adcc28`  
		Last Modified: Wed, 11 Oct 2023 18:28:45 GMT  
		Size: 53.7 MB (53707810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c04e556b0b665fddae8fe1113c4701b454a8828d28fe31c1992aed42edfe1d`  
		Last Modified: Wed, 11 Oct 2023 19:01:29 GMT  
		Size: 152.1 MB (152120097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac27c9546aa1f283f8fe0b0269e2e21b07890befb9173edceb6a902d78d34fa4`  
		Last Modified: Wed, 11 Oct 2023 19:02:08 GMT  
		Size: 72.0 MB (72017129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26497667a7318d0c727da6b25c96cf89a35d544539241b9a63e1233fdf383663`  
		Last Modified: Wed, 11 Oct 2023 19:02:01 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cbc8cc83039ef3af09a9acc553efab044532fa2ff1695bf5bf30570ecf40a3`  
		Last Modified: Wed, 11 Oct 2023 19:02:01 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
