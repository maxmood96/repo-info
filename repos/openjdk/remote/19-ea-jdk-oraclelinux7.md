## `openjdk:19-ea-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:f3dd34c52bacdb0f67467186294fd02490a582cf44ae26a697323726c025af18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:19-ea-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:afa4eaf2bdebcfefc1abe2e6c0aae47bb7416e8007ee115c650d340ca7eafad6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.8 MB (258802458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba6a676530a2e0e362ca81c69014d1f7dc948497a72b5babbdbda3e416dfef90`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 19 May 2022 18:21:17 GMT
ADD file:60c2a17c0433d95caf7d6bac5520da02174f48bf0c50f6f369b00bf8f9774f82 in / 
# Thu, 19 May 2022 18:21:17 GMT
CMD ["/bin/bash"]
# Thu, 19 May 2022 18:22:53 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 19 May 2022 18:22:54 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Thu, 19 May 2022 18:22:54 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 May 2022 18:22:54 GMT
ENV LANG=en_US.UTF-8
# Mon, 06 Jun 2022 19:44:06 GMT
ENV JAVA_VERSION=19-ea+25
# Mon, 06 Jun 2022 19:44:16 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/25/GPL/openjdk-19-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='f03ae5efd6a8fe2211e9c3e0566289d405193244c67af680e202aa9f44473cb0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/25/GPL/openjdk-19-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='f0c7f51bcf0bcca03127dd1dc7f9b59a88636714ea2bfd0707da665f98011237'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 06 Jun 2022 19:44:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f0182e2fe516824cf8f93b207b7c4b65d05c48db476f53312b17b5cd952bfcc3`  
		Last Modified: Thu, 19 May 2022 18:22:04 GMT  
		Size: 48.8 MB (48757934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf5bd358537747774933b2ee9c613076ddeadddfb40f451054ba3989a4b2a80`  
		Last Modified: Thu, 19 May 2022 18:29:27 GMT  
		Size: 14.2 MB (14244311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96886e436c746baad2edf15b0703bb6597a65b0d17a75aa45eee5c3b9db5f4e3`  
		Last Modified: Mon, 06 Jun 2022 19:51:22 GMT  
		Size: 195.8 MB (195800213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-ea-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:134038684416a658adc87199df3128519b39ae2fa0f6dd64e593617dd6044bcc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.3 MB (259299392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e4e875feb78bdf0038d94e5db8f0aec450dcef76a0b86a791ebca413cc8ed5b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Jun 2022 17:42:45 GMT
ADD file:38edee0c3395726e7b6c49418111c57515fb5158f2d9007df25b1126becbe835 in / 
# Wed, 01 Jun 2022 17:42:45 GMT
CMD ["/bin/bash"]
# Wed, 01 Jun 2022 18:06:10 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Wed, 01 Jun 2022 18:06:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Wed, 01 Jun 2022 18:06:11 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Jun 2022 18:06:12 GMT
ENV LANG=en_US.UTF-8
# Mon, 06 Jun 2022 22:45:36 GMT
ENV JAVA_VERSION=19-ea+25
# Mon, 06 Jun 2022 22:45:53 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/25/GPL/openjdk-19-ea+25_linux-x64_bin.tar.gz'; 			downloadSha256='f03ae5efd6a8fe2211e9c3e0566289d405193244c67af680e202aa9f44473cb0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/25/GPL/openjdk-19-ea+25_linux-aarch64_bin.tar.gz'; 			downloadSha256='f0c7f51bcf0bcca03127dd1dc7f9b59a88636714ea2bfd0707da665f98011237'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 06 Jun 2022 22:45:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f32f2fa821eee2ec9063a1b4319bd010b81853e0530a69451b35606e68be303b`  
		Last Modified: Wed, 01 Jun 2022 17:45:48 GMT  
		Size: 49.3 MB (49342882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7422ac4472668232f731f99e0cfcf6637faa083e23675a9b4fd3259163ebff4`  
		Last Modified: Wed, 01 Jun 2022 18:19:08 GMT  
		Size: 15.3 MB (15264563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0fa6610fbd20e7087f6ffdc63f6436b58fe2887af298dd14d038c9e51e8eb4`  
		Last Modified: Mon, 06 Jun 2022 22:58:38 GMT  
		Size: 194.7 MB (194691947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
