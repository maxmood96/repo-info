## `sapmachine:23-jdk-alpine-3.21`

```console
$ docker pull sapmachine@sha256:a9c259d43a2f6d27a37cb89e5104150a7696f0e9d0ef31ddc0c120260cc9f95e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:23-jdk-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:61c5614f474160e278aceb1ef807ee22d455eee31bd3b4fe89879326ca1d7ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.0 MB (226952810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d1c47dedb17ab82c69ba50b7c97397a9d62c85c43eadb1c03ac3553e29cc07f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 27 Jan 2025 13:39:22 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-23-jdk=23.0.2-r0 # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-sapmachine-jdk
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23b29555d613ca7946f6c4ff7726d8d38bffdd977dc2d5020a2b0c3efab5a84`  
		Last Modified: Mon, 03 Feb 2025 21:09:11 GMT  
		Size: 223.3 MB (223311095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jdk-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4561feb26d7375e1febe41f486b8f1deea3d0a58f0d39e5ce784b4b2006bdaa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.1 KB (522097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c8a38423752ed2aada3b1c71891a71ade55ae2647d993c1b10a7fe4ca683f80`

```dockerfile
```

-	Layers:
	-	`sha256:47f093a55abe6932961a98ded24f6911ee177ded2de137e22d7c379ccb8542bf`  
		Last Modified: Tue, 28 Jan 2025 01:29:48 GMT  
		Size: 512.8 KB (512839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2287de62cd3cd71c8d1d830fefd6c6890fea07b9e90e9bfe6f97e443af98b02b`  
		Last Modified: Tue, 28 Jan 2025 01:29:48 GMT  
		Size: 9.3 KB (9258 bytes)  
		MIME: application/vnd.in-toto+json
