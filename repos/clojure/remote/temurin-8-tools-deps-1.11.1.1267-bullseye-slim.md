## `clojure:temurin-8-tools-deps-1.11.1.1267-bullseye-slim`

```console
$ docker pull clojure@sha256:d3251e5bff9165868ee313ad6627fbb1a24a79ecfe47f5d1a7191b33882c3ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-tools-deps-1.11.1.1267-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f8a693d0287e2862672a04da554d9e5ebe6cb00599faa3f63bfa1912c3a6d28f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147543061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd6d947f78e8aa028d89fc49abb20639e6739bbee687bfc40e12dc888eba50a`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:17:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 Mar 2023 06:17:47 GMT
COPY dir:bbb84183d7ea38d81d8401f01e29d08935ee4c8bf6f90c6527579a1554c3bde1 in /opt/java/openjdk 
# Thu, 23 Mar 2023 06:17:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Apr 2023 23:56:45 GMT
ENV CLOJURE_VERSION=1.11.1.1267
# Mon, 03 Apr 2023 23:56:45 GMT
WORKDIR /tmp
# Mon, 03 Apr 2023 23:57:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "c949c9ba24ee46a2c57c6e6aeff262ebb0ff8112ee2367b3dbabd2f2df75380a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Mon, 03 Apr 2023 23:57:02 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Mon, 03 Apr 2023 23:57:02 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1977e261c2ece5904696fe62d44f44495568e580f96e10c2adb6f00ef7e609c9`  
		Last Modified: Thu, 23 Mar 2023 06:29:27 GMT  
		Size: 54.6 MB (54635545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec9e3070477e312934117b0cf2479dbeba4d7b1fff1e94c556581201a85a9ba`  
		Last Modified: Tue, 04 Apr 2023 00:06:20 GMT  
		Size: 61.5 MB (61495494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4467fae7c7a1949e354ad55f8a7bf04e3d94e4f7d30b3a31c9148933e5c32af`  
		Last Modified: Tue, 04 Apr 2023 00:06:12 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-tools-deps-1.11.1.1267-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bf65830ce80768226e37658fc3831f49f92499bec29f423af74c2a183c8325e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145403016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bef7af9c5f2c8a7e3abe5b5aef2869b6d536825611bc8ac9d87ed77cedf3a81f`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:49 GMT
ADD file:7b3c55926db26568f849247e80abdec3cfd6642929a40f0bbee95e4cb176051e in / 
# Wed, 12 Apr 2023 00:39:49 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:18:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Apr 2023 01:18:46 GMT
COPY dir:b6d7e5613532d986930216de9e0fece0632e82564ce7a6a98baf63b4115f840d in /opt/java/openjdk 
# Wed, 12 Apr 2023 01:18:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 01:20:18 GMT
ENV CLOJURE_VERSION=1.11.1.1267
# Wed, 12 Apr 2023 01:20:18 GMT
WORKDIR /tmp
# Wed, 12 Apr 2023 01:20:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "c949c9ba24ee46a2c57c6e6aeff262ebb0ff8112ee2367b3dbabd2f2df75380a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 12 Apr 2023 01:20:32 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 12 Apr 2023 01:20:32 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ebc3dc5a2d72427c585c8cda7574a75d96e04b9a37572bd3af0bff905abefbb9`  
		Last Modified: Wed, 12 Apr 2023 00:42:35 GMT  
		Size: 30.1 MB (30063826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4beeaea1bb320b3b40a83a6b31783cdc7af5081dd6683ffd28ef3a3b39f888ff`  
		Last Modified: Wed, 12 Apr 2023 01:28:11 GMT  
		Size: 53.7 MB (53727937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ce63753086f6e0643dffc71d44e76b23a7919a4766babd2de1f4d5c984a6fc`  
		Last Modified: Wed, 12 Apr 2023 01:29:01 GMT  
		Size: 61.6 MB (61610641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ca3e776de4ae5cb0af36572f4e00d670205b9592000d673aafb2915b168aae`  
		Last Modified: Wed, 12 Apr 2023 01:28:56 GMT  
		Size: 612.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
