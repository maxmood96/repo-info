## `amazoncorretto:8-alpine`

```console
$ docker pull amazoncorretto@sha256:c95b7a8b94480aedc11755abc9c8b7d5bd44194a546d5525622383461f4c2c4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5adb5fce00b5aa8d5936669c3884441caf8c39d3562dc1748519ae0fbc30eadf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104094871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ee1e915ef5d353e2664da9bc6d25c1cf8e88cf074da7eb027efe3b025a369b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=8.462.08.1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=8.462.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 18 Jul 2025 19:06:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73204ee579640710093fde3a57e563aa1538477f34cc691377b3deae24a5bb61`  
		Last Modified: Fri, 18 Jul 2025 20:07:43 GMT  
		Size: 100.3 MB (100295182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:982f8fe30d4e37d6f426ea58b4237dfd8ae75dbbd29efd36c800201b9654d500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.7 KB (261669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ac9a2b9114af693cd5e580e7c25355172089bbedaf7f88240403cf2a5bdb7c`

```dockerfile
```

-	Layers:
	-	`sha256:fda24206ef547b27d86beb22b9f60e5d93104715a690e0b0ea69af2971b44698`  
		Last Modified: Fri, 18 Jul 2025 21:49:02 GMT  
		Size: 251.0 KB (250973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd03bb47afba7d386b28517cd8324eff702de6780ca7cfc246e886a2b34313f8`  
		Last Modified: Fri, 18 Jul 2025 21:49:03 GMT  
		Size: 10.7 KB (10696 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:dbe3e4243c323bc0ade604a4ab00ee70bb09ebb75e9426c8006865f8ca045b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104223113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e05cd3244d4b86ec4e1f6d491e21a25f28106e3042d04c23ce95d28778ccda7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=8.462.08.1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=8.462.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 18 Jul 2025 19:06:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac20185427f1c943ee893d60f765f6e7ef03a7b7fc6c4199d972082d5f1172b`  
		Last Modified: Fri, 18 Jul 2025 19:53:18 GMT  
		Size: 100.1 MB (100092363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:75654266d30c25ee39a3d039c0ab964e5403e79a80f195e24e183a6482fb97b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 KB (262001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da56e9ac2f6bd9bed07f4366da3f456f99ea5ea091c73521a9b0bf1e464762d8`

```dockerfile
```

-	Layers:
	-	`sha256:e7d8dea64c53802050dbefad0737a3fcc40dd178945e1bfb74580318ebeffe20`  
		Last Modified: Fri, 18 Jul 2025 21:49:06 GMT  
		Size: 251.2 KB (251153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47be5c6459fa220d38b5c1975a406566abb213c06f63eefc9785d18e7fe9e6be`  
		Last Modified: Fri, 18 Jul 2025 21:49:07 GMT  
		Size: 10.8 KB (10848 bytes)  
		MIME: application/vnd.in-toto+json
