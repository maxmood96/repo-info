## `sapmachine:jre-alpine-3.21`

```console
$ docker pull sapmachine@sha256:0d4f7c4b606799260755dd3b0ba57155ae84a5062a178069c332b3df835bb67e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:jre-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:13d11a2d0f35fda77cb4d7feddb69324cdc7476b7f087a3934773173be94875a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63697980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56182abea9544661d37cc49bfc151b040037e7532a312ac347c3a0dc5cda7b7f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Mon, 27 Jan 2025 13:39:22 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-23-jre=23.0.2-r0 # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-sapmachine-jre
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63d3d4e5f06fd81c0c552fd277c2a84b42860d6c5814209acd0cb4907d8e57c`  
		Last Modified: Wed, 12 Feb 2025 13:12:30 GMT  
		Size: 60.1 MB (60056265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4e35e51bf86081968e0442781e4e7c239bd0231694eaa37e73902386502951ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.3 KB (432275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4feb59c97a60d15baf05c2087f2fe817d697a9a49371e9f65ff64bf3cf016d7`

```dockerfile
```

-	Layers:
	-	`sha256:af5cdc46362b39656418043ffa78761ce5f13426e01fd0d428fa94ebdc90f7e6`  
		Last Modified: Tue, 28 Jan 2025 08:51:04 GMT  
		Size: 424.0 KB (423985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b74a2ea17b21df9ba37109ef72fbd3e289adfabc9f98dad4d816e3b57d582f4c`  
		Last Modified: Tue, 28 Jan 2025 08:51:04 GMT  
		Size: 8.3 KB (8290 bytes)  
		MIME: application/vnd.in-toto+json
