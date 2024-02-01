## `clojure:temurin-17-boot-bookworm`

```console
$ docker pull clojure@sha256:ffba574c51a40a5e319d554cf430e0fc1d7bf203298c50207d9bbd9fd26e5e73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:78a1ad707a662c1f9839bfbf9a172f2a6631b881c8d772dceb5386e6994a19fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.8 MB (258827595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ddab3ae7e15e5cc1539a052187a448c3da02fd33913c91cec81bebccdf3914`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:05 GMT
ADD file:6d9e71f0d3afb0b288cf2c06425795d528a142872692072ab1cd1ad275b67d1f in / 
# Wed, 31 Jan 2024 22:35:06 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:41:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 31 Jan 2024 23:54:01 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Wed, 31 Jan 2024 23:54:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 31 Jan 2024 23:54:02 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 31 Jan 2024 23:54:02 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 31 Jan 2024 23:54:02 GMT
WORKDIR /tmp
# Wed, 31 Jan 2024 23:54:08 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 31 Jan 2024 23:54:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 31 Jan 2024 23:54:08 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 31 Jan 2024 23:54:27 GMT
RUN boot
# Wed, 31 Jan 2024 23:54:28 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 31 Jan 2024 23:54:28 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 31 Jan 2024 23:54:28 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6a299ae9cfd996c1149a699d36cdaa76fa332c8e9d66d6678fa9a231d9ead04c`  
		Last Modified: Wed, 31 Jan 2024 22:39:27 GMT  
		Size: 49.6 MB (49583754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:905caf01436c21afb3e3cd4e9723995acc020cdcf8335a6ac61199bf19d74e37`  
		Last Modified: Thu, 01 Feb 2024 00:11:59 GMT  
		Size: 144.9 MB (144892527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9830dfffbebfa803bf72523161fec16caea854881fd6513bfab7b405e517a6cc`  
		Last Modified: Thu, 01 Feb 2024 00:11:49 GMT  
		Size: 5.5 MB (5530357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6af28312d228f64a7f6ae48053df0208f21bacd2400a26939945a7433b6d1e3`  
		Last Modified: Thu, 01 Feb 2024 00:11:51 GMT  
		Size: 58.8 MB (58820557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdae56da2eeba1f94f0f188d6e1b529251920b27e55d1a628e08f50df1b7e07e`  
		Last Modified: Thu, 01 Feb 2024 00:11:48 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b3f43178d234ac2185955feaf59d50a2e64a091e056a8b91370f7beb77c800e9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.5 MB (257510475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97040a5049493a661aa2fe54281bb0199dd79a3383ade2ae578e5e330fb57a26`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:15 GMT
ADD file:8bc7f537dd3dc4b92ec9006080fd563cc79205ee1ec3f456d03e869125a5bc21 in / 
# Wed, 31 Jan 2024 22:44:15 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:18:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Feb 2024 06:29:32 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Thu, 01 Feb 2024 06:29:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Feb 2024 06:29:35 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 01 Feb 2024 06:29:35 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 01 Feb 2024 06:29:35 GMT
WORKDIR /tmp
# Thu, 01 Feb 2024 06:29:41 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 01 Feb 2024 06:29:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 01 Feb 2024 06:29:41 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 01 Feb 2024 06:29:58 GMT
RUN boot
# Thu, 01 Feb 2024 06:29:58 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 01 Feb 2024 06:29:58 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Feb 2024 06:29:59 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:66932e2b787d33a94ee3eb8b489be6e6838b29f5c1d732262da306da9b1f2eed`  
		Last Modified: Wed, 31 Jan 2024 22:47:40 GMT  
		Size: 49.6 MB (49615296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c897b1db3cde970641a7e5eb09c234946039c6c77786e114c7eac70c67203419`  
		Last Modified: Thu, 01 Feb 2024 06:45:28 GMT  
		Size: 143.7 MB (143720907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab6c486f6eced937139ca4a8897103ad6be75a8aedbb78ca4d3d51308d535730`  
		Last Modified: Thu, 01 Feb 2024 06:45:20 GMT  
		Size: 5.4 MB (5353362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff43185560916d835bda22e98150a13f62ae99f730ac88e33e1fc9c478b8cba1`  
		Last Modified: Thu, 01 Feb 2024 06:45:22 GMT  
		Size: 58.8 MB (58820510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb948082e280897bda7463f9da3d01b2def563e3192fe80a9fc7c5cfc2bbc3d4`  
		Last Modified: Thu, 01 Feb 2024 06:45:19 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
