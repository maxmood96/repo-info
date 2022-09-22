## `openjdk:18-oraclelinux7`

```console
$ docker pull openjdk@sha256:d4b0348e5717d1191085239481f2b2b843d9877cd8742245a05fedcb016b3df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `openjdk:18-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:67a797a81e8f0aeeb431baaaf6a1585a50015b946ccae0ffb369cd486bd1bd16
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.8 MB (252763656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ce790013e7e4482c27740d0935467aeb1f8539fd2a86563bd499748e611284`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 22 Sep 2022 18:21:00 GMT
ADD file:bc2c7ba728e9e4bfc9aa5e6072db4cbab3cadbd76aff485b6afd233dcdfbdb1e in / 
# Thu, 22 Sep 2022 18:21:00 GMT
CMD ["/bin/bash"]
# Thu, 22 Sep 2022 18:37:37 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 22 Sep 2022 18:38:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Thu, 22 Sep 2022 18:38:09 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Sep 2022 18:38:09 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Sep 2022 18:38:09 GMT
ENV JAVA_VERSION=18.0.2.1
# Thu, 22 Sep 2022 18:38:22 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.2.1/db379da656dc47308e138f21b33976fa/1/GPL/openjdk-18.0.2.1_linux-x64_bin.tar.gz'; 			downloadSha256='3bfdb59fc38884672677cebca9a216902d87fe867563182ae8bc3373a65a2ebd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.2.1/db379da656dc47308e138f21b33976fa/1/GPL/openjdk-18.0.2.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='79900237a5912045f8c9f1065b5204a474803cbbb4d075ab9620650fb75dfc1b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 22 Sep 2022 18:38:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a2a00260331c858dbb0d8dae185769162dbb3e7cb3342d52798d837e7a156c45`  
		Last Modified: Thu, 22 Sep 2022 18:21:50 GMT  
		Size: 49.8 MB (49796793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f00f9fe80a003e345fd0fbed09df87921267e2893a69170bde00961786a40f31`  
		Last Modified: Thu, 22 Sep 2022 18:40:40 GMT  
		Size: 14.2 MB (14223074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced9336e3101b6a75bc0047be4d9ef36c46f7ead26b6ce238ed1b4f03516dc8c`  
		Last Modified: Thu, 22 Sep 2022 18:41:47 GMT  
		Size: 188.7 MB (188743789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:18-oraclelinux7` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:0480320e43e14ce1c3e6f2cdc64c95efb56cf79ba26351ca70f0b78fc9e21fa3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.3 MB (253300992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd69e054ebd303f1ed3bc929a29602862ef0fca2e74adf98c66017f77b1c4c6`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 22 Sep 2022 18:41:04 GMT
ADD file:fd12a0d7821d135c61925e186ce7d33634745a38f1db7d39d2f06a27585fbeab in / 
# Thu, 22 Sep 2022 18:41:05 GMT
CMD ["/bin/bash"]
# Thu, 22 Sep 2022 19:00:03 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Thu, 22 Sep 2022 19:01:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Thu, 22 Sep 2022 19:01:15 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Sep 2022 19:01:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 22 Sep 2022 19:01:17 GMT
ENV JAVA_VERSION=18.0.2.1
# Thu, 22 Sep 2022 19:01:37 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.2.1/db379da656dc47308e138f21b33976fa/1/GPL/openjdk-18.0.2.1_linux-x64_bin.tar.gz'; 			downloadSha256='3bfdb59fc38884672677cebca9a216902d87fe867563182ae8bc3373a65a2ebd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.2.1/db379da656dc47308e138f21b33976fa/1/GPL/openjdk-18.0.2.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='79900237a5912045f8c9f1065b5204a474803cbbb4d075ab9620650fb75dfc1b'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 22 Sep 2022 19:01:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63b915e1b20e56956b453bc1d5b77fa94f0901ef3367114af0ce6baff9e507a3`  
		Last Modified: Thu, 22 Sep 2022 18:42:03 GMT  
		Size: 50.4 MB (50377925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c29288401cec214da58d603f66600fe99310ca836e0f5a37863ecb4d0cc448`  
		Last Modified: Thu, 22 Sep 2022 19:06:21 GMT  
		Size: 15.3 MB (15263714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b85456aa8979976263b578240ef04ac52be79f878d5bbd553b5e3bb3407cbc`  
		Last Modified: Thu, 22 Sep 2022 19:07:48 GMT  
		Size: 187.7 MB (187659353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
