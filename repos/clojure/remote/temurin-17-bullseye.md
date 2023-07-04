## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:03ced1d7ac0471e26ffd45f45807a20c76fa45e6fbfa7959d0212687de2a0f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1f742265e9c355abfafa6e7e1e004534f424d4c0da7c30285992c93e7cc535df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.5 MB (319519681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7c8486115bafd8624a42493d2ed0f1898e80b171585854605aab66f7e64f5f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:09 GMT
ADD file:b7c0be2bb90e88689b1c16da78dea0b85760b55b90ef2e5bc4a529c89e4fa25b in / 
# Tue, 04 Jul 2023 01:20:10 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:59:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Jul 2023 04:05:49 GMT
COPY dir:bd419ef2141504aa2f648c196bb8bfe0688018838c9b92d958b5908207ce1f25 in /opt/java/openjdk 
# Tue, 04 Jul 2023 04:05:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jul 2023 04:07:43 GMT
ENV CLOJURE_VERSION=1.11.1.1347
# Tue, 04 Jul 2023 04:07:43 GMT
WORKDIR /tmp
# Tue, 04 Jul 2023 04:07:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "d9158bf3a1d92fbf8551656e47a86f42e93d10f1db9defa2124bfee206ce8c8f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 04 Jul 2023 04:08:00 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 04 Jul 2023 04:08:00 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 04 Jul 2023 04:08:00 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Jul 2023 04:08:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:34df401c391c7595044379e04e8ad4856a5a3974cdbf5a160f0a204d761e88aa`  
		Last Modified: Tue, 04 Jul 2023 01:25:21 GMT  
		Size: 55.1 MB (55055300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d5749ce62c0fb43ce9ee4298e4f571f0584facdde1f4b6b77b68dcf21129c2`  
		Last Modified: Tue, 04 Jul 2023 04:15:06 GMT  
		Size: 192.6 MB (192580329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa2f1fe05bec9a1a5069e39105638c773df0346f0f1f39c09a5b0d81c1706c7`  
		Last Modified: Tue, 04 Jul 2023 04:16:15 GMT  
		Size: 71.9 MB (71883043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47772eccf43dbaf601d0be1ba98e5eaf51ac470c1360bed330b5822dd55a79d8`  
		Last Modified: Tue, 04 Jul 2023 04:16:08 GMT  
		Size: 613.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8faef1f848799777a026a8d3d6b4b2fab5c20e3cd54639eae80411d01ca118`  
		Last Modified: Tue, 04 Jul 2023 04:16:08 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8de0918aa1b3555ab0a7a8e58bd7d8c645ba4b52f2d9f0fe411c2607203feb6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.1 MB (317090041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b6a29502487b7c59616003c21246aa56bd85e8c9037401cb7097bfc8290a7f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:22 GMT
ADD file:caddd2f40296ec5c1bf7487617ca8694cfff9a1d9b7484159e203b6514cb5f5f in / 
# Mon, 12 Jun 2023 23:40:23 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 04:50:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jun 2023 04:46:29 GMT
COPY dir:a7888c4ea2b71681cd7f19a201b81930752c61fdfa5815ca0d4cf6337d5ee1e8 in /opt/java/openjdk 
# Fri, 16 Jun 2023 04:46:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jun 2023 04:49:16 GMT
ENV CLOJURE_VERSION=1.11.1.1347
# Fri, 16 Jun 2023 04:49:16 GMT
WORKDIR /tmp
# Fri, 16 Jun 2023 04:49:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "d9158bf3a1d92fbf8551656e47a86f42e93d10f1db9defa2124bfee206ce8c8f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 16 Jun 2023 04:49:31 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 16 Jun 2023 04:49:32 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 16 Jun 2023 04:49:32 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jun 2023 04:49:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:663ccfaf62a5d7b997bca03d1dc6d5dfff01b9e0de08d86dbea8957ea92d7d16`  
		Last Modified: Mon, 12 Jun 2023 23:44:25 GMT  
		Size: 53.7 MB (53704136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:172252176b2d2b44f66626001ffedf36355c238558bbc403980303e6b6c92ae9`  
		Last Modified: Fri, 16 Jun 2023 04:56:58 GMT  
		Size: 191.4 MB (191387640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231a074c0eb6849037814ef704dac609e348782986feac371e6e9f22eebe1a7a`  
		Last Modified: Fri, 16 Jun 2023 04:58:58 GMT  
		Size: 72.0 MB (71997252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b2c045e1466ebaa4a302a68584ff34368dd0c857f428cf091cdae505e56209a`  
		Last Modified: Fri, 16 Jun 2023 04:58:52 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639e98924115aaa1638d58466fd4c12f1ffe0bdb23d5af2e2fef966566ec4307`  
		Last Modified: Fri, 16 Jun 2023 04:58:52 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
