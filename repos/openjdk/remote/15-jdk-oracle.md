## `openjdk:15-jdk-oracle`

```console
$ docker pull openjdk@sha256:55f23337da037cbd25a967605b15b2f27afdc1769c319a823d9ff7d12e8c2dc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:15-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:9f02e065aca09ba392b5fc978f5418893cc145e5a2630adb4c72f30c4555dcb9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.6 MB (256613592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d362fca316091d61ae7a2275b85c2c6da9bd652f23e66a44f51e13dac3987f5`
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
# Tue, 28 Jan 2020 21:53:10 GMT
ENV JAVA_VERSION=15-ea+7
# Tue, 28 Jan 2020 21:53:10 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/7/GPL/openjdk-15-ea+7_linux-x64_bin.tar.gz
# Tue, 28 Jan 2020 21:53:10 GMT
ENV JAVA_SHA256=1e6dce68fd46f21334f33ab68804f7fe4d89180b03dbf4151f61af4d50674e85
# Tue, 28 Jan 2020 21:56:51 GMT
RUN set -eux; 		curl -fL -o /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Tue, 28 Jan 2020 21:56:51 GMT
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
	-	`sha256:f7011708aabcea75a08a579efb67b9b3401791069e28049fdde2f792f91711f7`  
		Last Modified: Tue, 28 Jan 2020 22:00:35 GMT  
		Size: 199.1 MB (199094970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
