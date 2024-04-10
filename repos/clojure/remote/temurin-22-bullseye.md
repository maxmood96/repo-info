## `clojure:temurin-22-bullseye`

```console
$ docker pull clojure@sha256:49f2fabfdc4cbb642a07c55dc61900cf0c73670843cd15ea6e2844bc5f32dad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `clojure:temurin-22-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dd0409461a6bc61f78993bbf36552fed00b91114e0977b06c132e7002aab5f99
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.7 MB (278733278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45425214a1b4902dda45b737911e8047c6d94735f1a4009cba2ab2be5856f90b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:30 GMT
ADD file:6fedb173fe261ff0e13b004ca692b7edcc74dcc3c4384fee092b96ef9508992c in / 
# Wed, 10 Apr 2024 00:40:30 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:39:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 18:10:59 GMT
COPY dir:804c07f15e876d329ef9551fe4e0597856a4396e905a8f833a1110ebfd35dfdc in /opt/java/openjdk 
# Wed, 10 Apr 2024 18:11:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 18:12:59 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 10 Apr 2024 18:12:59 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 18:13:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -sLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Wed, 10 Apr 2024 18:13:15 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 10 Apr 2024 18:13:15 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 10 Apr 2024 18:13:15 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 10 Apr 2024 18:13:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:197947a07d5f6c6ff020ca65dcea4e52671f85f67bee1b59af46cb0dc36580d9`  
		Last Modified: Wed, 10 Apr 2024 00:44:24 GMT  
		Size: 53.7 MB (53729176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453e0e45824683f2713a59af9cbd4793284df183e3286817c53b364313825b61`  
		Last Modified: Wed, 10 Apr 2024 18:25:25 GMT  
		Size: 155.9 MB (155861708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:954306fa647967a8a5b8fc10877886db9cefcf8653d8b4183083367c04008618`  
		Last Modified: Wed, 10 Apr 2024 18:27:02 GMT  
		Size: 69.1 MB (69141379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a83650e07ec9b789806ab33450ff275de8051bbd240392b0edf1deb2d8549a`  
		Last Modified: Wed, 10 Apr 2024 18:26:56 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3576cf7e979f68938322403224ff43e8571f098d5f16fee8e6ddd481d8f9279`  
		Last Modified: Wed, 10 Apr 2024 18:26:56 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
