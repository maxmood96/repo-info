## `openjdk:17-oraclelinux7`

```console
$ docker pull openjdk@sha256:83205aa1f32365bd0e9c289996f4c2185e49307df347ca13774f37e1ddc2fbf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:17-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:b54f383da0321661d0f4c608d09bca06af7cd3a54794cbcd03af933ea8673500
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.3 MB (249274311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63663eedf043d30ca28a0b5fc374aadd49ff189d227865690e846af68e1ef96`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Mar 2021 00:21:32 GMT
ADD file:837f2bca2cab135736ad43644356710dcac6516fdfc2023d239d157d1fa4ba7c in / 
# Wed, 17 Mar 2021 00:21:32 GMT
CMD ["/bin/bash"]
# Wed, 17 Mar 2021 00:38:33 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 17 Mar 2021 00:38:33 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Wed, 17 Mar 2021 00:38:34 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Mar 2021 00:38:34 GMT
ENV LANG=en_US.UTF-8
# Fri, 19 Mar 2021 18:24:27 GMT
ENV JAVA_VERSION=17-ea+14
# Fri, 19 Mar 2021 18:24:36 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/14/GPL/openjdk-17-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='d4bfd596e0b4f3eefb416719a5b6ad98ab3f37f27855573e7c94526a4ffad7d2'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/14/GPL/openjdk-17-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='16646d2498690f98b44f196e74da8361ef05155038a04cb6f62fbb76df08e72f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 19 Mar 2021 18:24:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:401a42e1eb4fe87d89990847d6ef97767b5ac57457c8001203ee2ea137736907`  
		Last Modified: Wed, 17 Mar 2021 00:22:34 GMT  
		Size: 48.3 MB (48263709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f752366003eed4ac964ebb4be3453e3f19d854828f4f50ff708900bb4c42924`  
		Last Modified: Wed, 17 Mar 2021 00:45:21 GMT  
		Size: 15.4 MB (15429957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5684dcb07adadce18cd060619072868b609ff82d26f9829031e3d184b6611c2b`  
		Last Modified: Fri, 19 Mar 2021 18:30:42 GMT  
		Size: 185.6 MB (185580645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:17-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0e70e9245b3682f51258848c81efc799f131c23903f682aaa14a36d213f1f92e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.0 MB (247007674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3708a65dd4e1f0847472e7636697a9879e796ee362a00f93481d578485dffd1e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Mar 2021 03:42:09 GMT
ADD file:035a776cfbed0261290447a1f521123f230f599d8a9ede7feb4616146e47fe10 in / 
# Wed, 17 Mar 2021 03:42:13 GMT
CMD ["/bin/bash"]
# Wed, 17 Mar 2021 04:00:37 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 17 Mar 2021 04:00:38 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Wed, 17 Mar 2021 04:00:39 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Mar 2021 04:00:39 GMT
ENV LANG=en_US.UTF-8
# Wed, 17 Mar 2021 04:00:40 GMT
ENV JAVA_VERSION=17-ea+13
# Wed, 17 Mar 2021 04:01:36 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/13/GPL/openjdk-17-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='1567d8227f5bfc1d742772d5557ceb13bd962ced4b87cd9ec0b4b82bb9b1024e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/13/GPL/openjdk-17-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='5b7dfa002613c0fd39da1fa373308061428949290e91411be09cdd3a2216ee19'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 17 Mar 2021 04:01:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d8ef6a6bcc7f4a961a86d5d1f004e51937aa0e6caf0086b892501d0f909ac044`  
		Last Modified: Wed, 17 Mar 2021 03:43:17 GMT  
		Size: 48.9 MB (48853748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4aee6eb11d4d9526fe0e54fda7fb88ac928a854d7984a42bda3cb37c97b5bf0`  
		Last Modified: Wed, 17 Mar 2021 04:07:44 GMT  
		Size: 16.5 MB (16465148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1aac63b594ef3941ba06eb675cd80d289ba960befb38ec07be1e2a71a0c1fa8`  
		Last Modified: Wed, 17 Mar 2021 04:08:05 GMT  
		Size: 181.7 MB (181688778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
