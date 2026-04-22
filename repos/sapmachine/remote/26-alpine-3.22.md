## `sapmachine:26-alpine-3.22`

```console
$ docker pull sapmachine@sha256:56aa9cdc025bbc16d570ae1c3900aa3e3ef3965aeae3b4326e9253323a0648a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:26-alpine-3.22` - linux; amd64

```console
$ docker pull sapmachine@sha256:975eacbe944a37842c89b774c2cf35d91f1858d74ce24c89233d1708f23807e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231601573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9514c3a5d8ef12f8b1c6cbab58ed06dc3ad801720fc9a67f2689ede2140f1918`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 23:02:39 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-26-jdk=26.0.1-r0 # buildkit
# Tue, 21 Apr 2026 23:02:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-sapmachine-jdk
# Tue, 21 Apr 2026 23:02:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a101bccbf688e60364ed7e3e84a9b2a93056f9807d57e337d62b5617de0b2934`  
		Last Modified: Tue, 21 Apr 2026 23:03:06 GMT  
		Size: 227.8 MB (227793384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-alpine-3.22` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9351db1933d51335a8d61295e5fe765e78f81dcc64a1b7c3fc1b0d84bb0453a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **507.6 KB (507585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:446b48449b89e1f8bf64cd5bc8587bd796f294672e7dd9e828d02862cfa2f7b9`

```dockerfile
```

-	Layers:
	-	`sha256:c09dc05b10a4fccb5c99e1458ad4b54002b7234f5e1edadc406e2b4bfa425d4c`  
		Last Modified: Tue, 21 Apr 2026 23:02:55 GMT  
		Size: 499.3 KB (499331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9ed49fe392e27f961577d3a052a39f42221db08d736cdd8e3bdeff89b761c46`  
		Last Modified: Tue, 21 Apr 2026 23:02:55 GMT  
		Size: 8.3 KB (8254 bytes)  
		MIME: application/vnd.in-toto+json
