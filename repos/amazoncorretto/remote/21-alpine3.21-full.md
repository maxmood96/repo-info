## `amazoncorretto:21-alpine3.21-full`

```console
$ docker pull amazoncorretto@sha256:1b53a05c5693b5452a0c41a39b1fa3b8e7d77aa37f325acc378b7928bc1d8253
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.21-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d4eb1978220a3ba2551e407d3d279bfc77a8903932814a0b4166bbee6588f92c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162597545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda9333c96c8382ec8566a920fe1b4778812d8b8f5097108369b76cbea998d6e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d56f35012a0efb0cf3144f926e650140b492ee84050727c5057e3319c49c1db`  
		Last Modified: Fri, 14 Feb 2025 19:12:53 GMT  
		Size: 159.0 MB (158955298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.21-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:929e328f5855b67c411454a42ca31cc7308a0d79a5e94a00cae681d6d5ad039d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.3 KB (394312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:895ec83d3fc2cd29421e567fa9960d0efc1aecd538cd51fc5094eaaf31e285fc`

```dockerfile
```

-	Layers:
	-	`sha256:5abf33a5bafd90470efcba33c903c901d2bc4b440403b60c9c37edf5fdde75e0`  
		Last Modified: Fri, 14 Feb 2025 19:12:51 GMT  
		Size: 383.6 KB (383592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:802b13fd04776ae20036da6fc1a4f46390c74a3399e014d1dae5eabd122fa924`  
		Last Modified: Fri, 14 Feb 2025 19:12:51 GMT  
		Size: 10.7 KB (10720 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.21-full` - linux; arm64 variant v8

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

### `amazoncorretto:21-alpine3.21-full` - unknown; unknown

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
