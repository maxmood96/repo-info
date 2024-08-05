## `openjdk:24-ea-9-oraclelinux8`

```console
$ docker pull openjdk@sha256:7f63378382a16bc9ef61548fafebe791f05843ad46f5f99613665cf4b7442752
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:24-ea-9-oraclelinux8` - linux; amd64

```console
$ docker pull openjdk@sha256:844f529491e4e4844e6e32fa87dee74c221ee5111eb098ba6b6e7457518bb645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.4 MB (278448989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c08d32c1a61688d303e85718e643b10e87c80baddb86b9f523514eab896e9d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 03 Jul 2024 23:20:38 GMT
ADD file:789b4bad3c8ec49deaec755e6ce00146287ec0b8dd5361181f491244ef0c5901 in / 
# Wed, 03 Jul 2024 23:20:38 GMT
CMD ["/bin/bash"]
# Fri, 02 Aug 2024 18:51:57 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 02 Aug 2024 18:51:57 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 02 Aug 2024 18:51:57 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Aug 2024 18:51:57 GMT
ENV LANG=C.UTF-8
# Fri, 02 Aug 2024 18:51:57 GMT
ENV JAVA_VERSION=24-ea+9
# Fri, 02 Aug 2024 18:51:57 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/9/GPL/openjdk-24-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='5dd8d67a4e4059d22eb6fe7c636bf7610832380061f522aec631b69fdbaba6ae'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/9/GPL/openjdk-24-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='ef04b828af0fa6aca544841b01f5efda63143b81f52f1f69b2b5cf46953713a7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Aug 2024 18:51:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:46ed4d5ee531c13affa3e9cde2a49eff959d69e21ccfb79df05d6d268512b8b9`  
		Last Modified: Wed, 03 Jul 2024 23:21:44 GMT  
		Size: 51.2 MB (51219624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a3fc4fdd25fc29b8acd6cbec61215047f36da0489a8e740d2ae14aafeb2a67`  
		Last Modified: Mon, 05 Aug 2024 18:58:29 GMT  
		Size: 15.0 MB (15036067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90590122321e3bcdb108924f5e409f178e46fa067a065954ad623ca4a2fd3fe`  
		Last Modified: Mon, 05 Aug 2024 18:58:31 GMT  
		Size: 212.2 MB (212193298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-9-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:6c2f86e0e66b95d402a7b0a0637b20728510e44964757954619ca1dcf6360b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df424bf85f82885e50639c973d92e0ffb6b4157cf2e88c967eab4f5305a85f5a`

```dockerfile
```

-	Layers:
	-	`sha256:67ed29b3f5a848f81ca192432ad055453bb6474e4078b3af490c51c3f342c7ed`  
		Last Modified: Mon, 05 Aug 2024 18:58:28 GMT  
		Size: 2.3 MB (2287817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bec5d6690e666b6ebe2312fe32508d708f13e30dd2f1d8aee233e39217ffcedd`  
		Last Modified: Mon, 05 Aug 2024 18:58:28 GMT  
		Size: 15.8 KB (15803 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-9-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:ef46731dd3f2cebffea62effedc710f0b58e6cc3d6fa645c849a9ac0b124523b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.7 MB (275671069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:115d480d4113a2703b32e139833a7be984b0e6ba4c24a2cb10e2d092c078646c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 03 Jul 2024 22:40:38 GMT
ADD file:9ac31171a67dc91bfde196a3549d21aab3aa264cb150e7566ad688937a369f22 in / 
# Wed, 03 Jul 2024 22:40:39 GMT
CMD ["/bin/bash"]
# Fri, 02 Aug 2024 18:51:57 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 02 Aug 2024 18:51:57 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 02 Aug 2024 18:51:57 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Aug 2024 18:51:57 GMT
ENV LANG=C.UTF-8
# Fri, 02 Aug 2024 18:51:57 GMT
ENV JAVA_VERSION=24-ea+9
# Fri, 02 Aug 2024 18:51:57 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/9/GPL/openjdk-24-ea+9_linux-x64_bin.tar.gz'; 			downloadSha256='5dd8d67a4e4059d22eb6fe7c636bf7610832380061f522aec631b69fdbaba6ae'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/9/GPL/openjdk-24-ea+9_linux-aarch64_bin.tar.gz'; 			downloadSha256='ef04b828af0fa6aca544841b01f5efda63143b81f52f1f69b2b5cf46953713a7'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 02 Aug 2024 18:51:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f6708363575e82894d4714b00358e6cfc904f5e8213ff218080d18d8c0a3aea8`  
		Last Modified: Wed, 03 Jul 2024 22:41:29 GMT  
		Size: 49.9 MB (49925030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca345db69d5fd49f13cb0fd444dd21dc5576cd6587605dd8acb1793f7ebac2b`  
		Last Modified: Mon, 29 Jul 2024 16:57:55 GMT  
		Size: 15.7 MB (15686119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e72d88d527b9c99ea6d6c3bc20e9e596a0c38d4d931ec6ce055f7c8eac8b969`  
		Last Modified: Mon, 05 Aug 2024 19:07:20 GMT  
		Size: 210.1 MB (210059920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-9-oraclelinux8` - unknown; unknown

```console
$ docker pull openjdk@sha256:4b2597f90cc778117f3981549465aab43982ed35900770c197946a42859d66d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f44a18e378f949cb21b99f20d143d56fc4206109b14c1ce7879aa68e265752`

```dockerfile
```

-	Layers:
	-	`sha256:b2507af29073f5b4aa297e4c207099de7a13e80e29484403c2e556b99edbab75`  
		Last Modified: Mon, 05 Aug 2024 19:07:16 GMT  
		Size: 2.3 MB (2287286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9a105881038a493ede12f684e7297b65221a888a4c81e774dbddf220d79091f`  
		Last Modified: Mon, 05 Aug 2024 19:07:15 GMT  
		Size: 16.1 KB (16134 bytes)  
		MIME: application/vnd.in-toto+json
