## `amazoncorretto:16-alpine-full`

```console
$ docker pull amazoncorretto@sha256:e5fbbc6038924611e3b05053546cf610fca46f1617b68888375eb7f03b08a9a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:16-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:937f9a8efb25fa28565a290aa49e1ee80f8a18550d26c9d1cc074c6bcfbd3868
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212399710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60afaebd1c1a68299d3d2208c6f554743225f186b8e5f326c265e2d779472e9e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Thu, 18 Mar 2021 01:21:42 GMT
ARG version=16.0.0.36.1
# Thu, 18 Mar 2021 01:21:53 GMT
# ARGS: version=16.0.0.36.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-16=$version-r0
# Thu, 18 Mar 2021 01:21:54 GMT
ENV LANG=C.UTF-8
# Thu, 18 Mar 2021 01:21:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 18 Mar 2021 01:21:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e29f7097b7fda6176cd5fdfa81433c23772dec0d1834795ea55e0725629548`  
		Last Modified: Thu, 18 Mar 2021 01:27:06 GMT  
		Size: 209.6 MB (209600217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
