## `openjdk:15-ea-oraclelinux7`

```console
$ docker pull openjdk@sha256:90f40ba166a36942a7d2e63b2d5e16ac31882da212a3820d3cd62a22eb076f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:15-ea-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:9031af0c5d42b3203070bf689fd29976db5fdff074cecdf5d6fdf4fc9b03421f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.6 MB (256562037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d70246ee8c5396465655dfc2d6173557fe06f37ceecd082a9ba2a865079f918c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Tue, 21 Jan 2020 05:21:23 GMT
ADD file:c8bbabb7270612c9e26467e961293f9b6550a7a7ad2bb07d08c08e14c8ea2961 in / 
# Tue, 21 Jan 2020 05:21:23 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2020 05:38:32 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 21 Jan 2020 05:38:32 GMT
ENV LANG=en_US.UTF-8
# Tue, 21 Jan 2020 05:38:32 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Tue, 21 Jan 2020 05:38:32 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Jan 2020 05:38:32 GMT
ENV JAVA_VERSION=15-ea+6
# Tue, 21 Jan 2020 05:38:32 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/6/GPL/openjdk-15-ea+6_linux-x64_bin.tar.gz
# Tue, 21 Jan 2020 05:38:33 GMT
ENV JAVA_SHA256=122a306f4bcf97ab06653d804fb6ff2cba6ef1943331a341193ec5d2b0f87587
# Tue, 21 Jan 2020 05:40:08 GMT
RUN set -eux; 		curl -fL -o /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Tue, 21 Jan 2020 05:40:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:977461c903012ec41b22a4c1bf975a3199570bd92ccc75a70f5a1119bca6d402`  
		Last Modified: Mon, 18 Nov 2019 23:06:50 GMT  
		Size: 42.7 MB (42712648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d4dba4c275cee34738472078397bb7c4e0fb5950b48fbb9560d344cfd5608d`  
		Last Modified: Tue, 21 Jan 2020 05:44:58 GMT  
		Size: 14.8 MB (14795181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e3f7e81001804a5ad106c658a2197049621aaac7339474effda244d195dce44`  
		Last Modified: Tue, 21 Jan 2020 05:44:58 GMT  
		Size: 199.1 MB (199054208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
