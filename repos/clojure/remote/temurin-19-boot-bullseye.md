## `clojure:temurin-19-boot-bullseye`

```console
$ docker pull clojure@sha256:fee6461c528329217eea7c22a55313f3f87503f0633423fa119f56a538840088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-19-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:d3c565301234d99db44e34cd64ab8c5c0e81007bf2ab2841954cebc8a1e5e7fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.3 MB (317341385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61b3f25871aacf4441b07e1c01679ad132c3776508ad15339a054ec10cd42c81`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:45 GMT
ADD file:513c5d5e501279c21a05c1d8b66e5f0b02ee4b27f0b928706d92fd9ce11c1be6 in / 
# Wed, 01 Mar 2023 04:09:46 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:40:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 07:49:43 GMT
COPY dir:94cb5af8175285c10c94286222d8a35302f3f8c290e00011a75c67156659d6ab in /opt/java/openjdk 
# Wed, 01 Mar 2023 07:49:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 07:49:45 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Mar 2023 07:49:45 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Mar 2023 07:49:45 GMT
WORKDIR /tmp
# Wed, 01 Mar 2023 07:49:51 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Mar 2023 07:49:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Mar 2023 07:49:51 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Mar 2023 07:50:09 GMT
RUN boot
# Wed, 01 Mar 2023 07:50:09 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 01 Mar 2023 07:50:09 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 01 Mar 2023 07:50:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:32fb02163b6bb519a30f909008e852354dae10bdfd6b34190dbdfe8f15403ea0`  
		Last Modified: Wed, 01 Mar 2023 04:13:58 GMT  
		Size: 55.0 MB (55045922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28081d65626e3fe290ed0277941e3e5a31dee293f2403db18b27a4b41888fb76`  
		Last Modified: Wed, 01 Mar 2023 08:00:49 GMT  
		Size: 201.1 MB (201112993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1fdcce508edd3816ebe6d4eb01100d2eefc025051f25dbf4bc94320de7e99a`  
		Last Modified: Wed, 01 Mar 2023 08:00:35 GMT  
		Size: 2.4 MB (2361618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08a7a92ae4278909677b53831adc50dbf4c8947ab5eac1c370fe535b4154f42c`  
		Last Modified: Wed, 01 Mar 2023 08:00:38 GMT  
		Size: 58.8 MB (58820454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2836dc0c883824b3701fe842e3d98229db700cc2546737f30475d5fd04e041`  
		Last Modified: Wed, 01 Mar 2023 08:00:34 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-19-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e60f2294757013ed8e3f8859ca3dfd264a2d03623a58c2877215ca618d42e861
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.7 MB (314730199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2adb7918bfefe1afc277360bd6f4738580cc9c1f037332794a791f917f55d15`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:30 GMT
ADD file:a6a1df499d0d5b07fb366d776a11c42ddee6261e2425a921041b38e868192770 in / 
# Wed, 01 Mar 2023 02:20:30 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:01:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 03:09:13 GMT
COPY dir:9a6a873ca11063f6f04e7f088397a1fce771e2b1aa8590b72eb07158cfac883f in /opt/java/openjdk 
# Wed, 01 Mar 2023 03:09:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 03:09:17 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Mar 2023 03:09:17 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Mar 2023 03:09:17 GMT
WORKDIR /tmp
# Wed, 01 Mar 2023 03:09:22 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Mar 2023 03:09:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Mar 2023 03:09:22 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Mar 2023 03:09:39 GMT
RUN boot
# Wed, 01 Mar 2023 03:09:39 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 01 Mar 2023 03:09:39 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 01 Mar 2023 03:09:39 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0f5fe16b1836feccd4765ac5685fc7a7b9c73445cac94fc595d2ffbc3cb59a7a`  
		Last Modified: Wed, 01 Mar 2023 02:23:53 GMT  
		Size: 53.7 MB (53703215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f14b17f40d43b36c3ca31112958858ecb243428662f3cf865bcfd47ff1cf7c3`  
		Last Modified: Wed, 01 Mar 2023 03:19:11 GMT  
		Size: 199.9 MB (199855198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e5ca17536fd9194f5c18c3b1e9941b9469f82cc49fade200aabd23a3b471f6`  
		Last Modified: Wed, 01 Mar 2023 03:18:59 GMT  
		Size: 2.4 MB (2351009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cfcef5c1deb8dca1dd939a15f11c3f5581c504379a1926fbf58654aea2497e`  
		Last Modified: Wed, 01 Mar 2023 03:19:02 GMT  
		Size: 58.8 MB (58820378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c966c0431db5929c9cdcb91d09e819b2dd8398145a689d50f2c24cbaacecaadc`  
		Last Modified: Wed, 01 Mar 2023 03:18:58 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
