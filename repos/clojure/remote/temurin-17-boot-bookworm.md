## `clojure:temurin-17-boot-bookworm`

```console
$ docker pull clojure@sha256:3bc2baf2894572e90b7f6282f2058c0e8d4a5d120496baf56038681abed5cb66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:201ff80fe80e40048f019b1c75e1756fcd1a32f03186ef52065491526d831e04
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.8 MB (258783470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee6e94f6288b057756606ad1da72dd490d84adc0290598cab87ed8e8dfa88bd3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:42 GMT
ADD file:077a3156bd8271f26498ae6ac3800e68a42b9277581bc81eea31fec1a123dca5 in / 
# Thu, 11 Jan 2024 02:37:43 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:50:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:03:43 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Thu, 11 Jan 2024 05:03:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 05:03:44 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 11 Jan 2024 05:03:44 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 11 Jan 2024 05:03:45 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 05:03:51 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 11 Jan 2024 05:03:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jan 2024 05:03:51 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 11 Jan 2024 05:04:10 GMT
RUN boot
# Thu, 11 Jan 2024 05:04:11 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 11 Jan 2024 05:04:11 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jan 2024 05:04:11 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1b13d4e1a46e5e969702ec92b7c787c1b6891bff7c21ad378ff6dbc9e751d5d4`  
		Last Modified: Thu, 11 Jan 2024 02:42:04 GMT  
		Size: 49.6 MB (49561490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108338e55df135d6bc601717541883bf916e61c490583967476dc73e4809007f`  
		Last Modified: Thu, 11 Jan 2024 05:21:08 GMT  
		Size: 144.9 MB (144873964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7e4081d92940e3fca5b00e0f1d7256174ddaadf12eef4e9949796bcd4675781`  
		Last Modified: Thu, 11 Jan 2024 05:20:56 GMT  
		Size: 5.5 MB (5527004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065baa300952c92770403cdbd7fd43766f2d5b2a8fa05c21f20c656a2bb8c774`  
		Last Modified: Thu, 11 Jan 2024 05:20:59 GMT  
		Size: 58.8 MB (58820612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe61f6f48cc86dc0405fa9770602e882e7769cbb2b280e9e8ec9b3e0bad8a8d6`  
		Last Modified: Thu, 11 Jan 2024 05:20:56 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b8753dc463c7b9146af0660edd2ad23f2d2d8bdc8cf9e7fc65b324c64102dee2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.4 MB (257443957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10034f3482684bd0b328756f7abd98fb96d04d1905f240145201cf07a4a1ef0a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:33 GMT
ADD file:051a18650d326af1d23e30c93370e647e62f94887ce43b22e1808052bce4f2a6 in / 
# Thu, 11 Jan 2024 02:40:34 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 07:57:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 08:08:49 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Thu, 11 Jan 2024 08:08:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 08:08:53 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 11 Jan 2024 08:08:53 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 11 Jan 2024 08:08:53 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 08:08:58 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 11 Jan 2024 08:08:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jan 2024 08:08:58 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 11 Jan 2024 08:09:15 GMT
RUN boot
# Thu, 11 Jan 2024 08:09:15 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 11 Jan 2024 08:09:16 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jan 2024 08:09:16 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5665c1f9a9e17acd68ae05b2839df402eac34afdd095f8c115f09886d757840c`  
		Last Modified: Thu, 11 Jan 2024 02:43:41 GMT  
		Size: 49.6 MB (49592247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886f8d516d17a08090ec426baf83613cd9f2274bd65007da0965c4bb9ce59484`  
		Last Modified: Thu, 11 Jan 2024 08:23:56 GMT  
		Size: 143.7 MB (143681717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcbe1edc4f62be3d75befef3c40ed6607054c59075843df7899561ab63f45685`  
		Last Modified: Thu, 11 Jan 2024 08:23:47 GMT  
		Size: 5.3 MB (5349219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7928127ab8232032c3e4dfb6096471b62027dd15e23a37ae0874b5d2b3ee6fb8`  
		Last Modified: Thu, 11 Jan 2024 08:23:50 GMT  
		Size: 58.8 MB (58820376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5cb0d260115172577a34ea08f1e62e24546140ac125fdcb4fce4fa35bcd5c8c`  
		Last Modified: Thu, 11 Jan 2024 08:23:46 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
