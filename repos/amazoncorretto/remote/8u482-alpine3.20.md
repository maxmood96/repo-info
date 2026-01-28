## `amazoncorretto:8u482-alpine3.20`

```console
$ docker pull amazoncorretto@sha256:c99701d66281b621e2b03707d00b75b5165bb4f57a15c84b991d86ba98e45cb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u482-alpine3.20` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:befdcd236ad5d5e699344644080305c7bb2014f9069ded52ee439182afc0b8dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104402724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68c41c38696d11f883eff1970913412d5f4bf1d0f7a04ef86d7227e232e4a84`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:16 GMT
ADD alpine-minirootfs-3.20.9-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:16 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:39:49 GMT
ARG version=8.482.08.1
# Wed, 28 Jan 2026 02:39:49 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:39:49 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:39:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:39:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:76eb174b37c3e263a212412822299b58d4098a7f96715f18c7eb6932c98b7efd`  
		Last Modified: Wed, 28 Jan 2026 01:18:21 GMT  
		Size: 3.6 MB (3627864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7874207ab763900d913e9c255284f79e444c83a98e9bd7ded9c44b9713d37a22`  
		Last Modified: Wed, 28 Jan 2026 02:40:03 GMT  
		Size: 100.8 MB (100774860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u482-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ef869cd0ed5a2bc236eef7d9e3972f7cd8c958312964bcbf1f93e62be781685e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.4 KB (254380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4d31896e04d6a02b6ec888c115b4f858368eea922ea739bf7a6503e9b7048d2`

```dockerfile
```

-	Layers:
	-	`sha256:3c5a54ad7718fb617115917c86aacd9ead7cf66f055d80bcb9ea362d9a5d4917`  
		Last Modified: Wed, 28 Jan 2026 02:40:00 GMT  
		Size: 245.0 KB (245026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9523450b0fcbf3a9fbec59c0defd18517600d31175ee9a821723c8ff0306c8`  
		Last Modified: Wed, 28 Jan 2026 02:40:00 GMT  
		Size: 9.4 KB (9354 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u482-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4b4574900602c27adcf6b7fd521b67f47ee37fd4076f3a2c56a0be2861f99dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104650311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e409deb02b979efcf71f7457abc419414213246c908c3b0bd6dd0612bfde90`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 18:59:02 GMT
ARG version=8.482.08.1
# Wed, 21 Jan 2026 18:59:02 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 18:59:02 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 18:59:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Wed, 08 Oct 2025 12:02:47 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e303e62d151868a1a26bbbc5ca1e304b961e725c56b7582b63bd2f42b23a34a`  
		Last Modified: Wed, 21 Jan 2026 18:59:17 GMT  
		Size: 100.6 MB (100560934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u482-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:dfa403c30dc47c5fece4c6e59af8c2644fa5045b0dd77abe4811efaad87575d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.6 KB (254616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e0fd571c8f7b579b59c540efe21cc56167f7c0d47234ffbf342d6d415cd8d1f`

```dockerfile
```

-	Layers:
	-	`sha256:7c6640f2da9252c103a09527ad8de29decb6d83c11bab87c459e104016221969`  
		Last Modified: Wed, 21 Jan 2026 18:59:15 GMT  
		Size: 245.2 KB (245158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d02c1b98fb36243c0410ab7072c346683d265aeafbad96f4be9e5f9124fa7e3`  
		Last Modified: Wed, 21 Jan 2026 18:59:15 GMT  
		Size: 9.5 KB (9458 bytes)  
		MIME: application/vnd.in-toto+json
