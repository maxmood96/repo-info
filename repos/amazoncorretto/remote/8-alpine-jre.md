## `amazoncorretto:8-alpine-jre`

```console
$ docker pull amazoncorretto@sha256:e7a7eac83af19f8d999e97e5bb5628e6f06515e6909a6480b99f65d4bbed53d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c1bfef33c8ad7e4b4860524b70101c35a65dc8faf98ca8863dd660e491b94f0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45603181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3536586bb4ad5111dfb1d62445a55cfca55471702901056e6407f2f1dac20a1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 18:59:38 GMT
ARG version=8.482.08.1
# Wed, 21 Jan 2026 18:59:38 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 18:59:38 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546fb189abad73aef87c876f2dceb51ca6fb1155894c5b4adc2b3086605b9a48`  
		Last Modified: Wed, 21 Jan 2026 19:00:15 GMT  
		Size: 41.7 MB (41743077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3ba7b48676b8675a551e1ff1a1c8a74a8df6e0e5beb03af61b5362b9ac16f487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.2 KB (197159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36cb5581f6ee7ecfe1bee88b4bca9f30a004845ef1f010ea8705cd49e3721a6c`

```dockerfile
```

-	Layers:
	-	`sha256:66509341a6a2294f789e4ab401bb69e29b0879848570d679cb60d1764cf75321`  
		Last Modified: Wed, 21 Jan 2026 19:55:28 GMT  
		Size: 187.8 KB (187843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a78fadd3b8b1d0123799028bff0841842c1eecec8b8c38327732342d2be43e6d`  
		Last Modified: Wed, 21 Jan 2026 19:55:31 GMT  
		Size: 9.3 KB (9316 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:fab8239f942f396478316f7daed2bec49cf8fa877b62ad4e3c76f2eebef4436e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45654773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d76888311ff5ec7c790679319145285757abab2934c20238a987a1170bd2e267`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 18:59:06 GMT
ARG version=8.482.08.1
# Wed, 21 Jan 2026 18:59:06 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 18:59:06 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2765a988a269006907aa5589f9f85cc938a2fabd4558c0e5a9bb24d346b5b857`  
		Last Modified: Wed, 21 Jan 2026 18:59:36 GMT  
		Size: 41.5 MB (41459034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:af9b097b98b2bbb0ba31d570cb79e28094d8430b136e9eb6d0a0b6dc4278e9b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 KB (196745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456521176c2bfc1f4353b418c40ebabb2463ac2f2c02ed48c153500482d6b54c`

```dockerfile
```

-	Layers:
	-	`sha256:87844206305ad4772793f5ce292e60a240d2f8b71ae873928a67236a2a8d0482`  
		Last Modified: Wed, 21 Jan 2026 18:59:15 GMT  
		Size: 187.3 KB (187325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b08769c811d58964b4f3b24ace21f35a60c1e313f7666fa06fa33200df96a467`  
		Last Modified: Wed, 21 Jan 2026 19:55:36 GMT  
		Size: 9.4 KB (9420 bytes)  
		MIME: application/vnd.in-toto+json
