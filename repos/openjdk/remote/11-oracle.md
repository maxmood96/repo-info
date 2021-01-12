## `openjdk:11-oracle`

```console
$ docker pull openjdk@sha256:f4d835ed0fc2c11ab2d8407fc3691585066a2bb772724e652fe8dcf57dcdc03e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:11-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:0d34f2df26d3e3238d9c05b74836a1577146f6a7c897ad50e4fcfa4c5b658c61
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243127911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:680c5ad86000544d2c36dfad29c715bf33ceebfba962f30458db566f8dfeff8b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Fri, 12 Apr 2019 00:39:30 GMT
ADD file:fc4b1a8a391c3bd11cdd229574a87e8d1133402deff8ef758f932756d5a82ca3 in / 
# Fri, 12 Apr 2019 00:39:30 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2019 01:03:22 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 12 Apr 2019 01:04:54 GMT
ENV JAVA_HOME=/usr/java/openjdk-11
# Fri, 12 Apr 2019 01:04:54 GMT
ENV PATH=/usr/java/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2019 01:04:54 GMT
ENV JAVA_VERSION=11.0.2
# Fri, 12 Apr 2019 01:04:55 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk11/9/GPL/openjdk-11.0.2_linux-x64_bin.tar.gz
# Fri, 12 Apr 2019 01:04:55 GMT
ENV JAVA_SHA256=99be79935354f5c0df1ad293620ea36d13f48ec3ea870c838f20c504c9668b57
# Fri, 12 Apr 2019 01:05:35 GMT
RUN set -eux; 		curl -fL -o /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Fri, 12 Apr 2019 01:05:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:35defbf6c365d4b156baefbecee36d050397bcc4fca7906aada0bbd00e34c76a`  
		Last Modified: Fri, 12 Apr 2019 00:41:39 GMT  
		Size: 42.6 MB (42610008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5362bf1d5ff8c939878cd11387a1f195da87c88b7c73c89b3d933917644c8fe1`  
		Last Modified: Fri, 12 Apr 2019 01:07:10 GMT  
		Size: 6.6 MB (6627887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c125b2a83b9fed99f5b4eb30b914cff23f54ad3f0fb6b63473c2d6f726b0ca`  
		Last Modified: Fri, 12 Apr 2019 01:08:19 GMT  
		Size: 193.9 MB (193890016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:11-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c10c2fc16328ca90a2865226328c8b0b0ef3072b24d186cb7471b75169d4f222
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.4 MB (250392806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c2128413109f90cbfb680ecc69fc25abef29ecefe42dd481904d1df7a62b17f`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Sep 2020 20:40:54 GMT
LABEL org.opencontainers.image.authors=Oracle Linux Product Team <ol-ovm-info_ww@oracle.com> org.opencontainers.image.url=https://github.com/oracle/container-images org.opencontainers.image.source=https://github.com/oracle/container-images/tree/dist-arm64v8/8-slim org.opencontainers.image.vendor=Oracle America, Inc org.opencontainers.image.title=Oracle Linux 8 (slim) org.opencontainers.image.description=Oracle Linux is an open-source       operating system available under the GNU General Public License (GPLv2) and       is suitable for both general purpose or Oracle workloads.
# Wed, 06 Jan 2021 20:45:01 GMT
ADD file:ad2b2ddca8e17229cc8d1380ecda32c4b2c04f1e2aed8f493f745c6352b34e60 in / 
# Wed, 06 Jan 2021 20:45:03 GMT
CMD ["/bin/bash"]
# Wed, 06 Jan 2021 21:04:08 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 06 Jan 2021 21:04:09 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jan 2021 01:04:45 GMT
ENV JAVA_HOME=/usr/java/openjdk-11
# Tue, 12 Jan 2021 01:04:46 GMT
ENV PATH=/usr/java/openjdk-11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jan 2021 01:04:47 GMT
ENV JAVA_VERSION=11.0.9.1
# Tue, 12 Jan 2021 01:05:10 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jdk_aarch64_linux_11.0.9.1_1.tar.gz ;; 		amd64 | i386:x86-64) downloadUrl=https://github.com/AdoptOpenJDK/openjdk11-upstream-binaries/releases/download/jdk-11.0.9.1%2B1/OpenJDK11U-jdk_x64_linux_11.0.9.1_1.tar.gz ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz.asc "$downloadUrl.sign"; 	curl -fL -o openjdk.tgz "$downloadUrl"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys EAC843EBD3EFDB98CC772FADA5CD6035332FA671; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --keyserver-options no-self-sigs-only --recv-keys CA5F11C6CE22644D42C6AC4492EF8D39DC13168F; 	gpg --batch --list-sigs --keyid-format 0xLONG CA5F11C6CE22644D42C6AC4492EF8D39DC13168F 		| tee /dev/stderr 		| grep '0xA5CD6035332FA671' 		| grep 'Andrew Haley'; 	gpg --batch --verify openjdk.tgz.asc openjdk.tgz; 	rm -rf "$GNUPGHOME"; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 			ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		cacertsFile=; for f in "$JAVA_HOME/lib/security/cacerts" "$JAVA_HOME/jre/lib/security/cacerts"; do if [ -e "$f" ]; then cacertsFile="$f"; break; fi; done; 	if [ -z "$cacertsFile" ] || ! [ -f "$cacertsFile" ]; then echo >&2 "error: failed to find cacerts file in $JAVA_HOME"; exit 1; fi; 	rm -rf "$cacertsFile"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$cacertsFile"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 12 Jan 2021 01:05:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d0eecbd2c3e7306adbf5b4a0d9bebc7d266ebe78bda044d35b0994c1cf655a54`  
		Last Modified: Wed, 06 Jan 2021 20:47:00 GMT  
		Size: 42.0 MB (41996293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d959bac04e84615265b829b8f4c62eddad4d65f7aabc8d560ca8430057b054`  
		Last Modified: Wed, 06 Jan 2021 21:13:39 GMT  
		Size: 14.1 MB (14057340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011e2e8973332e8b5741cb72d12be871217e79ebcc04e386f2b91b8ed0836df9`  
		Last Modified: Tue, 12 Jan 2021 01:15:13 GMT  
		Size: 194.3 MB (194339173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
