## `clojure:temurin-17-boot-bookworm`

```console
$ docker pull clojure@sha256:5876357f722456dcdccf5ec9d6822d9bb827e7ad1459b271828a25f6dcdc7ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:2cb735f46f14c96cab4842da43479974cb434a64d0a65ecf2038d8f6fa47c26f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.8 MB (258793189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494e96fda932957837a550823cb93a30a0a48e168da3615a9bbe150f5d1e8eea`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 12 Mar 2024 01:20:46 GMT
ADD file:b18b4c32dd8042f45097997c732dc29b3917fd7d5f337f9e772eee5875fbe6f1 in / 
# Tue, 12 Mar 2024 01:20:46 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:10:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 Mar 2024 06:22:32 GMT
COPY dir:3be96ae7faea81e90455993c99b71c9b45986c7e71f70fc577ab97699c92b508 in /opt/java/openjdk 
# Tue, 12 Mar 2024 06:22:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 06:22:34 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 12 Mar 2024 06:22:34 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 12 Mar 2024 06:22:34 GMT
WORKDIR /tmp
# Tue, 12 Mar 2024 06:22:40 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 12 Mar 2024 06:22:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 Mar 2024 06:22:40 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 12 Mar 2024 06:22:57 GMT
RUN boot
# Tue, 12 Mar 2024 06:22:57 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 12 Mar 2024 06:22:58 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 12 Mar 2024 06:22:58 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:71215d55680cf0ab2dcc0e1dd65ed76414e3fb0c294249b5b9319a8fa7c398e4`  
		Last Modified: Tue, 12 Mar 2024 01:25:15 GMT  
		Size: 49.6 MB (49552196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d3e1168edecb607a9a702240c3146bfcd248cb8e0072ed8f1b9a687c433b12`  
		Last Modified: Tue, 12 Mar 2024 06:40:32 GMT  
		Size: 144.9 MB (144893222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c71b16f8ef22c180aa88327b6f7befbb04fd7c092722e6f21f151f8a211a2d`  
		Last Modified: Tue, 12 Mar 2024 06:40:22 GMT  
		Size: 5.5 MB (5527094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d110a26195558d30494299553c710cd936a3763f26d6b753404a9c91ddfc36aa`  
		Last Modified: Tue, 12 Mar 2024 06:40:24 GMT  
		Size: 58.8 MB (58820277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d29dc15b36d066e9fd429068f4bb5dccb958f0ae04dca03da03765e9c0bafab`  
		Last Modified: Tue, 12 Mar 2024 06:40:21 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3f66d3e663f447a7e044d0870fd57b0c28e1ee0599623994a36fbce382a943a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.5 MB (257482013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f507b200859c499e240d4e22606b28cb4d6c6d72c0ecad9e0549e290b483a61`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:26 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Tue, 12 Mar 2024 00:45:27 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:42:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 Mar 2024 01:53:22 GMT
COPY dir:4a8c697909e89d854b955537d3c80fbcec33336dd00fb9805f3c0a9edf3861db in /opt/java/openjdk 
# Tue, 12 Mar 2024 01:53:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 01:53:26 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 12 Mar 2024 01:53:26 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 12 Mar 2024 01:53:26 GMT
WORKDIR /tmp
# Tue, 12 Mar 2024 01:53:31 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 12 Mar 2024 01:53:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 12 Mar 2024 01:53:31 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 12 Mar 2024 01:53:48 GMT
RUN boot
# Tue, 12 Mar 2024 01:53:48 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Tue, 12 Mar 2024 01:53:48 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 12 Mar 2024 01:53:48 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443552151656ad6d5da787f634193a1ca51b30410c526ec21a27bae6141632c0`  
		Last Modified: Tue, 12 Mar 2024 02:08:44 GMT  
		Size: 143.7 MB (143720910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac2b542e43fcf8b62c6a8eb2d54988656a7ca6a2253bb22848271f726595504`  
		Last Modified: Tue, 12 Mar 2024 02:08:36 GMT  
		Size: 5.3 MB (5349353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe30cb4a5695278748b7b3e28760e999d5640566e108df88e2aa0f0684decc30`  
		Last Modified: Tue, 12 Mar 2024 02:08:38 GMT  
		Size: 58.8 MB (58820367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e03d561c3cd30cb8d169adca8a1fe718080331b0adc33f42620fda871a3d1dc`  
		Last Modified: Tue, 12 Mar 2024 02:08:34 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
