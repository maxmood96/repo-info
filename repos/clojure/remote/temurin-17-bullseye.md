## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:e682121ad2f528a74a0ef9384e56a03b76c12a12b79332c8a461565cd3777c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:2cfedb04f387222bdd9d604536a62f05e8d8b074197647fba826fda71c554596
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294779762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a23230325370f93b30dce1b3f56fca33c3c85e74bce78f0448b6ab5aa34159bd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:42 GMT
ADD file:26702ba2c3e94cb21cdb3c550cf01cf848823d160f3417b559116d4c718e5df0 in / 
# Tue, 25 Oct 2022 01:43:42 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:32:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 07 Nov 2022 20:47:28 GMT
COPY dir:fa15c3254735d08fe4cb4c940d6fc08efc9755ff0499a6eb8e51c961cea48d5c in /opt/java/openjdk 
# Mon, 07 Nov 2022 20:47:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 20:51:15 GMT
ENV CLOJURE_VERSION=1.11.1.1189
# Mon, 07 Nov 2022 20:51:15 GMT
WORKDIR /tmp
# Mon, 07 Nov 2022 20:51:31 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1afd91b165776615eca84cce2271e5fe5d5818c55dee0f082b1304bb1464b3e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Mon, 07 Nov 2022 20:51:32 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Mon, 07 Nov 2022 20:51:32 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Mon, 07 Nov 2022 20:51:32 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 07 Nov 2022 20:51:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:17c9e6141fdb3387e5a1c07d4f9b6a05ac1498e96029fa3ea55470d4504f7770`  
		Last Modified: Tue, 25 Oct 2022 01:47:28 GMT  
		Size: 55.0 MB (55046332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b66875a43c96e16e03416e5d3e0d399e19e6ebbd34b69c21f639ea24b829431`  
		Last Modified: Mon, 07 Nov 2022 20:57:33 GMT  
		Size: 192.4 MB (192431266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c368d77159b02f226b8cc1994fa4121d86774055d77fa613eceef4fc7e08079e`  
		Last Modified: Mon, 07 Nov 2022 21:00:45 GMT  
		Size: 47.3 MB (47301144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6513d423d77352485084182373e4810ac47c84e68846c233a0f2cf53bad687e8`  
		Last Modified: Mon, 07 Nov 2022 21:00:39 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4aae3495e4043e2e0be4c6ea13eee3a570c649d269e01517102c821af848ef1`  
		Last Modified: Mon, 07 Nov 2022 21:00:39 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1f051043f4157a88d673f973e72129d0dd3cea9e6b1d189329ca2e29a3244452
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.2 MB (292212769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd8dadcc15007fdccb2de826aea8c2f1fadbfe8c529b4dcd472d099b93f75eca`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 25 Oct 2022 05:45:55 GMT
ADD file:b16745ece8ef84c028d7e9ac4bf026ac64f885d4170bfcc9d435f237144a1b99 in / 
# Tue, 25 Oct 2022 05:45:56 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 23:53:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 07 Nov 2022 21:03:20 GMT
COPY dir:36850aee002fdc5445f17d75b8266c48f8e705973ece815c3b53d28b6656ac3e in /opt/java/openjdk 
# Mon, 07 Nov 2022 21:03:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 21:06:32 GMT
ENV CLOJURE_VERSION=1.11.1.1189
# Mon, 07 Nov 2022 21:06:32 GMT
WORKDIR /tmp
# Mon, 07 Nov 2022 21:06:46 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1afd91b165776615eca84cce2271e5fe5d5818c55dee0f082b1304bb1464b3e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Mon, 07 Nov 2022 21:06:47 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Mon, 07 Nov 2022 21:06:47 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Mon, 07 Nov 2022 21:06:47 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 07 Nov 2022 21:06:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8e1d92e7d04d2a9a9880cb45dc3c32c2805912cd86abed96d0ada3ff28748205`  
		Last Modified: Tue, 25 Oct 2022 05:48:40 GMT  
		Size: 53.7 MB (53701966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1e4dcae904908999385d0b955f5ebdc51329825e0aa473155c319828d97c6b`  
		Last Modified: Mon, 07 Nov 2022 21:11:42 GMT  
		Size: 191.2 MB (191215247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52191bd27a440b93e87270a83ed4fe094812c9c3e809b069d99a48e5bb48d26e`  
		Last Modified: Mon, 07 Nov 2022 21:14:09 GMT  
		Size: 47.3 MB (47294537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9aab88fcda1ad3fe4daba8c2fd6f5ec29d4775e0c017239ef337f79d7343dd`  
		Last Modified: Mon, 07 Nov 2022 21:14:03 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d8fbd967c7e90b77d5145a4ba878322273d2b78b23b13105f9c1b49cbe57b2`  
		Last Modified: Mon, 07 Nov 2022 21:14:03 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
