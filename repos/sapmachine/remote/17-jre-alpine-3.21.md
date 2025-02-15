## `sapmachine:17-jre-alpine-3.21`

```console
$ docker pull sapmachine@sha256:d404f4ecb790b7927ba382c2b7c3a04a6f9594b2aeb6ba8adcd4b5149860c0a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:17-jre-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:4fd190fe2837ebbde07ee9ad3f22830cc67d255683c6d00710c3e9d81611967c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57798756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d35975dc50d95b375797e597c8f1808d3c705137ced3390d9b019d9d5359ca8`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:16 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["/bin/sh"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-17-jre=17.0.14-r0 # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-sapmachine-jre
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3214b4d11fe2ccc8244b0c8ee6fc8b1ebeaf676eb67b7173f27714db83b59a4b`  
		Last Modified: Sat, 15 Feb 2025 21:05:24 GMT  
		Size: 54.2 MB (54156509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b4ee12b0b87d30530cdf14cee2b6160ffcea2f99fc09d7cddac5dd08adcae5b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.4 KB (428450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7974b4d1db00cb9ac67aaaf24c93f9339f259bf1b58e9d0757acdba675f292e4`

```dockerfile
```

-	Layers:
	-	`sha256:d606ded152da90049c12310bab2a975728909ca6aecce0494bf71029d3e81588`  
		Last Modified: Fri, 14 Feb 2025 22:05:08 GMT  
		Size: 420.8 KB (420789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a8226509db77531d7f0bba517b8a9e8bdc414d6b1cb198f65a7c3591f9d13ae`  
		Last Modified: Fri, 14 Feb 2025 22:05:08 GMT  
		Size: 7.7 KB (7661 bytes)  
		MIME: application/vnd.in-toto+json
