## `clojure:temurin-17-tools-deps-1.11.3.1456-bullseye-slim`

```console
$ docker pull clojure@sha256:71ca13a6a82eca88cd8ce7b2e29a72f51f4a55eb0d9db5c266c3903caf2acdef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.3.1456-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:8e0c41e683f578a1f9abc341d476c132c1689e35e5ca42f42724ba071836df49
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235155889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57d20eaa4aaba84ddfeae868669d202a6da405df4cd79956db2e998641a325b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 May 2024 05:37:51 GMT
COPY dir:d78c0cec90816231fd61ebcd7c27b07c1af0064b89c255fd2a157e0b344541d4 in /opt/java/openjdk 
# Thu, 02 May 2024 05:37:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 05:40:07 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Thu, 02 May 2024 05:40:07 GMT
WORKDIR /tmp
# Thu, 02 May 2024 05:40:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Thu, 02 May 2024 05:40:24 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 02 May 2024 05:40:24 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 02 May 2024 05:40:24 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 02 May 2024 05:40:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e268d530bb0340ef766b9e0f0d211389263a101865620f87d4fb5336aeb2801`  
		Last Modified: Thu, 02 May 2024 05:51:03 GMT  
		Size: 145.1 MB (145095139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3760eb37fd63324496e82ded55dedae4ae67246649d3bae455dd10b5313eb4`  
		Last Modified: Thu, 02 May 2024 05:52:37 GMT  
		Size: 58.6 MB (58625466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503ce6bb442ae12668cd65348f8aafdd1b2cd00a93ff4169a7df1396d7d4d689`  
		Last Modified: Thu, 02 May 2024 05:52:30 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff526a9950935c5d311e897b34fc23ad5732afd88218f945b027474b797785b`  
		Last Modified: Thu, 02 May 2024 05:52:30 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-1.11.3.1456-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ebfb2bbb028e5f3bb8f7a5df731feab04e68d1a74fa12c19810bc097bf3a428f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.7 MB (232728915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d082e546815d9f4cf8114476ef8ee3c7ebb9ac0af2f66cbe993c89b6786190b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:44:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 May 2024 05:35:12 GMT
COPY dir:317487729b1812635c51c5f305bd9178bd957a141903eab756a1683874b5752b in /opt/java/openjdk 
# Thu, 02 May 2024 05:35:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 05:37:03 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Thu, 02 May 2024 05:37:03 GMT
WORKDIR /tmp
# Thu, 02 May 2024 05:37:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Thu, 02 May 2024 05:37:17 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 02 May 2024 05:37:17 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 02 May 2024 05:37:18 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 02 May 2024 05:37:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a3b3d69cafffc3e133d39d891034eec7b1b1444b75b4e14daa56549f5561ab8`  
		Last Modified: Thu, 02 May 2024 05:46:18 GMT  
		Size: 143.9 MB (143891838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a4718338a92c0e645db5c25666ff1ae871c9dd00eda6223cf8610bea96ecdd`  
		Last Modified: Thu, 02 May 2024 05:47:48 GMT  
		Size: 58.7 MB (58748719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3147c0c1ce5ef1d5ab6dc9bf04606a6072e5f7ba9c4fc9635568881601283c42`  
		Last Modified: Thu, 02 May 2024 05:47:43 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4426c67e7a01507a9c4c0e38ae1bc09d5730b7999f43a0ef3b25e0f49e095c`  
		Last Modified: Thu, 02 May 2024 05:47:42 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
