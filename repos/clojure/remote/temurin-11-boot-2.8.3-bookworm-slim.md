## `clojure:temurin-11-boot-2.8.3-bookworm-slim`

```console
$ docker pull clojure@sha256:5f8ca732b4385f29a644676c56425e0aec57499e8ec77d71900745cfafe11442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:41ce696ee84bf2ff902d3957f7d4eb33c3c2d42aa1a60544104ecebcfa355102
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 MB (236721305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbbac7ed3a91ea784e7777ba83cf9e656b2bb26bc8839ff2cfec77df51f82ba4`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:48 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Wed, 10 Apr 2024 01:50:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:17:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 06:23:14 GMT
COPY dir:4cef005a87cd4606dd69ccb04c755a46f4aa2c925fb1aacc59928d64687208f2 in /opt/java/openjdk 
# Wed, 10 Apr 2024 06:23:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:23:16 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 10 Apr 2024 06:23:16 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 10 Apr 2024 06:23:16 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 06:23:22 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 10 Apr 2024 06:23:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 10 Apr 2024 06:23:22 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 10 Apr 2024 06:23:41 GMT
RUN boot
# Wed, 10 Apr 2024 06:23:42 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed28721d3594017943f3547d57bc37d04bfc57a97f0bce49df19ccea514aace`  
		Last Modified: Wed, 10 Apr 2024 06:42:39 GMT  
		Size: 145.3 MB (145271203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a24ce234101524f7f1f7f3e11266c5a14d5960ada88b2c556c036341bce61ba2`  
		Last Modified: Wed, 10 Apr 2024 06:42:29 GMT  
		Size: 3.5 MB (3498220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47fab44babf7f528663479784cba1b8624bdddc319aaf9b4784ccd8eb53f604`  
		Last Modified: Wed, 10 Apr 2024 06:42:31 GMT  
		Size: 58.8 MB (58820524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ba2a945c19625d9fb190542186b1647f72ae90c9ccc826949155da6a5686341b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.3 MB (233311243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10aef280d63269a05fb32fc7cbc767adae67b7cd9c6fa541800e15e316b77598`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:23 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Wed, 10 Apr 2024 00:40:23 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:38:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 04:43:45 GMT
COPY dir:d5fb8d9a38dea7496f2aff176bc9a34bbca80551c2dc57109d2dae5907a339ee in /opt/java/openjdk 
# Wed, 10 Apr 2024 04:43:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 04:43:49 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 10 Apr 2024 04:43:49 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 10 Apr 2024 04:43:49 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 04:43:54 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 10 Apr 2024 04:43:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 10 Apr 2024 04:43:54 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 10 Apr 2024 04:44:12 GMT
RUN boot
# Wed, 10 Apr 2024 04:44:12 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013c2e6bf82efe02b13eb59abbd4169a1826267ea9b1eb19d743ae4301e7c31c`  
		Last Modified: Wed, 10 Apr 2024 05:01:34 GMT  
		Size: 142.0 MB (142006347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1025ac5ede5c1105d55fc7acf700790063d7c34fcfdba2da495b5a6171702733`  
		Last Modified: Wed, 10 Apr 2024 05:01:26 GMT  
		Size: 3.3 MB (3322171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f548b028a176335ae096a1b65127beea399135382ca333526a249963bf2dc48`  
		Last Modified: Wed, 10 Apr 2024 05:01:29 GMT  
		Size: 58.8 MB (58820568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
