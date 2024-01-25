## `openjdk:22-ea-32-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:447b94680b5f483d84b049ef3a6475e7102c4ee77a483173423c751bcebcc659
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
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

### `openjdk:22-ea-32-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:9d40dad6fe46c57818ad17ee8879c5d50f2a7e6855e4fa43e7d8ed309cd765c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.1 MB (267078019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:540d6abbed3cd7f835f3991b83b6dcd5029683fad5970f6e19218b35b68927e1`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Jan 2024 22:08:17 GMT
ADD file:8e4f54dbc6703a8208e63085c4e5598de223be1f27406807e223bc6ef121c4cf in / 
# Wed, 17 Jan 2024 22:08:18 GMT
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
	-	`sha256:963289c7c202b6b90d04fa4c851434fe886f6eaf9d3f3cd608dd53d3616791ea`  
		Last Modified: Wed, 17 Jan 2024 22:10:14 GMT  
		Size: 51.0 MB (51000317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385c41166173f9457fc478a9d47f500342a45b6725b38dbcfe193311857a8963`  
		Last Modified: Thu, 18 Jan 2024 10:43:55 GMT  
		Size: 15.3 MB (15257951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215a9e5f8bf44551dd7fee25bcbfc623738dba189f0c4328f3df99b16325e285`  
		Last Modified: Thu, 25 Jan 2024 04:31:18 GMT  
		Size: 200.8 MB (200819751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-ea-32-jdk-oraclelinux7` - unknown; unknown

```console
$ docker pull openjdk@sha256:a50a03bbcd5bfcc52ef6aec01117e80d995e1dbc16e08cf0031a0216a37a85eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3780807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7e0b2ff23cde5fdc20ca1f9a6be0191e6986b8385e3aa47f5bdc49e048c44b`

```dockerfile
```

-	Layers:
	-	`sha256:18431f5e5602b48377094040609116f4a977db79bac6552280c239244ce4088d`  
		Last Modified: Thu, 25 Jan 2024 04:31:12 GMT  
		Size: 3.8 MB (3764557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eb1979ef02a000c507eb59b0c1d924e6999953b1ccc47b561578bfb022bee37`  
		Last Modified: Thu, 25 Jan 2024 04:31:12 GMT  
		Size: 16.2 KB (16250 bytes)  
		MIME: application/vnd.in-toto+json
