## `sapmachine:17-jre-alpine-3.21`

```console
$ docker pull sapmachine@sha256:f5a2b8e1c29ce879cf2cd42ffa96d105ad28bbe84e03bbd53f93effaed96252f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:17-jre-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:5eda0ced56578317d4a13bac861f6cd49dfb4b6ee9f6d449b86cfedb9ccc63da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57765063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41fc4476fe8fd0f289cdec61746fff72133bbb267a540d820e4238abf40de414`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-17-jre=17.0.14-r0 # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-sapmachine-jre
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d7dc96ac6fad215933e83987f5ac3a34302581f34324165dcaf1789c03fbaa`  
		Last Modified: Wed, 12 Feb 2025 10:08:31 GMT  
		Size: 54.1 MB (54123348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a05d9571244d7f0cd7baf2388a029c32ef223e3cf51c3b0b67c6a294e34f6b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.4 KB (428444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d79becd5d40c28fc4892fa48ce6ef34a240dab8c19d35b945a00711de6ab85a`

```dockerfile
```

-	Layers:
	-	`sha256:b0797e2d294a5a2c8e0757557947c647d3b9a93dff084fff05e3213afaeeb039`  
		Last Modified: Tue, 28 Jan 2025 08:51:01 GMT  
		Size: 420.8 KB (420783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d932a9ad519f08d3576761d0375aa564c79b15aeeeadaccd47a4f5a5c02beeb1`  
		Last Modified: Tue, 28 Jan 2025 08:51:01 GMT  
		Size: 7.7 KB (7661 bytes)  
		MIME: application/vnd.in-toto+json
