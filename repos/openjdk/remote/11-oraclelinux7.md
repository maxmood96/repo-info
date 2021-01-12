## `openjdk:11-oraclelinux7`

```console
$ docker pull openjdk@sha256:c57cc480f36996e61ef33147b44fc615865685852a5a184b1bac551a6dc60a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:11-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:2f66f76928d4332d2f180b08867b3eecc2eca6129bfabdb0d2d872409c49a337
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.4 MB (260429789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c2e4bbb6a069c9e655b5e762df14fff28f08901904daff1704ed0b003fea28`
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
# Tue, 12 Jan 2021 10:57:20 GMT
ENV JAVA_HOME=/usr/java/openjdk-11
# Tue, 12 Jan 2021 10:57:20 GMT
ENV PATH=/usr/java/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jan 2021 10:57:21 GMT
ENV JAVA_VERSION=11.0.9.1
# Tue, 12 Jan 2021 10:57:37 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jdk_aarch64_linux_11.0.9.1_1.tar.gz ;; 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jdk_x64_linux_11.0.9.1_1.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 	curl -fL -o openjdk.tgz "$downloadUrl"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done; 	if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi; 	rm -rf "$cacertsFile"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$cacertsFile"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 12 Jan 2021 10:57:37 GMT
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
	-	`sha256:97b56716498daf1af5c7c0a76edffef4384d3dfbc9de445b15c896db7c840081`  
		Last Modified: Tue, 12 Jan 2021 11:13:48 GMT  
		Size: 196.7 MB (196737428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:11-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e191e22e39268c85a490ab5817f237d908f034625afa628790b1c87485d6744c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.7 MB (259670273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff793430501ec95be2b0b8ea5efe5345aee80c6324c5dd81ab6e83c82050fb3a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Sep 2020 20:41:36 GMT
LABEL org.opencontainers.image.authors=Oracle Linux Product Team <ol-ovm-info_ww@oracle.com> org.opencontainers.image.url=https://github.com/oracle/container-images org.opencontainers.image.source=https://github.com/oracle/container-images/tree/dist-arm64v8/7-slim org.opencontainers.image.vendor=Oracle America, Inc org.opencontainers.image.title=Oracle Linux 7 (slim) org.opencontainers.image.description=Oracle Linux is an open-source       operating system available under the GNU General Public License (GPLv2) and       is suitable for both general purpose or Oracle workloads.
# Wed, 06 Jan 2021 20:45:46 GMT
ADD file:d4d5ffcc8d57e27f8de10063c4e347d2f4da299f62166d6f6387a7714f5e0f06 in / 
# Wed, 06 Jan 2021 20:45:48 GMT
CMD ["/bin/bash"]
# Wed, 06 Jan 2021 21:06:15 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 06 Jan 2021 21:06:16 GMT
ENV LANG=en_US.UTF-8
# Tue, 12 Jan 2021 01:05:22 GMT
ENV JAVA_HOME=/usr/java/openjdk-11
# Tue, 12 Jan 2021 01:05:22 GMT
ENV PATH=/usr/java/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jan 2021 01:05:23 GMT
ENV JAVA_VERSION=11.0.9.1
# Tue, 12 Jan 2021 01:05:49 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jdk_aarch64_linux_11.0.9.1_1.tar.gz ;; 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jdk_x64_linux_11.0.9.1_1.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 	curl -fL -o openjdk.tgz "$downloadUrl"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done; 	if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi; 	rm -rf "$cacertsFile"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$cacertsFile"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 12 Jan 2021 01:05:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e2e87614faabf530f11811ae8eb1be9e586d5d923036268129a39eae319cb772`  
		Last Modified: Wed, 06 Jan 2021 20:47:54 GMT  
		Size: 48.9 MB (48858154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141908ad8b1f3520523867010d20883b59e3c504867fad3ab621d90a951a0a31`  
		Last Modified: Wed, 06 Jan 2021 21:14:34 GMT  
		Size: 16.5 MB (16470893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d58b78826316c58df57aa43481e536962e7dafdfec0c3f22e3bbb75badd432`  
		Last Modified: Tue, 12 Jan 2021 01:16:17 GMT  
		Size: 194.3 MB (194341226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
