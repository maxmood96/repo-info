## `clojure:temurin-11-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:f9bd3cbb411364bec3349ca9e8a9d497d2cb0231a03cd97213ea432add741bdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:75ea4e84abc7c354148d95a97f5cbca1b2d1b284cdd7ff649e8238eb48c0b123
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275324071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64122cbe0e68d0fea4cde02d634af5ae4350c6c04e81afb7dbdadb8e7ebba0e2`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:34 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
# Wed, 10 Apr 2024 01:50:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:16:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 06:22:41 GMT
COPY dir:4cef005a87cd4606dd69ccb04c755a46f4aa2c925fb1aacc59928d64687208f2 in /opt/java/openjdk 
# Wed, 10 Apr 2024 06:22:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:26:42 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 10 Apr 2024 06:26:42 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 06:27:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 10 Apr 2024 06:27:01 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 10 Apr 2024 06:27:01 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a514947677172b8fc44890310625cf6cc5b905b6756bd6f81147c12bf9d8653f`  
		Last Modified: Wed, 10 Apr 2024 06:42:18 GMT  
		Size: 145.3 MB (145271226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4905a088760d1ec0bfc7af95a496cfc8956be0693cafb20f8ea98e150d007403`  
		Last Modified: Wed, 10 Apr 2024 06:44:23 GMT  
		Size: 80.5 MB (80491868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32e1412bd44ed4afa2a817489a4f376e346afb835ef4a192179ba4f42d0216b`  
		Last Modified: Wed, 10 Apr 2024 06:44:14 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9fcbf2ac871db14e09a985c69e4c4ebcb84c24799eddb1d249de2feec8bf310d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271858812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5832188e093a9509f1406251a3f46732a011832ce126f59c2887ad03f396c27`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:12 GMT
ADD file:d795219dc83a41b5bb4106e62eebd31ceef0aae1b81541156eae5fe98e89337c in / 
# Wed, 10 Apr 2024 00:40:13 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:37:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 04:43:13 GMT
COPY dir:d5fb8d9a38dea7496f2aff176bc9a34bbca80551c2dc57109d2dae5907a339ee in /opt/java/openjdk 
# Wed, 10 Apr 2024 04:43:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 04:46:52 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Wed, 10 Apr 2024 04:46:52 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 04:47:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 10 Apr 2024 04:47:08 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 10 Apr 2024 04:47:08 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1e92f3a395ff98a929e797a3c392bb6d0f05531068d34b81d3cd41ed6ce82ca4`  
		Last Modified: Wed, 10 Apr 2024 00:43:42 GMT  
		Size: 49.6 MB (49596265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9bdda611d99cfbb82c7d1a5c1aec0235837c8fadc922cd581de255634dfb66`  
		Last Modified: Wed, 10 Apr 2024 05:01:17 GMT  
		Size: 142.0 MB (142006303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e503a1d8b5a6a374a82947178f82f44cdff3a3fc9d84f6c66d2b0ec979dae42`  
		Last Modified: Wed, 10 Apr 2024 05:03:08 GMT  
		Size: 80.3 MB (80255626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6211e2b6b1caabf907b387e34c3f84b862fac43a7955a148123ec9247b87203c`  
		Last Modified: Wed, 10 Apr 2024 05:02:59 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
