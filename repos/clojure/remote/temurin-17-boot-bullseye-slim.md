## `clojure:temurin-17-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:ba1e105726cddabcdbfe2da39b38a6f68805a2dc4b3f53c72a5756e87907770d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:245d85c8ac41d505eb896fc09ef6ef699cccf8d3e0e92b1357b52ee99e648b18
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.2 MB (236210776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cb42d6d4ff1c932498584091de2aceb8e796611180848b6bc597ab777785e0e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:44:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 23:55:44 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Wed, 31 Jan 2024 23:55:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:55:45 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 31 Jan 2024 23:55:45 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 31 Jan 2024 23:55:45 GMT
WORKDIR /tmp
# Wed, 31 Jan 2024 23:55:51 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 31 Jan 2024 23:55:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 31 Jan 2024 23:55:51 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 31 Jan 2024 23:56:09 GMT
RUN boot
# Wed, 31 Jan 2024 23:56:09 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 31 Jan 2024 23:56:09 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 31 Jan 2024 23:56:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada2cf41cb8c5a69262cd16ed219afecfb15a02b85a90f3f7b04709e0dc6dd35`  
		Last Modified: Thu, 01 Feb 2024 00:13:12 GMT  
		Size: 144.9 MB (144892503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2754ed8628a6e8ce037c32b542b3de59cfaa897f7ec2621d1b728b718cf119`  
		Last Modified: Thu, 01 Feb 2024 00:12:59 GMT  
		Size: 1.1 MB (1079493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6116485c8782a79dd201601ec3070eb3d8582de0f100b8c112264de6383c3bc2`  
		Last Modified: Thu, 01 Feb 2024 00:13:09 GMT  
		Size: 58.8 MB (58820550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec037ae86e991d7bba6fee6591177dbf6e3d4b524498b2ae183b2d655b57a97f`  
		Last Modified: Thu, 01 Feb 2024 00:12:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dab32d621ad1848d1a25d8d9c6f5facf1b277db0e63ace4250976e74dc83d354
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.7 MB (233672974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d6b7b53381a4d9f39c2daf5b920c97aabdd3497782dd93378dcde7ae706711`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:42 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Wed, 31 Jan 2024 22:44:42 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:21:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 06:31:13 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Thu, 01 Feb 2024 06:31:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:31:17 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 01 Feb 2024 06:31:17 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 01 Feb 2024 06:31:17 GMT
WORKDIR /tmp
# Thu, 01 Feb 2024 06:31:22 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 01 Feb 2024 06:31:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 01 Feb 2024 06:31:22 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 01 Feb 2024 06:31:39 GMT
RUN boot
# Thu, 01 Feb 2024 06:31:39 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 01 Feb 2024 06:31:39 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Feb 2024 06:31:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772d5b458459761483051b45f421f5aff8c05038820ab7bed52a988cb2718dca`  
		Last Modified: Thu, 01 Feb 2024 06:46:25 GMT  
		Size: 143.7 MB (143720888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a40be2036dbd20cf84b26de88723bc899fb72a968e667f264fce501c99c815`  
		Last Modified: Thu, 01 Feb 2024 06:46:15 GMT  
		Size: 1.1 MB (1066872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d694e2f48193666d207d4dc7818a5be003422b5b2608c7af255205a05b9d90`  
		Last Modified: Thu, 01 Feb 2024 06:46:18 GMT  
		Size: 58.8 MB (58820479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b923b88464c2adf5b52dbf98b88b312502cf7d252c2d3fc550723e8d974ab589`  
		Last Modified: Thu, 01 Feb 2024 06:46:15 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
