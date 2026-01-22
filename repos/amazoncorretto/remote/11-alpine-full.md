## `amazoncorretto:11-alpine-full`

```console
$ docker pull amazoncorretto@sha256:77dad91c1da1fa2230f7f1fa2e465337281e6f9f5cc8c5d95291e5777f89c897
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:61dfa2e8d7791b718fb74511dc468c19c6be3798179b394be272a504e2fca980
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147446032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a30176560ca73a5e325f645f6f946808de0bc2e564aaada768ba7c84cef5da1b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 19:00:10 GMT
ARG version=11.0.30.7.1
# Wed, 21 Jan 2026 19:00:10 GMT
# ARGS: version=11.0.30.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 19:00:10 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:00:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 19:00:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37533683d9d9c426fc0a82ce538cf1d7151c8208b37752b241ceb9592c254abc`  
		Last Modified: Wed, 21 Jan 2026 19:00:27 GMT  
		Size: 143.6 MB (143585928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c32a80c4a6b9baf2db989c68c7fe69e6a89ff806cedaca062389cc9d80771494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.6 KB (599611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5a7d59b4754c738be26db78db1ed1d7114b65ab89fcf2f62bf43a42027441f5`

```dockerfile
```

-	Layers:
	-	`sha256:8a6f70ee29dc79482e9b170cc44eedd61cc14988d5dc2ab97af9b65ccd73ad67`  
		Last Modified: Wed, 21 Jan 2026 19:48:20 GMT  
		Size: 588.9 KB (588929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c04c2b3e12e2813c0e2cf2de0e5702afc40752f30845e1631cbeca0042e69490`  
		Last Modified: Wed, 21 Jan 2026 19:00:24 GMT  
		Size: 10.7 KB (10682 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d529c0e4180a5d135d8ca8b591b4bf736113794ce198c4f96ed280078716d1f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146051586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1040161fa121c96dff3453f474eb5a1f347573847bf908e9952877603c38b6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 18:59:01 GMT
ARG version=11.0.30.7.1
# Wed, 21 Jan 2026 18:59:01 GMT
# ARGS: version=11.0.30.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 18:59:01 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 18:59:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c016f1d7921cb0297977d531731dee15427272f3b40ad659102fa9e1c718223a`  
		Last Modified: Wed, 21 Jan 2026 18:59:18 GMT  
		Size: 141.9 MB (141855847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c9a59e7e8b0b840a947f7483209decf82246d770affb7a11d828638d72bde353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.2 KB (599217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83ab0179a6fc385dda5bad24dbe977b931d7199b9f8afcd7340240f12134c85`

```dockerfile
```

-	Layers:
	-	`sha256:7767a401fe2990247ec6f2327da95c57a971f3a2a152a9d5471239b2a14616ca`  
		Last Modified: Wed, 21 Jan 2026 18:59:15 GMT  
		Size: 588.4 KB (588383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cae6af08b33660bd64a21076a0352de3c8f68a04f51283e974f7abfd44dc4ba`  
		Last Modified: Wed, 21 Jan 2026 19:48:26 GMT  
		Size: 10.8 KB (10834 bytes)  
		MIME: application/vnd.in-toto+json
