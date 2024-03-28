## `clojure:temurin-17-boot-bookworm`

```console
$ docker pull clojure@sha256:69e8f2c5f5435654764f46c362ce89b7e60d2d2fff7fb4a0cc8cae852e6a83ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:7c644d7721eb25e77683f1b14aa290767f137223b9469a2e72f750b74522d8b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.8 MB (258793420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2247cd328b5831a339b5f3e3c3f5d4b3d72a10632588950cd5274eb37d87ae8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 12 Mar 2024 01:20:46 GMT
ADD file:b18b4c32dd8042f45097997c732dc29b3917fd7d5f337f9e772eee5875fbe6f1 in / 
# Tue, 12 Mar 2024 01:20:46 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:10:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 03:06:12 GMT
COPY dir:88c5118aff6896f6ed535dcde576d68ef88ded459cca013e0f9beb3e430ebb52 in /opt/java/openjdk 
# Thu, 28 Mar 2024 03:06:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 03:06:13 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 28 Mar 2024 03:06:13 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 03:06:13 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 03:06:20 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 28 Mar 2024 03:06:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 03:06:20 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 28 Mar 2024 03:06:37 GMT
RUN boot
# Thu, 28 Mar 2024 03:06:37 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 28 Mar 2024 03:06:37 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 28 Mar 2024 03:06:38 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:71215d55680cf0ab2dcc0e1dd65ed76414e3fb0c294249b5b9319a8fa7c398e4`  
		Last Modified: Tue, 12 Mar 2024 01:25:15 GMT  
		Size: 49.6 MB (49552196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd1d09ff668169a35ad1340a1e6c8ef47bc12ff42bb04e3501d7f507ad781a6`  
		Last Modified: Thu, 28 Mar 2024 03:24:17 GMT  
		Size: 144.9 MB (144893081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1619b5072313d2ea977227bf813f52c9cd057235def0bea81e05309afcc1045b`  
		Last Modified: Thu, 28 Mar 2024 03:24:07 GMT  
		Size: 5.5 MB (5527200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd2f05fbe986b148682a23d9df853619b0d673597e62d50b325bdb921e1b4ad`  
		Last Modified: Thu, 28 Mar 2024 03:24:09 GMT  
		Size: 58.8 MB (58820543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e2bfc1f8d32369c178df9b0750143042756b5ac3551ad58a4e9eae27e4a4d5`  
		Last Modified: Thu, 28 Mar 2024 03:24:06 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:293fdf8a1e027aadf9a184378950fa93fb39c58e87e5c5f5c632eb8b0c20e787
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.5 MB (257482194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ac420286867ba39ebe36b3b89d18c699a38596d05b74c69fe73bc3269ac3c25`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:26 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Tue, 12 Mar 2024 00:45:27 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:42:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 02:38:59 GMT
COPY dir:a5d0039514ccd79689a0ea6094d70ca92113e8cbcc38d473b7c0fcc04a1f496a in /opt/java/openjdk 
# Thu, 28 Mar 2024 02:39:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 02:39:02 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 28 Mar 2024 02:39:02 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 02:39:03 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 02:39:08 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 28 Mar 2024 02:39:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 02:39:08 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 28 Mar 2024 02:39:24 GMT
RUN boot
# Thu, 28 Mar 2024 02:39:24 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 28 Mar 2024 02:39:24 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 28 Mar 2024 02:39:24 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a3ab6309e95d793e36791ae047faf4e012dfe9d2c539164c9626d54ab9fced`  
		Last Modified: Thu, 28 Mar 2024 02:53:43 GMT  
		Size: 143.7 MB (143720940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b38a881d4b92f787ffb69c7932420f3f1a2bfbf186a0333e6e9a490c0de0d32`  
		Last Modified: Thu, 28 Mar 2024 02:53:35 GMT  
		Size: 5.3 MB (5349510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07835845127372b3a72e32cc2bf2d3208bc3ef42463854e17cb7aa4cc05c61c`  
		Last Modified: Thu, 28 Mar 2024 02:53:36 GMT  
		Size: 58.8 MB (58820361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7f410300d23ca6da15884ec1369dfcf09571c95b3a58249c9508815dfe6c53`  
		Last Modified: Thu, 28 Mar 2024 02:53:34 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
