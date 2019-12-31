## `openjdk:15-ea-jdk-oraclelinux7`

```console
$ docker pull openjdk@sha256:cdb9a365ab5dbe967e14d25741be1e1c5cd99c4e2e80faed691e357b241b9036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:15-ea-jdk-oraclelinux7` - linux; amd64

```console
$ docker pull openjdk@sha256:9c822ec60f91a33026ac0c13948d54b951157772818dd92d7bc7579f639edfd5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.5 MB (256544818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1127fbc80d02aecb6372247a7fca7c10d484ba687ded75eddb065171482b8f16`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Fri, 20 Dec 2019 01:46:43 GMT
ADD file:e662b0d428c91ed028fec1db2cccbeddea848eb36b32c8bfad324619b8e57d9f in / 
# Fri, 20 Dec 2019 01:46:44 GMT
CMD ["/bin/bash"]
# Fri, 20 Dec 2019 02:05:13 GMT
RUN set -eux; 	yum install -y 		gzip 		tar 				binutils 		freetype fontconfig 	; 	rm -rf /var/cache/yum
# Fri, 20 Dec 2019 02:05:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Dec 2019 02:05:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Fri, 20 Dec 2019 02:05:13 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Dec 2019 23:21:47 GMT
ENV JAVA_VERSION=15-ea+3
# Mon, 30 Dec 2019 23:21:47 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/3/GPL/openjdk-15-ea+3_linux-x64_bin.tar.gz
# Mon, 30 Dec 2019 23:21:47 GMT
ENV JAVA_SHA256=4f40dbefac1f389b141f9ce2c76a5272fcb589885263f3e28b1edef602632733
# Mon, 30 Dec 2019 23:22:21 GMT
RUN set -eux; 		curl -fL -o /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Mon, 30 Dec 2019 23:22:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:822ace0353cbeeb23baa4e10b00916d8aae76c005023f5807d16cd97e6339b9b`  
		Last Modified: Fri, 20 Dec 2019 01:48:50 GMT  
		Size: 42.7 MB (42725372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf4d0631bf4e4c98ff5629cdf7958d9db134bbabd5a323f89f8fd783ca4c524`  
		Last Modified: Fri, 20 Dec 2019 02:10:52 GMT  
		Size: 14.8 MB (14793038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fcb4c844843cdec15e1e7a2fdd24ca152f8b0b36cf3aafb0d70f3b31e5a7bf6`  
		Last Modified: Mon, 30 Dec 2019 23:29:09 GMT  
		Size: 199.0 MB (199026408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
