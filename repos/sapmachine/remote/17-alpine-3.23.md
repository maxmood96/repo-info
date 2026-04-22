## `sapmachine:17-alpine-3.23`

```console
$ docker pull sapmachine@sha256:bc7406d34dfe82a22660c3f1d6ce1f6fe2229de83eac5169dd753aa25925d5ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:17-alpine-3.23` - linux; amd64

```console
$ docker pull sapmachine@sha256:17b32f199f3c81360a5bbc6d65406eb5dad72d54b76905afa6b6932c463b2c22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.9 MB (206873787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e4866f4e0cf29ff4f84eaf2f950129a1b04bf0156d7e16986ae2cee830535e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 21 Apr 2026 23:05:35 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-17-jdk=17.0.19-r0 # buildkit
# Tue, 21 Apr 2026 23:05:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-sapmachine-jdk
# Tue, 21 Apr 2026 23:05:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2754c7b2e2d74d6fa4bbdd7d66b93ec1524702887190747d91519ad3b3f0e6a9`  
		Last Modified: Tue, 21 Apr 2026 23:05:55 GMT  
		Size: 203.0 MB (203009598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-alpine-3.23` - unknown; unknown

```console
$ docker pull sapmachine@sha256:de5641b9a93d2b73f787d56f440931cc9eabf37cf26b6548671ed8dd0b6ce75f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.6 KB (521566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01e16e6cf180d1797ef7994405361f97c0541df590693bdcd437300ceda858e5`

```dockerfile
```

-	Layers:
	-	`sha256:59a2a39692bdf60928d5fa2ae0121f0f2f1d91d568773c973b5f84c63dd66f1c`  
		Last Modified: Tue, 21 Apr 2026 23:05:51 GMT  
		Size: 512.7 KB (512659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:485d8062bbf40666ffe0002049e2a55b4d266604b9620a15456c467df354d86e`  
		Last Modified: Tue, 21 Apr 2026 23:05:51 GMT  
		Size: 8.9 KB (8907 bytes)  
		MIME: application/vnd.in-toto+json
