## `amazoncorretto:21-alpine3.21-jdk`

```console
$ docker pull amazoncorretto@sha256:e2e2f8d10373f16a1a4dcd8dbdd8ced7ceb5ef14b318a4c83f9eef55a59606f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.21-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:205526a42c31fe002b54b920362e8c8d6b7d2c07ecf54fa00fbaa54ce49626ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162675384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adfea98241c4df24e7f15c569cfcba04ac7a4a543694e8c9e6dba2e2c28f986e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=21.0.7.6.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=21.0.7.6.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 15 Apr 2025 21:50:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209e4116f79b2918b726369fcc5f1d66871a9826a9cc697241281621042e8ac1`  
		Last Modified: Tue, 15 Apr 2025 23:55:56 GMT  
		Size: 159.0 MB (159033137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.21-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0db63aab1d631d59f553e1e2a83efaa9db1ec26813cdeb0e0e5010d62c299aa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.3 KB (394312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a48a99d9e6d868cc1b0dc12f0f09a97d444837e4cad100c84b5fa900baac435f`

```dockerfile
```

-	Layers:
	-	`sha256:834ad402454d7e8bdf6886c2e853825886ff607fa680dbd464eb423d508521c3`  
		Last Modified: Tue, 15 Apr 2025 23:55:53 GMT  
		Size: 383.6 KB (383592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41c68cf7ba7124a69e6fac36d29614eebc87b3863aa4323dec356757305569ae`  
		Last Modified: Tue, 15 Apr 2025 23:55:53 GMT  
		Size: 10.7 KB (10720 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.21-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:75403d7a1019b2bbe5a801dfd16ba457d078eb8db09634607f91e658a150746b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160928341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ff865341883b5501d04efff6d005b2c01fc18408ae749d9f78cd24a3995b2b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e191a064c87c1670d74b11fad78096a8c5d30bbd31d3e71b3dbe4d032af4cdaa`  
		Last Modified: Fri, 14 Feb 2025 22:39:49 GMT  
		Size: 156.9 MB (156935312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.21-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8820ba37f26ae61936f6650e97284495054990e708ec6cf9bdfdaff696f8e6b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.9 KB (393931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd4b01c4e7aa7a43f02f03c477827b690b5f57e7496cff0a153ac5c391c7a3d7`

```dockerfile
```

-	Layers:
	-	`sha256:1c12abe5adfd0f23313bbfdb64a951e1743758c86c9b3b384f2a8b61af7ec79d`  
		Last Modified: Fri, 14 Feb 2025 22:39:45 GMT  
		Size: 383.1 KB (383059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:102b07d0a85ffa099b1ceebe4c6504e1a02d002128eb94827d9c320dcccaca9f`  
		Last Modified: Fri, 14 Feb 2025 22:39:45 GMT  
		Size: 10.9 KB (10872 bytes)  
		MIME: application/vnd.in-toto+json
