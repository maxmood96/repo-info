## `clojure:temurin-8-boot-bullseye`

```console
$ docker pull clojure@sha256:2e201271fe0436daaeafbd9bcd771092f86eaaca582d7eae539decd89abc798f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:bd1b2340c9a3498f2c95a58d2652542c3ac1e4652764607c9d4a0512a87f749c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.8 MB (219759739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b29ecc3d847e61fbe616b01e49b06d46805506c21bbbc2f1e0a79d7c72f31fba`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:42 GMT
ADD file:26702ba2c3e94cb21cdb3c550cf01cf848823d160f3417b559116d4c718e5df0 in / 
# Tue, 25 Oct 2022 01:43:42 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:32:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 05 Nov 2022 01:05:42 GMT
COPY dir:53540f2d79f4eef9b2bf8c4b39ecdbbd82fb14bfcf951e14853afffd2efa2ecb in /opt/java/openjdk 
# Sat, 05 Nov 2022 01:05:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Nov 2022 01:05:43 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 05 Nov 2022 01:05:43 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 05 Nov 2022 01:05:43 GMT
WORKDIR /tmp
# Sat, 05 Nov 2022 01:05:50 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 05 Nov 2022 01:05:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 05 Nov 2022 01:05:50 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 05 Nov 2022 01:06:11 GMT
RUN boot
# Sat, 05 Nov 2022 01:06:11 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:17c9e6141fdb3387e5a1c07d4f9b6a05ac1498e96029fa3ea55470d4504f7770`  
		Last Modified: Tue, 25 Oct 2022 01:47:28 GMT  
		Size: 55.0 MB (55046332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f77be6fc7ee7a23862824d57222a5b7aab790f7c035085316a7a705cdf9f3d`  
		Last Modified: Sat, 05 Nov 2022 01:21:48 GMT  
		Size: 103.5 MB (103530617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7027a68c71e2137790b76fb8c72b254402032dc6b77c0b1aea0447be979cbd42`  
		Last Modified: Sat, 05 Nov 2022 01:21:39 GMT  
		Size: 2.4 MB (2362203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7334328207fc98629fd94a75886c7832f78f23a8f458b392f25208df2167c0b2`  
		Last Modified: Sat, 05 Nov 2022 01:21:43 GMT  
		Size: 58.8 MB (58820587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ce46e6b5d61755ff9af8def26bdea822b56379f341862e8858dafc780fed84c3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 MB (217501443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9d98d7f004c34b067cb1f84c4ccb20fb1d86b63964ab0105bf7ebe0c2bd36f`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 25 Oct 2022 05:45:55 GMT
ADD file:b16745ece8ef84c028d7e9ac4bf026ac64f885d4170bfcc9d435f237144a1b99 in / 
# Tue, 25 Oct 2022 05:45:56 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 23:53:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 04 Nov 2022 23:07:17 GMT
COPY dir:8a3fd802e7e57a45d80b19a89e91b421563b952585d39995819354f278317671 in /opt/java/openjdk 
# Fri, 04 Nov 2022 23:07:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Nov 2022 23:07:20 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 04 Nov 2022 23:07:20 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 04 Nov 2022 23:07:20 GMT
WORKDIR /tmp
# Fri, 04 Nov 2022 23:07:26 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 04 Nov 2022 23:07:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 04 Nov 2022 23:07:26 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 04 Nov 2022 23:07:48 GMT
RUN boot
# Fri, 04 Nov 2022 23:07:48 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:8e1d92e7d04d2a9a9880cb45dc3c32c2805912cd86abed96d0ada3ff28748205`  
		Last Modified: Tue, 25 Oct 2022 05:48:40 GMT  
		Size: 53.7 MB (53701966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee19b345ab323043bdfd21232589344dffd26f964f848e9862ddd6f0d36d3db`  
		Last Modified: Fri, 04 Nov 2022 23:19:59 GMT  
		Size: 102.6 MB (102626601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3761b5794646d5538709fe74ea790e33d4fb83c0f32645dd074671dcbeef71e9`  
		Last Modified: Fri, 04 Nov 2022 23:19:52 GMT  
		Size: 2.4 MB (2352299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61b05abd0b399cd10531459468fd9d1cdba3b746ac1576f5ae25d23cf5cebe6`  
		Last Modified: Fri, 04 Nov 2022 23:19:55 GMT  
		Size: 58.8 MB (58820577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
