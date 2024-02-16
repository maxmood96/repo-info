## `clojure:temurin-17-boot-2.8.3-bookworm`

```console
$ docker pull clojure@sha256:ecc9c65fc1cfdaabaad86bac3685847f26770fbcdad65f248cd2bad0e7ae3b2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:d8e959a27f92af759a175e6931f914867c7a424e6013303773c171ad0e24c5a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.8 MB (258793381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0681a8bc64e4c96ddb374a75f33e9732f342cea72bd40722c41fe64c704621e4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:09 GMT
ADD file:333b899a197a48b3333115a3b59efed559494808873943f606a9bc2b6e242c49 in / 
# Tue, 13 Feb 2024 00:37:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:46:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 05:21:14 GMT
COPY dir:6673b976fb9ccd391df2de00f5738789bfa84c9bc068b98b869cb1d7436fd333 in /opt/java/openjdk 
# Fri, 16 Feb 2024 05:21:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 05:21:16 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 16 Feb 2024 05:21:16 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 16 Feb 2024 05:21:16 GMT
WORKDIR /tmp
# Fri, 16 Feb 2024 05:21:23 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 16 Feb 2024 05:21:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Feb 2024 05:21:23 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 16 Feb 2024 05:21:42 GMT
RUN boot
# Fri, 16 Feb 2024 05:21:42 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 16 Feb 2024 05:21:43 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Feb 2024 05:21:43 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7bb465c2914923b08ae03b7fc67b92a1ef9b09c4c1eb9d6711b22ee6bbb46a00`  
		Last Modified: Tue, 13 Feb 2024 00:41:39 GMT  
		Size: 49.6 MB (49552605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cee6a20b1d6827a6139790562d9fc18a62179a51eaaa22afa6fd789c3950e7c`  
		Last Modified: Fri, 16 Feb 2024 05:36:25 GMT  
		Size: 144.9 MB (144892557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:475672fad08e9c00fa10516950946d2d48e2c6b7d76859a39ee304aec7b5793d`  
		Last Modified: Fri, 16 Feb 2024 05:36:14 GMT  
		Size: 5.5 MB (5527270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3dc47ebb7e9ab678ef2c03bb51e50cf69e15d1432d044413cf66231d4585af`  
		Last Modified: Fri, 16 Feb 2024 05:36:16 GMT  
		Size: 58.8 MB (58820552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e525350aa198529ca348c504d727c5bfc5868407e1df43017a00ad4e67b38f5`  
		Last Modified: Fri, 16 Feb 2024 05:36:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a58e572edd6a90dfd0c5744807180fb0f2088b084c6e81726ca1d5f15060b033
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.5 MB (257482270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cdd2cc4d711002f92f848acc38392477072636195a7f848b40d04e33ec65bdb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:10 GMT
ADD file:73b36e8089732e9bb253d9a9db76cc1cf5c430bd49647849b77924cd5fdaf8ae in / 
# Tue, 13 Feb 2024 00:41:10 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:53:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Feb 2024 07:58:10 GMT
COPY dir:868002d69a8870cfd22502db6415e3cd8591d5271a62d90057620eefd5ce7d20 in /opt/java/openjdk 
# Fri, 16 Feb 2024 07:58:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2024 07:58:14 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 16 Feb 2024 07:58:14 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 16 Feb 2024 07:58:14 GMT
WORKDIR /tmp
# Fri, 16 Feb 2024 07:58:20 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 16 Feb 2024 07:58:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 16 Feb 2024 07:58:20 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 16 Feb 2024 07:58:38 GMT
RUN boot
# Fri, 16 Feb 2024 07:58:38 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Fri, 16 Feb 2024 07:58:38 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Feb 2024 07:58:38 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:c2964e85ea54bbef26d274e85fa0a3fde68f074e0774d0729e6ebe341e24eee1`  
		Last Modified: Tue, 13 Feb 2024 00:44:29 GMT  
		Size: 49.6 MB (49590965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3342fa935d374dc3389000b71ebda754f3edadc6d0478ccb4df3c5df36e0c8b`  
		Last Modified: Fri, 16 Feb 2024 08:11:25 GMT  
		Size: 143.7 MB (143720902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3bc108f7c430a96f8596db6a89b4856a3e74c24a2fed49ab7c6927fa0b19569`  
		Last Modified: Fri, 16 Feb 2024 08:11:17 GMT  
		Size: 5.3 MB (5349405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71fe1c864a40d9e87f356445b6352b8df13fef7af4eafb8198de292785f43075`  
		Last Modified: Fri, 16 Feb 2024 08:11:18 GMT  
		Size: 58.8 MB (58820600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50abe1092297a2125d386cc6b4beef1d98cceddd77fe6f9703e206c9c820b645`  
		Last Modified: Fri, 16 Feb 2024 08:11:16 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
