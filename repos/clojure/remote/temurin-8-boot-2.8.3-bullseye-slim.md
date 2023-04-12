## `clojure:temurin-8-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:12ed3e2aafae551637b8d4cb85fe285ed8a818bb0363bedde9d82b663e8a4927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2107e266fafb06223a9f5beaae095d19dc6c3b28c76d966b373453886ee7295d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.9 MB (145944695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2602fbf90b8c163e52c5adb0121bb452feff0d8d329852d82bf2ed20e61110`
-	Default Command: `["boot","repl"]`

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
# Thu, 23 Mar 2023 06:17:48 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 23 Mar 2023 06:17:48 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 23 Mar 2023 06:17:48 GMT
WORKDIR /tmp
# Thu, 23 Mar 2023 06:17:53 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 23 Mar 2023 06:17:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 23 Mar 2023 06:17:53 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 23 Mar 2023 06:18:10 GMT
RUN boot
# Thu, 23 Mar 2023 06:18:11 GMT
CMD ["boot" "repl"]
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
	-	`sha256:c1e622ad49c17f249d06a9110797d6470803f637fa8202665cc61e330e8f4b94`  
		Last Modified: Thu, 23 Mar 2023 06:29:21 GMT  
		Size: 1.1 MB (1077364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4716835939df2da63cc2dbad9d3c507584040df9606d1fbb7eb806f78d5a9b4d`  
		Last Modified: Thu, 23 Mar 2023 06:29:24 GMT  
		Size: 58.8 MB (58820381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1a1bf737367813f1d9f9f5baeef5c66fadde262a8d2aa459a6fe03aa83ed5423
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143677037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383d68ac35f45fcbfda9ccc455703fc0bc1e26a065d58752da3b7d1fb9099255`
-	Default Command: `["boot","repl"]`

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
# Wed, 12 Apr 2023 01:18:47 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 12 Apr 2023 01:18:47 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 12 Apr 2023 01:18:47 GMT
WORKDIR /tmp
# Wed, 12 Apr 2023 01:18:52 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 12 Apr 2023 01:18:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 12 Apr 2023 01:18:52 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 12 Apr 2023 01:19:10 GMT
RUN boot
# Wed, 12 Apr 2023 01:19:10 GMT
CMD ["boot" "repl"]
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
	-	`sha256:e57a2837a2cc9f72adbfdb72e848b55988e5f4380c77ceeba4af44829069d826`  
		Last Modified: Wed, 12 Apr 2023 01:28:06 GMT  
		Size: 1.1 MB (1064821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d84987be50e9054eb5252b00f4316d0920448752d31acd03040424ca40f000`  
		Last Modified: Wed, 12 Apr 2023 01:28:08 GMT  
		Size: 58.8 MB (58820453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
