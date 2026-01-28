## `amazoncorretto:8-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:a5ce6cad50f9b5c14bb19be81e1687dcf3b1dd6a8af8bb208c73fcd707ac4ca7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ff864ef816a5e3e5b9ebf34cf37df66c768e32ea9160ed7227d7c6628278f19a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104638741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3eecd3db73d8a970e8228e4cf8221842da6ddbb2e3cef600a76b24ad76752a2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:43:25 GMT
ARG version=8.482.08.1
# Wed, 28 Jan 2026 02:43:25 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:43:25 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:43:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:43:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c6833e8b5869e0f48dfb0827fe8ce0f2ec7bc4abc9a375d40ddca18d755ab20`  
		Last Modified: Wed, 28 Jan 2026 02:43:38 GMT  
		Size: 100.8 MB (100776920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2274d3ee0a3fe24965ab0343b039202fb420dd051a086f9bd99a972f2aba9eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.2 KB (261174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f04bb3ddcf3b86f143a0743e7c15618dc1dd5cc7f83a17298da392b6ab951905`

```dockerfile
```

-	Layers:
	-	`sha256:ea3d84eeb5914b227890be9e03a7f468b1238696c34ca3c9623f2926c2ef8329`  
		Last Modified: Wed, 28 Jan 2026 02:43:36 GMT  
		Size: 250.5 KB (250521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ba7f4ce446fd8cdbc9939e56abcfd0dd3ddd5b346e22316724e74203c2153f7`  
		Last Modified: Wed, 28 Jan 2026 02:43:35 GMT  
		Size: 10.7 KB (10653 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:41ffcd684ee9c015cd76b8f91efdb9b0635463e1744307dc79447664679b3bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104759452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:006086a51106220067d30896dd6eaf36cf30e70e92b4ca5e0516960a76bd8293`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 18:59:38 GMT
ARG version=8.482.08.1
# Wed, 21 Jan 2026 18:59:38 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 18:59:38 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 18:59:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047533b14f4ab303c4d71a845580fa91d40febf5ca499462201ad8920789770a`  
		Last Modified: Wed, 21 Jan 2026 18:59:52 GMT  
		Size: 100.6 MB (100563713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1e399a6a671494aaacdf167bc62f67a23654fca69c291ae230a44def7eb5cb17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.9 KB (260856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b637de84fe39a27b8c93f90fd5ccaeae1fd927fdccddf07c02b4e0f53b140e77`

```dockerfile
```

-	Layers:
	-	`sha256:408fa38a2827f1a78eb696affca407e8c8dad7c4f730c93d6feb171965042df5`  
		Last Modified: Wed, 21 Jan 2026 18:59:50 GMT  
		Size: 250.1 KB (250051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07fa31f493011a7e5e7ebe64d492dc705eda46144d10d26a1b601e1f93d16d8f`  
		Last Modified: Wed, 21 Jan 2026 18:59:49 GMT  
		Size: 10.8 KB (10805 bytes)  
		MIME: application/vnd.in-toto+json
