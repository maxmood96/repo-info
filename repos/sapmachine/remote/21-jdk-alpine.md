## `sapmachine:21-jdk-alpine`

```console
$ docker pull sapmachine@sha256:ed646d0d2dab6652348baa8f5c444476261c9e8c1b43f969095450801a6c1c39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:21-jdk-alpine` - linux; amd64

```console
$ docker pull sapmachine@sha256:6e7d12ff19e5bc50cd219f6bbec3e7a048dc13d444367b27636fa683635da6c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.7 MB (219721605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c9fd1a28164de151be1cf5429c880e53efccf5d58cb18e3651b0ff22a476b67`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 04 Jul 2025 15:51:06 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-21-jdk=21.0.7-r0 # buildkit
# Fri, 04 Jul 2025 15:51:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-sapmachine-jdk
# Fri, 04 Jul 2025 15:51:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de609fdac17def0851b4f9d21940aaf658e11d315af3d0ed25a0fd9d5f1974a0`  
		Last Modified: Tue, 08 Jul 2025 04:40:35 GMT  
		Size: 215.9 MB (215924759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-alpine` - unknown; unknown

```console
$ docker pull sapmachine@sha256:698c5fc800c005df11a62578f20ab69824d0a762521ee1090f01ddb0cb327956
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.2 KB (525158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e4da9cb0d88b032a57271b13c3a75e89c748ad1cbecdafbd33783e271f2381`

```dockerfile
```

-	Layers:
	-	`sha256:6bea4d9ea0aa0f4ec1426c12df0c9fa640ecdd9402887f91487b29423d5efff1`  
		Last Modified: Mon, 07 Jul 2025 21:05:43 GMT  
		Size: 514.9 KB (514929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8a33eff03ad3dca49f58ab5dd5a2b7cb80f2878f7ed4d35f7528fdc55eb0849`  
		Last Modified: Mon, 07 Jul 2025 21:05:44 GMT  
		Size: 10.2 KB (10229 bytes)  
		MIME: application/vnd.in-toto+json
