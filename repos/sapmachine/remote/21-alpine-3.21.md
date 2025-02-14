## `sapmachine:21-alpine-3.21`

```console
$ docker pull sapmachine@sha256:3f88afae2ddcf1cb5aaff3f8e9e686c1a37b58896ae9e0e3375b3b55eafea53e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:21-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:1c89deea77719358a7a2451f139a22a0e71c061b345a25ca317023b7b47efc3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.4 MB (219352923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:995ba73af7c686b544258339b7f9cf33d77ff6f9752287fa5232d40d634fd10e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:13 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["/bin/sh"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-21-jdk=21.0.6-r0 # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-sapmachine-jdk
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92be78232d89252cd0b608424aaeaf304179ded5f5ff1add6f5dd7ab599e5c98`  
		Last Modified: Fri, 14 Feb 2025 19:14:24 GMT  
		Size: 215.7 MB (215710676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9a6dc80b27800a6859cad6c0627815c41b6040a0f3687b171a376b09d33060d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.2 KB (520187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:876b9ab821280f85b8cfb12ef463333d40cfa862c4041f7aa1db755ec08b3f31`

```dockerfile
```

-	Layers:
	-	`sha256:ca2286980c0c1cc97a48428de9ab9b55543436236e171ce0e31300dfaaac5144`  
		Last Modified: Fri, 14 Feb 2025 22:05:51 GMT  
		Size: 510.9 KB (510904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f59ee7fa684ecf04c65531d668f3888fdcdd0f065bb9fc075dfda4e4ccf81e3`  
		Last Modified: Fri, 14 Feb 2025 22:05:51 GMT  
		Size: 9.3 KB (9283 bytes)  
		MIME: application/vnd.in-toto+json
