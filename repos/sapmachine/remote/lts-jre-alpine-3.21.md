## `sapmachine:lts-jre-alpine-3.21`

```console
$ docker pull sapmachine@sha256:3dcf9bafd3004fe83e7fdd2f17874bbc443a1b3d31e85e58e07d23eac130f800
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:lts-jre-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:7d4a407e19aebbcbdd2c15fad034983e5b68adb915fc405fa4ce8699bf60ad88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (60950993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b24415f2595e18b3cc38df551601cb59d0654c83867ffe0ac87166ff5af543d`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 21:30:17 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-25-jre=25.0.1-r0 # buildkit
# Tue, 21 Oct 2025 21:30:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-sapmachine-jre
# Tue, 21 Oct 2025 21:30:17 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Sun, 07 Dec 2025 13:55:07 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5c192a404d7969cff2436a4b4776302f6456f0b8beb731a3f03d68da907213`  
		Last Modified: Wed, 22 Oct 2025 02:42:34 GMT  
		Size: 57.3 MB (57308424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:907fb835ad03016c175728b998f5167ae6a70274c9f569816120b87f8c721292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.6 KB (436581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babfd76cd6d7f694101a1b99dc92cbcd58875651198344629e2065d67e7f0622`

```dockerfile
```

-	Layers:
	-	`sha256:703a1563469c61429ffc1519be9103b1001104cc90a0069bb429b5db3531004a`  
		Last Modified: Wed, 22 Oct 2025 06:13:52 GMT  
		Size: 428.9 KB (428925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c83a1dda704af539edd6e9cd592c01c86fa307d2f3d7b7d20acf45b333435950`  
		Last Modified: Wed, 22 Oct 2025 06:13:53 GMT  
		Size: 7.7 KB (7656 bytes)  
		MIME: application/vnd.in-toto+json
