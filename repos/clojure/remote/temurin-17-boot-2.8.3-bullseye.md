## `clojure:temurin-17-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:a7635399bca87cae1e56d5eacdd1aa9830bded5acbfcbca688cd227b5fb714c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:61c7312aec3f8991e280adbfe685668721dd38ae8a81714cfd46507546c821c2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.7 MB (308660738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61cf2c1da7d33d872a0678a31dea3772192127ba42e2c50c5d5b297029aa0a36`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:42 GMT
ADD file:26702ba2c3e94cb21cdb3c550cf01cf848823d160f3417b559116d4c718e5df0 in / 
# Tue, 25 Oct 2022 01:43:42 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:32:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 07 Nov 2022 20:47:28 GMT
COPY dir:fa15c3254735d08fe4cb4c940d6fc08efc9755ff0499a6eb8e51c961cea48d5c in /opt/java/openjdk 
# Mon, 07 Nov 2022 20:47:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 20:47:30 GMT
ENV BOOT_VERSION=2.8.3
# Mon, 07 Nov 2022 20:47:30 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Mon, 07 Nov 2022 20:47:30 GMT
WORKDIR /tmp
# Mon, 07 Nov 2022 20:47:36 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Mon, 07 Nov 2022 20:47:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 07 Nov 2022 20:47:37 GMT
ENV BOOT_AS_ROOT=yes
# Mon, 07 Nov 2022 20:47:57 GMT
RUN boot
# Mon, 07 Nov 2022 20:47:57 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Mon, 07 Nov 2022 20:47:58 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 07 Nov 2022 20:47:58 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:17c9e6141fdb3387e5a1c07d4f9b6a05ac1498e96029fa3ea55470d4504f7770`  
		Last Modified: Tue, 25 Oct 2022 01:47:28 GMT  
		Size: 55.0 MB (55046332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b66875a43c96e16e03416e5d3e0d399e19e6ebbd34b69c21f639ea24b829431`  
		Last Modified: Mon, 07 Nov 2022 20:57:33 GMT  
		Size: 192.4 MB (192431266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde2c73f95b3d25c0ac41f5da3df389db58ccd36895cd6cd90eb91190aea63be`  
		Last Modified: Mon, 07 Nov 2022 20:57:19 GMT  
		Size: 2.4 MB (2362106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb951024b1c54da2557dd121ddd3bcd26f83086b2c6d6680f21e8a727e7f908`  
		Last Modified: Mon, 07 Nov 2022 20:57:22 GMT  
		Size: 58.8 MB (58820634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7d6729cb0866d6857c09229dcc40213b3bb6e2f5e73604671df5329dce3e6e`  
		Last Modified: Mon, 07 Nov 2022 20:57:18 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9265df24c00059eb59b1d2a174ac55cb64a64bac0c58d604b38aaca00a150132
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.1 MB (306090426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34b2a8efc2dbdb4fe192e94fffe64e786cecc11ff8061195ddf26760b87d9576`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 25 Oct 2022 05:45:55 GMT
ADD file:b16745ece8ef84c028d7e9ac4bf026ac64f885d4170bfcc9d435f237144a1b99 in / 
# Tue, 25 Oct 2022 05:45:56 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 23:53:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 07 Nov 2022 21:03:20 GMT
COPY dir:36850aee002fdc5445f17d75b8266c48f8e705973ece815c3b53d28b6656ac3e in /opt/java/openjdk 
# Mon, 07 Nov 2022 21:03:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 07 Nov 2022 21:03:25 GMT
ENV BOOT_VERSION=2.8.3
# Mon, 07 Nov 2022 21:03:25 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Mon, 07 Nov 2022 21:03:25 GMT
WORKDIR /tmp
# Mon, 07 Nov 2022 21:03:31 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Mon, 07 Nov 2022 21:03:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 07 Nov 2022 21:03:31 GMT
ENV BOOT_AS_ROOT=yes
# Mon, 07 Nov 2022 21:03:48 GMT
RUN boot
# Mon, 07 Nov 2022 21:03:49 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Mon, 07 Nov 2022 21:03:49 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 07 Nov 2022 21:03:49 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8e1d92e7d04d2a9a9880cb45dc3c32c2805912cd86abed96d0ada3ff28748205`  
		Last Modified: Tue, 25 Oct 2022 05:48:40 GMT  
		Size: 53.7 MB (53701966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a1e4dcae904908999385d0b955f5ebdc51329825e0aa473155c319828d97c6b`  
		Last Modified: Mon, 07 Nov 2022 21:11:42 GMT  
		Size: 191.2 MB (191215247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ceb788e6aa684039c6d03ab7a98baa2b9199a09d960a137a2b2fc5ce51c505`  
		Last Modified: Mon, 07 Nov 2022 21:11:30 GMT  
		Size: 2.4 MB (2352306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3f1d423724937f60b0043cc618c232f52108762942f32ac614fd2cf9f680c6`  
		Last Modified: Mon, 07 Nov 2022 21:11:33 GMT  
		Size: 58.8 MB (58820506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6c1f5f5d47efb27bb9645dcda56d7387d87b1b972a3df86eb080ad0976de1c`  
		Last Modified: Mon, 07 Nov 2022 21:11:30 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
