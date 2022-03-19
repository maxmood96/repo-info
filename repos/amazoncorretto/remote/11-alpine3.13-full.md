## `amazoncorretto:11-alpine3.13-full`

```console
$ docker pull amazoncorretto@sha256:b70aee876f0f00778ea0598e039eba693c235f908809fd0541ff3beede2a07c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:11-alpine3.13-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:30b9e54cfa9e9c9094794c54bc6df614d19ad4c8bed5165d68b2d4130045bfaf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196278792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d166d8df0c7fa89aa2299e059b5d74542feddafece167e03fa06af60b791430`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:36 GMT
ADD file:51c08645923aa2d3513f66571f0c598a727dd5805e4f2bb87fb660b2f789348d in / 
# Thu, 17 Mar 2022 15:19:36 GMT
CMD ["/bin/sh"]
# Sat, 19 Mar 2022 00:36:21 GMT
ARG version=11.0.14.9.1
# Sat, 19 Mar 2022 00:36:31 GMT
# ARGS: version=11.0.14.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Sat, 19 Mar 2022 00:36:32 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 00:36:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Sat, 19 Mar 2022 00:36:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:e1096b72685a2366348e697f5b57e3b8feb41660e3dbe68447e168381515111a`  
		Last Modified: Thu, 17 Mar 2022 15:20:24 GMT  
		Size: 2.8 MB (2817181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1513993c1afc6ab505c3d2524d66e815005749c4e869aeebde7be6332d3d62d`  
		Last Modified: Sat, 19 Mar 2022 00:44:19 GMT  
		Size: 193.5 MB (193461611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
