## `openjdk:22-rc-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:ab3f5d2b4782cde8a78321356ae1ff7509f724bb8bb63797dff5cb2107328773
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `openjdk:22-rc-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:ac037232fdaab6fa2652b7e7482eae9420a8709591ce82154107be6e53d4b983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.4 MB (267386091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f99ff5da9cdcace3b274b5df5f0347216a7d1a588b8162024c3ef54a2431c6da`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 09 Feb 2024 19:48:12 GMT
ADD file:6c43f1bc1b598f7b1a5fc6f5c7951e8525eee01704f8f5e5caec8a944a4ecb4d in / 
# Fri, 09 Feb 2024 19:48:12 GMT
CMD ["/bin/bash"]
# Fri, 09 Feb 2024 19:48:12 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum # buildkit
# Fri, 09 Feb 2024 19:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 09 Feb 2024 19:48:12 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Feb 2024 19:48:12 GMT
ENV LANG=en_US.UTF-8
# Fri, 09 Feb 2024 19:48:12 GMT
ENV JAVA_VERSION=22
# Fri, 09 Feb 2024 19:48:12 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/35/GPL/openjdk-22_linux-x64_bin.tar.gz'; 			downloadSha256='37b0e1d93e9b6478824c21753f2e8445c8caad885a2245f393b35658be1695b3'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/35/GPL/openjdk-22_linux-aarch64_bin.tar.gz'; 			downloadSha256='5bc8c3ea634bf3be8a275c789dabbaa3e68eb639ee920b6fbce1b2236082086d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 09 Feb 2024 19:48:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ff90099b5a4df32952d1822d472a72c931c53a68c05a3ba7431ea0f85d54135`  
		Last Modified: Wed, 14 Feb 2024 01:50:04 GMT  
		Size: 50.4 MB (50389833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2366487f2b2cd85f083af7430006a562bfabc8902ee38751f8560e0fce50250`  
		Last Modified: Wed, 14 Feb 2024 02:55:53 GMT  
		Size: 14.2 MB (14231536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3067bbb412f0ed70cdf03a477af7fe34e262cd8f18f95426ec7fe1550f4a2f8b`  
		Last Modified: Wed, 14 Feb 2024 02:55:56 GMT  
		Size: 202.8 MB (202764722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-rc-jdk-oraclelinux7` - unknown; unknown

```console
$ docker pull openjdk@sha256:5690d3bb6c9da5702c641f2a20268cf0aece5010956133054639a7ed9b8cb2b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3783815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eea8cc51b88d4b8fd74439a8718ee7ca7f6b4fc3c7b301fc3f33eb7a7e2844dc`

```dockerfile
```

-	Layers:
	-	`sha256:b846bb2ac9a5b2e3c6e372972c4684a4f8d732a63894e76c1bf6b79f18e410a7`  
		Last Modified: Wed, 14 Feb 2024 02:55:52 GMT  
		Size: 3.8 MB (3768017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c129489bfebcffa276b9a990226f8d8cb83dfe19e395a76909732c8944b53a3`  
		Last Modified: Wed, 14 Feb 2024 02:55:52 GMT  
		Size: 15.8 KB (15798 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:22-rc-jdk-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:910b15229f33f8dac0e75321016a14fee29cdc5c9218bdae1539a87dab0c5b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.1 MB (267076346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14f469ab7f97308106a089d9b4eb63d6e069b39afea47ef955dcfa985bfdaf72`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Jan 2024 22:08:17 GMT
ADD file:8e4f54dbc6703a8208e63085c4e5598de223be1f27406807e223bc6ef121c4cf in / 
# Wed, 17 Jan 2024 22:08:18 GMT
CMD ["/bin/bash"]
# Fri, 09 Feb 2024 19:48:12 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum # buildkit
# Fri, 09 Feb 2024 19:48:12 GMT
ENV JAVA_HOME=/usr/java/openjdk-22
# Fri, 09 Feb 2024 19:48:12 GMT
ENV PATH=/usr/java/openjdk-22/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Feb 2024 19:48:12 GMT
ENV LANG=en_US.UTF-8
# Fri, 09 Feb 2024 19:48:12 GMT
ENV JAVA_VERSION=22
# Fri, 09 Feb 2024 19:48:12 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/35/GPL/openjdk-22_linux-x64_bin.tar.gz'; 			downloadSha256='37b0e1d93e9b6478824c21753f2e8445c8caad885a2245f393b35658be1695b3'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk22/830ec9fcccef480bb3e73fb7ecafe059/35/GPL/openjdk-22_linux-aarch64_bin.tar.gz'; 			downloadSha256='5bc8c3ea634bf3be8a275c789dabbaa3e68eb639ee920b6fbce1b2236082086d'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 09 Feb 2024 19:48:12 GMT
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
	-	`sha256:16b9c98caa8fb27b5e3193214b82b6e2bbe5ead093126d9cfe128c147495acb6`  
		Last Modified: Tue, 13 Feb 2024 00:30:59 GMT  
		Size: 200.8 MB (200818010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:22-rc-jdk-oraclelinux7` - unknown; unknown

```console
$ docker pull openjdk@sha256:e036a6c5163f06dc0150fd8730d0cca61142e254e1aa6e62ab82b251020c0aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3780482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b16d4e93743aed2959c395d4e3010762ddeb92ddbcd7aad2b61a5b2b84bc65e`

```dockerfile
```

-	Layers:
	-	`sha256:8951e48518cbd54beebbec1728b8eb305490ebdff19f2ff25bddb8f83fafe7d9`  
		Last Modified: Tue, 13 Feb 2024 00:30:55 GMT  
		Size: 3.8 MB (3764840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d288ba5e4792858ff6c802f3ac62341c6745c11c30a56be498ece5a5297aa3ad`  
		Last Modified: Tue, 13 Feb 2024 00:30:54 GMT  
		Size: 15.6 KB (15642 bytes)  
		MIME: application/vnd.in-toto+json
