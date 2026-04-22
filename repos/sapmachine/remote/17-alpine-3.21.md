## `sapmachine:17-alpine-3.21`

```console
$ docker pull sapmachine@sha256:bd5a00f1be4cd17f86591f18cb7805c5acf3f999b7783136991327e3a7c1c25b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:17-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:36f1a8e87d440904efc2d041eb472df0e5ac2e73f0a4561cf595f443ee31d22c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.1 MB (206113918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffdc5554428dec53fa97bfdb242d590d5f2d4411f71a3f0a182775f179205b08`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 23:06:06 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-17-jdk=17.0.19-r0 # buildkit
# Tue, 21 Apr 2026 23:06:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-sapmachine-jdk
# Tue, 21 Apr 2026 23:06:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3bf7a1b9a127b1aa2435e247fd29ac2271c69c3ec80e2cee0d5c0bd2df40d25`  
		Last Modified: Tue, 21 Apr 2026 23:06:27 GMT  
		Size: 202.5 MB (202467043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fd8b3003c10dba465dfacbf2e47d91e70766e18db3fbdf17b27ef83055d808ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.8 KB (521766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b40947dde2b461eab953d7848fe8430af75340df8cda717838a94903106f541`

```dockerfile
```

-	Layers:
	-	`sha256:1c44531189859d6f262200e9f9fea9689b946260c035d5d9e50d7aa5a8a2a13c`  
		Last Modified: Tue, 21 Apr 2026 23:06:22 GMT  
		Size: 514.1 KB (514144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72d4fcc3a155c0b3565a7230f95dea0e67f667bb6d7d5b20625280763b61b770`  
		Last Modified: Tue, 21 Apr 2026 23:06:21 GMT  
		Size: 7.6 KB (7622 bytes)  
		MIME: application/vnd.in-toto+json
