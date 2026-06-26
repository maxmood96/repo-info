## `openjdk:28-ea-jdk-oracle`

```console
$ docker pull openjdk@sha256:f485904ebd4cc0f850122aa6d861e1c7b8afc286adb70a34d0b2303f22861845
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:28-ea-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:37180c9fbdb053aacf7c7f343d4c26a4f40c0fa9932a658918613b30556efb80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308187586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f458263639edf737252edc99385ef41c86854a940fc46e10a17c86267dd43e76`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:08 GMT
ADD oraclelinux-10-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:08 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:49:34 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 26 Jun 2026 17:49:44 GMT
ENV JAVA_HOME=/usr/java/openjdk-28
# Fri, 26 Jun 2026 17:49:44 GMT
ENV PATH=/usr/java/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jun 2026 17:49:44 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jun 2026 17:49:44 GMT
ENV JAVA_VERSION=28-ea+4
# Fri, 26 Jun 2026 17:49:44 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/4/GPL/openjdk-28-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='3f349a9ae39761069b8132f7ba529bec7bf6c759376f77cb57520d3f21d4fa23'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/4/GPL/openjdk-28-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='a49e869b72df691c734d29e133fd15ae49bed271913327704c9bca6c2132525d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jun 2026 17:49:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ded2aa0abafd1e1e93e05338cb1b14916dbeb283d3862aa21e5d8b0164f4cbf3`  
		Last Modified: Tue, 12 May 2026 18:44:20 GMT  
		Size: 43.1 MB (43080582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f33c2767f1258249fd3138c95a77cdf445ec500d0b72cdf0ec80865c4307258`  
		Last Modified: Fri, 26 Jun 2026 17:50:08 GMT  
		Size: 37.7 MB (37687216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922b47249f9035226eaeb47c8f23353dad870b8f258d8fe217299c1277f452dc`  
		Last Modified: Fri, 26 Jun 2026 17:50:11 GMT  
		Size: 227.4 MB (227419788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:9ac06dd12ba203fc9513dd276f5f19e86fc8a89c018702e5f0837a86b2c10de3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6ad553a6b1455917b09f8a54b14472f710b59f795457ae77b4018eb7fa02a8`

```dockerfile
```

-	Layers:
	-	`sha256:c48b4d392f2b43f1a0cc64be9478bf21cc7390a589aecbd38ee7cd58b11fa80a`  
		Last Modified: Fri, 26 Jun 2026 17:50:05 GMT  
		Size: 2.4 MB (2366446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82f3fed06784e3bf0c2264af1dd9f66e81b4f786cadfbd11810112f3b078b33d`  
		Last Modified: Fri, 26 Jun 2026 17:50:05 GMT  
		Size: 17.8 KB (17829 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:28-ea-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:a89069ac1e79f38f26139c356f4ff8630d71e48a4c75d023f1beba157ceabe91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.6 MB (304644295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55d06178dce04af775c7155ae93f2119124284c6a58e39b3199e155285d5a69`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:43:55 GMT
ADD oraclelinux-10-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:43:55 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:54:35 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 26 Jun 2026 17:54:47 GMT
ENV JAVA_HOME=/usr/java/openjdk-28
# Fri, 26 Jun 2026 17:54:47 GMT
ENV PATH=/usr/java/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jun 2026 17:54:47 GMT
ENV LANG=C.UTF-8
# Fri, 26 Jun 2026 17:54:47 GMT
ENV JAVA_VERSION=28-ea+4
# Fri, 26 Jun 2026 17:54:47 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/4/GPL/openjdk-28-ea+4_linux-x64_bin.tar.gz'; 			downloadSha256='3f349a9ae39761069b8132f7ba529bec7bf6c759376f77cb57520d3f21d4fa23'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/4/GPL/openjdk-28-ea+4_linux-aarch64_bin.tar.gz'; 			downloadSha256='a49e869b72df691c734d29e133fd15ae49bed271913327704c9bca6c2132525d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jun 2026 17:54:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:523b5fcd95921b1880258a8c56e30985e8f3adf21d143bf177907dc76d6a562b`  
		Last Modified: Tue, 12 May 2026 18:44:06 GMT  
		Size: 41.5 MB (41495695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6874a711555de5763ac0a1baf87290916d7b912ed089634e4042b6e9aa672b6`  
		Last Modified: Fri, 26 Jun 2026 17:55:10 GMT  
		Size: 37.7 MB (37695940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd72f79b37847e8a9f4c0dc38f246594dc4020e19bb20cc4c972b19fd81804aa`  
		Last Modified: Fri, 26 Jun 2026 17:55:14 GMT  
		Size: 225.5 MB (225452660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:13da6a2631ca0165f301f8b397bc5e2f673a31890c4d66ee3746bb5974aaeb70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab83a7011a582d9db3e5005ee630b2b477b299844a7503420779bde1c3c25963`

```dockerfile
```

-	Layers:
	-	`sha256:23cd1a91e1fa5d076c719946feb0b94b86c9e1e2aa311d9e4e580f71edb0e8c8`  
		Last Modified: Fri, 26 Jun 2026 17:55:09 GMT  
		Size: 2.4 MB (2365974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bf953469b994e9f78be82cbc40fc4a24e7e514b4cd64b9cd534549a7108a86f`  
		Last Modified: Fri, 26 Jun 2026 17:55:08 GMT  
		Size: 18.0 KB (18044 bytes)  
		MIME: application/vnd.in-toto+json
