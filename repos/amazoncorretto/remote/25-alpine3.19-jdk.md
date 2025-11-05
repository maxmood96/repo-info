## `amazoncorretto:25-alpine3.19-jdk`

```console
$ docker pull amazoncorretto@sha256:6483fe4f6dd2265ff46a882ae51b833c5e74ea0fc566270ff3a75d9c4b50f3d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine3.19-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:635c0f4f53203e0a80fbe429aa396192f97887e1a076630a4830035517afad38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.1 MB (184134563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59fa1aa4661902f3e64f1f544bab3d5aa6a1a656b29fef6cd46a09a12a6f0a9d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:40 GMT
ADD alpine-minirootfs-3.19.9-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:40 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 01:07:05 GMT
ARG version=25.0.1.9.1
# Wed, 05 Nov 2025 01:07:05 GMT
# ARGS: version=25.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 05 Nov 2025 01:07:05 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:07:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 05 Nov 2025 01:07:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:17a39c0ba978cc27001e9c56a480f98106e1ab74bd56eb302f9fd4cf758ea43f`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 3.4 MB (3419815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ad7b96ac2d62c8cb2702f5c048a79f6f8a2bc7f70ce17fceb0763d0bfdf734`  
		Last Modified: Wed, 05 Nov 2025 06:45:27 GMT  
		Size: 180.7 MB (180714748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b58547a8715a560f3a88be50945f419084858ef6aac9f249e6873ec0f2b243dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.4 KB (603426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f442cdaab7f49884070f99b355a9c9f892418c7669940f80d4e3d81da077fff`

```dockerfile
```

-	Layers:
	-	`sha256:c482cca3d380cc6cdf15d7bfd37165ad215ad7a11e8119d43fab53febb4be4cd`  
		Last Modified: Wed, 05 Nov 2025 04:49:49 GMT  
		Size: 594.1 KB (594055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e72c46d0dd8be307a96e6cf818c1a4036173dc93933e7a7bbd16a56cbadc84e`  
		Last Modified: Wed, 05 Nov 2025 04:49:49 GMT  
		Size: 9.4 KB (9371 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine3.19-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:48e0b9876f0e30215183b32e94a4838f692e68993053cd01f7c8bd2a15b56099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.7 MB (181732411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5459f697d29cd2e948dd9b94b2f9d80d284c463f55954e11d0b3cc73fb8e37e4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:40 GMT
ADD alpine-minirootfs-3.19.9-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:40 GMT
CMD ["/bin/sh"]
# Tue, 04 Nov 2025 23:16:22 GMT
ARG version=25.0.1.9.1
# Tue, 04 Nov 2025 23:16:22 GMT
# ARGS: version=25.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Tue, 04 Nov 2025 23:16:22 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:16:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 04 Nov 2025 23:16:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5711127a7748d32f5a69380c27daf1382f2c6674ea7a60d2a3e338818590fea1`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.4 MB (3359301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d7720b4309abda73af51f29b88a62219f5fa3cd19a0b3ce57bfaa3085720c8`  
		Last Modified: Wed, 05 Nov 2025 07:10:29 GMT  
		Size: 178.4 MB (178373110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1b3f33860033e60dcd6dde30b0728de04e0e4cf88c6644ab5444160ba57885ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.9 KB (602946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08e0f0c90e3866690c9b08739de14e04c1b24767a234a3cb7c99b44fa6362f45`

```dockerfile
```

-	Layers:
	-	`sha256:e932532a2c2d6602cefc9f7bb89b2388ff17bd648cca713c1f0c5b2e56d6a0d1`  
		Last Modified: Wed, 05 Nov 2025 01:49:59 GMT  
		Size: 593.5 KB (593471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e813bfc292dd6f2c474b4109ca61be3cf0e35486a23163f6a2377b1175489779`  
		Last Modified: Wed, 05 Nov 2025 01:50:00 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json
