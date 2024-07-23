## `openjdk:24-ea-7-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:ddb4c05dbc0b4f3cb43c3056a84aabba640e3dfad13991a1d9177647dfb603d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-7-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:2dcd2a56db5990767ebad7d0e3cd6174b43421a0725efc9383969a1a3d3b37d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298390686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b836db5a9448e2d444fffcb439c0a7ec33747634cf4b5b62fdb87ba12fda67a9`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
CMD ["/bin/bash"]
# Sat, 20 Jul 2024 00:52:05 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 20 Jul 2024 00:52:05 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Sat, 20 Jul 2024 00:52:05 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 00:52:05 GMT
ENV LANG=C.UTF-8
# Sat, 20 Jul 2024 00:52:05 GMT
ENV JAVA_VERSION=24-ea+7
# Sat, 20 Jul 2024 00:52:05 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/7/GPL/openjdk-24-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='d175c4cfc7ab8306b42cf88fe0e60b2b827a2106c026ae6d2a3f2e51bbcb60d0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/7/GPL/openjdk-24-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='5df46f7b64a38a7a34e1b283f6c37b57f8238567b81c3db0f127f348f4842977'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 20 Jul 2024 00:52:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2920cc2c11af612b622d60cb0efe552bd6ba226ef084ef8060c17399289d7444`  
		Last Modified: Mon, 22 Jul 2024 21:00:06 GMT  
		Size: 37.9 MB (37871931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9a29a9c955047ef4c9646b22e92de51ea17b8c54d6d2c853b342491db359dc`  
		Last Modified: Mon, 22 Jul 2024 21:00:09 GMT  
		Size: 211.5 MB (211525019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-7-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:04c7ca6f50bf7cfc4278ebd857b96731549f864ad4e8003c3f6a265125d3cdde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3377698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68a61438acc4f9ab6efec86712d89c3422594234885843e06609a1757a067eb`

```dockerfile
```

-	Layers:
	-	`sha256:a8bf82b5e8d260d4ca1fc7a06ba5233d304aacf6b96e1af06abfff352a08010c`  
		Last Modified: Mon, 22 Jul 2024 21:00:06 GMT  
		Size: 3.4 MB (3358195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fa193321b0932b134f82eaae2d765278bd321d09b0fd232ad9247878a998df8`  
		Last Modified: Mon, 22 Jul 2024 21:00:05 GMT  
		Size: 19.5 KB (19503 bytes)  
		MIME: application/vnd.in-toto+json
