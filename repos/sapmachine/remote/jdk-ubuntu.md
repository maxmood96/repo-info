## `sapmachine:jdk-ubuntu`

```console
$ docker pull sapmachine@sha256:4142c3cebe92a2816fc7664a979ccd8584a8ce15e42a3d618b40c28ab26aff6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:f197a006a1e6efa6a610e87ff1379d1849945ffb1282c351b7dd349e0c1c59f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.1 MB (262147077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca7cbd594bfbfa2fed5ab72059646e3129e8ae2f8cf5bee08598e68f3d08913`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:43:12 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:43:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:43:14 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 08 Apr 2025 10:43:15 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb74487086b0e317b63ed32b4dc0b06911fe4edb99d7db2daa58335d2f06ce69`  
		Last Modified: Wed, 16 Apr 2025 16:13:50 GMT  
		Size: 232.4 MB (232429425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:022b505c28d3f9a5e438d3b4e93ffe0cc0b9ba56f18d4abf4ddbf3b2b07607f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2478183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f8f0497f0c87c3fc9dd591bc03c13b01336708cbe92be66cf7f696793d9bb7`

```dockerfile
```

-	Layers:
	-	`sha256:524e4afb97c4c28ae12add924e7cfad815ba7eaee6c60c56c60edf03b43a416f`  
		Last Modified: Wed, 16 Apr 2025 16:13:46 GMT  
		Size: 2.5 MB (2464899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f5a36ee1a65460f6de66ed4a11bbe3c3233b2ad5acde37d53d77efe5c46dbef`  
		Last Modified: Wed, 16 Apr 2025 16:13:46 GMT  
		Size: 13.3 KB (13284 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:68c2a1e88b0e3506f18e09ad1e676b41309e5102ac9e034fa6c25338bfd31433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.2 MB (259206964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7845e4e798f0d07e83cc613c0041e218aab70d0ed92dadbf131f38504db1aecd`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:09 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:12 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 08 Apr 2025 10:46:13 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca5b195d2485c8941fd3560db8bd21646133d98b318e6b2b3a280a57560e1e75`  
		Last Modified: Wed, 16 Apr 2025 16:13:51 GMT  
		Size: 230.4 MB (230360006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b9af878fbba3f9f7573b78e2bad05f89f2dfd481cf33bf73c7d746456de0744c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2479089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bad3e2cc6f11b427356f1d26ee0080458042e64ad7c4736879193d07f38737c`

```dockerfile
```

-	Layers:
	-	`sha256:610ba45565b0baf99c815166651305e13b7f20659fbd78fc8d66042974407ccb`  
		Last Modified: Wed, 16 Apr 2025 16:13:46 GMT  
		Size: 2.5 MB (2465532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4d05e7158c803832a6000e2ed191d78f5e88d24931cb6f40f50dbd568caa4b5`  
		Last Modified: Wed, 16 Apr 2025 16:13:46 GMT  
		Size: 13.6 KB (13557 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:8416e274b81e1d859e2750afd64b8a0dce9f0902a57035fff3cd3cea2dc28fe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.1 MB (268111930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0041d8a59be4889d394696c014a5eac1310788d489092deca36254f4ac3e559`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:11 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:14 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Tue, 08 Apr 2025 10:46:15 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1ad4ce3eb227a8a7956abe526af7257ad5fc3e8233c2195ab8136b6d33fb9e`  
		Last Modified: Wed, 16 Apr 2025 16:15:01 GMT  
		Size: 233.8 MB (233771063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6f4c64c55786315eace4c1d8954a0334bc00722b1411a758551e99a9fb8b867a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2479771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a121075549327c97de75f13ac8606c57ad3253d6ddafc64c65863f31efc508e3`

```dockerfile
```

-	Layers:
	-	`sha256:20349a640c357f558f8f2b36c1c41c59b9a4be09c17ae0d75abc656435b6d566`  
		Last Modified: Wed, 16 Apr 2025 16:14:55 GMT  
		Size: 2.5 MB (2466358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0471d9a9071a5f236db247503395a7d808ccc8ca9d22e90ce763beb4d4771013`  
		Last Modified: Wed, 16 Apr 2025 16:14:54 GMT  
		Size: 13.4 KB (13413 bytes)  
		MIME: application/vnd.in-toto+json
