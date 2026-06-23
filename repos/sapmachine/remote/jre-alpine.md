## `sapmachine:jre-alpine`

```console
$ docker pull sapmachine@sha256:2b8f7fb8714f85fc20a824819ccf016cfb1606745c96e78e7e106bb6fedebc24
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:jre-alpine` - linux; amd64

```console
$ docker pull sapmachine@sha256:ab4b72553a26dd1e1e21eb3dc7197bb218b34822adfeb8f5e06f5b7277db5a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63590568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e8ad03124b75dddac0affd57f32cec47e5e5686cc9d957a791ec16c1702d4d`
-	Default Command: `["sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:07:41 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-26-jre=26.0.1-r0 # buildkit
# Mon, 22 Jun 2026 20:07:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-sapmachine-jre
# Mon, 22 Jun 2026 20:07:41 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75f949043f9224fb429f032ffaecf712a917e869d29fdbf8104475dc646dfc7`  
		Last Modified: Mon, 22 Jun 2026 20:07:53 GMT  
		Size: 59.7 MB (59746147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-alpine` - unknown; unknown

```console
$ docker pull sapmachine@sha256:423a92cae60c7eb2836b1ca0b5d9573d12ece722c506582c8c9bc459e56665d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **440.1 KB (440078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d94a1be65c212ea8cc9bf1b638362ed1f91262d7a6a3a80ac663b541e8d09e`

```dockerfile
```

-	Layers:
	-	`sha256:7cdda4ecc68d0727fbfb0b93ce9d4c3ae6f9a33a4e7ea36e1afa79225becc71d`  
		Last Modified: Mon, 22 Jun 2026 20:07:51 GMT  
		Size: 431.8 KB (431836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:550c2449514876b18f9dae40f94e26d8e73e449eb0898cd67e851ff20b2d4921`  
		Last Modified: Mon, 22 Jun 2026 20:07:51 GMT  
		Size: 8.2 KB (8242 bytes)  
		MIME: application/vnd.in-toto+json
