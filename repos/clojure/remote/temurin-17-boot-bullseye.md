## `clojure:temurin-17-boot-bullseye`

```console
$ docker pull clojure@sha256:56cbd14fecc601bd531cb407051f4e8351c20c3de160824d4df5f4ee88e9796f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:57a8092ec5a8789469047c699b7e509345261c8e5160d05f598cc1d023529e66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.0 MB (261015430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:417a55b3303ef80fda97ba6f8ac0e0b9edd1e773bac22f8ba2275f4aea5c43ab`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 20 Sep 2023 04:55:51 GMT
ADD file:85db4f4c5016f51f7112a5d09cb7d4620f565a1379ae4b8a03c5ffc23886a876 in / 
# Wed, 20 Sep 2023 04:55:51 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:21:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 Sep 2023 07:27:45 GMT
COPY dir:61bbef45bd137d5078f6a6f774d9bc49d275ae5fe27274294232d075ae1a5bf2 in /opt/java/openjdk 
# Wed, 20 Sep 2023 07:27:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 07:27:47 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 20 Sep 2023 07:27:47 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 20 Sep 2023 07:27:47 GMT
WORKDIR /tmp
# Wed, 20 Sep 2023 07:27:53 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 20 Sep 2023 07:27:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 Sep 2023 07:27:53 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 20 Sep 2023 07:28:10 GMT
RUN boot
# Wed, 20 Sep 2023 07:28:10 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 20 Sep 2023 07:28:11 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 Sep 2023 07:28:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ddf874abf16cc990e0fd75a154a34ca0a03ee310ad895a18fb62ae15bf4171fb`  
		Last Modified: Wed, 20 Sep 2023 05:00:41 GMT  
		Size: 55.1 MB (55056714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf4a672ed9955378a963316cbf18411e8a03dfdf04af1c6124a50daf2a46955`  
		Last Modified: Wed, 20 Sep 2023 07:37:17 GMT  
		Size: 144.8 MB (144775739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8f951f10159e45e345e354fcb2238a13ddc9c44ea8ac2f620f7bbd6adadbc1`  
		Last Modified: Wed, 20 Sep 2023 07:37:05 GMT  
		Size: 2.4 MB (2362095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d7fbe130a41acb26242463b46399a52d39b0f0805b280ca6e0392d9a910a5f`  
		Last Modified: Wed, 20 Sep 2023 07:37:11 GMT  
		Size: 58.8 MB (58820483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba26c4398e028d3d9e75d98163478681361e356df535eb4a24b3408efec78704`  
		Last Modified: Wed, 20 Sep 2023 07:37:05 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1e10a2196f080c048c258cd538526f4a2af73700e4529db618ee98bc419e0792
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.4 MB (258420374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64dae3e98d9984ee439cd3869ecd631ea991ae7896264141cbe5624954c4e360`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:45 GMT
ADD file:6bc001e951ef1280f566a92e65fcff57aefb8a280aa3510b7cd4b4e0a54c5cff in / 
# Thu, 07 Sep 2023 00:39:46 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 09:03:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 Sep 2023 09:09:15 GMT
COPY dir:ffc7dc4725a3524e0b294e59a90d1e58e69ec448374b50aef6bef0cfa219cb0f in /opt/java/openjdk 
# Thu, 07 Sep 2023 09:09:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 09:09:18 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 07 Sep 2023 09:09:18 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 07 Sep 2023 09:09:19 GMT
WORKDIR /tmp
# Thu, 07 Sep 2023 09:09:24 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 07 Sep 2023 09:09:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 07 Sep 2023 09:09:24 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 07 Sep 2023 09:09:41 GMT
RUN boot
# Thu, 07 Sep 2023 09:09:41 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 07 Sep 2023 09:09:41 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 07 Sep 2023 09:09:41 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:61c16b7975697b00760ff9536c09eed29b6a76923d4d98be38e9cdc749506417`  
		Last Modified: Thu, 07 Sep 2023 00:43:21 GMT  
		Size: 53.7 MB (53704716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11abafe6bd868d46b7ee281876a4f1449b1024ece764bcbdf2e54191d6f14bf0`  
		Last Modified: Thu, 07 Sep 2023 09:17:33 GMT  
		Size: 143.5 MB (143543491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be05c2962b5ebaa558079a426a506136d92228b44d2ffd055747b5e83232655`  
		Last Modified: Thu, 07 Sep 2023 09:17:24 GMT  
		Size: 2.4 MB (2351383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33997da7a0b618ef7594a8377e559dbe26038d7191738e9419fc06b4737d5073`  
		Last Modified: Thu, 07 Sep 2023 09:17:26 GMT  
		Size: 58.8 MB (58820385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00699bb9a628d649b3f9ff85acc796643f7a0dce26c32b4e3b52b72e6fa4f88b`  
		Last Modified: Thu, 07 Sep 2023 09:17:23 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
