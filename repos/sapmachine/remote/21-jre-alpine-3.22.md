## `sapmachine:21-jre-alpine-3.22`

```console
$ docker pull sapmachine@sha256:df4e440cf443351566f934c5afdd61d52b3869db22198f55c97dba6bec2356f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:21-jre-alpine-3.22` - linux; amd64

```console
$ docker pull sapmachine@sha256:7e4a38a5ceb5d66fdbe45fa7561afdc9fee6bafe10210ef41e7b4f817f007775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 MB (64066153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daccfa23ad77d51c0334da4f96069512faff3e88d91c4a7ec5b28a8e4e1ed2fd`
-	Default Command: `["sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 11 Aug 2025 06:09:32 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add nss sapmachine-21-jre=21.0.8-r0 # buildkit
# Mon, 11 Aug 2025 06:09:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-sapmachine-jre
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc2e4a5a3a72ae3c6b8f8f07318ad6ebf96b70be0731a32f87caeab79a95646`  
		Last Modified: Wed, 17 Sep 2025 22:58:25 GMT  
		Size: 60.3 MB (60266464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-alpine-3.22` - unknown; unknown

```console
$ docker pull sapmachine@sha256:78e75d77fa5e699da70aa98e68636653e5ffaf801c4ad56a635fa2b20b6eeaab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.1 KB (431112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc83235ea8f117720dc28d6576add50c3f0c8bcc694fb804b24a5a458f310d1a`

```dockerfile
```

-	Layers:
	-	`sha256:56955e04060379f1fce457da966ed8bea856e34085802e2aeeda992035e9f114`  
		Last Modified: Wed, 17 Sep 2025 21:08:15 GMT  
		Size: 423.5 KB (423456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f197ce5d6c2878fc6247b8d45ef272aefe2c9d0368bd8e6cca59a2db8dbabca0`  
		Last Modified: Wed, 17 Sep 2025 21:08:16 GMT  
		Size: 7.7 KB (7656 bytes)  
		MIME: application/vnd.in-toto+json
