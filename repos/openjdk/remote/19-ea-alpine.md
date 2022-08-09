## `openjdk:19-ea-alpine`

```console
$ docker pull openjdk@sha256:1686909f4ca66f3e13463e2b00a1c53808aa155f81ae9a8aad8f4b89420d91ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `openjdk:19-ea-alpine` - linux; amd64

```console
$ docker pull openjdk@sha256:a8ac92087e997ddbb21211a57eb0fcb02d10e81edbfb88c451cc021d7f407aae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 MB (194337988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5391561d376b245c65bc2a15eaffdba0eb0cef3f53bf54c092faae848d84171f`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 21:09:57 GMT
RUN apk add --no-cache java-cacerts
# Tue, 09 Aug 2022 21:09:57 GMT
ENV JAVA_HOME=/opt/openjdk-19
# Tue, 09 Aug 2022 21:09:57 GMT
ENV PATH=/opt/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Aug 2022 21:09:57 GMT
ENV JAVA_VERSION=19-ea+5
# Tue, 09 Aug 2022 21:10:27 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/5/binaries/openjdk-19-ea+5_linux-x64-musl_bin.tar.gz'; 			downloadSha256='0ee67a41fe97341f131bd4f065ed6092d55c15de5f00f8ba1e57d21eefb2c787'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 09 Aug 2022 21:10:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b915427458bc94c8d27b2d5b98d76b7eb0074c61b0daf90b4bb19dd0451d901c`  
		Last Modified: Tue, 09 Aug 2022 21:16:55 GMT  
		Size: 939.1 KB (939120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b2ef90fa5eab15cc31f40f31d39e4715086230cc2c28c03fff04b93aa1d7406`  
		Last Modified: Tue, 09 Aug 2022 21:17:10 GMT  
		Size: 190.6 MB (190592814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
