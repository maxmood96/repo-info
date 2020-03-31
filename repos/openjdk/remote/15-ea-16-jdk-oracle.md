## `openjdk:15-ea-16-jdk-oracle`

```console
$ docker pull openjdk@sha256:fc0e90dfbb8883e4808668fd33a2042a902d0d348789a7f3326d62f94078a288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:15-ea-16-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:f70bbbd60dd8b9553edc13e2661bd104b68e2c657d7d824f84f38dab5b2864ac
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.0 MB (255996956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9362105a385f91b9cb0e61597d7c0bb54f7526c0bb3f9be209cd2d2c7342324a`
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
# Tue, 31 Mar 2020 00:34:15 GMT
ENV JAVA_VERSION=15-ea+16
# Tue, 31 Mar 2020 00:34:15 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/16/GPL/openjdk-15-ea+16_linux-x64_bin.tar.gz
# Tue, 31 Mar 2020 00:34:15 GMT
ENV JAVA_SHA256=9f4ade109eb9ceea18fe3fd3b1a2428eeb8e01b5485d61916f87602b295bef7d
# Tue, 31 Mar 2020 00:34:52 GMT
RUN set -eux; 		curl -fL -o /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Tue, 31 Mar 2020 00:34:52 GMT
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
	-	`sha256:10547ec3569d29156cae2a5cd1e987c8fef26a4157d2fb8584ee5711d073d86d`  
		Last Modified: Tue, 31 Mar 2020 00:37:13 GMT  
		Size: 198.5 MB (198501126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
