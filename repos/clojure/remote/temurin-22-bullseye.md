## `clojure:temurin-22-bullseye`

```console
$ docker pull clojure@sha256:903055127f9e54103de46233bed2a575a3fe48d94eaa3d96b176739573f90c1c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `clojure:temurin-22-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:33d2a19b8a0fb4c4d9386b0011b8fd283ece48671fbcfc52821d1a9fa2e948f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 MB (280632290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1569b914e5e60b8b1e904b84314dc58a61a549a2a9d68d20e6f840132e50f62`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:14 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 14 May 2024 01:28:14 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5450f27dbd9b9fd0347d787cba74d81bbe13a56d3c0c2e0db084d707ce48bc8`  
		Last Modified: Wed, 29 May 2024 19:59:26 GMT  
		Size: 156.7 MB (156715502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2b5c5117b36d04d55b23fdaade95e5868db5055c9027b4f7080bbd04583b5c`  
		Last Modified: Wed, 29 May 2024 19:59:25 GMT  
		Size: 68.8 MB (68816340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6613035c1716e5c150436bd7c1830987e128c778dd33599f7aa4d8582faaf60`  
		Last Modified: Wed, 29 May 2024 19:59:24 GMT  
		Size: 618.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9005e1dba41c1becbd93e1be93463c779e523b36c6e97bc6895112af5e8f25`  
		Last Modified: Wed, 29 May 2024 19:59:24 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:463f787937d4e641a8f8a2889bedc8d6e5a799e069bfc743b5d9dc16330284fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7015136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19258c638f77a30de9aee3e39d00ac20d0ac419832c8712a116235bcd5a2e80b`

```dockerfile
```

-	Layers:
	-	`sha256:7d2c940fe696fc31c9fa062d9fcd053bae74b79de54890de3a67f34c6315746c`  
		Last Modified: Wed, 29 May 2024 19:59:24 GMT  
		Size: 7.0 MB (6999746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0829d39d7dd611f6369ac920013817a72343a32c508053c7f6aaf34ef4a93a29`  
		Last Modified: Wed, 29 May 2024 19:59:24 GMT  
		Size: 15.4 KB (15390 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:886846af12730b8d203d6e263ca83c1d353339e0ff7b06d97a79ed3aad9cd84b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.6 MB (277615470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f85ed8f3100f470885c612a5fc02cdf0c64385a8b35d803835ce2e8d316923`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:47 GMT
ADD file:43721c605da3f74f0c3f71384780fc0e57e2478b88197672caaf4baa3eddab23 in / 
# Tue, 14 May 2024 00:39:48 GMT
CMD ["bash"]
# Tue, 28 May 2024 19:44:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 20:02:43 GMT
COPY dir:8db4aa7d00469f3c784932412aa95caf68b05146a02559362a91df21ce463ad4 in /opt/java/openjdk 
# Tue, 28 May 2024 20:02:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 20:04:43 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 20:04:43 GMT
WORKDIR /tmp
# Tue, 28 May 2024 20:04:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl
# Tue, 28 May 2024 20:04:58 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 28 May 2024 20:04:58 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 28 May 2024 20:04:58 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 20:04:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:078d9526cc72763b2db16388f6b511c18a73e3e7f9d229364b3b85a6b5277bc8`  
		Last Modified: Tue, 14 May 2024 00:43:13 GMT  
		Size: 53.7 MB (53738990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84a1f76b155da5c15c43207f175b35e0a21820d0d8c424cae5b958fe3956aa4`  
		Last Modified: Tue, 28 May 2024 20:22:14 GMT  
		Size: 154.7 MB (154737692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f00810a24c34d95dfa6239e4f7c936be5e017290105de10256119b5f556f93a5`  
		Last Modified: Tue, 28 May 2024 20:23:39 GMT  
		Size: 69.1 MB (69137770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591692a0ca8d8f98b41ff6f1a960fd481679018b016cd266b8927a49e1ef1a9a`  
		Last Modified: Tue, 28 May 2024 20:23:31 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77b9ebec0978a3b11daee34cddd60693e2647499b60c196699de3f2cce9b34e`  
		Last Modified: Tue, 28 May 2024 20:23:31 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
