## `clojure:temurin-20-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:13876467d6998016f1ccafd8290d4ca2e9436ef19f4459036bea57c9cc6e4a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-20-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2fb82c4e4dc44668d80021625dfbc9cc5716d08ad782bd0f1790a6f8069b92f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246713868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9035b43523a32ae3f86d88a7e1f90f64459b5c31736221dc7f7f2db0476d420f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:13 GMT
ADD file:cb13581b8e7a9de4396639e5ca2f3817763435c0563232f85e3d899f6388a1b3 in / 
# Wed, 11 Oct 2023 18:35:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:51:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Oct 2023 19:00:31 GMT
COPY dir:6a540db71f2a37db361084aee8addd6817cd7c4f18237e6f852a38e98bdb4182 in /opt/java/openjdk 
# Wed, 11 Oct 2023 19:00:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 19:01:19 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Wed, 11 Oct 2023 19:01:19 GMT
WORKDIR /tmp
# Wed, 11 Oct 2023 19:01:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 11 Oct 2023 19:01:35 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 11 Oct 2023 19:01:35 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 11 Oct 2023 19:01:36 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 11 Oct 2023 19:01:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e67fdae3559346105027c63e7fb032bba57e62b1fe9f2da23e6fdfb56384e00b`  
		Last Modified: Wed, 11 Oct 2023 18:40:17 GMT  
		Size: 31.4 MB (31417862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf394a08e5a36fada07296c8979f418501aa31a80a997032f74a35e0376851c`  
		Last Modified: Wed, 11 Oct 2023 19:09:43 GMT  
		Size: 153.8 MB (153791707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658df9596a6010bfbd145a442bb9e67311c1b5c0bcf428ca4c6d525ecce83044`  
		Last Modified: Wed, 11 Oct 2023 19:10:27 GMT  
		Size: 61.5 MB (61503280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e8105b88dd19d0f5d9566ccdf8713ac77cae43d6bfb2974207a93128e6fee43`  
		Last Modified: Wed, 11 Oct 2023 19:10:20 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18acec13ac96f019831394b2e352b022bc4c5d262ceaed84d56118e637770866`  
		Last Modified: Wed, 11 Oct 2023 19:10:20 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-20-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:892d42c81c6660b1749e1bd7c8534893ddfa272d7ceb39d430fe597b7116e161
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243805530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfbf43ece8d5a08699db08cf47d6e988b0a263d2f631f89736c490217000afac`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Oct 2023 18:53:48 GMT
COPY dir:d35c6357dd030960bb6081f48b2bc10afb3da11efc1525ff916214b03be70ddf in /opt/java/openjdk 
# Wed, 11 Oct 2023 18:53:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 18:54:37 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Wed, 11 Oct 2023 18:54:37 GMT
WORKDIR /tmp
# Wed, 11 Oct 2023 18:54:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 11 Oct 2023 18:54:52 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 11 Oct 2023 18:54:52 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 11 Oct 2023 18:54:52 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 11 Oct 2023 18:54:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a9bf06dd0a1869053afd51d94cc0cd10e847819bb08600e5d6ef3b112e2efe`  
		Last Modified: Wed, 11 Oct 2023 19:01:50 GMT  
		Size: 152.1 MB (152120116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:156fcf967111377b9f8968981c97eee056469b0976e8694c409ce85e5228bcad`  
		Last Modified: Wed, 11 Oct 2023 19:02:25 GMT  
		Size: 61.6 MB (61620316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3bc173f8d5b31cf3b53c41db33ff6ed2887065232b7693de57216b005e502a`  
		Last Modified: Wed, 11 Oct 2023 19:02:19 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd88d4778db92aeaf6b8edf274561e481b3e6faaf5ca7f6ebeed97d28d02599`  
		Last Modified: Wed, 11 Oct 2023 19:02:19 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
