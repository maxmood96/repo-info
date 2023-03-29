## `amazoncorretto:11-alpine3.15`

```console
$ docker pull amazoncorretto@sha256:8e9af7bd14565cae707e0369a140dbacd5d9225443d3819841178b3e1a08e996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:11-alpine3.15` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6473b345b65c47d7ec4d13f67e114291bff6fe92e85292ef2da96351feb8ec30
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.0 MB (197959953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f8e7dbfe2b9121785890c1db8cb2d59b0ffe88bbee60539cf25063402d3e925`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:33 GMT
ADD file:08ad6c1c886a26e30ae4ab103ff377ee6cfbc1be2437fa227ec28a335c63d78a in / 
# Wed, 29 Mar 2023 18:19:33 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:18:07 GMT
ARG version=11.0.18.10.1
# Wed, 29 Mar 2023 19:18:12 GMT
# ARGS: version=11.0.18.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Wed, 29 Mar 2023 19:18:13 GMT
ENV LANG=C.UTF-8
# Wed, 29 Mar 2023 19:18:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 29 Mar 2023 19:18:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:0ce1dd7918a48990ab749aab2e805c26f691a3a8103495530e7ea5a1d168af4a`  
		Last Modified: Wed, 29 Mar 2023 18:20:17 GMT  
		Size: 2.8 MB (2826596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa1c7dee7c930d9d2d94dd2e8fc55989a415a72df582c1a467aaa82ce21c313`  
		Last Modified: Wed, 29 Mar 2023 19:24:32 GMT  
		Size: 195.1 MB (195133357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
