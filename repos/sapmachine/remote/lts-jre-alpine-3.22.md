## `sapmachine:lts-jre-alpine-3.22`

```console
$ docker pull sapmachine@sha256:8673f305b48c4deda5eed3928a19323124be6502ac14cc9a437322a676800cee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:lts-jre-alpine-3.22` - linux; amd64

```console
$ docker pull sapmachine@sha256:af79a224a6a013adc64c063cd9af0488f3d8a110bc8f6fb55da64978e5446c7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61862987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37f1b3e80863a3857a63fe93776b4e95a95aa73154f2e80e523c2e32cbd84339`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:08:23 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-25-jre=25.0.3-r0 # buildkit
# Mon, 22 Jun 2026 20:08:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-sapmachine-jre
# Mon, 22 Jun 2026 20:08:23 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e595bdc54e7e4771385c4dc4b9fc9d4f233317dd9ef415e22d37e996824d37f6`  
		Last Modified: Mon, 22 Jun 2026 20:08:34 GMT  
		Size: 58.1 MB (58075392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-alpine-3.22` - unknown; unknown

```console
$ docker pull sapmachine@sha256:58fe883ae53bf5c15ea889de9a17215a585e2a284f45125e7b5b0ee6d6293f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **439.4 KB (439443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:685f1eea1d762c27f700aa5fb2575f6679381d077bb69e8c1e908a549b9470e6`

```dockerfile
```

-	Layers:
	-	`sha256:5778076713c3f128ed5159a2ba91bc0a92164eb42598ceec1fa0edc022ddee82`  
		Last Modified: Mon, 22 Jun 2026 20:08:33 GMT  
		Size: 432.2 KB (432155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:996c0b571922045871a798ce77860309a9e095e004714d25a140848701b56c98`  
		Last Modified: Mon, 22 Jun 2026 20:08:33 GMT  
		Size: 7.3 KB (7288 bytes)  
		MIME: application/vnd.in-toto+json
