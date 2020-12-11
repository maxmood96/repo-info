## `amazoncorretto:15-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:4223f26700e534b251f73de6b0a3c81e6a2201b38f899b560a31c409b06915f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:15-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7ecdbd7c06dbcdab16d69a4d86256ec395922ddf278144f0e077e647f9c22930
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207714884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3c65bf033ee406ac95fc6e2c709f8bb3e291a8b7f31765b6d4e3eba0f18e59b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:47:56 GMT
ARG version=15.0.1.9.1
# Fri, 11 Dec 2020 02:48:05 GMT
# ARGS: version=15.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-15=$version-r0
# Fri, 11 Dec 2020 02:48:08 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 02:48:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 11 Dec 2020 02:48:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d154da8290a272bc25dd6b7c712f4d4829c389afbdea6b9a5e449786db0b9c39`  
		Last Modified: Fri, 11 Dec 2020 02:50:21 GMT  
		Size: 204.9 MB (204917939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
