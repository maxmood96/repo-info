## `openjdk:23-oraclelinux9`

```console
$ docker pull openjdk@sha256:9a6c1f6ef7ca75397ce89d11b953a9dc5bde5ff9caad159463a6f40bc6928ad5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-oraclelinux9` - linux; amd64

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

### `openjdk:23-oraclelinux9` - unknown; unknown

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

### `openjdk:23-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9c7eba130249fa6d19a0b7505f20f88e00f7863b0b4aef05f52a2da1ea89f3e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 MB (297927301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b37c977c525bd5d2a8b9e70466202fd26c162867d28b6f1390bdba9851739dfe`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 21 Aug 2024 18:48:11 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
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
	-	`sha256:ed6a7145c00ee1c4b91b6b37765e2a7addef2d9b96e12546b2f7aad0a198ae3f`  
		Last Modified: Tue, 10 Sep 2024 05:32:56 GMT  
		Size: 47.9 MB (47913808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb8c247ecf1b88686d212c2f55e0f5ac4d4ba8cde9b5d6f216ca338a07e7b87`  
		Last Modified: Tue, 10 Sep 2024 06:43:07 GMT  
		Size: 40.8 MB (40844369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabeb64a81a518f6c45c47b2d4cf89a152dd5787c7b606789c2113c9d3601040`  
		Last Modified: Tue, 10 Sep 2024 06:45:32 GMT  
		Size: 209.2 MB (209169124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:a93d6611d55dedd71249c55b82ad8cadc6d514e026c501a99877d609369b7879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3685198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c3cc4db004bcb9173cf6b96766580bce86778aa4bb5073597108b3b84ee7e58`

```dockerfile
```

-	Layers:
	-	`sha256:1cae743d2642c91b5d59475c3b6a2730ddcecbf4e2122eef2b8ff9531d727704`  
		Last Modified: Tue, 10 Sep 2024 06:45:28 GMT  
		Size: 3.7 MB (3666870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:156e9be1e9d8fff0e29d6b91297027fc49557268e77ce14bbf3ce48c7ab8a9ff`  
		Last Modified: Tue, 10 Sep 2024 06:45:27 GMT  
		Size: 18.3 KB (18328 bytes)  
		MIME: application/vnd.in-toto+json
