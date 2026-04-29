## `openjdk:27-ea-19-jdk-oraclelinux10`

```console
$ docker pull openjdk@sha256:0b31ad0b494bc0edc97c767f49cca0065e050b732e35ce765aec3405cee51142
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-19-jdk-oraclelinux10` - linux; amd64

```console
$ docker pull openjdk@sha256:4de51f5b03000847bfe50d0c0a9c503ce7693de68c1f676a6e54842062cc66a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.2 MB (309177213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1272652ca88e9cdb7eaa943f92b1f726cb81a100e9406791bbd1a00a825c4ae5`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:51 GMT
ADD oraclelinux-10-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:51 GMT
CMD ["/bin/bash"]
# Tue, 28 Apr 2026 23:34:34 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 28 Apr 2026 23:34:42 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 28 Apr 2026 23:34:42 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 23:34:42 GMT
ENV LANG=C.UTF-8
# Tue, 28 Apr 2026 23:34:42 GMT
ENV JAVA_VERSION=27-ea+19
# Tue, 28 Apr 2026 23:34:42 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/19/GPL/openjdk-27-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='97a3527cdc677e8205e755bd56b8931a8e3461c1bdd7fdd564da9b7842bcea0b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/19/GPL/openjdk-27-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='5d6876749a41cfecbcda3332da94d88a9e3097292f0eeafdb6d7fd41f66265c8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 28 Apr 2026 23:34:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:59f98efa373e352e94c44103a934ba322d4b0d08d660faa4e8642d56b03dd4fe`  
		Last Modified: Fri, 17 Apr 2026 23:39:02 GMT  
		Size: 43.1 MB (43074999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4efa39decda6d75716791ead213d78253fa51c9e1d14bdda4e55d68bf5212e`  
		Last Modified: Tue, 28 Apr 2026 23:35:05 GMT  
		Size: 37.7 MB (37678608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f926cd90bdc2740b16f5f23f3047436bc16636124b8cdccd50ee0da74a56d7ae`  
		Last Modified: Tue, 28 Apr 2026 23:35:09 GMT  
		Size: 228.4 MB (228423606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-19-jdk-oraclelinux10` - unknown; unknown

```console
$ docker pull openjdk@sha256:b61e87dc7a1c8b67d4ba1fc418946688f1350b1897f54552320070c801ee69e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ad32202737d169653888ba9e86632aa41c891f1c3b76cceb6d3346203bd51b`

```dockerfile
```

-	Layers:
	-	`sha256:d95a7e0ecfddce322cf0c656c8e29ec961956b2235f66a995d58c42571ff5c22`  
		Last Modified: Tue, 28 Apr 2026 23:35:03 GMT  
		Size: 2.4 MB (2367767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70ff30811de813fef034097882b48114170d97cb71242896fa23ca41ea34841a`  
		Last Modified: Tue, 28 Apr 2026 23:35:03 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-19-jdk-oraclelinux10` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:cd3714498e2e3cc3be9c490a9902bf5be0bc95af19914b4018ad99c33bd27f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.6 MB (305563665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f18ee50e41bbf669b3d6227044109a37670cecf0547838db1718f745e722a00`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 17 Apr 2026 23:38:18 GMT
ADD oraclelinux-10-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 17 Apr 2026 23:38:18 GMT
CMD ["/bin/bash"]
# Tue, 28 Apr 2026 23:35:21 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 28 Apr 2026 23:35:31 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 28 Apr 2026 23:35:31 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 23:35:31 GMT
ENV LANG=C.UTF-8
# Tue, 28 Apr 2026 23:35:31 GMT
ENV JAVA_VERSION=27-ea+19
# Tue, 28 Apr 2026 23:35:31 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/19/GPL/openjdk-27-ea+19_linux-x64_bin.tar.gz'; 			downloadSha256='97a3527cdc677e8205e755bd56b8931a8e3461c1bdd7fdd564da9b7842bcea0b'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/19/GPL/openjdk-27-ea+19_linux-aarch64_bin.tar.gz'; 			downloadSha256='5d6876749a41cfecbcda3332da94d88a9e3097292f0eeafdb6d7fd41f66265c8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 28 Apr 2026 23:35:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b998cd5b08c06e4f5efb16eb3e3a01c0e5c56b8b33a94e55d1a919f120c4e0ab`  
		Last Modified: Fri, 17 Apr 2026 23:38:28 GMT  
		Size: 41.5 MB (41476716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c39126078eea4e991819819920a18f3b3e12ac70a492e41544c0ea0624dc07`  
		Last Modified: Tue, 28 Apr 2026 23:35:54 GMT  
		Size: 37.7 MB (37699082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2692ca652e6177ce50031fce7890e42906da8a04a200c614dc20d04878e74fa`  
		Last Modified: Tue, 28 Apr 2026 23:35:58 GMT  
		Size: 226.4 MB (226387867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-19-jdk-oraclelinux10` - unknown; unknown

```console
$ docker pull openjdk@sha256:3010f377558e6b23c2b77057910ed1a0016252ac92b38ec61fb4bc050d2a55c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fe181417e1cf3eaf7a172efd71622ea0345f9409c8f1890d5cdb62759476634`

```dockerfile
```

-	Layers:
	-	`sha256:45614c4364a67c902724fd89715fabaf47de63d833186bd4f5dc1603a529206b`  
		Last Modified: Tue, 28 Apr 2026 23:35:52 GMT  
		Size: 2.4 MB (2367295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f70efe2498e26e8fbc94bebe96ec8b7627bf50299106ba75ae2631d05411067c`  
		Last Modified: Tue, 28 Apr 2026 23:35:52 GMT  
		Size: 18.1 KB (18065 bytes)  
		MIME: application/vnd.in-toto+json
