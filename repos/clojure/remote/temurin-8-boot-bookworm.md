## `clojure:temurin-8-boot-bookworm`

```console
$ docker pull clojure@sha256:de66d9d702b883a59b8377c9b849b7e3576ca0602b62ec3ebeaccd6cbec9960b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-boot-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:dc7d6d29771eaf2e0f32a51aa6c0cbd42a81d03083dd2bfc54e20f6f8cc40af9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 MB (217508163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac70d8f4e1f171af110623b9862b02ccf678d64985cb9ae19f3e35f097281e1`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:42 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Thu, 11 Jan 2024 02:37:43 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:50:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 04:51:42 GMT
COPY dir:a294625293e4e40913c98181a9aeff55bc5e737b728d424dfdc884f576bd8f8d in /opt/java/openjdk 
# Thu, 11 Jan 2024 04:51:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 04:51:43 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 11 Jan 2024 04:51:43 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 11 Jan 2024 04:51:43 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 04:51:50 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 11 Jan 2024 04:51:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jan 2024 04:51:50 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 11 Jan 2024 04:52:40 GMT
RUN boot
# Thu, 11 Jan 2024 04:52:41 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:1b13d4e1a46e5e969702ec92b7c787c1b6891bff7c21ad378ff6dbc9e751d5d4`  
		Last Modified: Thu, 11 Jan 2024 02:42:04 GMT  
		Size: 49.6 MB (49561490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ee0cab5ab6aa98c37ed3fc43d77bcaf83ea4c8a69ec6d510ecb9e0057ee49c`  
		Last Modified: Thu, 11 Jan 2024 05:14:21 GMT  
		Size: 103.6 MB (103598285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbad9ae50351bc0224317832f3ce474c72568b5010ee6bb51a05277c0d8834f`  
		Last Modified: Thu, 11 Jan 2024 05:14:12 GMT  
		Size: 5.5 MB (5527108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b6d6edcd5baea68eafe2adb0ad97f551010088a5ce1668f28119d93e309030`  
		Last Modified: Thu, 11 Jan 2024 05:14:14 GMT  
		Size: 58.8 MB (58821280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-boot-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:da4471b7519b459016aba0bb904f65de91f54594517faf2e6c18a2433d4dfe3b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216463733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8402802b23c8edfc408855d78cbc6b9a73adb1d99000c825a85ab9c6bd502d9e`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:33 GMT
ADD file:051a18650d326af1d23e30c93370e647e62f94887ce43b22e1808052bce4f2a6 in / 
# Thu, 11 Jan 2024 02:40:34 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 07:57:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 07:58:40 GMT
COPY dir:95966e8772805277b939f0a555f93ce7d7e01898449cdb0fb69c182fe80d4021 in /opt/java/openjdk 
# Thu, 11 Jan 2024 07:58:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 07:58:43 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 11 Jan 2024 07:58:43 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 11 Jan 2024 07:58:43 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 07:58:48 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 11 Jan 2024 07:58:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jan 2024 07:58:48 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 11 Jan 2024 07:59:18 GMT
RUN boot
# Thu, 11 Jan 2024 07:59:18 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:5665c1f9a9e17acd68ae05b2839df402eac34afdd095f8c115f09886d757840c`  
		Last Modified: Thu, 11 Jan 2024 02:43:41 GMT  
		Size: 49.6 MB (49592247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0473a06dd3e65811b2c343888eadcab9128c6ea79472e9800f83ce98d6ea356c`  
		Last Modified: Thu, 11 Jan 2024 08:17:59 GMT  
		Size: 102.7 MB (102701526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b9e0c2027d3577fa1a2a775ac00300f90ffae72c3501d718ce13a2e4eda2a5`  
		Last Modified: Thu, 11 Jan 2024 08:17:53 GMT  
		Size: 5.3 MB (5349215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6425756450be8cdc108c5d98bcf206e3d7ba1638b0991d53f804ae48e2da7997`  
		Last Modified: Thu, 11 Jan 2024 08:17:55 GMT  
		Size: 58.8 MB (58820745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
