## `clojure:temurin-17-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:234295e7883573b82bc872814ed56b305300b6d5089c8be49d55939b6b005584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ecaab745fc5bd61c403703941b83638c33873164733d59e7d71bfc1ba621596e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.2 MB (236192134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf96a035a355cf35325cad8451352615101dc53defc17161a777eb641aa1b37`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Dec 2023 14:06:55 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Sat, 16 Dec 2023 15:34:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Dec 2023 15:34:02 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 16 Dec 2023 15:34:02 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 16 Dec 2023 15:34:02 GMT
WORKDIR /tmp
# Sat, 16 Dec 2023 15:34:07 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 16 Dec 2023 15:34:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 16 Dec 2023 15:34:07 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 16 Dec 2023 15:34:24 GMT
RUN boot
# Sat, 16 Dec 2023 15:34:24 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Sat, 16 Dec 2023 15:34:24 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Dec 2023 15:34:24 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d14040669239de7bca2344d0124913a16ae7c1d2b4c9c7fd78bed42344683be`  
		Last Modified: Sat, 16 Dec 2023 14:10:12 GMT  
		Size: 144.9 MB (144873945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7feeb2f3283d3aee3c068788e252ca39d5a70a12b02f639b02571231df521c6c`  
		Last Modified: Sat, 16 Dec 2023 15:49:37 GMT  
		Size: 1.1 MB (1079479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ceede2de30f008504cf7e641274e4ecc9a8a336d50ebc828a038b7746ee775`  
		Last Modified: Sat, 16 Dec 2023 15:49:40 GMT  
		Size: 58.8 MB (58820486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea19cea0419465a13ef4bef68e5965e4bc364003697d9e341dfcccb450eec90b`  
		Last Modified: Sat, 16 Dec 2023 15:49:37 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:75ee53894f7f6b8d6ae20941e198433a0ed2b3199542ae860bf8a6c9925b0d5d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233633397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc3310758ea10b27291a4d45824eb725a2a5cde817ccd90e9a97731aed8acf0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 08:54:33 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Sat, 02 Dec 2023 08:54:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 08:54:36 GMT
ENV BOOT_VERSION=2.8.3
# Sat, 02 Dec 2023 08:54:36 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Sat, 02 Dec 2023 08:54:36 GMT
WORKDIR /tmp
# Sat, 02 Dec 2023 08:54:41 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Sat, 02 Dec 2023 08:54:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Sat, 02 Dec 2023 08:54:41 GMT
ENV BOOT_AS_ROOT=yes
# Sat, 02 Dec 2023 08:54:57 GMT
RUN boot
# Sat, 02 Dec 2023 08:54:57 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Sat, 02 Dec 2023 08:54:57 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 02 Dec 2023 08:54:58 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d93fb72555944d51d7e18e85dbba1405725af6fa11dc155f20ab3dc455df52`  
		Last Modified: Sat, 02 Dec 2023 09:08:50 GMT  
		Size: 143.7 MB (143681749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28a946ea6e7a547181655f7690fb82f9ccc4f140040ea712fb23a3b4146eafd`  
		Last Modified: Sat, 02 Dec 2023 09:08:38 GMT  
		Size: 1.1 MB (1066829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd976269ff9bc013147dccb3c0ea5103e01393baff92a2f50858e7a5d7b6f3f6`  
		Last Modified: Sat, 02 Dec 2023 09:08:40 GMT  
		Size: 58.8 MB (58820295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed8ea7f126b2558cc2e0deb2134e869db53c0d9377ce457f586f6fa7dabfe268`  
		Last Modified: Sat, 02 Dec 2023 09:08:38 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
