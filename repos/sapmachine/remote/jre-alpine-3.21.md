## `sapmachine:jre-alpine-3.21`

```console
$ docker pull sapmachine@sha256:360645c8d39f2d826678240a78fc1d5ee67999dcd9c982366fe0f81fd4076db6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:jre-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:651cd95ff574d29452231b97289cc80f218dc3ea5fb607f7c7a91fc4af12d4dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62854443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55be7d1cecfda421abee50420fd9e397a3b5da1dad1ab222f2d8a478913faace`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 23:03:03 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-26-jre=26.0.1-r0 # buildkit
# Tue, 21 Apr 2026 23:03:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-sapmachine-jre
# Tue, 21 Apr 2026 23:03:03 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120b55c637c020b3644722b52d93b746ab822bc8d8a56d7d054f2f5a4ed7ea33`  
		Last Modified: Tue, 21 Apr 2026 23:03:16 GMT  
		Size: 59.2 MB (59207568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ea6fb0b926b40f964e7d7a7bdc602802a177f777603e66fa767de3d30d391a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.2 KB (438236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:516772ff55b4c71ca3f65e3c13c87e831642bae04edabad5bd7b9c0ab795e944`

```dockerfile
```

-	Layers:
	-	`sha256:dc1c5e3ee85eb43825abfa7e094f1b67b881bcf0e7ce235f3f4449072288038a`  
		Last Modified: Tue, 21 Apr 2026 23:03:14 GMT  
		Size: 431.0 KB (430955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f427f049cfc01cc1f5dc350fb65841a1caaa4c40e12e096f7b0d6a9b67b6f18`  
		Last Modified: Tue, 21 Apr 2026 23:03:14 GMT  
		Size: 7.3 KB (7281 bytes)  
		MIME: application/vnd.in-toto+json
