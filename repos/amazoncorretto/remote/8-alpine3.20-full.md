## `amazoncorretto:8-alpine3.20-full`

```console
$ docker pull amazoncorretto@sha256:75360df56df567b3c0aa8bcabeaf75c4fd150a1cad66cc813f4a88ea6a4bf9d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.20-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:dd81ca7a4b40faebbb0e2191b3947affc92f88adab1a179253493af804aa787c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104401931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e2c744f91df34a1f110aad9ee02bf88ca4de9436c36ec9017d6a251547590e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 18:58:57 GMT
ARG version=8.482.08.1
# Wed, 21 Jan 2026 18:58:57 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 18:58:57 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:58:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 18:58:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:02:45 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69ce6c0855cc24361965329f869cf2c9df9638642de4273bf317d489ec2e980`  
		Last Modified: Wed, 21 Jan 2026 18:59:10 GMT  
		Size: 100.8 MB (100774875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:71310104a4ced80a702067abe4b9496aac8062d5ae3943e66b5df55a4ecdf81a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.4 KB (254380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15929182bc2dece999a3a3162bb8836572308c5787e7cba1db8a8472d3f7202`

```dockerfile
```

-	Layers:
	-	`sha256:f28d334e94a48913121e44eaf103d6b6f7d0947f51303c2a065956f2ff981ba4`  
		Last Modified: Wed, 21 Jan 2026 18:59:08 GMT  
		Size: 245.0 KB (245026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d839975da407e357e3601172a286a040f0e30bef09a82a22d5c9a69c40e59746`  
		Last Modified: Wed, 21 Jan 2026 19:55:36 GMT  
		Size: 9.4 KB (9354 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.20-full` - linux; arm64 variant v8

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
		Last Modified: Sun, 07 Dec 2025 13:54:57 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e303e62d151868a1a26bbbc5ca1e304b961e725c56b7582b63bd2f42b23a34a`  
		Last Modified: Wed, 21 Jan 2026 19:14:27 GMT  
		Size: 100.6 MB (100560934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20-full` - unknown; unknown

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
