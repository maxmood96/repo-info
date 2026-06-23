## `sapmachine:lts-jdk-alpine-3.22`

```console
$ docker pull sapmachine@sha256:5f5f42b81fa860b22bfed6bcc5f5157916a4a1ba063d30d17098cfe306ad8e61
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:lts-jdk-alpine-3.22` - linux; amd64

```console
$ docker pull sapmachine@sha256:32c4d605cbc3106b03f021327ad96135a3b3a2e23475bb6a7695c71ffbf92268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.8 MB (226777749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33722af37819c6675aa0a03556244bb6cd17024ac16cca1886b48ae07987a9c3`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:08:15 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-25-jdk=25.0.3-r0 # buildkit
# Mon, 22 Jun 2026 20:08:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-sapmachine-jdk
# Mon, 22 Jun 2026 20:08:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f65b05fd6cd356d93b5c38ea656f2dd0e2a3b16240df6a715ecb030aafd9626`  
		Last Modified: Mon, 22 Jun 2026 20:08:36 GMT  
		Size: 223.0 MB (222990154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-alpine-3.22` - unknown; unknown

```console
$ docker pull sapmachine@sha256:11432903362a60d59dc4fd0e423d9e0022d6ecd8c9a8516427157d329df9ca4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.2 KB (510191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955a0917425d6969c11cd351f407642884911b5a407384f2a50a78ae205066d8`

```dockerfile
```

-	Layers:
	-	`sha256:6429774ee234c0d1829d3125d70fe250728ffce23710bfed79ee9848a4e14267`  
		Last Modified: Mon, 22 Jun 2026 20:08:31 GMT  
		Size: 501.9 KB (501921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3741f11eee2530b53ce2c6f18cf5ac58276605a0fbec36ab8f5735ca14506dec`  
		Last Modified: Mon, 22 Jun 2026 20:08:31 GMT  
		Size: 8.3 KB (8270 bytes)  
		MIME: application/vnd.in-toto+json
