## `openjdk:26-ea-oracle`

```console
$ docker pull openjdk@sha256:8b66dedd7110fc9283432f819a03f152c23f2858666edf13ddd0d82c627014cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:26-ea-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:523fb57e418827e911712efb99c3a4130c7e2132d2754f699f2f0f693374d999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313456100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c0506400ce5698088153ba874b4cf5fa7f4ba26c2f7aeb0385cab9de1fc0dc`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:05:44 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:05:56 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 23 Jan 2026 01:05:56 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jan 2026 01:05:56 GMT
ENV LANG=C.UTF-8
# Fri, 23 Jan 2026 01:05:56 GMT
ENV JAVA_VERSION=26-ea+31
# Fri, 23 Jan 2026 01:05:56 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/31/GPL/openjdk-26-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='bfc006ca65cf590a40d808e5dc5cc973b98e11e309d0efa5dc36340c8b3ffdbb'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/31/GPL/openjdk-26-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='3b9511be1b72db3be1c49c25cbecda90f37642003c9844f7d363455ad702ff7b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 23 Jan 2026 01:05:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7567ec5ead2f2a3d46652fe66e8c9ff777d9df550b7f827115b76680ca7b1f26`  
		Last Modified: Fri, 23 Jan 2026 01:06:18 GMT  
		Size: 38.3 MB (38296810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54b9f1b2da02e4e9f5aec977f4ae8378495225cadc13fac8b8c5cd8b54b98f6`  
		Last Modified: Fri, 23 Jan 2026 01:06:21 GMT  
		Size: 227.8 MB (227845742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:51b637a26fdc72a3c758c0477b96807de7c79a62a5f94049f11ce722724a2c1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472a78c3740ffc4553c786e94888caf334ee3a6cdcd120e066600916b37db1e3`

```dockerfile
```

-	Layers:
	-	`sha256:ca2d7317fa899efe42786c697f13d87105ca8c99b17bb98e152c518c853cf763`  
		Last Modified: Fri, 23 Jan 2026 01:06:16 GMT  
		Size: 3.7 MB (3655375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0f5098fd16fe9f1e17b65a86a751213c8d0364aca24b413cf54507a02ce38f8`  
		Last Modified: Fri, 23 Jan 2026 01:06:16 GMT  
		Size: 17.8 KB (17839 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:26-ea-oracle` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0acd132dc14def81e7402080b503d9197d48b65338012db9e11f5afc50293934
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310372235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb94a23efdc56b7e45293b0117a1c16a381f3124a74b612eab9ebc85a1905647`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:02:56 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:07 GMT
ENV JAVA_HOME=/usr/java/openjdk-26
# Fri, 23 Jan 2026 01:03:07 GMT
ENV PATH=/usr/java/openjdk-26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Jan 2026 01:03:07 GMT
ENV LANG=C.UTF-8
# Fri, 23 Jan 2026 01:03:07 GMT
ENV JAVA_VERSION=26-ea+31
# Fri, 23 Jan 2026 01:03:07 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/31/GPL/openjdk-26-ea+31_linux-x64_bin.tar.gz'; 			downloadSha256='bfc006ca65cf590a40d808e5dc5cc973b98e11e309d0efa5dc36340c8b3ffdbb'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk26/31/GPL/openjdk-26-ea+31_linux-aarch64_bin.tar.gz'; 			downloadSha256='3b9511be1b72db3be1c49c25cbecda90f37642003c9844f7d363455ad702ff7b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 23 Jan 2026 01:03:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10149318b0d3fb31545f370908584b5804c5ac797fe8224b0f91ee6dc712ac13`  
		Last Modified: Fri, 23 Jan 2026 01:03:30 GMT  
		Size: 38.7 MB (38699886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63b73fda125793a74fa17da84c0678c3d1c60fdffe943ff5789a6177c211511`  
		Last Modified: Fri, 23 Jan 2026 01:03:33 GMT  
		Size: 225.8 MB (225770439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:26-ea-oracle` - unknown; unknown

```console
$ docker pull openjdk@sha256:e9fb9cac46e361014a6f8a828c165be7722579c99178426ca4194ed0133aa524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3671119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fda278c29fad9682298a7cb7e2b7d708fc5e45118344dcc1e1785afe55996c8`

```dockerfile
```

-	Layers:
	-	`sha256:5c403914f637ee7eaba0238af4c40b5fd8e68ca0930d67ecd048a563cdab3c47`  
		Last Modified: Fri, 23 Jan 2026 01:03:28 GMT  
		Size: 3.7 MB (3653065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:244760da3829ed1e8f9051d141bd063fa8168afad3a57716f2743ae71170a16a`  
		Last Modified: Fri, 23 Jan 2026 01:03:28 GMT  
		Size: 18.1 KB (18054 bytes)  
		MIME: application/vnd.in-toto+json
