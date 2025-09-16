## `sapmachine:jre-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:e31805aadc1d162cc671c20f955856ad8c18bd88df50eea392a5e4e5f3fb1902
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:b5f35dc1860e3e4329ec66ee35d010d22e14a7f34efc5272c3a8d919e818249f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 MB (96614276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0c41d8f9de0ad648a9681b4cedfb6952ca24e3d1fa24382854978191c062cb`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:20 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:20 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef8c32fbe5a88f273114c96f21eb6cebe0a6f7c9d82b54d35c4a7c3d9847686`  
		Last Modified: Mon, 15 Sep 2025 22:27:43 GMT  
		Size: 66.9 MB (66890826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:23e8c30dcb5aa6191646b72bc3ac972e9ee6c5f269c5f9600e952e103a45b516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2292801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e631ac71b37bf3c85a0227dd793d103e7de6c545af8c2e8f634411d429d113`

```dockerfile
```

-	Layers:
	-	`sha256:bff52d8e07296fd9113b448a5ff524d7cec309ab636eb9f18565847baaf84c0b`  
		Last Modified: Tue, 16 Sep 2025 00:10:57 GMT  
		Size: 2.3 MB (2281200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:325184377c718c8beb0dd17cb36271a07279f5da062105de857b51b64ebc7b1b`  
		Last Modified: Tue, 16 Sep 2025 00:10:57 GMT  
		Size: 11.6 KB (11601 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:abdc26b74b6f68770a244edcd8e09e1e74e209c2bcccb3d1e7d50008206d36f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94798634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e3030710745bcca0cf0823d677371d75f8b3da3d8c0b297c189cb7bfb28db05`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:20 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:20 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2b7ed95d4daaa146f86f903d4b2e87e4fcc9fd7ee093942821543225d577c5`  
		Last Modified: Mon, 15 Sep 2025 22:25:56 GMT  
		Size: 65.9 MB (65937317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:12952191d48bb015cd386cedefcacc5e04523eb1dd310ab8b8b5f25f6b6756bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2293553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6616cc9761dc493f0c59e8c61fe116314503ec00772b4ed39da90e9ad9e37ce1`

```dockerfile
```

-	Layers:
	-	`sha256:0536dadbe044b8b4f61907d5f2c235c1003f038bb76bd2bedec427bfb2658014`  
		Last Modified: Tue, 16 Sep 2025 00:11:02 GMT  
		Size: 2.3 MB (2281752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75670a0b5db99d405fda017fde95356d7301e7ab8f98ba6508bbb52fc697e6cb`  
		Last Modified: Tue, 16 Sep 2025 00:11:03 GMT  
		Size: 11.8 KB (11801 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:8319b829ad89646b0ffc4bbca96f7d093fb4246b9297ece546e386c8606a7c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101963338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb20d37c16a05b77cd95d4ee3f1ccb7bc85d9b696373b79ddc64ff8427bebcf4`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:20 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:20 GMT
ADD file:55e5af389c76b79c77275691d488810a1fd875fe7e47b4b14a8b70f1230bf1a2 in / 
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5128fb40eedc06172c4cc2920b45ddb874f5b42c161d0a777ed53f0b9f80b8e7`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 34.3 MB (34329533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48149862eda7cf5716d342b7adb46e048c7c6828e961900161fe3eea19788bda`  
		Last Modified: Tue, 02 Sep 2025 01:53:15 GMT  
		Size: 67.6 MB (67633805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f796a96ee9ba7521f4277a540f6d318c7522a518ead08a632533ca7584f51a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2290282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31526fbd79e7316912ee1abf11c969d16e86d936cb875b97688e376df6a40b52`

```dockerfile
```

-	Layers:
	-	`sha256:5ab593365f9fc1b79f4494e52391bbaee68b2368429278d35b8a134b08f9934c`  
		Last Modified: Tue, 02 Sep 2025 03:09:50 GMT  
		Size: 2.3 MB (2278590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da6f163375a1fa90bf8cd45fd3f467ce01092ee233bf45b2a1e706882cc53c54`  
		Last Modified: Tue, 02 Sep 2025 03:09:51 GMT  
		Size: 11.7 KB (11692 bytes)  
		MIME: application/vnd.in-toto+json
