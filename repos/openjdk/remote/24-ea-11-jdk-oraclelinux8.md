## `openjdk:24-ea-11-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:169ef17d19a314826ad45d50f399245dc850fe72cc71abdae192b81c02034099
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:24-ea-11-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:9a4a420c2f6edc0c7901fd863eb74361092e5375ed343335859acc9f6df8d799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278482101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b04f95b01c491c18cf16fb1d6c253cb06c4ee910d2e0a9b2bf5f23c1ecf0fd`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 15 Aug 2024 00:20:50 GMT
ADD file:f88a328d16b39a012900e14f6463799b448cd9796472d5fb3c58c2cc5ebdee21 in / 
# Thu, 15 Aug 2024 00:20:50 GMT
CMD ["/bin/bash"]
# Fri, 16 Aug 2024 18:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 16 Aug 2024 18:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 16 Aug 2024 18:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Aug 2024 18:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 16 Aug 2024 18:48:14 GMT
ENV JAVA_VERSION=24-ea+11
# Fri, 16 Aug 2024 18:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/11/GPL/openjdk-24-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='c8cc4f7709c86eca1eb249323b8502416afffc54ddffc85278182dc222b1dcd8'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/11/GPL/openjdk-24-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='cd79e2e9877e5f8efa2324bc78851af99fbd9dc936c41c7c07ba928efd889c21'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 16 Aug 2024 18:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:964443381b57e80f40937734e7dfea9e93836abe517bd3e9e9c0fc9f21af4ee5`  
		Last Modified: Thu, 15 Aug 2024 00:21:56 GMT  
		Size: 51.2 MB (51221701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e06d02e0827282431e78f77c137c0e8ed7449a03e32f18c3a3d75a3655638e0`  
		Last Modified: Fri, 16 Aug 2024 21:58:31 GMT  
		Size: 15.0 MB (15036152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d069f5a45e4d27d7e1676aff2e69a36bde6f23d60089d33c48211c08c0b2c1b`  
		Last Modified: Fri, 16 Aug 2024 21:58:34 GMT  
		Size: 212.2 MB (212224248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-11-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:466851f0e4e5b7f8c961517cc8dcfd820d5526a9b17f5bce7d0be1266ea99984
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c24823c996f2deb957f43c13ef3c88107aeb0e3f4e2976e655ff088cecb315a4`

```dockerfile
```

-	Layers:
	-	`sha256:06c818da187f9d36462ec49041f966d7a78f2d8f4344e1b5e32760e8909ace2d`  
		Last Modified: Fri, 16 Aug 2024 21:58:31 GMT  
		Size: 2.3 MB (2287841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e80cc9e453cea437006a9f708455098000c7fc397d661764f07779c6d4d07fa5`  
		Last Modified: Fri, 16 Aug 2024 21:58:31 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json
