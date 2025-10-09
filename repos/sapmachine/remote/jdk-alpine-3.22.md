## `sapmachine:jdk-alpine-3.22`

```console
$ docker pull sapmachine@sha256:c2623bff4b4bbdfecbbb719b0cfb01facd8018f0f9ab05a127ecb737017e6f6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:jdk-alpine-3.22` - linux; amd64

```console
$ docker pull sapmachine@sha256:fce55f33a1ee9a2288f353caa15dfadca766f37afb6fb446056b953e643be784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.6 MB (238639226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1e42379678008c43765c4c64c145f406f98e0770e266401fb2c49c512f197e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Sep 2025 04:28:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-25-jdk=25-r0 # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-sapmachine-jdk
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a83bd9ffa297e827d6d4e07f07d1f69b21e07972f2c3c2606c14484594d5d4e`  
		Last Modified: Wed, 08 Oct 2025 23:20:11 GMT  
		Size: 234.8 MB (234836774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-alpine-3.22` - unknown; unknown

```console
$ docker pull sapmachine@sha256:be7eef82d311ce00be5f56a7dc9d99ebe21a7035b7224420b2a517cf927a2e7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.4 KB (511423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc73515ab20786e9b620b77e9d4277b682bd8980d80e4fd154768181adfd87c`

```dockerfile
```

-	Layers:
	-	`sha256:36ac0ffe30b985dfaec22c383ed7a1249bf9b977b559f781a1c989b7bb06928c`  
		Last Modified: Thu, 09 Oct 2025 00:07:01 GMT  
		Size: 501.3 KB (501258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c4c40e2a9b43408d64e3c92acff2a054fffa70122759867602a9182efad3059`  
		Last Modified: Thu, 09 Oct 2025 00:07:02 GMT  
		Size: 10.2 KB (10165 bytes)  
		MIME: application/vnd.in-toto+json
