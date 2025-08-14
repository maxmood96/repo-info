## `sapmachine:lts-alpine-3.21`

```console
$ docker pull sapmachine@sha256:d9b30de5be290a00f9cd51853fa501a76070c5c83dbae78d8622b582286890a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:lts-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:23201bdd2fff65a7650133fe4d8ff5c1eff7264b45f6e45d25d35f7ea090490f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.8 MB (219797223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9a41ae633053bad2079c9948d9f7c88a8df0417b7f887c84670323441c0c77`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-21-jdk=21.0.8-r0 # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-sapmachine-jdk
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f2ec7f052284f2a583989ada1cf63f7f7f11f99cd5a9daf8be0b693003ba66a`  
		Last Modified: Wed, 16 Jul 2025 21:41:52 GMT  
		Size: 216.2 MB (216159653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2912d1bef54b394e578f4d7bd1335e89cf0be51a73f653c9e69c38a53caf0eeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **520.5 KB (520548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd5bf8e6b23e6794354f39285064fee102c7df70fa883b1ff73b334b11375823`

```dockerfile
```

-	Layers:
	-	`sha256:324e4c4ed763350a99c9174b72c8198fccdf2556cc4d1c61e7eaa451e9a1f0ff`  
		Last Modified: Wed, 16 Jul 2025 00:07:37 GMT  
		Size: 512.2 KB (512235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bd4d98795e8ea786e62171848fb354cce1ca1198a808f4ccd85e87853054669`  
		Last Modified: Wed, 16 Jul 2025 00:07:37 GMT  
		Size: 8.3 KB (8313 bytes)  
		MIME: application/vnd.in-toto+json
