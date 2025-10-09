## `sapmachine:lts-jre-alpine-3.22`

```console
$ docker pull sapmachine@sha256:e80fee6c3ade6d164f355d0981ba9acf75d85ff8259dc1004bd21cade08dfdd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:lts-jre-alpine-3.22` - linux; amd64

```console
$ docker pull sapmachine@sha256:035b61c90d9d96087077ccbe066245a97e5393af3e114bfef4ee292f1155614a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72941042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:953b4b2ed9a5ad1ad2b0e12ab3819a6e4c0c876b089c93c72067c82035f0a838`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 17 Sep 2025 04:28:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-25-jre=25-r0 # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-sapmachine-jre
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1439a69ae31cc6c6557fdf48cf7a2986072da6fa26e359bb078180b49cc07e12`  
		Last Modified: Wed, 08 Oct 2025 23:19:58 GMT  
		Size: 69.1 MB (69138590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-alpine-3.22` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f5b9b18cbc6e18d4642abd21151030e79e8363f43197d75802f0b11466630202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.8 KB (438840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9cb693cf843c29c6edbce554fb803688ac6fcb696fc47280afa28b26851087e`

```dockerfile
```

-	Layers:
	-	`sha256:7355bb1a19dafa3a4f19eb0f1538a4b3a6c979d51758436f221c6787610192a2`  
		Last Modified: Thu, 09 Oct 2025 00:07:24 GMT  
		Size: 430.6 KB (430574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:949d9268bf5d02fe726650b1459c84c3b02a051a3ccda2d7ab0e90907bd90bab`  
		Last Modified: Thu, 09 Oct 2025 00:07:25 GMT  
		Size: 8.3 KB (8266 bytes)  
		MIME: application/vnd.in-toto+json
