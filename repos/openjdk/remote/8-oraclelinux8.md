## `openjdk:8-oraclelinux8`

```console
$ docker pull openjdk@sha256:ecb2d5a5e5340039b72d9197a2c5a3735017e3f4b349971e17ed299f2f854042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:8-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:ac7dba3e653292f34eb780d3550ba91a2601392c72ca51e7d01443d4e9fdb98a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161123577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f88add7679c282a13fcad48772cc4baa23ad15b7e7a7fd7880c81814475e1ef`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Sep 2020 21:22:07 GMT
LABEL org.opencontainers.image.authors=Oracle Linux Product Team <ol-ovm-info_ww@oracle.com> org.opencontainers.image.url=https://github.com/oracle/container-images org.opencontainers.image.source=https://github.com/oracle/container-images/tree/dist-amd64/8-slim org.opencontainers.image.vendor=Oracle America, Inc org.opencontainers.image.title=Oracle Linux 8 (slim) org.opencontainers.image.description=Oracle Linux is an open-source       operating system available under the GNU General Public License (GPLv2) and       is suitable for both general purpose or Oracle workloads.
# Wed, 06 Jan 2021 20:21:43 GMT
ADD file:2987f8143a9c4f758731c17e307a6c7ca9e5e1a974df3405a17d2699da7d8351 in / 
# Wed, 06 Jan 2021 20:21:44 GMT
CMD ["/bin/bash"]
# Wed, 06 Jan 2021 20:39:53 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 06 Jan 2021 20:39:53 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jan 2021 10:59:31 GMT
ENV JAVA_HOME=/usr/java/openjdk-8
# Tue, 12 Jan 2021 10:59:31 GMT
ENV PATH=/usr/java/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jan 2021 10:59:31 GMT
ENV JAVA_VERSION=8u275
# Tue, 12 Jan 2021 10:59:41 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_x64_linux_8u275b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 	curl -fL -o openjdk.tgz "$downloadUrl"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done; 	if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi; 	rm -rf "$cacertsFile"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$cacertsFile"; 		javac -version; 	java -version
```

-	Layers:
	-	`sha256:a73adebe9317092fb1f120a1d0d21f460296e9bde7ac683fd452cfc628c528cf`  
		Last Modified: Wed, 06 Jan 2021 20:23:26 GMT  
		Size: 42.1 MB (42069921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01539a440662c3eb557891fa6a645060175a11221504049aa1b23cd50cc3f6fa`  
		Last Modified: Wed, 06 Jan 2021 20:47:24 GMT  
		Size: 13.3 MB (13277651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5708549e5317343b0d55f01f362ebb33f5a0b81ef8e96149a22b879af89cc74`  
		Last Modified: Tue, 12 Jan 2021 11:16:53 GMT  
		Size: 105.8 MB (105776005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
