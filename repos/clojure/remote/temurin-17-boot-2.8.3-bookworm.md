## `clojure:temurin-17-boot-2.8.3-bookworm`

```console
$ docker pull clojure@sha256:db79eeaab40418dba68f05e5b97ee65aca42bc59a87861fa25818c7984d91a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bookworm` - linux; amd64

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
