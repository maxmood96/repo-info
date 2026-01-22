## `sapmachine:17-jre-alpine-3.22`

```console
$ docker pull sapmachine@sha256:131b9032a3a9a7bbfb406de3cb2e4a64140577d4a81cc61738d5d6bd3536775a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:17-jre-alpine-3.22` - linux; amd64

```console
$ docker pull sapmachine@sha256:6dbeb797825c9f5d108922be53144f4120fa543bd82b7207589e321d5389f4ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.8 MB (58806603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41f1a6cd80b8ebe877f7719db5d702cf35129c722be4c23083cdbbe1ad2e64cd`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 20:05:04 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-17-jre=17.0.18-r0 # buildkit
# Wed, 21 Jan 2026 20:05:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-sapmachine-jre
# Wed, 21 Jan 2026 20:05:04 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ebb13e12e4ee8336688bcb332291f9fa595b09a559bff8b0b28033de5c3624`  
		Last Modified: Wed, 21 Jan 2026 20:05:15 GMT  
		Size: 55.0 MB (55004151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-alpine-3.22` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9f6c3444573d667aad5d8de53cc27b0f06670f95b65dfced71e247bbfe47bea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.6 KB (433606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f8bb26d4fb2c3cb6b9ecd99f02c8072f10e33cd03db488356f61f99eee0bb1`

```dockerfile
```

-	Layers:
	-	`sha256:b1b9450fd9d3cae0b3c74a9c148d1b73c2beed46abd459b84b7391a171fd7ff6`  
		Last Modified: Wed, 21 Jan 2026 22:07:43 GMT  
		Size: 426.0 KB (425996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3598208d3e02065532b6513c1a69a916bb42be435e18cc3151ed0359c02ed66e`  
		Last Modified: Wed, 21 Jan 2026 22:07:41 GMT  
		Size: 7.6 KB (7610 bytes)  
		MIME: application/vnd.in-toto+json
