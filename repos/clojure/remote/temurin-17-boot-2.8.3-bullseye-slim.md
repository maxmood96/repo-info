## `clojure:temurin-17-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:731b7a13247e83e5405f07b50609ff775a3626c4b09eabed7b03938474aceae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:42b7ed0a3261327fd9e55c89cd3d1ced47b915885b3f8640843e76a6f1ffba4a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.2 MB (236192238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32ab78859cfa7306d4ce5d4ec65a26ded114897cf199694d3a2ada0625ed237`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:53:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 05:05:25 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Thu, 11 Jan 2024 05:05:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 05:05:27 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 11 Jan 2024 05:05:27 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 11 Jan 2024 05:05:27 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 05:05:32 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 11 Jan 2024 05:05:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jan 2024 05:05:33 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 11 Jan 2024 05:05:52 GMT
RUN boot
# Thu, 11 Jan 2024 05:05:53 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 11 Jan 2024 05:05:53 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jan 2024 05:05:53 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e82fb8ae1d9aa781ed28040189489f538266e8f6b9daab125df3d5b96a8f5c`  
		Last Modified: Thu, 11 Jan 2024 05:22:13 GMT  
		Size: 144.9 MB (144873905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50dfbeec8990bbac2cb741dc563a8091b2267af161a2851bf3ed2578c72f4b4e`  
		Last Modified: Thu, 11 Jan 2024 05:22:01 GMT  
		Size: 1.1 MB (1079449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81a857476d9d82c817e77b59473b5475f755bb1fbd202e854b902d99375ea82a`  
		Last Modified: Thu, 11 Jan 2024 05:22:05 GMT  
		Size: 58.8 MB (58820531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be1b2031d15444a208a509813af3bff715444f6e5eccb90cadb2ecb6e2166fc7`  
		Last Modified: Thu, 11 Jan 2024 05:22:01 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9f08abf5f8b31e2065c0d2a72c8fc66a4bc29fd0261811bd8f9b36157f58db95
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233633538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6614bce0d38fb7e375a96f0e18efce5a893857551a8916d746f5971e79828466`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:21:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 06:21:51 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Thu, 11 Jan 2024 08:10:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 08:10:22 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 11 Jan 2024 08:10:22 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 11 Jan 2024 08:10:22 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 08:10:27 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 11 Jan 2024 08:10:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jan 2024 08:10:27 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 11 Jan 2024 08:10:45 GMT
RUN boot
# Thu, 11 Jan 2024 08:10:45 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 11 Jan 2024 08:10:45 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jan 2024 08:10:45 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8895dc7c6e785e9c7eac944cc80657f666eadf36b4309f2c7cfd8b55d9141251`  
		Last Modified: Thu, 11 Jan 2024 06:24:51 GMT  
		Size: 143.7 MB (143681741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edc729e34ddfa144debe71efe737b27981c6d99a51c1f2c79ff721e8a9b1a5e2`  
		Last Modified: Thu, 11 Jan 2024 08:24:45 GMT  
		Size: 1.1 MB (1066825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c55bcaa446e69b6e089619dfd4695b337ae43d57126b2a1abd9fa6b914e73fe`  
		Last Modified: Thu, 11 Jan 2024 08:24:48 GMT  
		Size: 58.8 MB (58820562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884d0f669063f93e3cd9c4620f4e1599d6e34143b90c29637227895ae79e6864`  
		Last Modified: Thu, 11 Jan 2024 08:24:45 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
