## `openjdk:28-ea-3-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:5275fd96ddd8fd8ae5eb00a65241a25e12857c6b949af880fc24083d58d94752
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:28-ea-3-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:96444f44cbee9738130920a13bbc13c3595c2860fbd0cf330ae45eef885eb26a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314346878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77b6f494f57f829a38851460cdfe2eefb1479e3b9f461634167745e63279df02`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:25 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:25 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 22:38:42 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 22 Jun 2026 22:38:51 GMT
ENV JAVA_HOME=/usr/java/openjdk-28
# Mon, 22 Jun 2026 22:38:51 GMT
ENV PATH=/usr/java/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:38:51 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 22:38:51 GMT
ENV JAVA_VERSION=28-ea+3
# Mon, 22 Jun 2026 22:38:51 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/3/GPL/openjdk-28-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='44b5bc19b0533fb00a363915f15ee1c9a9514dca2fb5bd56d13c204676ceef67'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/3/GPL/openjdk-28-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='12d4698e60552120853334a624fd1d10ffca8386b1c52b0089fc9c607a9d46e8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 22 Jun 2026 22:38:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1dced004aaec9f4dae6c0e7fe81bf3c92963d98025502b68b1f19e4ac85b0c17`  
		Last Modified: Tue, 12 May 2026 18:44:37 GMT  
		Size: 47.3 MB (47309573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ab4020b86732245aa84fcdb0767c88272d4e770d16d555a8c5e9892ede6699`  
		Last Modified: Mon, 22 Jun 2026 22:39:15 GMT  
		Size: 39.7 MB (39652467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfab60b76f83449699355a64e13c31c38eb8e4de11f6047aa8ea4852316cb5bf`  
		Last Modified: Mon, 22 Jun 2026 22:39:18 GMT  
		Size: 227.4 MB (227384838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-3-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:1beed0f1dfed065013d945f676defffa7d9e2ee25ffceb39842abff3f86037ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3691872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac43f93884671e0a1a7b66739316c4d20b9deb5856993b8de70aecb838debbc`

```dockerfile
```

-	Layers:
	-	`sha256:5436a3ee8df27e052486e513831d97edde5f0ffc82c181799ec0375e1ca46785`  
		Last Modified: Mon, 22 Jun 2026 22:39:13 GMT  
		Size: 3.7 MB (3676546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea539976945d1a2bb45c4ed88b80e6655a19fb247abe02c72fbd4a1a8c2ab505`  
		Last Modified: Mon, 22 Jun 2026 22:39:12 GMT  
		Size: 15.3 KB (15326 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:28-ea-3-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:420d6d3473ac571f3f6bfcdfe79470b0d2496b39d4bbef60d5f26ff7cafc77b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.4 MB (311364171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfdf81d1c5be8dc9823263b9d4a4395e316e2ab6dba61a2d280418315047b405`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 12 May 2026 18:44:53 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Tue, 12 May 2026 18:44:53 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 22:38:45 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Mon, 22 Jun 2026 22:38:55 GMT
ENV JAVA_HOME=/usr/java/openjdk-28
# Mon, 22 Jun 2026 22:38:55 GMT
ENV PATH=/usr/java/openjdk-28/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Jun 2026 22:38:55 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 22:38:55 GMT
ENV JAVA_VERSION=28-ea+3
# Mon, 22 Jun 2026 22:38:55 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/3/GPL/openjdk-28-ea+3_linux-x64_bin.tar.gz'; 			downloadSha256='44b5bc19b0533fb00a363915f15ee1c9a9514dca2fb5bd56d13c204676ceef67'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk28/3/GPL/openjdk-28-ea+3_linux-aarch64_bin.tar.gz'; 			downloadSha256='12d4698e60552120853334a624fd1d10ffca8386b1c52b0089fc9c607a9d46e8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Mon, 22 Jun 2026 22:38:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:000edcaa94f8b608f347845846057365cafc2769493dbb0d0ece60231b3e2483`  
		Last Modified: Tue, 12 May 2026 18:45:05 GMT  
		Size: 45.9 MB (45899090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65dff0fbe92c7c9d7ad3a660a73cab5bb982254dcc988a4cb67592bf2c944ad`  
		Last Modified: Mon, 22 Jun 2026 22:39:18 GMT  
		Size: 40.0 MB (40046902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7c1d976f31bff8e152f95dc0843cfb21f302e4a4eacba3d59fe6d734fcb3bc`  
		Last Modified: Mon, 22 Jun 2026 22:39:22 GMT  
		Size: 225.4 MB (225418179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:28-ea-3-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:c28f47c8a8b8049889346fb846a23bb0d82ddd8136a8447db6098b6355256466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3689583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b6dc1a3d0a9650277028f78a5de8a48cc8d624902bdef233ef223a3592e275`

```dockerfile
```

-	Layers:
	-	`sha256:30ccbd9693b518f7e7196e6200d707a8f6b1aa673c8ae1bed591ff0387f31557`  
		Last Modified: Mon, 22 Jun 2026 22:39:16 GMT  
		Size: 3.7 MB (3674140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:091800c793d2555fbf725056a39c973381b2d853c014b88e93c8e674d514632a`  
		Last Modified: Mon, 22 Jun 2026 22:39:16 GMT  
		Size: 15.4 KB (15443 bytes)  
		MIME: application/vnd.in-toto+json
