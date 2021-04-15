## `openjdk:17-jdk-alpine3.12`

```console
$ docker pull openjdk@sha256:398d76985254139ec3339fc4f59333343c3d3848388fd3fef7af3cd7be91639c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:17-jdk-alpine3.12` - linux; amd64

```console
$ docker pull openjdk@sha256:328da912c48ddff37ba907eca8b2ed4527c5e10744e118cb62576925494ce4bc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.5 MB (190526299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a3085e56a365403fc602f583cb7ea5368edffe4d688e7b312930ef5aa230b2`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:36:46 GMT
RUN apk add --no-cache java-cacerts
# Wed, 14 Apr 2021 23:36:46 GMT
ENV JAVA_HOME=/opt/openjdk-17
# Wed, 14 Apr 2021 23:36:46 GMT
ENV PATH=/opt/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 23:36:46 GMT
ENV JAVA_VERSION=17-ea+14
# Wed, 14 Apr 2021 23:36:57 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/alpine/14/binaries/openjdk-17-ea+14_linux-x64-musl_bin.tar.gz'; 			downloadSha256='f07a1ac921333dafac1cd886ad49600ce143be7efebd32e1a02599a8a0829dd4'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 14 Apr 2021 23:36:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29da60970598a02604210b331bfe8295102181393801ab6a6634bd1b5ad42958`  
		Last Modified: Wed, 14 Apr 2021 23:42:56 GMT  
		Size: 927.4 KB (927388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb4cb9d375cfba23b7eaaaf37753bbd45290c9ee24bdd0221efdb1d1d911f32`  
		Last Modified: Wed, 14 Apr 2021 23:43:14 GMT  
		Size: 186.8 MB (186798344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
