## `sapmachine:21-alpine-3.21`

```console
$ docker pull sapmachine@sha256:353da5a175c06271b836462e2c99f47aa0618db253da0b46996fc0f88dac3c33
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:21-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:0407f6943f05ce0b6f2bc2b49bc09913c59482a9f556a4835ac25360fdfc8a38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.3 MB (219320176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f02b9c9720a0e4b50c5b55d2594b7ba8ad473df704c6134476d7602586dbf92`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-21-jdk=21.0.6-r0 # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-sapmachine-jdk
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44cd8fab7c83e0922f76f9e41f692d96fb626fc7d50aadacc9b9b496391011a`  
		Last Modified: Tue, 28 Jan 2025 01:30:23 GMT  
		Size: 215.7 MB (215678461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:37ffaaf432ac87d07ee7cf241c93e5372f64b738c88119a22de0776103f78537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.2 KB (520181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b0cb740f21e9f0e347d6a6e634df8d452b0e3f458b342125a7b468f5fcd0491`

```dockerfile
```

-	Layers:
	-	`sha256:4f16f79af15434912395d306013de5b0783bbd8788ba62baee564924817a04a9`  
		Last Modified: Tue, 28 Jan 2025 01:30:20 GMT  
		Size: 510.9 KB (510898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f8f41fa4f2f6aa24320de9f13d056aa5404249f9773cf1f680f3074a1acf7c1`  
		Last Modified: Tue, 28 Jan 2025 01:30:20 GMT  
		Size: 9.3 KB (9283 bytes)  
		MIME: application/vnd.in-toto+json
