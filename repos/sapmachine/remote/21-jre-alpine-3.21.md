## `sapmachine:21-jre-alpine-3.21`

```console
$ docker pull sapmachine@sha256:823708679b648243a0572c0765d32ef7f2c7e93a8389f13db8bb1b22720357e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:21-jre-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:1afdccd8b290a52339f4a649540beefea3e8113bb45ea98068ded74821a0d31c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63625985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6814285b2960451e814e809fb0fef07278e861edff0df74df0aabbcbd55971a2`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-21-jre=21.0.6-r0 # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-sapmachine-jre
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e1ca57af189f6c73db04b0d5e42073972374bf18f9b09327e6d5b90ec170c1`  
		Last Modified: Tue, 28 Jan 2025 01:29:50 GMT  
		Size: 60.0 MB (59984270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:690f0da91bf66b9c5cddfab7a82554a47d80f05b53661429cafbcb7bf2657d38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.0 KB (431011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca76e3e19ed66e4d41913d9be30f5699c21bdc816a0bd00350f2266908e7e35a`

```dockerfile
```

-	Layers:
	-	`sha256:2eecc4bf9dae7d35db57907401de7265c02dd514501a51461261cad7de0ba7a0`  
		Last Modified: Tue, 28 Jan 2025 01:29:49 GMT  
		Size: 422.7 KB (422705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e732d3b5505e7dadebb83b671995b78f975c1503daaa6835205ec644b25e5b66`  
		Last Modified: Tue, 28 Jan 2025 01:29:49 GMT  
		Size: 8.3 KB (8306 bytes)  
		MIME: application/vnd.in-toto+json
