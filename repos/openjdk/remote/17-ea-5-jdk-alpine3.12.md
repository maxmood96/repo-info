## `openjdk:17-ea-5-jdk-alpine3.12`

```console
$ docker pull openjdk@sha256:50f9b632a40a175f45e9505d3eb82a99edac7da56ac9ab51cc33033d11dee18a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:17-ea-5-jdk-alpine3.12` - linux; amd64

```console
$ docker pull openjdk@sha256:7349bbb1f74b4260819f6dec995abbac3152a0bfa7696cc777f58a5744facea4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.8 MB (190797599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d58131561b93f8c13468f732a4303b6dcaf137297c13341e495903e9b852ac`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:15:27 GMT
RUN apk add --no-cache java-cacerts
# Mon, 01 Feb 2021 19:47:02 GMT
ENV JAVA_HOME=/opt/openjdk-17
# Mon, 01 Feb 2021 19:47:03 GMT
ENV PATH=/opt/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 19:47:03 GMT
ENV JAVA_VERSION=17-ea+5
# Mon, 01 Feb 2021 19:47:20 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/5/binaries/openjdk-17-ea+5_linux-x64-musl_bin.tar.gz'; 			downloadSha256='709daae3577453dba8e4ea03e8b52daeb11370648d2da1d012df527556c0cda2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 01 Feb 2021 19:47:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7f0194508bfdf90c2d4c810091723a528db557a8f15dc3342de6f146b13a31`  
		Last Modified: Thu, 17 Dec 2020 13:21:09 GMT  
		Size: 927.2 KB (927220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c7aa5543b72e13681e9111aa6ea8986c5f8ec75693b90e6745e56d90228326`  
		Last Modified: Mon, 01 Feb 2021 20:03:08 GMT  
		Size: 187.1 MB (187071313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
