## `openjdk:23-ea-18-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:ad5d8c3958e1befa52e9b3c65b16c0158c42856e314a0e0d2cdcd23cfc546cf9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:23-ea-18-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:a59a82f89505bb4c2e7204c92ce5eb7a01d0a1bf894d7cfa7931cce3219cea02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.6 MB (297568684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55545a2bc6941f3c94e2b34afc79d78fab694ea665e4bb94937aee93101ac7e6`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 08 Mar 2024 19:21:04 GMT
ADD file:9bcef05fa351e2fb72a4b6052a0252eeaa2cff794ed089a482670c67961d2e90 in / 
# Fri, 08 Mar 2024 19:21:04 GMT
CMD ["/bin/bash"]
# Fri, 12 Apr 2024 18:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 12 Apr 2024 18:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 12 Apr 2024 18:48:10 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Apr 2024 18:48:10 GMT
ENV LANG=C.UTF-8
# Fri, 12 Apr 2024 18:48:10 GMT
ENV JAVA_VERSION=23-ea+18
# Fri, 12 Apr 2024 18:48:10 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/18/GPL/openjdk-23-ea+18_linux-x64_bin.tar.gz'; 			downloadSha256='618c320c28c4d2d71fd5a366876b5f9ef8cf16819e9793e7d960ecea1caf9d5d'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/18/GPL/openjdk-23-ea+18_linux-aarch64_bin.tar.gz'; 			downloadSha256='aecde065716b2226217e12905a714da37b06daca526e77821a55d09eab1b5489'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 12 Apr 2024 18:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:972029ff9873af36c6c0fcee05b14acbc57a61ecd0b8bf86b167bdf46f973823`  
		Last Modified: Fri, 08 Mar 2024 19:22:31 GMT  
		Size: 49.0 MB (48978454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c8fb48c63a569481e807a25c94b1d8783ee334e33e8770a345b1f8e3057bc7`  
		Last Modified: Mon, 15 Apr 2024 17:50:57 GMT  
		Size: 37.7 MB (37737439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c1a1eba528b372d129eb51da1f1055384d7e84bf29d707abc7c2aaa0f2b7e1`  
		Last Modified: Mon, 15 Apr 2024 17:51:04 GMT  
		Size: 210.9 MB (210852791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-18-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:cada8d0f0037b3699d545c8426ecc341dbefbeddb3c79500f88fd07589fb2945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3349427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212af066051ef1f4e7bec64bfcf12610e1eeea5407de54cd413e575121821a27`

```dockerfile
```

-	Layers:
	-	`sha256:1b07959307129c73fa60f7e8ce699cf214a7e39e6d12b7a8ee8ad6e9868f8038`  
		Last Modified: Mon, 15 Apr 2024 17:50:56 GMT  
		Size: 3.3 MB (3329538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db158c0e86dbae96543a0ac258e879eb24be25ff467a3d4f04d4e989b27d5dcf`  
		Last Modified: Mon, 15 Apr 2024 17:50:56 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.in-toto+json
