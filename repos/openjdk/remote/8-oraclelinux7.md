## `openjdk:8-oraclelinux7`

```console
$ docker pull openjdk@sha256:1fae6a3adb2a4de048d98efffecb153086ae0594541c53591afa5f14cbb5a056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:8-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:b0fee178d3465a328c7fea78ccb601bdd2be827cda9e118101c66d9699bb9e5a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169468565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:756e4a1684fb8694d873135038cb0a0c2491af2927a3a1b19c39d9d8119579b9`
-	Default Command: `["\/bin\/bash"]`

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
# Tue, 12 Jan 2021 10:59:46 GMT
ENV JAVA_HOME=/usr/java/openjdk-8
# Tue, 12 Jan 2021 10:59:46 GMT
ENV PATH=/usr/java/openjdk-8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jan 2021 10:59:47 GMT
ENV JAVA_VERSION=8u275
# Tue, 12 Jan 2021 10:59:56 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk8-upstream-binaries/releases/download/jdk8u275-b01/OpenJDK8U-jdk_x64_linux_8u275b01.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 	curl -fL -o openjdk.tgz "$downloadUrl"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done; 	if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi; 	rm -rf "$cacertsFile"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$cacertsFile"; 		javac -version; 	java -version
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
	-	`sha256:d15f09d5d05a2e0ec2575b7266c335168634c7878b25935f433bfa05f4c78c81`  
		Last Modified: Tue, 12 Jan 2021 11:17:35 GMT  
		Size: 105.8 MB (105776204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
