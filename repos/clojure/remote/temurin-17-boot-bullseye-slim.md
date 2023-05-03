## `clojure:temurin-17-boot-bullseye-slim`

```console
$ docker pull clojure@sha256:4994070f134ad26a7492670e1241d854cc96a67416b10623b0c8b95180c65bb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5afca65287d96eda2d0c773d6bf067f31943e5196c5029c2a006da5992481272
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.9 MB (283882330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84e4ccf6da5bd831d04a46f73300d4de28f8d108f918e2556754442c3aeccab2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 03 May 2023 20:30:06 GMT
COPY dir:097a611561277927a8e367a60640ce12877b7a6373689dec24d5cfb76f99c807 in /opt/java/openjdk 
# Wed, 03 May 2023 20:30:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 20:30:08 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 03 May 2023 20:30:08 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 03 May 2023 20:30:08 GMT
WORKDIR /tmp
# Wed, 03 May 2023 20:30:14 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 03 May 2023 20:30:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 03 May 2023 20:30:14 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 03 May 2023 20:30:31 GMT
RUN boot
# Wed, 03 May 2023 20:30:31 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 03 May 2023 20:30:31 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 03 May 2023 20:30:31 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd3b479fcddcbb50b65db69b8812d87215c90a11a644267765f3dc0e7f19bde9`  
		Last Modified: Wed, 03 May 2023 20:38:39 GMT  
		Size: 192.6 MB (192580429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621c903869bcd9ad994681d95fc3b7e94d3a183341e4530743b538ac02e0c046`  
		Last Modified: Wed, 03 May 2023 20:38:22 GMT  
		Size: 1.1 MB (1077516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f0b9fd8a26d9a7f8eea7bcec4b990d59760d737707e025c6365b1e17719ba0`  
		Last Modified: Wed, 03 May 2023 20:38:32 GMT  
		Size: 58.8 MB (58820472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1b55730d2647b70ac63dbad715d16b2dc9e30eee59e2525b648762f5ff4321`  
		Last Modified: Wed, 03 May 2023 20:38:22 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f9634f9ca86d5b9bd19c892dd991878d07b5540dfeed99e9709feb0b4bbfff81
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281326170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a55a2a7862042c08d5a4b3fcad1f344f5b64fafbc3652ef989c5c41996590cd6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 03 May 2023 00:22:49 GMT
ADD file:66d4d9078579608530442620145336062a293cc19f159b154a63a1bcdcce3f4c in / 
# Wed, 03 May 2023 00:22:50 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:44:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 03 May 2023 17:49:05 GMT
COPY dir:d3d9f08d06fd1214b20f5d901cee398f498773bedf69f0d3cc795772967cfe44 in /opt/java/openjdk 
# Wed, 03 May 2023 17:49:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 17:49:10 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 03 May 2023 17:49:10 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 03 May 2023 17:49:10 GMT
WORKDIR /tmp
# Wed, 03 May 2023 17:49:14 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 03 May 2023 17:49:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 03 May 2023 17:49:15 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 03 May 2023 17:49:32 GMT
RUN boot
# Wed, 03 May 2023 17:49:32 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 03 May 2023 17:49:32 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 03 May 2023 17:49:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:b5d25b35c1dbfa256bea3dd164b2048d6c7f8074a555213c493c36f07bf4c559`  
		Last Modified: Wed, 03 May 2023 00:25:53 GMT  
		Size: 30.1 MB (30052733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6baebd3611c04da99c6391c894e4c5ba7eaa103bf201a26eba6d26bbdd244f42`  
		Last Modified: Wed, 03 May 2023 17:56:41 GMT  
		Size: 191.4 MB (191387733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0fc846c08b7318ea63b766820855ed70be5ce95dba9c685160c156359d7f627`  
		Last Modified: Wed, 03 May 2023 17:56:31 GMT  
		Size: 1.1 MB (1064804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:316f11328c8bf81cb038d73c86d5c032342697e1670a0660aec36ddde5aa5795`  
		Last Modified: Wed, 03 May 2023 17:56:33 GMT  
		Size: 58.8 MB (58820503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b047eb4a1923d574a295d5e702b2ca2a59525b080f6200e43e7b78aef0ef3188`  
		Last Modified: Wed, 03 May 2023 17:56:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
