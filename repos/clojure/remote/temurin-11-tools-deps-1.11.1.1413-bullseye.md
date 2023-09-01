## `clojure:temurin-11-tools-deps-1.11.1.1413-bullseye`

```console
$ docker pull clojure@sha256:45c17225ef43a3535a4ad043c7aeaf15f09515456dabcbcf79c4c019af72ad8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-1.11.1.1413-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:fd095c8534ee93dba361a3a8e3c6a9017508312c28e737fa234421b96b59c8d8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 MB (271761182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8920d27d746cf7a960766ac973e83b69d9f1c41f2f246c9cc10428fcc025d461`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 16 Aug 2023 00:59:57 GMT
ADD file:20f89ff93bfbd6c9fb1a97058a1f3de4485a8974e8a83892072c511fbd2e4134 in / 
# Wed, 16 Aug 2023 00:59:58 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:26:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 31 Aug 2023 23:22:26 GMT
COPY dir:9c2351d5d5cdf669213a7cfcfa52bd6bd8e9fc36b0a8e93328276d7280e1bab3 in /opt/java/openjdk 
# Thu, 31 Aug 2023 23:22:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Aug 2023 23:29:28 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Thu, 31 Aug 2023 23:29:29 GMT
WORKDIR /tmp
# Thu, 31 Aug 2023 23:29:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 31 Aug 2023 23:29:48 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 31 Aug 2023 23:29:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6a70103cc499a199e10e379794c60aa524d9598587cc2bdfe2995642c2da8df7`  
		Last Modified: Wed, 16 Aug 2023 01:04:50 GMT  
		Size: 55.1 MB (55056621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab352bd56ec5464a5d56238b020eb3ec17516ac2525535fdf339dacbad129b6`  
		Last Modified: Thu, 31 Aug 2023 23:41:03 GMT  
		Size: 144.8 MB (144826073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b22774749efd55fe031cbdfa0a386098a026fc4631de0726a41e6bca67e9d9`  
		Last Modified: Thu, 31 Aug 2023 23:43:00 GMT  
		Size: 71.9 MB (71877870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f089de89d382ef569a275846f9d8a0ce1563a42a78d4461b60071bdaee3ac906`  
		Last Modified: Thu, 31 Aug 2023 23:42:52 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-1.11.1.1413-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7f6d7e1377ae3a3f54a6511282c4ffdbb2b4e6eafdbe5cbcd11d094def76e6b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.3 MB (267273565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7526d72ca5d2978efc3df5f76b18691decedb48a4b7c67df4530b0b26dcf5616`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:03 GMT
ADD file:8973cddb2d84a543b71001635599951bea6485a3526ae4ff916443b584864c83 in / 
# Tue, 15 Aug 2023 23:40:04 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 31 Aug 2023 22:19:28 GMT
COPY dir:5893aa8259c326023fbed778b793e0c69a0437031d8da5faa0a285cd6e549029 in /opt/java/openjdk 
# Thu, 31 Aug 2023 22:19:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 31 Aug 2023 22:23:07 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Thu, 31 Aug 2023 22:23:07 GMT
WORKDIR /tmp
# Thu, 31 Aug 2023 22:23:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 31 Aug 2023 22:23:24 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 31 Aug 2023 22:23:24 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e837d9f05c625de5b814b851adbc03559ba02ea7078f57c81a01e18fc65bf42b`  
		Last Modified: Tue, 15 Aug 2023 23:43:37 GMT  
		Size: 53.7 MB (53704779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e54d5a5b9b0ab064bd62ec31a004d4656e7dfbfcf689a0b384a216a9e32a301`  
		Last Modified: Thu, 31 Aug 2023 22:29:51 GMT  
		Size: 141.6 MB (141570304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbfe2f527f539d9f6bb7dd3972bc9f857ec69e5b60fbc7fa411a459b6e8da14d`  
		Last Modified: Thu, 31 Aug 2023 22:31:33 GMT  
		Size: 72.0 MB (71997864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6f51d0c8055541e1ca4946e8a62764a6bc6e80fc34e52edd29723ff2fe20db`  
		Last Modified: Thu, 31 Aug 2023 22:31:26 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
