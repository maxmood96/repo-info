## `openjdk:17-ea-5-alpine`

```console
$ docker pull openjdk@sha256:198b8046154ee83f7b816fa9f6221bd66434d44e9799a681cdbfba24f8165440
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:17-ea-5-alpine` - linux; amd64

```console
$ docker pull openjdk@sha256:9617421debf102e020ba50af50ac1d8696acadfbeb1d52659d4f6b7ba250c972
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.8 MB (190810474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ab1ef2efdcdb55709556d2df2f6e2b061f6d585dde39f94ff4c64ca50a3eb9`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 28 Jan 2021 23:19:38 GMT
ADD file:0e2d487cd80773e947c8aae6daad3d565b7bb019a954af2b8bff188681c00d81 in / 
# Thu, 28 Jan 2021 23:19:38 GMT
CMD ["/bin/sh"]
# Mon, 01 Feb 2021 19:46:23 GMT
RUN apk add --no-cache java-cacerts
# Mon, 01 Feb 2021 19:46:24 GMT
ENV JAVA_HOME=/opt/openjdk-17
# Mon, 01 Feb 2021 19:46:24 GMT
ENV PATH=/opt/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 19:46:24 GMT
ENV JAVA_VERSION=17-ea+5
# Mon, 01 Feb 2021 19:46:53 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/5/binaries/openjdk-17-ea+5_linux-x64-musl_bin.tar.gz'; 			downloadSha256='709daae3577453dba8e4ea03e8b52daeb11370648d2da1d012df527556c0cda2'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 01 Feb 2021 19:46:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4c0d98bf9879488e0407f897d9dd4bf758555a78e39675e72b5124ccf12c2580`  
		Last Modified: Thu, 28 Jan 2021 23:20:08 GMT  
		Size: 2.8 MB (2811321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1834e342ac63f74ab268f59b78219089f04f37c6c39e469afc0292192b9c2d`  
		Last Modified: Mon, 01 Feb 2021 20:02:23 GMT  
		Size: 928.2 KB (928244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7725e946473d9a3cfc38a4fa08da3e90f5b50fdb1cce768b9a5f0d73d2f34d0b`  
		Last Modified: Mon, 01 Feb 2021 20:02:40 GMT  
		Size: 187.1 MB (187070909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
