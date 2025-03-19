## `sapmachine:jre-alpine-3.21`

```console
$ docker pull sapmachine@sha256:3152e5de8242e20ff9bf128683cdfae184e8044464e29269832bacab459a5970
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:jre-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:538edbb9d72275dd35bee6ac35c64c80fd2298c77e9a2a57c1dd3e26dfc09096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71580143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd8184c4c8bfd89299fb103065ee7513534f7a69de0f661bb6675161f64dee5`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-24-jre=24-r0 # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-sapmachine-jre
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd44310900c485ac2c69f4de32bbdaa05b038ac326e5b81ace3ee8b6532bbb9e`  
		Last Modified: Wed, 19 Mar 2025 20:32:49 GMT  
		Size: 67.9 MB (67937896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6b675c7ddfc4eb3ebba6bc0d411d5e7e01bb4a87836bdfb8d66c4a64a11e552f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.8 KB (436780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a268c6690725e2c360447ae2215741f54ca6b21801f36f2c4721e59a4042cf74`

```dockerfile
```

-	Layers:
	-	`sha256:68838038208bfe7537e7c68c39520f0ea95c693287c33193f28ab6e5a875991c`  
		Last Modified: Wed, 19 Mar 2025 20:32:48 GMT  
		Size: 429.2 KB (429164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee7235a37ffdfc55346c1e97ad1712f2b59645d3334ce2efc45dab05e7142ba0`  
		Last Modified: Wed, 19 Mar 2025 20:32:48 GMT  
		Size: 7.6 KB (7616 bytes)  
		MIME: application/vnd.in-toto+json
