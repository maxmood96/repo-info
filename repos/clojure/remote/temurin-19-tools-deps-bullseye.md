## `clojure:temurin-19-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:deb67ae905a4bdfeee903a70d590299e072ed7836c869b68fed5d90fe40327cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-19-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:f9342eaa6ad06d1a9c3cf73ade9dd326094832c1b15c791514b02832bc708785
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.0 MB (328038263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb845bb09eecf833dc2bf2793213d9b7d572624ee3e73f492d8affbc2f3a743c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:45 GMT
ADD file:513c5d5e501279c21a05c1d8b66e5f0b02ee4b27f0b928706d92fd9ce11c1be6 in / 
# Wed, 01 Mar 2023 04:09:46 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:40:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 07:49:43 GMT
COPY dir:94cb5af8175285c10c94286222d8a35302f3f8c290e00011a75c67156659d6ab in /opt/java/openjdk 
# Wed, 01 Mar 2023 07:49:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 07:51:52 GMT
ENV CLOJURE_VERSION=1.11.1.1224
# Wed, 01 Mar 2023 07:51:52 GMT
WORKDIR /tmp
# Wed, 01 Mar 2023 07:52:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3bbab4d253eda43e3122fd5705014a69c44944a6dee8ea4d7d567afe157eb4ef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 01 Mar 2023 07:52:10 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 01 Mar 2023 07:52:10 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 01 Mar 2023 07:52:10 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 01 Mar 2023 07:52:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:32fb02163b6bb519a30f909008e852354dae10bdfd6b34190dbdfe8f15403ea0`  
		Last Modified: Wed, 01 Mar 2023 04:13:58 GMT  
		Size: 55.0 MB (55045922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28081d65626e3fe290ed0277941e3e5a31dee293f2403db18b27a4b41888fb76`  
		Last Modified: Wed, 01 Mar 2023 08:00:49 GMT  
		Size: 201.1 MB (201112993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155d789c076971240636e648df0565a2c47d08d743dcaae32e4593406a47f6b9`  
		Last Modified: Wed, 01 Mar 2023 08:01:54 GMT  
		Size: 71.9 MB (71878333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a0a8425b83fcad8b0534a53b75204d8392f067433f9a6955bb07c02926cd0e`  
		Last Modified: Wed, 01 Mar 2023 08:01:46 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d272e7dcaf18a9eaa9dec1fd8900ed325488f974ddac9d6dc9eb43c6dafd6595`  
		Last Modified: Wed, 01 Mar 2023 08:01:46 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-19-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:51afff9142638b85a30c3bad1d7ff73dcc08e94a8c9b69204256d3c7974de8a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325549397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6922c5ea796a78f04959c17b782e999e25d9910e92901cae8cd739faeb24b81`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:30 GMT
ADD file:a6a1df499d0d5b07fb366d776a11c42ddee6261e2425a921041b38e868192770 in / 
# Wed, 01 Mar 2023 02:20:30 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:01:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 03:09:13 GMT
COPY dir:9a6a873ca11063f6f04e7f088397a1fce771e2b1aa8590b72eb07158cfac883f in /opt/java/openjdk 
# Wed, 01 Mar 2023 03:09:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 03:11:05 GMT
ENV CLOJURE_VERSION=1.11.1.1224
# Wed, 01 Mar 2023 03:11:05 GMT
WORKDIR /tmp
# Wed, 01 Mar 2023 03:11:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3bbab4d253eda43e3122fd5705014a69c44944a6dee8ea4d7d567afe157eb4ef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 01 Mar 2023 03:11:20 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 01 Mar 2023 03:11:20 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 01 Mar 2023 03:11:20 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 01 Mar 2023 03:11:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0f5fe16b1836feccd4765ac5685fc7a7b9c73445cac94fc595d2ffbc3cb59a7a`  
		Last Modified: Wed, 01 Mar 2023 02:23:53 GMT  
		Size: 53.7 MB (53703215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f14b17f40d43b36c3ca31112958858ecb243428662f3cf865bcfd47ff1cf7c3`  
		Last Modified: Wed, 01 Mar 2023 03:19:11 GMT  
		Size: 199.9 MB (199855198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518bdcc6f1882b23e725217d8e8e30729dbf6c873bc7b5782bd51dfc5e3c4e45`  
		Last Modified: Wed, 01 Mar 2023 03:20:10 GMT  
		Size: 72.0 MB (71989969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0fd044c648cced530de0d94715206b41940d42e1fc15e5c1919d23fe5caedb1`  
		Last Modified: Wed, 01 Mar 2023 03:20:03 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e42887f255643daa3e383bd31d03821fbc6d06304d755832600c4db22810f6`  
		Last Modified: Wed, 01 Mar 2023 03:20:03 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
