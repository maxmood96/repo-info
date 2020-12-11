## `amazoncorretto:11-alpine`

```console
$ docker pull amazoncorretto@sha256:1a89f072bc00f51b3aa4401d315d74dd1bf8a98575ec9dd9e54171f892cf70ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:11-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f540bd83bc69dc00c4fd337851b8775888173270e901b02319d573e319c1e5d4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.0 MB (194994699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:833ef1f0967aba46040fadc0b3cd2e3f25bff3fb661eaae090864b619b671369`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:47:40 GMT
ARG version=11.0.9.12.1
# Fri, 11 Dec 2020 02:47:47 GMT
# ARGS: version=11.0.9.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Fri, 11 Dec 2020 02:47:48 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 02:47:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 11 Dec 2020 02:47:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4745f8afc1b0b851828482b818c87de04f0f2428325d2b3b259f694ee4e2c0`  
		Last Modified: Fri, 11 Dec 2020 02:49:43 GMT  
		Size: 192.2 MB (192197754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
