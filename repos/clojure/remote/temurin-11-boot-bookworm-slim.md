## `clojure:temurin-11-boot-bookworm-slim`

```console
$ docker pull clojure@sha256:59e60a73f9260d1313077051874a778aa5774ed646d396e1cd4091fbe17db972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3d0046e8618a1b4b90d5420595f830c01d31cbfb4e6ef337af2284413489115d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.7 MB (236710803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b96d957d6cb1b7e78de36694bb69dd47d9d6c2b49ac1dc3aa3dd689a2af2c9`
-	Default Command: `["boot","repl"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:52:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jan 2024 04:58:38 GMT
COPY dir:7cbebf37ba11e5c859b49d766118c0899546d922ac426dfa1230f08ebde784dc in /opt/java/openjdk 
# Thu, 11 Jan 2024 04:58:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jan 2024 04:58:39 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 11 Jan 2024 04:58:39 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 11 Jan 2024 04:58:39 GMT
WORKDIR /tmp
# Thu, 11 Jan 2024 04:58:45 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 11 Jan 2024 04:58:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 11 Jan 2024 04:58:46 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 11 Jan 2024 04:59:07 GMT
RUN boot
# Thu, 11 Jan 2024 04:59:07 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7fbe5aa6b4fe7cefda24d4cc70b9d7345aa6d93be5fe42f5f6c5e49702b33a7`  
		Last Modified: Thu, 11 Jan 2024 05:17:59 GMT  
		Size: 145.3 MB (145266341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feb6d326e72f40993d4143b76de85e6086ce1337bc3034c55779483cd4253f8a`  
		Last Modified: Thu, 11 Jan 2024 05:17:48 GMT  
		Size: 3.5 MB (3498051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29bb488c039af9b4a73ef888b402a94b981cdf770f936003218e597bf172193f`  
		Last Modified: Thu, 11 Jan 2024 05:17:51 GMT  
		Size: 58.8 MB (58820490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c020f2206c7b0e32a97fd9d0132acbf3fc372affad33f377530dce6b8baba55e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.3 MB (233301520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f550692f103a8962e323a3d9275763a338be6bbabca24398db6880fd915525`
-	Default Command: `["boot","repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:11 GMT
ADD file:262fd7bf0bc26e5d2a229fba52626e22b8a93beac29733acfc60e716c26e689d in / 
# Tue, 19 Dec 2023 01:41:11 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:54:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 06:59:31 GMT
COPY dir:679954ac595f0d76b401a9a7d1ae039330e7231cb1c29892d5f56a0e84534783 in /opt/java/openjdk 
# Tue, 19 Dec 2023 06:59:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 06:59:35 GMT
ENV BOOT_VERSION=2.8.3
# Tue, 19 Dec 2023 06:59:35 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Tue, 19 Dec 2023 06:59:35 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 06:59:40 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Tue, 19 Dec 2023 06:59:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 19 Dec 2023 06:59:40 GMT
ENV BOOT_AS_ROOT=yes
# Tue, 19 Dec 2023 06:59:56 GMT
RUN boot
# Tue, 19 Dec 2023 06:59:56 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:24e221e92a36ab5b0075dd156b4f2ff095532a9b0927946cf6070bb1bea208b8`  
		Last Modified: Tue, 19 Dec 2023 01:44:38 GMT  
		Size: 29.2 MB (29157269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3caa98fe64b6e771f2487121c32bd24ed3c1efe0b70cd6eba73ff5a9db11b6`  
		Last Modified: Tue, 19 Dec 2023 07:16:03 GMT  
		Size: 142.0 MB (142001823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51dd17915340db71b8388a9b788f875fcff51ae38204fa64804f1dbef7814d57`  
		Last Modified: Tue, 19 Dec 2023 07:15:54 GMT  
		Size: 3.3 MB (3321991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5d7c6012bf97911da4a9a0a64993365bd66dd367871051dd133ac982907fa2`  
		Last Modified: Tue, 19 Dec 2023 07:15:57 GMT  
		Size: 58.8 MB (58820437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
