## `amazoncorretto:8-alpine3.19-jdk`

```console
$ docker pull amazoncorretto@sha256:eefd201c96ef5201a4858c6f464d088767030500412dc884a2b8fd7637aee6ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.19-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d6b2d311a9e356d47e75951a3b3654f3b92dd4478a91a511d92f1e8810c81fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103616948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3116f342832df3bed7340226c2039b471d4c1fbb4eb50ccd0a9b28e6fe3c8ce1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=8.432.06.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b700b01e0c01a7eaa4c2d32ba640aa5527e1cc03789feb8f2d7321961c88f3e`  
		Last Modified: Tue, 12 Nov 2024 02:11:45 GMT  
		Size: 100.2 MB (100197220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ef4cb14abafe94fdb383a206287fdb9389507f139a9d4c5da40c83cceed5c0be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 KB (255282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efcfcc14941d7ac5796bde0a832f96ed9b6f68619c5c8140dd38b5597aa31a51`

```dockerfile
```

-	Layers:
	-	`sha256:1aca4df51ac3d84810361407f423f61794f532a9d7ec16202d6bf3282cb56536`  
		Last Modified: Tue, 12 Nov 2024 02:11:44 GMT  
		Size: 245.9 KB (245885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78a94c85a82a1e1f05af614c1e9a5b7edd4e7577f6e8f8a58ed900ef8d5142e3`  
		Last Modified: Tue, 12 Nov 2024 02:11:44 GMT  
		Size: 9.4 KB (9397 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.19-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:bdab83426a1f43dcdd133b3da29ceb7c7c3db2c4b0501f9000c785c8f660f75f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.3 MB (103338088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:733cbed5308751eaabbb7a153e65567bda7ba74c7302afa92b86f40c18fc65fd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:16 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 06 Sep 2024 22:44:16 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=8.432.06.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3522236ec70b3044238d56d02ab22ea1f719f75fd641dde2ed0c2b895fe8c08a`  
		Last Modified: Wed, 16 Oct 2024 18:09:16 GMT  
		Size: 100.0 MB (99978985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2328f586ef0c0d107236cb70ed9283051cbcd18b1367e7126e38fe200be3c935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.2 KB (255212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d70d85535f9287934d71196f9607d31b927049e53ee4ba3e3383fe9aedd5fb4`

```dockerfile
```

-	Layers:
	-	`sha256:b7bf72ec388ddf4d3399d8ffe05631b45453aaebba8cf84ab7464a0dcb16442b`  
		Last Modified: Wed, 16 Oct 2024 18:09:13 GMT  
		Size: 245.9 KB (245924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2481605f45d42f65d87ff7e3bf9aeeb3140e1faa15b457772b1d446f7e113679`  
		Last Modified: Wed, 16 Oct 2024 18:09:13 GMT  
		Size: 9.3 KB (9288 bytes)  
		MIME: application/vnd.in-toto+json
