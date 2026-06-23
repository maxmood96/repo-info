## `sapmachine:17-jdk-alpine-3.22`

```console
$ docker pull sapmachine@sha256:30106cdfadf26d66fc63dc62827e6320d76f8712b7edac483f8e25747e5f0a70
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:17-jdk-alpine-3.22` - linux; amd64

```console
$ docker pull sapmachine@sha256:43dc762de783c6cb9885a6469baed8e6376237d81162fdf04b1f25f400ef70e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.4 MB (206390855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f861b25b61ba49259691ae51e314f6c030c862edcaabdfdfd59cb81bfcd6c2d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:08:48 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-17-jdk=17.0.19-r0 # buildkit
# Mon, 22 Jun 2026 20:08:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-sapmachine-jdk
# Mon, 22 Jun 2026 20:08:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a8cfb10aa7b765ee1eec8c4f6a2613ef36d29a6b72c768de31073987a11af5`  
		Last Modified: Mon, 22 Jun 2026 20:09:08 GMT  
		Size: 202.6 MB (202603260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-alpine-3.22` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bd6fecce0a1f17ed821f3c291e14c3d5dca918a1c85d846c9e9997b43ef88f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.3 KB (518345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e56ec496ba6c70f23843015c8b6daf557ba8b9c2e9b355ec9b44efea38cf30b1`

```dockerfile
```

-	Layers:
	-	`sha256:3b4cdd98f46b3ea3467826d4af392382ff93bc9fc3abbeb133d1a3a96b40a143`  
		Last Modified: Mon, 22 Jun 2026 20:09:03 GMT  
		Size: 510.7 KB (510723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ed5689a991fb8d18ee40c7adf1a15f5f352537f9bda113fe5a16337949e5a67`  
		Last Modified: Mon, 22 Jun 2026 20:09:03 GMT  
		Size: 7.6 KB (7622 bytes)  
		MIME: application/vnd.in-toto+json
