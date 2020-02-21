## `openjdk:15-alpine3.11`

```console
$ docker pull openjdk@sha256:5c5c7c4ae0f0d8805ac20565c5bc1a0e2f87d28af3c5256baa80569f8ba7564d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:15-alpine3.11` - linux; amd64

```console
$ docker pull openjdk@sha256:54e8064fffe1168f26a2009ed5879e347435bd46da249d250547886f0987eb37
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202680459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e90d358c716b2ba2ecc330df3977690845f42fe0c554e067aa263d9e77ee72`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Tue, 11 Feb 2020 01:23:05 GMT
ENV JAVA_HOME=/opt/openjdk-15
# Tue, 11 Feb 2020 01:23:05 GMT
ENV PATH=/opt/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Feb 2020 03:10:37 GMT
ENV JAVA_VERSION=15-ea+10
# Fri, 21 Feb 2020 03:10:37 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/alpine/10/binaries/openjdk-15-ea+10_linux-x64-musl_bin.tar.gz
# Fri, 21 Feb 2020 03:10:37 GMT
ENV JAVA_SHA256=15a5e8002e24ed129b82bfe55ffe4bdbf3cfd0a7e5ad3399879cdd44175bfd06
# Fri, 21 Feb 2020 03:12:12 GMT
RUN set -eux; 		wget -O /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		java -Xshare:dump; 		java --version; 	javac --version
# Fri, 21 Feb 2020 03:12:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1e2c6ffcab9fe4b21845575aa34ab8d0f3caeb0b58c4d20590d46053cef466a`  
		Last Modified: Fri, 21 Feb 2020 03:15:55 GMT  
		Size: 199.9 MB (199877502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
