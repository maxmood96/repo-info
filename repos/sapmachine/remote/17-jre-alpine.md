## `sapmachine:17-jre-alpine`

```console
$ docker pull sapmachine@sha256:605f1eb6d075c599787f69cf8953359d7c3203e153279e0ac3ce3ea86221862a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:17-jre-alpine` - linux; amd64

```console
$ docker pull sapmachine@sha256:f238bcd9b7c9bcf64bd33e430fd75392b542534a98b69e78d19595ff93f1a4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57814618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef143353775b3f2cf55cb20458fdb81366ecb169d0fc14157fed05b829248bb9`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-17-jre=17.0.15-r0 # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-sapmachine-jre
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e946c4f7c8470dd31f60593f8ef8a925900c6bfd8d719793257119d375513e3`  
		Last Modified: Thu, 08 May 2025 18:15:43 GMT  
		Size: 54.2 MB (54172371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-alpine` - unknown; unknown

```console
$ docker pull sapmachine@sha256:75f7fc250ba1e3c6abe973403762b3d16312c05439fd31592f7d134e974237e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.4 KB (428450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d1072a0d5a3b3da1bd2498ebf6d6455aa89f1ed7b0dfde2cf4b98641fb3352b`

```dockerfile
```

-	Layers:
	-	`sha256:5ec08b7a701aa323249eef2db0b7bfc49f37f771a5dc05471281bfc3e0696e0e`  
		Last Modified: Tue, 17 Jun 2025 10:21:07 GMT  
		Size: 420.8 KB (420789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71a598c9f60d559c1918a957d1847921a444087a3230deed832afbc95abaf8ec`  
		Last Modified: Tue, 17 Jun 2025 10:21:08 GMT  
		Size: 7.7 KB (7661 bytes)  
		MIME: application/vnd.in-toto+json
