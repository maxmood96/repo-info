## `sapmachine:26-jre-alpine-3.23`

```console
$ docker pull sapmachine@sha256:4ef28b36163ec0f98c8c2fb40730f7ae83416f8cfc01bd2abcd764c538f36e08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:26-jre-alpine-3.23` - linux; amd64

```console
$ docker pull sapmachine@sha256:eaeccbfdd719ea83c691126996129013c3149f7558dc34608f820bc546559430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.6 MB (63605762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:641424358fde052f739ed8a520f9615165b2ddce337b85c43aac8eddfd2db49b`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 18 Mar 2026 17:49:53 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-26-jre=26-r0 # buildkit
# Wed, 18 Mar 2026 17:49:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-sapmachine-jre
# Wed, 18 Mar 2026 17:49:53 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1627ebb2d2d862d0e022b98ff8ea55bcf6a1a9f62c19a43c0e5e18fc286e0d5`  
		Last Modified: Wed, 18 Mar 2026 17:50:05 GMT  
		Size: 59.7 MB (59743941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jre-alpine-3.23` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1e56007c6c0e16f981c8707bba2e74224d59eae306dd42017520a770172ef309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.7 KB (438695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6319f9aba45a56a0fc66abff47ad01649a28007ed3016fd4293259dcec701a74`

```dockerfile
```

-	Layers:
	-	`sha256:da55e0a474671bcffe53dba601547a32bd5a4fd3838fffd507ee4cdfd47bbed8`  
		Last Modified: Wed, 18 Mar 2026 17:50:04 GMT  
		Size: 431.1 KB (431126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17d66088c0bd109a32c6307452ba5510a67971cfcb40c30823fe17e40634944a`  
		Last Modified: Wed, 18 Mar 2026 17:50:04 GMT  
		Size: 7.6 KB (7569 bytes)  
		MIME: application/vnd.in-toto+json
