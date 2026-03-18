## `sapmachine:21-jdk-alpine`

```console
$ docker pull sapmachine@sha256:211e88084c9012538c9273eac6715428baea1b2f1e87b0e9fb0e01b21ff7c28d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:21-jdk-alpine` - linux; amd64

```console
$ docker pull sapmachine@sha256:6d57176133889df6a5b750ed6b1a1ce1c75bf7771d048d089857e66cf6fa5926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221767372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e158bc0a2250e2daad528ed3154206557310d21dbac5457d8694394c1e36d0c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 18 Mar 2026 17:50:48 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-21-jdk=21.0.10.0.1-r0 # buildkit
# Wed, 18 Mar 2026 17:50:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-sapmachine-jdk
# Wed, 18 Mar 2026 17:50:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f39ff2d8fd3b2ffd3214d567c517e49de39e2181d89ae3bea45ad5cab389290a`  
		Last Modified: Wed, 18 Mar 2026 17:51:11 GMT  
		Size: 217.9 MB (217905551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-alpine` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5501eefc6ada2a6c0271d5ebbe8a908c7bbc12c44383dbf0609e18a7e0d9d39b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.9 KB (522881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94dab25d411170aa1e11cb9f1ba2bd8ea22899a94fcb0142ee6c03bcf394bc40`

```dockerfile
```

-	Layers:
	-	`sha256:4792a37bfcdc237d7287fbc59424d706714379f91f967c09bd7e55dc8d8512f4`  
		Last Modified: Wed, 18 Mar 2026 17:51:04 GMT  
		Size: 513.9 KB (513934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26e07480e223523153d27afd6b8209e5cdf14e61e00fb6d116e7980561f9d142`  
		Last Modified: Wed, 18 Mar 2026 17:51:03 GMT  
		Size: 8.9 KB (8947 bytes)  
		MIME: application/vnd.in-toto+json
