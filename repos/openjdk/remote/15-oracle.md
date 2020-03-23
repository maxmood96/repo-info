## `openjdk:15-oracle`

```console
$ docker pull openjdk@sha256:6ae8b6de2fc4dddc1f51ef8567f6af7084364807519543f7d1e9e3f1e9a426a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:15-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:3b223d7a992d9ea6e9cb550df4509f03f94f51c53f0b82c0491e4e060f307cf9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.9 MB (255942970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ec20e9b9b292a00aae7a261f564b174c84e5124c7d921f8a2a8211e2f1d2071`
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
# Mon, 23 Mar 2020 20:20:44 GMT
ENV JAVA_VERSION=15-ea+15
# Mon, 23 Mar 2020 20:20:45 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/15/GPL/openjdk-15-ea+15_linux-x64_bin.tar.gz
# Mon, 23 Mar 2020 20:20:45 GMT
ENV JAVA_SHA256=5ac08aae3a6533ef6d6284230f30ec060ca70dc53fa94358f4b16fe1209fa557
# Mon, 23 Mar 2020 20:21:31 GMT
RUN set -eux; 		curl -fL -o /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Mon, 23 Mar 2020 20:21:31 GMT
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
	-	`sha256:a260e7ef0586f8567cbc6e0c71b15918f5c14d178e26ac5d28d0133b3a30da8c`  
		Last Modified: Mon, 23 Mar 2020 20:24:08 GMT  
		Size: 198.4 MB (198447140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
