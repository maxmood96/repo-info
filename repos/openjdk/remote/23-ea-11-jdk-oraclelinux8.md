## `openjdk:23-ea-11-jdk-oraclelinux8`

```console
$ docker pull openjdk@sha256:7e1b300a009123aeeee00b5d30d602e706382854964308ec522a80bfe5e5ab6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:23-ea-11-jdk-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:ebb61f5d0d7719532bdc0f3ead37919c5836439982622ad93aae829fd99b42fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269435499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc35225ca1006a2801e7bb41e74dc66d1a8f66063534c28f8d8f49b7dc47d19d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Feb 2024 01:47:16 GMT
ADD file:cbc540158e77b85113e3a0e0ed1e202046cf293cdb8d7cd890b04883493dbf35 in / 
# Wed, 14 Feb 2024 01:47:16 GMT
CMD ["/bin/bash"]
# Fri, 23 Feb 2024 07:48:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 23 Feb 2024 07:48:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 23 Feb 2024 07:48:15 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 07:48:15 GMT
ENV LANG=C.UTF-8
# Fri, 23 Feb 2024 07:48:15 GMT
ENV JAVA_VERSION=23-ea+11
# Fri, 23 Feb 2024 07:48:15 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/11/GPL/openjdk-23-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='e297d7f6d296a96d9b3c30a8ab90ab911fb920560690f4b77168b6b6fbde162c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/11/GPL/openjdk-23-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='a5d67060b45e0752b89e71a8d98a36978ac8528efbc12eaded427ea8c0f69b90'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 23 Feb 2024 07:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:81badc5f380f1ca21f6c430303f4107b9b5e0af27c59e3725bf731915b457fc8`  
		Last Modified: Wed, 14 Feb 2024 01:49:17 GMT  
		Size: 51.3 MB (51325575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f80a11cfe821a0f2aeeaeff63f97f9edb94e9b24dcae5bdb5125d58fce0f75`  
		Last Modified: Fri, 23 Feb 2024 18:51:32 GMT  
		Size: 15.0 MB (15005900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fceab7a7fa99d09305a91580225e608758bb8b1ddb1ee668d90bdb3c980f99bf`  
		Last Modified: Fri, 23 Feb 2024 18:51:36 GMT  
		Size: 203.1 MB (203104024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-11-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:a70677f0bcd2cb05e3454a2b5a73c357cf9e270880c93d04e459d8ac6af654e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2291093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be926a06b2a2c5fab291bd5a3b4f8268eb77c174ccc8fb87a45ceade05a35b55`

```dockerfile
```

-	Layers:
	-	`sha256:2b520a871d27eaff3634f13140bdc61a579e649df2dbeecd2dd9aa2cce0b3aa8`  
		Last Modified: Fri, 23 Feb 2024 18:51:31 GMT  
		Size: 2.3 MB (2271204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:235ab52a59a5d345fce57492533618b48d279b220af5c7510a7b1a9a42ae9b12`  
		Last Modified: Fri, 23 Feb 2024 18:51:31 GMT  
		Size: 19.9 KB (19889 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:23-ea-11-jdk-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0103e9e69bc529db91a5a7aa5103cbedcc0629d076afa18f45c920e08cf2eed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.8 MB (266767478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c7e6b7f76fb3df8966a3197c24401f5f9e4c2a37ecae6890428324fe679275`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Feb 2024 01:44:45 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Wed, 14 Feb 2024 01:44:46 GMT
CMD ["/bin/bash"]
# Fri, 23 Feb 2024 07:48:15 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 23 Feb 2024 07:48:15 GMT
ENV JAVA_HOME=/usr/java/openjdk-23
# Fri, 23 Feb 2024 07:48:15 GMT
ENV PATH=/usr/java/openjdk-23/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 23 Feb 2024 07:48:15 GMT
ENV LANG=C.UTF-8
# Fri, 23 Feb 2024 07:48:15 GMT
ENV JAVA_VERSION=23-ea+11
# Fri, 23 Feb 2024 07:48:15 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/11/GPL/openjdk-23-ea+11_linux-x64_bin.tar.gz'; 			downloadSha256='e297d7f6d296a96d9b3c30a8ab90ab911fb920560690f4b77168b6b6fbde162c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk23/11/GPL/openjdk-23-ea+11_linux-aarch64_bin.tar.gz'; 			downloadSha256='a5d67060b45e0752b89e71a8d98a36978ac8528efbc12eaded427ea8c0f69b90'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 23 Feb 2024 07:48:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5b1d3eb6a012567065354e86eb0bac67a32e425e65bc6fe8b5cd84b95a0643`  
		Last Modified: Wed, 14 Feb 2024 11:04:46 GMT  
		Size: 15.7 MB (15691290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a95e47ef295f8bc9ed57f24adb2f7168cf709502aabc269e9d9ca54aec0f9ea`  
		Last Modified: Fri, 23 Feb 2024 19:01:55 GMT  
		Size: 201.0 MB (201003274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:23-ea-11-jdk-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:4c5fe71966627d65ec1a30dee1676b6b2d0fa65ee31a6fbf61ba7b81a7ab5be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2289433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2d0250880f04c4a7860b134e16d017fb031b87cb68d48806b3fc5a53704d0f`

```dockerfile
```

-	Layers:
	-	`sha256:51979b48aeb3938bf454d0b357c32e7ac7ec2f100f891ab3eb48ef1188101b5a`  
		Last Modified: Fri, 23 Feb 2024 19:01:51 GMT  
		Size: 2.3 MB (2269674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2047fb0f2fe52a3605cc567ac51df21c154856d754ef9575f634c16bc1e4b079`  
		Last Modified: Fri, 23 Feb 2024 19:01:50 GMT  
		Size: 19.8 KB (19759 bytes)  
		MIME: application/vnd.in-toto+json
