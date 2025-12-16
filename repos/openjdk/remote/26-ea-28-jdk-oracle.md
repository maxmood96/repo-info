## `openjdk:26-ea-28-jdk-oracle`

```console
$ docker pull openjdk@sha256:56fe771b082b0123a41e92d48a31a56f8c3e1eb192bcfef1b4354a31e79c7ae6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-28-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:0a70b1422e6db123e9f0da34821495286ad31e76ce7265df2ad2a36ea9fd644e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.4 MB (313431891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee96a7d88c7194a414e98b81e9e7dc146ae1e12b980b4115383a696f14133d8`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:31 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:31 GMT
CMD ["/bin/bash"]
# Tue, 16 Dec 2025 00:02:35 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 16 Dec 2025 00:02:45 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Tue, 16 Dec 2025 00:02:45 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 00:02:45 GMT
ENV LANG=C.UTF-8
# Tue, 16 Dec 2025 00:02:45 GMT
ENV JAVA_VERSION=26-ea+28
# Tue, 16 Dec 2025 00:02:45 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/28/GPL/openjdk-26-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='a18910b0bdceb12a4f78147a1feebee50cc621ad8114c07a1ab071e58c17b09d'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/28/GPL/openjdk-26-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='d330a706e3fc611f4b39f6768f104e47d0a755ffabda31e3299dbc2e791f4f18'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Dec 2025 00:02:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7a5e1e9175268f8a5062cd666fcd7ea2d50d08a02f6eb1873586009eb9e27529`  
		Last Modified: Tue, 02 Dec 2025 21:17:55 GMT  
		Size: 47.3 MB (47314748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795be9687a89d72dfa96f36a2dc857ace42392b9e386013f4dbead076eb8b220`  
		Last Modified: Tue, 16 Dec 2025 00:03:32 GMT  
		Size: 38.3 MB (38297199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c000f7227ee778d29e004e46e3a94923fe49576866652dfb883e0f127f901d`  
		Last Modified: Tue, 16 Dec 2025 00:03:40 GMT  
		Size: 227.8 MB (227819944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-28-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:3570ce40cd3532996bfea0ed9ff6d1e6de764e2028ae523ddc65d7125bdb4099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383028a4bb98c917656ae722244bc58112f144be4446b743768902416efa58a9`

```dockerfile
```

-	Layers:
	-	`sha256:8f900582b30481f5c1adc480401e399c4b92eb25d256c2bf86c6f615fa255bd6`  
		Last Modified: Tue, 16 Dec 2025 01:23:26 GMT  
		Size: 3.7 MB (3655331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4d6d9e2ae1a1998c111159edb53c415f76c3150f04a0eb85b469d3d2c8ca244`  
		Last Modified: Tue, 16 Dec 2025 01:23:27 GMT  
		Size: 17.8 KB (17839 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-28-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:6f1ff89e8557ab814aa24d28950f80afaf487a7febfe15ff3673e89c4ad5c343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.3 MB (310331810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7143b634beb64397204c89ee04b3ff54e6f7e4adc1cb0a538c2b8feb473a79`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 02 Dec 2025 21:17:01 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 02 Dec 2025 21:17:01 GMT
CMD ["/bin/bash"]
# Tue, 16 Dec 2025 00:02:24 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 16 Dec 2025 00:02:45 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Tue, 16 Dec 2025 00:02:45 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Dec 2025 00:02:45 GMT
ENV LANG=C.UTF-8
# Tue, 16 Dec 2025 00:02:45 GMT
ENV JAVA_VERSION=26-ea+28
# Tue, 16 Dec 2025 00:02:45 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/28/GPL/openjdk-26-ea+28_linux-x64_bin.tar.gz'; 			downloadSha256='a18910b0bdceb12a4f78147a1feebee50cc621ad8114c07a1ab071e58c17b09d'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/28/GPL/openjdk-26-ea+28_linux-aarch64_bin.tar.gz'; 			downloadSha256='d330a706e3fc611f4b39f6768f104e47d0a755ffabda31e3299dbc2e791f4f18'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 16 Dec 2025 00:02:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:842b90544a0050f7b114b301fe9bf455545f1ec7b827c2f9ec9585171d12c48f`  
		Last Modified: Tue, 02 Dec 2025 21:17:32 GMT  
		Size: 45.9 MB (45897032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc939c9928182a9c75221b9568a63a4fe7499d89f832ead56b8ea289392e8e0`  
		Last Modified: Tue, 16 Dec 2025 00:03:32 GMT  
		Size: 38.7 MB (38700187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f65678c1ac0e7dc12c615167283fe402abaca32375a7efd2db08fd51547969`  
		Last Modified: Tue, 16 Dec 2025 00:03:41 GMT  
		Size: 225.7 MB (225734591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-28-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:5efd71de9edfe6a852d5a8c083921b74efb0eb3f4d5d4c544ebe295f15f8bc30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f9601468582e3586d0029648f81c53e255f6acc93345784c80810135ba010fa`

```dockerfile
```

-	Layers:
	-	`sha256:817441da23b2e606e20ec2602f6dd2e6017cbe6f509cf5d864cd449f0683e8e6`  
		Last Modified: Tue, 16 Dec 2025 01:23:31 GMT  
		Size: 3.7 MB (3653021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bf14522b56929cfb752915cde0e0732581cb24a139351f2a406a9b60d26f73a`  
		Last Modified: Tue, 16 Dec 2025 01:23:32 GMT  
		Size: 18.1 KB (18054 bytes)  
		MIME: application/vnd.in-toto+json
