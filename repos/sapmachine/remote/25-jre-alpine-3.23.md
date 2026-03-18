## `sapmachine:25-jre-alpine-3.23`

```console
$ docker pull sapmachine@sha256:83ec031a517700266fb4950bb785f6bedc6f70c37c88771fd0fa1d86c246881c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:25-jre-alpine-3.23` - linux; amd64

```console
$ docker pull sapmachine@sha256:70d96455d1c3d2bfbff568520d57767a326361782fdf6601c01d3e62cae6e582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62251116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1214904d9d034f0977a8d200445e781cb224f89726207537a55900cf2a3539f7`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 18 Mar 2026 17:50:36 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-25-jre=25.0.2-r0 # buildkit
# Wed, 18 Mar 2026 17:50:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-sapmachine-jre
# Wed, 18 Mar 2026 17:50:36 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b19df56f6c6f72389e502d955024723cff547f2962552f4f6e412476a1336a`  
		Last Modified: Wed, 18 Mar 2026 17:50:50 GMT  
		Size: 58.4 MB (58389295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-alpine-3.23` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c51defe28d39e102468f64cb9c02253e12716e9a5e5d7ffa249dccaf268a424f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.4 KB (441365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88fc77561c6aef75d48decee1727be643193b6c40ad6e92d70a9ce2947a382b4`

```dockerfile
```

-	Layers:
	-	`sha256:34e85a0076ee6252282b7662c798c1d94e1d1ed323e3323905755502eb7bb0a7`  
		Last Modified: Wed, 18 Mar 2026 17:50:47 GMT  
		Size: 433.1 KB (433106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec3beadb2e736b73b93245d1a1d0d829f2a55e72d1e5fd56c20b1fde584c291b`  
		Last Modified: Wed, 18 Mar 2026 17:50:47 GMT  
		Size: 8.3 KB (8259 bytes)  
		MIME: application/vnd.in-toto+json
