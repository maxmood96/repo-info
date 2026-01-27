## `openjdk:26-ea-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:d773d34ae720a2c06a2a9d302f5bfb7a1492ff835e62167e6c2657c4c9bb9e2c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:f7390e552a48ddbc0148c57b8c49f7cd642445eda8de421eef2c20191cbb32fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294781672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6d780b1187995236b607e39ab47798ff991202fbf5c183ab58fe7c3e5b7d6cc`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 26 Jan 2026 22:04:10 GMT
ADD oraclelinux-8-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 26 Jan 2026 22:04:10 GMT
CMD ["/bin/bash"]
# Mon, 26 Jan 2026 22:20:52 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 26 Jan 2026 22:21:00 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Mon, 26 Jan 2026 22:21:00 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:21:00 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jan 2026 22:21:00 GMT
ENV JAVA_VERSION=26-ea+32
# Mon, 26 Jan 2026 22:21:00 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/32/GPL/openjdk-26-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='99e956807a500a396bc799f5b450e79c295bccece78ae9ca67f3e75646d3a099'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/32/GPL/openjdk-26-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='ef6d53835db7740daeda9be917698b14f742df288966e4985504f7f2e465ad0b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 26 Jan 2026 22:21:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:70f5c9ee868f124c508277177dfd78acddb8ada1f704dc8be2b2cdd99836131c`  
		Last Modified: Mon, 26 Jan 2026 22:04:22 GMT  
		Size: 51.5 MB (51467065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c22601a166c38db3fe5d5b19aa58ab985dbd8fc7a08ce77521cef6118f3871`  
		Last Modified: Mon, 26 Jan 2026 22:21:21 GMT  
		Size: 15.0 MB (14991226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb22c6368e9f580cefac6d3bb6c5db1fdf21f8bec18e8edbda43d266ccfab60`  
		Last Modified: Mon, 26 Jan 2026 22:21:25 GMT  
		Size: 228.3 MB (228323381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:9f5b51f33327ee9d23dc85e29ae990e23d9189e9ffaf3d79148c5af75561e48f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b743edb1f99ab90d199d2b05d7d3f393da5ed687cef03a5d6ab54401eeebfaa6`

```dockerfile
```

-	Layers:
	-	`sha256:79ac99bd046e6b1848d54f4ddb6b6038e86ff3d66de24f23c2c6cc1f372d0b61`  
		Last Modified: Mon, 26 Jan 2026 22:21:20 GMT  
		Size: 2.4 MB (2448688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cebe6765ccd0887c56cefe95bd0f6ea3844a009e5d179ccce41b32b27e6ef404`  
		Last Modified: Mon, 26 Jan 2026 22:21:20 GMT  
		Size: 15.3 KB (15343 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3cce5738151b525d171acae0db0c92ecdc2f9c1a0bde539e1e81a025ca3cd2f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292145432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84bef004d896863dd629424337da7afe556b255fbe85c1d88023953040d3364`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 26 Jan 2026 22:07:11 GMT
ADD oraclelinux-8-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 26 Jan 2026 22:07:11 GMT
CMD ["/bin/bash"]
# Mon, 26 Jan 2026 22:17:16 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 26 Jan 2026 22:17:25 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Mon, 26 Jan 2026 22:17:25 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jan 2026 22:17:25 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jan 2026 22:17:25 GMT
ENV JAVA_VERSION=26-ea+32
# Mon, 26 Jan 2026 22:17:25 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/32/GPL/openjdk-26-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='99e956807a500a396bc799f5b450e79c295bccece78ae9ca67f3e75646d3a099'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/32/GPL/openjdk-26-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='ef6d53835db7740daeda9be917698b14f742df288966e4985504f7f2e465ad0b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 26 Jan 2026 22:17:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3e76a047bd66be5e3e8818d893725279bf9a5b8a583db4b258f0d16df8850a42`  
		Last Modified: Mon, 26 Jan 2026 22:07:23 GMT  
		Size: 50.2 MB (50197120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1b3aa08084e10d32a9d04d08cde12fbd41fde6d8de4a29dfc0f3ce24a661f9`  
		Last Modified: Mon, 26 Jan 2026 22:17:46 GMT  
		Size: 15.7 MB (15687661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e17eab9133f91988fcf680022d99ebb7f863b33a58a5540b7a8d08703bacb5`  
		Last Modified: Mon, 26 Jan 2026 22:17:50 GMT  
		Size: 226.3 MB (226260651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:a69fa5295aee11284ea0d0a38139d76f20d9fd7325771837a64a0d03b77311fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2462960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e574143ffde5adb9c69ccff33b1d06aeb502b330974d0fe81a181dc83243c0b`

```dockerfile
```

-	Layers:
	-	`sha256:f5eed877a41ba5769740a34a6f5bff56106be467d260a0a94a631e1fa9448a2b`  
		Last Modified: Mon, 26 Jan 2026 22:17:46 GMT  
		Size: 2.4 MB (2447498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc5c3ff1fe56467c3ca67fbb9f5bd465977807b51f214328b69829e1bb13a08c`  
		Last Modified: Mon, 26 Jan 2026 22:17:45 GMT  
		Size: 15.5 KB (15462 bytes)  
		MIME: application/vnd.in-toto+json
