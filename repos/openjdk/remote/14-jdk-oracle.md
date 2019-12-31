## `openjdk:14-jdk-oracle`

```console
$ docker pull openjdk@sha256:9521cfbdb5bb0c564a446d3d83df5b8669cf3bc12252c70c1546cc5cad292e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:14-jdk-oracle` - linux; amd64

```console
$ docker pull openjdk@sha256:b34101282111943443f789f41ae77970497157a8c7b2ae78bb285ad062e4a7c9
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.5 MB (256538822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09215ccd4b0871be4de9c3e526c2ed46fcea3f23003b6c91915877c1ac73daf3`
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
# Fri, 20 Dec 2019 02:06:57 GMT
ENV JAVA_HOME=/usr/java/openjdk-14
# Fri, 20 Dec 2019 02:06:57 GMT
ENV PATH=/usr/java/openjdk-14/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Dec 2019 23:24:28 GMT
ENV JAVA_VERSION=14-ea+29
# Mon, 30 Dec 2019 23:24:28 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk14/29/GPL/openjdk-14-ea+29_linux-x64_bin.tar.gz
# Mon, 30 Dec 2019 23:24:28 GMT
ENV JAVA_SHA256=16981e7212ed6035580dff619f93356f707b75f6abfca9a3df7b45a290e8f521
# Mon, 30 Dec 2019 23:24:48 GMT
RUN set -eux; 		curl -fL -o /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		java --version; 	javac --version
# Mon, 30 Dec 2019 23:24:48 GMT
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
	-	`sha256:b8d6c2a0457e32c05d85b431b7ee7fa1d500d358ad6971ebf355ca768fba4aa4`  
		Last Modified: Mon, 30 Dec 2019 23:30:31 GMT  
		Size: 199.0 MB (199020412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
