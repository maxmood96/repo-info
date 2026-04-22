## `sapmachine:26-jre-alpine-3.22`

```console
$ docker pull sapmachine@sha256:9c8d1756cd9f6e20990ac5651dca37a230f4635e48ded59d4919a74a16e379ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:26-jre-alpine-3.22` - linux; amd64

```console
$ docker pull sapmachine@sha256:e9a9c4ed57c987172a1011c41b6aae45739320eb00b268f6e114e9b9c37ec74c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63145570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9c10cc47e447818947e2a306137de6702943fd8c008675ad69b82e3efee46d5`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 23:02:37 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-26-jre=26.0.1-r0 # buildkit
# Tue, 21 Apr 2026 23:02:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-sapmachine-jre
# Tue, 21 Apr 2026 23:02:37 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecab01ffc630c2a3c193786ad9e76c6509561f5b3d99abc6559a49bcaf21f7f9`  
		Last Modified: Tue, 21 Apr 2026 23:02:49 GMT  
		Size: 59.3 MB (59337381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jre-alpine-3.22` - unknown; unknown

```console
$ docker pull sapmachine@sha256:868e18fb166c1690dcd362e05e93781a91992b476c7a0b4641dafcf74edbfab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **437.5 KB (437498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58c666933379bec054d0a5cbb3e16988d619f68d9520716ec956230ad0968f93`

```dockerfile
```

-	Layers:
	-	`sha256:bab69c7f34917d471a68700028568650b973a835a80db7f69d6c95cd9d8692cb`  
		Last Modified: Tue, 21 Apr 2026 23:02:47 GMT  
		Size: 430.2 KB (430217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b060345984585b6cfb7b2244844ab9c136eb8daaedee3f717bd1e8451e10a8a9`  
		Last Modified: Tue, 21 Apr 2026 23:02:47 GMT  
		Size: 7.3 KB (7281 bytes)  
		MIME: application/vnd.in-toto+json
