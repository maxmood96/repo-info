## `openjdk:15-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:8517e032be71467706281eb56affa477cae5061918e3683755d5f5d9ba7865a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:15-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:a63f9f8969b544649313511422bf42a834329aee1b399332c7b785e72991e218
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.3 MB (250276903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:428d694a25c59291f8b16f22d901f8dbf87e26fb1b21090f8dc3e5af56016c7e`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Mon, 04 May 2020 20:20:53 GMT
ADD file:d23891d2372d6aae3d738388c74dacd92f9406083ee0c1ac0e2bfd140f92ec2b in / 
# Mon, 04 May 2020 20:20:53 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2020 20:38:21 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Mon, 04 May 2020 20:38:21 GMT
ENV LANG=en_US.UTF-8
# Mon, 04 May 2020 20:38:21 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Mon, 04 May 2020 20:38:21 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 May 2020 20:38:22 GMT
ENV JAVA_VERSION=15-ea+21
# Mon, 04 May 2020 20:38:22 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/21/GPL/openjdk-15-ea+21_linux-x64_bin.tar.gz
# Mon, 04 May 2020 20:38:22 GMT
ENV JAVA_SHA256=c8ff25779035a045f1a74f21b51a7383eb5f5d78d06973d722ea259886d9da62
# Mon, 04 May 2020 20:38:50 GMT
RUN set -eux; 		curl -fL -o /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Mon, 04 May 2020 20:38:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:83755823a002357171a0b229ef5769a60db47a90b624adc45f8c6b7cd1d1394f`  
		Last Modified: Mon, 04 May 2020 20:22:07 GMT  
		Size: 43.5 MB (43455265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e105caaf23acf967db67aa1f683d428603dbb51e12295bfe8f5df6a4cce8bb`  
		Last Modified: Mon, 04 May 2020 20:40:58 GMT  
		Size: 14.8 MB (14758294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad577f4f0881d5ec5f1d146723b6fa8e2e8883ad2fdde68afe04f1e1cb10a748`  
		Last Modified: Mon, 04 May 2020 20:41:13 GMT  
		Size: 192.1 MB (192063344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
