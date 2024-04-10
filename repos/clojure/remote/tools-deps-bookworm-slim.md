## `clojure:tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:75c5d473e3e594852c2e21a9e0ca7707ba8f30ec1d0aa9679ec8e97776d19cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ad10ca29336395d7b06daa6fa43e4e7ce902af9837ab505ace0019bb711db48d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.8 MB (257777315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1999372b06fe5350bbbf2d64a6a8b0bf8c20a4735b8dd55d0ad98e953d6b93ab`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:17:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 06:34:12 GMT
COPY dir:64a8841762a9afbd2fb8b4cf497b2dee87765737d44ff0387ce1cfc51371c9a2 in /opt/java/openjdk 
# Wed, 10 Apr 2024 06:34:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:35:53 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 10 Apr 2024 06:35:53 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 06:36:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 10 Apr 2024 06:36:12 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 10 Apr 2024 06:36:12 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 10 Apr 2024 06:36:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 10 Apr 2024 06:36:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a60ce6f3f5cc5f9f734b801978be67d2f134eb8358976fd04daf3f15c7c16228`  
		Last Modified: Wed, 10 Apr 2024 06:49:21 GMT  
		Size: 159.6 MB (159582870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ef6d553d7321e00bfd520c1c668ee82bcc457d0cdc7d8c75aa485838937799`  
		Last Modified: Wed, 10 Apr 2024 06:51:02 GMT  
		Size: 69.1 MB (69062071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e81854ddaec10418bfff8fdc977136367d5a5215dd1d887a32a1f6a061ab7f8`  
		Last Modified: Wed, 10 Apr 2024 06:50:54 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21ad9a2a6876bbdaef012833e11d9194180844170d0c630b023308944282b741`  
		Last Modified: Wed, 10 Apr 2024 06:50:54 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ded977c788e2763a1f4b317ee27a586998c40430903e2e37b6ca411d1ce84aee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255765305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008dae85a90f1da886159ecd6c3d07f802def7f8613ecc6879066c351d9f97e1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:23 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Wed, 10 Apr 2024 00:40:23 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:38:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 04:53:16 GMT
COPY dir:ab40534e435f9942975c0e8b5454d6b7a8d69c445f8e0758c1bd9c500e157fca in /opt/java/openjdk 
# Wed, 10 Apr 2024 04:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 04:54:56 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 10 Apr 2024 04:54:56 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 04:55:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 10 Apr 2024 04:55:11 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 10 Apr 2024 04:55:11 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 10 Apr 2024 04:55:11 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 10 Apr 2024 04:55:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a58fe06d24a9c9973da82863c842560b8b11ab8de0f315e299af1d20774048a`  
		Last Modified: Wed, 10 Apr 2024 05:07:52 GMT  
		Size: 157.8 MB (157784670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b131504e3fc97f94e30e1837018d46555a2295a430406dbf85e43802e39dd2c`  
		Last Modified: Wed, 10 Apr 2024 05:09:29 GMT  
		Size: 68.8 MB (68817461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b137a01203577e95724d67ced5beb7ed1a3f0d3f1aadc60537f23e7c3baa8cd`  
		Last Modified: Wed, 10 Apr 2024 05:09:22 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba61d16e4afa6bf1a7385b538fe41398d0a90a4053f663034886e36503c59327`  
		Last Modified: Wed, 10 Apr 2024 05:09:22 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
