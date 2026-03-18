## `sapmachine:26-jdk-alpine-3.21`

```console
$ docker pull sapmachine@sha256:24ea365f2fc808b35e5cec78f17bd4ea8213bf94ea3a6670edb1568ff44eeed0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:26-jdk-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:4d1ad9595396777200aac1ab729390344defa6be3d74c7f969b6dca95ac1f76a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231279322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:130c22df75d761c91f935a7eb69ef94c186f8a7c09d14b8d88de374af91b5898`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 18 Mar 2026 17:50:19 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-26-jdk=26-r0 # buildkit
# Wed, 18 Mar 2026 17:50:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-sapmachine-jdk
# Wed, 18 Mar 2026 17:50:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367cb9d63fd0d156da168a0c65970db1f7f2de0c4f93b3345a518b6072be80ba`  
		Last Modified: Wed, 18 Mar 2026 17:50:47 GMT  
		Size: 227.6 MB (227635580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jdk-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:27c6851be81f421edf6238a4512c8021aa730bbf8c24a71edf5bbc952573bc59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **509.5 KB (509479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4931f66acf16778e9d83a6a272c952168a853af9db4f1c1723c1a170a99e250e`

```dockerfile
```

-	Layers:
	-	`sha256:fc6f26d118c35893e53082990f5abaf2fcadd72da9979956668bb82acb08ab63`  
		Last Modified: Wed, 18 Mar 2026 17:50:37 GMT  
		Size: 501.9 KB (501901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44a95d4d570e11b2261b70dc55368eca3bae5b5b965f019109c46ce77cf6918d`  
		Last Modified: Wed, 18 Mar 2026 17:50:37 GMT  
		Size: 7.6 KB (7578 bytes)  
		MIME: application/vnd.in-toto+json
