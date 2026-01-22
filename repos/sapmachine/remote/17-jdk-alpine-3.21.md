## `sapmachine:17-jdk-alpine-3.21`

```console
$ docker pull sapmachine@sha256:d6213113390a05212157ac6093336abf3c86594cef6ff5e6e8b6007cf3cc0506
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:17-jdk-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:70cb64fd6f7c080b8461f45a2ee54e33dbec1d8e358cbe84183aede01fd8c969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.9 MB (205858054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e006384a7b303651f78e45b03815329f77847e6025df84ca6005683625cfbbda`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 20:05:08 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-17-jdk=17.0.18-r0 # buildkit
# Wed, 21 Jan 2026 20:05:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-sapmachine-jdk
# Wed, 21 Jan 2026 20:05:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Sun, 07 Dec 2025 13:55:07 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9aacd58af14d3f689b733e315991379248bc210c2062806dd42231782d6ec66`  
		Last Modified: Wed, 21 Jan 2026 20:05:27 GMT  
		Size: 202.2 MB (202215485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f61d7fa63711ccc5584b74e6b833c45650584c6180dec725ae63d95528b88074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.1 KB (521120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c1546bb0b3ee7ef006d9c07d0da76c26868904ec97471f1b610c9af28a5b43`

```dockerfile
```

-	Layers:
	-	`sha256:62cf94005b216caf9cc0819cf8024ca1b2779d5a96409826cbf84322872e40c4`  
		Last Modified: Wed, 21 Jan 2026 22:06:31 GMT  
		Size: 513.5 KB (513497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f64545a7effb19c850b214e9473d4f0be70d77069a9cfd935d2938ec1d5d3014`  
		Last Modified: Wed, 21 Jan 2026 20:05:22 GMT  
		Size: 7.6 KB (7623 bytes)  
		MIME: application/vnd.in-toto+json
