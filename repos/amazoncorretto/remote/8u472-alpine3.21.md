## `amazoncorretto:8u472-alpine3.21`

```console
$ docker pull amazoncorretto@sha256:40bc146f8ee72dc764684f12d82bc5b1831e82f6f1d556fbd7fcc6e69ebf36ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u472-alpine3.21` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6dd1b5cc512919c6fe88d78ed96accf01c588bc64fb38919a192945d91f6e747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104400088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7489fc53bc0153f84aad9140898451fe39c3ee221ddac084aff79cdb26d6b08`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=8.472.08.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=8.472.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Sun, 07 Dec 2025 13:55:07 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c11a284cb99ad969ccb8fe7b9a6cbd6a68074a346f5d2cde10c23b35542cdcd`  
		Last Modified: Tue, 21 Oct 2025 23:25:43 GMT  
		Size: 100.8 MB (100757519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u472-alpine3.21` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fe96ace4bda18ce99ada88717eb094076397f06f0904407457c4ee565d9bee9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 KB (260327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac91506d577c9ebd44e421393b3b740a68d3a194debf5eb42628a778a7b0f1c4`

```dockerfile
```

-	Layers:
	-	`sha256:0faf2f558fb064eedb2505652b3271feab574b0940d59e0d5837edbdb6395f13`  
		Last Modified: Tue, 21 Oct 2025 23:25:41 GMT  
		Size: 250.9 KB (250929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21aeb388fc4971201dce77f187a3bf67a6b9d86559c558fafbd93d53b8c599ab`  
		Last Modified: Thu, 01 Jan 2026 16:39:05 GMT  
		Size: 9.4 KB (9398 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u472-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:fd4ea940079afe9bac34057492b061a17997727b35520c1f917ac47b97a17343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104525667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f393929456b6153681c0ef5bf39d4003a93826fbb54ea5f30d0e19b810276c53`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=8.472.08.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=8.472.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Sun, 07 Dec 2025 17:54:48 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7123485e9d560b8d5c763149aca82f356523037f9d5de179f0ae8aeec403c441`  
		Last Modified: Tue, 21 Oct 2025 21:49:15 GMT  
		Size: 100.5 MB (100533314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u472-alpine3.21` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:af7091d222f0d937e347af26d81cfc1ecfdb97b9100a3bcf32fc4f3fa1d9f075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.6 KB (260563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5255b9d1e4362dfd48ee64143c6c6f52d6eb92ef556f3720756d89d40cb7dd9e`

```dockerfile
```

-	Layers:
	-	`sha256:339e19a482086f7420e51abc2158eadfef87010feb904c8e36708509fa41ddb5`  
		Last Modified: Tue, 21 Oct 2025 21:49:12 GMT  
		Size: 251.1 KB (251061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fccbfc2ede76c6385c3a76f11b62f0d4cadb283c63e332a3a6c28db8dc78ca00`  
		Last Modified: Mon, 19 Jan 2026 10:37:37 GMT  
		Size: 9.5 KB (9502 bytes)  
		MIME: application/vnd.in-toto+json
