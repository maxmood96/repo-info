## `openjdk:14-ea-33-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:6f9c8c7feae06e87f7642e3e46f214c68ac02789c44c0e83c8fba33559904476
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:14-ea-33-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:528e85aae648bd3e594b092ea982b31df32c81c0e5b5a1b8f4f21a587a65a2a8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.2 MB (257207176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d29ba3aed1b454043cdb7032b36d19c0bfb1eef22fe00ab0a866e8785c1ef911`
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
# Tue, 28 Jan 2020 21:57:09 GMT
ENV JAVA_HOME=/usr/java/openjdk-14
# Tue, 28 Jan 2020 21:57:09 GMT
ENV PATH=/usr/java/openjdk-14/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2020 21:57:09 GMT
ENV JAVA_VERSION=14-ea+33
# Tue, 28 Jan 2020 21:57:09 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk14/33/GPL/openjdk-14-ea+33_linux-x64_bin.tar.gz
# Tue, 28 Jan 2020 21:57:09 GMT
ENV JAVA_SHA256=5ab11e33d3c622b0c8b8833329b9d557c5b7b23750e025746b28f01bb9216928
# Tue, 28 Jan 2020 21:57:55 GMT
RUN set -eux; 		curl -fL -o /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Tue, 28 Jan 2020 21:57:56 GMT
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
	-	`sha256:cd3a6d88ca3db196fbec9737ba5ae5b219b68d4519d7d14357fdd8cb607e3405`  
		Last Modified: Tue, 28 Jan 2020 22:01:05 GMT  
		Size: 199.7 MB (199688554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
