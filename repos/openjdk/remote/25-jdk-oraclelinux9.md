## `openjdk:25-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:da731a3c0c9fa0bd7b363011c3eb30bd36c0b481082a355f9c52a39c263be05a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:25-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:27e4e11e337da15cd89b1858c9c420d378b0057679afb830351e81f79f7d8b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310648965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d76b7be7ab1a6449a3f2e466f1b3daa72863aaeb0a0ffe4166c2381457ee212`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 05 Jul 2025 00:48:10 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Sat, 05 Jul 2025 00:48:10 GMT
CMD ["/bin/bash"]
# Sat, 05 Jul 2025 00:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 05 Jul 2025 00:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 05 Jul 2025 00:48:10 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Jul 2025 00:48:10 GMT
ENV LANG=C.UTF-8
# Sat, 05 Jul 2025 00:48:10 GMT
ENV JAVA_VERSION=25-ea+30
# Sat, 05 Jul 2025 00:48:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/30/GPL/openjdk-25-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='42cb8d0281909a790e94c154ae2a4492b990bca08ce399f8a431c58d92bebb37'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/30/GPL/openjdk-25-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='95be885f2e12ffb9ba3745dc29d8699a388c89f6826955aa9eb0c2f44a2d789b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 05 Jul 2025 00:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:90dac1e734aa2e08c0e4e8bb7d30232985487cf8abfb490025986f98bc2e5382`  
		Last Modified: Thu, 10 Jul 2025 23:20:44 GMT  
		Size: 49.5 MB (49500230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb2ff44a034c46522ac94f047b3ae010bfe1cc1275ac0709ca649821c5b6942`  
		Last Modified: Fri, 11 Jul 2025 00:08:45 GMT  
		Size: 38.1 MB (38093349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13580177ffb479926c4794d0b294a6f936bcf28c4dc343a74a1956beeb8498c`  
		Last Modified: Fri, 11 Jul 2025 04:30:46 GMT  
		Size: 223.1 MB (223055386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:178fc00cd5488631dfdc751accee726a45685dcf55ae76c182efffb925fbab3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3661055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752c6a796392e6f04108f6a0474fbabf92f18fab1e718d8da2df8759a474d3cc`

```dockerfile
```

-	Layers:
	-	`sha256:71e11a38255c535c982fab33a9ac28539b1a6b1b6414bf92854b11ee8d71a28d`  
		Last Modified: Fri, 11 Jul 2025 03:23:20 GMT  
		Size: 3.6 MB (3641310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f62325be4ea0e68971d729804b9ac5d3f782edd76cf41c949e213574e10d3b20`  
		Last Modified: Fri, 11 Jul 2025 03:23:21 GMT  
		Size: 19.7 KB (19745 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:25-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c4c20c5d9135577bc76efec15b21974f47d449119fa313986ec3cf52006b4fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.4 MB (307436838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5a4f4a5f7bb5431bf1b077449bb114db662928e7a369c3c7682311161375666`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 05 Jul 2025 00:48:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Sat, 05 Jul 2025 00:48:10 GMT
CMD ["/bin/bash"]
# Sat, 05 Jul 2025 00:48:10 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 05 Jul 2025 00:48:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-25
# Sat, 05 Jul 2025 00:48:10 GMT
ENV PATH=/usr/java/openjdk-25/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 05 Jul 2025 00:48:10 GMT
ENV LANG=C.UTF-8
# Sat, 05 Jul 2025 00:48:10 GMT
ENV JAVA_VERSION=25-ea+30
# Sat, 05 Jul 2025 00:48:10 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/30/GPL/openjdk-25-ea+30_linux-x64_bin.tar.gz'; 			downloadSha256='42cb8d0281909a790e94c154ae2a4492b990bca08ce399f8a431c58d92bebb37'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk25/30/GPL/openjdk-25-ea+30_linux-aarch64_bin.tar.gz'; 			downloadSha256='95be885f2e12ffb9ba3745dc29d8699a388c89f6826955aa9eb0c2f44a2d789b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 05 Jul 2025 00:48:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4447c51b3bde441b803aaaf0a684a8bbac02d7fce9167a7c1e87c313add07cf4`  
		Last Modified: Thu, 10 Jul 2025 23:23:17 GMT  
		Size: 48.1 MB (48085739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971f07a392e04b4b6e3af0d916043d20304174997e2490b9db70ba78668b2551`  
		Last Modified: Fri, 11 Jul 2025 00:13:53 GMT  
		Size: 38.5 MB (38493030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4706cbf8d74c55985fce1b99158bd08e899e1d0ea102b25b7f383a865dbdcccc`  
		Last Modified: Fri, 11 Jul 2025 07:10:47 GMT  
		Size: 220.9 MB (220858069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:25-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:336a26f5e7058ceccfa0c74f51e55fe956a74ee688c0dcb594a72390021d2b61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3659105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0657a674985496ae459b42cdf8708a89e4dd07cb40a4da9d30934ecb362bd5a3`

```dockerfile
```

-	Layers:
	-	`sha256:2a64de550e96e91f67af0e89e9114f63b23311046e87e393703027fe8dab65f6`  
		Last Modified: Fri, 11 Jul 2025 03:23:25 GMT  
		Size: 3.6 MB (3639072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da69069d9e4df003a0b4d2c0f873dc8e13674444bd09bb2e2f4fc38c67712600`  
		Last Modified: Fri, 11 Jul 2025 03:23:26 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json
