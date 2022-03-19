## `amazoncorretto:8u322-alpine3.14-jre`

```console
$ docker pull amazoncorretto@sha256:ed9a63ce9affad436b369e719d6d889106b2b304c471ad680cceffbaf965915c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8u322-alpine3.14-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b1a9c3a6020a0cf47e45042c915559531cf4d3c66a368045908cc975f8d37e50
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43197224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f591a90782293885cd102d744e2c8435a47449d23fd25eaed3d4b4a36e9d6ee3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Sat, 19 Mar 2022 00:35:01 GMT
ARG version=8.322.06.2
# Sat, 19 Mar 2022 00:35:18 GMT
# ARGS: version=8.322.06.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0
# Sat, 19 Mar 2022 00:35:18 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 00:35:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ce352f92dd94cc92e06e3061136bebf117cd4acb3779236c3063c8b28458be`  
		Last Modified: Sat, 19 Mar 2022 00:42:36 GMT  
		Size: 40.4 MB (40381055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
