## `openjdk:17-ea-3-oraclelinux7`

```console
$ docker pull openjdk@sha256:c6069c922ecce207dda61718c020fb80ad3e9e84eb5feaeb64e647855f0513f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:17-ea-3-oraclelinux7` - linux; amd64

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

### `openjdk:17-ea-3-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:dc36899fe1c6daa63db7dcb83c190622e974388a2f334bd4160e0e572686dcd7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.6 MB (245618453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa9d9adc8b789f1c85c9d4990d2513d5f8b11538c4e622c96717313bb9bc5e4`
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
# Mon, 28 Dec 2020 20:42:42 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Mon, 28 Dec 2020 20:42:43 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Dec 2020 20:42:44 GMT
ENV JAVA_VERSION=17-ea+3
# Mon, 28 Dec 2020 20:43:35 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk17/3/GPL/openjdk-17-ea+3_linux-aarch64_bin.tar.gz; 			downloadSha256=eacf61fc385681aa56993d5a326acbdb2d40658fb741a7c5b45b002f335262ad; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk17/3/GPL/openjdk-17-ea+3_linux-x64_bin.tar.gz; 			downloadSha256=fa2562dcc7bf374fc91c01dc722032147ea7553f961a250f8ae7348e6091dabc; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 28 Dec 2020 20:43:37 GMT
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
	-	`sha256:929b672a24fe449d3c61aefcf3c3d039473b85d472207ee589c856f99279ef5a`  
		Last Modified: Mon, 28 Dec 2020 20:49:20 GMT  
		Size: 180.3 MB (180268642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
