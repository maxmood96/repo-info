## `sapmachine:lts-alpine-3.21`

```console
$ docker pull sapmachine@sha256:675764f9454f80741f3f389973ba0e5e7749aeed16b130240f91edcfe1b748c0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:lts-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:93466489650e3fcfa9d559d32dea77360df300f21ceb943f10c62a582554cf46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.5 MB (226507052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f31ed0e7fe10597f54e900545cb33b51e3ab396caf25116e43a50604ec11c66d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 23:04:08 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-25-jdk=25.0.3-r0 # buildkit
# Tue, 21 Apr 2026 23:04:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-sapmachine-jdk
# Tue, 21 Apr 2026 23:04:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f709c7cf1a10fd68d239fb1ea5d2fb007049d049911a502bc124896035180b`  
		Last Modified: Tue, 21 Apr 2026 23:04:31 GMT  
		Size: 222.9 MB (222860177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5f58736e2ba05aa4c4b8d1a1b45d7c8a30d61954fbb68dced3f8257b24180d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.6 KB (513612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f52f9ed75fdcef97a4d07323f003103a92f141eb99a193834d79bb474a13fb`

```dockerfile
```

-	Layers:
	-	`sha256:a4661f96c6df6b492229b225f20361b04488c78b8bb921503217ec8da22567a1`  
		Last Modified: Tue, 21 Apr 2026 23:04:26 GMT  
		Size: 505.3 KB (505342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22f54006ec96de6c8e464798a988ed804635aae5f365dde41b644bcd868669b4`  
		Last Modified: Tue, 21 Apr 2026 23:04:25 GMT  
		Size: 8.3 KB (8270 bytes)  
		MIME: application/vnd.in-toto+json
