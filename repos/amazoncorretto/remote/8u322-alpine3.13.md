## `amazoncorretto:8u322-alpine3.13`

```console
$ docker pull amazoncorretto@sha256:9dfae3123b00f5209cfe1e46652414f94bd4037150b892d6b9547caece34e3fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8u322-alpine3.13` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e671315a88a09f5f15a7aed02e8b2b6bf40d6253cec3242d1f468279782ccf48
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101927388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:892ce49a9110367c4391f8882d91a1d57b732ea594e4cf487124932bbb4180b0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:36 GMT
ADD file:51c08645923aa2d3513f66571f0c598a727dd5805e4f2bb87fb660b2f789348d in / 
# Thu, 17 Mar 2022 15:19:36 GMT
CMD ["/bin/sh"]
# Sat, 19 Mar 2022 00:34:40 GMT
ARG version=8.322.06.2
# Sat, 19 Mar 2022 00:34:46 GMT
# ARGS: version=8.322.06.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Sat, 19 Mar 2022 00:34:47 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 00:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Sat, 19 Mar 2022 00:34:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:e1096b72685a2366348e697f5b57e3b8feb41660e3dbe68447e168381515111a`  
		Last Modified: Thu, 17 Mar 2022 15:20:24 GMT  
		Size: 2.8 MB (2817181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5297b3636d4e45d5eba70230e9a9e9e6cf7053d643ed17b502ca0fe6a5d547e2`  
		Last Modified: Sat, 19 Mar 2022 00:41:30 GMT  
		Size: 99.1 MB (99110207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
