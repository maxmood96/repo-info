## `sapmachine:26-jre-alpine-3.23`

```console
$ docker pull sapmachine@sha256:1d86a7aa068c2a76f094c91d48df6e2059ba85c030f94d204abf4b2c58b4a93f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:26-jre-alpine-3.23` - linux; amd64

```console
$ docker pull sapmachine@sha256:eea1c83b4a0bd76103e8a6ceb38ed3c4ac22165ffc73f992db69f1f7940c2d69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63609536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7bd05855c30aceadb9cc352e6b62233ec791d83f192a94f35f2550c97e929d9`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:57:49 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-26-jre=26-r0 # buildkit
# Wed, 15 Apr 2026 20:57:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-sapmachine-jre
# Wed, 15 Apr 2026 20:57:49 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0687c212d16c36e5488006222f9598646c40844f3811a80b9754ea9028723815`  
		Last Modified: Wed, 15 Apr 2026 20:58:02 GMT  
		Size: 59.7 MB (59745347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jre-alpine-3.23` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d074e5fbfc75bbd36e04b365dea7ff657fa0c9255c81d2d10d4bc96ae914d25f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.7 KB (438723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586c51519603b4e539717e6e93a3073d826312a8c7c675edafbff72af5612afd`

```dockerfile
```

-	Layers:
	-	`sha256:13cb69f3835c414a768968309be7ad1a7d00b9b529cedbcce3b77ea2a8a54c7d`  
		Last Modified: Wed, 15 Apr 2026 20:58:01 GMT  
		Size: 431.2 KB (431154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64bff0e45c75711efd68bcbd7f5ad33fec8eed6996a82584ca941b6f4665364f`  
		Last Modified: Wed, 15 Apr 2026 20:58:01 GMT  
		Size: 7.6 KB (7569 bytes)  
		MIME: application/vnd.in-toto+json
