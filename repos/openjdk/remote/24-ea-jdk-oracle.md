## `openjdk:24-ea-jdk-oracle`

```console
$ docker pull openjdk@sha256:4c4a62841b4232035333f62f191cb269168e9e3fb3fea84e1c93180961e78725
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:bb775d80c2d72eb0b92f6421b43d2fc364b09a0f69546732b7d75d426df89605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.1 MB (300058858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96e9f66d2c4901dd8646fd3a46e1ceebbdbddb9d3552a1894c024a0e735f5601`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Aug 2024 18:48:14 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Fri, 16 Aug 2024 18:48:14 GMT
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
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4322799a14f7d92dd8d8f90e6c46e188ce6e3b737e17c2e3161acaf70f55495`  
		Last Modified: Fri, 23 Aug 2024 01:50:46 GMT  
		Size: 39.1 MB (39068112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5aef70e9107dd2a5aedb40d7dff3ae225d99ff7f3db5546f9b4b9306494a40c`  
		Last Modified: Fri, 23 Aug 2024 01:50:48 GMT  
		Size: 211.8 MB (211756682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:64566d6ea46fd4c0c7fc5590871aec5637c01605f6a3193dbdc64b743bcaa648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3663778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c1f3d0527d2d8a6ad78b5f67bfbe91f11b18c2c3dbe237bc0b95277ef6ba075`

```dockerfile
```

-	Layers:
	-	`sha256:226a7da84af435bcc1235e14d3017febaca3eeb68ba1bf8fc1ef58eae4d8701e`  
		Last Modified: Fri, 23 Aug 2024 01:50:45 GMT  
		Size: 3.6 MB (3644251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5da6424fd65399f0b4071453588cb80060de0c3000977bc61e8326df01dd869`  
		Last Modified: Fri, 23 Aug 2024 01:50:45 GMT  
		Size: 19.5 KB (19527 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:744e8bc9e49b01b99944181afffba42580b871818f6306c9f686d85c24ea35a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.0 MB (296992268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca59ef5b8f50f2e53fe3b25c8a752f3d516a5c101deff3c6c8db5ef2a2326fb`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 16 Aug 2024 18:48:14 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Fri, 16 Aug 2024 18:48:14 GMT
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
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd1b36cd87201413a78d843fcfb1218c857939c3962a8c46b1f8126a2336f87`  
		Last Modified: Fri, 23 Aug 2024 01:54:37 GMT  
		Size: 39.5 MB (39496829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2890105f9ec25867ee76e02bf36128c83925a3c439045ca5fda24abd81272c9a`  
		Last Modified: Fri, 23 Aug 2024 01:54:42 GMT  
		Size: 209.6 MB (209607648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:a61582f29c7d9f13f2b105bd6beef6c7ccd1c824f10c578024a3e0a5bc10e9c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3662637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff4fe6347448ee6a6c7c68b169d72e26185caa36156ceba1a1aaff3c7a4eb39`

```dockerfile
```

-	Layers:
	-	`sha256:fd9bd3a7eec396f182419ee6a73d5780d524378edd94269593e6e4fc6db4b679`  
		Last Modified: Fri, 23 Aug 2024 01:54:36 GMT  
		Size: 3.6 MB (3642634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39b717c0da2dda303d455d4056cad4750a663721ce5b5ce0f355c18e955baddc`  
		Last Modified: Fri, 23 Aug 2024 01:54:36 GMT  
		Size: 20.0 KB (20003 bytes)  
		MIME: application/vnd.in-toto+json
