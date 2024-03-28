## `clojure:temurin-11-boot-2.8.3-bookworm`

```console
$ docker pull clojure@sha256:b68c47dc53fc8708f8b0662c44c57d14d359a8b76cd3a08b4340bd3910b29158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-2.8.3-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:7485919eb62c34fa27885bae89f960a5b3b776a0d486f7eb5811784e8790b945
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259171057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:335d30357bb7a4e67c316ceaa098d752bc7aeeb24ef088d204db4f5e16a95e1b`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 12 Mar 2024 01:20:46 GMT
ADD file:b18b4c32dd8042f45097997c732dc29b3917fd7d5f337f9e772eee5875fbe6f1 in / 
# Tue, 12 Mar 2024 01:20:46 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:10:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 02:58:02 GMT
COPY dir:4cef005a87cd4606dd69ccb04c755a46f4aa2c925fb1aacc59928d64687208f2 in /opt/java/openjdk 
# Thu, 28 Mar 2024 02:58:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 02:58:03 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 28 Mar 2024 02:58:03 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 02:58:03 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 02:58:10 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 28 Mar 2024 02:58:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 02:58:11 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 28 Mar 2024 02:58:28 GMT
RUN boot
# Thu, 28 Mar 2024 02:58:29 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:71215d55680cf0ab2dcc0e1dd65ed76414e3fb0c294249b5b9319a8fa7c398e4`  
		Last Modified: Tue, 12 Mar 2024 01:25:15 GMT  
		Size: 49.6 MB (49552196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a875645a27e3ccc8bfba72105d6bf6ac46ec1c8cbe99056efaa0a86db4bfd0f4`  
		Last Modified: Thu, 28 Mar 2024 03:19:12 GMT  
		Size: 145.3 MB (145271224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6a712a96523e79128ef947c0a81bb33094151265d6bf7de3004b0b1b097b3e`  
		Last Modified: Thu, 28 Mar 2024 03:19:01 GMT  
		Size: 5.5 MB (5527292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c735002800da07948f46c65b6ecb85d68ec2f857ad9517a1c3a8cc7da5a4fc74`  
		Last Modified: Thu, 28 Mar 2024 03:19:04 GMT  
		Size: 58.8 MB (58820345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-2.8.3-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:99072b796f91004c17996f91ce661ecfd70457d0d425c258ecaa9d319863bea2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255767353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7d4febc406c257651abca20d804d1b39490acff785727685f13e53fbb74961`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:26 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Tue, 12 Mar 2024 00:45:27 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:42:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 02:32:13 GMT
COPY dir:d5fb8d9a38dea7496f2aff176bc9a34bbca80551c2dc57109d2dae5907a339ee in /opt/java/openjdk 
# Thu, 28 Mar 2024 02:32:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 02:32:17 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 28 Mar 2024 02:32:17 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 28 Mar 2024 02:32:17 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 02:32:23 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 28 Mar 2024 02:32:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 28 Mar 2024 02:32:23 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 28 Mar 2024 02:32:40 GMT
RUN boot
# Thu, 28 Mar 2024 02:32:40 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095e0c8804330303f34a1bc5a23f03e613b1984ea526d87d9d7910e9b5449ef4`  
		Last Modified: Thu, 28 Mar 2024 02:49:26 GMT  
		Size: 142.0 MB (142006296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989b70d0c121909480066090a7a70f81b5569b07138eef9cce30cd88bed8da87`  
		Last Modified: Thu, 28 Mar 2024 02:49:18 GMT  
		Size: 5.3 MB (5349602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bc592020320ef772e9d130e2df63d5c0ed4f2a07fec388276b1eba5e98ba26`  
		Last Modified: Thu, 28 Mar 2024 02:49:20 GMT  
		Size: 58.8 MB (58820471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
