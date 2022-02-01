## `openjdk:19-ea-5-jdk-alpine3.14`

```console
$ docker pull openjdk@sha256:559143a2aabeb0588c1465f2168e7d6f0dad83bd4d1038a89bd62c782ce96e8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `openjdk:19-ea-5-jdk-alpine3.14` - linux; amd64

```console
$ docker pull openjdk@sha256:84f1913bca606c52931b16f41154d28ab6ed0de84695d760cbc0186d36b0b229
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.3 MB (194343890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e19bf830ca20d6ef0e355d22f5ba681291356dd649ccb70eeb530f3240069eb`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 07:32:26 GMT
RUN apk add --no-cache java-cacerts
# Tue, 01 Feb 2022 03:12:08 GMT
ENV JAVA_HOME=/opt/openjdk-19
# Tue, 01 Feb 2022 03:12:09 GMT
ENV PATH=/opt/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Feb 2022 03:12:09 GMT
ENV JAVA_VERSION=19-ea+5
# Tue, 01 Feb 2022 03:12:21 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/5/binaries/openjdk-19-ea+5_linux-x64-musl_bin.tar.gz'; 			downloadSha256='0ee67a41fe97341f131bd4f065ed6092d55c15de5f00f8ba1e57d21eefb2c787'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 01 Feb 2022 03:12:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad0d0169427449f303a2c6baf5a00c969d2b2b85c2edd07aaa19ce580773a4a`  
		Last Modified: Sat, 13 Nov 2021 07:40:09 GMT  
		Size: 928.2 KB (928186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6c40bac23dd9301b23b951a578ea0d36defafb4c80acd9cf5a23e24b42eea9`  
		Last Modified: Tue, 01 Feb 2022 03:24:47 GMT  
		Size: 190.6 MB (190592723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
