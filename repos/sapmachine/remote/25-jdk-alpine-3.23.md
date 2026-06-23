## `sapmachine:25-jdk-alpine-3.23`

```console
$ docker pull sapmachine@sha256:d362039030250d424390480d3426e5a5fe21409500024b333f31dc61c48c11ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:25-jdk-alpine-3.23` - linux; amd64

```console
$ docker pull sapmachine@sha256:dcb2e19aa9ea4e01e56e37f3253c3c23aafaf29c82789a290b7deea7fe4744d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 MB (227243317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8cf42db9087230f7bbc8851459cd36f31f08523b16272e0775ecbca9cef048`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 20:08:11 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-25-jdk=25.0.3-r0 # buildkit
# Mon, 22 Jun 2026 20:08:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-sapmachine-jdk
# Mon, 22 Jun 2026 20:08:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93aca39cef94b267af071a99efa8042b167b0ee4c3a92ddce8b5bbd3914e1657`  
		Last Modified: Mon, 22 Jun 2026 20:08:33 GMT  
		Size: 223.4 MB (223398896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-alpine-3.23` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9238d906f395a347c4325c23d53aafe6beaa437205c96633b573ccb1b2f7001f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.7 KB (514675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613c2d888793e4c8483ff46a50367999c3f6a51aeb48940311b71ec226324f7f`

```dockerfile
```

-	Layers:
	-	`sha256:14006a27bcb666e9d835b24a805b3e3cc38702ce2316ac1304e3214608956767`  
		Last Modified: Mon, 22 Jun 2026 20:08:28 GMT  
		Size: 504.5 KB (504489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3536022a3cbae53dad1c6a1d58e13be908a2f2862b6e67f65b5eb720258b647`  
		Last Modified: Mon, 22 Jun 2026 20:08:27 GMT  
		Size: 10.2 KB (10186 bytes)  
		MIME: application/vnd.in-toto+json
