## `openjdk:15-ea-19-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:9f898f0dcd68ab799fe161ce3ff907578d402a3fbb6631ced6171b4a546f64ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:15-ea-19-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:893737bdea252f0960ed115fe7a5a99d5cec45630248b2b6ba7c3fa895c8f041
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255662110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56ecef26f82a84849b26086d519911e5430bc5dc7f45b73a6cd54a4ead83551`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Fri, 10 Apr 2020 20:26:28 GMT
ADD file:53599f8bbed1dcb68d6fd6418597c9692c328f49a3a3864871c5237c64e00375 in / 
# Fri, 10 Apr 2020 20:26:28 GMT
CMD ["/bin/bash"]
# Fri, 10 Apr 2020 20:43:19 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 10 Apr 2020 20:43:19 GMT
ENV LANG=en_US.UTF-8
# Fri, 10 Apr 2020 20:43:19 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Fri, 10 Apr 2020 20:43:19 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 20 Apr 2020 18:24:47 GMT
ENV JAVA_VERSION=15-ea+19
# Mon, 20 Apr 2020 18:24:47 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/19/GPL/openjdk-15-ea+19_linux-x64_bin.tar.gz
# Mon, 20 Apr 2020 18:24:47 GMT
ENV JAVA_SHA256=bb111954337ae9a48c7928f5638096c82d681a20a64f630efaebf2172bf7c924
# Mon, 20 Apr 2020 18:25:32 GMT
RUN set -eux; 		curl -fL -o /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Mon, 20 Apr 2020 18:25:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:79ccf0f4e30fb9e8aa16b93e5123f4ebd2ebe8e0f8d21cc01956016f867ab3bf`  
		Last Modified: Fri, 10 Apr 2020 20:27:25 GMT  
		Size: 43.5 MB (43457734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ceb08e4244f41a1398e621d60c54d89e7f76991ffec77188bc98bb07e60001`  
		Last Modified: Fri, 10 Apr 2020 20:45:52 GMT  
		Size: 14.8 MB (14762210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30f9f0cfffd03025fd87dc651ce9ceedc8da40782372d02f4e6847b46da5148`  
		Last Modified: Mon, 20 Apr 2020 18:29:15 GMT  
		Size: 197.4 MB (197442166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
