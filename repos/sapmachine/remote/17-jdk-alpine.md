## `sapmachine:17-jdk-alpine`

```console
$ docker pull sapmachine@sha256:c5811f66a14339f58ab98994f2200f9380eb5fd570756cf1ec1bee43b1cc13eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:17-jdk-alpine` - linux; amd64

```console
$ docker pull sapmachine@sha256:d7472a58f89a238b17ea83a8ac0a29960a63673e82d7af90a8aca445d7dad748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204871551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b368ca504feeec3f8d482291b6f345868cdac1f7d32b12dcb32a74b3ce61201c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 11 Aug 2025 06:09:35 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add nss sapmachine-17-jdk=17.0.16-r0 # buildkit
# Mon, 11 Aug 2025 06:09:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-sapmachine-jdk
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004659796e126b0ad3786f911ceaef02c84682e9777a29f079573bc6965859e7`  
		Last Modified: Wed, 17 Sep 2025 17:41:31 GMT  
		Size: 201.1 MB (201071862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-alpine` - unknown; unknown

```console
$ docker pull sapmachine@sha256:dc0e111ef64419339f3a00b66f33c903ff410ba4d3ba05bf3f14637fd96932b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.5 KB (516509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d8befafbc9029d985b55adc673690b89c3622804f31e45c8c1acb8addf76a0c`

```dockerfile
```

-	Layers:
	-	`sha256:b78bd34a1d2dad841dff1ac1caf8d310b63a4d29ee8affe5f608e9ee51506079`  
		Last Modified: Wed, 17 Sep 2025 21:05:19 GMT  
		Size: 507.6 KB (507551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5019bf4989008e91077c2bb090380c224ea2905159ffdaa6113477ce29f824a`  
		Last Modified: Wed, 17 Sep 2025 21:05:20 GMT  
		Size: 9.0 KB (8958 bytes)  
		MIME: application/vnd.in-toto+json
