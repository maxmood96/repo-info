## `amazoncorretto:8-alpine-full`

```console
$ docker pull amazoncorretto@sha256:48ced6cb07acca793c83441f1bc1dcb9db414ecbf1357d8d0cbaa467e95b46cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:be77811c01adf2b5c39748012026a9b6348d7adee4a8cbf7747ab474d79633ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104636996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461124ced3bdb08b0f7894672a72bd7b998f14c64d8c9d61d299a25621a9b212`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 18:59:02 GMT
ARG version=8.482.08.1
# Wed, 21 Jan 2026 18:59:02 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 18:59:02 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 18:59:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003da162f155cdfcf4369568a4cd7d92ffc15e92bfbf342de3a2d17e188030d8`  
		Last Modified: Wed, 21 Jan 2026 18:59:16 GMT  
		Size: 100.8 MB (100776892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f5c06762096f8c7fa8a327a7d9acc0d6e3bb586240b6b0b4c2e862654f7f463d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.2 KB (261174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4fd547e3aad8736be1b03419be7bf4f6dac45952e61866595248c055a2ac4ff`

```dockerfile
```

-	Layers:
	-	`sha256:892e39c5d60a615ce440a56efff3486e0de6c8d3c03f4177dc6c24fa5037dbb5`  
		Last Modified: Wed, 21 Jan 2026 18:59:14 GMT  
		Size: 250.5 KB (250521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bb4afd59773200eb04bf0f808305575f5c4baef92d09c6100ac24a86342f174`  
		Last Modified: Wed, 21 Jan 2026 19:55:21 GMT  
		Size: 10.7 KB (10653 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:41ffcd684ee9c015cd76b8f91efdb9b0635463e1744307dc79447664679b3bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104759452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:006086a51106220067d30896dd6eaf36cf30e70e92b4ca5e0516960a76bd8293`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 18:59:38 GMT
ARG version=8.482.08.1
# Wed, 21 Jan 2026 18:59:38 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 18:59:38 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 18:59:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047533b14f4ab303c4d71a845580fa91d40febf5ca499462201ad8920789770a`  
		Last Modified: Wed, 21 Jan 2026 18:59:52 GMT  
		Size: 100.6 MB (100563713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1e399a6a671494aaacdf167bc62f67a23654fca69c291ae230a44def7eb5cb17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.9 KB (260856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b637de84fe39a27b8c93f90fd5ccaeae1fd927fdccddf07c02b4e0f53b140e77`

```dockerfile
```

-	Layers:
	-	`sha256:408fa38a2827f1a78eb696affca407e8c8dad7c4f730c93d6feb171965042df5`  
		Last Modified: Wed, 21 Jan 2026 18:59:50 GMT  
		Size: 250.1 KB (250051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07fa31f493011a7e5e7ebe64d492dc705eda46144d10d26a1b601e1f93d16d8f`  
		Last Modified: Wed, 21 Jan 2026 18:59:49 GMT  
		Size: 10.8 KB (10805 bytes)  
		MIME: application/vnd.in-toto+json
