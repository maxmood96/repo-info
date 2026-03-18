## `sapmachine:26-alpine`

```console
$ docker pull sapmachine@sha256:b08c98ce470172ca0524d46b91fceb1c3b5539ec85a7c5e0ac98fab4e111fe6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:26-alpine` - linux; amd64

```console
$ docker pull sapmachine@sha256:8bcaaa276f2f9f30fb83eceb94ac363ed5a7afc0939aad5ad3df329405abd07b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (232042178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ff5183f051403ceef0c93e7383ff5fa3ee3642471c71c8bd831b35ff181828`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 18 Mar 2026 17:49:33 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-26-jdk=26-r0 # buildkit
# Wed, 18 Mar 2026 17:49:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-sapmachine-jdk
# Wed, 18 Mar 2026 17:49:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fbf0db29d01fe0b3c46be9a49967f1b0c7ce4fdcc98ccc48833adf218d9cb2`  
		Last Modified: Wed, 18 Mar 2026 17:49:56 GMT  
		Size: 228.2 MB (228180357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-alpine` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6f0850305079a8ce1e2ab8d440150ae929591f2341d4cef2f475f8064f9afc2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **509.4 KB (509358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b64600e1a1f9bd64f432c86089225b1dcfb1dc7085b5a0758094b9808e36ff`

```dockerfile
```

-	Layers:
	-	`sha256:21a01ff8d623f297cda471ff2e86a52b12d2f23654b3eb2f26a436ce69a0185b`  
		Last Modified: Wed, 18 Mar 2026 17:49:51 GMT  
		Size: 500.5 KB (500528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47344c3800258725b2e8dc0f1fea1cd66af98908c931e374ae7c8811251b321b`  
		Last Modified: Wed, 18 Mar 2026 17:49:51 GMT  
		Size: 8.8 KB (8830 bytes)  
		MIME: application/vnd.in-toto+json
