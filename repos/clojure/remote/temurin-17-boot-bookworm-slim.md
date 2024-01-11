## `clojure:temurin-17-boot-bookworm-slim`

```console
$ docker pull clojure@sha256:5b50da2b94f63624c81bb60ad90e2e7f60e1703af54d0829dd6036a04aa6394c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d2e8cb9034de33529586162a2ebbdb02e2ae45b66c21d5478dda9876efb6f8b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.3 MB (236318570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef81b71615926590ae04e602a1fdcf62c4cb2f05ecb2eff59d1670184db52f33`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:52:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:04:16 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Thu, 11 Jan 2024 05:04:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 05:04:18 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 11 Jan 2024 05:04:18 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 11 Jan 2024 05:04:18 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 05:04:24 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 11 Jan 2024 05:04:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jan 2024 05:04:24 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 11 Jan 2024 05:04:43 GMT
RUN boot
# Thu, 11 Jan 2024 05:04:43 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 11 Jan 2024 05:04:43 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jan 2024 05:04:43 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f048e54c11677788c22f8c8eb2f24de20279e99d3d9dc508ac867922b77d91ee`  
		Last Modified: Thu, 11 Jan 2024 05:21:33 GMT  
		Size: 144.9 MB (144873944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb5bbcb303286fdd21a83e2ae8bcef8093fd89ec74452c211a6db0a4c52e4e18`  
		Last Modified: Thu, 11 Jan 2024 05:21:22 GMT  
		Size: 3.5 MB (3498040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4b34892c267ce225d7c7f48d3f7a49cee4fc92636e301a1653fb45897be543`  
		Last Modified: Thu, 11 Jan 2024 05:21:25 GMT  
		Size: 58.8 MB (58820267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793f2407e99b76109216ee2ae3cbd63f6c14cfa9a05bb563f10f975489ae15ee`  
		Last Modified: Thu, 11 Jan 2024 05:21:21 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:649083fb4a62e57b9299aa3dcdf3d3389f0a53fa8eedbf0e5ed3f3378d2d3cff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (234981753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0515bc6b5914e1635a1faaa60d52899797430a9ac6957aee0d9bb89a8afbeec6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:11 GMT
ADD file:262fd7bf0bc26e5d2a229fba52626e22b8a93beac29733acfc60e716c26e689d in / 
# Tue, 19 Dec 2023 01:41:11 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:54:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 07:04:08 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Tue, 19 Dec 2023 07:04:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 07:04:11 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 19 Dec 2023 07:04:11 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 19 Dec 2023 07:04:11 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 07:04:16 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 19 Dec 2023 07:04:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 Dec 2023 07:04:17 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 19 Dec 2023 07:04:32 GMT
RUN boot
# Tue, 19 Dec 2023 07:04:33 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 19 Dec 2023 07:04:33 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 Dec 2023 07:04:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:24e221e92a36ab5b0075dd156b4f2ff095532a9b0927946cf6070bb1bea208b8`  
		Last Modified: Tue, 19 Dec 2023 01:44:38 GMT  
		Size: 29.2 MB (29157269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ee60140f19529393a1624031eddbd14b1675cecae82a1f83a9055965ebb645`  
		Last Modified: Tue, 19 Dec 2023 07:19:05 GMT  
		Size: 143.7 MB (143681714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdc13cff3b76d5fb94d2eb94ce62fa65e610938423a0a5e01e9b72b065045fa`  
		Last Modified: Tue, 19 Dec 2023 07:18:56 GMT  
		Size: 3.3 MB (3321960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4b48c67081dc03b26aa98973c14a5e1e582526fb49ccc0c4edd37e81777f34`  
		Last Modified: Tue, 19 Dec 2023 07:18:59 GMT  
		Size: 58.8 MB (58820409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97bd8003c6033755637b109c8864ac9718efd76c2ee3e0ee9c2a9b86baa9aea1`  
		Last Modified: Tue, 19 Dec 2023 07:18:56 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
