## `sapmachine:jre-alpine-3.22`

```console
$ docker pull sapmachine@sha256:c89e107b253b114db0e54fc281a5100c26cb5da4794295c1fb5b421ea02908f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:jre-alpine-3.22` - linux; amd64

```console
$ docker pull sapmachine@sha256:bb851964ea8a79d09ec45fa46461841796dc92b332efaeab0cd620b5c82554a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63142012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a7e838ed50c9c12341424e04cb6c644fbd1ed0ec933d8d8aff2c301c4b4a9ae`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 18 Mar 2026 17:50:12 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-26-jre=26-r0 # buildkit
# Wed, 18 Mar 2026 17:50:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-sapmachine-jre
# Wed, 18 Mar 2026 17:50:12 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e13dbb5a9414cd7cdfe74af29f67df39d85f665881d39f08e8cbe5750d70b37`  
		Last Modified: Wed, 18 Mar 2026 17:50:24 GMT  
		Size: 59.3 MB (59337137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-alpine-3.22` - unknown; unknown

```console
$ docker pull sapmachine@sha256:124a4a7b1fc9608fce4981230ba435266f071901d9e851a7b1cc8e3dd7ad7809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.8 KB (436798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bae2256407379881f503dc4014de4028adb71678b01205fee294c6fc855fa74`

```dockerfile
```

-	Layers:
	-	`sha256:308cd1a8b03bc1c323687846fdd274c938ab8cf748870402d52410090e8c7b7e`  
		Last Modified: Wed, 18 Mar 2026 17:50:23 GMT  
		Size: 429.9 KB (429863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9b3fd94370b1e8c491a9a30450471b6d0d9ed3e2ef20daa184d7b29875102ee`  
		Last Modified: Wed, 18 Mar 2026 17:50:22 GMT  
		Size: 6.9 KB (6935 bytes)  
		MIME: application/vnd.in-toto+json
