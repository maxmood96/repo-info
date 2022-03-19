## `amazoncorretto:17-alpine3.13-jdk`

```console
$ docker pull amazoncorretto@sha256:2e96b52e6b68dad22c902d2e7a70487c6f9e1cff55d2418b0836da981b4c7517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:17-alpine3.13-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e420d314ada29fc1e1625d5e37740d2617ad824f840f06fca9de5eafb0f8aba4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194626980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add00493ae55aeff598ddd165e32d3d570b083b67060facc71509b99a39c83ae`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:36 GMT
ADD file:51c08645923aa2d3513f66571f0c598a727dd5805e4f2bb87fb660b2f789348d in / 
# Thu, 17 Mar 2022 15:19:36 GMT
CMD ["/bin/sh"]
# Sat, 19 Mar 2022 00:37:53 GMT
ARG version=17.0.2.8.1
# Sat, 19 Mar 2022 00:38:03 GMT
# ARGS: version=17.0.2.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0
# Sat, 19 Mar 2022 00:38:04 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 00:38:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Sat, 19 Mar 2022 00:38:04 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:e1096b72685a2366348e697f5b57e3b8feb41660e3dbe68447e168381515111a`  
		Last Modified: Thu, 17 Mar 2022 15:20:24 GMT  
		Size: 2.8 MB (2817181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90ff3681a1f30145536f6295352147f0b226c095fd11d5e9f85f7a711391118`  
		Last Modified: Sat, 19 Mar 2022 00:46:55 GMT  
		Size: 191.8 MB (191809799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
