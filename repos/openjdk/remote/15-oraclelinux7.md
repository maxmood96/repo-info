## `openjdk:15-oraclelinux7`

```console
$ docker pull openjdk@sha256:35c0cf31a3b362db17458f4728ef65f402603a3a036f9ad38abd48afbf1ecf62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:15-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:d1756bc86decb2526ea47a079aaff89d165e3d3faed2f77f5f96a06f9b6f92d6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.6 MB (256554224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f10aeedb1d9a1abec69bad181832f7e1c3edc7aa25bb84a91fc1e235191cad75`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Tue, 28 Jan 2020 21:36:05 GMT
ADD file:a320cfe017a986947ac6b09db573e476eacafc80311e517efcc5e965fcc445fb in / 
# Tue, 28 Jan 2020 21:36:06 GMT
CMD ["/bin/bash"]
# Tue, 28 Jan 2020 21:53:09 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 28 Jan 2020 21:53:09 GMT
ENV LANG=en_US.UTF-8
# Tue, 28 Jan 2020 21:53:10 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Tue, 28 Jan 2020 21:53:10 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 31 Jan 2020 17:22:16 GMT
ENV JAVA_VERSION=15-ea+8
# Fri, 31 Jan 2020 17:22:16 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/8/GPL/openjdk-15-ea+8_linux-x64_bin.tar.gz
# Fri, 31 Jan 2020 17:22:17 GMT
ENV JAVA_SHA256=ab41dd4e616e015ec94f26e4d2c8253f376f5f5d574db811f341abc6c55e333c
# Fri, 31 Jan 2020 17:22:43 GMT
RUN set -eux; 		curl -fL -o /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Fri, 31 Jan 2020 17:22:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:86607bb85307f4e017c6cc236573951482f1de084e0987480fecea9295c2f923`  
		Last Modified: Tue, 28 Jan 2020 21:37:18 GMT  
		Size: 42.7 MB (42725283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1d217c4e16034b1dca5abb6ea80aabded93c73f35686d806d9f2aa8555743da`  
		Last Modified: Tue, 28 Jan 2020 22:00:21 GMT  
		Size: 14.8 MB (14793339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b4577c1713574dd967f070c4ea9a752d2348496fe29f40e7e5f4dc24e6bcf1`  
		Last Modified: Fri, 31 Jan 2020 17:26:45 GMT  
		Size: 199.0 MB (199035602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
