## `clojure:temurin-11-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:9c726612ccf03e051afc4d7906010b7c700d507046ad114cfd88ce7189679912
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:bd72b2c79edb47ebbc8339aa340bf54956026468704d1a3ec5edd5e58c8acc14
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275315968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7bb4ae300810015ee917540da8a9d2b70a71e4d01bf51b9ad08bc7a5ba88fc`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:46:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 01:52:46 GMT
COPY dir:b67fa5b31406358a1c40465f439a0fe28f2585d2aa41aff7249c3c30b266c578 in /opt/java/openjdk 
# Tue, 13 Feb 2024 01:52:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 01:56:49 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Tue, 13 Feb 2024 01:56:49 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 01:57:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 13 Feb 2024 01:57:09 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 13 Feb 2024 01:57:09 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe3470e538d4e3cfd65043bfc65a4966ed42ab558a0d02d70086e803479fa66`  
		Last Modified: Tue, 13 Feb 2024 02:12:52 GMT  
		Size: 145.3 MB (145271036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f070551bda2410bb996b98ad27e1caad484b5267a2dde624cec32679f3aab9`  
		Last Modified: Tue, 13 Feb 2024 02:15:01 GMT  
		Size: 80.5 MB (80491710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802555bc563df2584fb7f54be6de5e2479cbafb46f0a19e351cbbdc418879fce`  
		Last Modified: Tue, 13 Feb 2024 02:14:51 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fa85c5d5833178d0324a8f21f6cc2fced243961caa083055f4da6e10e1512fcd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271853399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:602c66c0bc1eec180504eee52c1b1c212de6407b8cf969383b033f3406b968f9`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:10 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Tue, 13 Feb 2024 00:41:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:53:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Feb 2024 01:59:30 GMT
COPY dir:66e2d93ab60a4ef1bb1a1f0fa29608c8835186fbe657955fddda78ed144821fc in /opt/java/openjdk 
# Tue, 13 Feb 2024 01:59:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Feb 2024 02:03:07 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Tue, 13 Feb 2024 02:03:07 GMT
WORKDIR /tmp
# Tue, 13 Feb 2024 02:03:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 13 Feb 2024 02:03:23 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 13 Feb 2024 02:03:23 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb18bf1feb8a022b56cb764ff4154c937334b989bb90ffde840254ce27e971b`  
		Last Modified: Tue, 13 Feb 2024 02:17:04 GMT  
		Size: 142.0 MB (142006386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7fee1eed74925d52dba32d2b4bad29d848b80418801b30f76f30908c7e0fbf7`  
		Last Modified: Tue, 13 Feb 2024 02:19:13 GMT  
		Size: 80.3 MB (80255431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63bb9cb07506fca7565f780098f447fc940d5d02d60ee604c09d7e6d358103d6`  
		Last Modified: Tue, 13 Feb 2024 02:19:04 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
