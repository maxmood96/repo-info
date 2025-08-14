## `openjdk:25-oraclelinux9`

```console
$ docker pull openjdk@sha256:2bbcde163c2c4c55c7dc9c47f87a0f4cb32982bb5403b2ef1f2288e396ce3041
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:53d824a1cedd3efcc82e3bc9794acb41c39ee6af376d76ff32c528c37b136f41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310562079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc31f8db2985cf9f6680913be37c318287185cb45f14223249e9efc1e2d18337`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 07 Aug 2025 20:58:59 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 07 Aug 2025 20:58:59 GMT
CMD ["/bin/bash"]
# Sat, 09 Aug 2025 00:48:09 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 09 Aug 2025 00:48:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 09 Aug 2025 00:48:09 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Aug 2025 00:48:09 GMT
ENV LANG=C.UTF-8
# Sat, 09 Aug 2025 00:48:09 GMT
ENV JAVA_VERSION=25
# Sat, 09 Aug 2025 00:48:09 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/35/GPL/openjdk-25_linux-x64_bin.tar.gz'; 			downloadSha256='c00224c25b0b915f4d69929d90e59dfd66e949f79f7437d334248f7789b646f4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/35/GPL/openjdk-25_linux-aarch64_bin.tar.gz'; 			downloadSha256='2cf9e308cd667a6134865652839a3f7d59a93198a10841cb893f65248d1852d7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 09 Aug 2025 00:48:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:10aec8a104c7ecf055b7137fb34a3666fce4dff1b9f6d210fb88eaddd4c8c329`  
		Last Modified: Thu, 07 Aug 2025 23:49:00 GMT  
		Size: 49.5 MB (49497127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18beaa66d5b2f4b1712c0bcd2e57b7dea3bdb319e7fe71d02d44e9803f4d542`  
		Last Modified: Tue, 12 Aug 2025 18:03:01 GMT  
		Size: 38.0 MB (38004926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da4374e5d3c667564f67fa2148749db38ad2d7ecc483d2df1ec815f4cf5b99b`  
		Last Modified: Tue, 12 Aug 2025 21:35:54 GMT  
		Size: 223.1 MB (223060026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:cd8ed50f1de8a51efba74fd0e8935fb0e671e8b267140418eede1fdda9dd4afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3657300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c9136c881102ae3e6d36501992a478b04a8391f7bd9f031ed5214301ce1a572`

```dockerfile
```

-	Layers:
	-	`sha256:e868b377dff9a463e4d429d4b0643cb950d27bb6e2309b52b7c883db7df70563`  
		Last Modified: Tue, 12 Aug 2025 21:23:26 GMT  
		Size: 3.6 MB (3639418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49c0995e1541d56443e3f3f85a839755675210dc5c67ce02d5c8ee81e681804b`  
		Last Modified: Tue, 12 Aug 2025 21:23:27 GMT  
		Size: 17.9 KB (17882 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9d744c29e3a2cb92d3baa54a25541287df6799176bc214591ec912d14360576d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.4 MB (307362436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03e31a9a5873191a01e1a4ca24a983d1321909108fc4d394f96f72a813f3bc0`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 07 Aug 2025 20:59:57 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 07 Aug 2025 20:59:57 GMT
CMD ["/bin/bash"]
# Sat, 09 Aug 2025 00:48:09 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 09 Aug 2025 00:48:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 09 Aug 2025 00:48:09 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Aug 2025 00:48:09 GMT
ENV LANG=C.UTF-8
# Sat, 09 Aug 2025 00:48:09 GMT
ENV JAVA_VERSION=25
# Sat, 09 Aug 2025 00:48:09 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/35/GPL/openjdk-25_linux-x64_bin.tar.gz'; 			downloadSha256='c00224c25b0b915f4d69929d90e59dfd66e949f79f7437d334248f7789b646f4'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk25/bd75d5f9689641da8e1daabeccb5528b/35/GPL/openjdk-25_linux-aarch64_bin.tar.gz'; 			downloadSha256='2cf9e308cd667a6134865652839a3f7d59a93198a10841cb893f65248d1852d7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 09 Aug 2025 00:48:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:da99ef17bcd1d6b39ce9eab8bcb39fc1902df72d68384325b4fa2b0342d5c908`  
		Last Modified: Fri, 08 Aug 2025 00:16:18 GMT  
		Size: 48.1 MB (48086911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868932e6de7288e116d57bafe15e69e4d2baebd6453c84a2fbd529067b423d95`  
		Last Modified: Fri, 08 Aug 2025 00:24:48 GMT  
		Size: 38.4 MB (38407094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa01a6ba673891c7aa3782df93745cf177d4d2033fcfdaf6a7af67c83cb5f947`  
		Last Modified: Wed, 13 Aug 2025 02:05:52 GMT  
		Size: 220.9 MB (220868431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:83c2f64c4d25a3b5771ce585a65ac3159fe1912171051792a8175e75e66d0d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3655204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44358f91ae76fcf1ac049faad684ac323a50c2fbcd865bbf98f6e656cc753177`

```dockerfile
```

-	Layers:
	-	`sha256:6ecc152c0d3ae49b598845fdfbe584847a0cebb9a0a226fc0c4422019d21fc5f`  
		Last Modified: Wed, 13 Aug 2025 00:23:23 GMT  
		Size: 3.6 MB (3637108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5ff687c95ee6340e4520247d296154b6533089c701068e768043b2dcba851e0`  
		Last Modified: Wed, 13 Aug 2025 00:23:24 GMT  
		Size: 18.1 KB (18096 bytes)  
		MIME: application/vnd.in-toto+json
