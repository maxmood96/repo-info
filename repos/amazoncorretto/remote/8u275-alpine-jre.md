## `amazoncorretto:8u275-alpine-jre`

```console
$ docker pull amazoncorretto@sha256:bf589d2877958cfa423955a9eee3162393acbbaec3a6b15436e8de68b95fbbab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8u275-alpine-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a0357ef50d477c994599c445c4befe270cf43ace5ecf1ce625527708db03db5a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43108328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79958c1f52ea286802cee08e086ceece191f7920e41bea21a5cfff4052ad5054`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:47:22 GMT
ARG version=8.275.01.2
# Fri, 11 Dec 2020 02:47:36 GMT
# ARGS: version=8.275.01.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0
# Fri, 11 Dec 2020 02:47:36 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 02:47:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3cb1bface849848879d3bdf8d3e42ae91fcb1cd361a6484e15b767c72cc69a6`  
		Last Modified: Fri, 11 Dec 2020 02:49:20 GMT  
		Size: 40.3 MB (40311383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
