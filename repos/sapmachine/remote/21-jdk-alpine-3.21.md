## `sapmachine:21-jdk-alpine-3.21`

```console
$ docker pull sapmachine@sha256:1aa8c32d8f32c11748914b8b21d6ee3c674ec2e9e7618937655886fef9d5af26
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:21-jdk-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:e40cfa959301b99cf0804a5dafcf2ad28220c2db409635f1da62e09af46ad378
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.2 MB (221202164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fe4e7f9a1a1198002f91c2bc73e3b3d62efe2f688738b02e98a949545aa0a7c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 23:05:10 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-21-jdk=21.0.11-r0 # buildkit
# Tue, 21 Apr 2026 23:05:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-sapmachine-jdk
# Tue, 21 Apr 2026 23:05:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62ab9dea66c8f499551288d6282055ec0dbe5a84ca20d3dd69f68ac191aa381`  
		Last Modified: Tue, 21 Apr 2026 23:05:31 GMT  
		Size: 217.6 MB (217555289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a183983c601c59deaff17b1add1aa1b2595555db58a654b6f20d2b24e2dcb9d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.7 KB (523665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94eb32f8fc1a58eb952668b68dd653181d989bb6625dafa06ca4c68f5674395`

```dockerfile
```

-	Layers:
	-	`sha256:550e75f9682c6a04f460501a0f5e6fb1b69c8e514a0ddec027a066ea9949745a`  
		Last Modified: Tue, 21 Apr 2026 23:05:25 GMT  
		Size: 516.0 KB (516042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc04fe8f4ad6305272b60821f17721ff65da9c97ec85114d68b1b8c5afc503c6`  
		Last Modified: Tue, 21 Apr 2026 23:05:25 GMT  
		Size: 7.6 KB (7623 bytes)  
		MIME: application/vnd.in-toto+json
