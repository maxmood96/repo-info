## `openjdk:24-ea-15-jdk-oracle`

```console
$ docker pull openjdk@sha256:0303f372ee62199124d4ed212fab83cb2a41da792d2d27a5a588e93c32c1d5bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-15-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0afe7650e2f8684027697bf700a88d8b25bbc4a13b2eab4a92847e824ba0369e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.5 MB (298459256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932595dcdca2fa82451b07ef6f6c184472adbc2762a0692d0b8b66978be874fa`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 09 Sep 2024 20:35:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 09 Sep 2024 20:35:51 GMT
CMD ["/bin/bash"]
# Sat, 14 Sep 2024 06:48:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 14 Sep 2024 06:48:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Sat, 14 Sep 2024 06:48:15 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 14 Sep 2024 06:48:15 GMT
ENV LANG=C.UTF-8
# Sat, 14 Sep 2024 06:48:15 GMT
ENV JAVA_VERSION=24-ea+15
# Sat, 14 Sep 2024 06:48:15 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/15/GPL/openjdk-24-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='b41d4867c348d7f1991085d8bcc8797eaf032d9dfaa3419bc9db15eaea75e91e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/15/GPL/openjdk-24-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='165b7c19403e9708ca261cdfe4c385e837df683049203e33ad2bf76228054a25'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 14 Sep 2024 06:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ed6a7145c00ee1c4b91b6b37765e2a7addef2d9b96e12546b2f7aad0a198ae3f`  
		Last Modified: Tue, 10 Sep 2024 05:32:56 GMT  
		Size: 47.9 MB (47913808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1be39ea2d18e49c60b19f004c35d6d158839de1ab591a32c52003cd6b2d1b9`  
		Last Modified: Mon, 16 Sep 2024 19:19:57 GMT  
		Size: 40.8 MB (40844107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ec9a476755f71cee55be483721187d841ffbacd3182c203e191653ab5b1e42`  
		Last Modified: Mon, 16 Sep 2024 19:20:01 GMT  
		Size: 209.7 MB (209701341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-15-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:5b60fe9f7b6229adffc04af0cbd3ba5190da434f78ef5c11d31f454b68f8b12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3689147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c952c44eb24f06febb690fc364f91618199a5f455db3b266b064573fb5fdc501`

```dockerfile
```

-	Layers:
	-	`sha256:71709746f2934aa607286bc77b4576cb86db69b10530ff00c7fdea984a957518`  
		Last Modified: Mon, 16 Sep 2024 19:19:56 GMT  
		Size: 3.7 MB (3668882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b398419c6233f373563ce4516dc49a2e0ad6ea586e2c31c255e3c6e37f366ec2`  
		Last Modified: Mon, 16 Sep 2024 19:19:56 GMT  
		Size: 20.3 KB (20265 bytes)  
		MIME: application/vnd.in-toto+json
