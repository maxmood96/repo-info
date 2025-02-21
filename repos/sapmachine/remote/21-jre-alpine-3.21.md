## `sapmachine:21-jre-alpine-3.21`

```console
$ docker pull sapmachine@sha256:6375192b34753cc532ed7716e5d3ce15d31709fe16dc8cd1602f0d9cc9d036cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:21-jre-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:2bd085c1e5b7f207ac1283ae34756daf6d348b328ea164166baceb184cc6b63c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63658659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a3a1a051185cacfaa21e9e3de1fd731b1b6e6abb7a3d9a3bca8c8766b6b4308`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:13 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["/bin/sh"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-21-jre=21.0.6-r0 # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-sapmachine-jre
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420c9c61c8444f90d823e3e14ec9fb6265183f93e1cb279c4f92a58a6df7d66d`  
		Last Modified: Fri, 14 Feb 2025 19:14:17 GMT  
		Size: 60.0 MB (60016412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e17a7c958e3e61adfd1655198ae9bb6500664e7d2813f0c3825d813238b58f9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.0 KB (431017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d6a88701f274869b63fa5b10b4ca357e7f6204d64f1d23ae2a64c1d4c4dc86`

```dockerfile
```

-	Layers:
	-	`sha256:1c9896a6d6acd6426500499624fe0f367ff23dabd8502b4fcc4db100a743b4dd`  
		Last Modified: Fri, 14 Feb 2025 19:14:17 GMT  
		Size: 422.7 KB (422711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dc25bae705e555a336f56ddb86265f3276ed61c01bdb2ec7662202b2f7d8fbc`  
		Last Modified: Fri, 14 Feb 2025 19:14:16 GMT  
		Size: 8.3 KB (8306 bytes)  
		MIME: application/vnd.in-toto+json
