## `openjdk:22-ea-34-oraclelinux7`

```console
$ docker pull openjdk@sha256:cd829b51ccbf468ff7770d1b3e22ed096d31bfca641e3074bed16bd73d629e90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:22-ea-34-oraclelinux7` - linux; amd64

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

### `openjdk:22-ea-34-oraclelinux7` - unknown; unknown

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
