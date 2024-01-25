## `openjdk:22-ea-32-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:9d020a85edc5e9fb4712b61e5019c52b9d544000a4d5516f79c1b9ca1dc92ecb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `openjdk:22-ea-32-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:05d750aea4565273601255427f128a03102509edff1005d2daa463b39e632c7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.4 MB (267385578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043c7824a93c8e5ecf3b47927a401f14b486a4d1cbfeba77d4f8408981c42998`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Jan 2024 21:35:22 GMT
ADD file:bbd183ec68733730893e5ca4bc8673cc42d54ecec8fc30444474122a66c84dab in / 
# Wed, 17 Jan 2024 21:35:22 GMT
CMD ["/bin/bash"]
# Tue, 23 Jan 2024 19:48:26 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum # buildkit
# Tue, 23 Jan 2024 19:48:26 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Tue, 23 Jan 2024 19:48:26 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Jan 2024 19:48:26 GMT
ENV LANG=en_US.UTF-8
# Tue, 23 Jan 2024 19:48:26 GMT
ENV JAVA_VERSION=22-ea+32
# Tue, 23 Jan 2024 19:48:26 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/32/GPL/openjdk-22-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='7ac0b8815f22c852796fa13b7680e07fa1dc340aa93f5e2bf1c5502337d952d6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk22/32/GPL/openjdk-22-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='7c565754b2926817c1779683d6b8f1975a94a8731fad35a670ea669a77aea182'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Tue, 23 Jan 2024 19:48:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5dd0ec2f99109a7ed9268ac1405fb9951743210620437ec13df10714ebe89b00`  
		Last Modified: Wed, 17 Jan 2024 21:37:41 GMT  
		Size: 50.4 MB (50385815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bed16d1b0ff6c7e778cd7245054aed3eb5b6f0c780d1e175cd48cd238cbda67`  
		Last Modified: Wed, 24 Jan 2024 20:50:16 GMT  
		Size: 14.2 MB (14232283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c2d5e4baa828db0b1ca1237866535bfb05b799124baa81d6c49ea1f7ce8b99`  
		Last Modified: Wed, 24 Jan 2024 20:50:20 GMT  
		Size: 202.8 MB (202767480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-32-jdk-oraclelinux7` - unknown; unknown

```console
$ docker pull openjdk@sha256:8d4c30c529d0aa6eef41f7c722303d130de72ea5bab15ce58c9e9c952d71d0e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3785093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3e456076419a1cf72a441ecfd69b5e7c5480acc58aee237e361cd7e30b674b`

```dockerfile
```

-	Layers:
	-	`sha256:271ff864065cdbcdc556f690f92355bc49f0b1f900f1240c856acf76bf911d41`  
		Last Modified: Wed, 24 Jan 2024 20:50:16 GMT  
		Size: 3.8 MB (3768690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21dee491f1c4e0d7dcdd1ff62cc688339d515d6b16bafbb3502908e7b709865e`  
		Last Modified: Wed, 24 Jan 2024 20:50:16 GMT  
		Size: 16.4 KB (16403 bytes)  
		MIME: application/vnd.in-toto+json
