## `openjdk:26-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:3419b1575dae9ecfb67f419deb0df93054e775257b0f3f6a04e7536b59c7b21f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:8b4021b21c7eb96596014bf9f9642e29a8f39deae5317d0177dc314cabbce68e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.1 MB (290109955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f512e5fb2e58072de5510ec9c66a83edb03e8880f0b4bf4a0c469fe02bedc461`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Aug 2025 17:11:12 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:11:12 GMT
CMD ["/bin/bash"]
# Sat, 20 Sep 2025 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 20 Sep 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 20 Sep 2025 00:48:11 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Sep 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 20 Sep 2025 00:48:11 GMT
ENV JAVA_VERSION=26-ea+16
# Sat, 20 Sep 2025 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/16/GPL/openjdk-26-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='87ee3d9cfd07f66858b6e519b07d2f23375fb1c1827faeebce6580c31045879f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/16/GPL/openjdk-26-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='116ea44265700afbfe2c15b751ef9e34921fa449663ac0dfb439adef9db9c379'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 20 Sep 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:418b242146d9b70c8138d90f461fca3714547f241d0bdfe50227cc23e442cc96`  
		Last Modified: Thu, 21 Aug 2025 18:55:10 GMT  
		Size: 51.3 MB (51323563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcfa415510bc9e6599c7773fc93a95c3d73dbe0a81f3cd1f8e5e9a34f42be662`  
		Last Modified: Mon, 22 Sep 2025 23:43:12 GMT  
		Size: 15.0 MB (14979263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d14344a86df5a7ed49ce2baa7669b17f02031db823cefdd946fbb0092726c9b`  
		Last Modified: Tue, 23 Sep 2025 00:36:10 GMT  
		Size: 223.8 MB (223807129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:17d62cfb01f2f3ed4d5df992514edd6ea1373022c9acb6c577f76624b8dba21a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407bf93f099af6c143f9b6ac7fb18c89b2fc4b411a44893ef2fa9cd9ce7f3b08`

```dockerfile
```

-	Layers:
	-	`sha256:880251b821f86d808f9c2de7804a7ab6d812cb44d3cc206339e85c6172e2873f`  
		Last Modified: Tue, 23 Sep 2025 00:24:03 GMT  
		Size: 2.5 MB (2451099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0fcfb3f948bf4be63ea42c269446fe826cb30ab20f3f1440966f4111d79d27c`  
		Last Modified: Tue, 23 Sep 2025 00:24:04 GMT  
		Size: 16.0 KB (16038 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:4bc8fb854382ddb1138c8999ff7fa3e506f9fb64aaacef9e247bd440ca3f20dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.4 MB (287387689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c7a18784f5c738539b9e30e667775bca99fa4df9bf7752c3d62b68933b0c043`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Aug 2025 17:12:13 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Aug 2025 17:12:13 GMT
CMD ["/bin/bash"]
# Sat, 20 Sep 2025 00:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 20 Sep 2025 00:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Sat, 20 Sep 2025 00:48:11 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Sep 2025 00:48:11 GMT
ENV LANG=C.UTF-8
# Sat, 20 Sep 2025 00:48:11 GMT
ENV JAVA_VERSION=26-ea+16
# Sat, 20 Sep 2025 00:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/16/GPL/openjdk-26-ea+16_linux-x64_bin.tar.gz'; 			downloadSha256='87ee3d9cfd07f66858b6e519b07d2f23375fb1c1827faeebce6580c31045879f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/16/GPL/openjdk-26-ea+16_linux-aarch64_bin.tar.gz'; 			downloadSha256='116ea44265700afbfe2c15b751ef9e34921fa449663ac0dfb439adef9db9c379'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 20 Sep 2025 00:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9866c68be293aa81b529074549b7f38395dba71a8ea8fc528f721fbf8543b957`  
		Last Modified: Thu, 21 Aug 2025 18:57:24 GMT  
		Size: 50.0 MB (50039817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d6ffbeca758959bd05da246368369d65da94dd2a368bd77cde8aca54865c51`  
		Last Modified: Mon, 22 Sep 2025 22:12:03 GMT  
		Size: 15.7 MB (15672251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e00b6acf428ec14a30d803e26659aa92d78daabaa700a9da41b9166eb9889e1`  
		Last Modified: Mon, 22 Sep 2025 23:13:35 GMT  
		Size: 221.7 MB (221675621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:c3a07f1599500a6bc60adeacdc516b5260be61ec2bb0d909a57f8d1f0626333c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e4d9ec496c1aed69ef64e112d337cb750ac88989569340e4eff96e1715f4b4a`

```dockerfile
```

-	Layers:
	-	`sha256:8d9633cfc351873b9ac05b6d22d1b45814105dd27984492e1be7841aff4aa894`  
		Last Modified: Tue, 23 Sep 2025 00:24:08 GMT  
		Size: 2.4 MB (2449933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa68a0ac00720676b9079edf03eec14ab35068eea083b265bbf9e78f59ce6160`  
		Last Modified: Tue, 23 Sep 2025 00:24:09 GMT  
		Size: 16.2 KB (16181 bytes)  
		MIME: application/vnd.in-toto+json
