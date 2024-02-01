## `clojure:temurin-21-bookworm-slim`

```console
$ docker pull clojure@sha256:0169e08e84b4db5dabf288775a4a5d7e142dd7c1d2dacc277de0e4a81e7b0f4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-21-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c23bf46c38f15cbb7f50a58a26b9c056ce31989c24fa9ab8cd18b7373c481733
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 MB (257799931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31d07c064d0f3565085974a42addec49147fba6fe594bff21ba679a017cb432`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:18 GMT
ADD file:af0f4e41d68b67ca88a1ce6297326159e18e27670d7bfc0bf5804a4e2b268cc8 in / 
# Wed, 31 Jan 2024 22:35:18 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:43:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 23:59:45 GMT
COPY dir:64a8841762a9afbd2fb8b4cf497b2dee87765737d44ff0387ce1cfc51371c9a2 in /opt/java/openjdk 
# Wed, 31 Jan 2024 23:59:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 00:01:35 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 01 Feb 2024 00:01:35 GMT
WORKDIR /tmp
# Thu, 01 Feb 2024 00:01:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 01 Feb 2024 00:01:53 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 01 Feb 2024 00:01:54 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 01 Feb 2024 00:01:54 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Feb 2024 00:01:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34c503f10693817d696b8ba77e56f4018337145c12d28ffd7e52fb4461160eb`  
		Last Modified: Thu, 01 Feb 2024 00:15:59 GMT  
		Size: 159.6 MB (159582944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2691436a4c027f7567cd9b5ab6110c4c81d7aed805ca5db7e67412db056ec113`  
		Last Modified: Thu, 01 Feb 2024 00:17:47 GMT  
		Size: 69.1 MB (69065505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f77832ee5ef4fcacced4d555c56044bf9e015ab72d219f8a465fe3b2839e4147`  
		Last Modified: Thu, 01 Feb 2024 00:17:38 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072f126db3827c3b9b0375c6d86b595e3afb30bfcef99ab7013d300cdae8c821`  
		Last Modified: Thu, 01 Feb 2024 00:17:39 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-21-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4e229f62818df0b1a6868cd8ab10c28d9e464b5d087c435d8f95f09828e7fc0e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255786049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9a7ee5050acefea2d550e3cc4abb26249830bc7ffbeacc2c26ed0688cdeac0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:26 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
# Wed, 31 Jan 2024 22:44:27 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:20:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 06:34:37 GMT
COPY dir:ab40534e435f9942975c0e8b5454d6b7a8d69c445f8e0758c1bd9c500e157fca in /opt/java/openjdk 
# Thu, 01 Feb 2024 06:34:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:36:11 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 01 Feb 2024 06:36:11 GMT
WORKDIR /tmp
# Thu, 01 Feb 2024 06:36:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 01 Feb 2024 06:36:27 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 01 Feb 2024 06:36:27 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 01 Feb 2024 06:36:27 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Feb 2024 06:36:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d1d7326c58fd6ddc737de53bf6ee504553b7bdd6d8248bcecc77c81e94e46d`  
		Last Modified: Thu, 01 Feb 2024 06:49:07 GMT  
		Size: 157.8 MB (157784601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3f6ae12096dbf2ab876a679fd537cf5c9b1e5588b7992210a4f2ec25e903de`  
		Last Modified: Thu, 01 Feb 2024 06:50:45 GMT  
		Size: 68.8 MB (68819599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128c5428ac1876730f8cd85517cf3716ed7950d7c522352d8ed659517c37b227`  
		Last Modified: Thu, 01 Feb 2024 06:50:38 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4b0ad9fe62696cf02773a93cbf5a9ea801797e29c59182107d006edd185add8`  
		Last Modified: Thu, 01 Feb 2024 06:50:37 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
