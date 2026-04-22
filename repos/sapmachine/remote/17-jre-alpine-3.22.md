## `sapmachine:17-jre-alpine-3.22`

```console
$ docker pull sapmachine@sha256:3ff177902764e9de3f0a0ed07ad6392eccf6dc98888dc4e08c07240302aec193
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:17-jre-alpine-3.22` - linux; amd64

```console
$ docker pull sapmachine@sha256:ee9fe5435e054b5014032723f634a640d44e1527f0431d5e3e8670ad2762ffb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58899212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca5421619290c82c0105141ab6f39e667180cade90c8d6416d9b70e8b15684ff`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 23:05:55 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-17-jre=17.0.19-r0 # buildkit
# Tue, 21 Apr 2026 23:05:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-sapmachine-jre
# Tue, 21 Apr 2026 23:05:55 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20280454d1505e53b557afed262ab3f956114159e05622bd6d93bf6b7e9376c`  
		Last Modified: Tue, 21 Apr 2026 23:06:06 GMT  
		Size: 55.1 MB (55091023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-alpine-3.22` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bbcf6a11deb27f5a0e98413ffe1d89587f8af2db75112fb90f80a8c46677bd35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.9 KB (432949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f17d6f69f837bf399b51056b93e0bcf676ff48447f0e5ef13469ead3abf82d71`

```dockerfile
```

-	Layers:
	-	`sha256:29dc9531c3c3a4e04cc75911da0802c59dc982deae6fb749706030b4d9361644`  
		Last Modified: Tue, 21 Apr 2026 23:06:04 GMT  
		Size: 426.0 KB (425989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bee0f6d7dba44e30880268aeb0d96a7b357246f56fa43049ad677e848e79b36`  
		Last Modified: Tue, 21 Apr 2026 23:06:05 GMT  
		Size: 7.0 KB (6960 bytes)  
		MIME: application/vnd.in-toto+json
