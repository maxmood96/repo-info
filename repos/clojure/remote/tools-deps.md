## `clojure:tools-deps`

```console
$ docker pull clojure@sha256:591997825711da0f9026916bc5eca091f92b60ae12c65ac5b2f48fe6161dc081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:170d9e3cda353c7309ab82ee0534c9bdf039e693b859c7ec47922a9c0e5fae74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289661683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9411326d95ff0c6d0cf6910de912dd9177fb119a0e6c273863c992ad0e0806a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:05 GMT
ADD file:6d9e71f0d3afb0b288cf2c06425795d528a142872692072ab1cd1ad275b67d1f in / 
# Wed, 31 Jan 2024 22:35:06 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:41:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 23:41:29 GMT
COPY dir:64a8841762a9afbd2fb8b4cf497b2dee87765737d44ff0387ce1cfc51371c9a2 in /opt/java/openjdk 
# Wed, 31 Jan 2024 23:41:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 00:01:11 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 01 Feb 2024 00:01:11 GMT
WORKDIR /tmp
# Thu, 01 Feb 2024 00:01:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 01 Feb 2024 00:01:30 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 01 Feb 2024 00:01:30 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 01 Feb 2024 00:01:30 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Feb 2024 00:01:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a299ae9cfd996c1149a699d36cdaa76fa332c8e9d66d6678fa9a231d9ead04c`  
		Last Modified: Wed, 31 Jan 2024 22:39:27 GMT  
		Size: 49.6 MB (49583754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c299f193861b5d2b1adc713471ff68491754a53d8441f8b4078311e342849d`  
		Last Modified: Thu, 01 Feb 2024 00:04:55 GMT  
		Size: 159.6 MB (159582922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eea30ae08f0ecebb58e008a3dc8809da5c03df5e7e172091cca00758904c8d4`  
		Last Modified: Thu, 01 Feb 2024 00:17:17 GMT  
		Size: 80.5 MB (80493989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de28cb38d9dc25aa171be0469c2ab4fb11a2efc472f49c090ae49fe737dd02a7`  
		Last Modified: Thu, 01 Feb 2024 00:17:08 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:853f50320f25782e127c0d6a5f03b5bb7b26cb0a003242086d35f41254de81e9`  
		Last Modified: Thu, 01 Feb 2024 00:17:08 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bbd56772b4bb8e8ec0cfe68cb3a4c41318d68cc3ea72600beade30ee63d7c970
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.7 MB (287659977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb8fc00b33b9309b0388e547c06039c7fcd96923db452326a400b1dcb69ce06`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:15 GMT
ADD file:8bc7f537dd3dc4b92ec9006080fd563cc79205ee1ec3f456d03e869125a5bc21 in / 
# Wed, 31 Jan 2024 22:44:15 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:18:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 06:18:22 GMT
COPY dir:ab40534e435f9942975c0e8b5454d6b7a8d69c445f8e0758c1bd9c500e157fca in /opt/java/openjdk 
# Thu, 01 Feb 2024 06:18:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:35:51 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 01 Feb 2024 06:35:51 GMT
WORKDIR /tmp
# Thu, 01 Feb 2024 06:36:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 01 Feb 2024 06:36:08 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 01 Feb 2024 06:36:08 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 01 Feb 2024 06:36:08 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Feb 2024 06:36:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:66932e2b787d33a94ee3eb8b489be6e6838b29f5c1d732262da306da9b1f2eed`  
		Last Modified: Wed, 31 Jan 2024 22:47:40 GMT  
		Size: 49.6 MB (49615296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f111917e60b82ad9b0f922efe4aa47bf72c7fa9d4456fcc76e7bdcf523cda38`  
		Last Modified: Thu, 01 Feb 2024 06:38:45 GMT  
		Size: 157.8 MB (157784591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228374e60b99c73ed6e0dbdf843113d89483e8d09b7d88d689b4e9a9d1d52a44`  
		Last Modified: Thu, 01 Feb 2024 06:50:16 GMT  
		Size: 80.3 MB (80259073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9675a4598d55b5baaffcd7a947e661340755e3b92a2c1c88e3224a292443bb38`  
		Last Modified: Thu, 01 Feb 2024 06:50:07 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31cfd822f806db1f7bfab42c5dee9355cd3ccadb66a0c6080460f91a211e99b`  
		Last Modified: Thu, 01 Feb 2024 06:50:07 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
