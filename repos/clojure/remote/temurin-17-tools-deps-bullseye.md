## `clojure:temurin-17-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:706e7a99d6772b10223a85600f227b509cdca7c26a6142e3eb627d04a3b3c378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:623d0163a9e99ed3927b8bd21657344a24400e3b98713517b79c88a2625b6b0c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.5 MB (319514222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d03c9873cfe78027194ee281d6283b53f06aff7abe1b8364570369f551dbdc2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 12 Apr 2023 00:19:55 GMT
ADD file:f2d012660f882f319a5878a3f9ce285f488b8f90fad49ad238541cf72089e035 in / 
# Wed, 12 Apr 2023 00:19:56 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 08:10:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Apr 2023 20:08:38 GMT
COPY dir:097a611561277927a8e367a60640ce12877b7a6373689dec24d5cfb76f99c807 in /opt/java/openjdk 
# Wed, 26 Apr 2023 20:08:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Apr 2023 20:12:07 GMT
ENV CLOJURE_VERSION=1.11.1.1273
# Wed, 26 Apr 2023 20:12:07 GMT
WORKDIR /tmp
# Wed, 26 Apr 2023 20:12:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4938afe6c0690d2a6553141857742d94a7350c02b4fa57cd6a9c1b7cbe66492e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 26 Apr 2023 20:12:23 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 26 Apr 2023 20:12:23 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 26 Apr 2023 20:12:23 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Apr 2023 20:12:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b0248cf3e63c73d0e496a67807d056ca41d5e968b61087e8eca2cf4b9b4d7b99`  
		Last Modified: Wed, 12 Apr 2023 00:23:20 GMT  
		Size: 55.1 MB (55052736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e363e191094639c858d95dc4482d74ded984d3d69a9dc0e9278ea1712a1c3b51`  
		Last Modified: Wed, 26 Apr 2023 20:24:02 GMT  
		Size: 192.6 MB (192580410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac9ae2134961fc899ca7e22127897b2a5ae7333b46e6bdda67d974108f5fd9c`  
		Last Modified: Wed, 26 Apr 2023 20:26:35 GMT  
		Size: 71.9 MB (71880062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc9ae1c8b533e4feb4efcfc4b68fe1a5eb3177b27918c3973986c1282e33de8`  
		Last Modified: Wed, 26 Apr 2023 20:26:27 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab8eae14197a7abedc7fb7cef99bb32674dcfe7b96e46edd8112f6ee87cfa0c`  
		Last Modified: Wed, 26 Apr 2023 20:26:27 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d2347115ad51e39bdc612eb6b3d34481fef09ea2978facbb99f3f2012ccd0a87
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.1 MB (317078147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02574811dc15bb17b131908444fc02b9eff0a4f3002ca0015fd4ee3e4680d645`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 03 May 2023 00:22:41 GMT
ADD file:f930fdb659332a615b0042ca415d6d7feda9ba6b2f58222e3e5bbed326db4d40 in / 
# Wed, 03 May 2023 00:22:42 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:43:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 03 May 2023 17:48:34 GMT
COPY dir:d3d9f08d06fd1214b20f5d901cee398f498773bedf69f0d3cc795772967cfe44 in /opt/java/openjdk 
# Wed, 03 May 2023 17:48:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 17:50:20 GMT
ENV CLOJURE_VERSION=1.11.1.1273
# Wed, 03 May 2023 17:50:20 GMT
WORKDIR /tmp
# Wed, 03 May 2023 17:50:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4938afe6c0690d2a6553141857742d94a7350c02b4fa57cd6a9c1b7cbe66492e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 03 May 2023 17:50:34 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 03 May 2023 17:50:34 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 03 May 2023 17:50:34 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 03 May 2023 17:50:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d677c78be691f8dcbe9d44ce576b97ad205b3dd78557dc62794e59eb19553ee9`  
		Last Modified: Wed, 03 May 2023 00:25:31 GMT  
		Size: 53.7 MB (53692705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54e3dfe953384be82597fea580dc9ef9ebb8b53e65fc436e07311295d7e9202`  
		Last Modified: Wed, 03 May 2023 17:56:22 GMT  
		Size: 191.4 MB (191387699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c6ba92ee17a5cb76a13f0bd62679a4c815a62db1d5069ff99b799d2e3ab9d2`  
		Last Modified: Wed, 03 May 2023 17:57:22 GMT  
		Size: 72.0 MB (71996728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd9359668f28b1826964c8abfa6ba1833a6c7387dda4ff0f1948a1ec7df699f`  
		Last Modified: Wed, 03 May 2023 17:57:16 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43abc36873969757ad2678a9ac3fd005622909b4b716295ad43c31917ff4ee3`  
		Last Modified: Wed, 03 May 2023 17:57:16 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
