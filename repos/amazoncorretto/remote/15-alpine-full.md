## `amazoncorretto:15-alpine-full`

```console
$ docker pull amazoncorretto@sha256:3140f360da4428dac33ac5865058d0e01e2d7c264360a93230af00b1ee569cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:15-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0f607d685f081e683a636316fe98eb831793bd30746eff3b205b417900a9e71a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207694266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96bd30231761eb2b90745fb63c5a236ca528a47e3c19366507d956af53128036`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:52:17 GMT
ARG version=15.0.0.36.1
# Thu, 22 Oct 2020 02:52:28 GMT
# ARGS: version=15.0.0.36.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-15=$version-r0
# Thu, 22 Oct 2020 02:52:28 GMT
ENV LANG=C.UTF-8
# Thu, 22 Oct 2020 02:52:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 22 Oct 2020 02:52:29 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c8330e301cf6a1d497fbd4ce0b7d7cf73b965b23af29fd36c5f07c66b060bb`  
		Last Modified: Thu, 22 Oct 2020 02:54:29 GMT  
		Size: 204.9 MB (204897406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
