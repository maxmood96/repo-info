## `openjdk:15-ea-oraclelinux7`

```console
$ docker pull openjdk@sha256:636ddc9da0ade07505d8a0c803e430ea1c31ffa0d068514f3ecd021d034b89a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:15-ea-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:60d3564155a8b64e79c882e89a7cd067bc21cbc5dac1c4bb9aef6639896f6abc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256131093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2fe98d27ae06c277ccf37ee110804ed352a9985e78a8a5eb422beb6b7a46013`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Tue, 10 Mar 2020 02:20:39 GMT
ADD file:ca821d696bf87ff0b7ed9d85b5b0acc4656fc6498d2f5bd2c051bb16a99bfcbf in / 
# Tue, 10 Mar 2020 02:20:40 GMT
CMD ["/bin/bash"]
# Tue, 10 Mar 2020 02:37:57 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 10 Mar 2020 02:37:57 GMT
ENV LANG=en_US.UTF-8
# Tue, 10 Mar 2020 02:37:57 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Tue, 10 Mar 2020 02:37:58 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Apr 2020 23:21:16 GMT
ENV JAVA_VERSION=15-ea+17
# Mon, 06 Apr 2020 23:21:16 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/17/GPL/openjdk-15-ea+17_linux-x64_bin.tar.gz
# Mon, 06 Apr 2020 23:21:16 GMT
ENV JAVA_SHA256=e8022a7a00c3f8cc7518cbe89f7023356322c2583ce884e2c727218c07595b1a
# Mon, 06 Apr 2020 23:22:50 GMT
RUN set -eux; 		curl -fL -o /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Mon, 06 Apr 2020 23:22:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd17e56c322c9601c98f41573bb47bd4cd68ff386d7d07538f156a7c0ef6c650`  
		Last Modified: Tue, 10 Mar 2020 02:22:01 GMT  
		Size: 42.7 MB (42725735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecdd73bb99224b1c73d7d3d8eea56a91f5e7fc73628dcfa3b5432cca23c7373d`  
		Last Modified: Tue, 10 Mar 2020 02:42:14 GMT  
		Size: 14.8 MB (14770095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486662a04f2c248e506892b8a1027b60a01a9eb4b5c0a8a4f58d9a30df53c59d`  
		Last Modified: Mon, 06 Apr 2020 23:25:33 GMT  
		Size: 198.6 MB (198635263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
