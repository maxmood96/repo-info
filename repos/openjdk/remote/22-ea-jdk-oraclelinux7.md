## `openjdk:22-ea-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:ef130b2a3e0da2c13ddc9db382b5f2a1a524f91fc5cb5c182684af4ef8f30466
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-ea-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:91045748547f8419534cae4989fd1f385f7916b34754bb7ff8932088d13cae5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.4 MB (267386238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d5d827b7fd0b08b5db6f6c59feb44d711971fa3db56928d7fa707d839953c9`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Jan 2024 21:35:22 GMT
ADD file:bbd183ec68733730893e5ca4bc8673cc42d54ecec8fc30444474122a66c84dab in / 
# Wed, 17 Jan 2024 21:35:22 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 19:48:11 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum # buildkit
# Fri, 02 Feb 2024 19:48:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 02 Feb 2024 19:48:11 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:48:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 Feb 2024 19:48:11 GMT
ENV JAVA_VERSION=22-ea+34
# Fri, 02 Feb 2024 19:48:11 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/34/GPL/openjdk-22-ea+34_linux-x64_bin.tar.gz'; 			downloadSha256='170b7192de3e30c796b95d765b12ca457d3f4b05e97bee0bf81709c8b43cd992'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/34/GPL/openjdk-22-ea+34_linux-aarch64_bin.tar.gz'; 			downloadSha256='63460b6a2c4d547d7a8cf4cf86d67a46f5e6a96a62843a787a2aabdbed4df119'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Feb 2024 19:48:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5dd0ec2f99109a7ed9268ac1405fb9951743210620437ec13df10714ebe89b00`  
		Last Modified: Wed, 17 Jan 2024 21:37:41 GMT  
		Size: 50.4 MB (50385815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d48026f7592dba84c123b4d791caf5f637314b217556b91eabd140588a82fc`  
		Last Modified: Fri, 02 Feb 2024 22:53:48 GMT  
		Size: 14.2 MB (14232290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c9bc001a349e7dc6dff6c9e5f85a2cf9aacebf9ffd731889db9ebd99f147a52`  
		Last Modified: Fri, 02 Feb 2024 22:53:52 GMT  
		Size: 202.8 MB (202768133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-jdk-oraclelinux7` - unknown; unknown

```console
$ docker pull openjdk@sha256:9a6d045ae35ccae502d08d19dde326a10530a045e21ad59098c31434639e1da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3785100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996d56fdcbb80fbb4c0eb40028cc2f5967281b964117328703e09ce57f9c9379`

```dockerfile
```

-	Layers:
	-	`sha256:6f4a72dc23bc4dc2550a70d86e0e65f5db7ad4746c2ea4385e173248765c42bc`  
		Last Modified: Fri, 02 Feb 2024 22:53:48 GMT  
		Size: 3.8 MB (3768697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:812816bc3b9fb22f208466c1bb8deb1c5c8b769ed2cf2d4176d29632dfa8893b`  
		Last Modified: Fri, 02 Feb 2024 22:53:48 GMT  
		Size: 16.4 KB (16403 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-ea-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3daabdc3aca95638e7f29029e3f1aca8f0bb6b4f669393c3b0eb5287d95bd88a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.1 MB (267078187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9da15d90ab2de5adc27d7d87e3fdbdecc0c7df01f8b3babad0a750719f89a25`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Jan 2024 22:08:17 GMT
ADD file:8e4f54dbc6703a8208e63085c4e5598de223be1f27406807e223bc6ef121c4cf in / 
# Wed, 17 Jan 2024 22:08:18 GMT
CMD ["/bin/bash"]
# Fri, 26 Jan 2024 01:48:32 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum # buildkit
# Fri, 26 Jan 2024 01:48:32 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 26 Jan 2024 01:48:32 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Jan 2024 01:48:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jan 2024 01:48:32 GMT
ENV JAVA_VERSION=22-ea+33
# Fri, 26 Jan 2024 01:48:32 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/33/GPL/openjdk-22-ea+33_linux-x64_bin.tar.gz'; 			downloadSha256='585ce01cf4908a98290ff33cc072d8733a012a58cb13a25304904bdb03c5e751'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/33/GPL/openjdk-22-ea+33_linux-aarch64_bin.tar.gz'; 			downloadSha256='1df9746a0ac9f82fa421e32e0eaa4347dd657d612ca3e414c50b7e689ad59b43'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 26 Jan 2024 01:48:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:963289c7c202b6b90d04fa4c851434fe886f6eaf9d3f3cd608dd53d3616791ea`  
		Last Modified: Wed, 17 Jan 2024 22:10:14 GMT  
		Size: 51.0 MB (51000317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42a06ab66b43a901c035f28bcf7a5d44201a1d0f6130c5d26dcce4d2d409c86`  
		Last Modified: Sat, 27 Jan 2024 20:34:04 GMT  
		Size: 15.3 MB (15258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c468006674b489e1070b98ebad8f544070a6a77ae8a0376159f0f7c3c2613700`  
		Last Modified: Sat, 27 Jan 2024 20:39:41 GMT  
		Size: 200.8 MB (200819851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-jdk-oraclelinux7` - unknown; unknown

```console
$ docker pull openjdk@sha256:16b7ddf954e80813c1f36e332d3da74f76f07d876c089e66836c6dff99fc893f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3780806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa5d7c779f6fec0ac26586f435394a1e058b5549c1a600e134762e88150b2af`

```dockerfile
```

-	Layers:
	-	`sha256:0e5616a28036561a3fedd837ca785b1f41df28cdaede9723d465cfc26aa34763`  
		Last Modified: Sat, 27 Jan 2024 20:39:37 GMT  
		Size: 3.8 MB (3764557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c32862a218ade6d16cfa4ee7617a53452aacb1a8c1925d5b574ac97e9014c36f`  
		Last Modified: Sat, 27 Jan 2024 20:39:36 GMT  
		Size: 16.2 KB (16249 bytes)  
		MIME: application/vnd.in-toto+json
