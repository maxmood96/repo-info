## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:490b1fbc01a833983f03f7d328536834284d88df57b2f2a8db06426357e24cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:9d17c2ad4ad1373eeb2c2401f6ee4e18c08560c8f06fc1465cc0da4e51a3b286
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.7 MB (271713466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7350f0b7858eee0ae68f700a2af83eed408469333dfacab9d5e67e3b28b50f3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 27 Jul 2023 23:24:55 GMT
ADD file:b493776b6d91132ce50735e2d82076620774a1e0a690cf96777ddd6b85f513ef in / 
# Thu, 27 Jul 2023 23:24:55 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 03:13:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 03:19:44 GMT
COPY dir:a55dd3c38ddfa99e934b5bc495cb4ba08870462d2df73b37a545f734490942d5 in /opt/java/openjdk 
# Fri, 28 Jul 2023 03:19:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 03:23:59 GMT
ENV CLOJURE_VERSION=1.11.1.1347
# Fri, 28 Jul 2023 03:23:59 GMT
WORKDIR /tmp
# Fri, 28 Jul 2023 03:24:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "d9158bf3a1d92fbf8551656e47a86f42e93d10f1db9defa2124bfee206ce8c8f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 28 Jul 2023 03:24:15 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 28 Jul 2023 03:24:15 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 28 Jul 2023 03:24:15 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 28 Jul 2023 03:24:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9a9e034800a1747ea288f38f6087c036acac99dd3ec5255bf7798abd8c23a304`  
		Last Modified: Thu, 27 Jul 2023 23:29:45 GMT  
		Size: 55.1 MB (55055571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aebc877887922ff2413aab64a1fb8e4d446b9669ade73fd06cd4ed11c9c851d9`  
		Last Modified: Fri, 28 Jul 2023 03:31:21 GMT  
		Size: 144.8 MB (144773747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:284c7df54e7a09b04cd4fdfa880e1e4c83882a81edb6646d5bfadee916782a28`  
		Last Modified: Fri, 28 Jul 2023 03:32:21 GMT  
		Size: 71.9 MB (71883132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e83a25c6f93740d37818a9df44f7b99273cb4b897e104801b53a5bd76f83106`  
		Last Modified: Fri, 28 Jul 2023 03:32:13 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95761c97a68b7272c16bfca6b705abaa78e608c2df96266c6947f6fb53cce8ef`  
		Last Modified: Fri, 28 Jul 2023 03:32:14 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:af4c954c870d3f44f7d9ce64065a218c0b84c0b8aa7110a310a62c0d8c8bbee5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269245128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8110636ed6bd9e13626e76197b74fc8c3a2e1e5914c5e0eb740ad594da8216f8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:07 GMT
ADD file:a0144d077c2c6b73bbb5f7e7b8e6b58e4127de2a5faf907cd4e83e4d83437fad in / 
# Thu, 27 Jul 2023 23:43:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 14:29:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 28 Jul 2023 14:35:02 GMT
COPY dir:ea833e6c6c81bc32cfded5d05d30b781acc802f6c770c2720afc9a9f14f4a7d5 in /opt/java/openjdk 
# Fri, 28 Jul 2023 14:35:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 28 Jul 2023 14:36:48 GMT
ENV CLOJURE_VERSION=1.11.1.1347
# Fri, 28 Jul 2023 14:36:48 GMT
WORKDIR /tmp
# Fri, 28 Jul 2023 14:37:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "d9158bf3a1d92fbf8551656e47a86f42e93d10f1db9defa2124bfee206ce8c8f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 28 Jul 2023 14:37:02 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 28 Jul 2023 14:37:02 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 28 Jul 2023 14:37:02 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 28 Jul 2023 14:37:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:49185a1a3bc353699370ac57d50a7b7234b59616b6aebde79ba6a0a0314bb107`  
		Last Modified: Thu, 27 Jul 2023 23:46:34 GMT  
		Size: 53.7 MB (53704790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d0f61795693efb86b2bc273c0ea30def7d3c4e57a24be4dac110415235a921`  
		Last Modified: Fri, 28 Jul 2023 14:43:11 GMT  
		Size: 143.5 MB (143538050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac59930209f31b09e9de58d9372cbc07716247c908bcacd77c1fbdd325ef3c6`  
		Last Modified: Fri, 28 Jul 2023 14:44:05 GMT  
		Size: 72.0 MB (72001272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e3e1e09cbf93d3710468dc4c9fe58ee3ef880aac80ad317e1d9b0c6a74324f`  
		Last Modified: Fri, 28 Jul 2023 14:43:58 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f6a583e146b8671482e73054f65e6db1527ad0620c6b3f4f6a6756c7a7ddcb`  
		Last Modified: Fri, 28 Jul 2023 14:43:58 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
