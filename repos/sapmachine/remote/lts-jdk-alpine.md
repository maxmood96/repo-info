## `sapmachine:lts-jdk-alpine`

```console
$ docker pull sapmachine@sha256:bba1e4783fe1c9aed5dc60277792b31ed157c0724c2843294bfd155bd1200ad9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:lts-jdk-alpine` - linux; amd64

```console
$ docker pull sapmachine@sha256:af95cce9c549570ba48529c851f008b6e53c1996a77d89cfca004d074394ab77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.6 MB (238633624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31badfc150e9fb2eb991b242812119fe5009b1ca44a44d7c69e656f740fd12c5`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-25-jdk=25-r0 # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-sapmachine-jdk
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d6d2b3df84d5cc439fae25c5964c3335243f1f919f1c3c73db79218ace21af`  
		Last Modified: Wed, 17 Sep 2025 21:29:22 GMT  
		Size: 234.8 MB (234833935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-alpine` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d206681d8d1d4951c11be92e826f14d80fd7dc1d7a9ec1679a2e31cb29ea9120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.4 KB (511423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38611911eda7caf909aebb9ebeeb1b1540ac93d53e815e3070c6f7de7b9dead2`

```dockerfile
```

-	Layers:
	-	`sha256:6be700dce4876eadb8b8713416601cb0cd75997af59dc3d46cc6c793d0f10fcd`  
		Last Modified: Wed, 17 Sep 2025 21:10:17 GMT  
		Size: 501.3 KB (501258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc656c9cf88e3357f95c4c95c0ae00b8a33f30bdd6302657aa4587d6516fc593`  
		Last Modified: Wed, 17 Sep 2025 21:10:18 GMT  
		Size: 10.2 KB (10165 bytes)  
		MIME: application/vnd.in-toto+json
