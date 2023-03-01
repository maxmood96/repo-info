## `clojure:temurin-17-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:8f3354099e30100d70565bbc2371805c746e931bfbff512cff75f6c5cfbee546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:8857bc037344a04b30acc2baf6f5bf36bbfb6919100433513c893c6a1918c498
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.7 MB (308666284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e0898835540939f37c24cea0e1fc6f348bc69099967a7314f629e8e91d17c3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:45 GMT
ADD file:513c5d5e501279c21a05c1d8b66e5f0b02ee4b27f0b928706d92fd9ce11c1be6 in / 
# Wed, 01 Mar 2023 04:09:46 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:40:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 07:46:48 GMT
COPY dir:5cf52f938fe415b0022fbccb8cf978562c503c0b8313cc9dedf46c1c4edb35cf in /opt/java/openjdk 
# Wed, 01 Mar 2023 07:46:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 07:46:49 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Mar 2023 07:46:49 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Mar 2023 07:46:50 GMT
WORKDIR /tmp
# Wed, 01 Mar 2023 07:46:55 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Mar 2023 07:46:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Mar 2023 07:46:55 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Mar 2023 07:47:13 GMT
RUN boot
# Wed, 01 Mar 2023 07:47:13 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 01 Mar 2023 07:47:13 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 01 Mar 2023 07:47:13 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:32fb02163b6bb519a30f909008e852354dae10bdfd6b34190dbdfe8f15403ea0`  
		Last Modified: Wed, 01 Mar 2023 04:13:58 GMT  
		Size: 55.0 MB (55045922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e2398cb32ac1a57ed5e07eacb837ab8e304b5c7c8726bc0e525810f442bb47c`  
		Last Modified: Wed, 01 Mar 2023 07:58:35 GMT  
		Size: 192.4 MB (192438071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b287ca4bbd790d594f8ba5070b55e4c2f604c2839c9093f53a813e973517e3f7`  
		Last Modified: Wed, 01 Mar 2023 07:58:21 GMT  
		Size: 2.4 MB (2361569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de3213985b9bdefcfb642c991e9f1cc455f4cdf71da3df25ca35e915d27af55`  
		Last Modified: Wed, 01 Mar 2023 07:58:24 GMT  
		Size: 58.8 MB (58820322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47428a5d9277ccf7210bd8114735d99e72dbb8d41f1d313e7253f14d8ba234e8`  
		Last Modified: Wed, 01 Mar 2023 07:58:20 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ab3913a2c40a39a3e4c2cdf15a4cb114c548bf632110bdf40466149cee485bc4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.1 MB (306135447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a71e4fc8335e45a0fdc4e2fd0bc252ec524ee1bff2104a7816ac6cd7cb794b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:30 GMT
ADD file:a6a1df499d0d5b07fb366d776a11c42ddee6261e2425a921041b38e868192770 in / 
# Wed, 01 Mar 2023 02:20:30 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:01:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 03:06:37 GMT
COPY dir:a1bd99c3d82513db94430c73467e1e5c69ea4624d0489571d594afe503e15dc5 in /opt/java/openjdk 
# Wed, 01 Mar 2023 03:06:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 03:06:41 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Mar 2023 03:06:41 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Mar 2023 03:06:41 GMT
WORKDIR /tmp
# Wed, 01 Mar 2023 03:06:46 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Mar 2023 03:06:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Mar 2023 03:06:46 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Mar 2023 03:07:04 GMT
RUN boot
# Wed, 01 Mar 2023 03:07:04 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 01 Mar 2023 03:07:04 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 01 Mar 2023 03:07:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0f5fe16b1836feccd4765ac5685fc7a7b9c73445cac94fc595d2ffbc3cb59a7a`  
		Last Modified: Wed, 01 Mar 2023 02:23:53 GMT  
		Size: 53.7 MB (53703215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c097dd772364568afdeb11bfacd1919beea269a0a3d0b0f445e90ba4644f1775`  
		Last Modified: Wed, 01 Mar 2023 03:17:19 GMT  
		Size: 191.3 MB (191260437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a24d4ed866cfd7225aa8154bdc517a3b758b9590daeffac17949f16375e98b7f`  
		Last Modified: Wed, 01 Mar 2023 03:17:08 GMT  
		Size: 2.4 MB (2350996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc0f6210329b5e7f95e68a7da489bf1b132965e3c8a0f8c8d6b89a7f842eb21`  
		Last Modified: Wed, 01 Mar 2023 03:17:11 GMT  
		Size: 58.8 MB (58820399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bba8e3de6a82d421b96af37c4bbf29be56df24d73dec5abe8e95026e9205e46`  
		Last Modified: Wed, 01 Mar 2023 03:17:08 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
