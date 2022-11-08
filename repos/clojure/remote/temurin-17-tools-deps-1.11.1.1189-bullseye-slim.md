## `clojure:temurin-17-tools-deps-1.11.1.1189-bullseye-slim`

```console
$ docker pull clojure@sha256:19ba385585b5fba1b04a9dc84e5e6a7e5b7cec420c632d2096312bd182cd526b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.1.1189-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9db1802ac22b5bd2a625fe5210947c2ed51e86847d2de61495ce8c56de9233c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.3 MB (285325773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e5223be5de8c6b199dfa738d1563b8d2e6ae5615b180208f81af35d0b758cc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 07 Nov 2022 20:48:08 GMT
COPY dir:fa15c3254735d08fe4cb4c940d6fc08efc9755ff0499a6eb8e51c961cea48d5c in /opt/java/openjdk 
# Mon, 07 Nov 2022 20:48:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 20:51:35 GMT
ENV CLOJURE_VERSION=1.11.1.1189
# Mon, 07 Nov 2022 20:51:35 GMT
WORKDIR /tmp
# Mon, 07 Nov 2022 20:51:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1afd91b165776615eca84cce2271e5fe5d5818c55dee0f082b1304bb1464b3e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Mon, 07 Nov 2022 20:51:53 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Mon, 07 Nov 2022 20:51:54 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Mon, 07 Nov 2022 20:51:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 07 Nov 2022 20:51:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2d9967bfe9b338d34c1d6b115d688a7c4c9b111a5ea71ceb27421142a7f12b`  
		Last Modified: Mon, 07 Nov 2022 20:57:59 GMT  
		Size: 192.4 MB (192431266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f511af75ab3f2b05174c546e722e7e72c1728d257713a39e7253fa5877b0f88`  
		Last Modified: Mon, 07 Nov 2022 21:01:05 GMT  
		Size: 61.5 MB (61473450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5dbaecbba1478fc45066155c796a3f71b7ed1a3392fea7575ca5e60dd7b3b3`  
		Last Modified: Mon, 07 Nov 2022 21:00:57 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293b4450d063411b6f8667fc06e25aada55962575982b98c8b40ce0ae6ce8018`  
		Last Modified: Mon, 07 Nov 2022 21:00:57 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-1.11.1.1189-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4de4544b1c0d14fe8802ee949a0d18bd5c2e550c2455fe303ff2cc792c74ef78
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282873208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb263650045a37e0f061f07fee65d497aaf5b125301d6a9769ee63c515341a88`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 07 Nov 2022 21:03:54 GMT
COPY dir:36850aee002fdc5445f17d75b8266c48f8e705973ece815c3b53d28b6656ac3e in /opt/java/openjdk 
# Mon, 07 Nov 2022 21:03:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 21:06:50 GMT
ENV CLOJURE_VERSION=1.11.1.1189
# Mon, 07 Nov 2022 21:06:50 GMT
WORKDIR /tmp
# Mon, 07 Nov 2022 21:07:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1afd91b165776615eca84cce2271e5fe5d5818c55dee0f082b1304bb1464b3e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Mon, 07 Nov 2022 21:07:05 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Mon, 07 Nov 2022 21:07:05 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Mon, 07 Nov 2022 21:07:05 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 07 Nov 2022 21:07:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da08ea5cf75b951398d57ee8bc9c95f4a6a9ffdd4548e791b7ac3a9ea4c9900a`  
		Last Modified: Mon, 07 Nov 2022 21:12:03 GMT  
		Size: 191.2 MB (191215226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036f4edce1fab76596a6690b6cdb2c3baacc5cf6d6efc1ae3cb443fd0b4a9f52`  
		Last Modified: Mon, 07 Nov 2022 21:14:27 GMT  
		Size: 61.6 MB (61593054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e80a737386810bcc78213f60cfc5fc93e1c0aed59ec43c9dfd1d6cc6819adbd`  
		Last Modified: Mon, 07 Nov 2022 21:14:21 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff526005755cfa2126551d855aaf2a887008c0c82b2cf60e3d834d661f0e3635`  
		Last Modified: Mon, 07 Nov 2022 21:14:21 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
