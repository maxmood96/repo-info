## `clojure:temurin-17-boot-2.8.3-bookworm`

```console
$ docker pull clojure@sha256:f6b92cfc1e3efaa39be6a44ffcf2cbbd3bf18298a81cd3db9e83c371b5dbb157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:19a32a47b40057a0d2d54931aa3310dd13839949d4309ae260fa1716602022af
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.8 MB (258801874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f6dfce7c42fd12ce783100e8509319c16db7e2366f7000e7aac10f12e2008d6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:42 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Thu, 11 Jan 2024 02:37:43 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:50:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:17:26 GMT
COPY dir:f32129cdf16cd5eee81dc24c5e5457011e489f134c2a5ee643ddf8ee33a43952 in /opt/java/openjdk 
# Wed, 24 Jan 2024 22:17:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 22:17:28 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 24 Jan 2024 22:17:28 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 24 Jan 2024 22:17:28 GMT
WORKDIR /tmp
# Wed, 24 Jan 2024 22:17:34 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 24 Jan 2024 22:17:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jan 2024 22:17:35 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 24 Jan 2024 22:17:51 GMT
RUN boot
# Wed, 24 Jan 2024 22:17:52 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 24 Jan 2024 22:17:52 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jan 2024 22:17:52 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1b13d4e1a46e5e969702ec92b7c787c1b6891bff7c21ad378ff6dbc9e751d5d4`  
		Last Modified: Thu, 11 Jan 2024 02:42:04 GMT  
		Size: 49.6 MB (49561490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb5e1df2b4a0ba2b0aa23e27252a2b6f4b9f6adfac076da3f6f2f19e8e3f88b`  
		Last Modified: Wed, 24 Jan 2024 22:41:53 GMT  
		Size: 144.9 MB (144892492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b94090d6814fa941651546124a66bdd4bb86da32e8427b3d1423ebf6bde9343`  
		Last Modified: Wed, 24 Jan 2024 22:41:42 GMT  
		Size: 5.5 MB (5527148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e2be35524bfcfda3798f32a7734b2381e6009b7bf182c4eeb13be313004ca8`  
		Last Modified: Wed, 24 Jan 2024 22:41:45 GMT  
		Size: 58.8 MB (58820343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7518394867a776357d0c97c3330b98f0ec038154710a34a701d9dd2bbaef4fd`  
		Last Modified: Wed, 24 Jan 2024 22:41:41 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ca59448216820e57e511ee13913431caa506e822dc576bd74c9b4ca51e668df1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.5 MB (257483023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc041a07c96a2dc68f54341110694a6d8df9cb6e5589e1f24a8a40f4355cf5d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:33 GMT
ADD file:051a18650d326af1d23e30c93370e647e62f94887ce43b22e1808052bce4f2a6 in / 
# Thu, 11 Jan 2024 02:40:34 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 07:57:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 22:20:42 GMT
COPY dir:7c9e57a7678108e8f16bbe5ccb6616df59216fd52f6dd8321cc6163370ace185 in /opt/java/openjdk 
# Wed, 24 Jan 2024 22:20:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 22:20:46 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 24 Jan 2024 22:20:46 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 24 Jan 2024 22:20:46 GMT
WORKDIR /tmp
# Wed, 24 Jan 2024 22:20:51 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 24 Jan 2024 22:20:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 24 Jan 2024 22:20:51 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 24 Jan 2024 22:21:06 GMT
RUN boot
# Wed, 24 Jan 2024 22:21:06 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 24 Jan 2024 22:21:06 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jan 2024 22:21:07 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5665c1f9a9e17acd68ae05b2839df402eac34afdd095f8c115f09886d757840c`  
		Last Modified: Thu, 11 Jan 2024 02:43:41 GMT  
		Size: 49.6 MB (49592247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d07bf629912a33be9736b6aba7cbb75b4ac2c3febaac5979dfd568c3169d333`  
		Last Modified: Wed, 24 Jan 2024 22:41:23 GMT  
		Size: 143.7 MB (143720870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bce1781486868f6649d587afb717067ee401151bcf8c6bc46a2b38b1621f5d8`  
		Last Modified: Wed, 24 Jan 2024 22:41:14 GMT  
		Size: 5.3 MB (5349251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6525b8b990a4e97dd6a158412d93b40f0e409cea03f8efb39afd958a3eb19d80`  
		Last Modified: Wed, 24 Jan 2024 22:41:17 GMT  
		Size: 58.8 MB (58820254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590fd3deb52d794af1e11edb084f5e6e78dd9458709bb8063c69e6e2f4521f9b`  
		Last Modified: Wed, 24 Jan 2024 22:41:14 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
