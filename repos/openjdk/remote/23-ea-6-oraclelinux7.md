## `openjdk:23-ea-6-oraclelinux7`

```console
$ docker pull openjdk@sha256:b540e6b7dcbc975b05d8370af6168855a9a13ab148abe8fdd190be71a1a43a70
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:23-ea-6-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:fcc3c0a2e87c84a3528ef7c5f54853552cd424c0585654f35c9e4959b840e6b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.7 MB (267675737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fd01d22671e64342a79288e11dfef5a8797d90d8728349eb72081b1d9c4d9c5`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Jan 2024 21:35:22 GMT
ADD file:bbd183ec68733730893e5ca4bc8673cc42d54ecec8fc30444474122a66c84dab in / 
# Wed, 17 Jan 2024 21:35:22 GMT
CMD ["/bin/bash"]
# Tue, 23 Jan 2024 20:18:23 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum # buildkit
# Tue, 23 Jan 2024 20:18:23 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Tue, 23 Jan 2024 20:18:23 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jan 2024 20:18:23 GMT
ENV LANG=en_US.UTF-8
# Tue, 23 Jan 2024 20:18:23 GMT
ENV JAVA_VERSION=23-ea+6
# Tue, 23 Jan 2024 20:18:23 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/6/GPL/openjdk-23-ea+6_linux-x64_bin.tar.gz'; 			downloadSha256='5163a8a077bfb1cb60e6b4ade06959b0ecba73399a509a5e83f8f9df5cebd140'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/6/GPL/openjdk-23-ea+6_linux-aarch64_bin.tar.gz'; 			downloadSha256='aa7e954bb29a17c5d0095c4ce94275bfe53383cb8aa7f14894d352e9c00110c8'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 23 Jan 2024 20:18:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5dd0ec2f99109a7ed9268ac1405fb9951743210620437ec13df10714ebe89b00`  
		Last Modified: Wed, 17 Jan 2024 21:37:41 GMT  
		Size: 50.4 MB (50385815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adeb265e503caf998c74f37673aef3b2acac5f793de4153e1088f49541f89ea`  
		Last Modified: Wed, 24 Jan 2024 20:50:20 GMT  
		Size: 14.2 MB (14232280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c2b03ddb3c0c9763323aed5e1c16d9bfbb00280bf635f7253e3ea1cafe417e`  
		Last Modified: Wed, 24 Jan 2024 20:50:24 GMT  
		Size: 203.1 MB (203057642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-6-oraclelinux7` - unknown; unknown

```console
$ docker pull openjdk@sha256:0752bb4802270b51b9ea70a8274c6d9c0ee4080dce33279419840d5dc9fd8b17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3785068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb98efbe1fd5c0ed1908fae8f765da8ea6762856e4943aef422bd671747395b`

```dockerfile
```

-	Layers:
	-	`sha256:a4c5f3a466bf9c7f311bd7651b6bd4d2d38bcf6d3b0a440c0aded1e2e0cab5be`  
		Last Modified: Wed, 24 Jan 2024 20:50:19 GMT  
		Size: 3.8 MB (3768682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e618f489e0aef99d5181194bddd4302cda5db908b2bc4db2ca94ba0607b6c31`  
		Last Modified: Wed, 24 Jan 2024 20:50:18 GMT  
		Size: 16.4 KB (16386 bytes)  
		MIME: application/vnd.in-toto+json
