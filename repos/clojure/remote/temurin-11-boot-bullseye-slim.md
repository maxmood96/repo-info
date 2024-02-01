## `clojure:temurin-11-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:ee305fccf7824de2a55d653d64349080d9fcec203f9128bccfb946b740f5e167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:92bc5add4cf3c67e9a13fdae239f155c5382f91832254f3b8a3d9dca0b29f624
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.6 MB (236588834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de74cc4666b21da743b5fd4e065a3bab0c95b1ad85ac74c483ae21660ec5e3fc`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 23:50:14 GMT
COPY dir:e1ce96bca1c423a1c79b84eacb7ae69429353a37485cc24af4161ce4b9d3ee2a in /opt/java/openjdk 
# Wed, 31 Jan 2024 23:50:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:50:15 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 31 Jan 2024 23:50:16 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 31 Jan 2024 23:50:16 GMT
WORKDIR /tmp
# Wed, 31 Jan 2024 23:50:21 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 31 Jan 2024 23:50:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 31 Jan 2024 23:50:21 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 31 Jan 2024 23:50:41 GMT
RUN boot
# Wed, 31 Jan 2024 23:50:41 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237cb6d9dedd71662d3dfef2792a61299af8d4b495bbb2a1e8f51c6f89c22ddd`  
		Last Modified: Thu, 01 Feb 2024 00:09:34 GMT  
		Size: 145.3 MB (145270936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a0fd4a1b29914c5528747a90854647fa44175561142158b4fe1e10d818e4e5`  
		Last Modified: Thu, 01 Feb 2024 00:09:23 GMT  
		Size: 1.1 MB (1079474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95edbefb260db8c5c5d1b253640d906e4ad30669eae43d777cf1da26794c887`  
		Last Modified: Thu, 01 Feb 2024 00:09:26 GMT  
		Size: 58.8 MB (58820597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1f05092ab2498ca02e56ff97a69400243d0a44ac0beb07a535a98746b6d2232d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231958211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c96de1f18c41693852e455129a29d00da2e1082e8dec76a3b2a2709af354245`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:42 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Wed, 31 Jan 2024 22:44:42 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:21:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 06:26:11 GMT
COPY dir:454699b64b949edd3264b234e72a891ace37d538f2726c5ec754e17e6fb3fb19 in /opt/java/openjdk 
# Thu, 01 Feb 2024 06:26:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:26:14 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 01 Feb 2024 06:26:14 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 01 Feb 2024 06:26:14 GMT
WORKDIR /tmp
# Thu, 01 Feb 2024 06:26:19 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 01 Feb 2024 06:26:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 01 Feb 2024 06:26:19 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 01 Feb 2024 06:26:38 GMT
RUN boot
# Thu, 01 Feb 2024 06:26:38 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eddf8729def8f436a94b509a37f4bf17c7819ac995ef5769ed48da7ddd3b0b64`  
		Last Modified: Thu, 01 Feb 2024 06:43:10 GMT  
		Size: 142.0 MB (142006498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12fd430af7d09a018fb68bbb5f111a94feee4d0a779bc28e81110efc1a9e9d8`  
		Last Modified: Thu, 01 Feb 2024 06:43:02 GMT  
		Size: 1.1 MB (1066872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd546d4cdeb688972bf1dc17560e2764ecadbc27221ed62675fd9228f0e7d9d`  
		Last Modified: Thu, 01 Feb 2024 06:43:09 GMT  
		Size: 58.8 MB (58820507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
