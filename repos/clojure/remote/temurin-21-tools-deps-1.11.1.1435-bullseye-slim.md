## `clojure:temurin-21-tools-deps-1.11.1.1435-bullseye-slim`

```console
$ docker pull clojure@sha256:5e432a0850812e84ef728c0c0545bbf6654896fc0dfa83e35b189c21dd5471a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-21-tools-deps-1.11.1.1435-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:bf851e4bed1b5a755506344ca1af36deb177cf26134873282d450ea83b3140c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.6 MB (248559299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee499817ad091dbc093a0352c04bed74f238bbf60623a8c422339c9d683dc00b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:06:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 21:30:16 GMT
COPY dir:2191d32deb04bfc59d7fcf2244f16c5ecbe60498375dcea5599e5d16a61b7305 in /opt/java/openjdk 
# Wed, 24 Apr 2024 21:30:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 21:32:22 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 21:32:22 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 21:32:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 21:32:40 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 21:32:40 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 21:32:40 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 21:32:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f31587c5252b3caffe16871dd550d885250af905ced053200fb2873bf1072a0`  
		Last Modified: Wed, 24 Apr 2024 21:53:03 GMT  
		Size: 158.5 MB (158498331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f00f73d081c4477a03e14395fd0cc92f31a49eaa0b7348d5f8f4a12bd278d5`  
		Last Modified: Wed, 24 Apr 2024 21:54:58 GMT  
		Size: 58.6 MB (58625685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b071ae06bf85f6366f28e1726856cae3eba101b046305268aa962e3eaa888e8a`  
		Last Modified: Wed, 24 Apr 2024 21:54:51 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3122a9b8b993c1f2ff704e1e342d5d28319bab61a5061b9a5f0a60899a717d0e`  
		Last Modified: Wed, 24 Apr 2024 21:54:51 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-21-tools-deps-1.11.1.1435-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e5ca3c0496d4975bc4a1c8caf480d7483abeb1ff791b8f3d12aceb8626da3c57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.5 MB (245505993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8481778a94f53c95440e46c6e8ec99f344d9b2407bee09f708517a954921fd8a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:44:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Apr 2024 19:13:38 GMT
COPY dir:96a90c8e1c03defb238a6d560d8927dc81a1a58af3fce1471cbce5249ed27f38 in /opt/java/openjdk 
# Wed, 24 Apr 2024 19:13:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 19:15:20 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 24 Apr 2024 19:15:20 GMT
WORKDIR /tmp
# Wed, 24 Apr 2024 19:15:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 24 Apr 2024 19:15:34 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 24 Apr 2024 19:15:34 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 24 Apr 2024 19:15:35 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Apr 2024 19:15:35 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b61445db65f0a8ce0fe56d7dfc756b270a5ccfe3b05485ad28420003f1653940`  
		Last Modified: Wed, 24 Apr 2024 19:32:45 GMT  
		Size: 156.7 MB (156665487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:207ffdb2953dc5f9cdf039bb3057ec428b13dad9e276271bc0434db921e3a213`  
		Last Modified: Wed, 24 Apr 2024 19:34:25 GMT  
		Size: 58.8 MB (58752152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe4837f6ff480f3118e60ec80823b6ed891150160b69a35a98b370be6d58649`  
		Last Modified: Wed, 24 Apr 2024 19:34:18 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f7858dab153f698b3ae5e417725faecdfeffe2c062c0ba871187578ad8c3fc`  
		Last Modified: Wed, 24 Apr 2024 19:34:18 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
