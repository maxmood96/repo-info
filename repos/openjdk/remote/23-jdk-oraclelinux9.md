## `openjdk:23-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:b987f69e7d2e0eeb8577d357105302a6248dd5610521db00f4101c9f727248ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:b7c9916461da61d076dd303d5391a006c59c13a4a6e444492a6511433cba6610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.6 MB (299577704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9add8806a15ca44035407dc84f0da83da66379f0b215b91a127eb3923804ee`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 21 Aug 2024 18:48:11 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
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
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c4c38190c3a885670864bf9cf65e77d9aca90916e8e27e9b941e11b92bb10d`  
		Last Modified: Fri, 23 Aug 2024 01:50:28 GMT  
		Size: 39.1 MB (39067694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da32cc069bbf73d02cb1e1498563414833bf5540085f6608829aeac1222561b`  
		Last Modified: Fri, 23 Aug 2024 01:50:32 GMT  
		Size: 211.3 MB (211275946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:cb28935ab923fb6bd9a17024c92b0a480da98c87148c80f3db69d45a1a7617ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3659975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58bd9fd261fbac39589d52c8faf41e679fb2d74b1cf3d48239815134fcb83dc`

```dockerfile
```

-	Layers:
	-	`sha256:d794e26230a41568af936194f0d88bf21b9f2efcba454207f0fc1d8926ce57b0`  
		Last Modified: Fri, 23 Aug 2024 01:50:27 GMT  
		Size: 3.6 MB (3642311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce8812d2fd0c1884a0cb8326ec70b035660956e0bb05a82319dd36aa54d43abd`  
		Last Modified: Fri, 23 Aug 2024 01:50:26 GMT  
		Size: 17.7 KB (17664 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-jdk-oraclelinux9` - linux; arm64 variant v8

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

### `openjdk:23-jdk-oraclelinux9` - unknown; unknown

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
