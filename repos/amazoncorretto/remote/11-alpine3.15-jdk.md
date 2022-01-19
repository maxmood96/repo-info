## `amazoncorretto:11-alpine3.15-jdk`

```console
$ docker pull amazoncorretto@sha256:048c8890b9bb0c98fa5841005be3ca415bf6ce0235d4c74a371b866dc597c93d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:11-alpine3.15-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b1be710deee75a8719428766160dea3c7d77c7a87c8b8b55139ba6af612c0b7d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196281792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a9c968079e75644cd5a0e1b0860dbb73bb5b3cf92ea87bb0604fd7f8d7584b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Wed, 19 Jan 2022 22:04:04 GMT
ARG version=11.0.14.9.1
# Wed, 19 Jan 2022 22:04:11 GMT
# ARGS: version=11.0.14.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Wed, 19 Jan 2022 22:04:12 GMT
ENV LANG=C.UTF-8
# Wed, 19 Jan 2022 22:04:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 19 Jan 2022 22:04:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a3251f38791e7691414f65905503820ee784c2dfd4dd9fd09aeaae8c152002`  
		Last Modified: Wed, 19 Jan 2022 22:13:41 GMT  
		Size: 193.5 MB (193463379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
