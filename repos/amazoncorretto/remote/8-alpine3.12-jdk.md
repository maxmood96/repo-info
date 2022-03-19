## `amazoncorretto:8-alpine3.12-jdk`

```console
$ docker pull amazoncorretto@sha256:2f7aa4ec18ad5b98d43042eb0b517b549ee3015e37aebdc19281db54e9920bf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8-alpine3.12-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f0ef0c835a489b7a2141fe63bd161e739d6b993064ec27474d4b6ae9b4170270
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101916468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:347bb6d991db40a13ca18b9e1cc019c7ad563d6d559e6590599a12e8acb35940`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:45 GMT
ADD file:cdff961a4dd899295df5fd92711f8ee8fd8e682208d52bcfcfa3fcffd295821f in / 
# Thu, 17 Mar 2022 15:19:45 GMT
CMD ["/bin/sh"]
# Sat, 19 Mar 2022 00:34:16 GMT
ARG version=8.322.06.2
# Sat, 19 Mar 2022 00:34:26 GMT
# ARGS: version=8.322.06.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Sat, 19 Mar 2022 00:34:27 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 00:34:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Sat, 19 Mar 2022 00:34:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c7f02851fb7d4b5eb2cdd31353ecdcfc954d48241f12bbe91b831f73abe2d29c`  
		Last Modified: Thu, 17 Mar 2022 15:20:34 GMT  
		Size: 2.8 MB (2806202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb83de650bbd9ba46db73a62ed2aa7390374d99144a99111a01619067aef02a`  
		Last Modified: Sat, 19 Mar 2022 00:40:50 GMT  
		Size: 99.1 MB (99110266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
