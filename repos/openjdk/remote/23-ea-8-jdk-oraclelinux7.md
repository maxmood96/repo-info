## `openjdk:23-ea-8-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:2d9fc333de8af4d9bf3c7060dec07abd5743b337238840f4d53186ce2d110413
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-8-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:47194eb901c37d753a78d412609ebc688621da32019163c006be3a2dbef20167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.8 MB (267760880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:680ff99df94a8e37323da7166fb1e5776469a2af167e7c75803b486a4dda8817`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 02 Feb 2024 19:54:38 GMT
ADD file:6c43f1bc1b598f7b1a5fc6f5c7951e8525eee01704f8f5e5caec8a944a4ecb4d in / 
# Fri, 02 Feb 2024 19:54:38 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 19:54:38 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum # buildkit
# Fri, 02 Feb 2024 19:54:38 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 02 Feb 2024 19:54:38 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:54:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 Feb 2024 19:54:38 GMT
ENV JAVA_VERSION=23-ea+8
# Fri, 02 Feb 2024 19:54:38 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/8/GPL/openjdk-23-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='3f36f003a7dbc52c00e66678dfd2c190be7939f729e85db1848911f3f3e61704'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/8/GPL/openjdk-23-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='a216441b0aeba416ff109cf7eb4337ce00c7f4eba5e77b0b45a1b79cde736690'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Feb 2024 19:54:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ff90099b5a4df32952d1822d472a72c931c53a68c05a3ba7431ea0f85d54135`  
		Last Modified: Wed, 14 Feb 2024 01:50:04 GMT  
		Size: 50.4 MB (50389833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a33cf30653839495d72a11b505d12eea60c96844ba9b1ee542a6b00705b452a`  
		Last Modified: Wed, 14 Feb 2024 02:55:55 GMT  
		Size: 14.2 MB (14231542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9424708221356c36d446ca9dfa7d42bb909a2661e6366a18a1bafa3ef9ffaa`  
		Last Modified: Wed, 14 Feb 2024 02:56:00 GMT  
		Size: 203.1 MB (203139505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-8-jdk-oraclelinux7` - unknown; unknown

```console
$ docker pull openjdk@sha256:886b896029bdb700e32785a2e3cf5be4a8f65ddab44f93da4303d7520b849050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3785075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1283dac4ab1430185b5fcc2252a4b2da2a64b1e87cd51ee8c4910f5fedb32c6`

```dockerfile
```

-	Layers:
	-	`sha256:1198a4b52a4615a722888a793ee06fdcaf010b6645d0ccddd9d8f355b1b895bf`  
		Last Modified: Wed, 14 Feb 2024 02:55:54 GMT  
		Size: 3.8 MB (3768689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dae64e7a6137f3838899615f8c7e3b1502f6a7437202be406472ba4c5c2c0eb0`  
		Last Modified: Wed, 14 Feb 2024 02:55:54 GMT  
		Size: 16.4 KB (16386 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-8-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:42ebb68884dbdcf28f9d9d5f30a79e4a9dea5a6018874d13988b4d2621263eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.3 MB (267280271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:022bc6cde49d33c8329aa3f51a35b97801d5df5b27eee1e37b9609e1719f230a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Jan 2024 22:08:17 GMT
ADD file:8e4f54dbc6703a8208e63085c4e5598de223be1f27406807e223bc6ef121c4cf in / 
# Wed, 17 Jan 2024 22:08:18 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 19:54:38 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum # buildkit
# Fri, 02 Feb 2024 19:54:38 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 02 Feb 2024 19:54:38 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Feb 2024 19:54:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 Feb 2024 19:54:38 GMT
ENV JAVA_VERSION=23-ea+8
# Fri, 02 Feb 2024 19:54:38 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/8/GPL/openjdk-23-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='3f36f003a7dbc52c00e66678dfd2c190be7939f729e85db1848911f3f3e61704'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/8/GPL/openjdk-23-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='a216441b0aeba416ff109cf7eb4337ce00c7f4eba5e77b0b45a1b79cde736690'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Feb 2024 19:54:38 GMT
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
	-	`sha256:5c3bd9ca8328f4b928fe3ab934c69ab9959cca7f839096156313ea39e79da9a0`  
		Last Modified: Sat, 03 Feb 2024 12:40:59 GMT  
		Size: 201.0 MB (201021935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-8-jdk-oraclelinux7` - unknown; unknown

```console
$ docker pull openjdk@sha256:5bdee935f650155e02bc80e874561862bc9a735e1b51cbf6adc5783b43ff7918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3780793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79a3cdcaf4a0696a2cdbb79fca2575320cbe1b7e31c0290509b365a461de4597`

```dockerfile
```

-	Layers:
	-	`sha256:fc2ec2e108a3e06ddaf6634b9739b38d3f3edfb0f8c1b345e1755292406519f0`  
		Last Modified: Sat, 03 Feb 2024 12:40:55 GMT  
		Size: 3.8 MB (3764560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a4e9b0bd4626a93eda6bf1556ffd995c7093de8d5c1ae7d01ade1ef1d22db05`  
		Last Modified: Sat, 03 Feb 2024 12:40:55 GMT  
		Size: 16.2 KB (16233 bytes)  
		MIME: application/vnd.in-toto+json
