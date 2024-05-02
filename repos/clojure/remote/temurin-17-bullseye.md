## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:a6915206d326daa552a072ef171e66e25ef036101f75083d2ccd916b755a3d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:f4c6a6a3c470d025fbbd647d338900aaeb605157bb28c632261467c51436d7dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269218761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8bf161feb97943cd688ed25366cef06395e82ee9d2637679d2272728c56897`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 May 2024 05:37:27 GMT
COPY dir:d78c0cec90816231fd61ebcd7c27b07c1af0064b89c255fd2a157e0b344541d4 in /opt/java/openjdk 
# Thu, 02 May 2024 05:37:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 05:39:46 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Thu, 02 May 2024 05:39:46 GMT
WORKDIR /tmp
# Thu, 02 May 2024 05:40:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Thu, 02 May 2024 05:40:04 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 02 May 2024 05:40:04 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 02 May 2024 05:40:04 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 02 May 2024 05:40:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:391faf0b4445debf40a16e0a0eabc23775d085761aa0ab4ced5a2239d961aaf7`  
		Last Modified: Thu, 02 May 2024 05:50:42 GMT  
		Size: 145.1 MB (145095180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5015e0148c268a95e4416dc50d87044d3751b57931197813394fd67ea76139b5`  
		Last Modified: Thu, 02 May 2024 05:52:21 GMT  
		Size: 69.0 MB (69023692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a0c63439583abea41a61025cfc7cca6704a664856efd433804935da2fa347b`  
		Last Modified: Thu, 02 May 2024 05:52:13 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0542834cea9bea7d9d374a8301d644b0cb74630b140cb76fb3548de99bedcc`  
		Last Modified: Thu, 02 May 2024 05:52:13 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6f89c891f6fa02863d4c0efcb2eaa099b58f1918653aae0804dfa656ed23e1bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.8 MB (266774257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15de5a4d8e78f3a8e4843b456edd532cee62e64ff90549fd55b61318ec962e7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:46 GMT
ADD file:3ebbb50438ec23ebe0c880a5421d505922771b7bd4202b5c8f839702dd726036 in / 
# Wed, 24 Apr 2024 04:10:46 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:44:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 02 May 2024 05:34:49 GMT
COPY dir:317487729b1812635c51c5f305bd9178bd957a141903eab756a1683874b5752b in /opt/java/openjdk 
# Thu, 02 May 2024 05:34:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 May 2024 05:36:47 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Thu, 02 May 2024 05:36:47 GMT
WORKDIR /tmp
# Thu, 02 May 2024 05:37:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Thu, 02 May 2024 05:37:01 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 02 May 2024 05:37:01 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 02 May 2024 05:37:01 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 02 May 2024 05:37:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:64d502aff46d2ed56e6228994304818b354d02b13d6122492c5d3e0886c92897`  
		Last Modified: Wed, 24 Apr 2024 04:14:26 GMT  
		Size: 53.7 MB (53739959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c72cc73ccc61231ef93582824dc792a5a36e2ce7cddcdeafe99bff48bd71e4`  
		Last Modified: Thu, 02 May 2024 05:46:01 GMT  
		Size: 143.9 MB (143891839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5e1a7a391544ddc77f93fb2f73f276d5551ddc546e00b24eb70c9f2b8e1bef`  
		Last Modified: Thu, 02 May 2024 05:47:32 GMT  
		Size: 69.1 MB (69141441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed3a43e4eaacfc3e68ee21805158bc97420eb49a73dc8d2807d59a7cb82906c`  
		Last Modified: Thu, 02 May 2024 05:47:26 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e8d8127660dcfe43221de7f19acdb3e8818ddfa143563560017db736192d6e`  
		Last Modified: Thu, 02 May 2024 05:47:26 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
