## `sapmachine:26-jre-alpine-3.21`

```console
$ docker pull sapmachine@sha256:ca85bbab229571f125bdc3bc804c7203bef552012c796096464c44b0a27a21a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:26-jre-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:334e3e7e4c1a8665060a4a7f25e7d77013844402d7fa5fb902b59cc8be6be3c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62844773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23064a76818b95677d1d6c6fc5d8123dd0214e12ec7168b1c3c80aa7b58c3268`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 18 Mar 2026 17:50:21 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-26-jre=26-r0 # buildkit
# Wed, 18 Mar 2026 17:50:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-sapmachine-jre
# Wed, 18 Mar 2026 17:50:21 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a588df401a1b15596c4306c0198799e46201d196db5a2d6d1f9779f84533a0ab`  
		Last Modified: Wed, 18 Mar 2026 17:50:33 GMT  
		Size: 59.2 MB (59201031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e1a226af1262bb220439c717901b72cff84fc7f07ff9f47e696fe5c2a43e3e4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.5 KB (437532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:535b7159fd337baaa8b572ff8f1c47db61a0ae67cbfb69384feb5fd8a795189f`

```dockerfile
```

-	Layers:
	-	`sha256:c2fb47055e8bb22a1a651be1a1be7aff4ce499c0c2bd3ce8ececc809081a6cec`  
		Last Modified: Wed, 18 Mar 2026 17:50:31 GMT  
		Size: 430.6 KB (430597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9315b07ef3c9d031eaa961982074dda8fd76fcf151a4745d094eed5582800aae`  
		Last Modified: Wed, 18 Mar 2026 17:50:31 GMT  
		Size: 6.9 KB (6935 bytes)  
		MIME: application/vnd.in-toto+json
