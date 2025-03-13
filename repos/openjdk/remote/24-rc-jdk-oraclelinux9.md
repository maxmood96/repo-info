## `openjdk:24-rc-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:0c0783a222f805a77a471ead025cb447b4ade1f1e88ba86debfad0f49e18c562
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-rc-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:a71dcd0ca1146f6546c7cd45ba2e056285b1e8f50f478b6f90ef182e9284677a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.7 MB (310687491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2362924ff4dabaf3f2e1f84c401569b8c0fe3808761ba6f26505da0c02f0a1ab`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Feb 2025 01:48:12 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 07 Feb 2025 01:48:12 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Feb 2025 01:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_VERSION=24
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-x64_bin.tar.gz'; 			downloadSha256='88b090fa80c6c1d084ec9a755233967458788e2c0777ae2e172230c5c692d7ef'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-aarch64_bin.tar.gz'; 			downloadSha256='a03867ed061c7bb661231e62b0967ff5a5a0b1bbaa37bdead3a924bd2ba3215f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:804bb8ae89decacdf918af27c892df04e6f2d3038e3a7d1e34475eef6be9aba3`  
		Last Modified: Thu, 13 Mar 2025 17:46:19 GMT  
		Size: 49.1 MB (49091441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c1951d12e05472fbe787ed447fad73c9468aa049fab5c4aeb43f872f770879`  
		Last Modified: Thu, 13 Mar 2025 17:53:05 GMT  
		Size: 48.8 MB (48758884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4e855ebd26f2c6684092ec3490639868c20cae8a5c2ecfb278ddcebdbdeba8`  
		Last Modified: Thu, 13 Mar 2025 17:53:08 GMT  
		Size: 212.8 MB (212837166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-rc-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:a4e5e067b46c78d48b894426b247c351b64aa8c167b8895446d772269d4d9525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4927336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c12d21dc9aa3e9b68428c387613659643e94631179aa4d760221158ceacf84`

```dockerfile
```

-	Layers:
	-	`sha256:84e148d995ce056725486ac3d57f30479d9a3403a48244b0ff973fbfab9f07c0`  
		Last Modified: Thu, 13 Mar 2025 17:53:05 GMT  
		Size: 4.9 MB (4909455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ea2e46ea1f929f08f6f748e079f3785bf57b42a832d639e49e0043b06989234`  
		Last Modified: Thu, 13 Mar 2025 17:53:04 GMT  
		Size: 17.9 KB (17881 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-rc-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:1215a7119dcc2358a20eba74503cb3e9411b615ea65a5664153369b7df8fd7b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.6 MB (307641188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bccd0629b92bc70b5500f140f728157967e8e4a6425bab7d42d1cd78ee65a9d6`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Feb 2025 01:48:12 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["/bin/bash"]
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 07 Feb 2025 01:48:12 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Feb 2025 01:48:12 GMT
ENV LANG=C.UTF-8
# Fri, 07 Feb 2025 01:48:12 GMT
ENV JAVA_VERSION=24
# Fri, 07 Feb 2025 01:48:12 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-x64_bin.tar.gz'; 			downloadSha256='88b090fa80c6c1d084ec9a755233967458788e2c0777ae2e172230c5c692d7ef'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk24/1f9ff9062db4449d8ca828c504ffae90/36/GPL/openjdk-24_linux-aarch64_bin.tar.gz'; 			downloadSha256='a03867ed061c7bb661231e62b0967ff5a5a0b1bbaa37bdead3a924bd2ba3215f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 07 Feb 2025 01:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ce92cb0849370fbaafa6ab88c7b03cebc3063fa56835d9dbf7d0b47c679a0097`  
		Last Modified: Thu, 13 Mar 2025 18:10:14 GMT  
		Size: 47.7 MB (47668022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4526627be0e2d666f68ddd55808801d398e443da5584c4a85a1289885b0191af`  
		Last Modified: Thu, 13 Mar 2025 19:16:07 GMT  
		Size: 49.2 MB (49185276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7b81781c78447d589ff5c0298b01257d06764be80d842bd3336e08ce6e699c`  
		Last Modified: Thu, 13 Mar 2025 19:16:10 GMT  
		Size: 210.8 MB (210787890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-rc-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:26ca55f23abe6c6d669d3e7d9d55cb3298c557f13f40a5ae01d3c7d848cb052c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4925241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d5f2327683b42ddb9ea05e9c26af74360c1cecea8beb052a8ebe5901235b6e0`

```dockerfile
```

-	Layers:
	-	`sha256:94f74af34d260c252a3711cdce250d861e62ead44caa5087b5c43e67e9adcb3a`  
		Last Modified: Thu, 13 Mar 2025 19:16:05 GMT  
		Size: 4.9 MB (4907145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc95c9327400443c1064f16fdffc032152ccf32d43006b382758b0e000450d89`  
		Last Modified: Thu, 13 Mar 2025 19:16:05 GMT  
		Size: 18.1 KB (18096 bytes)  
		MIME: application/vnd.in-toto+json
