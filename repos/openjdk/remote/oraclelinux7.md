## `openjdk:oraclelinux7`

```console
$ docker pull openjdk@sha256:16d415606aebacacd63af96bcc974a58db60362327e2b59b0fd46f090445d7e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:b4556bd1088b137936365f41b207c488a631687fdd36de2b2ffce7c26c2421fc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.4 MB (257354479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30503f5328a09588923743711b642ebd453f29e97f4400716da55d938db21ac1`
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
# Fri, 10 Apr 2020 20:44:17 GMT
ENV JAVA_HOME=/usr/java/openjdk-14
# Fri, 10 Apr 2020 20:44:17 GMT
ENV PATH=/usr/java/openjdk-14/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Apr 2020 20:44:17 GMT
ENV JAVA_VERSION=14
# Fri, 10 Apr 2020 20:44:18 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk14/076bab302c7b4508975440c56f6cc26a/36/GPL/openjdk-14_linux-x64_bin.tar.gz
# Fri, 10 Apr 2020 20:44:18 GMT
ENV JAVA_SHA256=c7006154dfb8b66328c6475447a396feb0042608ee07a96956547f574a911c09
# Fri, 10 Apr 2020 20:44:32 GMT
RUN set -eux; 		curl -fL -o /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Fri, 10 Apr 2020 20:44:32 GMT
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
	-	`sha256:ab5b731c8334a5063e3b4d8353d2afcd11e95285fc35d1864e80cb4f72e54614`  
		Last Modified: Fri, 10 Apr 2020 20:46:36 GMT  
		Size: 199.1 MB (199134535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
