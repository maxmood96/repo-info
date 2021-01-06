## `openjdk:17-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:abba29770764a98b9d79338d98f03f1c21660b5e0ed1f305a9213f4ed3bc7697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:17-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:1e5fa99980a7bc778c2293216b8f468a0688cbe296a992c5b26903e6b9eb51c2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.6 MB (249596953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0a49e894760dca02f2086fc2440079c3f57b6624033d1aac18f0909aaf690b`
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
# Wed, 06 Jan 2021 20:41:03 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Wed, 06 Jan 2021 20:41:03 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Jan 2021 20:41:04 GMT
ENV JAVA_VERSION=17-ea+3
# Wed, 06 Jan 2021 20:41:16 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk17/3/GPL/openjdk-17-ea+3_linux-aarch64_bin.tar.gz; 			downloadSha256=eacf61fc385681aa56993d5a326acbdb2d40658fb741a7c5b45b002f335262ad; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk17/3/GPL/openjdk-17-ea+3_linux-x64_bin.tar.gz; 			downloadSha256=fa2562dcc7bf374fc91c01dc722032147ea7553f961a250f8ae7348e6091dabc; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 06 Jan 2021 20:41:16 GMT
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
	-	`sha256:0640e10b112035ca18317b91eef93d04bb7b75995b7effbe029bd045dcd6d456`  
		Last Modified: Wed, 06 Jan 2021 20:48:08 GMT  
		Size: 185.9 MB (185904592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:17-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:99d68606f8a6a3610cbcd4fa08ff8f9bf5982b3231f1e15509ca64f5e8823296
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.6 MB (245597725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d2a428b9a731e3070a31009b587c75aece8d8b468e2f32db6a8300fb5255650`
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
# Wed, 06 Jan 2021 21:06:16 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Wed, 06 Jan 2021 21:06:17 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 06 Jan 2021 21:06:17 GMT
ENV JAVA_VERSION=17-ea+3
# Wed, 06 Jan 2021 21:06:42 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk17/3/GPL/openjdk-17-ea+3_linux-aarch64_bin.tar.gz; 			downloadSha256=eacf61fc385681aa56993d5a326acbdb2d40658fb741a7c5b45b002f335262ad; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk17/3/GPL/openjdk-17-ea+3_linux-x64_bin.tar.gz; 			downloadSha256=fa2562dcc7bf374fc91c01dc722032147ea7553f961a250f8ae7348e6091dabc; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 06 Jan 2021 21:06:44 GMT
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
	-	`sha256:b2ef8d791d2bca5360b816d20743629b601c40da5d975534fd0d4bf783fe6b13`  
		Last Modified: Wed, 06 Jan 2021 21:14:54 GMT  
		Size: 180.3 MB (180268678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
