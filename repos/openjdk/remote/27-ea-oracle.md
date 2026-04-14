## `openjdk:27-ea-oracle`

```console
$ docker pull openjdk@sha256:fec3fb9779b35cb5cf71071b590adfdeeca91631acfe155986ddaf3b0f686301
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:27-ea-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:9099f0c734553d1389c49fbb97845abc5fc392b618cded59a8b630f8db970204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.6 MB (309596959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fe8aaf9d77e17e26131115d7ee47a5e1dc7b3cdb8933bbce2efaa234026710f`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 27 Mar 2026 00:16:42 GMT
ADD oraclelinux-10-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 27 Mar 2026 00:16:42 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 00:00:45 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 00:00:55 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 14 Apr 2026 00:00:55 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:00:55 GMT
ENV LANG=C.UTF-8
# Tue, 14 Apr 2026 00:00:55 GMT
ENV JAVA_VERSION=27-ea+17
# Tue, 14 Apr 2026 00:00:55 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='9052972f914c38a9c00c5d8104a0b58217438f9a672ae7abead7c12347bb0d7c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='c2be8295243785a5077e17817615b5f355a643367e44eef5972e58fcbd8bde4b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 14 Apr 2026 00:00:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1101a6a16bdd51aef6dda35e785dca1d7934d2937fdc0c8dfc0f002ced99f85a`  
		Last Modified: Fri, 27 Mar 2026 00:16:52 GMT  
		Size: 43.1 MB (43068827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59c08ed4691881002c69f605ab78a66efb019ce17c4513eddac26ae8e2f0d1a`  
		Last Modified: Tue, 14 Apr 2026 00:01:20 GMT  
		Size: 37.7 MB (37679016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f1b3576bfd0a9b65df437fc2a02439ec16f9f3a0f24704d32b18102f0a1bc7`  
		Last Modified: Tue, 14 Apr 2026 00:01:22 GMT  
		Size: 228.8 MB (228849116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:e1847050738878e59a0350955a889cd7cdba7473ff255b8388c36f89f107d2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136a0ac139da2264581f9d7c6e2f7b6c91b9adb74523d177d5bb30927665ba20`

```dockerfile
```

-	Layers:
	-	`sha256:4cd8912a583e4fdd89c3ec116977c6edde5255551ce1f8306db3a53530e26ef0`  
		Last Modified: Tue, 14 Apr 2026 00:01:17 GMT  
		Size: 2.4 MB (2368347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e791431ee844c517d591b68097c6a1cf43d58b60f9470398c9a01b864d0c86eb`  
		Last Modified: Tue, 14 Apr 2026 00:01:20 GMT  
		Size: 17.9 KB (17850 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:27-ea-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:293f1cf8d4b8afb0ed79aadaeed79de0353d0fd962185ba980ddd3f585b32176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.0 MB (305970422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77bc8708680dcb4d5d501767e60341ed156d41f03dee5271777e9eed51c76ffd`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 27 Mar 2026 00:16:42 GMT
ADD oraclelinux-10-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 27 Mar 2026 00:16:42 GMT
CMD ["/bin/bash"]
# Tue, 14 Apr 2026 00:02:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Tue, 14 Apr 2026 00:02:35 GMT
ENV JAVA_HOME=/usr/java/openjdk-27
# Tue, 14 Apr 2026 00:02:35 GMT
ENV PATH=/usr/java/openjdk-27/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 14 Apr 2026 00:02:35 GMT
ENV LANG=C.UTF-8
# Tue, 14 Apr 2026 00:02:35 GMT
ENV JAVA_VERSION=27-ea+17
# Tue, 14 Apr 2026 00:02:35 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='9052972f914c38a9c00c5d8104a0b58217438f9a672ae7abead7c12347bb0d7c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='c2be8295243785a5077e17817615b5f355a643367e44eef5972e58fcbd8bde4b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 14 Apr 2026 00:02:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3db22c05661dd4dd65ed2c3add4946b3292ef86d7a62c06699ee25367fc2e1b`  
		Last Modified: Fri, 27 Mar 2026 00:16:52 GMT  
		Size: 41.5 MB (41474500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeab489b9e49969b98c3dfdd4686c60ff5fb869fa9f77df263596a96b834efa4`  
		Last Modified: Tue, 14 Apr 2026 00:02:58 GMT  
		Size: 37.7 MB (37687760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a785c8c3ceba94f04a81cf4a003598e20a6e71970a4de00f9f8114939e54517d`  
		Last Modified: Tue, 14 Apr 2026 00:03:02 GMT  
		Size: 226.8 MB (226808162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:27-ea-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:a6df0cf8f020ebcae6b4a09d6b4159f2831a26944786030a26654d21371acf67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2385940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2edc183a6eeb139c546a0d88314123c05cfb79feadd82364084679a211603a5c`

```dockerfile
```

-	Layers:
	-	`sha256:43fcc2091f17a9823cbde4f5d0229f37b7937349a15f7bf5ce90db99b87adef2`  
		Last Modified: Tue, 14 Apr 2026 00:02:57 GMT  
		Size: 2.4 MB (2367875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f91a7be347a233b0f6a5c50726bf922d47a4ebf439b7f54e7e42c4c38272c92d`  
		Last Modified: Tue, 14 Apr 2026 00:02:56 GMT  
		Size: 18.1 KB (18065 bytes)  
		MIME: application/vnd.in-toto+json
