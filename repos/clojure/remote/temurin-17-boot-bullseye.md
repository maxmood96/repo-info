## `clojure:temurin-17-boot-bullseye`

```console
$ docker pull clojure@sha256:3e25966a0c884727ecaf9ce817c32f31964dbe95a1c90956f69008ccd9781c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:a394c9fa89ca7bea869320feb50a8fa69dd440f888ac411846a0e5ad9607b99b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261120956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:733ab7c959ce85853a1c1da0b5f3ac67bd5b7afd413e98406dc1fff047145358`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:38 GMT
ADD file:d3a2f1f42338ba7066e352cea3b7bf4c7576e6b96fef785e8da763114f337c0e in / 
# Tue, 19 Dec 2023 01:20:38 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:53:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 07:05:15 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Tue, 19 Dec 2023 07:05:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 07:05:16 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 19 Dec 2023 07:05:16 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 19 Dec 2023 07:05:16 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 07:05:22 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 19 Dec 2023 07:05:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 Dec 2023 07:05:22 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 19 Dec 2023 07:05:40 GMT
RUN boot
# Tue, 19 Dec 2023 07:05:40 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 19 Dec 2023 07:05:40 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 Dec 2023 07:05:40 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:18f2c3b7ca52caba205d748b9ce41784eb010ca83ece9e84e2a09130a5ec3cbc`  
		Last Modified: Tue, 19 Dec 2023 01:25:17 GMT  
		Size: 55.1 MB (55057340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a8723a17a720d83e3d9875a3c822dcbf06f9947afb9171f9c00341da1c2363`  
		Last Modified: Tue, 19 Dec 2023 07:22:18 GMT  
		Size: 144.9 MB (144873963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7a8a2633cb16659a803d47f7d51f8541f4549ac9cd43a908d4dc35817ad896`  
		Last Modified: Tue, 19 Dec 2023 07:22:07 GMT  
		Size: 2.4 MB (2368788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d430e9a2178ae53f5d04b499c8cd68d315f12078e73c522bf8fa8c5844d27f`  
		Last Modified: Tue, 19 Dec 2023 07:22:10 GMT  
		Size: 58.8 MB (58820463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:415e756ebf89f93b3201a1c3f7584b3a24c7589aa612f00529c4ca4dca7390d1`  
		Last Modified: Tue, 19 Dec 2023 07:22:06 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:26b85655f9bc8612f4641fdcbfe98cf3735596768735e3c328fad878bad09c59
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258568074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1943c1add91a6918e4c485e17f9e5d7ce8c306b06fa9e5cdeff20d0be4991e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:17 GMT
ADD file:06ba7e39a2f8e1a7bcbb929fa9d1e6fb1f8bdcf5096dc903576af8f7014e353b in / 
# Tue, 19 Dec 2023 01:41:18 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:55:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 07:04:36 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Tue, 19 Dec 2023 07:04:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 07:04:39 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 19 Dec 2023 07:04:39 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 19 Dec 2023 07:04:39 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 07:04:44 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 19 Dec 2023 07:04:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 Dec 2023 07:04:44 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 19 Dec 2023 07:05:00 GMT
RUN boot
# Tue, 19 Dec 2023 07:05:00 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 19 Dec 2023 07:05:00 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 Dec 2023 07:05:00 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:396a672fee8bade1a7c9f228d919717447f110f39046d8b5ed21ad45ae13ab61`  
		Last Modified: Tue, 19 Dec 2023 01:44:57 GMT  
		Size: 53.7 MB (53708091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd07311e78c2924fc080a1762e027781ac7b4ae611c86133314aba5a664a33ef`  
		Last Modified: Tue, 19 Dec 2023 07:19:23 GMT  
		Size: 143.7 MB (143681714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0867e5a13d451c249fd405b3af65d25cbffc40503c6a760cb65d45751f4349`  
		Last Modified: Tue, 19 Dec 2023 07:19:14 GMT  
		Size: 2.4 MB (2357517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f97da41410ebd65e975585d05fb49d33bf80f6d668ad0d9813f79e57fbcb94`  
		Last Modified: Tue, 19 Dec 2023 07:19:16 GMT  
		Size: 58.8 MB (58820352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978f694fbd03c66ddeb2afe472f32ccf6d86b8e617735a39b388fb202fd13aca`  
		Last Modified: Tue, 19 Dec 2023 07:19:14 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
