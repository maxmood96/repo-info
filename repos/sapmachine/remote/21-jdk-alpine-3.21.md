## `sapmachine:21-jdk-alpine-3.21`

```console
$ docker pull sapmachine@sha256:fe3665fc7390a8b913a3e4934293a79d94a2de21b708b419e1ad6f874cdf77af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:21-jdk-alpine-3.21` - linux; amd64

```console
$ docker pull sapmachine@sha256:000ab62896815dfa86201d952c4dad8f36cfb2ac593af7bcd8325cb096d3e709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.8 MB (219805086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16f4d3f99ae363b28ad597b0a12d4e647c7f51904595855d6f06c6b624296ed7`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:32 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["/bin/sh"]
# Mon, 11 Aug 2025 06:09:32 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add nss sapmachine-21-jdk=21.0.8-r0 # buildkit
# Mon, 11 Aug 2025 06:09:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-sapmachine-jdk
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15c7b9b0acab8e5fc8339b97bdc8ed749483b4e73e8a723f746f08676be26cd`  
		Last Modified: Thu, 09 Oct 2025 15:25:18 GMT  
		Size: 216.2 MB (216162517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-alpine-3.21` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4d0aa5a8de0acf2b717bff185b861d754bfdf88b45e58c6cac912a00edae329d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **519.2 KB (519248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a7679d86413c76453e1cb1e69785059e57a21e61b307edb4d096cd0d8e3945`

```dockerfile
```

-	Layers:
	-	`sha256:c9fa7f02982b6fd3164dbedb98d9d303798c62e560049747cefcfaf8f395d495`  
		Last Modified: Thu, 09 Oct 2025 00:05:51 GMT  
		Size: 511.6 KB (511579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f69598fef52f9c71abb5b514f118ca2a5c468f0c1ec34bb96181236e5ebef3af`  
		Last Modified: Thu, 09 Oct 2025 00:05:52 GMT  
		Size: 7.7 KB (7669 bytes)  
		MIME: application/vnd.in-toto+json
