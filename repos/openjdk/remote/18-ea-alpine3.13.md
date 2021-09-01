## `openjdk:18-ea-alpine3.13`

```console
$ docker pull openjdk@sha256:c20a0ddb084ae5a7e3647f960471446ea610057eccc026dadaab49a72e657671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `openjdk:18-ea-alpine3.13` - linux; amd64

```console
$ docker pull openjdk@sha256:d2b58158c7c5b57707465ff02adc14de2023cd8e142a27a0a9b3031e88a57d25
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192442129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1deb514118a7e9a08079f09c1a0fb7c834fd2253c3a7f5e2471f795b93fbd5f9`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 05:22:56 GMT
RUN apk add --no-cache java-cacerts
# Wed, 01 Sep 2021 05:22:56 GMT
ENV JAVA_HOME=/opt/openjdk-18
# Wed, 01 Sep 2021 05:22:56 GMT
ENV PATH=/opt/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Sep 2021 05:22:56 GMT
ENV JAVA_VERSION=18-ea+11
# Wed, 01 Sep 2021 05:23:08 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/11/binaries/openjdk-18-ea+11_linux-x64-musl_bin.tar.gz'; 			downloadSha256='86fad9069587a5e9dd003e7354a69b2f720a05c12706d2f2345a0c8d90e56c47'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 01 Sep 2021 05:23:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2472b57245f9dd14d4c225e1bacfc600984158e1ebfc6cf62dc53910ac1cbc`  
		Last Modified: Wed, 01 Sep 2021 05:29:13 GMT  
		Size: 928.4 KB (928412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2faa1e02748d561737720fd0ddcafcad9630b276712c6f00d908590ca1827a19`  
		Last Modified: Wed, 01 Sep 2021 05:29:27 GMT  
		Size: 188.7 MB (188699638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
