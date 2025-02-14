## `sapmachine:jdk-alpine-3.21`

```console
$ docker pull sapmachine@sha256:5a4ed758fdcd51c28271a42cd9081a44acb28e3428be0efa5e771dd350949cc6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:jdk-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:18af9236fa4120a1e9acc59d136ac3e7bf10843b5b29d6db8a6a9698cc240ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.0 MB (226986892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af5ae42196821741bc2a6f9fd5657f595ead4f786b22bcc7cfd82251b4fb2ffc`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:22 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["/bin/sh"]
# Mon, 27 Jan 2025 13:39:22 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-23-jdk=23.0.2-r0 # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-sapmachine-jdk
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fca06c9f69cb1375d117af8193ceeb82e4c49d9eff18e60465279715601a56`  
		Last Modified: Fri, 14 Feb 2025 19:14:27 GMT  
		Size: 223.3 MB (223344645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4fd404de79bbd3852e52689dd93b0746e4339fefb75e672452ce86a7d9856d80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.1 KB (522103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e410db792172ad78cba9292aecf815db5c50059fdd5065243c5af3e1efd7b9d3`

```dockerfile
```

-	Layers:
	-	`sha256:734d12ec62ffcdd6f5c99d3fae3bdc219ec207088b6e9cc4113ba408e58bfb0a`  
		Last Modified: Fri, 14 Feb 2025 22:06:48 GMT  
		Size: 512.8 KB (512845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33a3772132d50a1d43ebd41434287b5122fa57b462e4897e766c95da3754288d`  
		Last Modified: Fri, 14 Feb 2025 22:06:48 GMT  
		Size: 9.3 KB (9258 bytes)  
		MIME: application/vnd.in-toto+json
