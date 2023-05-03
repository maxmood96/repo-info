## `clojure:temurin-20-tools-deps-1.11.1.1273-bullseye-slim`

```console
$ docker pull clojure@sha256:6e01315796227992c6c43b41fe89164d8b478623d273975397f370a9afa7ecb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-20-tools-deps-1.11.1.1273-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7f905108cf6ea18f9e7b233140a95f080c8c0f065c98b909b187a0ba859472eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.7 MB (295728759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0106520c04d529cb0e41920cc4c5b8f0b1270a484330b8d93f875144d594c122`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 12 Apr 2023 00:20:06 GMT
ADD file:11b1acca3f68b5c5787e292ff8dbdd114964a7272bf3519ab07710cbc01a0838 in / 
# Wed, 12 Apr 2023 00:20:06 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:11:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Apr 2023 20:14:06 GMT
COPY dir:02736280d197ac4d1b6ebf68d948efb46e7eeffd579505356f8c94946dbcce6f in /opt/java/openjdk 
# Wed, 26 Apr 2023 20:14:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Apr 2023 20:15:14 GMT
ENV CLOJURE_VERSION=1.11.1.1273
# Wed, 26 Apr 2023 20:15:14 GMT
WORKDIR /tmp
# Wed, 26 Apr 2023 20:15:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4938afe6c0690d2a6553141857742d94a7350c02b4fa57cd6a9c1b7cbe66492e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 26 Apr 2023 20:15:30 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 26 Apr 2023 20:15:30 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 26 Apr 2023 20:15:30 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Apr 2023 20:15:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:26c5c85e47da3022f1bdb9a112103646c5c29517d757e95426f16e4bd9533405`  
		Last Modified: Wed, 12 Apr 2023 00:23:43 GMT  
		Size: 31.4 MB (31418228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cabfc7eac33e1c6a185b010546e68b0921d7e2d2b07054bdd7a3e1284ff10b6`  
		Last Modified: Wed, 26 Apr 2023 20:28:40 GMT  
		Size: 202.8 MB (202813973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89475d246f03d1b58f46083279b567d12c0fe2e1e41f79b16acd271648a5df6`  
		Last Modified: Wed, 26 Apr 2023 20:29:39 GMT  
		Size: 61.5 MB (61495545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976b154a09361cf1242cf2147d5fbb94226aa5fdbe629b9e5679eaeebc9be1b5`  
		Last Modified: Wed, 26 Apr 2023 20:29:32 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f973fd4bdf77cc050db569062d0d17fac61c0439a69ec771ee965696ceac88ee`  
		Last Modified: Wed, 26 Apr 2023 20:29:32 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-20-tools-deps-1.11.1.1273-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:38eabcc172fa42c424e6d080adf3eeed37f680429cb7556f69ef89e5a2d0d49c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.8 MB (292822504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce92585ffcab4081acd10f6fbfb62a060846fd180bd787671638b4cb1e8eb6f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 03 May 2023 17:51:22 GMT
COPY dir:f555428af67a610819205eec573e23f479077e0999818ee9dc0f3375599d21db in /opt/java/openjdk 
# Wed, 03 May 2023 17:51:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 17:52:09 GMT
ENV CLOJURE_VERSION=1.11.1.1273
# Wed, 03 May 2023 17:52:09 GMT
WORKDIR /tmp
# Wed, 03 May 2023 17:52:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4938afe6c0690d2a6553141857742d94a7350c02b4fa57cd6a9c1b7cbe66492e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 03 May 2023 17:52:23 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 03 May 2023 17:52:23 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 03 May 2023 17:52:23 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 03 May 2023 17:52:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428345b4e9aa28cfa10998d30caebabc2e8cc0a23cb3c5e1642b394643a3de24`  
		Last Modified: Wed, 03 May 2023 17:58:23 GMT  
		Size: 201.2 MB (201158010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417c7a64ae3e1de9f512338f755f60948915fababd0fd2dbb6b6490f9f3279c6`  
		Last Modified: Wed, 03 May 2023 17:58:54 GMT  
		Size: 61.6 MB (61610748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:622f515e353c736e9c6513f1974fecbc5d39579bbd4304128dfca1aa31f13847`  
		Last Modified: Wed, 03 May 2023 17:58:48 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579adddc825965271dc1a4dfefdfae60530387086570c732b7dbc7c58e25b025`  
		Last Modified: Wed, 03 May 2023 17:58:48 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
