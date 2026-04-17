## `sapmachine:lts-jdk-alpine-3.22`

```console
$ docker pull sapmachine@sha256:6a131fee83cb87e169e86e5b23d0662fec1f98f0acb97c4385e7e742490baf56
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:lts-jdk-alpine-3.22` - linux; amd64

```console
$ docker pull sapmachine@sha256:5d32335090fab7b55d9679a9187b335dac54f0642b2125c95342db1ac42f84d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226553508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a080cc7cf38020c1a7cd9043ff160440bf1e801708aeafff3ce9968267fe6d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:34:28 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-25-jdk=25.0.2-r0 # buildkit
# Fri, 17 Apr 2026 00:34:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-sapmachine-jdk
# Fri, 17 Apr 2026 00:34:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d123ebc1055c591921893573cb6d0eee33d2b3353d69650c86d8c84e2b0522d`  
		Last Modified: Fri, 17 Apr 2026 00:34:50 GMT  
		Size: 222.7 MB (222745319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-alpine-3.22` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1ab19d5731ea3e715a4fd1df5a4301c996291ad8cca46a5121bb75af8ca65764
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **509.5 KB (509543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dcf92e996dc575215c05dd9f7a35da51a1ac4e6b3d09416c5c259c71683c78f`

```dockerfile
```

-	Layers:
	-	`sha256:c802e0e5a02c4eb6140f39752de2d07235fc60fbb87336eba97a489a3ce6d800`  
		Last Modified: Fri, 17 Apr 2026 00:34:45 GMT  
		Size: 501.3 KB (501273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02c879de69c603dfb094bb14ea2840ccd9511980cf5099fdb1fa59337dd021d9`  
		Last Modified: Fri, 17 Apr 2026 00:34:45 GMT  
		Size: 8.3 KB (8270 bytes)  
		MIME: application/vnd.in-toto+json
