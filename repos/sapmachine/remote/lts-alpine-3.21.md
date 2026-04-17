## `sapmachine:lts-alpine-3.21`

```console
$ docker pull sapmachine@sha256:6223cb0152ba00f79bbd091c6b75d28cde02b497c8a233565030f3f87874eeb5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:lts-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:b99b6c66136f1c408dfe86337cea0a7bbef0c32a38dc98ec6124a0ca36b7132f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226262064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ac4520bb1084251f10e20321d08e35d70af79d46c65f5eb07d5d688552ba87`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:34:36 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-25-jdk=25.0.2-r0 # buildkit
# Fri, 17 Apr 2026 00:34:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-sapmachine-jdk
# Fri, 17 Apr 2026 00:34:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a69315a544a50795934df2cce837601f284069b3159fddf3cdc01ae4e236a4`  
		Last Modified: Fri, 17 Apr 2026 00:34:57 GMT  
		Size: 222.6 MB (222615189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4c183d9fb27d3d05b8dfad77bb4ab02f8b2bec61c3676d63dc9e64c8fc848c4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **513.0 KB (512968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f336c4c9ca2f2b001c12a6f62f90ee898d2d71a7d6b9616cc0964ac133b27d30`

```dockerfile
```

-	Layers:
	-	`sha256:d862af1c805cf018c24f72649502cfc7d0e5ae5cd8a6e05c77b5658dc477387b`  
		Last Modified: Fri, 17 Apr 2026 00:34:52 GMT  
		Size: 504.7 KB (504699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed6c4fa5b11a355b19fa1f8104201dc93e5be5d8b538a715144587cd61af3bb1`  
		Last Modified: Fri, 17 Apr 2026 00:34:52 GMT  
		Size: 8.3 KB (8269 bytes)  
		MIME: application/vnd.in-toto+json
