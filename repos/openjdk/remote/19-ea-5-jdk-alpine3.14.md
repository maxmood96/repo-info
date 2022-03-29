## `openjdk:19-ea-5-jdk-alpine3.14`

```console
$ docker pull openjdk@sha256:740e24f32673acf988d04deef6bb0cb22474f37099a6efd300186dfedd0a59b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `openjdk:19-ea-5-jdk-alpine3.14` - linux; amd64

```console
$ docker pull openjdk@sha256:939bcd85b10e3688fa779afdd4459f661ed4ceaa5b51c260e1aa1c372e54e769
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 MB (194324421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df471afc77cb63a7effd56e2a2bed3a266545e904d1d393de8eecdbbbafb4e02`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:41 GMT
ADD file:900b3c9d6bd18f94bde19b8eb177a55f956f4030deea9171e6c3da797a213636 in / 
# Tue, 29 Mar 2022 00:19:41 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 00:53:29 GMT
RUN apk add --no-cache java-cacerts
# Tue, 29 Mar 2022 00:53:29 GMT
ENV JAVA_HOME=/opt/openjdk-19
# Tue, 29 Mar 2022 00:53:29 GMT
ENV PATH=/opt/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 00:53:29 GMT
ENV JAVA_VERSION=19-ea+5
# Tue, 29 Mar 2022 00:53:40 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/5/binaries/openjdk-19-ea+5_linux-x64-musl_bin.tar.gz'; 			downloadSha256='0ee67a41fe97341f131bd4f065ed6092d55c15de5f00f8ba1e57d21eefb2c787'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 29 Mar 2022 00:53:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cfab2db722092277479ddd659049695fa8081d2a03c31b01d388cc21802de8b4`  
		Last Modified: Tue, 29 Mar 2022 00:20:33 GMT  
		Size: 2.8 MB (2818354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228bdffc2917788b5d6ea79f06a0da4e9ac650b23c0c114e6e585134e0179ae8`  
		Last Modified: Tue, 29 Mar 2022 01:07:20 GMT  
		Size: 913.3 KB (913297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c72b5f381f2525a5b89e88da887ed0047fcf271b8966131ecb54754f13779855`  
		Last Modified: Tue, 29 Mar 2022 01:07:33 GMT  
		Size: 190.6 MB (190592770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
