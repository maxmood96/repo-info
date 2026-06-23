## `sapmachine:25-jre-alpine`

```console
$ docker pull sapmachine@sha256:faa6c7953712ab29eebdfccdbf6f70bd34dcc139ded85cbff5bc8dfe6855a511
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:25-jre-alpine` - linux; amd64

```console
$ docker pull sapmachine@sha256:12a6b1c88ffd08fac0bd6a9deff4d5370fbc2e9f62f744df1921470b978406a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62327403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a69dbb34547a2667c6e37edcfb849430a9d864944f4ab5cb308426936388b69`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:08:02 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-25-jre=25.0.3-r0 # buildkit
# Mon, 22 Jun 2026 20:08:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-sapmachine-jre
# Mon, 22 Jun 2026 20:08:02 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09999e6fa8afc22547185e167177bdf102d8b9ccc73089d7c8b9bcd2e5fddc2c`  
		Last Modified: Mon, 22 Jun 2026 20:08:14 GMT  
		Size: 58.5 MB (58482982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-alpine` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e68843598292252f5bf81252a69092cbedc2320b17f86272ca59ff687cf1bedd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.0 KB (442036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cafe7444479bb7b75d93fb394a95186cced76bb66dae2cf1283dd7d8514300e5`

```dockerfile
```

-	Layers:
	-	`sha256:9a6be0e74e909e598faa56a80b56dea37c4857ec226e39e4fa1a26675e76e0a1`  
		Last Modified: Mon, 22 Jun 2026 20:08:13 GMT  
		Size: 433.8 KB (433777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b6a5f24bcd664b84d40d68b6a35ee3cad69df17ed61664d5da797a22aad36d7`  
		Last Modified: Mon, 22 Jun 2026 20:08:12 GMT  
		Size: 8.3 KB (8259 bytes)  
		MIME: application/vnd.in-toto+json
