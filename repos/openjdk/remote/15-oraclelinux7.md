## `openjdk:15-oraclelinux7`

```console
$ docker pull openjdk@sha256:a167e9a3d6da8f80d195426c433ebcb80ec4eccea2dac2c048515933ad1ebf49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:15-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:524985f58174318715d38f888ad2ac027401542c6b482819d1bf9abeed51ec90
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.9 MB (255944545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d40fca076f816e28f6385842795bd1fba24c1b9c20e256526fc9a6f98794440c`
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
# Fri, 06 Mar 2020 22:29:20 GMT
ENV JAVA_VERSION=15-ea+13
# Fri, 06 Mar 2020 22:29:20 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/13/GPL/openjdk-15-ea+13_linux-x64_bin.tar.gz
# Fri, 06 Mar 2020 22:29:20 GMT
ENV JAVA_SHA256=4c3132ba41129cec900517c684fc14c64dc82dd46b673c3ef4a6ef3272938b1f
# Fri, 06 Mar 2020 22:29:59 GMT
RUN set -eux; 		curl -fL -o /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Fri, 06 Mar 2020 22:29:59 GMT
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
	-	`sha256:5ed6865d8cc70ca512d3242ab88cbb081e687f6bf845b1a8f610006f416bbddb`  
		Last Modified: Fri, 06 Mar 2020 22:33:11 GMT  
		Size: 198.4 MB (198425923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
