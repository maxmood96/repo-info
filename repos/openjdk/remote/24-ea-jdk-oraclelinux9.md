## `openjdk:24-ea-jdk-oraclelinux9`

```console
$ docker pull openjdk@sha256:c3e26ccc7d4eb05a96c91c262b994b053e436937cfe5690b00ef02ca51d9d989
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-jdk-oraclelinux9` - linux; amd64

```console
$ docker pull openjdk@sha256:61950483f4ec62aef3a986e1b214b738cd06cced5a092e1b0efaba97d440add7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.2 MB (298171702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:252317e09d7600a6f7973b38b43516f6a9df28d84554ef494adf5a4770b15623`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 01 Jun 2024 00:47:59 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Sat, 01 Jun 2024 00:48:00 GMT
CMD ["/bin/bash"]
# Thu, 13 Jun 2024 18:54:09 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 13 Jun 2024 18:54:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Thu, 13 Jun 2024 18:54:09 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 18:54:09 GMT
ENV LANG=C.UTF-8
# Thu, 13 Jun 2024 18:54:09 GMT
ENV JAVA_VERSION=24-ea+2
# Thu, 13 Jun 2024 18:54:09 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/2/GPL/openjdk-24-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='5219b8df6c8c43be5dab2d1ab5251df85610360ab22789e497ee05c66fa4c7e6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/2/GPL/openjdk-24-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='5632c71df051ca5b6640c3c2a09ca3dd2b3dd131ea632906bd0eef7033323223'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 13 Jun 2024 18:54:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5529165bc563c3caa689fecba5e2ec431c7ffad2d9991834a099da7933355b`  
		Last Modified: Fri, 14 Jun 2024 01:01:19 GMT  
		Size: 37.9 MB (37862639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51c963449bf02511865fb07969c2d4847d9a490f614893bc1607199a78f7a8e`  
		Last Modified: Fri, 14 Jun 2024 01:01:22 GMT  
		Size: 211.3 MB (211314185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:574fb78ccb772cc6d00a1a87bc00601b1f426a9b47219bf15d12e01dfb4ca90e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3352730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6124162166392cb06e145ef1a82734d66adf87777f3585f117555bcc880cfeb5`

```dockerfile
```

-	Layers:
	-	`sha256:994e304807e492659411d6a06fd7cc01ceb0f2e6cf46d4a8a2e2032ae7f800f6`  
		Last Modified: Fri, 14 Jun 2024 01:01:19 GMT  
		Size: 3.3 MB (3333227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:229a0c96e7ce249e7aa3528cb34ba87bd2b20e11d7a5bb6012575a0f1f9013f6`  
		Last Modified: Fri, 14 Jun 2024 01:01:19 GMT  
		Size: 19.5 KB (19503 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-jdk-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:301e88286e122afa8f360404e5f4eac1c68b2e123c28b874dd629863925b5320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295107781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9bb6b64f890b4159d8f537201ea131d578cdf753459f876217149474838395`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 01 Jun 2024 01:47:52 GMT
ADD file:e2d1c7a0eab3573f307b1affb1e88a1c24614b2ec92eb17723bc07cfa2083423 in / 
# Sat, 01 Jun 2024 01:47:53 GMT
CMD ["/bin/bash"]
# Thu, 13 Jun 2024 18:54:09 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 13 Jun 2024 18:54:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Thu, 13 Jun 2024 18:54:09 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 13 Jun 2024 18:54:09 GMT
ENV LANG=C.UTF-8
# Thu, 13 Jun 2024 18:54:09 GMT
ENV JAVA_VERSION=24-ea+2
# Thu, 13 Jun 2024 18:54:09 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/2/GPL/openjdk-24-ea+2_linux-x64_bin.tar.gz'; 			downloadSha256='5219b8df6c8c43be5dab2d1ab5251df85610360ab22789e497ee05c66fa4c7e6'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/2/GPL/openjdk-24-ea+2_linux-aarch64_bin.tar.gz'; 			downloadSha256='5632c71df051ca5b6640c3c2a09ca3dd2b3dd131ea632906bd0eef7033323223'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 13 Jun 2024 18:54:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:da7a98631edf9304544ff835ff2891b9c7a6773ae8a8bbd8041b6ef3af01fae9`  
		Last Modified: Sat, 01 Jun 2024 01:49:25 GMT  
		Size: 47.7 MB (47651991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4126ceeefbe5a1d06272578a6b6a99a1d422489b25511cbccbaaeb1576551bfd`  
		Last Modified: Sun, 02 Jun 2024 01:54:26 GMT  
		Size: 38.3 MB (38259157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c687af639c87d37909583fc0e83aeda6191345dd8c8e80cba9f43c5977d240`  
		Last Modified: Fri, 14 Jun 2024 04:04:23 GMT  
		Size: 209.2 MB (209196633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk-oraclelinux9` - unknown; unknown

```console
$ docker pull openjdk@sha256:345e89fd92f3f26698d8474b0b02030bbcf49bd4d5288001ec5b881a5f710140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3351588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:900c9e8f6c401b923c576b6fa1c66338f11678afbdece8327c517bfe6c8e5c8a`

```dockerfile
```

-	Layers:
	-	`sha256:193a205e6b43e4830a84b685c8a0459e944880f5ac1734a7a71f531a70f1042a`  
		Last Modified: Fri, 14 Jun 2024 04:04:17 GMT  
		Size: 3.3 MB (3331610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:454cf33d6e04386056b9cb107fa0e92490344750a7ef094dea5e240d4f56b2c0`  
		Last Modified: Fri, 14 Jun 2024 04:04:17 GMT  
		Size: 20.0 KB (19978 bytes)  
		MIME: application/vnd.in-toto+json
