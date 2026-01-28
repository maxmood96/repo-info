## `amazoncorretto:21-alpine3.20`

```console
$ docker pull amazoncorretto@sha256:cf9b393e92bbc27283b5c5b969960f2d4ecefd060c0a44b7c3e7055d9fab9f13
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.20` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a5d7175503b5e4526ac85d4a889853586360adfdac2bfeb7722372683a0d8a5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.2 MB (165205984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77fd02cce3d0008cc249f1322b201bea11ba9f9bd5fa485b593b27e26d90223`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:48:46 GMT
ARG version=21.0.10.7.1
# Wed, 28 Jan 2026 02:48:46 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:48:46 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:48:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:48:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b361f814b6886f0da2cc6f6c4f46b2fadaa7dcae4177efc119f5dae490c4f2`  
		Last Modified: Wed, 28 Jan 2026 02:49:05 GMT  
		Size: 161.6 MB (161578120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:34a00fe882eca9e1898702daf13424143b3489828b289b4fe118b81cd75e629e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.9 KB (589930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee12bcd4648371da822321ca4e9f7b078afcfafd547bcfbaa46d6266ecf7232`

```dockerfile
```

-	Layers:
	-	`sha256:29328acb49075b9f09034cfedb18186bab1a3e98c6b2211deac7e34e585af48c`  
		Last Modified: Wed, 28 Jan 2026 02:49:01 GMT  
		Size: 580.6 KB (580557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9391ebda45107c4ec1e36330379c3351d95d16b72fa966ebddc615744fe09d5`  
		Last Modified: Wed, 28 Jan 2026 02:49:01 GMT  
		Size: 9.4 KB (9373 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f5b66789281dbc27256df3f2e53dcfdf4e554e3e7d796309026a79b1d14fc7d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163708807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e5e9912c981cc17e5c76823ed8ecc0a772407ff5a9ace73b197552f1258b458`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 19:01:22 GMT
ARG version=21.0.10.7.1
# Wed, 21 Jan 2026 19:01:22 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 19:01:22 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:01:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 19:01:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Wed, 08 Oct 2025 12:02:47 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aad94969b530bfd5e73fd625a447fc905ac466cd49bffcab6a5961d341c6f49`  
		Last Modified: Wed, 21 Jan 2026 19:01:41 GMT  
		Size: 159.6 MB (159619430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c85bbec49a36e54905e3ee88701242930d691b8b7e9b201a4e1c338633d5c101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.5 KB (589454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6727b35482f303d6950bfb557e2fa22046aeba65c17e7472d0894996db49057f`

```dockerfile
```

-	Layers:
	-	`sha256:9677c4346f88197ffb2098711cd97c18e2e03e7a882eb1ce9692456df6578805`  
		Last Modified: Wed, 21 Jan 2026 19:01:38 GMT  
		Size: 580.0 KB (579976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3963b1447d53f64f0da505daee522840db0fa0b710feee6b2d97ef52f015a416`  
		Last Modified: Wed, 21 Jan 2026 19:01:38 GMT  
		Size: 9.5 KB (9478 bytes)  
		MIME: application/vnd.in-toto+json
