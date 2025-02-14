## `sapmachine:17-jdk-alpine-3.21`

```console
$ docker pull sapmachine@sha256:ae2903bea07d1416e147ddcd4fb2629447fe02462bb6d9f573b890bcd8d489f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:17-jdk-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:58c34d9e202d9a45c36ccd8d6ca338d13380a61df955d4d349d7a6292101d159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.2 MB (204164868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1deacda827e215d80294ae545f5a589bee90f3149d9eae860ece5f7be993d494`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-17-jdk=17.0.14-r0 # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-sapmachine-jdk
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0458479c062774b18347e0cb6c7696b9b580472cb1a482b9c24ba06ec083ea95`  
		Last Modified: Fri, 14 Feb 2025 21:20:22 GMT  
		Size: 200.5 MB (200523153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c4fd32daf49e267ea019452f31efbf57f0e99768177484d2f8ba2d3832a6f6fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.3 KB (516348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f5c82f81b6a9d4444aee86d0eeb5095caafe3eb368da9d9deda209bc2c7d39a`

```dockerfile
```

-	Layers:
	-	`sha256:17fc3f74a72e676d823a63d8333c93c2c4e2f7f2c9b4d06be6c21da4a994b341`  
		Last Modified: Tue, 28 Jan 2025 01:30:48 GMT  
		Size: 508.0 KB (508032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b67af8e92767c4f89e912f9217f04a456816959e6a61b75d93e3c628128aabb1`  
		Last Modified: Tue, 28 Jan 2025 01:30:48 GMT  
		Size: 8.3 KB (8316 bytes)  
		MIME: application/vnd.in-toto+json
