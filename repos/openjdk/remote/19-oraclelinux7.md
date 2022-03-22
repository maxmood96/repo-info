## `openjdk:19-oraclelinux7`

```console
$ docker pull openjdk@sha256:1b3f05e3633167ff3a7255cbac54bfc765ba4fcc6392eadcb1321c1b308463ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:b3ce69f1487c9611de02663286cb53234016c6b850a656dc697d2676eafcb108
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256053158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f9be5445010c69e2386d666623be19ea7af669e2a5fecc35b64db1256342fef`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 18 Mar 2022 23:22:25 GMT
ADD file:19ae95221a518b3855b98aeb91f6c13f250d6caa59ee16bf155d73f7f5cdcc41 in / 
# Fri, 18 Mar 2022 23:22:26 GMT
CMD ["/bin/bash"]
# Sat, 19 Mar 2022 10:18:15 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Sat, 19 Mar 2022 10:18:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Sat, 19 Mar 2022 10:18:15 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 10:18:16 GMT
ENV LANG=en_US.UTF-8
# Tue, 22 Mar 2022 01:23:55 GMT
ENV JAVA_VERSION=19-ea+14
# Tue, 22 Mar 2022 01:24:05 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/14/GPL/openjdk-19-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='7c64317f728ce251b1fa6fcc612bbc5e4fac4d2862cf0f9b9edd98800072b6bc'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/14/GPL/openjdk-19-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='166aaa023baf2fff6484465efd16040557b4bbd57362409d730acec5d01fe749'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 22 Mar 2022 01:24:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fb9cda09c679c7a8d70feb22223b7546c2d4d46d555312571fa2e3cc65347d9b`  
		Last Modified: Fri, 18 Mar 2022 23:23:20 GMT  
		Size: 48.7 MB (48745506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f858fe6b2907e344c8421154471dfeff5be2cb6510210efa614c5d1eacf06d25`  
		Last Modified: Sat, 19 Mar 2022 10:35:39 GMT  
		Size: 14.2 MB (14218591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea0c225f3708d967a214d07cd3d2fc058721550578c432680cb24fce1788afa4`  
		Last Modified: Tue, 22 Mar 2022 01:31:51 GMT  
		Size: 193.1 MB (193089061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a4316fbca41c1b4337adcc45f182d3f56750423851de179978630e8b3d6b78e7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.7 MB (256738234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f6e37959d69eaaf1f4d4e4a4795a9012376baff2f1a38a355308917ad71cf52`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 19 Mar 2022 01:00:51 GMT
ADD file:a5f18f088f362b979701dd9843b784391fd01ee9f85e19b4a66089ccba650d8a in / 
# Sat, 19 Mar 2022 01:00:51 GMT
CMD ["/bin/bash"]
# Sat, 19 Mar 2022 07:23:15 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Sat, 19 Mar 2022 07:23:16 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Sat, 19 Mar 2022 07:23:17 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 19 Mar 2022 07:23:18 GMT
ENV LANG=en_US.UTF-8
# Tue, 22 Mar 2022 10:03:05 GMT
ENV JAVA_VERSION=19-ea+14
# Tue, 22 Mar 2022 10:03:22 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/14/GPL/openjdk-19-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='7c64317f728ce251b1fa6fcc612bbc5e4fac4d2862cf0f9b9edd98800072b6bc'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/14/GPL/openjdk-19-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='166aaa023baf2fff6484465efd16040557b4bbd57362409d730acec5d01fe749'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 22 Mar 2022 10:03:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:141b1a23f5c914f6ea3d33bbb54ee6e46d83e342a4f16e079f825362e6db5a24`  
		Last Modified: Sat, 19 Mar 2022 01:01:46 GMT  
		Size: 49.3 MB (49339592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdcf257e8020deec6d6f5ad76b9c36d1eca4b42e96527feb4c52735766f320b7`  
		Last Modified: Sat, 19 Mar 2022 07:44:40 GMT  
		Size: 15.3 MB (15278942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8194db90aa4df0527629bff3cac4abd5239d57e2f3484cd31babcd79a4595b8e`  
		Last Modified: Tue, 22 Mar 2022 10:17:16 GMT  
		Size: 192.1 MB (192119700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
