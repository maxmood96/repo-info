## `sapmachine:lts-alpine`

```console
$ docker pull sapmachine@sha256:746ce680ffb92643e85a13a44b60d1eef5675e05d297ef688bc3c1c6b94f08e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:lts-alpine` - linux; amd64

```console
$ docker pull sapmachine@sha256:f9d10015b158cb3d0ba338a869f34acaa4a10bb5b178f2584f62d226f4e445d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.3 MB (227263898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d29d748c876c0d5b18378d6693fa6bb1df598222b39c241428698e61fd6ded`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 23:03:39 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-25-jdk=25.0.3-r0 # buildkit
# Tue, 21 Apr 2026 23:03:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-sapmachine-jdk
# Tue, 21 Apr 2026 23:03:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e355e75fef8192ec794c6b0fd6422a60e5241d26ca29ab2b83226b1dd6ccb389`  
		Last Modified: Tue, 21 Apr 2026 23:04:00 GMT  
		Size: 223.4 MB (223399709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-alpine` - unknown; unknown

```console
$ docker pull sapmachine@sha256:aa50855e8b5e609c378a95ca74a2766084cdc637b02eb55eff930e149b94dc35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.7 KB (514675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5f366ce84ed72da0d20b8ea02e123045625f7f316d0890f6948c5f6b60d5b68`

```dockerfile
```

-	Layers:
	-	`sha256:1eb228f230d7b6387ee10852bbc2cb6f7fcfa654d1fa3772b03aad21a59a7d10`  
		Last Modified: Tue, 21 Apr 2026 23:03:55 GMT  
		Size: 504.5 KB (504489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9772d2d771a6112294175713dab96e8aace484a9fa89f848bc8a69972aa3bbb0`  
		Last Modified: Tue, 21 Apr 2026 23:03:55 GMT  
		Size: 10.2 KB (10186 bytes)  
		MIME: application/vnd.in-toto+json
