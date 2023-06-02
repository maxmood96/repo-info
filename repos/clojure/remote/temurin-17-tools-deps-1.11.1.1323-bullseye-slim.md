## `clojure:temurin-17-tools-deps-1.11.1.1323-bullseye-slim`

```console
$ docker pull clojure@sha256:2a8acea04d005b1836553f69fc36ae1cc9b1a1aeec49b4baccb55d6c10e9f917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.1.1323-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6aeae59af9360abcbe33bedf37c3af1971433e638d4d44b221a88d6ade8ada28
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285479916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f838f91b1db75c84e3b2c678a936d2774efa7c0f3bb609daca0939e6796d043b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 04:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 May 2023 04:18:39 GMT
COPY dir:05dd898ce921dff423e175db4bfabc77c7b70b060cfa18a18ee060c7533c567b in /opt/java/openjdk 
# Tue, 23 May 2023 08:10:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 08:12:01 GMT
ENV CLOJURE_VERSION=1.11.1.1323
# Tue, 23 May 2023 08:12:01 GMT
WORKDIR /tmp
# Tue, 23 May 2023 08:12:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "c4666f0e2c2397b91554befd71ff6149b2e89acbf90400e1dcf557526cfb593d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 23 May 2023 08:12:16 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 23 May 2023 08:12:17 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 23 May 2023 08:12:17 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 23 May 2023 08:12:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e304d0221eddeca3682794711387f6677072df1d6fd9df02ff4f7487148d1df`  
		Last Modified: Tue, 23 May 2023 04:20:31 GMT  
		Size: 192.6 MB (192580374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e328837cc756ae5c2304e13636ea06cec8448dac82b425a7069d525e7bfabad`  
		Last Modified: Tue, 23 May 2023 08:19:40 GMT  
		Size: 61.5 MB (61494940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d860ca0bef0ee3ba08402af9e1b97b3ea893c90c786cb66c17ee997f8148f7cb`  
		Last Modified: Tue, 23 May 2023 08:19:33 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cbc6df53d547e76db80b3d30cfd72838ab93cbc798fe724baf57d1249c07225`  
		Last Modified: Tue, 23 May 2023 08:19:33 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-1.11.1.1323-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8b47d17245ecd383dc942a5c00e6851b24b838901050e0b732790554d05d9e3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.1 MB (283050277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036f1d9751f3b38fba7016f0a917d644cd249dbf184978b0dc7802f7bb9880e8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:24:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 02 Jun 2023 01:19:09 GMT
COPY dir:61701986201ad0602f1c757565ae6dd6ea34364a0201d8cacf0d9cb6de78ccff in /opt/java/openjdk 
# Fri, 02 Jun 2023 01:19:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Jun 2023 01:21:09 GMT
ENV CLOJURE_VERSION=1.11.1.1323
# Fri, 02 Jun 2023 01:21:09 GMT
WORKDIR /tmp
# Fri, 02 Jun 2023 01:21:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "c4666f0e2c2397b91554befd71ff6149b2e89acbf90400e1dcf557526cfb593d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 02 Jun 2023 01:21:23 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 02 Jun 2023 01:21:23 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 02 Jun 2023 01:21:23 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 02 Jun 2023 01:21:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fef9843ee3a4a3c4e66d6cadc553539db33fb835faee455b450d59d554959ee`  
		Last Modified: Fri, 02 Jun 2023 01:27:17 GMT  
		Size: 191.4 MB (191387656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f67382e0bc60c397bbb707330e73a8b70f9add541a88131fbca4b2022a6730c`  
		Last Modified: Fri, 02 Jun 2023 01:28:49 GMT  
		Size: 61.6 MB (61608856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703ab6a62731c9eef194863a5cd973862251d90401ca748886b2a57b9f481388`  
		Last Modified: Fri, 02 Jun 2023 01:28:42 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b972c5964b1c434978784afaee09ff28d8e08a30172237bdcfed416f8460ac`  
		Last Modified: Fri, 02 Jun 2023 01:28:42 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
