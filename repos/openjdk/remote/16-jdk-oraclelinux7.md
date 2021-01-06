## `openjdk:16-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:1e1c4b61eed450360935ef30e4a828a0baf2e6d6319d6a69db09817a90d923f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:16-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:39c45ef72fac5bad08de5155d2ba2a312fd231ad7f4b4c6b4972fa11611bd252
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.5 MB (248540314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3def70d11bc8e2dba65c8eb0d7b8498be9e5acba073e3c7d69e1c1d6b621c461`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Sep 2020 21:23:41 GMT
LABEL org.opencontainers.image.authors=Oracle Linux Product Team <ol-ovm-info_ww@oracle.com> org.opencontainers.image.url=https://github.com/oracle/container-images org.opencontainers.image.source=https://github.com/oracle/container-images/tree/dist-amd64/7-slim org.opencontainers.image.vendor=Oracle America, Inc org.opencontainers.image.title=Oracle Linux 7 (slim) org.opencontainers.image.description=Oracle Linux is an open-source       operating system available under the GNU General Public License (GPLv2) and       is suitable for both general purpose or Oracle workloads.
# Wed, 06 Jan 2021 20:22:16 GMT
ADD file:dee09ad1ed4e7359b14fabc84890b1fb687ad4efe75f7c4800c0a907fd4f70a3 in / 
# Wed, 06 Jan 2021 20:22:16 GMT
CMD ["/bin/bash"]
# Wed, 06 Jan 2021 20:41:03 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 06 Jan 2021 20:41:03 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Jan 2021 20:42:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Wed, 06 Jan 2021 20:42:13 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Jan 2021 20:42:13 GMT
ENV JAVA_VERSION=16-ea+30
# Wed, 06 Jan 2021 20:42:25 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/30/GPL/openjdk-16-ea+30_linux-aarch64_bin.tar.gz; 			downloadSha256=82cc271dfc10530a176b89f20ad2bcbc9733b78f39e3997ac54132956ce53ff1; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/30/GPL/openjdk-16-ea+30_linux-x64_bin.tar.gz; 			downloadSha256=01ef449013825308ac144c91fbbbadd9562b084d6e17cd8d428a088386707556; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 06 Jan 2021 20:42:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:980316e412373040bc280150078ae453b259ece36b750a0a9b6f4c99751ce4f9`  
		Last Modified: Wed, 06 Jan 2021 20:24:02 GMT  
		Size: 48.3 MB (48260808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:344a44c175048c7ccd1f6f0be52b7945e1a34a79995fb5de5737026d0474ebfe`  
		Last Modified: Wed, 06 Jan 2021 20:47:51 GMT  
		Size: 15.4 MB (15431553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c479076fe7c5ae53162e23fbf2b60de86e34a3d6240282976566f41b8f866fd`  
		Last Modified: Wed, 06 Jan 2021 20:49:15 GMT  
		Size: 184.8 MB (184847953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:16-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:7e43327b8fdc4c930a8f58dbcab0d654a8b47fa1dc645dc8217cde5356f54bab
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244559981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5597fdd2e857fe4507535458ef5b229df4934f7a65bf22d3f7d4dbfdcfb9b43e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Sep 2020 20:41:36 GMT
LABEL org.opencontainers.image.authors=Oracle Linux Product Team <ol-ovm-info_ww@oracle.com> org.opencontainers.image.url=https://github.com/oracle/container-images org.opencontainers.image.source=https://github.com/oracle/container-images/tree/dist-arm64v8/7-slim org.opencontainers.image.vendor=Oracle America, Inc org.opencontainers.image.title=Oracle Linux 7 (slim) org.opencontainers.image.description=Oracle Linux is an open-source       operating system available under the GNU General Public License (GPLv2) and       is suitable for both general purpose or Oracle workloads.
# Tue, 22 Dec 2020 17:40:57 GMT
ADD file:ec95b4619b5e5fc03a6ad9b5ae466fc891abf449e7dbde03283ce3a9885f238e in / 
# Tue, 22 Dec 2020 17:41:01 GMT
CMD ["/bin/bash"]
# Tue, 22 Dec 2020 17:58:47 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 22 Dec 2020 17:58:48 GMT
ENV LANG=en_US.UTF-8
# Tue, 22 Dec 2020 17:58:49 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Tue, 22 Dec 2020 17:58:49 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Dec 2020 18:46:00 GMT
ENV JAVA_VERSION=16-ea+30
# Mon, 28 Dec 2020 18:46:22 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/30/GPL/openjdk-16-ea+30_linux-aarch64_bin.tar.gz; 			downloadSha256=82cc271dfc10530a176b89f20ad2bcbc9733b78f39e3997ac54132956ce53ff1; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/30/GPL/openjdk-16-ea+30_linux-x64_bin.tar.gz; 			downloadSha256=01ef449013825308ac144c91fbbbadd9562b084d6e17cd8d428a088386707556; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 28 Dec 2020 18:46:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2fa5b4561d489d4ba037541bc1400de45a1aad2d6e7197b8bfa0999af4c62266`  
		Last Modified: Tue, 22 Dec 2020 17:42:05 GMT  
		Size: 48.9 MB (48867329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f4fbf760ea337587e3374187a1443f6bf6d20437e76dcacf8de2747a34e1a2`  
		Last Modified: Tue, 22 Dec 2020 18:04:33 GMT  
		Size: 16.5 MB (16482482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ae5664b5befcd5313ee6da8237f207d1999812a6c389e916e0da5eef349560`  
		Last Modified: Mon, 28 Dec 2020 18:51:08 GMT  
		Size: 179.2 MB (179210170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
