## `openjdk:27-ea-13-jdk-oracle`

```console
$ docker pull openjdk@sha256:5c25a6a171c7fbde0172b0986e9d6d75dc2d811ded783fea39cc0c4aac80978f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-13-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:90f3d6ac7c0f670f1b5db064e2849244fddb5652c37e20f603b6b95858ced74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.1 MB (309112272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe59cf2c0e77ceb8c572b7c824e9594326e9d481ae52c1b4f0ed5fdf12731dc3`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 03 Mar 2026 00:40:51 GMT
ADD oraclelinux-10-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 03 Mar 2026 00:40:51 GMT
CMD ["/bin/bash"]
# Wed, 18 Mar 2026 21:37:07 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 18 Mar 2026 21:37:16 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Wed, 18 Mar 2026 21:37:16 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Mar 2026 21:37:16 GMT
ENV LANG=C.UTF-8
# Wed, 18 Mar 2026 21:37:16 GMT
ENV JAVA_VERSION=27-ea+13
# Wed, 18 Mar 2026 21:37:16 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='abf2fddc7c040d0da78ea21bf8a24e8886b7db5b0451535b1382c8d04555a3a6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='2279406d233d34ad8cd779ec6d67043d77c66a16ba54b2b8085cc3a8e8709de7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 18 Mar 2026 21:37:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cb67f37368a87957df0eb5901d942cd123d97d089d4956fcec5c0f2ffa2828b0`  
		Last Modified: Tue, 03 Mar 2026 00:41:02 GMT  
		Size: 43.0 MB (43032813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe5de7f48660d898887e1a00ff4330d279c96d75d917aee9c8adc33797194d84`  
		Last Modified: Wed, 18 Mar 2026 21:37:37 GMT  
		Size: 37.6 MB (37643942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a933e97e495deaab16ee6fc55a3c3113a08e5ed8f1771e20126c588350135c67`  
		Last Modified: Wed, 18 Mar 2026 21:37:41 GMT  
		Size: 228.4 MB (228435517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-13-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:fb5e0fce54fb92cb5385363faa42aaf3f838658b019368f2e055fed540955618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:112a5c5526d82982bf96efde65fefde334cf431a6d3f5d7072002dee990afe61`

```dockerfile
```

-	Layers:
	-	`sha256:3c97d5d156959a7541b263f185107b1ff9f6c31770e985d0353e355e1f72b42f`  
		Last Modified: Wed, 18 Mar 2026 21:37:37 GMT  
		Size: 2.4 MB (2368329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcda886185c61ed557a237f06965a7ed5de4030952cf563509e2b4d8292466cf`  
		Last Modified: Wed, 18 Mar 2026 21:37:36 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-13-jdk-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:5cbe8560282c4570e4925787317ce806e7fa4eafacc8e838bd02e456a269f6b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.5 MB (305496494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8cf615b00c30783aef2752e366a21bae2d4e8134d85f280dba868223ebd4da`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 03 Mar 2026 00:40:38 GMT
ADD oraclelinux-10-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 03 Mar 2026 00:40:38 GMT
CMD ["/bin/bash"]
# Wed, 18 Mar 2026 21:36:54 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Wed, 18 Mar 2026 21:37:05 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Wed, 18 Mar 2026 21:37:05 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Mar 2026 21:37:05 GMT
ENV LANG=C.UTF-8
# Wed, 18 Mar 2026 21:37:05 GMT
ENV JAVA_VERSION=27-ea+13
# Wed, 18 Mar 2026 21:37:05 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_linux-x64_bin.tar.gz'; 			downloadSha256='abf2fddc7c040d0da78ea21bf8a24e8886b7db5b0451535b1382c8d04555a3a6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_linux-aarch64_bin.tar.gz'; 			downloadSha256='2279406d233d34ad8cd779ec6d67043d77c66a16ba54b2b8085cc3a8e8709de7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Wed, 18 Mar 2026 21:37:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b54727896c96f10ba558e1e01ab50406624252c92aadc5e38acb1cb78a5da11c`  
		Last Modified: Tue, 03 Mar 2026 00:40:48 GMT  
		Size: 41.4 MB (41439954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7c5fa13f57e5733011c171e99ff06e4bb971a011824239b7c1f04f69ee95c8`  
		Last Modified: Wed, 18 Mar 2026 21:37:27 GMT  
		Size: 37.6 MB (37648311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2fe4cbcc4caf7845a9a7c2145b054fd317317f19b5535e048954172bec7dbf`  
		Last Modified: Wed, 18 Mar 2026 21:37:31 GMT  
		Size: 226.4 MB (226408229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-13-jdk-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:8bf5551c5fa2e3ffc8c14f95eb6cf562e013369e5706e23b151b54a5df7e61e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc164ab94e6d07f3b87cbfeef3ec76b1966ee3e249d6bd0d998fd2892abce2e`

```dockerfile
```

-	Layers:
	-	`sha256:49ddd8b5359fd429f0b55025c84b2efa29e7bc0597002255761fda249cf12477`  
		Last Modified: Wed, 18 Mar 2026 21:37:26 GMT  
		Size: 2.4 MB (2367857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1add1d661d234f89c9a5e415fbae2d021bd8c55383c085a11fdfd5f81540aec7`  
		Last Modified: Wed, 18 Mar 2026 21:37:26 GMT  
		Size: 18.1 KB (18065 bytes)  
		MIME: application/vnd.in-toto+json
