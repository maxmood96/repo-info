## `openjdk:19-ea-alpine3.14`

```console
$ docker pull openjdk@sha256:7cff0b6eafd6c1aedd3d6aa109fdc043c39b677d3618ed7bf176af2b7b579979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `openjdk:19-ea-alpine3.14` - linux; amd64

```console
$ docker pull openjdk@sha256:7bbd958177d23420e64be404db67754eb022dbc05b380963c9abb29f4c46b639
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 MB (194324324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d7f9af96099f074ddbee1adc8a5f198ef52887bab1517a5dadd7fd5273e73e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Tue, 05 Apr 2022 10:20:56 GMT
RUN apk add --no-cache java-cacerts
# Tue, 05 Apr 2022 10:20:57 GMT
ENV JAVA_HOME=/opt/openjdk-19
# Tue, 05 Apr 2022 10:20:57 GMT
ENV PATH=/opt/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Apr 2022 10:20:57 GMT
ENV JAVA_VERSION=19-ea+5
# Tue, 05 Apr 2022 10:21:07 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/5/binaries/openjdk-19-ea+5_linux-x64-musl_bin.tar.gz'; 			downloadSha256='0ee67a41fe97341f131bd4f065ed6092d55c15de5f00f8ba1e57d21eefb2c787'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 05 Apr 2022 10:21:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e601d4fa60a14c882ae121702306ef6a4a37403f9287fbb904108796905bd8f7`  
		Last Modified: Tue, 05 Apr 2022 10:27:41 GMT  
		Size: 913.3 KB (913326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a3883616dee8a9177c90a5726519d51c87ada73c9ec02d1016452ab24737ed`  
		Last Modified: Tue, 05 Apr 2022 10:27:55 GMT  
		Size: 190.6 MB (190592628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
