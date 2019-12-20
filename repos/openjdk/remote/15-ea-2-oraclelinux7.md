## `openjdk:15-ea-2-oraclelinux7`

```console
$ docker pull openjdk@sha256:a671b0a528812fdafa84a2c6dab536ecebc333ed461e4f893ac82ff035d11414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:15-ea-2-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:bb84a3ae8aaf1489c81c1032e609e766502c0173e97cfe63c4cbc3419f457348
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.5 MB (256503778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9443c8d0ca3e9c17d62d23409aa4439446711ed58e53285fdfe508531f2e3f45`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Mon, 18 Nov 2019 23:05:29 GMT
ADD file:c8bbabb7270612c9e26467e961293f9b6550a7a7ad2bb07d08c08e14c8ea2961 in / 
# Mon, 18 Nov 2019 23:05:30 GMT
CMD ["/bin/bash"]
# Tue, 19 Nov 2019 04:23:39 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Tue, 19 Nov 2019 04:23:39 GMT
ENV LANG=en_US.UTF-8
# Thu, 19 Dec 2019 04:39:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Thu, 19 Dec 2019 04:39:11 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Dec 2019 23:28:22 GMT
ENV JAVA_VERSION=15-ea+2
# Thu, 19 Dec 2019 23:28:22 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/2/GPL/openjdk-15-ea+2_linux-x64_bin.tar.gz
# Thu, 19 Dec 2019 23:28:22 GMT
ENV JAVA_SHA256=a329c96e555819bfd005a9fbf11e75cd180c2c4331b1d2637c071ff9276e9f69
# Thu, 19 Dec 2019 23:28:52 GMT
RUN set -eux; 		curl -fL -o /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Thu, 19 Dec 2019 23:28:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:977461c903012ec41b22a4c1bf975a3199570bd92ccc75a70f5a1119bca6d402`  
		Last Modified: Mon, 18 Nov 2019 23:06:50 GMT  
		Size: 42.7 MB (42712648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b03bc4978d77c248161b19b002c5b1814492890df489738fda21ebfadf7867e`  
		Last Modified: Tue, 19 Nov 2019 04:26:37 GMT  
		Size: 14.8 MB (14789460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d3d17954a021ba6b4f731943b71a64b899005fd2274193d4dcb565cdb5116e`  
		Last Modified: Thu, 19 Dec 2019 23:33:15 GMT  
		Size: 199.0 MB (199001670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
