## `sapmachine:24-alpine-3.22`

```console
$ docker pull sapmachine@sha256:deee44695389ec2c1eec3501064d154fba68bf19d8e8eb64e037d26c1604b560
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:24-alpine-3.22` - linux; amd64

```console
$ docker pull sapmachine@sha256:458dfd6f7afc5d8832a99821e1acce103f902de5d15e21c28e5b3f36b977ccdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.1 MB (237075932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:471c5df532d7b6377c78021b5962e1dd55fb7be4ed03eca7a7b62148207dc93f`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-24-jdk=24.0.2-r0 # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-sapmachine-jdk
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff1e1322546305eaac50411914dff0e3037102f3006cd3df317cfab2fa5cab9`  
		Last Modified: Wed, 16 Jul 2025 06:31:11 GMT  
		Size: 233.3 MB (233276243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-alpine-3.22` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8bdce6cd899d62d85c1b5fe6fa075d6805938e364b42820f576fdbdecf3eef7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.7 KB (515685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:328c2c33b421ff05a5afaca7dd13a82145f780be2cc514e61e149638c995b3f4`

```dockerfile
```

-	Layers:
	-	`sha256:43a15c201cbc007438cd12d6a10c054f3def6558542bf904bbdeede38d377990`  
		Last Modified: Wed, 16 Jul 2025 00:09:36 GMT  
		Size: 505.5 KB (505488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49e7f147e9e066deab6cf640ad582cae8c2ef29f7e3539387f5559c0555f6dd7`  
		Last Modified: Wed, 16 Jul 2025 00:09:37 GMT  
		Size: 10.2 KB (10197 bytes)  
		MIME: application/vnd.in-toto+json
