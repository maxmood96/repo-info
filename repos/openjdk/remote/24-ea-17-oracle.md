## `openjdk:24-ea-17-oracle`

```console
$ docker pull openjdk@sha256:2b0cd35ef45ed1878756e78fb99182e3685744fdb1ace8661edca99da6e68f9d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-17-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:56eb57c30267cd68ab05a93dba90c479feb0e6b218de1308fda1266233e8db49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300440862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d385bdc8de8a9f6adf8b3bc2635a65272754b9aa994ea7f433a48f4f68e02d12`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
CMD ["/bin/bash"]
# Fri, 27 Sep 2024 06:48:27 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 27 Sep 2024 06:48:27 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 27 Sep 2024 06:48:27 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 06:48:27 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 06:48:27 GMT
ENV JAVA_VERSION=24-ea+17
# Fri, 27 Sep 2024 06:48:27 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/17/GPL/openjdk-24-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='983faf25eff38b5b396afabd191a91b239a1d803a0dadd01863861ecf731f034'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/17/GPL/openjdk-24-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='c9eb980b4f1fde9c2387e0fab6b91b6f68cb109e3ddd43eda0013d9ee345f2dc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 27 Sep 2024 06:48:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e646149b36fdec6d4c532f77f5500952e677d7fc8a2c95fcd14dd3cff7a17b73`  
		Last Modified: Sat, 28 Sep 2024 01:01:23 GMT  
		Size: 39.1 MB (39058916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28aa30e0b5cb8c9aa59b3a131a3769d0ce37c63c3ff14e27ccb3c45e56038a18`  
		Last Modified: Sat, 28 Sep 2024 01:01:33 GMT  
		Size: 212.1 MB (212135004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-17-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:ec17ab611ca73debf8e1a486fa402f1626e5096dfe64922119b8dfed45ddbf50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3801930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68564f989587a6f464dc499606526ffe249b2f1d34845cba27d1c030418e5dd9`

```dockerfile
```

-	Layers:
	-	`sha256:01d2d6598e90b0ff82780733324343b446f736d38538c91f1a6debb0a268bdbc`  
		Last Modified: Sat, 28 Sep 2024 01:01:22 GMT  
		Size: 3.8 MB (3782218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08ed3425cf352980b12f6102eb48c657c907ac1e379b2106f373d9c4b50cd47c`  
		Last Modified: Sat, 28 Sep 2024 01:01:22 GMT  
		Size: 19.7 KB (19712 bytes)  
		MIME: application/vnd.in-toto+json
