## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:549d22bb964f5eac4262fbe34ad337b39d1f8d5b99bc46319d006bbc8048650a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:fa1d5fef52ab0c1e91db86ee0941c30eda07f5c112b1936ffd1a61c9b6c5d629
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.7 MB (271726053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8d29991ea8348d88861f8236a09bcb0d8d04542966c80c1ac3a8119785d709`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 16 Aug 2023 00:59:57 GMT
ADD file:20f89ff93bfbd6c9fb1a97058a1f3de4485a8974e8a83892072c511fbd2e4134 in / 
# Wed, 16 Aug 2023 00:59:58 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 18:08:24 GMT
COPY dir:534dada44a8b7afe6fc6978f0ae46933b536905423b1ac2af86e550e59d392b1 in /opt/java/openjdk 
# Wed, 16 Aug 2023 18:08:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 18:10:48 GMT
ENV CLOJURE_VERSION=1.11.1.1386
# Wed, 16 Aug 2023 18:10:48 GMT
WORKDIR /tmp
# Wed, 16 Aug 2023 18:11:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3a09e2df4d3abd89b5b1286af0133a36a525ff3acfe1432f98b5c24b170940e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 16 Aug 2023 18:11:05 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 16 Aug 2023 18:11:05 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 16 Aug 2023 18:11:05 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 16 Aug 2023 18:11:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a70103cc499a199e10e379794c60aa524d9598587cc2bdfe2995642c2da8df7`  
		Last Modified: Wed, 16 Aug 2023 01:04:50 GMT  
		Size: 55.1 MB (55056621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4fbbfc9003ff6a7a7db701f4c4c225eecdff24e8d91f37e9d447417a6e458b2`  
		Last Modified: Wed, 16 Aug 2023 18:17:54 GMT  
		Size: 144.8 MB (144773721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:612cbcb17e320381f2769cc843fd470e3702a9d9579277c80c9ce5d1e3b9fc51`  
		Last Modified: Wed, 16 Aug 2023 18:19:34 GMT  
		Size: 71.9 MB (71894696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a36f8098736a3fbafae141eb6637bd4724910a0cdb7d47e1ab4262b0aedbeb4`  
		Last Modified: Wed, 16 Aug 2023 18:19:26 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b734e05a0eb50d066102acea508b255514670f5c064e2a73993b6cc0dd67d3ea`  
		Last Modified: Wed, 16 Aug 2023 18:19:26 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3655f9cfc208139628173b8efb27550a143e503a1ae3771ac37efbd4a3f72e7b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.3 MB (269252476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8779541109c561b73f4d4cd3013146c34f07650c6c2e9d782fcbffbb659fc74e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:03 GMT
ADD file:8973cddb2d84a543b71001635599951bea6485a3526ae4ff916443b584864c83 in / 
# Tue, 15 Aug 2023 23:40:04 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:25:20 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Wed, 16 Aug 2023 17:25:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Aug 2023 17:27:32 GMT
ENV CLOJURE_VERSION=1.11.1.1386
# Wed, 16 Aug 2023 17:27:33 GMT
WORKDIR /tmp
# Wed, 16 Aug 2023 17:27:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3a09e2df4d3abd89b5b1286af0133a36a525ff3acfe1432f98b5c24b170940e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 16 Aug 2023 17:27:47 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 16 Aug 2023 17:27:47 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 16 Aug 2023 17:27:47 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 16 Aug 2023 17:27:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e837d9f05c625de5b814b851adbc03559ba02ea7078f57c81a01e18fc65bf42b`  
		Last Modified: Tue, 15 Aug 2023 23:43:37 GMT  
		Size: 53.7 MB (53704779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:407f1b0394be128a63af2359d89c3282164b67cd2fac29716c6f2f5e348ec07a`  
		Last Modified: Wed, 16 Aug 2023 17:34:01 GMT  
		Size: 143.5 MB (143538089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f62ae6c1ea02b4bf225950b30fbf203a7854c4e564335874b0e84bdd3d2761e2`  
		Last Modified: Wed, 16 Aug 2023 17:35:43 GMT  
		Size: 72.0 MB (72008590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21797bd990a943cd569d1bb8c28b3aefcc954ca8f30841bd058916e7d76aa1f8`  
		Last Modified: Wed, 16 Aug 2023 17:35:36 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45756ad9a6ee4d24159602689ea0ab0758cfe6a014ea98a1d59e5ee92aaa796d`  
		Last Modified: Wed, 16 Aug 2023 17:35:36 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
