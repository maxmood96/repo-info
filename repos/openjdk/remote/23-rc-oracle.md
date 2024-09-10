## `openjdk:23-rc-oracle`

```console
$ docker pull openjdk@sha256:5db92784b4a0ae3ad4828298952d44c6a636b2a519283a19052262d0d909fc8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-rc-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:79b3709d6cbf229121678d03417b3b43462f0ce9acd617bedf19091068ad90ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.9 MB (300933262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fae20072d2a12db20f634ae5afd5f7617a68ea594d6c852d22fd962804099eb`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 21 Aug 2024 18:48:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
CMD ["/bin/bash"]
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Wed, 21 Aug 2024 18:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Aug 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_VERSION=23
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-x64_bin.tar.gz'; 			downloadSha256='08fea92724127c6fa0f2e5ea0b07ff4951ccb1e2f22db3c21eebbd7347152a67'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-aarch64_bin.tar.gz'; 			downloadSha256='076dcf7078cdf941951587bf92733abacf489a6570f1df97ee35945ffebec5b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5e407bf3af905fb1f6edf271f870052697e79b018f921119921615cd25365fdb`  
		Last Modified: Tue, 10 Sep 2024 01:02:42 GMT  
		Size: 49.2 MB (49239252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c1ea9e315646607184654c85696fc0269f0c99b2067585f1dc26e206a13230`  
		Last Modified: Tue, 10 Sep 2024 01:54:58 GMT  
		Size: 40.4 MB (40418005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdea025156ce54480a983c8a9ad7b91e8c6002863e9219f9e73f21478e0fd2d6`  
		Last Modified: Tue, 10 Sep 2024 01:55:02 GMT  
		Size: 211.3 MB (211276005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-rc-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:f82c3e9451a4dce4db6ac50e39738eee20b98178c0cb39b378c821abf1d8f7f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3686407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14faf4928d334231a9a509865bafa6010862fbc61273d34f6b7496328c39228a`

```dockerfile
```

-	Layers:
	-	`sha256:38403cf5d344931a65db5fa2c3b5b98beeb7b2c25210470973a7e6007d305dbd`  
		Last Modified: Tue, 10 Sep 2024 01:54:57 GMT  
		Size: 3.7 MB (3668559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d69e32f25d55ec253015bbb9ef55cd4fa057bac05c397ad813180a3182a9307`  
		Last Modified: Tue, 10 Sep 2024 01:54:57 GMT  
		Size: 17.8 KB (17848 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-rc-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:88d2adffde7c89904076f544cb06c5b2d9dca70f4ee8f85ead86cf63ef916fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296553666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5da917fd321b4106301e27f12f9141e858c7279364f2922bd9e3ebdf5742bf`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 21 Aug 2024 18:48:11 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Wed, 21 Aug 2024 18:48:11 GMT
CMD ["/bin/bash"]
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Wed, 21 Aug 2024 18:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Aug 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Wed, 21 Aug 2024 18:48:11 GMT
ENV JAVA_VERSION=23
# Wed, 21 Aug 2024 18:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-x64_bin.tar.gz'; 			downloadSha256='08fea92724127c6fa0f2e5ea0b07ff4951ccb1e2f22db3c21eebbd7347152a67'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/37/GPL/openjdk-23_linux-aarch64_bin.tar.gz'; 			downloadSha256='076dcf7078cdf941951587bf92733abacf489a6570f1df97ee35945ffebec5b7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 21 Aug 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd1b36cd87201413a78d843fcfb1218c857939c3962a8c46b1f8126a2336f87`  
		Last Modified: Fri, 23 Aug 2024 01:54:37 GMT  
		Size: 39.5 MB (39496829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043c1ae1df4c4ca2e4cd88f272ab37539ddb6f0a031d82cf4c896c99aa710e9a`  
		Last Modified: Fri, 23 Aug 2024 01:57:00 GMT  
		Size: 209.2 MB (209169046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-rc-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:427340032311635f9382d5597f0c56ac3846cfdc531a0772c202a5fb849faff1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3658689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1294b2e55b461b5ab7d53dc3c5ab7467b17cfde0ab1ab79ac938eeefe9cad5d6`

```dockerfile
```

-	Layers:
	-	`sha256:d26addc2f56cb570984de1bcd08ea4c7ef405c0af88f45e7b5e2abe9b3f2102b`  
		Last Modified: Fri, 23 Aug 2024 01:56:55 GMT  
		Size: 3.6 MB (3640622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f3bb64954b9d5f1bb6a2f257a6c3240c2856132824e3e88b9fbe4eec82859c6`  
		Last Modified: Fri, 23 Aug 2024 01:56:55 GMT  
		Size: 18.1 KB (18067 bytes)  
		MIME: application/vnd.in-toto+json
