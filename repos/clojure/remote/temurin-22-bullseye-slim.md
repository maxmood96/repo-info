## `clojure:temurin-22-bullseye-slim`

```console
$ docker pull clojure@sha256:8b5ddedda455ce84c070eceb0e9cd001c7ca1163ee607933fb1a2a93d473a627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-22-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:840585661590c52dc404eb9a6b0fe767e3b76d507604aa6740bcebf5d5384382
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.8 MB (246776191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4179ddc154bbcd2854e6dbc9eb3994e8b9df72f39864367f08bc524150ecbe`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 21:34:51 GMT
COPY dir:26aa9b736de249ab67b8c50e579c4c188c999c32408e8bbdcde37c30c2d0e7d3 in /opt/java/openjdk 
# Wed, 24 Apr 2024 21:34:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 21:37:01 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 21:37:01 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:37:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 21:37:18 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 21:37:18 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 21:37:18 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 21:37:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086f333d7ea40659a9a5e7a8b1ae8ac89112d5aaed9f665450c7a728aeb3bf32`  
		Last Modified: Wed, 24 Apr 2024 21:56:58 GMT  
		Size: 156.7 MB (156714948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b15868f1185f698d5f5af6704bab7965169d7f3af124edeb45a85e1e28e6c7a`  
		Last Modified: Wed, 24 Apr 2024 21:58:33 GMT  
		Size: 58.6 MB (58625961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9245daa065c94c436d15678af2d99005b00aa3c1e0dd02635300c3a696f95c3b`  
		Last Modified: Wed, 24 Apr 2024 21:58:26 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9398bda52fdcaa4477566aef40fca42b93ac1556a1560dc9a0ba00ba37a90378`  
		Last Modified: Wed, 24 Apr 2024 21:58:26 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-22-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a45e835aa838bf49e0bc1d4013d812c40fcd571e06b7048caafcd7b93d60a6af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243578263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ba9ad3e77bfe5a2d75e25c4db50c943d5285d179e36ece38e6e1b4a4d633280`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:44:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 19:17:17 GMT
COPY dir:8db4aa7d00469f3c784932412aa95caf68b05146a02559362a91df21ce463ad4 in /opt/java/openjdk 
# Wed, 24 Apr 2024 19:17:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 19:18:58 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 19:18:58 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 19:19:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 19:19:14 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 19:19:14 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 19:19:14 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 19:19:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81b0d6af894922630c0bf5aae1320817996daadf3bc262b667f8bff3921d8676`  
		Last Modified: Wed, 24 Apr 2024 19:36:08 GMT  
		Size: 154.7 MB (154737725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa6f8438f6f6a7419408d3e8e7835ec587890995a11a7bbc3c6736b1ea40483`  
		Last Modified: Wed, 24 Apr 2024 19:37:31 GMT  
		Size: 58.8 MB (58752185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afabcdb83d7b2b5eb470ee6c7ab974d8f64432a6b31a9f366df02fc38725883c`  
		Last Modified: Wed, 24 Apr 2024 19:37:24 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f36130b1a80ba1b6ba4db7cf44225ddc78cc090f4393cf819d5f119ef7ba67`  
		Last Modified: Wed, 24 Apr 2024 19:37:24 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
