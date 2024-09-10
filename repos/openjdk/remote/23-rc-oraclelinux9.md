## `openjdk:23-rc-oraclelinux9`

```console
$ docker pull openjdk@sha256:fbf41d61299ec894447fbc1be5a5d1acca7a233c5d3fb40055d7809a3a67a4ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-rc-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:4f466e1c9760899c1fe54ed23323e629941b3f1d628956e77c7439f8a818812e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.6 MB (299574548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac253b86a4d7b1a3fb142bda867f26d479739c127bd2e5040a91180eebefa44`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 21 Aug 2024 18:48:11 GMT
ADD file:d8a38112d165940510d5cfd57f316139caf4069546c97dfc10a08f33f3f1ca9f in / 
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
	-	`sha256:12d7e45337f84111b352ed27b6a21ab109dec7571b23ebc522b6bb6b318d883b`  
		Last Modified: Mon, 09 Sep 2024 22:21:36 GMT  
		Size: 49.2 MB (49237791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb18a03e90e9af487c207e7ea7b87e5fb5a799c86d672ac3ad9492ef1f018caf`  
		Last Modified: Mon, 09 Sep 2024 23:01:55 GMT  
		Size: 39.1 MB (39060765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8c850584c7a65d42e8fe736e4ce886160111b414b459c2284416e1e9de1a9b`  
		Last Modified: Mon, 09 Sep 2024 23:01:57 GMT  
		Size: 211.3 MB (211275992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-rc-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:fb82eb1bfef362f8f19fb49d7e763640df3de21e020eb4e778bc8692704ddba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3660003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b7cf4fd1b16f5a45c18e1b0341897c4c86381d294dc4ba5f04ecd92cfe60ed9`

```dockerfile
```

-	Layers:
	-	`sha256:addc98c6ec9b4a616a8ed1234c59d882a1fdc2457a78522cf3e8cd88b8953f09`  
		Last Modified: Mon, 09 Sep 2024 23:01:54 GMT  
		Size: 3.6 MB (3642339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5386e5f642465545e11b74a723df6d7f7d63c3871a5a9bb5b7a22e5f186e0f6a`  
		Last Modified: Mon, 09 Sep 2024 23:01:54 GMT  
		Size: 17.7 KB (17664 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-rc-oraclelinux9` - linux; arm64 variant v8

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

### `openjdk:23-rc-oraclelinux9` - unknown; unknown

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
