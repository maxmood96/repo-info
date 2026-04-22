## `sapmachine:lts-jre-alpine-3.22`

```console
$ docker pull sapmachine@sha256:a341b99d12ec06c71efe4ca90b71eff123490b497ec059fcf0b2a64ad6bb3455
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:lts-jre-alpine-3.22` - linux; amd64

```console
$ docker pull sapmachine@sha256:1ab3f651fd37e9adb050ac211315bf7480a20ca4e5c0df161368df3a2bce2cec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61883290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06bcd1c010793b5536adc05559e343fad3a6d397f9e98ef572a8fd826e19087d`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 23:03:57 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-25-jre=25.0.3-r0 # buildkit
# Tue, 21 Apr 2026 23:03:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-sapmachine-jre
# Tue, 21 Apr 2026 23:03:57 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4188836184bf0b7751b714e4bb6143d6fed46410948940ee9a51433a9ce4f79b`  
		Last Modified: Tue, 21 Apr 2026 23:04:09 GMT  
		Size: 58.1 MB (58075101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-alpine-3.22` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a09f6b3fc9ee997a0e4dff243ddf5f06973238626d2adf3a0225357e14d1f840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **439.4 KB (439439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6faec8cf03aa782f4e2f469321a534395091e394b3530ab7628637c2c4cc0238`

```dockerfile
```

-	Layers:
	-	`sha256:94f30ba787e139485266e65f08b4498d0bf62fbebfd9143cda6c31cb8673e5d6`  
		Last Modified: Tue, 21 Apr 2026 23:04:07 GMT  
		Size: 432.1 KB (432150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98e2fee980852450bf0c8526431fb3e1f52b72ad91881b8b8cb973785e036488`  
		Last Modified: Tue, 21 Apr 2026 23:04:07 GMT  
		Size: 7.3 KB (7289 bytes)  
		MIME: application/vnd.in-toto+json
