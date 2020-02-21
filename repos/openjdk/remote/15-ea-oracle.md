## `openjdk:15-ea-oracle`

```console
$ docker pull openjdk@sha256:d14fb6bdd1b146d2566b95dbc571865b990c7bc18e44e60ea749c254dd34d721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:15-ea-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:28802be866a4c110ae502049383207262028a8f4fa5fb22470e612010286d40f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255731562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2209d3617be9071240a968322763a462feeeec142af4f889a610c29aabaa1302`
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
# Fri, 21 Feb 2020 03:08:14 GMT
ENV JAVA_VERSION=15-ea+11
# Fri, 21 Feb 2020 03:08:14 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/11/GPL/openjdk-15-ea+11_linux-x64_bin.tar.gz
# Fri, 21 Feb 2020 03:08:14 GMT
ENV JAVA_SHA256=dbaed2c9b6a3158494de3a5d87e772a9950535f9053a239c5dcbc1baee5b967d
# Fri, 21 Feb 2020 03:09:49 GMT
RUN set -eux; 		curl -fL -o /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Fri, 21 Feb 2020 03:09:49 GMT
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
	-	`sha256:f16eac9ec9e9c26a8dfe60ed7867ff803c9cb9f968e4d6aeec89b5b0b10c4117`  
		Last Modified: Fri, 21 Feb 2020 03:14:25 GMT  
		Size: 198.2 MB (198212940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
