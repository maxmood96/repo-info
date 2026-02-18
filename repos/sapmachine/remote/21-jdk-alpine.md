## `sapmachine:21-jdk-alpine`

```console
$ docker pull sapmachine@sha256:41bff0e6c3918b341cff62d0b2c64a5358bdc82192bc1024944c5b16bda9a4f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:21-jdk-alpine` - linux; amd64

```console
$ docker pull sapmachine@sha256:fd8eb059ae95c8e7f50363c1e5516e7a87c431994ef72e456bac22755b1e35e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.3 MB (221302145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280d1440bab86abdd70fc468ebd8b480cb607a37cba2b5abb4a77d7d4b3d3675`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 18 Feb 2026 19:23:21 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-21-jdk=21.0.10.0.1-r0 # buildkit
# Wed, 18 Feb 2026 19:23:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-sapmachine-jdk
# Wed, 18 Feb 2026 19:23:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777a3953a771a5ae1f2e61ed82eee09defa596768626895ee2dfb27cd6d4ce1d`  
		Last Modified: Wed, 18 Feb 2026 19:23:43 GMT  
		Size: 217.5 MB (217497270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-alpine` - unknown; unknown

```console
$ docker pull sapmachine@sha256:20437b519048c625df55445cb354419aac260fc4086cf5ffbe3ee71fdcbb1eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.3 KB (522252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ddacf7b8f4e2bc4ee37f2b0af2cf914928b7067c799e88628be661495ed1504`

```dockerfile
```

-	Layers:
	-	`sha256:8b3324539cf5459cbe300e84a6892b9980491e798b89b1b860a3cd528d6e3c94`  
		Last Modified: Wed, 18 Feb 2026 19:23:39 GMT  
		Size: 513.3 KB (513305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1cb96de1e7693ef4e2649377b294c53c033d0ebf8d58d8c73bcdadb09a61abe`  
		Last Modified: Wed, 18 Feb 2026 19:23:38 GMT  
		Size: 8.9 KB (8947 bytes)  
		MIME: application/vnd.in-toto+json
