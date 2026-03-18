## `sapmachine:21-jre-alpine-3.23`

```console
$ docker pull sapmachine@sha256:6d8fa6e57885580c95a2ebf7be5aaee9472b0a6c9f8402010bd170c2a0598fbd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:21-jre-alpine-3.23` - linux; amd64

```console
$ docker pull sapmachine@sha256:d190844737dc110b23afec1ba5de0bf169708dc8a9d80106ca86c607d85fb157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65116690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095fa06b2601e4d5b323bd5334978116aec7e3c0e8cccafa58f9abca35dcaea8`
-	Default Command: `["sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 18 Mar 2026 17:50:44 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-21-jre=21.0.10.0.1-r0 # buildkit
# Wed, 18 Mar 2026 17:50:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-sapmachine-jre
# Wed, 18 Mar 2026 17:50:44 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f355d59f165064e22f94eb3fa309466388e1ee0040d19ef29dbb1aa817dffe49`  
		Last Modified: Wed, 18 Mar 2026 17:50:57 GMT  
		Size: 61.3 MB (61254869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-alpine-3.23` - unknown; unknown

```console
$ docker pull sapmachine@sha256:36e306522b35f3e51f9294d044550d3cb5548d6d32b7396e49b91ba6f36c984b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **435.6 KB (435571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a40b0d0a74b1340d147382489837447b28225fe2c946ad743e1d4211657b378`

```dockerfile
```

-	Layers:
	-	`sha256:60356a596c5b84a18896ddcb9d7c4a85c12b13011c6c32724308a9e6084ea733`  
		Last Modified: Wed, 18 Mar 2026 17:50:55 GMT  
		Size: 427.9 KB (427933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87bee538ae544ef7c5f6697bf77648f146af8c19141957d75c75ffc15d772c5b`  
		Last Modified: Wed, 18 Mar 2026 17:50:56 GMT  
		Size: 7.6 KB (7638 bytes)  
		MIME: application/vnd.in-toto+json
