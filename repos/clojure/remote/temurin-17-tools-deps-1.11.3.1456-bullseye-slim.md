## `clojure:temurin-17-tools-deps-1.11.3.1456-bullseye-slim`

```console
$ docker pull clojure@sha256:26525400abbe9d7a1d4680f8ac52260ee49ef4fc0a338930cc1148df70e941a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.3.1456-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9048043790a8c6f93255ab4943fb7f12cd06141f5544a76ac8a60f73aefcbbd4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235156093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16b2d642715550609ac411c84aae2db78596cf1aa0f9222e6ad241b291f2ad0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 21:25:34 GMT
COPY dir:61bea833528044db01491107d8c3fb583322243082c7798fd60ade98f7eb7613 in /opt/java/openjdk 
# Wed, 24 Apr 2024 21:25:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Apr 2024 19:35:41 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Thu, 25 Apr 2024 19:35:41 GMT
WORKDIR /tmp
# Thu, 25 Apr 2024 19:35:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Thu, 25 Apr 2024 19:35:58 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 25 Apr 2024 19:35:58 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 25 Apr 2024 19:35:58 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 25 Apr 2024 19:35:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7e18e44024b12fa79056e86f735c6c20697aa58245c774350b1e9ddca45558`  
		Last Modified: Wed, 24 Apr 2024 21:49:00 GMT  
		Size: 145.1 MB (145095322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b749e622f12cd31e66149d7ff988e08fc7ff81a0a5df5c31aa77ce06cf4737`  
		Last Modified: Thu, 25 Apr 2024 19:53:35 GMT  
		Size: 58.6 MB (58625490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad3881e187271bc55f336b3beea409bf87c69978733dae008c1a446329e1f09`  
		Last Modified: Thu, 25 Apr 2024 19:53:27 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2ce4f35db521fa18467e745b5bfab9654cfd5a326206c9d8c74830a04197a1`  
		Last Modified: Thu, 25 Apr 2024 19:53:27 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-1.11.3.1456-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ed46dd569b65d5d388388e6fa7624ef0e9b67f388b6b6debec779b2cead29b01
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.7 MB (232728952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646bbf17d40edd920bbd1e7923f856f0639584bf0598d35107b9dc4577dfa6f4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:44:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 19:09:57 GMT
COPY dir:894420f494a8d73ff0a7e5986ef0142218654b95343c81b2b9fc9a9d3ea0c174 in /opt/java/openjdk 
# Wed, 24 Apr 2024 19:10:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 25 Apr 2024 19:52:49 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Thu, 25 Apr 2024 19:52:49 GMT
WORKDIR /tmp
# Thu, 25 Apr 2024 19:53:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Thu, 25 Apr 2024 19:53:03 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 25 Apr 2024 19:53:03 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 25 Apr 2024 19:53:03 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 25 Apr 2024 19:53:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e3254ac111733cd25bc460b2088616d0660016859ecaff8c9aaf6f761abfcc9`  
		Last Modified: Wed, 24 Apr 2024 19:29:09 GMT  
		Size: 143.9 MB (143891815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55b9a186a8ad62ec91df6d465e480b5d1ea521a54e159e3ec73956b58c5157a5`  
		Last Modified: Thu, 25 Apr 2024 20:08:01 GMT  
		Size: 58.7 MB (58748783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ca521893c0a8f08cf768fb035be5a2f46738747a5d2026bae4bb599f9afce5`  
		Last Modified: Thu, 25 Apr 2024 20:07:55 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254a37df3802385fe038b1c160543c7541ad7031ddc5dee669622f4620b2a6a9`  
		Last Modified: Thu, 25 Apr 2024 20:07:55 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
