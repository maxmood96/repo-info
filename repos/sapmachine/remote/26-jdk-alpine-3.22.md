## `sapmachine:26-jdk-alpine-3.22`

```console
$ docker pull sapmachine@sha256:53e77af904ee17d330d924b3dcf80ed353b7aef91386f1cbfee1cb8edcaa9246
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:26-jdk-alpine-3.22` - linux; amd64

```console
$ docker pull sapmachine@sha256:d4c8990e19e42723e615aa340734e72458f3eeb0dc236fd34524be22fe3ba32a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231576607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd5b633a37b3d77bfb93dab31ed3c29e02f182c378ccc8bfbbdb59ac0cb3076`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 18 Mar 2026 17:50:11 GMT
RUN wget -qO /etc/apk/keys/sapmachine-apk.rsa.pub https://dist.sapmachine.io/alpine/sapmachine-apk.rsa.pub &&     echo "4444e47cabf35695f9406692848de191d3b7cbd47dcdc1ffb62f4f70aea06e89 /etc/apk/keys/sapmachine-apk.rsa.pub" | sha256sum -c - &&     echo "https://dist.sapmachine.io/alpine" >> /etc/apk/repositories &&     apk add sapmachine-26-jdk=26-r0 # buildkit
# Wed, 18 Mar 2026 17:50:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-sapmachine-jdk
# Wed, 18 Mar 2026 17:50:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a312ef97d44ec283f2cbe3687fb5f53f99cf56aad339fbfe642fdde637a9f5`  
		Last Modified: Wed, 18 Mar 2026 17:50:34 GMT  
		Size: 227.8 MB (227771732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jdk-alpine-3.22` - unknown; unknown

```console
$ docker pull sapmachine@sha256:50c99d723970c4b810951ba6c0d402ad583274771f47466e545e174211184fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **506.2 KB (506225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c3a889157bfd5269f46bceb875daf352e3a79e538b96da1c972dfa55f116aa5`

```dockerfile
```

-	Layers:
	-	`sha256:c289efe2de3f60c6f8427f7333f15f42fee6e9ae9691b48ea0877ccc239cfd84`  
		Last Modified: Wed, 18 Mar 2026 17:50:29 GMT  
		Size: 498.6 KB (498647 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca982402ab0fbe3ff34ac155528ef4f4c2d5eb1e8a2419970424adac8e7d3c01`  
		Last Modified: Wed, 18 Mar 2026 17:50:29 GMT  
		Size: 7.6 KB (7578 bytes)  
		MIME: application/vnd.in-toto+json
