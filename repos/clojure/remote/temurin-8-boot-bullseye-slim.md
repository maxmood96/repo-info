## `clojure:temurin-8-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:c5eb0282686afd8077055dc0b544ad78077564f82a2d96097c4b1be47ffb2352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ab37930cf5fd3f62383a18e15c5db9cd423f86fe53e05edc57b123eb7833feef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.9 MB (194917933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0174339f97385fc3edd57a425f3a5269d2ed42a1b425eedfbe47cce56033c2d2`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:11 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
# Wed, 10 Apr 2024 01:51:11 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:18:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 06:18:37 GMT
COPY dir:7a6a87e7bb8d56b27d71b1f614847d2afb4282190a48214e2e48b164fbef7bc7 in /opt/java/openjdk 
# Wed, 10 Apr 2024 06:18:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:18:38 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 10 Apr 2024 06:18:38 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 10 Apr 2024 06:18:38 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 06:18:44 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 10 Apr 2024 06:18:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 10 Apr 2024 06:18:44 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 10 Apr 2024 06:19:04 GMT
RUN boot
# Wed, 10 Apr 2024 06:19:04 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55ef082ce01a10224573de24abd18368efb3c2247c2930a6621d743ff95b2a5`  
		Last Modified: Wed, 10 Apr 2024 06:39:53 GMT  
		Size: 103.6 MB (103591917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76360f39ee39c8b73368793948071fae82f39bef7c383045bff31e3a755de167`  
		Last Modified: Wed, 10 Apr 2024 06:39:45 GMT  
		Size: 1.1 MB (1077712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b890eff41ee66b07af6ef71bff9daf4e50eb1a60becba6efb6d805f5f843cb73`  
		Last Modified: Wed, 10 Apr 2024 06:39:48 GMT  
		Size: 58.8 MB (58820566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:60e7ae743ec157aac770cb21fae0dbea68b23386c0bae47fbb1d3fe9a2c055cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.7 MB (192664808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b89a3a38a87697204b2a125d267042904087a8195dda712db45006216a2f858e`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:38 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Wed, 10 Apr 2024 00:40:39 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:39:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 10 Apr 2024 04:39:58 GMT
COPY dir:d67e1a8d4006c4d31bb089f955cdf6054ae46936c41fb4bbc9c830e6a49d11d6 in /opt/java/openjdk 
# Wed, 10 Apr 2024 04:40:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 04:40:00 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 10 Apr 2024 04:40:00 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 10 Apr 2024 04:40:00 GMT
WORKDIR /tmp
# Wed, 10 Apr 2024 04:40:05 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 10 Apr 2024 04:40:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 10 Apr 2024 04:40:05 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 10 Apr 2024 04:40:23 GMT
RUN boot
# Wed, 10 Apr 2024 04:40:24 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dc7b60cefd1fc4e73a9a6119c7259d78c2ad4535fc7ae43de949e775da2cacb`  
		Last Modified: Wed, 10 Apr 2024 04:58:37 GMT  
		Size: 102.7 MB (102703050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f600be1e7fc2e7a2b8ac2e56fd39ddad5cb6da4a473aac7a1c602b15260eb959`  
		Last Modified: Wed, 10 Apr 2024 04:58:31 GMT  
		Size: 1.1 MB (1064950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e02f9a33126342f0bc96bc90331ae807dda47cdc6a8cd0b50c1ad9da4b1da8`  
		Last Modified: Wed, 10 Apr 2024 04:58:34 GMT  
		Size: 58.8 MB (58820502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
