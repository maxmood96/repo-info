## `sapmachine:21-alpine-3.21`

```console
$ docker pull sapmachine@sha256:2824a00ff79538664de6088ece2d0e3041003730cff38ef0706d1e430e76aeb1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:21-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:57bc60a19c647c97fba8cb36c0488e7e78c905da45fa450af254ac5951dc77cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219442385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d6838415cc6ea02511a1643cbf7d3ea593737112f0ad760b915b87502b9f84`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-21-jdk=21.0.7-r0 # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-sapmachine-jdk
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cc1ce8a979745a416165455ef5c62115410102aafc4df5f44da1be5e2eea64`  
		Last Modified: Wed, 16 Apr 2025 16:14:19 GMT  
		Size: 215.8 MB (215800138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c444f189e17b32841ecd73c37eef5e12bb361b305b48b77107f50ab5ed94b8b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.2 KB (520187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1fde847207182492bc04a65210210ccfa97a3bd0d2826725ec9528a6175ebee`

```dockerfile
```

-	Layers:
	-	`sha256:f12207cfb4b335b486c926ebfd7d2e2651e11b5958e008aae384bc5e557578f3`  
		Last Modified: Wed, 16 Apr 2025 16:14:13 GMT  
		Size: 510.9 KB (510904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16d1f80f0b4f0c58067dc7d9a74b018d7915c4ef24cce2e91dceff08b2964633`  
		Last Modified: Wed, 16 Apr 2025 16:14:13 GMT  
		Size: 9.3 KB (9283 bytes)  
		MIME: application/vnd.in-toto+json
