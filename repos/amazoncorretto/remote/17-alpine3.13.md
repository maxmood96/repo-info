## `amazoncorretto:17-alpine3.13`

```console
$ docker pull amazoncorretto@sha256:edc4a5455b7b3d39e6eba3e4176f4605acec64e3c6c63334d2dfad10c870bb05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:17-alpine3.13` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2d1d73ca4979aad4420f6ec57c1fe11b23143bfbce12c9e8036f91cd03372f57
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194632226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34f010ee593263770a155266e48508bcff96c9ae599a3f8af80baec2e85f2fe3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Wed, 19 Jan 2022 22:05:03 GMT
ARG version=17.0.2.8.1
# Wed, 19 Jan 2022 22:05:09 GMT
# ARGS: version=17.0.2.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0
# Wed, 19 Jan 2022 22:05:10 GMT
ENV LANG=C.UTF-8
# Wed, 19 Jan 2022 22:05:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 19 Jan 2022 22:05:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19cf9363da7ba080b91a26d6ac2b190a8f1ddd8cff87a79270d4fc25ff6fe21e`  
		Last Modified: Wed, 19 Jan 2022 22:16:37 GMT  
		Size: 191.8 MB (191809801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
