## `amazoncorretto:26-alpine3.21`

```console
$ docker pull amazoncorretto@sha256:7a5bf8064b2d4f4f84ac76811676fbf6c3171c8d52a376435f253a1b2a4c3ff8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-alpine3.21` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1671ed32569aaf27252093a9979b868d2a3932ba9bef56cd4b7375df69e93d34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.6 MB (188559840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e8dbf5730fe474f24ddc400e78555e98f86c0c71444c411910942f3e4d5b6e0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Tue, 17 Mar 2026 22:59:48 GMT
ARG version=26.0.0.35.2
# Tue, 17 Mar 2026 22:59:48 GMT
# ARGS: version=26.0.0.35.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-26=$version-r0 &&     rm -rf /usr/lib/jvm/java-26-amazon-corretto/lib/src.zip # buildkit
# Tue, 17 Mar 2026 22:59:48 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 22:59:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 17 Mar 2026 22:59:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce232686e2b0a6fb4b727d4c19b053e592ab9f9cd684abce01d64fb771c68ca`  
		Last Modified: Tue, 17 Mar 2026 23:00:11 GMT  
		Size: 184.9 MB (184916098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-alpine3.21` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b996e6f125eea4444b9db242eba66f89aec85226d189a3630674da63f6364d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **600.2 KB (600213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e5af8efd3a9d5e71aecefcbb2dd15388d1700a75c1c1352c77aab97988f8820`

```dockerfile
```

-	Layers:
	-	`sha256:c046727c84a5e759025894fda23ce81ccbce06d4db60b75b62bf7dd1a2e5e5ad`  
		Last Modified: Tue, 17 Mar 2026 23:00:08 GMT  
		Size: 590.8 KB (590841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44f983048358e3fc883390a47a5bb2f4bc100124c259a8f54f3f0a6b2bb39e28`  
		Last Modified: Tue, 17 Mar 2026 23:00:09 GMT  
		Size: 9.4 KB (9372 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:178a6f7cf8689bdf1f9098b8250702c88d276ca95444a093551c088d5ade69ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.5 MB (186472996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fbe5cb9d9b4db7513d62eb40e15a919621f8c2b7f22d2afc5ea8d6a5aa6fb06`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Tue, 17 Mar 2026 23:00:20 GMT
ARG version=26.0.0.35.2
# Tue, 17 Mar 2026 23:00:20 GMT
# ARGS: version=26.0.0.35.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-26=$version-r0 &&     rm -rf /usr/lib/jvm/java-26-amazon-corretto/lib/src.zip # buildkit
# Tue, 17 Mar 2026 23:00:20 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 23:00:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 17 Mar 2026 23:00:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622e04540ec4677bad745be75ffc177f774bbca69fd9b0317b3d5a8956ed99f2`  
		Last Modified: Tue, 17 Mar 2026 23:00:45 GMT  
		Size: 182.5 MB (182480116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-alpine3.21` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6efc7672950a98efca3077a4e3356c2b79c62fbdb1ddc7a25270c21bf8d7b3b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.7 KB (599733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26979620670d6276dcf5ac303287e24afb9f87a138e839de457a3e02c9acf216`

```dockerfile
```

-	Layers:
	-	`sha256:f896f3c821ccaa820153ef2d09272006edb951477d43fe7bb39694d42089c4f6`  
		Last Modified: Tue, 17 Mar 2026 23:00:41 GMT  
		Size: 590.3 KB (590257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0eec8ae17e6e885bdfd8c97e0feae676163215cd5684a369dbaa30dac060086e`  
		Last Modified: Tue, 17 Mar 2026 23:00:41 GMT  
		Size: 9.5 KB (9476 bytes)  
		MIME: application/vnd.in-toto+json
