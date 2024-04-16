## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:2cdbdcd43b8375957df9261ff24d9ac0c9af9e4209aec675e163bac74dbb988c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:cf548e5579e177f77996a948fe62622f96bacbec8125e87247bf019bffd1d425
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (269000463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f3744055e8ea42d5fc68d13adc6a8e5c14b3ee2b0c9bc68d63c9cc5d712245`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:59 GMT
ADD file:8efdcc3201e79c8a09fc9c1ade08492ea33f838047332a7c61988f6357339dee in / 
# Wed, 10 Apr 2024 01:50:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:18:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Apr 2024 11:03:58 GMT
COPY dir:634e6dc1071a76d830a1c58e20efb6c42c0d02beb44d214374fc7817b69efa15 in /opt/java/openjdk 
# Tue, 16 Apr 2024 11:04:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 11:09:13 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Tue, 16 Apr 2024 11:09:13 GMT
WORKDIR /tmp
# Tue, 16 Apr 2024 11:09:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -sLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 16 Apr 2024 11:09:30 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 16 Apr 2024 11:09:30 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 16 Apr 2024 11:09:30 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Apr 2024 11:09:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ac323bdaa10f869bd9e7adecd8f5326e44acc4c59168868108b1cdf3891089cc`  
		Last Modified: Wed, 10 Apr 2024 01:55:52 GMT  
		Size: 55.1 MB (55090264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16199a1d15aa77000652c9bf81de1324ecf36eb5aad0f612c186f29d6b572226`  
		Last Modified: Tue, 16 Apr 2024 11:22:34 GMT  
		Size: 144.9 MB (144893099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8117c422888550ced71c935fa37700b4e24bfd94dfdb60f97a00d21a4ac3c0d6`  
		Last Modified: Tue, 16 Apr 2024 11:26:13 GMT  
		Size: 69.0 MB (69016083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186db37a3d7571f56d6db42d6ae867060150c28d07489aea28c1beae43047693`  
		Last Modified: Tue, 16 Apr 2024 11:26:05 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0e524c8b172beba3f0eed8d39d9380458c4bb5ec25ebb77e62eb4ae7dd683f`  
		Last Modified: Tue, 16 Apr 2024 11:26:05 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:18d3d9b9fd504de9d8d115bfb46b4b381b7c986bfd60c102a179565f77959222
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.6 MB (266592226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7e4c8e195f6207330b5b9b5273816e706c1d698baa631de7a021550c44161c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:30 GMT
ADD file:6fedb173fe261ff0e13b004ca692b7edcc74dcc3c4384fee092b96ef9508992c in / 
# Wed, 10 Apr 2024 00:40:30 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:39:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Apr 2024 06:41:00 GMT
COPY dir:00f694ce512d2e49bdb0844fa7f6d54a4b39a35418d1c6b32b574b5d44cfc1da in /opt/java/openjdk 
# Tue, 16 Apr 2024 06:41:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Apr 2024 06:45:31 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Tue, 16 Apr 2024 06:45:31 GMT
WORKDIR /tmp
# Tue, 16 Apr 2024 06:45:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -sLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 16 Apr 2024 06:45:46 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 16 Apr 2024 06:45:46 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 16 Apr 2024 06:45:46 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 16 Apr 2024 06:45:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:197947a07d5f6c6ff020ca65dcea4e52671f85f67bee1b59af46cb0dc36580d9`  
		Last Modified: Wed, 10 Apr 2024 00:44:24 GMT  
		Size: 53.7 MB (53729176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d38c21b09d53fed41b7bd3ec1a4b9e920db379f3c64904afb6272b7efd4be7ad`  
		Last Modified: Tue, 16 Apr 2024 06:57:09 GMT  
		Size: 143.7 MB (143720948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58e33750386b21945f9775280b5d91e867b3d01872c1b5d0f41007d0f48cbd7`  
		Last Modified: Tue, 16 Apr 2024 06:59:43 GMT  
		Size: 69.1 MB (69141086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b09ec007ea56db81a6081f9741c6d86f65b1ac95333df6ebeb436aaeeafb15`  
		Last Modified: Tue, 16 Apr 2024 06:59:37 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6deee3184442ee72edeffc95f0fc3fab998e6f291d402b4c86eff7d045c9a3f`  
		Last Modified: Tue, 16 Apr 2024 06:59:36 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
