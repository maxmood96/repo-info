## `openjdk:16-ea-17-oraclelinux7`

```console
$ docker pull openjdk@sha256:e41c3ac418f086ef64de6a87cd0b1dc8382e5f832afb089389096789fdd6db69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm64 variant v8

### `openjdk:16-ea-17-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:191df61017a7fbb2901b5a41c4d5a32ceaa66cba35df65713851ba6770b875c2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240601161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893cc206cab7f406a6e381512097baf783a7d62252dd4c688de5799fba0c39a8`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Sep 2020 20:41:36 GMT
LABEL org.opencontainers.image.authors=Oracle Linux Product Team <ol-ovm-info_ww@oracle.com> org.opencontainers.image.url=https://github.com/oracle/container-images org.opencontainers.image.source=https://github.com/oracle/container-images/tree/dist-arm64v8/7-slim org.opencontainers.image.vendor=Oracle America, Inc org.opencontainers.image.title=Oracle Linux 7 (slim) org.opencontainers.image.description=Oracle Linux is an open-source       operating system available under the GNU General Public License (GPLv2) and       is suitable for both general purpose or Oracle workloads.
# Tue, 15 Sep 2020 20:41:43 GMT
ADD file:f07cad218c7e24e1cbce662268da25d9318627f636feebb0f669155354c7f365 in / 
# Tue, 15 Sep 2020 20:41:44 GMT
CMD ["/bin/bash"]
# Tue, 15 Sep 2020 21:00:40 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 15 Sep 2020 21:00:49 GMT
ENV LANG=en_US.UTF-8
# Tue, 15 Sep 2020 21:00:52 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Tue, 15 Sep 2020 21:00:53 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Sep 2020 20:52:56 GMT
ENV JAVA_VERSION=16-ea+17
# Fri, 25 Sep 2020 20:53:20 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/17/GPL/openjdk-16-ea+17_linux-aarch64_bin.tar.gz; 			downloadSha256=e7005f023a943945defa57440bc7207cfb5f97b7ce4a0f054542948631c53cb6; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/17/GPL/openjdk-16-ea+17_linux-x64_bin.tar.gz; 			downloadSha256=b7244f2059e486aabb071dcf1be5185d86a1a723cc213d6b44551a4973d5e54f; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 25 Sep 2020 20:53:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f5053e285643065e9638a069d53c6f62fd6bf1d6d4d16001d48a66ee024d7397`  
		Last Modified: Fri, 17 Jul 2020 01:45:56 GMT  
		Size: 48.6 MB (48633508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891c11a7b021d2684a0bbcbc93b7f9b3a89839303cdf3e7ff528cf95eeb11ed6`  
		Last Modified: Tue, 15 Sep 2020 21:05:28 GMT  
		Size: 16.4 MB (16442444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2676c539f406004cf73180779a81320f467088b419063d69509e7c43e271806f`  
		Last Modified: Fri, 25 Sep 2020 20:57:44 GMT  
		Size: 175.5 MB (175525209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
