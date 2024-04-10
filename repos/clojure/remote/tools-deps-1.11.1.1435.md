## `clojure:tools-deps-1.11.1.1435`

```console
$ docker pull clojure@sha256:7dc600e9c6509e95a84253be543e0549fa0c1c819810c629a3a41ac0b88259a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:tools-deps-1.11.1.1435` - linux; amd64

```console
$ docker pull clojure@sha256:51dcf35cac2208a45df88ffcc90b23807790f993b7d48a3ff11713ae6be788b2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.6 MB (289636396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15cb719b5138bd3c859f15b4251b9a0e95f3983f44911d4370de5d66868d5fe1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:34 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
# Wed, 10 Apr 2024 01:50:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:16:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 06:16:06 GMT
COPY dir:64a8841762a9afbd2fb8b4cf497b2dee87765737d44ff0387ce1cfc51371c9a2 in /opt/java/openjdk 
# Wed, 10 Apr 2024 06:16:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:35:29 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 10 Apr 2024 06:35:29 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 06:35:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 10 Apr 2024 06:35:47 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 10 Apr 2024 06:35:48 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 10 Apr 2024 06:35:48 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 10 Apr 2024 06:35:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597273d7ee30733a9fdb1ec4cf7c6b4d77146cf3c37fafac5b543993c51e4b78`  
		Last Modified: Wed, 10 Apr 2024 06:38:49 GMT  
		Size: 159.6 MB (159582872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2e860ab960b7f92039d692c7ac541b57e02002f5c2b3543032aaff5503968a`  
		Last Modified: Wed, 10 Apr 2024 06:50:34 GMT  
		Size: 80.5 MB (80492144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa30f92e258ae0f436f915b90b99a6d7370b092eb5f2833be9440622450f3ae`  
		Last Modified: Wed, 10 Apr 2024 06:50:25 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3206367279ac37d88578fdea620fe9e807ee18fd1b8ffb899017654eece02876`  
		Last Modified: Wed, 10 Apr 2024 06:50:25 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:tools-deps-1.11.1.1435` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e98e7305bd0f79532f52212643d53412c364f379a8c733db591f6ac3816d5421
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.6 MB (287638212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f2e72dccc1c6af0553870bf771036bd3e0a152cb79e3b55e4aa81091272f34`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:12 GMT
ADD file:d795219dc83a41b5bb4106e62eebd31ceef0aae1b81541156eae5fe98e89337c in / 
# Wed, 10 Apr 2024 00:40:13 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:37:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 04:37:06 GMT
COPY dir:ab40534e435f9942975c0e8b5454d6b7a8d69c445f8e0758c1bd9c500e157fca in /opt/java/openjdk 
# Wed, 10 Apr 2024 04:37:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 04:54:36 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 10 Apr 2024 04:54:36 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 04:54:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 10 Apr 2024 04:54:52 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 10 Apr 2024 04:54:52 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 10 Apr 2024 04:54:52 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 10 Apr 2024 04:54:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1e92f3a395ff98a929e797a3c392bb6d0f05531068d34b81d3cd41ed6ce82ca4`  
		Last Modified: Wed, 10 Apr 2024 00:43:42 GMT  
		Size: 49.6 MB (49596265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d3dd9dac863ad9ab25765a41c50957c1f6ebaccff440acc13fd3d5bb05647f9`  
		Last Modified: Wed, 10 Apr 2024 04:57:37 GMT  
		Size: 157.8 MB (157784669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65132f4c7103699627f5798d272c6c02f77990d5da81cf11c72195e77ce69637`  
		Last Modified: Wed, 10 Apr 2024 05:08:59 GMT  
		Size: 80.3 MB (80256265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11093bc6c415073864754b3924d245177834edd46dbc4d399e2592bec8ed43fe`  
		Last Modified: Wed, 10 Apr 2024 05:08:50 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8338116eb135b65f6256728258a0b45fad5a5f389c852cfee3819d4e43caf6eb`  
		Last Modified: Wed, 10 Apr 2024 05:08:50 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
