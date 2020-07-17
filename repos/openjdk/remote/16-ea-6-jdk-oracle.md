## `openjdk:16-ea-6-jdk-oracle`

```console
$ docker pull openjdk@sha256:cf8ce4d2b9db3b3cf4323fd7497ddda65ebcd813f5a8d8769c8bba1947af9be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:16-ea-6-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:7e6c1330f4ddd0b0db2d286404f898939d9ec23918e081acd126f440b9d8dd2f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.6 MB (254620951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07986a79f1c3b68e7dba7403f84a7971a8607c325f4bab7a853954e4fb6e387b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Wed, 10 Jun 2020 18:22:32 GMT
ADD file:79bb5b8b89fe54ba99fd9d42d4f8774bfb9c1319ac3ead17a2005a3bde852451 in / 
# Wed, 10 Jun 2020 18:22:32 GMT
CMD ["/bin/bash"]
# Wed, 10 Jun 2020 18:39:27 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 10 Jun 2020 18:39:28 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Jun 2020 20:37:38 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Thu, 18 Jun 2020 20:37:39 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Jul 2020 22:35:28 GMT
ENV JAVA_VERSION=16-ea+6
# Thu, 16 Jul 2020 22:36:07 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/6/GPL/openjdk-16-ea+6_linux-aarch64_bin.tar.gz; 			downloadSha256=c9ecf57bfb0f727ed96419f975d018d8205b83f4db1896801e3c96c9b441cd1d; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/6/GPL/openjdk-16-ea+6_linux-x64_bin.tar.gz; 			downloadSha256=8c4672179d1259e172534b062c562b6f70f56ddc4507db0368b52b1483e28c41; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o /openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java --version; 	javac --version
# Thu, 16 Jul 2020 22:36:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fa926a7d213a8145d6a906d68a085b21909a4b26871f142804e68b322bf8881f`  
		Last Modified: Wed, 10 Jun 2020 18:23:43 GMT  
		Size: 43.5 MB (43457466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22aed8993d2fb0bb3a658c631a1dfbd05c0e5d42218f419d18238996bd06ea08`  
		Last Modified: Wed, 10 Jun 2020 18:42:25 GMT  
		Size: 14.8 MB (14760261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018ac644deed19264ebe173fdf9f16fc9ef14fc988690a933d31242bb627481e`  
		Last Modified: Thu, 16 Jul 2020 22:42:10 GMT  
		Size: 196.4 MB (196403224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:16-ea-6-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:79010fb194979a2fa9d0366311b6fb852a00da9e9730dde9c27e250bb02c7ea2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (234040716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70c554882b10e10f1f9c8e2bee48c9f533d233a2226b87ae87c1e64d27e29326`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 May 2019 21:40:52 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Wed, 10 Jun 2020 18:54:47 GMT
ADD file:64c488ae0df14676929e149538eb50b12e9a99518a126c88ee9704e8a88424e5 in / 
# Wed, 10 Jun 2020 18:54:49 GMT
CMD ["/bin/bash"]
# Wed, 10 Jun 2020 19:12:05 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 10 Jun 2020 19:12:06 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Jun 2020 23:55:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Thu, 18 Jun 2020 23:55:13 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Jul 2020 22:12:46 GMT
ENV JAVA_VERSION=16-ea+6
# Thu, 16 Jul 2020 22:13:35 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/6/GPL/openjdk-16-ea+6_linux-aarch64_bin.tar.gz; 			downloadSha256=c9ecf57bfb0f727ed96419f975d018d8205b83f4db1896801e3c96c9b441cd1d; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/6/GPL/openjdk-16-ea+6_linux-x64_bin.tar.gz; 			downloadSha256=8c4672179d1259e172534b062c562b6f70f56ddc4507db0368b52b1483e28c41; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o /openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java --version; 	javac --version
# Thu, 16 Jul 2020 22:13:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b791ce794f1b8ac779f7e2bb939c8f822209f7507dbc7f70d072d98b700e55a`  
		Last Modified: Wed, 10 Jun 2020 18:55:52 GMT  
		Size: 44.1 MB (44072411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7857b3d293f1062b1c04189b86491b9bbfd2e793fec6975e1bdcabf4ef9ed3`  
		Last Modified: Wed, 10 Jun 2020 19:14:19 GMT  
		Size: 15.0 MB (15012793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9821cfbdec691d8e7b44e2c76f4cd921c7208d7daf4a84101c92ce344fa06ebb`  
		Last Modified: Thu, 16 Jul 2020 22:20:59 GMT  
		Size: 175.0 MB (174955512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
