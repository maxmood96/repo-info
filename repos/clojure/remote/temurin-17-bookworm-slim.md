## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:9827375da60adbad0f20757d3af1595985cd85fbd7f7a2d79dffe32f1e444691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5c893bb947972dd851173e9c0da8dc58eb64c04da302fbfff2d0e532539ac2b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243062738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28930f1987fd801242aaca4e588fa144071b85a102547ac34d17f360e103dd89`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:52:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 14:19:46 GMT
COPY dir:df4bc774e538040069d2de3701d4e1bdcb670139eb43073b03a326d09099ff77 in /opt/java/openjdk 
# Wed, 17 Jan 2024 14:19:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 14:24:18 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 17 Jan 2024 14:24:18 GMT
WORKDIR /tmp
# Wed, 17 Jan 2024 14:24:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 17 Jan 2024 14:24:37 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 17 Jan 2024 14:24:37 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 17 Jan 2024 14:24:37 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 17 Jan 2024 14:24:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253a46fd3dbe7a206ac008f95cf1f4bf7a0a42da2fe3654b652e9c9dae11d877`  
		Last Modified: Wed, 17 Jan 2024 14:56:59 GMT  
		Size: 144.9 MB (144873978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8a4a6c9da68fa728471937be6016c403d0cfd5c1905a36f0ed70a76f4ca0adb`  
		Last Modified: Wed, 17 Jan 2024 15:01:57 GMT  
		Size: 69.1 MB (69061821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58893bcc55cdd303e362d81348dac630b7f353758aae5859befbbd1dc8767039`  
		Last Modified: Wed, 17 Jan 2024 15:01:48 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da57df8c1c0ed2cac404a38efe6cf01021602350f3a06cffa6888759ae32af9`  
		Last Modified: Wed, 17 Jan 2024 15:01:48 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:042a583d299f160ab8482cde90f4adcba7bc7908fa5e7ccb6e0e1e809f2e55a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241657403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de5ac0b3972ad16da4bfc3bf70c241e709dbe00f12cf23b45d6daedafc9385fb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:44 GMT
ADD file:70e4f0c71f88c97c8db279b998c10d4943954d304ff9f51875c3699a4dc5ee4e in / 
# Thu, 11 Jan 2024 02:40:45 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 07:59:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 17 Jan 2024 09:28:39 GMT
COPY dir:5c06fb4b5daaa6784ba170c718d211b83c290b42eddb2ce95b7a2b1603c507ca in /opt/java/openjdk 
# Wed, 17 Jan 2024 09:28:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jan 2024 09:32:26 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 17 Jan 2024 09:32:27 GMT
WORKDIR /tmp
# Wed, 17 Jan 2024 09:32:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 17 Jan 2024 09:32:42 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 17 Jan 2024 09:32:42 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 17 Jan 2024 09:32:42 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 17 Jan 2024 09:32:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a5573528b1f0cf2f5d87c94fe0aee9d8967d5de98258be9303c3c6fa477824ec`  
		Last Modified: Thu, 11 Jan 2024 02:44:04 GMT  
		Size: 29.2 MB (29157335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9ec6808b922620606ea5e24590df6eaa935e6797301a16b35c7cca4bd3a011c`  
		Last Modified: Wed, 17 Jan 2024 09:42:10 GMT  
		Size: 143.7 MB (143681766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590898266f4c13fc86518f3f4936f1320f8384df77224c49df5d0571ac826ebc`  
		Last Modified: Wed, 17 Jan 2024 09:44:19 GMT  
		Size: 68.8 MB (68817288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897496155ff8302d76e8ab35ba78d482c9e0d6d41d665adfa51c9f8186efe9f2`  
		Last Modified: Wed, 17 Jan 2024 09:44:12 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb523ae9d7bb0ae4f305707d0eb993dc86ba47940901de017d9c67281833749b`  
		Last Modified: Wed, 17 Jan 2024 09:44:12 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
