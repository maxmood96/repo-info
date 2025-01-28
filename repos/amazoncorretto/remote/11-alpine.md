## `amazoncorretto:11-alpine`

```console
$ docker pull amazoncorretto@sha256:21a3775e5d63667c014925de669f79f9155961b8b376f68a1081216a9342a75a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:83805acf392e49256089043743e7a18448a12a178d3218285dbf0051b28b7f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.6 MB (145552551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab7b2e39566c06eb64e2bf6241edd969109e843952bf5de33ab0632c98d5216`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=11.0.26.4.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=11.0.26.4.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a915fe4a043559f177f7ef109470731297bd54126f275972376046f80d3a2b2`  
		Last Modified: Fri, 24 Jan 2025 23:26:32 GMT  
		Size: 141.9 MB (141910836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:07dd1bd815b21f12cb66a0dd1a9af05d9056a4e8f74f56f32270223d1d767c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.2 KB (401215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1941be06b5d4549157b3d98a467b1a5ef56d4c73a8f47d3bed5db7c86582823e`

```dockerfile
```

-	Layers:
	-	`sha256:a739b7a50131b21d697bcf15d9436071efed5fa5c7d447adba8a139293f0193d`  
		Last Modified: Fri, 24 Jan 2025 23:26:28 GMT  
		Size: 390.5 KB (390491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c39dab563449bd3d325f716f50c9e939bc75c408f78a5625dbf36f048fd2de22`  
		Last Modified: Fri, 24 Jan 2025 23:26:28 GMT  
		Size: 10.7 KB (10724 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:161f3feca13b7a9418ebd822cc5f4d6258c93b3eee5e08c49e08c92a2508f0d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (144027225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e35e95dd90fc71a442551fd73a7f3aaf15d9591ebc2beec89e519c6169cdba`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=11.0.26.4.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=11.0.26.4.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ec5dfe54623281a40254bf460746e547599d8a234a62d6d68cfd2080a79453`  
		Last Modified: Fri, 24 Jan 2025 23:27:29 GMT  
		Size: 140.0 MB (140034866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:57d99b392163c73e398399e8d89ee245fd195c914ef64b52b5ffa9cc11f8fc97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.5 KB (401472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7cbc3bff947a3aed489ab3b7bbba07281660c98d55189e223bd82e509d9201`

```dockerfile
```

-	Layers:
	-	`sha256:d5ae6c8ab4a5c805658a1a2cbeef3d2651eb3aefac827762c0ad93c9cea8cf2e`  
		Last Modified: Fri, 24 Jan 2025 23:27:25 GMT  
		Size: 390.6 KB (390595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9399a2554c9fba24d42ff4b0c9f3c268338b8dc185b36185c7a6890dd5125614`  
		Last Modified: Fri, 24 Jan 2025 23:27:25 GMT  
		Size: 10.9 KB (10877 bytes)  
		MIME: application/vnd.in-toto+json
