## `openjdk:15-oraclelinux7`

```console
$ docker pull openjdk@sha256:51160ab6e5994b9ca544d36cb46e9f04c9deb5315e2936e2e5eaccc2d94cc3cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:15-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:4da4eb6c81863a72a445e0476a6657d67d5bb8852f23615bb875538e542835d2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.9 MB (255921802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8016d639fff6a7cca58dfc83c2e6928dfd649eea4fcea6be1295abcbc0fe936e`
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
# Tue, 10 Mar 2020 02:37:58 GMT
ENV JAVA_VERSION=15-ea+13
# Tue, 10 Mar 2020 02:37:58 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/13/GPL/openjdk-15-ea+13_linux-x64_bin.tar.gz
# Tue, 10 Mar 2020 02:37:58 GMT
ENV JAVA_SHA256=4c3132ba41129cec900517c684fc14c64dc82dd46b673c3ef4a6ef3272938b1f
# Tue, 10 Mar 2020 02:38:44 GMT
RUN set -eux; 		curl -fL -o /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Tue, 10 Mar 2020 02:38:44 GMT
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
	-	`sha256:2c97191fd01a971ab02e6ead5b438e18f8c03d02ce3d60ee3124132d849a7604`  
		Last Modified: Tue, 10 Mar 2020 02:42:35 GMT  
		Size: 198.4 MB (198425972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
