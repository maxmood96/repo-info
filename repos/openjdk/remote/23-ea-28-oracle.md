## `openjdk:23-ea-28-oracle`

```console
$ docker pull openjdk@sha256:1d2db8e3d5b72839328fdd481a208800c5c4f6c9c22b88efc0ba71b9a65c7ead
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:23-ea-28-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:16be829b4cf4170ca5b2f707786c417ed23a989ed05c9118217a81913ba97c8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.1 MB (298142617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fffb77a5a955b88253b88798abbf4d0d1635fc8555711f1b654680c66895cceb`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 21 Jun 2024 18:48:11 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 18:48:11 GMT
CMD ["/bin/bash"]
# Fri, 21 Jun 2024 18:48:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 21 Jun 2024 18:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 21 Jun 2024 18:48:11 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Jun 2024 18:48:11 GMT
ENV LANG=C.UTF-8
# Fri, 21 Jun 2024 18:48:11 GMT
ENV JAVA_VERSION=23-ea+28
# Fri, 21 Jun 2024 18:48:11 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/28/GPL/openjdk-23-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='55c6ef3457ea9e056119ae7ab55e4691742458d74fbe1a1a7cdb7d08527bee1f'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/28/GPL/openjdk-23-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='9844e3616fd6e16a94212badb2aee65f0a5805b43c587d80e9ae85174f18b984'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 21 Jun 2024 18:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcae7285977df73b8350d3d0da793cbcc242a3b2f55df9c1893cff8a72f3f5d4`  
		Last Modified: Sat, 22 Jun 2024 00:56:04 GMT  
		Size: 37.9 MB (37862509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348bd7f7f93c039716a4e306a73e27d66bfdb99b42c92c76311101733e54caee`  
		Last Modified: Sat, 22 Jun 2024 00:56:05 GMT  
		Size: 211.3 MB (211286455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-28-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:3ec576cdac4df8eba3da71a11525ad524cba092d2782aadd84fcf6666b4a175c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3352772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6e855417a388ac1e62d20f3559f9c05ccab8bff6bac27070a3c28a8c30f8f5`

```dockerfile
```

-	Layers:
	-	`sha256:54c07a240ab06d2ee7b459fcf042d3f6925061fe20ea2ba1755908cfdcb13dee`  
		Last Modified: Sat, 22 Jun 2024 00:56:02 GMT  
		Size: 3.3 MB (3333244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:579cc8ba5d68f37d9b4488901bb91ae1f9546562501abb2a998e2444d8af1782`  
		Last Modified: Sat, 22 Jun 2024 00:56:02 GMT  
		Size: 19.5 KB (19528 bytes)  
		MIME: application/vnd.in-toto+json
