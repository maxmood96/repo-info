## `amazoncorretto:11-alpine-full`

```console
$ docker pull amazoncorretto@sha256:8e9bb1bc18954fc2634632ebf4f2322f4a34202466cfdd2573110d281bea66f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:11-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ce812cc8bc2345fd2fb1b046150bf75837a6ee9042530b672224fa4276089ea2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.0 MB (195003745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a3a89243ece990a938647c53ed624ec6a8555155c5bc0d23c5319dd9be55dc2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:52:00 GMT
ARG version=11.0.9.11.1
# Thu, 22 Oct 2020 02:52:10 GMT
# ARGS: version=11.0.9.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Thu, 22 Oct 2020 02:52:11 GMT
ENV LANG=C.UTF-8
# Thu, 22 Oct 2020 02:52:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 22 Oct 2020 02:52:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4650ec59cfb84326c52d7ff96d2a71e1ac9ee09cb8419aad8530c44076138251`  
		Last Modified: Thu, 22 Oct 2020 02:53:57 GMT  
		Size: 192.2 MB (192206885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
