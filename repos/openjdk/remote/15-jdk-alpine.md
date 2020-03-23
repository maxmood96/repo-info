## `openjdk:15-jdk-alpine`

```console
$ docker pull openjdk@sha256:45cae7a0e8b0d95b6d547ee983f6333b8ebaefb948669cb9b6ad5dfa1ffc4e0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:15-jdk-alpine` - linux; amd64

```console
$ docker pull openjdk@sha256:477d0b3406e8bb54bf1852f21acf908c7f43c37b3bcdf65bb6709cd71caad4cf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202680604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97674f54ffe1f9f9b9db6b92485e80dcd4197747edbda71fc9268d8200ccba42`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Mar 2020 21:19:34 GMT
ADD file:0c4555f363c2672e350001f1293e689875a3760afe7b3f9146886afe67121cba in / 
# Mon, 23 Mar 2020 21:19:34 GMT
CMD ["/bin/sh"]
# Mon, 23 Mar 2020 21:22:47 GMT
ENV JAVA_HOME=/opt/openjdk-15
# Mon, 23 Mar 2020 21:22:47 GMT
ENV PATH=/opt/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 23 Mar 2020 21:22:47 GMT
ENV JAVA_VERSION=15-ea+10
# Mon, 23 Mar 2020 21:22:47 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/alpine/10/binaries/openjdk-15-ea+10_linux-x64-musl_bin.tar.gz
# Mon, 23 Mar 2020 21:22:48 GMT
ENV JAVA_SHA256=15a5e8002e24ed129b82bfe55ffe4bdbf3cfd0a7e5ad3399879cdd44175bfd06
# Mon, 23 Mar 2020 21:23:14 GMT
RUN set -eux; 		wget -O /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		java -Xshare:dump; 		java --version; 	javac --version
# Mon, 23 Mar 2020 21:23:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:aad63a9339440e7c3e1fff2b988991b9bfb81280042fa7f39a5e327023056819`  
		Last Modified: Mon, 23 Mar 2020 21:19:53 GMT  
		Size: 2.8 MB (2803255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff46896e56bf113407cf2f8c33ef8f9f4193a9265ad0c71d6e4071c5dad69126`  
		Last Modified: Mon, 23 Mar 2020 21:25:00 GMT  
		Size: 199.9 MB (199877349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
